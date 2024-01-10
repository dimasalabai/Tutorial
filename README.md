
# THIS

1. _this_ обробника події посилається на елемент обробника події
2. _this_ змінюється, коли функція викликається як обробник події (призначається
   обробником події)
3. _this_ змінюється, коли в setTimeout передали першим аргументом назву функції
   (_this_ стане _window_)

---

## THIS в React

==Передача в обробники==

1. Якщо ми потрібно функцію без параметрів _handleClick()_, то оголошуємо метот
   класу як стрілочну функцію -

   ```javascript
   handleClick = () => {
     console.log(this);
   };
   ```

   та передаємо в обробник

   ```javascript
   onClick={this.handleClick}

   ```

2. Якщо потрібно функцію з параметрами _handleClick(idx)_, то оголошуємо метотод
   класу як зазвичай -

   ```javascript
   handleClick (idx) {
     console.log(this);
   };
   ```

   та передаємо в обробник

   ```javascript
   onClick={() => this.handleClick(index)}
   ```
