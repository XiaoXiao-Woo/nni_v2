.. 24e980bd73ba5e335fba0d026916955e

###########################
Neural Network Intelligence
###########################


..  toctree::
    :maxdepth: 2
    :titlesonly:
    :hidden:

    概述<Overview>
    安装 <installation>
    入门<Tutorial/QuickStart>
    自动（超参数）调优 <hyperparameter_tune>
    神经网络架构搜索<nas>
    模型压缩<model_compression>
    特征工程<feature_engineering>
    参考<reference>
    示例与解决方案<CommunitySharings/community_sharings>
    研究和出版物 <ResearchPublications>
    常见问题 <Tutorial/FAQ>
    如何贡献 <contribution>
    更改日志 <Release>


.. raw:: html

  <div class="rowHeight">
    <div class="chinese"><a href="https://nni.readthedocs.io/zh/stable/">English</a></div>
    <b>NNI (Neural Network Intelligence)</b> 是一个轻量但强大的工具包，帮助用户<b>自动</b>的进行
    <a href="FeatureEngineering/Overview.html">特征工程</a>，<a href="NAS/Overview.html">神经网络架构搜索</a>， <a href="Tuner/BuiltinTuner.html">超参调优</a>以及<a href="Compression/Overview.html">模型压缩</a>。
  </div>
  <p class="gap rowHeight">
    NNI 管理自动机器学习 (AutoML) 的 Experiment，
    <b>调度运行</b>
  由调优算法生成的 Trial 任务来找到最好的神经网络架构和/或超参，支持
    <b>各种训练环境</b>，如
    <a href="TrainingService/LocalMode.html">本机</a>,
    <a href="TrainingService/RemoteMachineMode.html">远程服务器</a>,
    <a href="TrainingService/PaiMode.html">OpenPAI</a>,
    <a href="TrainingService/KubeflowMode.html">Kubeflow</a>,
    <a href="TrainingService/FrameworkControllerMode.html">基于 K8S 的 FrameworkController（如，AKS 等)</a>,
    <a href="TrainingService/DLTSMode.html">DLWorkspace (又称 DLTS)</a>,
    <a href="TrainingService/AMLMode.html">AML (Azure Machine Learning)</a>
  以及其它云服务。
  </p>
  <!-- Who should consider using NNI -->
  <div>
    <h1 class="title">使用场景</h1>
    <ul>
      <li>想要在自己的代码、模型中试验<b>不同的自动机器学习算法</b>。</li>
      <li>想要在<b>不同的环境中</b>加速运行自动机器学习。</li>
      <li>想要更容易<b>实现或试验新的自动机器学习算法</b>的研究员或数据科学家，包括：超参调优算法，神经网络搜索算法以及模型压缩算法。
      </li>
      <li>在机器学习平台中<b>支持自动机器学习</b>。</li>
    </ul>
  </div>
  <!-- nni release to version -->
  <div class="inline gap">
    <h3><a href="https://github.com/microsoft/nni/releases">NNI v2.6 已发布！</a></h3>
    <img width="48" src="_static/img/release_icon.png">
  </div>
  <!-- NNI capabilities in a glance -->
  <div class="gap">
    <h1 class="title">NNI 功能一览</h1>
    <p class="rowHeight">
      NNI 提供命令行工具以及友好的 WebUI 来管理训练的 Experiment。
      通过可扩展的 API，可定制自动机器学习算法和训练平台。
      为了方便新用户，NNI 内置了最新的自动机器学习算法，并为流行的训练平台提供了开箱即用的支持。
    </p>
    <p class="rowHeight">
      下表中，包含了 NNI 的功能，同时在不断地增添新功能，也非常希望您能贡献其中。
    </p>
  </div>

  <p align="center">
    <a href="#overview"><img src="_static/img/overview.svg" /></a>
  </p>

  <table class="main-table">
    <tbody>
      <tr align="center" valign="bottom" class="column">
        <td></td>
        <td class="framework">
          <b>框架和库</b>
        </td>
        <td>
          <b>算法</b>
        </td>
        <td>
          <b>训练平台</b>
        </td>
      </tr>
      </tr>
      <tr>
        <td class="verticalMiddle"><b>内置</b></td>
        <td>
          <ul class="firstUl">
            <li><b>支持的框架</b></li>
            <ul class="circle">
              <li>PyTorch</li>
              <li>Keras</li>
              <li>TensorFlow</li>
              <li>MXNet</li>
              <li>Caffe2</li>
              <a href="SupportedFramework_Library.html">更多...</a><br />
            </ul>
          </ul>
          <ul class="firstUl">
            <li><b>支持的库</b></li>
            <ul class="circle">
              <li>Scikit-learn</li>
              <li>XGBoost</li>
              <li>LightGBM</li>
              <a href="SupportedFramework_Library.html">更多...</a><br />
            </ul>
          </ul>
          <ul class="firstUl">
            <li><b>示例</b></li>
            <ul class="circle">
              <li><a href="https://github.com/microsoft/nni/tree/master/examples/trials/mnist-pytorch">MNIST-pytorch</li>
              </a>
              <li><a href="https://github.com/microsoft/nni/tree/master/examples/trials/mnist-tfv2">MNIST-tensorflow</li>
              </a>
              <li><a href="https://github.com/microsoft/nni/tree/master/examples/trials/mnist-keras">MNIST-keras</li></a>
              <li><a href="TrialExample/GbdtExample.html">Auto-gbdt</a></li>
              <li><a href="TrialExample/Cifar10Examples.html">Cifar10-pytorch</li></a>
              <li><a href="TrialExample/SklearnExamples.html">Scikit-learn</a></li>
              <li><a href="TrialExample/EfficientNet.html">EfficientNet</a></li>
              <li><a href="TrialExample/OpEvoExamples.html">GPU Kernel 调优</li></a>
              <a href="SupportedFramework_Library.html">更多...</a><br />
            </ul>
          </ul>
        </td>
        <td align="left">
          <a href="Tuner/BuiltinTuner.html">超参调优</a>
          <ul class="firstUl">
            <div><b>穷举搜索</b></div>
            <ul class="circle">
              <li><a href="Tuner/BuiltinTuner.html#Random">Random Search（随机搜索）</a></li>
              <li><a href="Tuner/BuiltinTuner.html#GridSearch">Grid Search（遍历搜索）</a></li>
              <li><a href="Tuner/BuiltinTuner.html#Batch">Batch（批处理）</a></li>
            </ul>
            <div><b>启发式搜索</b></div>
            <ul class="circle">
              <li><a href="Tuner/BuiltinTuner.html#Evolution">Naïve Evolution（朴素进化）</a></li>
              <li><a href="Tuner/BuiltinTuner.html#Anneal">Anneal（退火算法）</a></li>
              <li><a href="Tuner/BuiltinTuner.html#Hyperband">Hyperband</a></li>
              <li><a href="Tuner/BuiltinTuner.html#PBTTuner">P-DARTS</a></li>
            </ul>
            <div><b>贝叶斯优化</b></div>
            <ul class="circle">
              <li><a href="Tuner/BuiltinTuner.html#BOHB">BOHB</a></li>
              <li><a href="Tuner/BuiltinTuner.html#TPE">TPE</a></li>
              <li><a href="Tuner/BuiltinTuner.html#SMAC">SMAC</a></li>
              <li><a href="Tuner/BuiltinTuner.html#MetisTuner">Metis Tuner</a></li>
              <li><a href="Tuner/BuiltinTuner.html#GPTuner">GP Tuner</a> </li>
              <li><a href="Tuner/BuiltinTuner.html#DNGOTuner">PPO Tuner</a></li>
            </ul>
          </ul>
          <a href="NAS/Overview.html">神经网络架构搜索</a>
          <ul class="firstUl">
            <ul class="circle">
              <li><a href="NAS/ENAS.html">ENAS</a></li>
              <li><a href="NAS/DARTS.html">DARTS</a></li>
              <li><a href="NAS/SPOS.html">SPOS</a></li>
              <li><a href="NAS/Proxylessnas.html">ProxylessNAS</a></li>
              <li><a href="NAS/FBNet.html">微信</a></li>
              <li><a href="NAS/ExplorationStrategies.html">基于强化学习</a></li>
              <li><a href="NAS/ExplorationStrategies.html">Network Morphism</a></li>
              <li><a href="NAS/Overview.html">TextNAS</a></li>
            </ul>
          </ul>
          <a href="Compression/Overview.html">模型压缩</a>
          <ul class="firstUl">
            <div><b>剪枝</b></div>
            <ul class="circle">
              <li><a href="Compression/Pruner.html#agp-pruner">AGP Pruner</a></li>
              <li><a href="Compression/Pruner.html#slim-pruner">Slim Pruner</a></li>
              <li><a href="Compression/Pruner.html#fpgm-pruner">FPGM Pruner</a></li>
              <li><a href="Compression/Pruner.html#netadapt-pruner">NetAdapt Pruner</a></li>
              <li><a href="Compression/Pruner.html#simulatedannealing-pruner">SimulatedAnnealing Pruner</a></li>
              <li><a href="Compression/Pruner.html#admm-pruner">ADMM Pruner</a></li>
              <li><a href="Compression/Pruner.html#autocompress-pruner">AutoCompress Pruner</a></li>
              <li><a href="Compression/Overview.html">更多...</a></li>
            </ul>
            <div><b>量化</b></div>
            <ul class="circle">
              <li><a href="Compression/Quantizer.html#qat-quantize">QAT Quantizer</a></li>
              <li><a href="Compression/Quantizer.html#dorefa-quantizer">DoReFa Quantizer</a></li>
              <li><a href="Compression/Quantizer.html#bnn-quantizer">BNN Quantizer</a></li>
            </ul>
          </ul>
          <a href="FeatureEngineering/Overview.html">特征工程（测试版）</a>
          <ul class="circle">
            <li><a href="FeatureEngineering/GradientFeatureSelector.html">GradientFeatureSelector</a></li>
            <li><a href="FeatureEngineering/GBDTSelector.html">GBDTSelector</a></li>
          </ul>
          <a href="Assessor/BuiltinAssessor.html">提前终止算法</a>
          <ul class="circle">
            <li><a href="Assessor/BuiltinAssessor.html#MedianStop">Median Stop（中位数终止）</a></li>
            <li><a href="Assessor/BuiltinAssessor.html#Curvefitting">Curve Fitting（曲线拟合）</a></li>
          </ul>
        </td>
        <td>
          <ul class="firstUl">
            <li><a href="TrainingService/LocalMode.html">本机</a></li>
            <li><a href="TrainingService/RemoteMachineMode.html">远程计算机</a></li>
            <li><a href="TrainingService/HybridMode.html">混合模式</a></li>
            <li><a href="TrainingService/AMLMode.html">AML(Azure Machine Learning)</a></li>
            <li><b>基于 Kubernetes 的平台</b></li>
            <ul>
              <li><a href="TrainingService/PaiMode.html">OpenPAI</a></li>
              <li><a href="TrainingService/KubeflowMode.html">Kubeflow</a></li>
              <li><a href="TrainingService/FrameworkControllerMode.html">基于 K8S 的 FrameworkController (如 AKS 等)</a></li>
              <li><a href="TrainingService/DLTSMode.html">DLWorkspace (又称 DLTS)</a></li>
              <li><a href="TrainingService/AdaptDLMode.html">AML (Azure Machine Learning)</a></li>
            </ul>
          </ul>
        </td>
      </tr>
      <tr valign="top">
        <td class="verticalMiddle"><b>参考</b></td>
        <td>
          <ul class="firstUl">
            <li><a href="Tutorial/HowToLaunchFromPython.html">Python API</a></li>
            <li><a href="Tutorial/AnnotationSpec.html">NNI Annotation</a></li>
            <li><a href="installation.html">支持的操作系统</a></li>
          </ul>
        </td>
        <td>
          <ul class="firstUl">
            <li><a href="Tuner/CustomizeTuner.html">自定义 Tuner</a></li>
            <li><a href="Assessor/CustomizeAssessor.html">自定义 Assessor</a></li>
            <li><a href="Tutorial/InstallCustomizedAlgos.html">安装自定义的 Tuner，Assessor，Advisor</a></li>
            <li><a href="NAS/QuickStart.html">定义 NAS 模型空间</a></li>
            <li><a href="NAS/ApiReference.html">NAS/Retiarii APIs</a></li>
          </ul>
        </td>
        <td>
          <ul class="firstUl">
            <li><a href="TrainingService/Overview.html">支持训练平台</a></li>
            <li><a href="TrainingService/HowToImplementTrainingService.html">实现训练平台</a></li>
          </ul>
        </td>
      </tr>
    </tbody>
  </table>

  <!-- Installation -->
  <div>
    <h1 class="title">安装</h1>
    <div>
      <h2 class="second-title">安装</h2>
      <p>
        NNI 支持并在 Ubuntu >= 16.04, macOS >= 10.14.1, 和 Windows 10 >= 1809 通过了测试。 在 <code>python 64-bit >= 3.6</code> 的环境中，只需要运行 <code>pip install</code> 即可完成安装。
      </p>
      <div class="command-intro">Linux 或 macOS</div>
      <div class="command">python3 -m pip install --upgrade nni</div>
      <div class="command-intro">Windows</div>
      <div class="command">python -m pip install --upgrade nni</div>
      <p class="topMargin">如果想要尝试最新代码，可通过源代码<a href="installation.html">安装
          NNI</a>。
      </p>
      <p>Linux 和 macOS 下 NNI 系统需求<a href="Tutorial/InstallationLinux.html">参考这里</a>，Windows <a href="Tutorial/InstallationWin.html">参考这里</a>。</p>
    </div>
    <div>
      <p>注意：</p>
      <ul>
        <li>如果遇到任何权限问题，可添加 --user 在用户目录中安装 NNI。</li>
        <li>目前，Windows 上的 NNI 支持本机，远程和 OpenPAI 模式。 强烈推荐使用 Anaconda 或 Miniconda <a href="Tutorial/InstallationWin.html">在 Windows 上安装 NNI</a>。</li>
        <li>如果遇到如 Segmentation fault 这样的任何错误请参考 <a
            href="installation.html">常见问题</a>。 Windows 上的常见问题，参考在 <a href="Tutorial/InstallationWin.html">Windows 上使用 NNI</a>。 Windows 上的常见问题，参考在 <a href="Tutorial/InstallationWin.html">Windows 上使用 NNI</a>。</li>
      </ul>
    </div>
    <div>
      <h2 class="second-title">验证安装</h2>
      <p>
        以下示例基于 TensorFlow 1.x 构建。 确保运行环境中使用的是 <b>TensorFlow 1.x</b>。
      </p>
      <ul>
        <li>
          <p>通过克隆源代码下载示例。</p>
          <div class="command">git clone -b v2.6 https://github.com/Microsoft/nni.git</div>
        </li>
        <li>
          <p>运行 MNIST 示例。</p>
          <div class="command-intro">Linux 或 macOS</div>
          <div class="command">nnictl create --config nni/examples/trials/mnist-tfv1/config.yml</div>
          <div class="command-intro">Windows</div>
          <div class="command">nnictl create --config nni\examples\trials\mnist-tfv1\config_windows.yml</div>
        </li>
        <li>
          <p>
            在命令行中等待输出 INFO: Successfully started experiment!  
            此消息表明 Experiment 已成功启动。
            通过命令行输出的 Web UI url 来访问 Experiment 的界面。
          </p>
          <!-- Indentation affects style！ -->
          <pre class="main-code">
  INFO: Starting restful server...
  INFO: Successfully started Restful server!
  INFO: Setting local config...
  INFO: Successfully set local config!
  INFO: Starting experiment...
  INFO: Successfully started experiment!
  -----------------------------------------------------------------------
  The experiment id is egchD4qy
  The Web UI urls are: http://223.255.255.1:8080   http://127.0.0.1:8080
  -----------------------------------------------------------------------

  You can use these commands to get more information about the experiment
  -----------------------------------------------------------------------
    commands                       description
  1. nnictl experiment show        show the information of experiments
  2. nnictl trial ls               list all of trial jobs
  3. nnictl top                    monitor the status of running experiments
  4. nnictl log stderr             show stderr log content
  5. nnictl log stdout             show stdout log content
  6. nnictl stop                   stop an experiment
  7. nnictl trial kill             kill a trial job by id
  8. nnictl --help                 get help information about nnictl
  -----------------------------------------------------------------------
  </pre>
        </li>
        <li class="rowHeight">
          在浏览器中打开 Web UI 地址，可看到下图的 Experiment 详细信息，以及所有的 Trial 任务。 查看<a href="Tutorial/WebUI.html">这里的</a>更多页面示例。
          <img src="_static/img/webui.gif" width="100%"/>
    </div>
    </li>
    </ul>
  </div>

  <!-- Documentation -->
  <div>
    <h1 class="title">文档</h1>
    <ul>
      <li>要了解 NNI，请阅读 <a href="Overview.html">NNI 概述</a>。</li>
      <li>要熟悉如何使用 NNI，请阅读<a href="index.html">文档</a>。</li>
      <li>要安装 NNI，请参阅<a href="installation.html">安装 NNI</a>。</li>
    </ul>
  </div>

  <!-- Contributing -->
  <div>
    <h1 class="title">贡献</h1>
    <p>
      本项目欢迎任何贡献和建议。 大多数贡献都需要你同意参与者许可协议（CLA），来声明你有权，并实际上授予我们有权使用你的贡献。
      有关详细信息，请访问 <a href="https://cla.microsoft.com">https://cla.microsoft.com</a>。
    </p>
    <p>
      当你提交拉取请求时，CLA 机器人会自动检查你是否需要提供 CLA，并修饰这个拉取请求（例如，标签、注释）。 只需要按照机器人提供的说明进行操作即可。 CLA 只需要同意一次，就能应用到所有的代码仓库上。
    </p>
    <p>
      该项目采用了 <a href="https://opensource.microsoft.com/codeofconduct/">Microsoft 开源行为准则 </a>。 有关详细信息,请参阅<a href="https://opensource.microsoft.com/codeofconduct/faq/">行为守则常见问题解答</a>或联系 <a
        href="mailto:opencode@microsoft.com">opencode@microsoft.com</a> 咨询问题或评论。
    </p>
    <p>
      熟悉贡献协议后，即可按照 NNI 开发人员教程，创建第一个 PR =) 了：
    </p>
    <ul>
      <li>推荐新贡献者先从简单的问题开始：<a
          href="https://github.com/Microsoft/nni/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22">'good first issue'</a> 或 <a
          href="https://github.com/microsoft/nni/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22">'help-wanted'</a>。
      </li>
      <li><a href="Tutorial/SetupNniDeveloperEnvironment.html">NNI 开发环境安装教程</a></li>
      <li><a href="Tutorial/HowToDebug.html">如何调试</a></li>
      <li>
        如果有使用上的问题，可先查看<a href="Tutorial/FAQ.html">常见问题解答</a>。如果没能解决问题，可通过 <a
          href="https://gitter.im/Microsoft/nni?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge">Gitter</a> 
  联系 NNI 开发团队或在 GitHub 上<a href="https://github.com/microsoft/nni/issues/new/choose">报告问题</a>。
      </li>
      <li><a href="Tuner/CustomizeTuner.html">自定义 Tuner</a></li>
      <li><a href="TrainingService/HowToImplementTrainingService.html">实现定制的训练平台</a>
      </li>
      <li><a href="NAS/Advanced.html">在 NNI 上实现新的 NAS Trainer</a></li>
      <li><a href="Tuner/CustomizeAdvisor.html">自定义 Advisor</a></li>
    </ul>
  </div>

  <!-- External Repositories and References -->
  <div>
    <h1 class="title">其它代码库和参考</h1>
    <p>经作者许可的一些 NNI 用法示例和相关文档。</p>
    <ul>
      <h2>外部代码库</h2>
      <li>在 NNI 中运行 <a href="NAS/ENAS.html">ENAS</a></li>
      <li>
        https://github.com/microsoft/nni/blob/master/examples/feature_engineering/auto-feature-engineering/README_zh_CN.md
      </li>
      <li>使用 NNI 的 <a
          href="https://github.com/microsoft/recommenders/blob/master/examples/04_model_select_and_optimize/nni_surprise_svd.ipynb">矩阵分解超参调优</a></li>
      <li><a href="https://github.com/ksachdeva/scikit-nni">scikit-nni</a> 使用 NNI 为 scikit-learn 开发的超参搜索。</li>
    </ul>

    <!-- Relevant Articles -->
    <ul>
      <h2>相关文章</h2>
      <li><a href="CommunitySharings/HpoComparison.html">超参数优化的对比</a></li>
      <li><a href="CommunitySharings/NasComparison.html">神经网络结构搜索的对比</a></li>
      <li><a href="CommunitySharings/ParallelizingTpeSearch.html">并行化顺序算法：TPE</a>
      </li>
      <li><a href="CommunitySharings/RecommendersSvd.html">使用 NNI 为 SVD 自动调参</a></li>
      <li><a href="CommunitySharings/SptagAutoTune.html">使用 NNI 为 SPTAG 自动调参</a></li>
      <li><a
          href="https://towardsdatascience.com/find-thy-hyper-parameters-for-scikit-learn-pipelines-using-microsoft-nni-f1015b1224c1">
          使用 NNI 为 scikit-learn 查找超参
        </a></li>
      <li>
        <strong>博客</strong> - <a
          href="http://gaocegege.com/Blog/%E6%9C%BA%E5%99%A8%E5%AD%A6%E4%B9%A0/katib-new#%E6%80%BB%E7%BB%93%E4%B8%8E%E5%88%86%E6%9E%90">AutoML 工具（Advisor，NNI 与 Google Vizier）的对比</a> 作者：@gaocegege - kubeflow/katib 的设计与实现的总结与分析章节
      </li>
      <li>
        Blog (中文) - <a href="https://mp.weixin.qq.com/s/7_KRT-rRojQbNuJzkjFMuA">NNI 2019 新功能汇总</a> by @squirrelsc
      </li>
    </ul>
  </div>

  <!-- feedback -->
  <div>
    <h1 class="title">反馈</h1>
    <ul>
      <li><a href="https://github.com/microsoft/nni/issues/new/choose">在 GitHub 上提交问题</a>。</li>
      <li>在 <a
          href="https://stackoverflow.com/questions/tagged/nni?sort=Newest&edited=true">Stack Overflow</a> 上使用 nni 标签提问。
      </li>
      <li>在 <a
          href="https://gitter.im/Microsoft/nni?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge">Gitter</a> 中参与讨论。</li>
    </ul>
    <div>
      <div>加入聊天组：</div>
      <table border=1 style="border-collapse: collapse;">
        <tbody>
          <tr style="line-height: 30px;">
            <th>Gitter</th>
            <td></td>
            <th>微信</th>
          </tr>
          <tr>
            <td class="QR">
              <img src="https://user-images.githubusercontent.com/39592018/80665738-e0574a80-8acc-11ea-91bc-0836dc4cbf89.png" alt="Gitter" />
            </td>
            <td width="80" align="center" class="or">或</td>
            <td class="QR">
              <img src="https://github.com/scarlett2018/nniutil/raw/master/wechat.png" alt="NNI 微信" />
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>

  <!-- Related Projects -->
  <div>
    <h1 class="title">相关项目</h1>
    <p>
      以探索先进技术和开放为目标，<a href="https://www.microsoft.com/zh-cn/research/group/systems-and-networking-research-group-asia/">Microsoft Research (MSR)</a> 还发布了一些相关的开源项目。</p>
    <ul id="relatedProject">
      <li>
        <a href="https://github.com/Microsoft/pai">OpenPAI</a>：作为开源平台，提供了完整的 AI 模型训练和资源管理能力，能轻松扩展，并支持各种规模的私有部署、云和混合环境。
      </li>
      <li>
        <a href="https://github.com/Microsoft/frameworkcontroller">FrameworkController</a>：开源的通用 Kubernetes Pod 控制器，通过单个控制器来编排 Kubernetes 上所有类型的应用。
      </li>
      <li>
        <a href="https://github.com/Microsoft/MMdnn">MMdnn</a>：一个完整、跨框架的解决方案，能够转换、可视化、诊断深度神经网络模型。 MMdnn 中的 "MM" 表示 model management（模型管理），而 "dnn" 是 deep neural network（深度神经网络）的缩写。
      </li>
      <li>
        <a href="https://github.com/Microsoft/SPTAG">SPTAG</a> : Space Partition Tree And Graph (SPTAG) 是用于大规模向量的最近邻搜索场景的开源库。
      </li>
    </ul>
    <p>我们鼓励研究人员和学生利用这些项目来加速 AI 开发和研究。</p>
  </div>

  <!-- License -->
  <div>
    <h1 class="title">许可协议</h1>
    <p>代码库遵循 <a href="https://github.com/microsoft/nni/blob/master/LICENSE">MIT 许可协议</a></p>
  </div>
  </div>