

## Components

### StopWordSkipper Application

#### Overview
The StopWordSkipper application utilizes Hadoop's distributed processing capabilities to filter out stop words from large datasets efficiently. It consists of two main components: the Mapper class (`SkipMapper`) and the main driver class (`StopWordSkipper`).

#### SkipMapper Class
- **Setup:** Initializes the stop word list by reading from a distributed cache file.
- **Read Stop Word File:** Populates the stop word list from the file.
- **Map:** Core function that filters out stop words from each line of input text.

#### StopWordSkipper Class
- **Configuration Setup:** Includes job name, output key/value classes, and mapper class.
- **Distributed Cache Configuration:** Adds the stop word file to the distributed cache.
- **Input/Output Format:** Specifies the formats for the MapReduce job.
- **Execution:** Initiates the Hadoop job and awaits its completion.
- **Counters Retrieval:** Retrieves and displays counts of good words and stop words.

### Personalized Medicine Recommendation

#### Approach
This component leverages NLP techniques for providing medication recommendations tailored to patient data. The process involves data preprocessing, text normalization, vectorization, similarity measurement, and recommendation retrieval.

- **Data Preprocessing:** Removes missing values and structures the dataset.
- **Text Normalization:** Utilizes stemming for consistent text representation.
- **Vectorization:** Converts text into numerical representations using techniques like `CountVectorizer`.
- **Cosine Similarity:** Measures similarity between medication vectors to identify closely related medications.
- **Recommendation Function:** Retrieves top similar medications based on user input.
- **Saving Data:** Ensures efficient retrieval and scalability by saving the preprocessed dataset and similarity matrix.

## Getting Started

To run this project, ensure you have Hadoop set up for the StopWordSkipper application and an appropriate Python environment for the personalized medicine recommendation system.

### Prerequisites

- Hadoop
- Python 3.x
- Libraries: numpy, scikit-learn

### Installation

Clone this repository and navigate to the project directory. Install the required Python libraries using:

```bash
pip install numpy scikit-learn
