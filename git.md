# Git general commands


**add files to git**
```
git add
```

**commit all changes**
```
git commit -m "<message>"
git commit -am  "<message">
```

**modify ssl parameter**
```
git config --global http.sslVerify true
```

**check all changes for all local commits**
```
git diff origin/master..HEAD
```

**check all local commits**
```
git log origin/master..master
```


# Creating Git tag

**For a lightweight tag: A lightweight tag is a simple pointer to a commit and contains no extra information.**

```
git tag v1.0.0
```
**For an annotated tag (recommended for releases): Annotated tags are stored as full objects in the Git database and include the tagger's name, email, and date, along with a message. This is a best practice for public releases.**

```
git tag -a v1.0.0 -m "Release version 1.0.0"
```

**To push a specific tag:**
```
git push origin v1.0.0
```

**To push all local tags at once:**
```
git push --tags
```
