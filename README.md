# resched_jd306

**算出训练资源调度工程师·函数调用的 schema 校验里各项的占比与比值。**

`resched_jd306` —— 从输入中抽取数值，计算训练资源调度工程师·函数调用的 schema 校验相关的比值与占比，分母为零时明确报错

- 零依赖，Python 3.10+ 标准库即可运行
- 单文件，`resched_jd306.py` 拷走就能用
- 不联网、不写文件

## 对应的岗位

- 目标岗位：**快手 · 架构训练资源调度工程师**
- 技能主线：Kubernetes、Ray、AI芯片算力
- 领域标签：AI基础设施、MLOps
- 研究方向：训练资源调度工程师·函数调用的 schema 校验

工具里的规则表就是照着上面这条岗位要求建的——每条规则都挂在技能线或领域标签上，命中时能指回具体要求。

<!-- ipos:install -->
## 安装

零依赖，Python 3.10+ 即可：

```bash
pip install wineriddle-resched_jd306
```

装完直接用命令名调用：

```bash
resched_jd306 --help
```

也可以不用安装，直接把 `resched_jd306.py` 拷走用——它只依赖标准库。

## 为什么需要它

分母为零时明确报错，不返回 0 也不返回无穷，避免污染下游统计

它遵守下面几条自己定的规矩：

1. **只报告能定位到具体位置的结论**，不做语义猜测。
2. **规则表公开**，每条命中都能对应到岗位要求的一条明示规则。
3. **输入为空或格式不对时明确报错**，不静默返回空结果。

## 用法

```bash
python resched_jd306.py --file input.txt
python resched_jd306.py --text "示例内容"
python resched_jd306.py --file input.txt --json
```

加 `--json` 可以拿到机器可读的结果，便于接到流水线里。

## 已知局限

- 比例的分母取自你给的口径，不替你选口径。
- 不判断比例高低是否合理。

## 跑测试

```bash
python test_resched_jd306.py
```

测试用独立的断言与临时数据，不污染工作目录。

## 来源与参考

- Python 标准库文档：<https://docs.python.org/3/>
- GitHub 仓库：<https://github.com/wineriddle/resched_jd306>

---

## 关于作者

wineriddle 做训练资源调度工程师·函数调用的 schema 校验相关的问题，方向对标快手的架构训练资源调度工程师岗位。这个工具先替你回答一个具体问题，再谈别的。

- 个人主页：<https://wineriddle.github.io>
- 仓库：<https://github.com/wineriddle/resched_jd306>

## 许可

MIT，见 [LICENSE](LICENSE)。
