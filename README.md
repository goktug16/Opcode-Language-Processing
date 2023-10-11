<h1>Detecting Vulnerability in Hardware Description Languages - Opcode Language Processing</h1>

<h2>Overview</h2>

<p>Our project uses a Convolutional Neural Network (CNN)-based architecture to find trojan patterns in hardware designs. We analyze both the opcode version of the Hardware Description Language (HDL) code and the HDL code itself to understand and compare the results. This helps us uncover security issues in hardware systems.</p>

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

<h2>Usage</h2>

<p>The project is designed to be easy to install and use, requiring only Jupyter Lab as the main environment. To get started, follow these simple steps:</p>

<ol>
    <li><strong>Install Jupyter Lab (if not already installed):</strong> You can install Jupyter Lab using pip with the following command:</li>
    <pre>
        <code>pip install jupyterlab</code>
    </pre>
</ol>

<p>Download Project Files:</p>

<ul>
    <li>Clone or download this repository to your local machine.</li>
</ul>

<ol start="2">
    <li><strong>Open Jupyter Lab:</strong> Launch Jupyter Lab in your terminal by running the command:</li>
    <pre>
        <code>jupyter lab</code>
    </pre>
</ol>

<ol start="3">
    <li><strong>Navigate to Project Directory:</strong> In Jupyter Lab, navigate to the directory where you downloaded the project's IPython Notebook (.ipynb) files.</li>
</ol>

<ol start="4">
    <li><strong>Run the Project:</strong> Open the desired IPython Notebook file, which contains the step-by-step model training and results. Each cell includes comments explaining the purpose of the functions and lines of code.</li>
</ol>

<ol start="5">
    <li><strong>Execute Cells Step by Step:</strong> Execute each cell one by one to observe the model training and view the results. The comments within the cells provide clear explanations of what each part of the code does.</li>
</ol>

<p>By following these steps, you can easily install, set up, and use the project within Jupyter Lab. The comments within the IPython Notebook files will guide you through the entire process, ensuring you understand the purpose of each function and line of code.</p>

<h2>Key Features</h2>

<ul>
    <li>
        <strong>Pattern Detection from HDL Code:</strong>
        <p>Instead of relying solely on traditional machine learning techniques that use numerical data, we take a unique approach. We aim to find trojan patterns directly from the Hardware Description Language (HDL) code itself.</p>
    </li>
    
<li>
        <strong>Exploring Raw HDL Code:</strong>
        <p>Initially, we analyzed raw HDL codes, including samples from both trojan-injected and trojan-free sources. However, our Convolutional Neural Network (CNN)-based architecture couldn't effectively detect patterns directly from the raw code.</p>
 </li>
    
<li>
        <strong>Comprehensive Testing:</strong>
        <p>All our experiments and testing related to HDL code processing can be found in the `HDL Processing.ipynb` file, which is readily available in our GitHub repository.</p>
    </li>
    
<li>
        <strong>Conversion to Opcodes:</strong>
        <p>In response to the initial limitations, we took an alternative approach. We transformed all HDL codes into opcodes to assess the model's ability to identify trojan patterns from opcodes.</p>
    </li>
    
<li>
        <strong>Improved Trojan Detection:</strong>
        <p>While simple machine learning models proved ineffective, our CNN-based architecture significantly enhanced trojan detection accuracy. It achieved an impressive accuracy rate of 94% when working with opcodes.</p>
    </li>
</ul>

<p>Our contributions and features represent a novel perspective on trojan detection in hardware designs, emphasizing a data-driven approach with remarkable accuracy improvements.</p>



<h2>Inserting Trojans into Hardware</h2>

<p>In our research, we employed a synthetic circuit benchmark generator, allowing the creation of circuit benchmarks with user-defined parameters. These parameters encompass depth levels, logical units, inputs/outputs, and wire counts. The objective was to evaluate the effectiveness of trojan detection methods in various hardware design scenarios.</p>

<h3>Identifying Rare Nodes</h3>

<p>The foundation of our trojan insertion approach revolves around identifying "rare nodes" within the circuit designs. These rare nodes are crucial because they represent potential points of vulnerability where trojans can be inserted. To select these nodes, we employ a vulnerability score (VS) computation:</p>

<p><strong>VS = Pr(0) * ((1 - CC0) / (CC0 + CC1))</strong></p>

<p>Where:</p>
<ul>
    <li><strong>Pr(0)</strong> represents the probability of a node transitioning to '0.'</li>
    <li><strong>CC0</strong> and <strong>CC1</strong> indicate the efforts required to guide the node to '0' and '1,' respectively.</li>
</ul>

<h3>Synthetic Trojan Insertion</h3>

<p>Based on the vulnerability score (VS) of a node, we synthetically inject trojans into the hardware designs. These trojans are carefully designed to target the rare nodes, making them particularly challenging to detect. This approach helps us assess the robustness of our trojan detection methods and their ability to uncover hidden vulnerabilities within hardware systems.</p>

<p>By systematically inserting trojans into synthetically generated benchmarks, we gain valuable insights into the performance and reliability of our trojan detection techniques. This comprehensive testing approach ensures that our methods are effective in identifying trojans across a range of scenarios, contributing to enhanced hardware security.</p>

<p>For a deeper understanding of our trojan insertion process and its impact on trojan detection, please refer to the provided documentation and research materials in our GitHub repository.</p>


