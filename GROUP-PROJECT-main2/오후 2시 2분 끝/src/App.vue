<template>
    <div class="container">
        <Header />
        <router-view v-bind="routerViewProps" />
        <Loading v-if="states.isLoading" />
    </div>
</template>

<script setup>
import { reactive, provide, computed, onMounted } from 'vue';
import { useRoute } from 'vue-router';
import Header from '@/components/Header.vue';
import Loading from '@/components/Loading.vue';
import axios from 'axios';

const owner = 'hong';
const BASEURI = '/api/todolist_long';

const states = reactive({
    todoList: [],
    isLoading: false,
});

const addTodo = async ({ todo, desc }, successCallback) => {
    states.isLoading = true;
    try {
        const payload = { todo, desc };
        const response = await axios.post(BASEURI + `/${owner}`, payload);
        if (response.data.status === 'success') {
            states.todoList.push({
                id: response.data.item.id,
                todo,
                desc,
                done: false,
            });
            successCallback();
        } else {
            alert('Todo 추가 실패 : ' + response.data.message);
        }
    } catch (error) {
        alert('에러발생 :' + error);
    }
    states.isLoading = false;
};

const updateTodo = async ({ id, todo, desc, done }, successCallback) => {
    states.isLoading = true;
    try {
        const payload = { todo, desc, done };
        const response = await axios.put(BASEURI + `/${owner}/${id}`, payload);
        if (response.data.status === 'success') {
            let index = states.todoList.findIndex((todo) => todo.id === id);
            states.todoList[index] = { id, todo, desc, done };
            successCallback();
        } else {
            alert('Todo 변경 실패 : ' + response.data.message);
        }
    } catch (error) {
        alert('에러발생 :' + error);
    }
    states.isLoading = false;
};

const deleteTodo = async (id) => {
    states.isLoading = true;
    try {
        const response = await axios.delete(BASEURI + `/${owner}/${id}`);
        if (response.data.status === 'success') {
            let index = states.todoList.findIndex((todo) => todo.id === id);
            states.todoList.splice(index, 1);
        } else {
            alert('Todo 삭제 실패 : ' + response.data.message);
        }
    } catch (error) {
        alert('에러발생 :' + error);
    }
    states.isLoading = false;
};

provide(
    'todoList',
    computed(() => states.todoList)
);
provide('actions', { addTodo, deleteTodo, updateTodo });

const route = useRoute();
const transactions = reactive({ users: [], expenditures: [] });

const updateTransactions = (date, transaction) => {
    const category = transaction.type === 'income' ? 'users' : 'expenditures';
    transactions[category].push(transaction);
};

provide('transactions', transactions);
provide('updateTransactions', updateTransactions);

const routerViewProps = computed(() => {
    if (route.meta.needsTransactions) {
        return {
            transactions: transactions || {},
            'onUpdate-transactions': updateTransactions,
        };
    }
    return {};
});

onMounted(async () => {
    try {
        states.isLoading = true;
        const [usersResponse, expendituresResponse] = await Promise.all([axios.get('http://localhost:3000/users'), axios.get('http://localhost:3000/expenditures')]);
        transactions.users = usersResponse.data;
        transactions.expenditures = expendituresResponse.data;
    } catch (error) {
        console.error('Error loading transactions:', error);
    } finally {
        // 2초 후에 isLoading을 false로 설정하여 loading 사진을 2초 동안 표시합니다.
        setTimeout(() => {
            states.isLoading = false;
        }, 1000);
    }
});
</script>

<style>
#app {
    font-family: 'Pretendard Variable', Pretendard, -apple-system, BlinkMacSystemFont, system-ui, Roboto, 'Helvetica Neue', 'Segoe UI', 'Apple SD Gothic Neo', 'Noto Sans KR',
        'Malgun Gothic', 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #967e76;
}
.content-wrapper {
    display: flex;
    justify-content: center; /* 가운데 정렬 */
    align-items: center; /* 수직 정렬 */
    min-height: 100vh; /* 화면 전체 높이 사용 */
}
</style>
