# &#x1F6A9; Gitlab : CI Pipeline Beginner

&nbsp;

### Gitlab - Push to a repository using access_token 
git remote add origin https://&lt;access-token-name&gt;:&lt;access-token&gt;@gitlab.com/dhony21/from-gitlab-my-simple-pipeline.git

&nbsp;

&nbsp;

&nbsp;

### Begin :

&nbsp;

<div align="center">
    <img src="./gambar-petunjuk/ss_gitlab_pipeline_001.png" alt="ss_gitlab_pipeline_001" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

<div align="center">
    <img src="./gambar-petunjuk/ss_gitlab_pipeline_002.png" alt="ss_gitlab_pipeline_002" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

<div align="center">
    <img src="./gambar-petunjuk/ss_gitlab_pipeline_003.png" alt="ss_gitlab_pipeline_003" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

Files : 
<pre>
    ❯ cd from-gitlab-my-simple-pipeline

    ❯ touch info.txt

    ❯ vim info.txt

        Bismillah.
</pre>

&nbsp;

File Pipeline
<pre>
    ❯ touch .gitlab-ci.yml


    ❯ vim .gitlab-ci.yml


        stages:
            - build
            - test
        
        build:
            stage: build
            script:
                - echo "Building"
                - mkdir build
                - touch build/info.txt
            artifacts:
                paths:
                    - build/
            
        test:
            stage: test
            script:
                - echo "Testing"
                - test -f build/info.txt    
</pre>

&nbsp;

In gitlab, for the pipeline to automatically activate when the repository recognizes the `.gitlab-ci.yml' file.
<pre>
    ❯ git init

    ❯ git add .

    ❯ git commit -m "Initial commit"

    ❯ git branch -M main

    ❯ git remote add origin https://&lt;access-token-name&gt;:&lt;access-token&gt;@gitlab.com/dhony21/from-gitlab-my-simple-pipeline.git

    ❯ git push -u origin main
</pre>

&nbsp;

<div align="center">
    <img src="./gambar-petunjuk/ss_gitlab_pipeline_004.png" alt="ss_gitlab_pipeline_004" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

<div align="center">
    <img src="./gambar-petunjuk/ss_gitlab_pipeline_005.png" alt="ss_gitlab_pipeline_005" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

<div align="center">
    <img src="./gambar-petunjuk/ss_gitlab_pipeline_006.png" alt="ss_gitlab_pipeline_006" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

<div align="center">
    <img src="./gambar-petunjuk/ss_gitlab_pipeline_007.png" alt="ss_gitlab_pipeline_007" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

<div align="center">
    <img src="./gambar-petunjuk/ss_gitlab_pipeline_008.png" alt="ss_gitlab_pipeline_008" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

<div align="center">
    <img src="./gambar-petunjuk/ss_gitlab_pipeline_009.png" alt="ss_gitlab_pipeline_009" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

&nbsp;

---

&nbsp;

<div align="center">
    <img src="./gambar-petunjuk/well_done.png" alt="well_done" style="display: block; margin: 0 auto;">
</div> 

&nbsp;

---

&nbsp;

&nbsp;

&nbsp;