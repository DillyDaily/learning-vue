<template>
  <div class="row">
      <div class="col-sm-12 col-md-6">
          <table class="table table-hover">
              <thead class="thead-default">
                  <tr>
                    <th>Size</th>
                    <th>Price</th>
                    <th>Add to Cart</th>
                  </tr>
              </thead>
              <tbody v-for="item in getMenuItems">
                  <tr>
                    <td><strong>{{ item.name }}</strong></td>
                  </tr>
                  <tr v-for="option in item.options">
                      <td>{{ option.size }}</td>
                      <td>{{ option.price }}</td>
                      <td><button   class="btn btn-sm btn-outline-success" 
                                    type="button"
                                    @click="addToCart( item, option )" >Add</button></td>
                  </tr>
              </tbody>
          </table>
      </div>
      {{ cart }}
  </div>
</template>

<script>
    export default {
        data() {
            return {
                cart: [],
                getMenuItems: {
                    1: {
                        'name': 'Margherita',
                        'description': 'yummm, right',
                        'options': [{
                            'size': 9,
                            'price': 6.95
                        }, {
                            'size': 12,
                            'price': 10.95
                        }]
                    },
                    2: {
                        'name': 'Mt Veggie',
                        'description': 'hippie yummm, right',
                        'options': [{
                            'size': 9,
                            'price': 8.95
                        }, {
                            'size': 12,
                            'price': 12.95
                        }]
                    },
                    3: {
                        'name': 'Mosso Delicioso',
                        'description': 'best tho yummm, right',
                        'options': [{
                            'size': 9,
                            'price': 10.95
                        }, {
                            'size': 12,
                            'price': 14.95
                        }]
                    },

                }
            }
        },
        methods: {
            addToCart(item, option) {
                this.cart.push({
                    name: item.name,
                    price: option.price,
                    size: option.size,
                    quantity: 1
                })
            }
        }
    }
</script>