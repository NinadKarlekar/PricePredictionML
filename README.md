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


    



