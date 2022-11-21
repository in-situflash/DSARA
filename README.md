# DSARA
Training and Testing Code for DSARA. The code is modified from the code provided by [AdvRush](https://github.com/nutellamok/advrush) 

## Environmental Set-up
```
Python == 3.6.12, PyTorch == 1.2.0, torchvision == 0.4.0
```


## Adversarial Training
```
cd advrush && python adv_train.py --batch_size 32 --gpu 2 --epochs 200 --adv_loss pgd --arch DSARA
```

## Evaluation under PGD Attack
Prior to the evaluation process, add all necessary checkpoint files (preferably in the form of .pth.tar) to the /eval/EXP folder.
To conduct white-box attacks, 
```
cd eval &&
python pgd_attack.py --white-box-attack True --test_best True --test-batch-size 10 --arch [arch_name] --data_type [cifar10/svhn]
```


## References

[AdvRush: Searching for Adversarially Robust Neural Architectures](https://openaccess.thecvf.com/content/ICCV2021/html/Mok_AdvRush_Searching_for_Adversarially_Robust_Neural_Architectures_ICCV_2021_paper.html) (ICCV '21)
