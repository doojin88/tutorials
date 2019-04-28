

# Anaconda 사용법



## 1. 자주 사용하는 프로그램

- basic
  - anaconda
  - python / pip / conda
  - jupyter notebook
  - pycharm
- packages
  - pandas
  - numpy
  - matplotlib
- learning
  - scikit-learn
  - tensorflow
  - keras
- text
  - nltk
  - konlpy
  - pattern



# 2. anaconda 설치



- 링크 : https://www.anaconda.com/distribution/
  - ![image](anaconda1.png)



# 3. conda 명령어

- conda -V
- conda up-to-date
  - conda update conda
  - conda update anaconda3
- env  생성
  - conda env list
  - conda create —name py36 python=3.6
  - conda activate py36
    - source activate py36
  - conda deactivate
- env package 설치
  - pip —version
  - pip install -U pip
  - pip show pandas
  - pip install pandas
  - pip install ipython
  - pip install tensorflow
  - pip install keras
  - Cf) conda 를 활용하는 경우
    - conda install -n py37 pandas
- 참고
  - https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html



# 4. jupyter notebook



####  1) jupyter notebook 설치 및 실행

- Command

  - ```bash
    $ conda activate py36
    $ pip install jupyter
    $ pip install ipython
    $ jupyter notebook
    ```



#### 2) jupyter notebook kernel 관리

- 준비

  - ```bash
    $ conda activate py36
    $ pip install -U pip
    $ pip install jupyter
    $ pip install ipykernel
    ```

- jupyter kernel `py36` 추가  : 

  - ```bash
    $ jupyter kernelspec list
    $ python -m ipykernel install --user --name py36 --display-name "Python (py37)"
    ```

- jupyter kernel 삭제

  - ```bash
  $ jupyter kernelspec
    $ jupyter kernelspec list
    $ jupyter kernelspec uninstall <NAME>
    ```



# 5. anaconda 에서 gpu 사용

참고 : 

- https://www.anaconda.com/getting-started-with-gpu-computing-in-anaconda/

- https://docs.anaconda.com/anaconda/user-guide/tasks/gpu-packages/

- https://www.tensorflow.org/guide/using_gpu

- https://stackoverflow.com/questions/38009682/how-to-tell-if-tensorflow-is-using-gpu-acceleration-from-inside-python-shell

  - ```
    import tensorflow as tf
    
    tf.test.is_gpu_available()  
    
    with tf.Session() as sess:
      devices = sess.list_devices()
    
    display(devices)
    ```

    

