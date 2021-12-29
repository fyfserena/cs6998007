# cs6998007

# cs6998fall2021 FinalProject

## Project Description and results please view Final Project Report yf2549.pdf

## Background Work
![image](https://github.com/fyfserena/cs6998012PraticalDLFinalProject/blob/main/Mind%20map%20with%20lines.png)

## Experiment Chart
![image](https://github.com/fyfserena/cs6998012PraticalDLFinalProject/blob/main/Support%20process%20example.png)

## Code structure: 
**SimCLR:** simclr pretrain framework

            usage: python pretrain/run.py -data ./datasets --dataset-name cifar10 --log-every-n-steps 100 --epochs 200 --batchsize 256
            
**finetune:** fine tune model with partial labeled data (adversarial training data)

            usage: python finetune/main.py --data cifar10 --batch_size 128 --pretrained_model <output pt file from previos step> --save_dir True --gpu 0 --partial 0.01 
            
**attack** generate adversarial example from cifar10 test data using FGSM

            usage: python attack/pgd_attack_cifar10.py

**Code Reference:**
* https://github.com/sthalles/SimCLR/tree/1848fc934ad844ae630e6c452300433fe99acfd9
* https://github.com/VITA-Group/Adv-SS-Pretraining
* https://github.com/yaodongyu/TRADES
