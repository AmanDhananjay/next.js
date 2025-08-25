# next.js
test1
<!DOCTYPE html>
<html>
<head>
    <title>Product Management System - Login</title>
</head>
<body>
    <h2>Login Screen</h2>
    <form action="dashboard.html">
        <label>Username:</label>
        <input type="text" name="username"><br>
        <label>Password:</label>
        <input type="password" name="password"><br>
        <input type="submit" value="Login">
    </form>
</body>
</html>



<!DOCTYPE html>
<html>
<head>
    <title>Product Dashboard</title>
</head>
<body>
    <h2>Product Dashboard</h2>
    <p>Welcome, [User]!</p>
    <p>Total Products: 120</p>
    <p>Active Products: 110</p>
    <p>Out of Stock: 10</p>
    <a href="productlist.html">Go to Product List</a>
</body>
</html>






<!DOCTYPE html>
<html>
<head>
    <title>Product List / Catalog</title>
</head>
<body>
    <h2>Product List / Catalog</h2>
    <table border="1">
        <tr>
            <th>ID</th><th>Name</th><th>Category</th>
            <th>Price</th><th>Stock</th><th>Actions</th>
        </tr>
        <tr>
            <td>001</td><td>Wireless Mouse</td><td>Accessories</td>
            <td>$25.00</td><td>45</td>
            <td>
                <a href="viewproduct.html">View</a> |
                <a href="editproduct.html">Edit</a> |
                <a href="deleteproduct.html">Delete</a>
            </td>
        </tr>
    </table>
    <br>
    <a href="addproduct.html">Add New Product</a>
    <br><br>
    <a href="dashboard.html">Back to Dashboard</a>
</body>
</html>







<!DOCTYPE html>
<html>
<head>
    <title>Add New Product</title>
</head>
<body>
    <h2>Add New Product Screen</h2>
    <form action="productlist.html">
        <label>Product Name:</label>
        <input type="text" name="name"><br>
        <label>Category:</label>
        <input type="text" name="category"><br>
        <label>Price:</label>
        <input type="text" name="price"><br>
        <label>Stock Quantity:</label>
        <input type="number" name="stock"><br>
        <label>Description:</label>
        <input type="text" name="desc"><br>
        <input type="submit" value="Add Product">
    </form>
    <br>
    <a href="productlist.html">Back to List</a>
</body>
</html>





<!DOCTYPE html>
<html>
<head>
    <title>Edit Product</title>
</head>
<body>
    <h2>Edit Product Screen</h2>
    <form action="productlist.html">
        <label>Product Name:</label>
        <input type="text" name="name" value="Wireless Mouse"><br>
        <label>Category:</label>
        <input type="text" name="category" value="Accessories"><br>
        <label>Price:</label>
        <input type="text" name="price" value="$25.00"><br>
        <label>Stock Quantity:</label>
        <input type="number" name="stock" value="45"><br>
        <label>Description:</label>
        <input type="text" name="desc" value="Ergonomic, wireless mouse with USB receiver."><br>
        <input type="submit" value="Update Product">
    </form>
    <br>
    <a href="productlist.html">Back to List</a>
</body>
</html>




<!DOCTYPE html>
<html>
<head>
    <title>Product Details</title>
</head>
<body>
    <h2>Product Details / View Screen</h2>
    <p><b>ID:</b> 001</p>
    <p><b>Name:</b> Wireless Mouse</p>
    <p><b>Category:</b> Accessories</p>
    <p><b>Price:</b> $25.00</p>
    <p><b>Stock Quantity:</b> 45</p>
    <p><b>Description:</b> Ergonomic, wireless mouse with USB receiver.</p>
    <a href="editproduct.html">Edit</a><br>
    <a href="productlist.html">Back to List</a>
</body>
</html>



<!DOCTYPE html>
<html>
<head>
    <title>Search and Filter</title>
</head>
<body>
    <h2>Search and Filter Screen</h2>
    <form action="productlist.html">
        <label>Search Products:</label>
        <input type="text" name="search"><br>
        <label>Category:</label>
        <select name="category">
            <option>All Categories</option>
            <option>Accessories</option>
            <option>Electronics</option>
            <option>Apparel</option>
        </select><br>
        <input type="submit" value="Search">
    </form>
    <br>
    <a href="productlist.html">Back to List</a>
</body>
</html>



<!DOCTYPE html>
<html>
<head>
    <title>Delete Product</title>
</head>
<body>
    <h2>Delete / Archive Product Screen</h2>
    <p>Are you sure you want to delete the product "Wireless Mouse"? This action cannot be undone.</p>
    <form action="productlist.html">
        <input type="submit" value="Yes, Delete">
    </form>
    <br>
    <a href="productlist.html">Cancel</a>
</body>
</html>
