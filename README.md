<template>
<div>
    <form v-on:submit="Add">
        <input style="margin-top: 4%; margin-left: 1%;" v-model="inputz"  placeholder="type a Tasks" type="text">
        <md-button style="margin-top: 3%;  min-width: 8%; margin-left: 0%;  background-color: #777d5c24;" class="md-dense md-primary" type="submit">Add</md-button>
    </form>
    <ol>
        <li v-for="(f,index) in fodo"> <input type="radio"  v-on:click="DoneItem(index)" onClick="return confirm('are you sure?');">{{f}}
        </li>
    </ol>

</div>
</template>

<script>
export default {

    data() {
        return {

            fodo: [],
            inputz: '',

        

        }
        //
        //<button  value="click" v-on:click="DoneItem(index) "onClick="return confirm('are you sure?');">Done</button>
    },
    methods: {
        Add: function () {
            this.fodo.push(this.inputz);

        },
        DoneItem: function (index) {
            this.fodo.splice(index, 1, );
            //  this.fodo.push(' the task is completed')

            this.fodo.push(this.inputz + ' task is completed')
          
        },
       

    }

}
</script>
