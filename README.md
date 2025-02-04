
<body>
  <h1>Screentime Analysis with Deep Learning</h1>
  
  <div class="badge">
    <a href="https://colab.research.google.com/github/Praveenkumarbalaji/Screentime_Analysis_Deeplearning/blob/main/Screentime_Analysis_Deeplearning.ipynb" target="_parent">
      <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
    </a>
  </div>
  
  <h2>Overview</h2>
  <p>
    This notebook demonstrates a deep learning approach to analyzing screentime data. The analysis includes:
  </p>
  <ul>
    <li>Loading a screentime dataset (from <code>screentime_analysis.csv</code>) containing metrics such as Date, App, Usage (minutes), Notifications, and Times Opened.</li>
    <li>Data preprocessing using a <code>MinMaxScaler</code> to normalize numerical features.</li>
    <li>Building and summarizing a neural network model (a Generative Adversarial Network, GAN) with Keras – including both a generator and a discriminator.</li>
    <li>Training the GAN on the normalized screentime data to generate synthetic data samples.</li>
    <li>Displaying model summaries and generated synthetic data for evaluation.</li>
  </ul>
  
  <h2>Table of Contents</h2>
  <ul>
    <li><a href="#overview">Overview</a></li>
    <li><a href="#installation">Installation &amp; Dependencies</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#model">Model &amp; Training Details</a></li>
    <li><a href="#results">Results</a></li>
    <li><a href="#structure">Notebook Structure</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
    <li><a href="#license">License</a></li>
  </ul>
  
  <h2 id="installation">Installation &amp; Dependencies</h2>
  <p>
    The notebook requires the following:
  </p>
  <ul>
    <li>Python 3.x</li>
    <li>TensorFlow and Keras</li>
    <li>scikit-learn</li>
    <li>pandas and numpy</li>
    <li>Matplotlib</li>
    <li>A CSV file (<code>screentime_analysis.csv</code>) containing your screentime data</li>
  </ul>
  <p>
    In a Colab environment you can install additional packages (if needed) via pip. For example:
  </p>
  <pre><code>!pip install tensorflow scikit-learn pandas numpy matplotlib</code></pre>
  
  <h2 id="usage">Usage</h2>
  <ol>
    <li>
      <strong>Open the Notebook:</strong> Click the Colab badge above to open the notebook in Google Colab.
    </li>
    <li>
      <strong>Run Cells Sequentially:</strong> Execute each cell from top to bottom. The notebook will:
      <ul>
        <li>Load the screentime dataset and display a preview.</li>
        <li>Normalize the data using MinMaxScaler.</li>
        <li>Build the generator and discriminator models for the GAN.</li>
        <li>Train the GAN on the normalized data.</li>
        <li>Generate synthetic data samples and display the output.</li>
      </ul>
    </li>
    <li>
      <strong>Review Outputs:</strong> Check the model summaries and the generated data outputs to assess the performance of the GAN.
    </li>
  </ol>
  
  <h2 id="model">Model &amp; Training Details</h2>
  <p>
    The notebook builds a GAN consisting of:
  </p>
  <ul>
    <li>A <strong>Generator</strong> model that accepts a latent noise vector (of dimension 100) and outputs synthetic screentime feature values.</li>
    <li>A <strong>Discriminator</strong> model that receives feature vectors (with three values corresponding to Usage, Notifications, and Times Opened) and classifies them as real or fake.</li>
  </ul>
  <p>
    The GAN is compiled with binary crossentropy loss and is trained in batches for a specified number of epochs. Progress is printed every 1000 epochs.
  </p>
  
  <h2 id="results">Results</h2>
  <p>
    After training, the notebook displays:
  </p>
  <ul>
    <li>The summary of the generator, discriminator, and GAN models.</li>
    <li>Sample synthetic data generated by the GAN, along with its inverse-transformed values to the original scale.</li>
  </ul>
  
  <h2 id="structure">Notebook Structure</h2>
  <pre>
Screentime_Analysis_Deeplearning.ipynb   // Main notebook file
screentime_analysis.csv                  // Screentime dataset file
README.html                              // This README file in HTML format
  </pre>
  
  <h2 id="acknowledgements">Acknowledgements</h2>
  <p>
    This notebook uses open-source tools and libraries such as TensorFlow, Keras, scikit-learn, and pandas. Special thanks to the contributors of these projects.
  </p>
  
  <h2 id="license">License</h2>
  <p>
    This project is licensed under the MIT License.
  </p>
</body>
</html>
