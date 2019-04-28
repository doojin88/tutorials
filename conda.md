

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









# 3. conda 명령어

- conda -V
- conda up-to-date
  - conda update conda
  - conda update anaconda3
- env  생성
  - conda env list
  - conda create —name py37 python=3.7
  - conda activate py37
    - source activate py37
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



####  1) jupyter notebook 설치





#### 2) jupyter notebook kernel 추가

- conda activate py37

  - conda install pip
  - pip install -U pip

- pip install ipykernel

- jupyter kernel `py37` 추가  : 

- ```
  python -m ipykernel install --user --name py37 --display-name "Python (py37)"
  ```

- 

#### 3) jupyter notebook kernel 삭제

- kernelspec

- 



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

    

