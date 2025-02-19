This Folder Contains the Training and Inference code of RODAM model.

For Training :
--------------
In rodam_training.py file, At bottom set the required file locations.
1) src_data_dir -- source data file path 
2) tgt_data_dir -- target data file path
3) model_save_path -- location, where you want to save the model
4) model_save_name -- name of the saved model (extension should be .pt)
5) checkpoint_name -- checkpoint model name
6) batch_size -- batch size
7) epochs
8) device - 0 (gpu-0), 1 (gpu-1)

Note -- source and target file format should be .jsonl file. In source and target, there should be 6 files, which are :
real.train -- train set human texts [text, text_perturb, label = 1]
real.valid -- valid set human texts [text, text_perturb, label = 1]
real.test -- test set human texts [text, text_perturb, label = 1]

fake.train -- train set ai texts [text, text_perturb, label = 0]
fake.valid -- valid set ai texts [text, text_perturb, label = 0]
fake.test -- test set ai texts [text, text_perturb, label = 0]


For Inferencing :
-----------------

In rodam_inference.py, go to Intitialization section (line no - 65)
Set the saved model path, inference dataset path and prediction saved path.

After the Program completion, the predictions are saved at the prediction saved path and the Performance is displayed in the ouput screen.
