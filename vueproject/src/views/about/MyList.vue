<template>
    <a-table :columns="columns" :data-source="data">
        <a slot="name" slot-scope="text">{{ text }}</a>
    </a-table>
</template>
<script>
    import axios from "axios";

    const columns = [
        {
        title: 'ID',
        dataIndex: 'id',
        key: 'id',
        scopedSlots: { customRender: 'name' },
        },

        {
            title: 'Name',
            dataIndex: 'name',
            key: 'name',
            scopedSlots: { customRender: 'name' },
        },
        {
            title: 'password',
            dataIndex: 'password',
            key: 'password',
            width: 80,
        },
        {
            title: 'email',
            dataIndex: 'email',
            key: 'email',
            ellipsis: true,
        },

    ];

    const data=[

        {
            key: '',
            id: '',
            name: '',
            password: '',
            email: '',
        },{},{},{},{},

    ]

    export default {
        data() {
            return {
                data,
                columns,
            };
        },
        mounted() {
            const _that = this
            axios.get('http://localhost:8084/user/getuser', {
                headers: {}
            }).then((res) => {

                for(var i=0;i<res.data.length;i++) {
                    _that.data[i].key = i+1
                    _that.data[i].id = res.data[i].id
                    _that.data[i].name = res.data[i].userName
                    _that.data[i].password = res.data[i].userPassword
                    _that.data[i].email = res.data[i].realName
                }



            })
        }
    }
</script>
