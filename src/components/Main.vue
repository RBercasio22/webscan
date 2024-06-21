<template>
    <div class="container">
    <div class="item-center">
        <div class="option">
        
        </div>
    
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis, repellat. Id facilis odit nesciunt in exercitationem! Aliquid tempore at numquam tenetur nemo blanditiis possimus quas consequuntur cum, reiciendis sint deleniti explicabo quia minus alias, facilis officia obcaecati et corrupti atque. Voluptas, explicabo veritatis obcaecati reprehenderit tenetur optio sunt nostrum, minima dolor sit asperiores dolorem ducimus earum quae eveniet mollitia aliquid dolorum quod ratione sequi ut dicta reiciendis! Odio iste fugiat assumenda totam harum ipsa. Provident, mollitia architecto. Ex possimus sint aliquam delectus. Laboriosam ex nobis et maxime, ducimus voluptatibus modi ut in quo blanditiis eaque tenetur nostrum soluta praesentium quam aperiam repellat! Animi provident repellat earum quod, doloribus at explicabo dolore unde, sed neque quos tempora illo sequi nisi mollitia nam esse rem repellendus. Dolore, odit. Laboriosam nostrum magni iste quod dicta vero repudiandae ipsum, ex dignissimos suscipit nihil dolorum molestias quidem aperiam nisi laudantium. Aut quos perspiciatis ab praesentium!</p>
        
            <h1>Warning: Ensure you have explicit permission from the website owner or administrator before conducting any scanning activities. Unauthorized scanning can be considered illegal and may result in legal action.</h1>
            
            <input type="text" placeholder="Target" v-model="textInput">
            <hr>
            <div class="container">
                <button @click="displayText" class="scan">Scan</button>
                <button class="scan" @click="sentData">Save</button>
                <button @click="clearText" class="scan">Clear</button>
            </div>
            <div class="container">
                <textarea name="text" id="1" v-model="textOutput" disabled></textarea>
            </div>

    </div>
    </div>
    
</template>


<script>

export default {
    name: 'mainPage',
   
    data() {
        return {
            textInput: '',
            textOutput: '',
        }
    },
    methods: {
        clearText() {
            if(this.textInput =='' && this.textOutput ==''){
                alert('Already clear')
            }else {
                this.textInput = '';
                this.textOutput = '';
            }
        },
        displayText() {
            this.textOutput = ''; // Clear previous output
            if(this.textInput === '') {
                alert('No URL!')

            } else {
                for (let i = 0; i < 100; i++) {
                setTimeout(() => {
                this.textOutput += `\nScan => ${this.textInput}`;
                }, (i + 1) * 200); 

                }
            } 
        },
        sentData() {
            alert('Not Availble')
        }

    }

}


</script>


<style scoped>

.container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.item {
  height: 100px;
  width: 100px; /* A fixed width as the default */
}

.item-center { 
  flex-grow: 1; /* Set the middle element to grow and stretch */
}

.item + .item { 
  margin-left: 2%; 
}

h1 {
    margin-top: 40px;
    color: red;
    border-radius: 5px;
    transition: 2s;
}
h1:hover {
    color: green;
}

input {
    outline: none;
    width: 100%;
    height: 30px;
    background-color: transparent;
    border: none;
    font-size: 16px;
    font-weight: bold;
    
}
.scan {
    background-color: rgb(200,0,0);
    color: white;
    height: 50px;
    width: 200px;
    border-radius: 5px;
    border: none;
    transition: 1s;
    text-transform: uppercase;
    font-weight: bold;
}
.scan:hover {
    background-color: rgb(150,0,0);

}

textarea {
    resize: none;
    height: 300px;
    width: 94%;
    border-radius: 5px;
    outline: none;
    
}

.option {
    display: flex;
    justify-content: right;
    align-items: center;
}
p {
    transition: 2s;
}
p:hover {
    color: red;
}
</style>



