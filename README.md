# Shopping App Portal

#### Authentication Module

- [x] Login
authAPI.login(email, password, role).then(response => {
    return response;
}).catch(err => {
    console.log(err.message);
    throw err;
});

#### Users Module

- [x] Register
userAPI.newUserRegister(userDetails).then(response => {
    console.log(response);
}).catch(err => {
    throw err;
});
- [x] Get User Details
userAPI.getUserDetail(userId).then(response => {
    return response
}).catch(err => {
    throw err;
});

#### Products Module
- [x] List All Products
productAPI.getAllProducts().then(response => {
    if (response.data) {
        return response.data;
    } else {
        throw new Error("Not able to fetch product details");
    }
});
- [x] List active products

productAPI.getActiveProducts().then(response => {
    return response;
}); 


- [x] Add Product
productAPI.addNewProduct(productDetails).then(response => {
    console.log("Response");
}).catch(err => {
    console.log(err);
    throw err;
});

- [x] Activate/Inactive Product

productAPI.checkValidProduct(orderId, status).then(response => {
    console.log("Products Status Changed");
}).catch(err => {
    console.log(err.message);
    throw err;
});

- [x] Get Product Details

productOrderAPI.getProduct(14).then(response => {
    console.log(response.data);

}).catch(err => {
    throw new Error("Please enter valid productId");
})

#### Orders Module
- [x] Add Order
productOrderAPI.orderProduct(orderDetails).then(response => {
        console.log("Order Placed");
}).catch(err => {
    console.log(err.message);
    throw err;
});

- [x] List All Orders
productOrderAPI.getAllOrders().then(response => {
    return response.data;
}).catch(err => {
    throw new Error("Not able to fetch the orders");
});
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
- [x] Update order status
productOrderAPI.changeStatus(orderId).then(response => {
    console.log(response);
}).catch(err => {
    throw err;
})
