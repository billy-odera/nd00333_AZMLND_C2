
# Project - Operationalizing Machine Learning

We used the <a href= 'https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv'> bank marketing dataset </a> to train, configure and deploy a machine learning model using  Azure Machine Learning Studio.

## Architectural Diagram

<p> Below is the architectural diagram that we will follow </p>
<img src= 'https://github.com/billy-odera/nd00333_AZMLND_C2/blob/master/a.jpg'>

<p> The steps are as follows :
<ol>
  <li>Load your dataset to azure ML studio</li>
  <li>Run the AutoML model using classification/li>
  <li>Select the best model and deploy using azure container instance(ACI)</li>
  <li>Enable insights to keep track of what is happening.</li>
  <li>Use the REST endpoint to interact with the deployed model with sample data and check predictions. </li>
  <li>Using python SDK create a pipeline selecting the best AutoML model and publish it.</li>
</ol>
</p>

## Key Steps

### 1. AutoML run
<section>
  <p> Create an experiment using Automated ML, configured a compute cluster, and used that cluster to run the experiment. Below screenshots highlight the steps. The best model was the voting ensemble</b> with an approximate accuracy of <b>91.9%</b>
  </p>
  <p>   
    <img src= 'https://github.com/billy-odera/nd00333_AZMLND_C2/blob/master/1.jpg' />
    <img src= 'https://github.com/billy-odera/nd00333_AZMLND_C2/blob/master/2.jpg' />
    <img src= 'https://github.com/billy-odera/nd00333_AZMLND_C2/blob/master/3.jpg' />
  </p>
</section>

### 2. Deploy and consume best model
<section>
  <p> We deployed the best model as captured below :
    <ul>
      <li> Enable logs </li>
      <li> Application insights enabled </li>
      <li> Use swagger to document anf consume the  RESTful web services </li>
    </ul>
  </p>
  <p>
    <img src= 'https://github.com/billy-odera/nd00333_AZMLND_C2/blob/master/4.jpg'/>
    <img src= 'https://github.com/billy-odera/nd00333_AZMLND_C2/blob/master/5.jpg' />
    <img src= 'https://github.com/billy-odera/nd00333_AZMLND_C2/blob/master/6.jpg' />
    </p>
    <p> Run the <i>endpoint.py</i> file which contains rest endpoint url to interact with the deployed model. Below is the output of the model.
    <img src= 'https://github.com/billy-odera/nd00333_AZMLND_C2/blob/master/7.jpg' />
  </p>
   <p> Run the <i>benchmark.sh</i>as captured below.
    <img src= 'https://github.com/billy-odera/nd00333_AZMLND_C2/blob/master/8.jpg' />
  </p>
</section>

### 3. Publish Machine Learning  Pipeline
<section>
  We use python SDK to create and publish the pipeline, as captured in the images beelow.
  <ul>
    <li> pipeline scheduled run details </li>
    <li> pipeline created successfully </li>
    <li> pipeline REST endpoint in active state </li>
  </ul>
  <p>
    <img src= 'https://github.com/billy-odera/nd00333_AZMLND_C2/blob/master/11.jpg'/>
    <img src= 'https://github.com/billy-odera/nd00333_AZMLND_C2/blob/master/12.jpg'/>
    <img src= 'https://github.com/billy-odera/nd00333_AZMLND_C2/blob/master/13.jpg'/>
    <img src= 'https://github.com/billy-odera/nd00333_AZMLND_C2/blob/master/14.jpg'/>
  </p>
</section>

### Future Work

<p> 
  <ul>
    <li> creating a front end web page to enhance interaction </li>

  </ul>
</p>
### Screen Recording

[![Azure ML Project](http://img.youtube.com/vi/KymP0PYUr7I/0.jpg)](https://www.youtube.com/watch?v=KymP0PYUr7I "Azure ML project")


