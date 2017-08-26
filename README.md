# Seasonal Sales

The Basics of the Project

* Build a web page that lists all of the products, the name of the department it's in, and the price. 
* Create a dropdown menu with the name of each season.
* As soon as you select one of the seasons, all prices on the page should immediately be discounted by the corresponding percentage.

* When Spring is chosen, all products in the corresponding Household category should have their prices updated with a 15% discount off the base price.

* The two JSON representations above should be in two files: products.json, and categories.json. You should load both files via XHRs and store the contents in two different JavaScript variables in your code.

## A Little Bit of Code

```function useForProducts() {

    products = JSON.parse(this.responseText).products;
    products.forEach(function(product) {
        for (var j = 0; j < departments.length; j++) {
            if (product.category_id === departments[j].id) {
                product["catagory_name"] = departments[j].name;
                product["catagory_discount"] = departments[j].discount;
                product["catagory_season_discount"] = departments[j].season_discount;
                product["season_price"] = product.price - (product.price * departments[j].discount)
            }
        }
    });
    productDom("none");
} 
```

![Screen Shot of Project](https://github.com/Matthensley777/seasonalsales/blob/master/images/Screen%20Shot%202017-08-26%20at%209.12.12%20AM.png)


### How To Download

* From Project page click on Clone Download link. 
* Click on Clipboard to copy link.

![Click on clipboard to copy link](https://github.com/Matthensley777/seasonalsales/blob/master/images/Screen%20Shot%202017-08-26%20at%209.36.24%20AM.png)
* From Terminal.
* Type git clone and past in link.
![type git clone, and past link](https://github.com/Matthensley777/seasonalsales/blob/master/images/Screen%20Shot%202017-08-26%20at%209.37.02%20AM.png)