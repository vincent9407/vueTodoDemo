new Vue({
    el : '#app',
    data : {
        newTodo : '',
        todos : [
            { text : 'Add Some Todos' }
        ]
    },
    methods : {
        addTodo : function(){
            var text = this.newTodo.trim()
            if(text){
                this.todos.push({ text : text })
                this.newTodo = ''
            }
        },
        removeTodo: function (index) {
            console.log(index);
            this.todos.splice(index, 1)
        }
    }
});