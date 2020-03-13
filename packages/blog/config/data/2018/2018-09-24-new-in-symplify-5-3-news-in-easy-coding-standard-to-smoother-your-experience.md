---
id: 150
title: "New in Symplify 5: 3 News in EasyCodingStandard to Smoother Your Experience"
perex: |
    Let's get lazier and lazier.
tweet: "New Post on My Blog: New in #Symplify 5 - 3 News in #EasyCodingStandard to Smoother Your Experience    #php #ecs #phpcsfixer #phpcodesniffer"
---

You don't have this package installed yet?

```bash
composer require symplify/easy-coding-standard --dev
```

Now enjoy the news ↓

## 1. Friendlier Skips

<a href="https://github.com/Symplify/Symplify/pull/948/files" class="btn btn-dark btn-sm">
    <em class="fab fa-github fa-fw"></em>
    See pull-request #948
</a>

Little details make more pleasant developer experience UX. You already know **you can use  [`fnmatch()`](http://php.net/manual/en/function.fnmatch.php) for skipping files**. The problem is, it requires very specific format people struggle with and often end up using explicit 10 paths to many files.

**Before** you had to hit the format:

```yaml
# ecs.yml
parameters:
    skip:
        SomeFixer:
            # this does
            - '*src/*CaseConverter.php'

            # this doesn't work
            - 'src/*CaseConverter.php'
```

**Now** you can use your intuition, copy paste the filename from error result and both versions work:

```yaml
# ecs.yml
parameters:
    skip:
        SomeFixer:
            # both works
            - 'src/*CaseConverter.php'
            - '*src/*CaseConverter.php'
```

## 2. In Lazy We Trust

<a href="https://github.com/Symplify/Symplify/pull/832/files" class="btn btn-dark btn-sm">
    <em class="fab fa-github fa-fw"></em>
    See pull-request #832
</a>

**Before** you had to type the whole config name:

```bash
easy-coding-standard.yaml
easy-coding-standard.yml
```

**Now** you can also use short version:

```bash
ecs.yaml
ecs.yml
```

## 3. Are There Some "array" Checkers?

<a href="https://github.com/Symplify/Symplify/pull/967/files" class="btn btn-dark btn-sm">
    <em class="fab fa-github fa-fw"></em>
    See pull-request #967
</a>

Many people asked for an overview of all checkers there are, if there any related to an array, to `strict_types` position and so on.


**Before** you had to go to huge `README.md` files of PHP CS Fixer and PHP_CodeSniffer on Github to read it all. But **why leave the luxury of CLI if these checkers are already downloaded** on your machine?

**Now** you can use "find" command:

<img src="/assets/images/posts/2018/symplify-5-ecs/find.gif" class="img-thumbnail">

Next time you'll wonder what are "Symplify" rules, keep your browser closed and just find them:

```bash
vendor/bin/ecs find symplify
```

<br>

Enjoy laziness, intuitive use and faster access to the information you look for.

We'll continue to make it this way!