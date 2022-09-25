<template>
    <v-card>
        <v-card-item>
            <v-row align="center">
                <v-col
                    cols="6"
                >
                    <v-row  align="center">
                        <v-col
                            cols="2"
                        >
                            <v-avatar
                                size="35"
                                rounded="0"
                            >
                                <v-img 
                                    src="data:image/png;base64,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" 
                                    lazy-src="data:image/png;base64,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"
                                    ></v-img>
                            </v-avatar>
                        </v-col>
                        <v-col
                            cols="10"
                        >
                            <p class="text-subtitle-1 text-yellow-lighten-1 ml-2">User Name</p>
                        </v-col>
                    </v-row>
                </v-col>
                <v-col
                    cols="6"
                >
                    <v-row  align="center">
                        <v-col
                            cols="2"
                        >
                            <v-avatar
                                size="35"
                                rounded="0"
                            >
                                <v-img 
                                    src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAUCAYAAACXtf2DAAAACXBIWXMAAAsTAAALEwEAmpwYAAADoUlEQVQ4jaWVfWhWZRjGf+ec13e6NtyHw0xRK9NW9jZcTJzOiUStjD4QRUVyk6aUlVqIEBGEqJQfSaXhB2wmYS1iQf+ZMJHlcJuDORmW4itO0mRzsnTzPc9z309/bK+54dzEGy44z7lurt9zP5wPDwh4iLpSu+7JMZmpLc7RGL/c+da0ku867vb94YTU/1yaPpgnYkXVRp2zhZPHpze1HVsz8YEAN0+t2xh7Kut8V8PaxffyJxR/ezF+qeNRtbbOiR2fk5FSW1O5JDXpR+4X3lW/Zr2PbFYRfNzzQFXSa//j3diolMgmK/rr6Jm7K4CiW40fNHkesYLpOYeBN+47wY26Vet9ZJuKQcVgbdjVf3R51qlZEHiy/0bdqo8B4pevv6RixKlZ0F5bXgQQ+X7z/Oi8Fx57QtUZByribHZGytIA2eJE7gQ60X4byJq973BnbdnYSOBvD+CL9uOlzWPmVh7trC37NBL4W6M+W4Ai//WiCbWjU/0zmWnBn1lpwbmc0ZHzvpMtag39ZQG48vuyZ9prlq8GyJxTsStMhJ+oNYzw9FDfvW1qDU7MLADfqZmRPIY+BQPWSSlASsR9Fniy+3rN0hMA2fMOfaliLqqYnKtHFhcDiDUnVUzvUaqY64MEDpQP0N1ze6uKueDUFPxzZOF6gDAM96sYAl9eAxAJ6/8H2JDhCmDCq9XN3bd6lqsN8dQsArBhokVtiLPm8d512JHsjyRJQ5WKu3PtIXkqinN0ATg1I1V81LneVGd8Fa8PYMNhvc0qzgFcqp7/ToDZoxZCo9sBPGdeVOthxbUAqA0n4iUBYjIeBOA5m6cC6tg0aeHxo3s35EZRW6pAZ5f5qbfZzks+1BFrzQ4PCgEDKGA9j2JgxACAD/DVj/G1b5eM3ZG3sjEO8EpBRrWKiTrHsdiKugsN+/LHqZjJgAWITFpUt3Hgbs8enBEbleKfAEbeBQBgZ1Wb7Kxqi5/cExs3NjP6gxMz18HttmuJJQA56d43ag3qOAiDfCqeXtF0ursnUejE9Dgx9Klfb3YaL6NmrhPzb3dPYvacD1va/6qMlaDmTSeGax3dnw8KAMgtazl9szsxS8UkVAw4+0i/KS/d/CUMw7KrHT3P5Za1NLceyM2P+PY3FYMJww0z32/9G8BjiB/Omb1T8qMjvI9C43ZOX33+1L16zh6Y8l4k8L4GUEfV1JXnliW9IQFDVcOuSVMz0vzWvvCKaeXx8rv9hwYMVf8BGBBZZ6GNbZIAAAAASUVORK5CYII=" 
                                    lazy-src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAUCAYAAACXtf2DAAAACXBIWXMAAAsTAAALEwEAmpwYAAADoUlEQVQ4jaWVfWhWZRjGf+ec13e6NtyHw0xRK9NW9jZcTJzOiUStjD4QRUVyk6aUlVqIEBGEqJQfSaXhB2wmYS1iQf+ZMJHlcJuDORmW4itO0mRzsnTzPc9z309/bK+54dzEGy44z7lurt9zP5wPDwh4iLpSu+7JMZmpLc7RGL/c+da0ku867vb94YTU/1yaPpgnYkXVRp2zhZPHpze1HVsz8YEAN0+t2xh7Kut8V8PaxffyJxR/ezF+qeNRtbbOiR2fk5FSW1O5JDXpR+4X3lW/Zr2PbFYRfNzzQFXSa//j3diolMgmK/rr6Jm7K4CiW40fNHkesYLpOYeBN+47wY26Vet9ZJuKQcVgbdjVf3R51qlZEHiy/0bdqo8B4pevv6RixKlZ0F5bXgQQ+X7z/Oi8Fx57QtUZByribHZGytIA2eJE7gQ60X4byJq973BnbdnYSOBvD+CL9uOlzWPmVh7trC37NBL4W6M+W4Ai//WiCbWjU/0zmWnBn1lpwbmc0ZHzvpMtag39ZQG48vuyZ9prlq8GyJxTsStMhJ+oNYzw9FDfvW1qDU7MLADfqZmRPIY+BQPWSSlASsR9Fniy+3rN0hMA2fMOfaliLqqYnKtHFhcDiDUnVUzvUaqY64MEDpQP0N1ze6uKueDUFPxzZOF6gDAM96sYAl9eAxAJ6/8H2JDhCmDCq9XN3bd6lqsN8dQsArBhokVtiLPm8d512JHsjyRJQ5WKu3PtIXkqinN0ATg1I1V81LneVGd8Fa8PYMNhvc0qzgFcqp7/ToDZoxZCo9sBPGdeVOthxbUAqA0n4iUBYjIeBOA5m6cC6tg0aeHxo3s35EZRW6pAZ5f5qbfZzks+1BFrzQ4PCgEDKGA9j2JgxACAD/DVj/G1b5eM3ZG3sjEO8EpBRrWKiTrHsdiKugsN+/LHqZjJgAWITFpUt3Hgbs8enBEbleKfAEbeBQBgZ1Wb7Kxqi5/cExs3NjP6gxMz18HttmuJJQA56d43ag3qOAiDfCqeXtF0ursnUejE9Dgx9Klfb3YaL6NmrhPzb3dPYvacD1va/6qMlaDmTSeGax3dnw8KAMgtazl9szsxS8UkVAw4+0i/KS/d/CUMw7KrHT3P5Za1NLceyM2P+PY3FYMJww0z32/9G8BjiB/Omb1T8qMjvI9C43ZOX33+1L16zh6Y8l4k8L4GUEfV1JXnliW9IQFDVcOuSVMz0vzWvvCKaeXx8rv9hwYMVf8BGBBZZ6GNbZIAAAAASUVORK5CYII="
                                    ></v-img>
                            </v-avatar>
                        </v-col>
                        <v-col
                            cols="10"
                        >
                            <p class="text-caption text-grey font-weight-thin font-italic ml-2">Dragon Boat Festival holiday!holiday!</p>
                        </v-col>
                    </v-row>
                </v-col>
            </v-row>
        </v-card-item>
    </v-card>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
    setup() {
        
    },
})
</script>
