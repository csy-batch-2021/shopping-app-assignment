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

- [x] Register
var userDetails = { name: "Dharani", email: "dharani@gmail.com", password: "dharani@90" };
userAPI.newUserRegister(userDetails).then(response => {
    console.log(response);
}).catch(err => {
    throw err;
});
- [x] Get User Details
//get all user details 
userAPI.getUsers().then(response => {
    if (response) {
        return response.data;
    } else {
        throw new Error("Not able to fetch the data");
    }
});

//get particular userId based fetch the value
  var userId = 10;
// userAPI.getUserDetail(userId).then(response => {
//     return response
// }).catch(err => {
//     throw err;
// })

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
- [ ] Add Product
- [ ] Activate/Inactive Product
- [ ] Get Product Details

#### Orders Module
- [ ] Add Order
- [ ] List All Orders
- [ ] List my Orders
- [ ] Cancel a Order
- [ ] Update order status
