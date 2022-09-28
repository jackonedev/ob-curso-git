# Clase 7

## Git flow sin flow

> git init .<br />
git checkout -b develop<br />
git checkout -b feature/feature_login: creo login.php<br />
git add index.php<br />
git commit -m "version inicial"<br />
git checkout main/develop<br />
#git branch -a???<br />
git merge feature/feature_login<br />
<>

## release start

> git checkout develop<br />
git checkout -b release/0.1: realizo cambios

> git checkout main<br />
git merge release/0.1


## hotfix

> git checkout main<br />
git checkout -b hotfix_1<br />
git checkout main<br />
git merge hotfix_1<br />
git checkout develop<br />
git merge hotfix_1<br />
git branch -D hotfix_1<br />
