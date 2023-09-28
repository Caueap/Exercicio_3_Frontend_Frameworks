<template>
    <div id="maindiv">
        <div id="input-button-div">
            <input id="maindiv-input" type="text">
            <button id="maindiv-button" @click="generateAnswer">Gerar resposta</button>
        </div>
        <p id="answer-parag">{{ answer }}</p>
    </div>
</template>

<script>
export default {
    name: 'MainDiv',

    data() {
        return {
            answer: ''
        }

    },
    methods: {
        generateAnswer() {
            const answers = [
                'Com certeza',
                'É... não tenho certeza!',
                'Claro que não',
                'Acho difícil',
                'Possivelmente não'
            ];
            const randomIndex = Math.floor(Math.random() * answers.length);

            this.answer = answers[randomIndex];
        }
    }
}

</script>

<style scoped>
#maindiv {
    margin-left: 50px;
    width: 400px;
    height: 200px;
    background-color: #3a5a40;
    display: flex;
    flex-direction: column;
    
    gap: 10px;
   justify-content: center;
}

#input-button-div {
    display: flex;
    
    gap: 10px;
}

#maindiv-input {
    margin-left: 50px;
    height: 25px;
    border-radius: 4px;
    border: none;
}

#maindiv-input:focus {
    box-shadow: 0 0 0 0;
    outline: 0;
}

#maindiv-button {
    height: 29px;
    width: fit-content;
    border-radius: 4px;
    border: none;

}

#question-parag {
    padding: 0px;
    margin-left: 50px;
    color: #fff;
}

#answer-parag {
    padding: 0px;
    margin: 0px 0px 0px 50px;
    color: #fff;
}

</style>