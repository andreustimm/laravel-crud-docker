<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-12">
                <div class="card">
                    <div class="card-header">Deixe um comentário!</div>
                    <div class="card-body">
                        <form-comment v-on:add-comment="addComment"></form-comment>
                        <view-comment v-on:remove-comment="removeComment" v-model="allComments" :allComments="allComments"></view-comment>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import FormComment from "./FormComment";
    import ViewComment from "./ViewComment";

    export default {
        components: {
            FormComment,
            ViewComment
        },
        data() {
            return {
                comments: []
            }
        },
        methods: {
            addComment(comment) {
                this.comments.push(comment);
            },
            removeComment(index) {
                console.log('Index:', index);
                this.comments.splice(index, 1);
            }
        },
        computed: {
            allComments() {
                return this.comments.map(comment => ({
                    ...comment,
                    name: comment.name.trim() === '' ? 'Anônimo' : comment.name
                }));
            }
        }
    }
</script>
