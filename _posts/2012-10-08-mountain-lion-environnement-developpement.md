---
layout: post
title: Mon environnement de développement sur Mac OS X 10.8 (Mountain Lion)
category: francais
tags: OSX tools
---

Dans le contexte d'une installation "fraiche" de Mac OSX `Mountain Lion` depuis une clé USB, voici la procédure que j'ai suivie afin d'installer un environnement de développement `Ruby On Rails`:


## Installer XCode, XCode Command Line Tools, XQuartz

* Installer `Xcode 4.5.1` depuis le AppStore;
* Installer les `Command Line Tools` depuis les preferences de Xcode.

    Non obligatoire, mais j'ai besoin de support X11 pour certaines de mes applications:
    Il m'a donc fallu installer `XQuartz` disponible au lien suivant: [http://xquartz.macosforge.org/landing/]()

## Installer [iterm2](http://www.iterm2.com/)

Mon terminal de prédilection, autant l'installer dès maintenant: [http://www.iterm2.com/](http://www.iterm2.com/)

## Installer [homebrew](http://mxcl.github.com/homebrew/)

Tout d'abord exécuter les commades suivantes dans votre terminal (ex: iterm2)

{% highlight bash %}
  $ ruby -e "$(curl -fsSkL raw.github.com/mxcl/homebrew/go)"
{% endhighlight %}

Le script explique ce qu'il va faire et fera une pause avant de faire quoi que ce soit.
Pour être sûr que tout est bien installé:

{% highlight bash %}
  $ brew doctor
{% endhighlight %}

## Personnaliser les [dotfiles](https://github.com/benichu/dotfiles)

Pourquoi ne pas utiliser mes fichiers dotfiles sur `bash`?
Voici un lien vers les instructions du [README](https://github.com/benichu/dotfiles/blob/master/README.md)

## Installer [git](http://git-scm.com/)

Facile avec `homebrew`!

{% highlight bash %}
  $ brew install git
{% endhighlight %}

## Installer [rbenv](https://github.com/sstephenson/rbenv)

OS X est livré avec Ruby installé, mais il s'agit d'une version plus ancienne, afin de ne pas jouer avec cette installation par défaut,
nous allons utiliser `rbenv` et `ruby-build` pour pouvoir gérer et installer facilement nos environnements de développement `Ruby`.
Pour commencer, installons `rbenv`:

{% highlight bash %}
  $ brew install rbenv
{% endhighlight %}

Si vous avez utilisé mes `dotfiles`, rien d'autres à faire, sinon voici la procédure: [lien vers rbenv (github)](https://github.com/sstephenson/rbenv#-22-homebrew-on-mac-os-x)

Pour pouvoir installer les différentes versions de `ruby`, il faut installer `ruby-build`:

{% highlight bash %}
  $ brew install ruby-build
  $ rbenv install -l
{% endhighlight %}

Choisissez les versions de [ruby](http://www.ruby-lang.org/) à installer. Dans mon cas:

__ruby 1.9.3__

{% highlight bash %}
  $ rbenv install 1.9.3-p194
  $ rbenv versions
    1.9.3p194
  $ rbenv global 1.9.3-p194
  $ rbenv rehash
  $ ruby -v
    ruby 1.9.3p194 (2012-04-20 revision 35410) [x86_64-darwin12.2.0]
  $ which ruby
    /Users/bthouret/.rbenv/shims/ruby
{% endhighlight %}

__ruby enterprise edition (1.8.7)__

Il m'a fallu installer `gcc` indépendament pour pouvoir installer des versions `1.8.x` de ruby:
[osx-gcc-installer](https://github.com/kennethreitz/osx-gcc-installer/downloads)

{% highlight bash %}
  $ rbenv install ree-1.8.7-2012.02
  $ rbenv versions
    1.9.3p194
    ree-1.8.7-2012.02
{% endhighlight %}

J'installe aussi [rbenv-gemset](https://github.com/jamis/rbenv-gemset) afin de mieux différencier mes `gemsets` de projets.

{% highlight bash %}
  $ brew install rbenv-gemset
{% endhighlight %}

## Installer et configurer [MySQL](http://www.mysql.com/)

{% highlight bash %}
  $ brew install mysql
{% endhighlight %}

## Installer et configurer [redis](http://redis.io/)

{% highlight bash %}
  $ brew install redis
{% endhighlight %}

## Installer [MacVim](http://code.google.com/p/macvim/)

{% highlight bash %}
  $ brew install macvim --override-system-vim
{% endhighlight %}

Tant que l'on y est, installons ma distribution vim, c'est facile:

{% highlight bash %}
  $ curl http://2ret.com/vim -L -o - | sh
{% endhighlight %}

Je vous conseille de consulter le [README](https://github.com/benichu/2ret-vim/blob/master/README.md) avant.

## Quelques utilitaires...

Voici une liste non-exhaustive des utilitaires que j'utilise quotidiennement:

* [Google Chrome - Navigateur Web](https://www.google.com/intl/en/chrome/)
* [Alfred - Lanceur d'application](http://www.alfredapp.com/#download-alfred)
* [SizeUp - Redimensionner rapidement les fenêtres d'application](http://www.irradiatedsoftware.com/sizeup/)
* [Dropbox - Synchronisation et partage de fichiers](https://www.dropbox.com/)
* [1Password - Centralisation de mes mots de passe](https://agilebits.com/onepassword)
* [Propane - Client pour Campfire](http://propaneapp.com/)
* [Sequel Pro - Interface de gestion MySQL](http://www.sequelpro.com/)

Voilà pour aujourd'hui, bonne installation!

