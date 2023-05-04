# Domain Scanning Tool

A tool for domain bulk scanning based on SOA record. It can be used to find nice domain hacks at high speed.

Its features include:

- Easy to use interface;
- Fast scanning speed;
- Supporting both IPv4 and IPv6
- (Theoretically) supporting all suffixes including secondary ones and even higher levels;
- Supporting scanning multiple suffixes at once;
- Only relying on Python built-in libraries.



操作步骤如下：  
**1、下载文件**
```
git clone https://github.com/dynos01/DomainScanningTool
cd DomainScanningTool
```
**2、设置带扫描的字典**

生成4个字母的字典  
echo {a..z}{a..z}{a..z}{a..z} | sed 's/ /\n/g' > LLLL.txt

生成4个数字的字典  
echo {0..9}{0..9}{0..9}{0..9} | sed 's/ /\n/g' > LLLL.txt

生成4个字母或者数字的字典    
echo {{a..z},{0..9}}{{a..z},{0..9}}{{a..z},{0..9}}{{a..z},{0..9}} | sed 's/ /\n/g' > LLLL.txt

**3、执行`python DomainScanningTool.py`**  
**4、输入DNS地址**  
Server addresses are like these: `8.8.8.8:53`, `1.1.1.1:53, [2001:4860:4860::8888]:53`

第三个dns地址可能会连不上，可以去掉

**5、输入域名后缀** 

Suffixes are like these: `com`, `com, net` (e.g. without the dot)

**6、输入字典文件名称**

The example dictionary `LLL.txt` contains all combinations of there letters. You can use your own dictionary instead.

**7、输入扫描结果的文件名称**



Known limitations:

- Can't distinguish reserved domains, as this tool relies on DNS system.
