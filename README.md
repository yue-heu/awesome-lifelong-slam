# Awesome_Lifelong_SLAM [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

My personal list of important content related to Lifelong SLAM and Robotics. Feel free to send me some suggestions: yuewangg@outlook.com

### Table of Contents
* **[Related survey papers](#related-survey-papers)**<br>
* **[Related research papers](#related-research-papers)**<br>
* **[Datasets](#researchers)**<br>
* **[Laboratories and Research Groups](#laboratories-and-research-groups)**<br>
* **[Conferences](#conferences)**<br>
* **[Journals](#journals)**<br>
* **[Courses](#courses)**<br>
------

## Related survey papers:

- [**A Systematic Literature Review on Long-Term Localization and Mapping for Mobile Robots**](https://www.researchgate.net/profile/Ricardo-Sousa-19/publication/364997498_A_Systematic_Literature_Review_on_Long-Term_Localization_and_Mapping_for_Mobile_Robots/links/636268b137878b3e8777a0c5/A-Systematic-Literature-Review-on-Long-Term-Localization-and-Mapping-for-Mobile-Robots.pdf). RB Sousa. the University of Porto. 2022

- [**A survey: which features are required for dynamic visual simultaneous localization and mapping?**](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8285453/pdf/42492_2021_Article_86.pdf). Zewen Xu,CAS. 2021

## Related research papers

- (ISRR 2022)[Continual SLAM: Beyond Lifelong Simultaneous Localization and Mapping Through Continual Learning](https://arxiv.org/pdf/2203.01578.pdf) 

  - 弗莱堡大学的持续SLAM，可以快速适应新环境，记忆以前见过的环境信息。 [page](http://continual-slam.cs.uni-freiburg.de/)，[code](https://github.com/robot-learning-freiburg/CL-SLAM)

- (IEEE RA-L'22)[DynaVINS: A Visual-Inertial SLAM for Dynamic Environments](https://arxiv.org/pdf/2208.11500), code:https://github.com/url-kaist/dynaVINS, 非深度学习结合的方案，而是使用约束对运动对象上的特征点进行去除

- [[2203.03923] ROLL: Long-Term Robust LiDAR-based Localization With Temporary Mapping in Changing Environments](https://arxiv.org/pdf/2203.03923) IROS 2022

  - code：https://github.com/HaisenbergPeng/ROLL

- [POCD: Probabilistic Object-Level Change Detection and Volumetric Mapping  in Semi-Static Scenes](https://arxiv.org/pdf/2205.01202v1)

  - RSS 2022，半静态场景中的地图更新


- L. Sun, Z. Yan, A. Zaganidis, C. Zhao, and T. Duckett, “**Recurrent-OctoMap: Learning State-Based Map Refinement for Long-Term Semantic Mapping With 3-D-Lidar Data**,” RAL
  - life long slam 

- P. Egger, P. V. K. Borges, G. Catt, A. Pfrunder, R. Siegwart, and R. Dubé, “**PoseMap: Lifelong, Multi-Environment 3D LiDAR Localization**,” IROS 2018
  - lifelong slam，ETH SAL组

- M. T. Lázaro, R. Capobianco, and G. Grisetti, “**[Efficient Long-term Mapping in Dynamic Environments](https://www.researchgate.net/profile/Maria-Lazaro-12/publication/330586668_Efficient_Long-term_Mapping_in_Dynamic_Environments/links/5f26efbe458515b729fe2f1b/Efficient-Long-term-Mapping-in-Dynamic-Environments.pdf)**,” IROS 2018
  - 高效的ICP方案，并且实现了地图实体的合并。由于处理的是2D地图，因此也就没有那么多的需要处理的东西。可以直接用点可视化来去除运动的点云。
  - **[code](https://gitlab.com/srrg-software/srrg_mapper2d_ros)**，

- T. Krajník, J. P. Fentanes, J. M. Santos, and T. Duckett, “**[FreMEn: Frequency Map Enhancement for Long-Term Mobile Robot Autonomy in Changing Environments](http://strands.acin.tuwien.ac.at/publications/y4/krajnik_TRO.pdf)**,” TRO 2017

- G. Kurz, M. Holoch, and P. Biber, “[**Geometry-based Graph Pruning for Lifelong SLAM**](http://arxiv.org/abs/2110.01286).” IROS 2021
  - 提出了一种新的方法，该方法考虑了几何准则来选择要剪枝的顶点。这是有效的，易于实现，并导致具有均匀分布的顶点的图形，这些顶点仍然是机器人轨迹的一部分。此外，我们提出了一种新的边际化方法，与现有方法相比，该方法对错误的循环闭包具有更强的鲁棒性。
    主要设计到SLAM后端的优化，当地图或者是因子图更新时，如何对因子图进行剪枝的问题。

- W. Ding, S. Hou, H. Gao, G. Wan, and S. Song, “[**LiDAR Inertial Odometry Aided Robust LiDAR Localization System in Changing City Scenes**](https://songshiyu01.github.io/pdf/LIO_W.Ding_S.Song_ICRA2020.pdf),” ICRA 2020
  - 百度出品的使用激光和IMU，在运动场景的定位，并且在之前构建的地图中，针对场景新增加的东西，将会新建相关的地图。
  - life-long SLAM

- G. D. Tipaldi, D. Meyer-Delius, and W. Burgard, “**Lifelong localization in changing environments**,” IJRR 2013
  - life-long的定位

- S. Zhu, X. Zhang, S. Guo, J. Li, and H. Liu, “**Lifelong Localization in Semi-Dynamic Environment**,” ICRA 2021
  - 清华，life-long的定位

- F. Pomerleau, P. Krüsi, F. Colas, P. Furgale, and R. Siegwart, “**Long-term 3D map maintenance in dynamic environments**,” ICRA 2014
  - 动态环境中，地图更新

- D. J. Yoon, T. Y. Tang, and T. D. Barfoot, “[**Mapless Online Detection of Dynamic Objects in 3D Lidar**](http://arxiv.org/abs/1809.06972).” Conference on Computer and Robot Vision (CRV) 2019
  - 点云动态检测

- M. Zhao *et al.*, “[**A General Framework for Lifelong Localization and Mapping in Changing Environment**](http://arxiv.org/abs/2111.10946).”  IROS 2021

  - 高仙机器人的**life-long** 定位的论文
  - 多session的地图表示和一种**高效的在线地图更新策略**，子系统组成：局部激光雷达里程计（LLO）、全局激光雷达匹配（GLM）和位姿图优化（PGR），LLO的作用是构建一系列局部一致的子地图，GLM子系统负责计算传入扫描点云和全局子地图之间的相对约束，并将子映地图和约束插入PGR，PGR是系统中最重要的部分，它从LLO和GLM收集子地图和约束关系，修剪并保存在历史地图中的旧的子地图，并执行姿势图稀疏化和优化。

- Pfreundschuh, Patrick, et al. “**[Dynamic Object Aware LiDAR SLAM Based on Automatic Generation of Training Data.](http://arxiv.org/abs/2104.03657)**” (*ICRA* *2021*)

  - **ETH ASL**,code, [video](https://youtu.be/LcDxd97r1Gc), [**dataset**](https://projects.asl.ethz.ch/datasets/doals), Lidar
  - 作者基于deep-learning（3D-MiniNet网络）进行实时3D动态物体检测，滤除动态物体后的点云被喂给LOAM，进行常规的激光SLAM。提供了学习的方法是属于无监督的方法。


- Chen Xieyuanli, et al. “**[Moving Object Segmentation in 3D LiDAR Data: A Learning-Based Approach Exploiting Sequential Data](https://www.ipb.uni-bonn.de/pdfs/chen2021ral-iros.pdf)**.” *IEEE Robotics and Automation Letters*, 2021
  - [code](https://github.com/PRBonn/LiDAR-MOS). [video](https://www.youtube.com/watch?v=NHvsYhk4dhw). University of Bonn.


- Rosen, David M., et al. “[**Towards Lifelong Feature-Based Mapping in Semi-Static Environments.**](https://doi.org/10.1109/ICRA.2016.7487237)” *(ICRA 2016)*

  
- Luiten Jonathon, et al. “[**Track to Reconstruct and Reconstruct to Track.**](https://arxiv.org/abs/1910.00130v3)”, (RAL+ICRA 2020)

  - [code](https://github.com/tobiasfshr/MOTSFusion), [video](https://youtu.be/PMOYkpBwE78). **Reconstruct**.

- Grinvald, Margarita, et al. “**[TSDF++: A Multi-Object Formulation for Dynamic Object Tracking and Reconstruction.](http://arxiv.org/abs/2105.07468)**”(ICRA 2021)

  - [code](https://github.com/ethz-asl/tsdf-plusplus), [video](https://youtu.be/dSJmoeVasI0).


## Datasets

- P Wenzel, R Wang, N Yang, Q Cheng,Qadeer Khan, Lukas von Stumberg, Niclas Zeller, Daniel Cremers， “**[4Seasons: A cross-season dataset for multi-weather SLAM in autonomous driving](https://arxiv.org/pdf/2009.06364.pdf)**,” DAGM GCPR 2020
  - 自动驾驶中多天气SLAM的跨季节数据集，TUM，[网站](https://www.4seasons-dataset.com/)

- X Shi, D Li et al. “**[Are We Ready for Service Robots? The OpenLORIS-Scene Datasets for Lifelong SLAM](https://arxiv.org/pdf/1911.05603.pdf)**,” ICRA 2020
  - 开放LORIS-场景数据集，清华大学，[网站](https://lifelong-robotic-vision.github.io/dataset/scene)

- Yin, Jie and Li, Ang and Li, Tao and Yu, Wenxian and Zou, Danping, “**[M2DGR: A Multi-sensor and Multi-scenario SLAM Dataset for Ground Robots](https://arxiv.org/pdf/2112.13659.pdf)**,” IEEE RA-L'21
  - M2DGR，上海交通大学，[网站](https://github.com/SJTU-ViSYS/M2DGR)

- Peng Yin and Shiqi Zhao et al. “**[ALITA: A Large-scale Incremental Dataset for Long-term Autonomy](https://arxiv.org/pdf/2205.10737.pdf)**,” arXiv 2022
  - ALITA，Carnegie Mellon University，[网站](https://github.com/MetaSLAM/ALITA)

- Y. Pan, B. Gao, J. Mei, S. Geng, C. Li, and H. Zhao, “**[SemanticPOSS: A Point Cloud Dataset with Large Quantity of Dynamic Instances](https://arxiv.org/pdf/2002.09147v1.pdf)**,” IV 2020
  - 动态物体室外数据集，北大，[网站](http://www.poss.pku.edu.cn/semanticposs.html)

- K. Minoda, F. Schilling, V. Wüest, D. Floreano, and T. Yairi, “**[VIODE: A Simulated Dataset to Address the Challenges of Visual-Inertial Odometry in Dynamic Environments,](https://doi.org/10.1109/LRA.2021.3058073)**”RAL 2021

  - 动态环境的数据集，包括了静态，动态等级的场景，感觉适合用来作为验证。
  - 东京大学，[code](https://github.com/kminoda/VIODE)

## Laboratories and Research Groups

### Global
* [AirLab](https://theairlab.org/) **| Carnegie Mellon University - Sebastian Scherer**
* [Autonomous Vision Group (AVG)](http://www.cvlibs.net/index.php) **| University of Tübingen - Andreas Geiger**
* [ICL Dyson Robotics Lab](http://wp.doc.ic.ac.uk/dyson-robotics-lab/) **| Imperial College London - Andrew Davison**
* [Robotics and Perception Group](http://rpg.ifi.uzh.ch/) **| University of Zurich - Davide Scaramuzza** [GitHub Link](https://github.com/uzh-rpg)
* [Laboratrio de Robótica Móvel](http://lrm.icmc.usp.br/web/index.php?n=Port.Home) **| ICMC/USP São Carlos - Fernando Osório**
* [StachnissLab](https://www.ipb.uni-bonn.de/) **| University of Bonn - Cyrill Stachniss** [GitHub Link](https://github.com/PRBonn)
* [Autonomous Intelligent Systems](http://ais.informatik.uni-freiburg.de/index_en.php) **| University of Freiburg - Wolfram Burgard**
* [Multi-Robt Systems Group](http://mrs.felk.cvut.cz/) **| University in Prague - Martin Saska**
* [Robotics and Intelligent Systems (ROBIN)](https://www.mn.uio.no/ifi/english/research/groups/robin/) **| University of Oslo - Jim Tørresen**
* [Machine Perception and Intelligent Robotics (MAPIR)](http://mapir.isa.uma.es/mapirwebsite/) **| University of Málaga - Javier Gonzalez Jimenez**
* [Robotics, Perception and Real Time Group](http://robots.unizar.es/) **| Universidad de Zaragoza - Juan D. Tardós and others** [GitHub Link](https://github.com/UZ-SLAMLab)
* [Team CoSTAR](https://costar.jpl.nasa.gov/) **| A collaboration between NASA’s JPL, MIT, Caltech, KAIST, LTU, and several industry partners** 
* [Autonomous Navigation and Perception Lab (ANPL)](https://vindelman.net.technion.ac.il/) **| Technion-Israel Institute of Technology - Vadim Indelman**
* [Institute for Robotics and Intelligent Machines (IRIM)](http://www.robotics.gatech.edu/) **| Georgia Institute of Technology**
* [Vijay Kumar Lab](https://www.kumarrobotics.org/) **| University of Pennsylvania - Vijay Kumar**
* [Phi Robotics](https://www.inf.ufrgs.br/phi-group/site/) **| Federal University of Rio Grande do Sul - Edson Prestes**
* [Computer Science and Artificial Intelligence Laboratory (CSAIL)](https://www.csail.mit.edu/) **| MIT’s research lab**
* [Goal-Oriented Long-Lived Systems (GOALS)](https://ori.ox.ac.uk/labs/goals/) **| Oxford Robotics Institute - Nick Hawes**
* [Skoltech Mobile Robotics](https://sites.skoltech.ru/mobilerobotics/) **| Skolkovo Institute of Science and Technology - Gonzalo Ferrer**
* [Compuver Vision and Intelligent Systems Laboratory](https://www.cs.ryerson.ca/~wangcs/cvis.html) **| Ryerson University - Guanghui (Richard) Wang**
* [UTS Robotics Institute](https://www.uts.edu.au/research/robotics-institute/) **| University of Technology Sydney - Sarath Kodagoda**
* [Lab for Autonomous Robotics Research](https://larr.snu.ac.kr/) **| Seoul National University - H. Jin Kim**  [GitHub Link](https://github.com/snu-larr)
* [ASRL - Autonomous Space Robotics Lab](http://asrl.utias.utoronto.ca/) **| University of Toronto - Tim Barfoot** [GitHub Link](https://github.com/utiasASRL)
* [Urban Robotics Lab](https://urobot.kaist.ac.kr/) **| KAIST (Korea Advanced Institute of Science and Technology) - Hyun MYUNG** [GitHub Link](https://github.com/url-kaist)
* [ETHZ V4RL](http://www.v4rl.ethz.ch/) **| ETH Zurich - Chli, Margarita** [GitHub Link](https://github.com/VIS4ROB-lab)
* [Dynamic Vision and Learning Group](https://dvl.in.tum.de) **| Technische Universität München - Laura Leal-Taixé** [GitHub Link](https://github.com/dvl-tum)
* [Computer Vision and Geometry Lab](http://cvg.ethz.ch) **| ETH Zurich - Marc Pollefeys** [GitHub Link](https://github.com/cvg)
* [MIST Laboratory](https://mistlab.ca/) **| University of Montreal - Giovanni Beltrame** [GitHub Link](https://github.com/MISTLab)
* [SPARK (Sensing, Perception, and Robot Kinetics) Lab](http://web.mit.edu/sparklab/) **| Massachusetts Institute of Technology - Luca Carlone** [GitHub Link](https://github.com/MIT-SPARK)
* [Stanford Vision and Learning Lab](https://svl.stanford.edu/) **| Stanford University - Fei-Fei Li** [GitHub Link](https://github.com/StanfordVL)
* [TUM Computer Vision Group](https://cvg.cit.tum.de/) **| Technische Universität München - Daniel Cremers** [GitHub Link](https://github.com/tum-vision)
* [Spatial AI & Robotics Lab](https://sairlab.org/) **| State University of New York at Buffalo - Chen Wang** [GitHub Link](https://github.com/sair-lab)
* [Robot Perception Lab](http://rpl.ri.cmu.edu/) **| Carnegie Mellon University - Michael Kaess** [GitHub Link]()
* [Robotics, Perception and Learning Lab](https://www.kth.se/is/rpl) **| KTH Royal Institute of Technology - Patric Jensfelt** [GitHub Link]()
* [Smart Robotics Lab](https://srl.cit.tum.de/) **| Technische Universität München - Stefan Leutenegger** 
* [UCLA VISION LAB](http://vision.ucla.edu/) **| UCLA - Stefano Soatto** [GitHub Link](https://github.com/ucla-vision)
* [Multiple Autonomous Robotic Systems (MARS) Laboratory](http://mars.cs.umn.edu/) **| University of Minnesota - Stergios Roumeliotis**
* [Active Vision Laboratory](https://www.robots.ox.ac.uk/ActiveVision/) **| University of Oxford - Victor Prisacariu**
* [Autonomous Systems Lab (ASL)](https://asl.ethz.ch/) **| ETH Zurich - Roland Siegwart** [GitHub Link](https://github.com/ethz-asl)
* [NTNU Autonomous Robots Lab](https://www.autonomousrobotslab.com/) **| Norwegian University of Science and Technology - Kostas Alexis** [GitHub Link](https://github.com/ntnu-arl)
 

### Chinese
* [ZJU3DV Lab of CAD&CG](http://www.cad.zju.edu.cn/index.html) **| Zhejiang University - 周晓巍** [GitHub Link](https://github.com/zju3dv)
* [Mechatronics and Robotic Systems (MaRS) Laboratory](https://mars.hku.hk/) **| The University of Hong Kong - Fu Zhang** [GitHub Link](https://github.com/hku-mars)
* [Integrated and Intelligent Navigation Group](http://www.i2nav.cn/) **| Wuhan University - 牛小骥** [GitHub Link](https://github.com/i2Nav-WHU)
* [MARS Lab](http://group.iiis.tsinghua.edu.cn/~marslab/#/) **| Tsinghua University - 赵行** [GitHub Link](https://github.com/tsinghua-mars-lab)
* [HKUST Aerial Robotics Group](https://uav.hkust.edu.hk/) **| the Hong Kong University of Science and Technology - Shaojie Shen (沈劭劼)** [GitHub Link](https://github.com/HKUST-Aerial-Robotics)
* [RAPID Laboratory](http://lab.sysu-robotics.com/index.html) **| Sun Yat-sen University - 成慧** [GitHub Link](https://github.com/SYSU-RoboticsLab)
* [MetaSLAM](https://metaslam.github.io/) **| City University of Hong Kong - 殷鹏** [GitHub Link](https://github.com/MetaSLAM)



## Conferences
* [ACM/IEEE International Conference on Human Robot Interaction (HRI)](http://ieeexplore.ieee.org/xpl/conhome.jsp?punumber=1040036)
* [CISM IFToMM Symposium on Robot Design, Dynamics and Control (RoManSy)](http://www.romansy2016.org/)
* [IEEE Conference on Decision and Controls (CDC)](http://ieeexplore.ieee.org/servlet/opac?punumber=1000188)
* [IEEE International Conference on Rehabilitation Robotics (ICORR)](http://www.rehabrobotics.org/)
* [IEEE International Conference on Robotics and Automation (ICRA)](http://www.ieee-ras.org/conferences-workshops/fully-sponsored/icra)
* [IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)](http://www.iros.org/)
* [IEEE-RAS International Conference on Humanoid Robots (Humanoids)](http://ieeexplore.ieee.org/servlet/opac?punumber=1002042)
* [International Symposium of Robotic Research (ISRR)](http://ifrr.org/isrr.php)
* [International Symposium of Experimental Robotics (ISER)](http://ifrr.org/iser.php)
* [Robotics: Science and Systems Conference (RSS)](http://www.roboticsconference.org/)
* [The International Workshop on the Algorithmic Foundations of Robotics (WAFR)](http://www.wafr.org/) 


## Journals
* [Robotics and Autonomous Systems](https://www.journals.elsevier.com/robotics-and-autonomous-systems) | **Elsevier - Impact factor: 2.259**
* [Journal of Intelligent & Robotic Systems (JINT)](https://www.springer.com/journal/10846) | **Springer - Impact factor: 2.825**
* [Transactions on Robotics (T-RO)](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=8860) | **IEEE - Impact factor: 6.123**
* [International Journal of Robotics Research (IJRR)](https://journals.sagepub.com/home/ijr) | **SAGE - Impact factor: 4.703**
* [Autonomous Robots](https://www.springer.com/journal/10514) | **Springer - Impact factor: 3.602**
* [Robotics and Computer-Integrated Manufacturing](https://www.journals.elsevier.com/robotics-and-computer-integrated-manufacturing) | **Elsevier - Impact factor: 5.057**
* [Journal of Field Robotics (JFR)](https://onlinelibrary.wiley.com/journal/15564967) | **Wiley - Impact factor: 3.581**
* [Robotics & Automation Magazine (RAM)](https://www.ieee-ras.org/publications/ram) | **IEEE - Impact factor: 4.250**
* [Robotica](https://www.cambridge.org/core/journals/robotica) | **Cambridge Core - Impact factor: 1.509**
* [Robotics and Automation Letters (RA-L)](https://www.ieee-ras.org/publications/ra-l) | **IEEE - Impact factor: 3.6**

## Courses
* [Mobile Sensing and Robotics](https://www.youtube.com/playlist?list=PLgnQpQtFTOGQJXx-x0t23RmRbjp_yMb4v) **| YouTube - Cyrill Stachniss**
* [Mobile Sensing and Robotics - 2 ](https://www.youtube.com/playlist?list=PLgnQpQtFTOGQh_J16IMwDlji18SWQ2PZ6) **| YouTube - Cyrill Stachniss**
* [Photogrametry](https://www.youtube.com/playlist?list=PLgnQpQtFTOGRsi5vzy9PiQpNWHjq-bKN1) **| YouTube - Cyrill Stachniss**
* [SLAM](https://www.youtube.com/playlist?list=PLgnQpQtFTOGQrZ4O5QzbIHgl3b1JHimN_) **| YouTube - Cyrill Stachniss**
* [Modern C++](https://www.youtube.com/playlist?list=PLgnQpQtFTOGR50iIOtO36nK6aNPtVq98C) **| YouTube - Cyrill Stachniss**
* [Become a Robotics Software Engineer](https://www.youtube.com/playlist?list=PLAwxTw4SYaPl_DVydJhS7TzeavJRTdIKV) **| YouTube -Udacity**
* [Different playlists about ROS](https://www.youtube.com/c/TheConstruct/playlists) **| YouTube - The Construct**
* [A platform to learn/teach robotics from zero](https://www.theconstructsim.com/) **| The Construct**
* [Autonomous Systems](https://www.udacity.com/school-of-autonomous-systems) **| Udacity**
* [Artificial Intelligence for Robotics](https://www.udacity.com/course/artificial-intelligence-for-robotics--cs373) **| Udacity - Prof. Dr. Sebastian Thrun**
* [C++ Essential Training](https://cpp.bw.org/) **| Bill Weinman**
* [Slides of Computer Vision](http://www.cs.cornell.edu/courses/cs4670/2013fa/lectures/lectures.html) **| Lectures from Cornell - 2013**
* [Computer Vision: Foundations and Applications](http://vision.stanford.edu/teaching/cs131_fall1415/index.html) **| Stanford University - Prof. Fei-Fei Li**
* [Interval Analysis](https://www.ensta-bretagne.fr/jaulin/iamooc.html) **| IAMOOC - Prof. Luc Jaulin**
* [Robot Mapping](http://ais.informatik.uni-freiburg.de/teaching/ws13/mapping/) **| University of Freiburg - Prof. Cyrill Stachniss**
* [JAI: Robótica e Simulação com o V-REP](https://www.sites.google.com/site/vrepjai/home) **| CSBC - Julho 2015**
* [Digital Image Processing](https://sisu.ut.ee/imageprocessing/avaleht) **| University of Tartu - Prof. Dr. Gholamreza Anbarjafari**
* [Tutorial on Visual Odometry](https://sites.google.com/site/scarabotix/tutorial-on-visual-odometry) **| University of Zurich - Prof. Davide Scaramuzza**
* [Visual SLAM Tutorial](http://www.cs.cmu.edu/~kaess/vslam_cvpr14/) **| Frank Dellaert and Michael Kaess**
* [Visual Odometry from scratch - A tutorial for beginners](https://avisingh599.github.io/vision/visual-odometry-full/) **| Avi Singh's blog**
* [Aerial Robot Courses](http://www.kostasalexis.com/courses.html) **| University of Nevada - Dr. Kostas Alexis**
* [Stereo Vision Tutorial](http://mccormickml.com/2014/01/10/stereo-vision-tutorial-part-i/) **| Chris McCormick**
* [Different ROS courses](https://www.udemy.com/courses/search/?q=ROS) **| Udemy**
* [Introduction to Mobile Robotics](http://ais.informatik.uni-freiburg.de/teaching/ss21/robotics/) **| University of Freiburg - Prof. Dr. Wolfram Burgard**
* [GaiTech EDU](https://edu.gaitech.hk/) **| Educational website on Robot Operating System (ROS)**
* [Robocademy](https://robocademy.com/) **| ROS Course from Lentin Joseph**
* [Hello (Real) World with ROS](https://www.edx.org/course/hello-real-world-with-ros-robot-operating-system) **| Delft University of Technology - edX**
* [Self-Driving Cars with ROS and Autoware](https://www.autoware.org/awf-course) **| The Autoware Foundation**
* [Programming for Robotics - ROS](https://rsl.ethz.ch/education-students/lectures/ros.html) **|ETH Zurich - Robotics System Lab**
* [CVML knowledge self-assessment](https://aiia.csd.auth.gr/cvml-knowledge-self-assessment/) **| Aristotle University of Thessaloniki - Prof. I. Pitas**
* [Think Autonomous](https://courses.thinkautonomous.ai/) **| Jeremy Cohen**
* [PyImageSearch](https://www.pyimagesearch.com/) **| Adrian Rosebrock**
* [DuckieTown](https://www.duckietown.org/) **| Learning Autonomy**
* [Machine Learning](https://www.coursera.org/learn/machine-learning?__s=4l8lmj4sp162iwy3z1p8) **| Stanford - Andrew Ng**
* [Deep Learning Specialization](https://www.coursera.org/specializations/deep-learning?__s=4l8lmj4sp162iwy3z1p8) **| Stanford - Andrew Ng**
* [OpenCV: C++ and Python](https://github.com/spmallick/learnopencv) **| Satya Mallick**
* [Awesome Self-Driving](https://github.com/Sid1057/awesome-self-driving) **| Ivan Deylid**
* [Principles of Computer Vision](https://fpcv.cs.columbia.edu/) **| Shree K. Nayar**
* [Awesome Computer Vision](https://github.com/jbhuang0604/awesome-computer-vision) **| Jia-Bin Huang**
* [Introduction to ROS: The Robot Operating System](https://tiziano-school.thinkific.com/courses/introduction-to-ros-the-robot-operating-system) **| Tiziano's school**
* [ROS Tutorials](https://erlerobotics.gitbooks.io/erle-robotics-erle-brain-a-linux-brain-for-drones/content/en/ros/rostutorials.html) **| Erle Robotics**
* [ROS Industrial Training](https://industrial-training-master.readthedocs.io/en/melodic/index.html) **| Industrial Training Exercises**
* [ROS C++ Hello World](https://jbohren.com/articles/roscpp-hello-world) **| Jonathan Bohren**
* [ROS2 C++ Hello World](https://jbohren.com/articles/rclcpp-hello-world) **| Jonathan Bohren**
* [LearnOpencv](https://learnopencv.com/) **| Satya Mallick**
* [Programming for Robotics](https://robotics.umich.edu/academic-program/courses/rob599-f19/) **| Acshi Haggenmiller (acshikh)**
* [Mathematics for Robotics](https://github.com/michiganrobotics/rob501) **| University of Michigan**
* [Introduction to the A* Algorithm](https://www.redblobgames.com/pathfinding/a-star/introduction.html) **| Red Blob Games**
* [Computer Science courses with video lectures](https://github.com/Developer-Y/cs-video-courses/blob/master/README.md) **| Developer-Y**
* [Common Path Planning Algorithms](https://github.com/KamalanathanN/PathPlanning) **| KamalanathanN**
* [PyVisualOdometry](https://github.com/polygon-software/python-visual-odometry) **| Polygon-Software**
* [KITTI Odometry in Python and OpenCV](https://github.com/FoamoftheSea/KITTI_visual_odometry) **| Nate Cibik**
* [Awesome 3D Reconstruction List](https://github.com/openMVG/awesome_3DReconstruction_list#mesh-storage-processing) **| OpenMVG**
* [ROS Autonomous Driving and Path Planning SLAM with TurtleBot3](https://github.com/noshluk2/ROS-Autonomous-Driving-and-Path-Planning-SLAM-with-TurtleBot) **| Muhammad Luqman**
* [ROS2 Ultimate learners Repository with Supporting Documentation](https://github.com/noshluk2/ROS2-Ultimate-learners-Repository) **| Muhammad Luqman**
* [ROS2 C++ learning](https://github.com/dottantgal/ROS2_learning) **| Antonio Mauro Galiano**
* [F1TENTH](https://f1tenth.readthedocs.io/en/foxy_test/index.html) **| F1TENTH Autonomous Racing Community**
* [ROS Industrial Training](https://github.com/ros-industrial/industrial_training) **| ROS Industrial**
* [ROS Book Sample Code](https://github.com/gbiggs/ros_book_sample_code) **| Programming Robots with ROS**
* [CPP Best Practices](https://github.com/cpp-best-practices/cppbestpractices) **| CPP Best Practices**
* [C++ Cheatsheet](https://github.com/mortennobel/cpp-cheatsheet) **| Modern C++ Cheatsheet**
* [Computer Vision](https://www.eecs.yorku.ca/~kosta/Courses/EECS4422/) **| Prof. Kosta Derpanis**
* [Machine Learning Course Notes](https://github.com/dair-ai/ML-Course-Notes) **| DAIR.AI**
* [Data Structure \& Algorithms 101](https://github.com/girliemac/a-picture-is-worth-a-1000-words) **| Girliemac**
* [Trending in 3D Vision](https://github.com/dragonlong/Trending-in-3D-Vision) **| Dragonlong**
* [Master Git list](https://twitter.com/NikkiSiapno/status/1559472755443220481) **| Master Git & GitHub**
* [Algorithms / Data Structures](https://github.com/girliemac/a-picture-is-worth-a-1000-words/tree/main/algorithms) **| A Picture is worth a 1000 words**
* [Udacity's autonomous car](https://github.com/udacity/self-driving-car) **| The Udacity open source self-driving car project**
* [Muhammad Luqman](https://www.youtube.com/channel/UC-QzGbqufzwncwPQlOJfUXw) **| Robotics Tutorials on YouTube by Muhammad**
* [Hummingbird](https://www.youtube.com/channel/UCPN4BAonS7QhKI-tODaA9cA/videos) **| Life in Robotics and Technology**
* [ROS Tutorials by CLEARPATH](http://www.clearpathrobotics.com/assets/guides/melodic/ros/) **| Step-by-step tutorials on ROS by Clearpath**
* [Robótica Educacional](https://www.donkeycar.com/) **| Robótica Educacional Paraná**
* [Roboflow Notebooks](https://github.com/roboflow/notebooks) **| Jupyter Notebooks with Computer Vision tutorials**
* [Autonomous Driving Lecture](https://github.com/Mayakshanesht/Autonomous_Driving_Lecture_resources) **| Autonomous driving lecture resources by Mayakshanesht**
* [C++ Best Practices](https://github.com/cpp-best-practices/cppbestpractices) **| Collaborative Collection of C++ Best Practices**
* [C++ Optimizations Diary](https://github.com/facontidavide/CPP_Optimizations_Diary) | Tips and tricks to optimize your C++ code
* [Visual SLAM Roadmap](https://github.com/changh95/visual-slam-roadmap) | Roadmap to becoming a Visual-SLAM developer in 2022 by @changh95
* [Official Repository RVSS](https://github.com/Tobias-Fischer/RVSS) | Colab notebooks for the Robotic Vision Summer School by @Tobias-Fischer
* [KF in Python](https://github.com/tbmoon/kalman_filter) | Kalman Filter in Python
* [Self Driving Cars](https://github.com/qiaoxu123/Self-Driving-Cars) | Coursera Open Courses from University of Toronto
* [Coding Notes and Tutorials](https://github.com/methylDragon/coding-notes) | A compilation of tutorials and references for different coding languages and frameworks
* [Introduction to Robotics](https://irom-lab.princeton.edu/intro-to-robotics/) | Princeton University
* [Michigan Robotics](https://robotics.umich.edu/academics/courses/online-courses/) | Michigan Robotics courses
* [Sensor Fusion Tutorial](https://github.com/methylDragon/ros-sensor-fusion-tutorial/blob/master/01%20-%20ROS%20and%20Sensor%20Fusion%20Tutorial.md) | A tutorial for sensor fusion using the robot_localization package
* [Coding Notes](https://github.com/methylDragon/coding-notes) | Coding notes in many programming languages by methylDragon
* [Rosetta Launch](https://github.com/MetroRobots/rosetta_launch) | A guide to understanding launch files in ROS 1 and ROS 2
* [Google Interview Preparation](https://github.com/mgechev/google-interview-preparation-problems) | Collection of problems and solutions of leetcode, geeksforgeeks challenges by mgechev
