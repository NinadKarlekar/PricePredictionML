# PricePredictionML
We will understand the problem of a real estate company from its CEO and then apply ML to solve it.

### Software And Tool Requirment

1. [GitHub Account](https://github.com/)
2. [Visual Studio code IDE](https://code.visualstudio.com/download)
3. [Heroku Account](https://www.heroku.com/)
4. [Git CLI](https://git-scm.com/book/en/v2/Getting-Started-The-Command-Line)


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

8. 