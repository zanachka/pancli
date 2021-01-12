# pancli
Pancli (also known as Pansi Cli), is a tool for running scrapy spider or interact to ScrapyDD.

# install
pancli is available on pip, you can install it by simply run:

```
pip install pancli
```

# commands
## run a spider

run a spider is very easy by executing `pancli crawl {spider_name}`, the command is compatiable with `scrapy crawl`

One special parameter which is the `-f ` parameter which specify a FIGURE file that all parameters of a spider can be writen in a simple JSON/YAML file. If you run spider verfy often, FIGURE file can save your life.

FIGURE fields:

* spider: the target spider name which is the same in the `scrapy list` command.
* settings: (dict) settings can be used to populate all settings at runtime, not only the literal/string values, but list/dicts

And other parameters, the more detail documentation is coming soon.

## package a spider
A packaged spider is extremely portable, with one spider package and a FIGURE file, you can easily crawl the whole internet.

When your current dir is in the scope of scrapy project(with any ancient folder which contains a scrapy.cfg file), you can easily run the following commmand to build a spider package.

```
pancli package
```

If you haven't create setup.py for the project, this command will help you create one.

And this command is inspired by [scrapyd-client](https://github.com/scrapy/scrapyd-client)



