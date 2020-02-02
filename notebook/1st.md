# PART 1: Machine Learning & PyTorch Basic

Lab-01-1 Tensor Manipulation 1 - 업데이트 : 2020.01.24좋아요10
Lab-01-2 Tensor Manipulation 2 - 업데이트 : 2020.01.20좋아요5
Lab-02 Linear regression - 업데이트 : 2020.01.21좋아요6
Lab-03 Deeper Look at GD - 업데이트 : 2020.01.06좋아요2
Lab-04-1 Multivariable Linear regression - 업데이트 : 2020.01.02좋아요1
Lab-04-2 Loading Data - 업데이트 : 2020.01.28좋아요3

# 들어가기 전에
- docker 세팅 : https://github.com/deeplearningzerotoall/PyTorch/blob/master/docker_user_guide.md

- 옵션 해석
```bash
$ $ docker run -i -t --name pt -p 8888:8888 -p 8097:8097 deeplearningzerotoall/pytorch /bin/bash
```
> exec 명령은 도커 컨테이너 안쪽에 명령어를 전송할때 사용한다.
이 때, 명령어를 /bin/bash 로 주게되면 도커 컨테이너 안쪽의 bash 쉘이 실행된다.
접속이란게 결국 리눅스의 쉘을 사용하겠다는 뜻이기 때문에, 이런 방식으로 컨테이너에 접속한다.

> 참고로 -i 옵션은 표준 입출력을 사용하겠다는 의미로,
-t 옵션만 주게되면 root@134adb2ba12:~/$ 와 같이 프롬프트 모양이 바뀌긴 한다.
하지만 표준 입출력 옵션을 주지 않았으므로 입력을해도 아무런 반응이 없다.

> 또한 -t 옵션은 가상 tty를 통해 접속하겠다는 의미로,
-i 옵션만 주게되면 root@134adb2ba12:~/$ 부분이 뜨지 않는다.

0b9f3abea81315c89259a10c0c2c7b3495ae2db87b1ba131


# Lab-01-1 Tensor Manipulation 1

>
> ## 학습목표
> - 텐서 조작(Tensor Manipulation)에 대해 알아본다.
>
> ## 핵심키워드
> - 텐서(Tensor)
> - 넘파이(NumPy)
> - 텐서 조작(Tensor Manipulation)
> - 브로드캐스팅(Broadcasting)


- pytorch 는 numpi보다 유사하거나 더 나은 기능을 제공함
- pytorch가 tensor를 어떻게 조작하는지 알아보자.

- 1D : Vector
- 2D : Matrix - 행렬
- 3D : Tensor
- 4D : Tensor 에서 위로 쌓아 올린 형태.
- 5D : 4D를 옆으로 확장.
- 6D : 5D를 뒤로 확장



Q) 1D, 2D, 3D 의 dimension 이랑, 텐서를 구성하는 dimension이랑은 다른 개념인가요?
