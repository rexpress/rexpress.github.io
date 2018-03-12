# regular.express

[regular.express](http://regular.express) is static website powered by Github Pages.

We use special library **[Jikji](https://github.com/Prev/jikji/tree/0.5)** to automate rendering pages. Datas are stored in [Cloudant](https://www.ibm.com/cloud/cloudant), which is document database service powered by IBM.



## Build manually

Originally, this website is built automatically for every hour by Jenkins. But now it stopped by cost problem.

However, you can build this website manually with terminal and `git`


### How to build & test service

```bash
$ git clone https://github.com/rexpress/web-res
$ cd web-res
$ pip install -r requirements.txt # or use pip3
$ python -m jikji . listen # or use python3
```

Then you can see website in `http://localhost:7000`


### Commit a website

Install `web-res` and then run command.

1. Fork [https://github.com/rexpress/rexpress.github.io](https://github.com/rexpress/rexpress.github.io).

2. Run command below.

```bash
$ git clone https://github.com/{YOUR_NICK_NAME}/rexpress.github.io
$ python -m jikji . generate
$ cd rexpress.github.io
$ git add *
$ git commit -am "Build manually"
$ git push
```

3. Make a pull request to `rexpress/rexpress.github.io`
4. We will accept for it!

