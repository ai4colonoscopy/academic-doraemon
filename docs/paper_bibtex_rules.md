# 如何使用正确的文献引用格式

**原则1**：引用顺序是“期刊>会议”
- 会议拓展期刊的，优先引用期刊

**原则2**：避免引用arXiv论文
- 特别是针对特别经典的论文，大概率90%是有会议或者期刊收录的，这时候一定要查清楚是否被正式收录了！

**原则3**：bibtex的具体格式

- 这里为什么强调投稿期间，特别是不同的期刊在acceptance后，修稿期间可能会要求你修改引用的格式，比如添加具体的doi什么的，等等。

- 期刊的bibtex格式
    - 对于有volume、number、page等具体信息的，建议引用格式如下
    ```text
    @article{wu2024towards,
        title={Towards open vocabulary learning: A survey},
        author={Wu, Jianzong and Li, Xiangtai and Yuan, Shilin Xu Haobo and Ding, Henghui and Yang, Yibo and Li, Xia and Zhang, Jiangning and Tong, Yunhai and Jiang, Xudong and Ghanem, Bernard and others},
        journal=TPAMI,
        year={2024},
        volume={46},
        number={7},
        pages={5092-5113},
    }
    ```
    - 对于没有上述信息的，请首先确保自己能完整的检索过！比如今年是2024年，如果你的bibtex是2023年或者2023之前的的还没有volume、number、page的，可能就是你的检索问题的（推荐IEEE论文直接上[官网检索](https://ieeexplore.ieee.org/Xplore/home.jsp)，不要在google scholar上检索）
    - 对于太新的论文，比如那些early access的论文，实在找不到的，请加上对应的doi号，如下所示：

    ```text
    @article{xu2024ssl,
        title={SSL-CPCD: Self-supervised learning with composite pretext-class discrimination for improved generalisability in endoscopic image analysis},
        author={Xu, Ziang and Rittscher, Jens and Ali, Sharib},
        journal=TMI,
        year={2024},
        volume={},
        number={},
        pages={},
        note={doi: \href{https://doi.org/10.1109/TMI.2024.3411933}{10.1109/TMI.2024.3411933}},
    }
    ```

- 会议的bibtex引用格式（建议是注释掉pages，这样子后期方便解注释）

    ```text
    @inproceedings{huang2017densely,
    title={Densely connected convolutional networks},
    author={Huang, Gao and Liu, Zhuang and Van Der Maaten, Laurens and Weinberger, Kilian Q},
    booktitle=CVPR,
    year={2017},
    \\pages={4700--4708}
    }
    ```

- 细心的你，一定会发现，上面的`booktitle`和期刊的`journal`使用了缩写，这里是为了节省投稿页面的空间。下面是我们自己收集的一些定义宏，为了方便进行bibtex文件的替换

```text

%%%%%%% conference %%%%%
@String(AAAI = {AAAI})
@String(CVPR  = {IEEE CVPR})
@String(CVPRW = {IEEE CVPR-W})
@String(ICCV  = {IEEE ICCV})
@String(ICCVW  = {IEEE ICCV-W})
@String(ECCV  = {ECCV})
@String(NeurIPS  = {NeurIPS})
@String(ICPR  = {IEEE ICPR})
@String(ICPRW  = {IEEE ICPR-W})
@String(BMVC  =	{BMVC})
@String(ICLR  = {ICLR})
@String(ICML  = {ICML})
@String(ICMLW  = {ICML-W})
@String(IJCAI = {IJCAI})
@String(MMM = {MMM})
@String(MMSys  = {ACM MMSys})
@String(ACMMM = {ACM MM})
@String(ACMMM-W = {ACM MM-W})
@String(CLEFW = {CLEF (Working notes)})
@String(IPMI = {IPMI})
@String(ISM = {IEEE ISM})
@String(ISVC = {ISVC})
@String(MICCAI= {MICCAI})
@String(MICCAIW= {MICCAI-W})
@String(MIDL = {MIDL})
@String(EMNLP = {EMNLP})
@String(IASTED = {IEEE IASTED})
@String(MI = {SPIE Med. Imaging})
@String(CVIP = {CVIP})
@String(IJCNN = {IJCNN})


%%%%%%% Journal %%%%%%%%
@String(MIR = {MIR})
@String(CIBM = {CIBM})
@String(CARS = {CARS})
@String(TPAMI = {IEEE TPAMI})
@String(IJCV  = {IJCV})
@String(TCSVT = {IEEE TCSVT})
@String(PR = {PR})
@String(JAIR = {CAAI AIR})
@String(ISBI = {IEEE ISBI} )
@String(AIIM = {AIIM})
@String(AS = {ApplSci})
@String(BMC = {BMCMI})
@String(BOE = {Biomed. Opt. Express})
@String(BSPC = {BSPC})
@String(CMIG = {CMIG})
@String(CVMJ = {CVMJ})
@String(EIO = {EIO})
@String(Gastro = {Gastro})
@String(GIE = {GIE})
@String(GRSL = {IEEE GRSL})
@String(TCYB = {IEEE TCYB})
@String(JBHI  = {IEEE JBHI})
@String(JI = {J. Imaging})
@String(MIA = {MedIA})
@String(PO = {PONE})
@String(MTAP = {MTAP})
@String(NECO = {Neural Comput.})
@String(NPJ = {NPJDM})
@String(SEND = {SEND})
@String(SD = {SData})
@String(TIM = {IEEE TIM})
@String(TNNLS = {IEEE TNNLS})
@String(TMI = {IEEE TMI})
@String(WJG = {WJG})
@String(BRMIC = {BRMIC})
@String(TMLR = {TMLR})
@String(IBD = {IBD})
@String(FMB = {FMOLB})
@String(SJG = {SJG})
@String(JHE = {JHE})
@String(IJIST = {IJIST})
@String(NR = {Nutr. Rev.})
@String(Gut = {Gut})
@String(PeerJ = {PeerJ})
@String(AFP = {AFP})
@String(SCIS = {SCIS})
@String(NM = {NM})
@String(SSI = {SSI})
@String(Nature = {Nature})
@String(Lancet = {The Lancet})
@String(TICS = {TICS})
@String(TNNLS = {IEEE TNNLS})
@String(TMM = {IEEE TMM})
@String(TII = {IEEE TII})
@String(ESWA = {ESWA})
@String(Nrgastro = {Nrgastro})
@String(NComms = {NComms})
@String(VI = {VI})
@String(CoRR = {CoRR})
%%%%%%%%%%%%%%%%%%%%%%%%

```