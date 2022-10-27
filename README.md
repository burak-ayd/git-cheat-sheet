# Git Cheat Sheet


### Index
* [Kurulum](#kurulum)
* [Repo Oluşturma](#Repo Oluşturma)
* [Branch Oluşturma](#Branch Oluşturma)
* [Yerel Değişiklikler](#yerel-değişiklikler)
* [Arama](#arama)
* [Commit Geçmişi](#commit-geçmişi)
* [Branches & Tags(Etiketler)](#branches--tags)
* [Güncelleştirme & Yayınlama](#güncelleştirme--yayınlama)
* [Merge(Birleştirme) & Rebase](#merge--rebase)
* [Geri Alma](#geri-alma)
* [Git Flow](#git-flow)

<hr>


## Kurulum

##### Mevcut ayarları göstermek:
```
$ git config --list
```
##### Repository(depo) ayarlarını göstermek:
```
$ git config --local --list
```

##### Global ayarları göstermek:
```
$ git config --global --list
```

##### Sistem ayarlarını göstermek:
```
$ git config --system --list
```

##### Sürüm geçmişinde gözükecek adı belirlemek:
```
$ git config --global user.name “[firstname lastname]”
```

##### Sürüm geçmişinde ilişkilendirilecek e-postayı belirlemek:
```
$ git config --global user.email “[valid-email]”
```

<hr>

## Repo Oluşturma

##### Yerel repo oluşturma:
```
$ git init
```
##### Yerel repo oluşturma:
```
$ git clone repo_url
```
##### Belirli bir dizinde yerel repo oluşturma:
```
$ git clone <dizin
```

## Branch Oluşturma

##### Yerel branch oluşturma:
```
$ git branch <branch-name>
```
##### Yerel branch Github'a göndermek:
```
$ git push -u <remote> <branch-name>
```
##### Branch detayları:
```
$ git branch
```
#### ya da
```
$ git branch --list
```
#### Branch silmek
```
$ git branch -d <branch-name>
```
## Yerel Değişiklikler

##### Çalışılan dizindeki dosyaların değişimi:
```
$ git status
```

##### İzlenen dosyalardaki değişiklikler:
```
$ git diff
```

##### Tüm güncel değişiklikleri sonraki commite ekleme:
```
$ git add .
```

##### Sonraki commite &lt;dosyasındaki&gt; bazı değişikleri ekleme:
```
$ git add -p <file>
```

##### Tüm izlenen dosyalardaki yerel değişiklikleri Commitleme:
```
$ git commit -a
```

##### Önceden hazırlanan değişiklikleri commitleme:
```
$ git commit
```

##### Mesaj ile commitleme:
```
$ git commit -m 'message here'
```

##### Önceki belli bir tarihe commitleme:
```
git commit --date="`date --date='n day ago'`" -am "Commit Message"
```
<hr>

## Commit Geçmişi

##### Tüm commitleri en yenisinden başlayarak listeler:
```
$ git log
```

##### Tüm commitleri görüntüler(Sadece commit hash ve commit mesajı görüntülenir.):
```
$ git log --oneline
```

##### Belli kullanıcıya ait commitleri görüntüler:
```
$ git log --author="username"
```

##### Belirli bir dosya üzerinde zaman içinde meydana gelen değişiklikleri göstermektedir:
```
$ git log -p <file>
```

##### &lt;Dosyayı&gt; kimin ne zaman değiştirdiğini gösterir:
```
$ git blame <file>
```

##### Referans kayıtlarını gösterir:
```
$ git reflog show
```

##### Referans kayıtlarını siler:
```
$ git reflog delete
```

<hr>

## Güncelleştirme & Yayınlama

##### Yapılandırılmış tüm güncel remoteları listeler:
```
$ git remote -v
```

##### Belirli bir &lt;remote&gt; hakkında bilgileri gösterir.:
```
$ git remote show <remote>
```

##### Yeni remote repository oluşturur, &lt;remote&gt; diye isimlendirir:
```
$ git remote add <remote> <url>
```

##### &lt;Remote&gt; da bulunan tüm değişiklikleri indirir, ama ana brachle birleştirmez:
```
$ git fetch <remote>
```

##### Değişiklikleri indirir ve doğrudan ana brache merge/integrate eder:
```
$ git remote pull <remote> <url>
```

##### Tüm ana Branchteki değişiklikleri yerel repositorye ekler:
```
$ git pull origin master
```

##### Remote da bulunan repositorye(depoya), yerel değişiklikleri yayınlar:
```
$ git push remote <remote> <branch>
```

##### Remote da bulunan bir branchi siler:
```
$ git push <remote> :<branch> (since Git v1.5.0)
```
ya da
```
$ git push <remote> --delete <branch> (since Git v1.7.0)
```

##### Etiketleri yayınlar:
```
$ git push --tags
```


