PRELOADER FEATURE





In the head, just paste this

```
    <style>
      /* Fullscreen Loader */
      #global-loader {
        position: fixed;
        inset: 0;
        background: #fff;
        display: flex;
        justify-content: center;
        align-items: center;
        z-index: 9999;
      }
      #global-loader .icon {
        height: 80px;
        width: 80px;
        background: #1877f2;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 48px;
        color: #fff;
        font-weight: bold;
        font-family: Arial;
      }
    </style>
```


 In the body, just paste this

 ```
    <!-- Loader will appear instantly before React loads -->
    <div id="global-loader">
      <div class="icon">f</div>
    </div>

   

```

main.jsx 
```
const loader = document.getElementById("global-loader");
if (loader) {
  loader.style.opacity = "0";
  loader.style.transition = "opacity 0.3s ease";
  setTimeout(() => loader.remove(), 300);
}

