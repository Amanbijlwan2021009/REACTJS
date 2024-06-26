***Concept explained below is in a rough way***

# While writing code , i get to know onething about `onClick` method. 🤔

`onClick` is a very unique method .          

`onClick` expects that you are giving function and we are giving reference down there.    

In App.jsx , If we call `setColor` like this :

```js

 <button className='outline-none text-white bg-red px-4 py-1 rounded-full shadow-lg' style={{ backgroundColor: "red" }} onClick={setColor}>
    Red 
 </button>

```

By this way , we cann't assign value/parameter to setColor .    

To do so , we need to use a function there that can pass a parameter .      

If we do like this :

```js

 <button className='outline-none text-white bg-red px-4 py-1 rounded-full shadow-lg' style={{ backgroundColor: "red" }} onClick={setColor("red")}>
    Red 
 </button>

```
Now here we directly execute setColor , So the return value that function will generate will go to `onClick` .      

And `onClick` needs a function and not its return value.      

**To solve this we can use `Callback function`**

```js

 <button className='outline-none text-white bg-red px-4 py-1 rounded-full shadow-lg' style={{ backgroundColor: "red" }} onClick={() => setColor("red")}>
    Red 
 </button>

```