
# Original Repo 

Original repo is from (https://github.com/yanx27/Pointnet_Pointnet2_pytorch)


## Part Segmentation
### Run
```
## Check model in ./models 
## E.g. pointnet2_msg

python train_partseg_plant.py --model pointnet2_part_seg_msg --batch_size 1 --epoch 10000 --log_dir pointnet2_part_seg_msg --npoint 10000


python test_partseg_plant.py  --batch_size 1  --log_dir pointnet2_part_seg_msg
```
### Performance(shapeNet)
| Model | Inctance avg IoU| Class avg IoU 
|--|--|--|
|PointNet (Official)	|83.7|80.4	
|PointNet2 (Official)|85.1	|81.9	
|PointNet (Pytorch)|	84.3	|81.1|	
|PointNet2_SSG (Pytorch)|	84.9|	81.8	
|PointNet2_MSG (Pytorch)|	**85.4**|	**82.5**	




## Visualization
### Using show3d_balls.py
```
## build C++ code for visualization
cd visualizer
bash build.sh 
## run one example 
python show3d_balls.py
```
![](/visualizer/pic.png)

### Using MeshLab
![](/visualizer/pic2.png)


## Reference By
[halimacc/pointnet3](https://github.com/halimacc/pointnet3)<br>
[fxia22/pointnet.pytorch](https://github.com/fxia22/pointnet.pytorch)<br>
[charlesq34/PointNet](https://github.com/charlesq34/pointnet) <br>
[charlesq34/PointNet++](https://github.com/charlesq34/pointnet2)

## Environments
Ubuntu 16.04 <br>
Python 3.6.11 <br>
Pytorch 1.1.0
