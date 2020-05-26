# testvc

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn run serve
```

### Compiles and minifies for production
```
yarn run build
```

### Run your tests
```
yarn run test
```

### Lints and fixes files
```
yarn run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

# Test questions

 _   _           _   _       _          _____       _ _           _   _           
| | | |         | | (_)     (_)        /  __ \     | | |         | | (_)          
| | | | ___  ___| |_ _  __ _ _ _ __ ___| /  \/ ___ | | | ___  ___| |_ ___   _____ 
| | | |/ _ \/ __| __| |/ _` | | '__/ _ \ |    / _ \| | |/ _ \/ __| __| \ \ / / _ \
\ \_/ /  __/\__ \ |_| | (_| | | | |  __/ \__/\ (_) | | |  __/ (__| |_| |\ V /  __/
 \___/ \___||___/\__|_|\__,_|_|_|  \___|\____/\___/|_|_|\___|\___|\__|_| \_/ \___|
                                                                                  
                                                                                  
 _____         _           _           _   _____         _                        
|_   _|       | |         (_)         | | |_   _|       | |                       
  | | ___  ___| |__  _ __  _  ___ __ _| |   | | ___  ___| |_                      
  | |/ _ \/ __| '_ \| '_ \| |/ __/ _` | |   | |/ _ \/ __| __|                     
  | |  __/ (__| | | | | | | | (_| (_| | |   | |  __/\__ \ |_                      
  \_/\___|\___|_| |_|_| |_|_|\___\__,_|_|   \_/\___||___/\__|                     
                                                                                  
                                                                                  
______               _   _____          _                                         
|  ___|             | | |  ___|        | |                                        
| |_ _ __ ___  _ __ | |_| |__ _ __   __| |                                        
|  _| '__/ _ \| '_ \| __|  __| '_ \ / _` |                                        
| | | | | (_) | | | | |_| |__| | | | (_| |                                        
\_| |_|  \___/|_| |_|\__\____/_| |_|\__,_|                                        
                                                                                  

## I - Development

Given the products.json that is on this project which represents a response from a getProducts() API call
Please provide a solution for each questions that follows with the stack/framework/language of your choice
Each question is independent from the others.

Comments are appreciated ;-)


1. User is coming from an Off-White promotion offer link, display only the Off-White's products with a reduced price of 10%.

not working very weel but the idea is to filter the item by their brand name, and apply a 10

2. Louis Vuitton doesn't want us to display the name of their brand on our website, could you reverse the name of the brand for each LV product to obfuscate their name ? 

done with conditional rendering

3. I'm a user from UK and I want to see product between 1500€ and 500€, ordered from the cheaper to the most expensive that are shippable to my country.

we should use sort() with the diferent input of the UI to trigger a function that sort the item

4. We want to add labels to display products following this order "Deposited Today", "Deposited Last Week", "Deposited Last Month", how do you handle that ?

I use the timestamp of the deposited and do the differnece with a New Date variable. TH result return tell me with a final switch which is the right label to display on the product

## II - Questions

There are no wrong answers, only good opportunities to learn something new.

1. What metrics are essential in term of Speed ? pages load is king

2. Can you name ways to increase speed (perceived or actual load time) ? make the file smaller by minimize it

3. Could you tell me what are Observables and how they work ? Its able to give a different value throught time while the promise only give a single value

4. You have a bug to fix, you find the file(s) where the bug occurs, the code is a mess, what do you do ? I indent it, reorganize by kind of tehcnologies (css, html, js). Then i try to separate in smaller component

5. What represent FrontEnd to you ? it's the art to bring the virtual world to our eyes

6. What was the last technical challenge you faced and how you do you handle it ? I had to create a dashboard connected with a lot of API. And for me the challenge was t read and manage thousand of complex object to deliver a simple dahsboard with all tha Math done under the hood. 

7. What is the next language/framework/stack you want to learn this year and why ?

typescript, because it's helps a lot the doucmentation of the code

## III - Extra Time

In case you want to have fun 

1. Could you implement the function resolveSudoku() ?
ain't no time