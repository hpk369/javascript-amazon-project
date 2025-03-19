# Amazon Clone E-Commerce Web Application

A fully functional e-commerce web application inspired by Amazon, built with vanilla JavaScript, HTML5, and CSS3. This project demonstrates front-end development skills with a focus on creating a responsive, interactive shopping experience.

## Features

- **Product Listings**: Dynamic product grid with detailed information and images
- **Shopping Cart**: Fully functional cart with add, remove, and quantity adjustment capabilities
- **Data Persistence**: Cart items persist between sessions using LocalStorage
- **Responsive Design**: Optimized for both desktop and mobile devices
- **Order Confirmation**: Complete checkout flow with order summaries

## Technologies Used

- **JavaScript ES6+**: Modern JavaScript syntax and features
- **HTML5/CSS3**: Semantic markup and advanced styling
- **DOM Manipulation**: Dynamic content rendering and updates
- **LocalStorage API**: Client-side data persistence
- **CSS Grid/Flexbox**: Responsive layout design
- **Event-Driven Programming**: Handling user interactions

## Project Structure

```
├── data/
│   ├── cart.js          # Shopping cart data management
│   └── products.js      # Product data and information
├── scripts/
│   ├── amazon.js        # Main application logic
│   ├── checkout.js      # Checkout functionality
│   └── utils.js         # Helper functions
├── styles/
│   ├── shared/          # Shared styling components
│   ├── amazon.css       # Main page styling
│   └── checkout.css     # Checkout page styling
├── images/              # Product and UI images
├── index.html           # Main product listing page
└── checkout.html        # Checkout and order confirmation page
```

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)

### Installation

1. Clone the repository:
   ```
   git clone https://github.com/hpk369/javascript-amazon-project.git
   ```

2. Navigate to the project directory:
   ```
   cd javascript-amazon-project
   ```

3. Open `index.html` in your browser to run the application locally.

## Usage Examples

### Adding Products to Cart

```javascript
// Example code from the implementation
function addToCart(productId) {
  let matchingItem;

  cart.forEach((item) => {
    if (productId === item.productId) {
      matchingItem = item;
    }
  });

  if (matchingItem) {
    matchingItem.quantity += 1;
  } else {
    cart.push({
      productId: productId,
      quantity: 1
    });
  }

  saveToStorage();
  updateCartQuantity();
}
```

### Persisting Cart Data

```javascript
// Example code demonstrating LocalStorage usage
function saveToStorage() {
  localStorage.setItem('cart', JSON.stringify(cart));
}

function loadFromStorage() {
  const cartData = localStorage.getItem('cart');
  return cartData ? JSON.parse(cartData) : [];
}
```

## Future Enhancements

- User authentication and account management
- Product search functionality
- Product filtering and sorting options
- Product reviews and ratings
- Payment gateway integration

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Inspired by Amazon's user interface and functionality
- Built as a demonstration of vanilla JavaScript skills without frameworks
- Created for educational purposes to showcase front-end development techniques
