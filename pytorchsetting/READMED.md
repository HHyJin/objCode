![**LOGO pytorch**](https://github.com/pytorch/pytorch/blob/master/docs/source/_static/img/pytorch-logo-dark.png)
--------------------------------------------------------------------------------
파이토치는 파이썬 패키지로 두가지 특징을 가진다.
- GPU로 Tesnor(Numpy처럼)를 다룰 수 있음
- 미분을 자동화를 기초로한 Deep Neural Networks이다
또한 PyTorch를 Extend하기 위해 Numpy와 같은 package들을 써도 된다.

## PyTorch important abstract
| Component | Description |
| ---- | --- |
| [**torch**](https://pytorch.org/docs/stable/torch.html) | Tensr lib로 GPU사용 |
| [**torch.autograd**](https://pytorch.org/docs/stable/autograd.html) | 미분쓰는 곳 |
| [**torch.jit**](https://pytorch.org/docs/stable/jit.html) | a compilation stack (TorchScript) to create serializable and optimizable models from PyTorch code  |
| [**torch.nn**](https://pytorch.org/docs/stable/nn.html) | a neural networks library deeply integrated with autograd designed for maximum flexibility |
| [**torch.multiprocessing**](https://pytorch.org/docs/stable/multiprocessing.html) | Python multiprocessing, but with magical memory sharing of torch Tensors across processes. Useful for data loading and Hogwild training |
| [**torch.utils**](https://pytorch.org/docs/stable/data.html) | DataLoader and other utility functions for convenience |

## Anaconda PyTorch setting
- Anaconda 홈페이지에서 version python=3.7 설치
- Anaconda prompt로 들어가서 가상환경 만들기 or Anaconda Navigator이용
``` linux
conda create -n condatest python=3.7 anaconda
conda info --envs (conda)
activate condatest
deactivate
```
- 가상환경 이름 : condatest
- 참고 : [**anaconda**](https://daily-error.tistory.com/14)

## VScode Setting
- VScode 알아서 다운
- C:\Users\"사용자이름"\Anaconda3\envs\condatest 폴더 Add to workspace
- ctrl+shift+p(vscode 명령창 열고)
- Pyhthon select workspace interpreter 검색 후 anaconda folder(workspace)선택
- interpreter는 아무거나 선택,`
- condatest(env)안에 .vscode가 생성이 되면 `settings.json으로 들어감
- pythonpath 경로를 C:\\Users\\"사용자 이름"\\Anaconda3\\envs\\condatest\\Scripts\\python.exe로 변경(역슬래쉬 2개 명심)
- VScode->File->Prefer->Settings-> settings.json 검색
- json file 변경 
``` linux
 "python.pythonPath": "C:/Users/Kweon/Anaconda3/envs/HJ/python.exe",
 "terminal.integrated.shellArgs.windows": ["/K", "C:/Users/Kweon/Anaconda3/envs/condatest/Scripts/activate.bat C:/Users/Kweon/Anaconda3/envs/condatest"], 
```
- 여기서 연결이 안되면 시스템환경변수에 내가 만든 env/,ripts를 추가해 주어야 함, 통합터미널은 cmd임
- 이제부터 가상환경을 여러개로 만들고 vscode에 연결하여 환경마다 다른 interpreter를 쓸수 있음

