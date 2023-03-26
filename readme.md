# The readme file

document is about how to get colab ready for chatGPT before running the colab code in this repository.

## chatGPT API

[https://platform.openai.com/docs/quickstart/build-your-application](https://platform.openai.com/docs/quickstart/build-your-application)


## Installation



1. install anaconda
2. Create a conda environment for the chatgpt project
    1. run in terminal “conda create --name chatgpt_api python=3.10”
    2. run in terminal “conda activate chatgpt_api”
3. Install the necessary packages for colab notebook (optional, [link here](https://research.google.com/colaboratory/local-runtimes.html))
    3. pip install jupyterlab
    4. pip install jupyter_http_over_ws
    5. jupyter serverextension enable --py jupyter_http_over_ws
    6. pip install --upgrade jupyter_http_over_ws>=0.0.7 &&   jupyter serverextension enable --py jupyter_http_over_ws
    7. done with the colab installation

(from here, the instruction is documented in [this link](https://platform.openai.com/docs/api-reference/introduction))



4. install open ai API tool kit by executing in terminal “pip install openai”
5. Get api keys by going to [this site](https://platform.openai.com/docs/api-reference/introduction) and click on personal -> view API keys



<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image1.png "image_tooltip")




<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image2.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image2.png "image_tooltip")


(the following is covered in the API safety best practice in [this link](https://help.openai.com/en/articles/5112595-best-practices-for-api-key-safety))



6. Set up the API key in the environment variable (mac/linux -> option 2):
    8. Set the api key as an environment variable by running in terminal “echo "export OPENAI_API_KEY='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'" >> ~/.bash_profile“
    9. Update the shell with new variable by running in terminal ”source ~/.bash_profile“
    10. Test if you can get this variable by running in terminal “echo $OPENAI_API_KEY”
    11. done on the API key environment steup
7. 


## Run the code



1. Activate conda environment by running in terminal “conda activate chatgpt_api”
2. Start notebook by running in terminal ”jupyter notebook  --NotebookApp.allow_origin='https://colab.research.google.com'  --port=8888 --NotebookApp.port_retries=0”, where the port id can be other values.
3. You will find the URL in the terminal (highlighted in light blue below), copy the highlighted URL.

    

<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image3.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image3.png "image_tooltip")


4. Go to [https://colab.research.google.com/](https://colab.research.google.com/), and click on the “new notebook” at the bottom right corner

    

<p id="gdcalert4" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image4.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert5">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image4.png "image_tooltip")


5. You are looking at a blank python notebook. click on the connect button on the upper right corner

    

<p id="gdcalert5" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image5.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert6">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image5.png "image_tooltip")


6. Paste the URL in the previous step into the backend URL (replace red words)

	

<p id="gdcalert6" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image6.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert7">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image6.png "image_tooltip")




7. in the colab, enter the following code “ 

        import os


        import openai


        openai.api_key = os.environ["OPENAI_API_KEY"]


    ”
8. Run the colab in this repository!
