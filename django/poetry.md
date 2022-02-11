## poetry

**python dependency manager**

Dependency manager는 프로젝트에 대한 모든 dependency를 관리하고 이러한 dependency는 프로젝트에 저장됩니다. Package manager가 사용하고 싶은 package를 관리하는 역할을 한다면, dependency manager는 package가 요구하는 목록(Dependency Tree)을 구성 합니다.

파이썬에는 공식 dependency manager인 `pip`가 있습니다. `pip`와 `virtualenv`의 기능을 동시에 수행하는 `Pipenv`도 있습니다. `pip`는 사용자가 직접 `requriements.txt`를 잘 작성해 dependency 충돌을 피해야합니다.

**Poetry: Dependency and Package manager for Python**

Poetry는 Python 프로젝트의 dependency를 선언, 관리, 설치하여 어디서나 프로젝트가 작동하도록 도와주는 툴입니다.

Pip와는 다르게 `.toml` file과 ‘`.lock'`파일을 생성해 dependency를 관리합니다. 생성된 `.toml` 파일에는 프로젝트 dependency의 **메타데이터**가, `.lock` 파일에는 설치된 패키지들의 **version**, **hash**가 저장되어있습니다.

reference : https://chacha95.github.io/2021-03-27-python7/

설치

```python
$ curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python -
```

삭제(M1)

```python
$ curl -sSL https://raw.githubusercontent.com/sdispater/poetry/master/get-poetry.py | python - --uninstall
```

create poetry project 

```python
$ poetry new <project_name>
```

poetry auto alias

```python
$ git clone https://github.com/darvid/zsh-poetry.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-poetry
$ echo "source ~/.oh-my-zsh/custom/plugins/zsh-poetry/poetry.zsh" >> ${HOME}/.zshrc
```