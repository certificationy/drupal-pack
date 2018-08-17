<p align="center">
    <img src="https://avatars0.githubusercontent.com/u/8029934?v=3&s=200">
</p>

# Certificationy - Drupal Pack
> This is the Drupal Pack for [Certificationy](https://github.com/certificationy).

This is provides a complete system to build multiple choice question system.
This is useful for any company that need to test an applicant, or to make a
certification website/training tool.

# How it looks?

![Certificationy application](https://cloud.githubusercontent.com/assets/1247388/17698070/434e3944-63b9-11e6-80c6-91706dbbea50.png "Certificationy application")

# How to use it?

As usual, use composer to install the library:

```bash
git clone https://github.com/certificationy/certificationy-cli.git
cd certificationy-cli
composer require "wengerk/certificationy-drupal-pack"
```

Then, you need to load packs using the `config.yml` file.

For instance, let's say you need the drupal-pack:

```yaml
# config.yaml
paths: ["vendor/wengerk/certificationy-drupal-pack/data"]
```

Then you can do:

```bash
php certificationy.php start
```

## More run options

### Select the number of questions

```bash
php certificationy.php start --number=10
```

The default value is 20.

### List categories

```bash
php certificationy.php start --list [-l]
```

Will list all the categories available

### Only questions from certain categories

```bash
php certificationy.php start "Automated tests" "Bundles"
```

Will only get the questions from the categories "Automated tests" and "Bundles"

Use the category list from [List categories](#list-categories)

### Hide the information that questions are/aren't multiple choice

```bash
php certificationy.php start --hide-multiple-choice
```

As default, the information will be displayed

![Multiple choice](https://cloud.githubusercontent.com/assets/795661/3308225/721b5324-f679-11e3-8d9d-62ba32cd8e32.png "Multiple choice")

### Set custom configuration file

```bash
bin/certificationy start --config=../config.yml
```

Will set custom config file

### And all combined

```bash
php certificationy.php start --number=5 --hide-multiple-choice "Automated tests" "Bundles"
```

* 5 questions
* We will hide the information that questions are/aren't multiple choice
* Only get questions from category "Automated tests" and "Bundles"

> Note: if you pass --list [-l] then you will ONLY get the category list, regarding your other settings

# Please, help us complete our official packs of questions!

You can submit PR with your own questions into the packs located under the [Certificationy Drupal Repository](https://github.com/wengerk/certificationy-drupal-pack).

Certificationy provides packs for both [PHP5](https://github.com/certificationy/php-pack) and [Symfony](https://github.com/certificationy/symfony-pack) certifications.

More we will have questions, the more powerful will be this tool!