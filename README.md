# Detecting-Vulnerability-in-Hardware-Description-Languages-Opcode-Language-Processing

**Overview:** 

Our project uses a Convolutional Neural Network (CNN)-based architecture to find trojan patterns in hardware designs. We analyze both the opcode version of the Hardware Description Language (HDL) code and the HDL code itself to understand and compare the results. This helps us uncover security issues in hardware systems.

<h2>Installation and Setup</h2>

<p>To run this project, users will need to have the following libraries installed:</p>

<ul>
    <li>nltk</li>
    <li>zipfile</li>
    <li>pandas</li>
    <li>numpy</li>
    <li>keras</li>
    <li>tensorflow</li>
    <li>scikit-learn (sklearn)</li>
    <li>nlpaug</li>
    <li>matplotlib</li>
    <li>seaborn</li>
</ul>

<p>Users can install these libraries using Python's package manager, pip. The following command should be used for each library:</p>

<pre>
    <code>pip install library-name</code>
</pre>

<p>Replace "library-name" with the name of the library they want to install.</p>


<h3>Implementation Environment</h3>

<h4>Using Anaconda (Recommended)</h4>

<p>For a hassle-free setup, it's recommended to use Anaconda. Follow these steps to set up the environment and install Jupyter Lab:</p>

<ol>
    <li><strong>Install Anaconda:</strong> If you don't have Anaconda installed, download and install it from the <a href="https://www.anaconda.com/products/distribution" target="_blank">Anaconda website</a>.</li>
    <li><strong>Create a New Anaconda Environment:</strong> Create a new Python environment for your project. Replace <code>myenv</code> with your desired environment name and specify the Python version you want to use (e.g., <code>python=3.8</code>).</li>
    <pre>
        <code>conda create --name myenv python=3.8</code>
    </pre>
    <li><strong>Activate the Environment:</strong> Activate the newly created environment.</li>
    <pre>
        <code>conda activate myenv</code>
    </pre>
    <li><strong>Install Jupyter Lab:</strong> Use conda to install Jupyter Lab within the activated environment.</li>
    <pre>
        <code>conda install -c conda-forge jupyterlab</code>
    </pre>
    <li><strong>Launch Jupyter Lab:</strong> Start Jupyter Lab by running the following command in your terminal. This will open Jupyter Lab in your default web browser.</li>
    <pre>
        <code>jupyter lab</code>
    </pre>
    <li><strong>Navigate to the Project Directory:</strong> In Jupyter Lab, navigate to the directory where the IPython Notebook (.ipynb) files are located.</li>
    <li><strong>Open and Run Notebooks:</strong> Users can open the desired IPython Notebook file and execute the code cells as needed.</li>
</ol>

<p>By following these steps, users can easily set up an Anaconda environment and install Jupyter Lab for running the project's code.</p>





