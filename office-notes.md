- Calling an API from the front end:

    -Each Component has a container file as well.
    
    - Import the corresponding duck file into the container file of that component.

    - And in the connect file, add it to the state and all that s.

    - Example : 

            import {getRetailerOrders} from '../../../store/orders/duck'

            const AdminOrderContainer = connect(
            // Map state to props
            (state) => ({
                retailOrders : state.orders.retailOrders
            }),
            // Map actions to dispatch and props
            {
                getRetailerOrders
            }
            )(AdminOrderComponent)

            export default AdminOrderContainer


    - In the container:

    This is the import from react ---> import React, { PureComponent } from 'react'

     This is the container declaration ---> class AdminOrderComponent extends PureComponent


              componentWillMount() {
                    const { getRetailerOrders } = this.props
                    
                    getRetailerOrders()    <-- The function call sends the request to the server

                    ---and stores the data in the props, with the key mentioned in the container.js         
                }


