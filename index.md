## Human-guided Reinforcement Learning with Sim-to-real Transfer for Autonomous Navigation

[Jingda Wu](https://scholar.google.com/citations?user=icu-ZFAAAAAJ&hl=en), [Yanxin Zhou](https://www.linkedin.com/in/yanxin-zhou-91b3a51a5/?originalSubdomain=sg), [Haohan Yang](https://scholar.google.com/citations?user=KmKMahwAAAAJ&hl=en) [Zhiyu Huang](https://scholar.google.com/citations?user=aLZEVCsAAAAJ&hl=en), [Chen Lv](https://scholar.google.com/citations?user=UKVs2CEAAAAJ&hl=en) 

[AutoMan Research Lab, Nanyang Technological University](https://lvchen.wixsite.com/automan)

## Abstract
Reinforcement learning (RL) is a promising approach in unmanned ground vehicles (UGVs) applications, but limited computing resource makes it challenging to deploy a well-behaved RL strategy with sophisticated neural networks. Meanwhile, the training of RL on navigation tasks is difficult, which requires a carefully-designed reward function and a large number of interactions, yet RL navigation can still fail due to many corner cases. This shows the limited intelligence of current RL methods, thereby prompting us to rethink combining RL with human intelligence. In this paper, a human-guided RL framework is proposed to improve RL performance both during learning in the simulator and deployment in the real world. The framework allows humans to intervene in RL's control progress and provide demonstrations as needed, thereby improving RL's capabilities. An innovative human-guided RL algorithm is proposed that utilizes a series of mechanisms to improve the effectiveness of human guidance, including human-guided learning objective, prioritized human experience replay, and human intervention-based reward shaping. Our RL method is trained in simulation and then transferred to the real world, and we develop a denoised representation for domain adaptation to mitigate the simulation-to-real gap. Our method is validated through simulations and real-world experiments to navigate UGVs in diverse and dynamic environments based only on tiny neural networks and image inputs. Our method performs better in goal-reaching and safety than existing learning- and model-based navigation approaches and is robust to changes in input features and ego kinetics. Furthermore, our method allows small-scale human demonstrations to be used to improve the trained RL agent and learn expected behaviors online.

## Results

Various demos illustrating the characteristics of the proposed Multi-Hug RL method and the goal-conditioned navigation strategy are provided below. You can also access the demos via [Video1](https://youtu.be/SXM2hgY1UwM) and [Video2](https://youtu.be/AbRW-jnCiKs)

### Indoor Navigation

In this part, the autonomous navigation strategy trained in simulation is deployed in an indoor environment, for navigating a UGV to a randomly specified goal position while avoiding collision with any static and dynamic surrounding obstacles. The generalization ability of the trained strategy with respect to different UGV types, kinetics, and perception information is also evaluated. 

| Case 1 | Case 2 | Generalization |
|:-------------------------------------:|:---------------------------------------:|:---------------------------------------:|
| <video muted controls width=380> <source src="./indoor1.mp4"  type="video/mp4"> </video> | <video muted controls width=380> <source src="./indoor2.mp4"  type="video/mp4"> </video> | <video muted controls width=380> <source src="./generalization.mp4"  type="video/mp4"> </video> |


### Outdoor Navigation

In this part, the autonomous navigation strategy trained in simulation is deployed in varying outdoor environments, for navigating a UGV to a randomly specified goal position while avoiding collision with any static and dynamic surrounding obstacles. 

| Case 1 | Case 2 | Case 3 |
|:-------------------------------------:|:---------------------------------------:|:---------------------------------------:|
| <video muted controls width=380> <source src="./outdoor1.mp4"  type="video/mp4"> </video> | <video muted controls width=380> <source src="./outdoor2.mp4"  type="video/mp4"> </video> | <video muted controls width=380> <source src="./outdoor3.mp4"  type="video/mp4"> </video> |


### Physical Human-guided Fine-tuning Process

In this part, the autonomous navigation strategy is exposed in an untrained scenario (equivalent to a corner case in autonomous driving) that would be ineffective and cause collisions, while humans can take over the provide demonstrations remotely, and our method can autonomously fine-tune the navigation strategy on-the-fly, and overcome the corner case. This character is useful to addressing the long-tail issue.

<video muted controls width=380> <source src="./human guidance.mp4"  type="video/mp4"> </video>



## Contact

If you have any questions, feel free to contact us (jingda001@e.ntu.edu.sg).
