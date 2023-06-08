# Huldrych Zwingli Correspondence Network Analysis

This repository presents a Python-based network analysis of the correspondence of Huldrych Zwingli, a leader of the Reformation in Switzerland. The analysis is primarily based on data obtained from the digital project "Huldrych Zwingli Briefe: Digitale Texte" hosted by the Institute for Swiss Reformation History at the University of Zurich. This project provides the text of Zwingli's correspondence in a digital format.

The code in this repository pre-processes this data, constructs a network graph based on the senders and receivers of the letters, and visualizes this network focusing on Zwingli and his key correspondents.

## Prerequisites

To run this code, you will need to have the following libraries installed in your Python environment:

- networkx
- pandas
- matplotlib
- seaborn
- csv
- re (Regular Expressions)

## Usage

### Data Processing

The script begins by reading the 'zwingli_letters.txt' file. It uses a regular expression pattern to parse the details of each letter, including the sender, the receiver, the city from which it was sent, and the date. 

A letter connection is established between each pair of sender and receiver, and the frequency of correspondence is tracked. This data is then written to a CSV file `letter_connections.csv`.

### Network Analysis

The pandas library is used to read the generated CSV file, which contains information about the senders and receivers of the letters and the count of their correspondences. The code then creates a graph using the networkx library, with nodes representing the senders and receivers, and edges representing their correspondence. The edges are weighted based on the count of correspondences.

A subgraph is then generated centered around Zwingli, and the number of nodes and edges in the graph is printed. Degree centrality for each node is also calculated, with a special focus on Zwingli.

### Visualization

Finally, the graph is visualized using matplotlib and seaborn. The layout of the nodes is based on a spring layout, with the weight reflecting the count of correspondences. The nodes for 'Zwingli', 'Erasmus', and 'Martin Luther' are marked with different colors. Edge labels for the edges connecting these nodes are also displayed, showing the count of correspondences.

## Output

Running this code will generate a network graph, showing the correspondences between Zwingli and his correspondents. The size of the nodes corresponds to the number of correspondences, and the color of the nodes for 'Zwingli', 'Erasmus', and 'Martin Luther' is distinct from the other nodes. The graph provides a visual representation of the patterns and central figures in Zwingli's correspondence.

## Contact

Please feel free to contact joyang@ethz.ch for more information about this project or for help running the code.

## Acknowledgments

We thank the Institute for Swiss Reformation History at the University of Zurich for making the digital project "Huldrych Zwingli Briefe: Digitale Texte" available to the public. 