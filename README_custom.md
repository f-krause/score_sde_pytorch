# Custom README 

## Activate environment on educloud
Activate virtual environment on educloud
```shell
source /projects/ec232/venvs/in5310/bin/activate
```


## Local set up
Set up virtual environment
```shell	
python -m venv venv
```

Activate custom virtual environment 
```shell
source venv/bin/activate
```

Install required packages
```shell
pip install -r requirements.txt
```

Add environment to Jupyter Notebook
```shell
python -m ipykernel install --user --name=venv
```

Create workdir and (TODO adapt later)
```shell
mkdir workdir eval
```


## Run Training
To run DDPM++ VP-SDE on CIFAR10
```shell
python main.py --config ./configs/vp/cifar10_ddpmpp.py --eval_folder 'eval' --workdir "workdir" --mode "train"
```

Run on MNIST
```shell
python main.py --config ./configs/vp/mnist_ddpmpp.py --eval_folder 'eval' --workdir "workdir" --mode "train"
```


## Run Evaluation
To evaluate DDPM++ VP-SDE
```shell
python main.py --config ./configs/vp/cifar10_ddpmpp.py --eval_folder 'eval' --workdir "workdir" --mode "eval"
```
