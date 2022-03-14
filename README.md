# lab02

## part I

**1-3) Create new repose and add first commit/ Create hello_world.cpp file**

`nano hello_world.cpp`

![This is an image](/pictures/pic-2.png)

**4-5) Add on local repos and commit**

`git add hello_world.cpp`

`git commit -m "meaningful message"`

![This is an image](/pictures/pic-3.png)

**6-9) Change cpp file and push on git/ check history of commit**

![This is an image](/pictures/pic-4.png)

`git commit -am "meaningful message"`

`git push -u origin main`

![This is an image](/pictures/vk1.png)

## part II

**1-4) Create new branch and change cpp file(right code)**

`git checkout -b patch1`

![This is an image](/pictures/pic-6.png)


**5) Create pull-request**

![This is an image](/pictures/vk2.png)

**6-8) Add comment in cpp file**

![This is an image](/pictures/8.png)

![This is an image](/pictures/vk3.png)

**9-12) Merge patch1 and main and delete patch1**

`git merge patch1`

![This is an image](/pictures/pic-7.png)

`git push origin :heads/patch1`

`git pull origin main`

![This is an image](/pictures/pic-9.png)

`git log`

![This is an image](/pictures/pic-10.png)

`git branch -d patch1`

## part III

**1) Create new branch patch2**

`git checkout -b patch2`

![This is an image](/pictures/pic-11.png)

**2-3) Use clanf-format to change our code**

`clang-format -i --style=Mozilla hello_world.cpp`

![This is an image](/pictures/pic-12.png)

![This is an image](/pictures/vk5.png)

**4-8) Add conflicts and solve they**

![This is an image](/pictures/vk6.png)

![This is an image](/pictures/vk7.png)

`git pull origin main`

`git commit`

`git rebase main`

~~Why we don`t use git pull --rebase!?~~

`git push --force main`

![This is an image](/pictures/vk8.png)

**9) Merge last pull-request**

`git merge patch2`

`git branch -d patch2`
