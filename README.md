# Shopping App Portal

#### Authentication Module

- [x] Login
authAPI.login(email, password, role).then(response => {
    return response;

}).catch(err => {
    console.log(err.message);
    throw err

});

#### Users Module

- [ ] Register
- [ ] Get User Details

#### Products Module
- [x] List All Products
  productAPI.getAllProducts().then(response => {
    return response.data;
  });
- [x] List active products
productAPI.getActiveProducts().then(response => {
    return response;
});
- [ ] Add Product
- [x] Activate/Inactive Product
productAPI.checkValidProduct(orderId, status).then(response => {
    console.log("Products Status Changed");
}).catch(err => {
    console.log(err.message);
    throw err;
});
- [ ] Get Product Details

#### Orders Module
- [x] Add Order
productOrderAPI.orderProduct(orderDetails).then(response => {
    // console.log("Order Placed");
}).catch(err => {
    console.log(err.message);
    throw err;
});

- [ ] List All Orders
- [x] List my Orders
productOrderAPI.myOrders(userId).then(response => {
    return response;
}).catch(err => {
    throw err;
});
- [x] Cancel a Order
productOrderAPI.orderCancel(cancelOrderId).then(response => {
    return "Order Cancelled Successfully";

}).catch(err => {
    console.log(err);
    throw err;
});
- [ ] Update order status
