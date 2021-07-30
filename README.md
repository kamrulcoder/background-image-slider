# [background Image slider  vinilla javascript project](https://kamrulcoder.github.io/background-image-slider/) 

## This project is very simple and straightforward. but I can learn something through this project. 

>
>>  That's what  I am learning javascript new sysntax or code here ..............

1. **foreach Loop **
1. **classList Contains **


> 
>> ## Project Code here ....

### Html code 

```
    <div class="slider-area">
        <div class="container">
            <div class="row">
                <div class="col-lg-8 offset-lg-2">
                    <div class="background-wrapper  ">
                        <div class="background">

                        </div>
                        <div class="arrow-btns">
                            <button class="btn btn-danger  prev ">Prev </button>
                            <button class="btn btn-success next">Next </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
```

###  Javascript Code Here 

```
        let btn = document.querySelectorAll(".btn");
        let background = document.querySelector(".background");
        let count = 0;
        let pictures = [
            'contBcg-0',
            'contBcg-1',
            'contBcg-2',
            'contBcg-3',
            'contBcg-4'
        ];

        btn.forEach(buttons => {
            buttons.addEventListener("click", function () {
                if (buttons.classList.contains("prev")) {
                    count--;
                    if (count < 0) {
                        count = pictures.length - 1;
                    }

                    background.style.background = `url('./img/${pictures[count]}.jpeg')`

                }

                if (buttons.classList.contains("next")) {
                    count++;
                    if (count > pictures.length - 1) {
                        count = 0;

                    }
                    background.style.background = `url('./img/${pictures[count]}.jpeg')`
                }
            })
        });
```
