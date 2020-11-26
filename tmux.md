## tmux 구성 요소
- **session** : 여러개의 window로 구성
- **window** : 터미널 화면, session내에서 탭처럼 사용 가능
- **pane** : 하나의 window내에서 화면 분할

## tmux function key
```
ctrl + b # 모드 동작
eg) (ctrl + b) ? # 단축키 목록
```


## session 명령어
```
# new session
tmux new -s "session name"

# session 및 window 같이 생성
tmux new -s "session name" -n "window name"

# session 나가기
exit

# session 목록
tmux ls

# session attach
tmux attach -t "session name"

# session dettach
(ctrl + b) d

# session scroll
ctrl + b + [

# 특정 session 강제 종료
tmux kill-session -t  "session number"
```

## window 명령어
```
# new window
(ctrl + b) c

# window 이동
(ctrl + b) "number"
```

## pane 명령어
```
# pane 좌,우로 나누기
(ctrl + b) %

# pane 위,아래로 나누기
(ctrl + b) "

# pane 이동
(ctrl + b) 방향키

# pane 순서 확인
(ctrl + b) q

# pane 순서대로 이동
(ctrl + b) o

# pane size 조정
(ctrl + b) : # 명령어 모드로 들어간다.
resize-pane -L # 왼쪽 10
            -R # 오른쪽 10
            -D # 아래 10
            -U # 위 10

# pane layout 조정
# 마음에 드는 layout으로 바꿀 수 있다.
(ctrl + b) spacebar
``` 
