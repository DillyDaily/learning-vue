<template>
    <form>
        <h3>Add new pizza: </h3>
        <div class="form-group row">
            <label class="col-sm-3">Name</label>
            <div class="col-sm-9">
                <input type="text" class="form-control" v-model="newPizza.name">
            </div>
        </div>

        <div class="form-group row">
            <label class="col-sm-3">Description</label>
            <div class="col-sm-9">
                <textarea type="text" class="form-control" rows="5" v-model="newPizza.description"></textarea>
            </div>
        </div>

        <p><strong>Option1:</strong></p>
        <div class="form-group row">
            <label class="col-sm-3">Size (")</label>
            <div class="col-sm-9">
                <!-- <input type="text" class="form-control" v-model="newPizza.options[0].size"> -->
            </div>
        </div>

        <div class="form-group row">
            <label class="col-sm-3">Price</label>
            <div class="col-sm-9">
                <!-- <input type="text" class="form-control" v-model="newPizza.options[0].price"> -->
            </div>
        </div>

        <p><strong>Option2:</strong></p>
        <div class="form-group row">
            <label class="col-sm-3">Size (")</label>
            <div class="col-sm-9">
                console.log(newPizza.options[1].size)
                <!-- <input type="text" class="form-control" v-model="newPizza.options[1].size"> -->
            </div>
        </div>
        
        <div class="form-group row">
            <label class="col-sm-3">Price</label>
            <div class="col-sm-9">
                <!-- <input type="text" class="form-control" v-model="newPizza.options[1].price"> -->
            </div>
        </div>

        <div class="form-group row">
            <button class="btn btn-success btn-block" type="button">Add</button>
        </div>

    </form>
</template>

<script>
    export default {
        data() {
            return {
                newPizza: {
                    1: {
                        'name': 'Ex. Margherita',
                        'description': 'Ex. yummm, right',
                        'options': [{
                            'size': 9,
                            'price': 6.95
                        }, {
                            'size': 12,
                            'price': 10.95
                        }]
                    }
                }
            }
        }
}
</script>