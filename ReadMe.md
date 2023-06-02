### ReadME

## Objective
The objective of this project is to develop a speech separation system for multi-talker environment with two or more speakers. 

## Description 
In this project, we have developed a deep learning solution for single-channel speaker independent speech separation system.

It allows a user to separate speech of individual speaker from an audio clip having multiple speaker speaking simultaneously.


Operating System - Windows 10/11

Softwares : 
	
		- Python 3
		- Nvidia Cuda 11.4 
		- CUDA Deep Neural Network (cuDNN)
		- Jupyter Notebook
		- Visual Studio Code
		- Git bash
		- Sound eXchange [SoX 14.4.2]
	

# Class Description
	1. Class: Deep model
		- It is a class implementing various methods for creating speech separation models on demand.
		- It contain various methods such as:
			__init__(): It is a constructor function which takes keyworded arguments containing parameters used for model creation.
						For example: n_src(number of speakers), n_filter(number of filter), sample_rate, stride etc
			get_model(): It return the model created as per user requirement.
			create_conv_model(): It created ConvTasNet model as per the specifications provided by the developer.
			create_dprnn_model(): It created DPRNNTasNet model as per the user requirement.
			load_my_model(): It is used to load a model from its saved copy.  


	2. Class: Training
		- It is a model training class which train model on data provided by user in the form of train loaders.
		- It contain various methods such as:
			__init__(): It is a constructor function which initializes various parameters, setup model trainer and train the model.
			get_optimizer(): It returns optimizer functions required in model training.
			setup_system(): It implements system object which is a wrapper class
			clear_cache(): It is used to clear cache memory of GPU.
			get_gpu_memory_summary(): It retrieve memory summary of GPU being used in training.


	3. Class: Tester
		- It is a tester class which take model and run test audio separation and generate output in test directory.
		- It contain following methods:
			__init__(): It initializes model and test directory parameters required for test audio separation.
			prepare_test(): It removes previous test file and result from test directory prepairing it for next test.
			test(): It prepares the test directory, creates a copy of test speech and run separation function on test file from model.
		    view_results(): It displays test sample and their result speeches. 



# Contributor
1. Dhruv Saini  
     . LinkedIN - https://www.linkedin.com/in/dhruv73     
     
# Requirements
	
	Hardware
		[Laptop]
			- CPU: Intel Core i5-8300H 
			- Memory: 8GB 
			- GPU: NVIDIA GeForce GTX 1050ti
			- Disk Space: 300GB
		
		[Google Colab]
			- System RAM: 12.7 GB
			- Disk: 107.7 GB
			- GPU Type: T4
			  or TPU
	
