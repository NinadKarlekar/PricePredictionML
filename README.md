# PricePredictionML
We will understand the problem of a real estate company from its CEO and then apply ML to solve it.

### Software And Tool Requirment

1. [GitHub Account](https://github.com/)
2. [Visual Studio code IDE](https://code.visualstudio.com/download)
3. [Heroku Account](https://www.heroku.com/)
4. [Git CLI](https://git-scm.com/book/en/v2/Getting-Started-The-Command-Line)
5. [Postman](https://www.postman.com/downloads/)


### Steps

1. Go to ***VS CODE*** and open project folder.

2. Create New environment

    ```
    conda create -p venv python==3.7 -y
    ``` 

3. Activate Environment
    ```
    conda activate venv/
    ```

4. Install Required libraries from [Requirements.txt](/requirements.txt)
    ```
    pip install -r requirements.txt
    ```

5. Cofigure username in git cli
    ```
    git config --global user.name "Ninad Karlekar"
    ```

6. Cofigure email in git cli
    ```
    git config --global user.email "< Write your github account email here >"
    ```

7. Commit and push

    <details>
    <summary>Steps</summary>
    <br>

    1. Add File
        1. Add a **single** file

            ``` 
            git add requirements.txt
            ```

        2. Add **all** files

            ```
            git add .
            ```

    2. To see **status**
        ```
        git status
        ```

    3. To **commit** with message
        ```
        git commit -m "Write message here"
        ```

    4. To **push** changes
        ```
        git push origin main
        ```

    </details>
    <br>

8. Create and run [app.py](/app.py)

    ```
    python app.py
    ```

9. Test with POSTMAN

    <details>
    <summary>Steps POSTMAN</summary>
    <br>

    1. Download and open [Postman](https://www.postman.com/downloads/)

    2. Change method from get to post

    3. Paste the following link
    ```
    http://127.0.0.1:5000/predict_api
    ```

    4. open dropdown and change to ***RAW*** and ***JSON***
    
    ![p1](https://user-images.githubusercontent.com/88243315/219637062-869ef1ad-a057-4b98-bc5d-37ab5eb2741c.png)


    5. Paste following code and click on **send**

    ```json
    {
    "data": {
        "CRIM": 0.00632,
        "ZN":18.0,
        "INDUS":2.31,
        "CHAS":0.0,
        "NOX":0.538,
        "RM":6.575,
        "AGE":65.2,
        "DIS":4.0900,
        "RAD":1.0,
        "TAX":296,
        "PTRATIO":15.3,
        "B":396.90,
        "LSTAT":4.98
        }
    }
    ```

    6. The prediction value should be visible
    
    ![p2](https://user-images.githubusercontent.com/88243315/219636981-69217d0c-ce94-4cae-853a-69276414f9a0.png)

10. Create a simple Html form

    <details>
    <summary>Code</summary>
       <br>

    ```html
    <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Real Estate prediction</title>
        </head>
        <body>
            <div class="login">
                <h1>Real Estate prediction</h1>

                <form action="{{ url_for('predict')}}" method="post">
                    <input type="text" name="CRIM" placeholder="CRIM" required="required"/><br>
                    <input type="text" name="ZN" placeholder="ZN" required="required"/><br>
                    <input type="text" name="INDUS" placeholder="INDUS" required="required"/><br>
                    <input type="text" name="CHAS" placeholder="CHAS" required="required"/><br>
                    <input type="text" name="NOX" placeholder="NOX" required="required"/><br>
                    <input type="text" name="RM" placeholder="RM" required="required"/><br>
                    <input type="text" name="AGE" placeholder="AGE" required="required"/><br>
                    <input type="text" name="DIS" placeholder="DIS" required="required"/><br>
                    <input type="text" name="RAD" placeholder="RAD" required="required"/><br>
                    <input type="text" name="TAX" placeholder="TAX" required="required"/><br>
                    <input type="text" name="PTRATIO" placeholder="PTRATIO" required="required"/><br>
                    <input type="text" name="B" placeholder="B" required="required"/><br>
                    <input type="text" name="LSTAT" placeholder="LSTAT" required="required"/><br> 

                    <button type="submit" class="btn btn-primary btn-block btn-large">predict</button><br><br>


                </form>
            </div>
        {{prediction_text}}
        </body>
        </html>
    ```

    </details>

11. Run [app.py](/app.py)

    ```
    python app.py
    ```

12. To deploy in Heroku create [***Procfile***](/Procfile)

```
web : gunicorn app:app
```






