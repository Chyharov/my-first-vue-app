# my-first-vue-app

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).

git clone - копіює репозиторій(папку з файлами) на компютер

git add . - зберігає зміни в файлах
git commit -m "commit message" - підписуємо збереженні зміни в файлах
git commit -am "commit message" - одразу дві команди "git add ." + "git commit -m "commit message""
git push - відправляємо зміни на сайт GitHub

git branch - показує список гілок в проєкті
git branch -r - показує список гілок на сайті GitHub
git branch -a - показує список гілок на компютері та на сайті GitHub
git branch "branchName" - створює гілку з назвою "branchName"
git checkout "branchName" - переходить на гілку з назвою "branchName"
git checkout -b "branchName" - сторюємо гілку з назвою "branchName" і переходим в неї
git push --set-upstream origin "branchName" - створює гілку і пушить код у поточну гілку
або
git push -u origin "branchName"
git pull - отримуємо останні зміни з сайту GitHub
git marge "branchName" - зливаеємо гілку з назвою "branchName" в поточну гілку
git merge --abort - відміняємо зливання гілок
git branch -d "branchName" - видаляє гілку локально з проекту
git push origin --delete "branchName" - видаляє гілку на сайті GitHub

git status - показує статус проекту

git fetch - отримуємо зміни з сайту GitHub
git status - зберігаємо не збережені зміни в файлах і кладемо їх в буфер обміну
git stash apply - вставляємо збережені зміни з буферу обміну
