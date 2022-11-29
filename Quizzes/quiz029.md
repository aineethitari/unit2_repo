# Quiz 29

## Code

```.py
def count_letters(my_dict,msg) -> str:
    for i in range(len(msg)):
        if msg[i] in my_dict.keys():
            my_dict[msg[i]] += 1
    return my_dict
```

## Result

<img width="578" alt="Quiz029 results" src="https://user-images.githubusercontent.com/112055062/204425026-e9a24bbc-9d91-4364-b775-198021f619cb.png">

<img width="543" alt="quiz029 result2" src="https://user-images.githubusercontent.com/112055062/204425107-0f163db8-17c7-4cee-a4e5-be2a4dbb463c.png">


