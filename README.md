# pipeline
Create a python pipeline

## 🏴‍☠️Challenge ##

### Develop a CI/CD pipeline for a Python script ###

<ul>
  <li>Create a Python script file</li>
  <li>Workflow triggered by push</li>
  <li>
  <details>
    <summary>
      <strong>Job 1:</strong> Test
    </summary>
    <p>
      <ul>
        <li><i>Check out the repo</i></li>
        <li><i>Run the script: python hello.py</i></li>
      </ul>
    </p>
  </details>
<details>
  <summary><strong>Job 2:</strong> Build </summary>
  <p> 
    <ul>
      <li>Depends on Job 1</li>
      <li>Check out the repo</li>
      <li>Create an artifact</li>
    </ul>
  </p>
</details>
</li>
</ul>


## 💡Solution ##

<h3>Steps:</h3>
<ol>
<li>Create new Repository with name pipeline for example,with a small description <br/>and check Add a Readme file</li>
<li>Create new file, hello.py and Commit new changes</li>
<li>Create .github/workflows/pipeline.yml</li>
<li>See all the details in pipeline.yml</li>
<li>We have 2 jobs: test and build:
<ul>
<li>test: Runs on ubuntu and we use actions/checkout and we run the python script</li>
<li>build: Runs on ubuntu and we use actions/checkout and action/upload-artifact with parameters name: hello and path (.) </li>
<li>with the world <i>needs</i> we set to run firstly the job test and later the job build
</ul>
</li>
</ol>
