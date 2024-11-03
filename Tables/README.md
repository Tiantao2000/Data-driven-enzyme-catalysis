# Table 1 Representation methods for enzyme catalysis

|Method|Description|Visualization|Ref<sup>a</sup>|
| :-: | :-: | :-: | :-: |
|**Reaction**||||
|SMILES|A specification in the form of a line notation for describing the structure.|CCO>> CC=O|<sup>1</sup>|
|Fingerprint|Vectorization of reactions using methods like symmetric difference or self-supervised learning.|[0, 0, 0, 1, …, -1]|<sup>2</sup>|
|Template|The substructures of molecules that participate in the reaction.|[C;H0:2]([OH:3])=[O:4]>>CC[O:3][C;HO:2](=[O:4])|<sup>3</sup>|
|Reaction graph|The graph representation of reactions which contains the nodes for chemical species and edges for interactions between them.|![](data:image/png;base64,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)|<sup>4</sup>|
|**Pathway**||||
|Tree graph|An undirected graph representing a pathway where any two nodes are connected by exactly one path.|![](data:image/png;base64,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)|<sup>5</sup>|
|Hypergraph|The graph representation contains hyperedges that can join multiple nodes.|![](data:image/png;base64,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)|<sup>6</sup>|
|Large-scale network|A network representation at macro scales, typically used for metabolic systems.||<sup>11</sup>|

<sup>a</sup>The selected reference is a classic example of using or describing the corresponding representation.

# Table 2 Major databases for enzyme catalysis 

|Database|Data|Website|` `Date|Ref|
| :-: | :-: | :-: | :-: | :-: |
|BRENDA|22912 reactions, 59868 specific activities, 8423 EC numbers|https://www.brenda-enzymes.org|2023\.1|<sup>13</sup>|
|KEGG|12102 biochemical reactions, 572 pathway graphs, 8158 EC numbers|https://www.kegg.jp/kegg/|2024\.7|<sup>14</sup>|
|MetaCyc|19020 reactions, 3153 pathways, 6741 EC numbers, 14437 enzymes|https://metacyc.org/|2024\.4|<sup>15</sup>|
|Rhea|16609 chemical and transport reactions of biological interest|https://www.rhea-db.org/|2024\.5|<sup>16</sup>|
|Reactome|15326 reactions, 2711 human pathways|https://reactome.org/|2024\.6|<sup>17</sup>|
|SABIO-RK|9872 reactions|http://sabio.h-its.org/|2024\.7|<sup>18</sup>|
|EAWAG|1503 reactions, 219 pathways, 993 enzymes|http://eawag-bbd.ethz.ch/|2016\.1|<sup>19</sup>|
|BioCatNet-DB|Experimental bio-catalytic measurement data, reaction conditions, and kinetic modeling|https://www.biocatnet.de/|2018|<sup>20</sup>|
|SciFinder|1180121 references related to enzyme catalysis|https://scifinder-n.cas.org|2024\.7|<sup>21</sup>|
|Reaxys|89583 reactions|https://www.reaxys.com/|2024\.7|<sup>22</sup>|
|RetroBioCat-DB|20083 reactions,1489 enzymes|https://retrobiocat.com/|2023\.11|<sup>23</sup>|





# Table 3 *De novo* pathway expansion methods

|Method|Single-step model|Search algorithm|Additional Information |Ref|
| :-: | :-: | :-: | :-: | - |
|***Uninformed search***|||||
|NICEPATH|Template-based|K-shortest search|Introducing the penalty for conserved atom ratio |<sup>24</sup>|
|BNICE|Template-based|DFS or BFS search|-|<sup>25</sup>|
|ATLASx|Template-based|K-shortest search|Expansion to chemoenzymatic biotransformation|<sup>26</sup>|
|RDEnzyme|Template-based|Similarity-based search|Employing evolution scoring to assign sequence|<sup>27</sup>|
|NovoPathFinder|Template-based|Similarity-based search|<h3>-</h3>|<sup>28</sup>|
|Probst et al.|Template-free|Beam search|Capturing biotransformation patterns from EC numbers|<sup>29</sup>|
|RetroBioCat|Template-based|Beam search|Focusing on chemoenzymatic biotransformation|<sup>3</sup>|
|***Informed search***|||||
|RetroPath RL|Template-based|MCTS|-|<sup>30</sup>|
|BioNavi-NP|Template-free|Retro\* Search|Revealing pathways to Nature Products (NPs)|<sup>31</sup>|
|Levin et al.|Template-based|MCTS|Merging the bio- and organic transformation|<sup>32</sup>|
|Zhao et al.|Template-based|MEEA\* search|-|<sup>33</sup>|
|TTLAB|Template-free|Best-first tree search|Focusing on chemoenzymatic biotransformation|<sup>34</sup>|
|ReadRetro|Template-free|Retro\* Search|Revealing the pathways of complex metabolites|<sup>35</sup>|
|Sankaranarayanan et al.|Template-based|MCTS|Focusing on chemoenzymatic biotransformation|<sup>36</sup>|






# Reference

1.	Weininger, D. (1988). SMILES, a chemical language and information system. 1. Introduction to methodology and encoding rules. Journal of chemical information and computer sciences *28*, 31-36.

2.	Xing, H., Cai, P., Liu, D., Han, M., Liu, J., Le, Y., Zhang, D., and Hu, Q.-N. (2024). High-throughput prediction of enzyme promiscuity based on substrate–product pairs. Briefings in Bioinformatics *25*, bbae089.

3.	Finnigan, W., Hepworth, L.J., Flitsch, S.L., and Turner, N.J. (2021). RetroBioCat as a computer-aided synthesis planning tool for biocatalytic reactions and cascades. Nature catalysis *4*, 98-104.

4.	Heid, E., and Green, W.H. (2021). Machine learning of reaction properties via learned representations of the condensed graph of reaction. Journal of Chemical Information and Modeling *62*, 2101-2110.

5.	Zhang, X., Liu, J., Yang, F., Zhang, Q., Yang, Z., and Shah, H.A. (2024). Planning biosynthetic pathways of target molecules based on metabolic reaction prediction and AND-OR tree search. Computational Biology and Chemistry, 108106.

6.	Chen, C., Liao, C., and Liu, Y.-Y. (2023). Teasing out missing reactions in genome-scale metabolic networks through hypergraph learning. Nature Communications *14*, 2375.

7.	Al-Anzi, B., Arpp, P., Gerges, S., Ormerod, C., Olsman, N., and Zinn, K. (2015). Experimental and computational analysis of a large protein network that controls fat storage reveals the design principles of a signaling network. PLoS computational biology *11*, e1004264.

8.	Kreutter, D., Schwaller, P., and Reymond, J.-L. (2021). Predicting enzymatic reactions with a molecular transformer. Chemical science *12*, 8648-8659.

9.	Yu, T., Cui, H., Li, J.C., Luo, Y., Jiang, G., and Zhao, H. (2023). Enzyme function prediction using contrastive learning. Science *379*, 1358-1363.

10.	Nanni, L., and Brahnam, S. (2020). Set of approaches based on position specific scoring matrix and amino acid sequence for primary category enzyme classification. Journal of Artificial Intelligence and Systems *2*, 38-52.

11.	Yue, Z.-X., Yan, T.-C., Xu, H.-Q., Liu, Y.-H., Hong, Y.-F., Chen, G.-X., Xie, T., and Tao, L. (2023). A systematic review on the state-of-the-art strategies for protein representation. Computers in Biology and Medicine *152*, 106440.

12.	Senior, A.W., Evans, R., Jumper, J., Kirkpatrick, J., Sifre, L., Green, T., Qin, C., Žídek, A., Nelson, A.W., and Bridgland, A. (2020). Improved protein structure prediction using potentials from deep learning. Nature *577*, 706-710.

13.	Chang, A., Jeske, L., Ulbrich, S., Hofmann, J., Koblitz, J., Schomburg, I., Neumann-Schaal, M., Jahn, D., and Schomburg, D. (2021). BRENDA, the ELIXIR core data resource in 2021: new developments and updates. Nucleic acids research *49*, D498-D508.

14.	Kanehisa, M., Furumichi, M., Sato, Y., Kawashima, M., and Ishiguro-Watanabe, M. (2023). KEGG for taxonomy-based analysis of pathways and genomes. Nucleic acids research *51*, D587-D592.

15.	Caspi, R., Billington, R., Keseler, I.M., Kothari, A., Krummenacker, M., Midford, P.E., Ong, W.K., Paley, S., Subhraveti, P., and Karp, P.D. (2020). The MetaCyc database of metabolic pathways and enzymes-a 2019 update. Nucleic acids research *48*, D445-D453.

16.	Bansal, P., Morgat, A., Axelsen, K.B., Muthukrishnan, V., Coudert, E., Aimo, L., Hyka-Nouspikel, N., Gasteiger, E., Kerhornou, A., and Neto, T.B. (2022). Rhea, the reaction knowledgebase in 2022. Nucleic acids research *50*, D693-D700.

17.	Milacic, M., Beavers, D., Conley, P., Gong, C., Gillespie, M., Griss, J., Haw, R., Jassal, B., Matthews, L., and May, B. (2024). The reactome pathway knowledgebase 2024. Nucleic acids research *52*, D672-D678.

18.	Wittig, U., Rey, M., Weidemann, A., Kania, R., and Müller, W. (2018). SABIO-RK: an updated resource for manually curated biochemical reaction kinetics. Nucleic acids research *46*, D656-D660.

19.	Gao, J., Ellis, L.B., and Wackett, L.P. (2010). The University of Minnesota biocatalysis/biodegradation database: improving public access. Nucleic acids research *38*, D488-D491.

20.	Buchholz, P.C., Vogel, C., Reusch, W., Pohl, M., Rother, D., Spieß, A.C., and Pleiss, J. (2016). BioCatNet: a database system for the integration of enzyme sequences and biocatalytic experiments. ChemBioChem *17*, 2093-2098.

21.	Ridley, D.D. (2002). Information Retrieval: SciFinder and SciFinder Scholar (John Wiley & Sons).

22.	Goodman, J. (2009). Computer software review: Reaxys.  ACS Publications.

23.	Finnigan, W., Lubberink, M., Hepworth, L.J., Citoler, J., Mattey, A.P., Ford, G.J., Sangster, J., Cosgrove, S.C., da Costa, B.Z., and Heath, R.S. (2023). RetroBioCat database: a platform for collaborative curation and automated meta-analysis of biocatalysis data. ACS catalysis *13*, 11771-11780.

24.	Hafner, J., and Hatzimanikatis, V. (2021). NICEpath: Finding metabolic pathways in large networks through atom-conserving substrate–product pairs. Bioinformatics *37*, 3560-3568.

25.	Hatzimanikatis, V., Li, C., Ionita, J.A., Henry, C.S., Jankowski, M.D., and Broadbelt, L.J. (2005). Exploring the diversity of complex metabolic networks. Bioinformatics *21*, 1603-1609.

26.	Hafner, J., MohammadiPeyhani, H., Sveshnikova, A., Scheidegger, A., and Hatzimanikatis, V. (2020). Updated ATLAS of biochemistry with new metabolites and improved enzyme prediction power. ACS synthetic biology *9*, 1479-1482.

27.	Sankaranarayanan, K., Heid, E., Coley, C.W., Verma, D., Green, W.H., and Jensen, K.F. (2022). Similarity based enzymatic retrosynthesis. Chemical Science *13*, 6039-6053.

28.	Ding, S., Tian, Y., Cai, P., Zhang, D., Cheng, X., Sun, D., Yuan, L., Chen, J., Tu, W., and Wei, D.-Q. (2020). novoPathFinder: a webserver of designing novel-pathway with integrating GEM-model. Nucleic acids research *48*, W477-W487.

29.	Probst, D., Manica, M., Nana Teukam, Y.G., Castrogiovanni, A., Paratore, F., and Laino, T. (2022). Biocatalysed synthesis planning using data-driven learning. Nature communications *13*, 964.

30.	Koch, M., Duigou, T., and Faulon, J.-L. (2019). Reinforcement learning for bioretrosynthesis. ACS synthetic biology *9*, 157-168.

31.	Zheng, S., Zeng, T., Li, C., Chen, B., Coley, C.W., Yang, Y., and Wu, R. (2022). Deep learning driven biosynthetic pathways navigation for natural products with BioNavi-NP. Nature Communications *13*, 3342.

32.	Levin, I., Liu, M., Voigt, C.A., and Coley, C.W. (2022). Merging enzymatic and synthetic chemistry with computational synthesis planning. Nature Communications *13*, 7747.

33.	Zhao, D., Tu, S., and Xu, L. (2024). Efficient retrosynthetic planning with MCTS exploration enhanced A* search. Communications Chemistry *7*, 52.

34.	Kreutter, D., and Reymond, J.-L. (2024). Chemoenzymatic Multistep Retrosynthesis with Transformer Loops. ChemRxiv.

35.	Lee, S., Kim, T., Choi, M.-S., Kwak, Y., Park, J., Hwang, S.J., and Kim, S.-G. (2023). READRetro: Natural Product Biosynthesis Planning with Retrieval-Augmented Dual-View Retrosynthesis. bioRxiv.

36.	Sankaranarayanan, K., and Jensen, K.F. (2023). Computer-assisted multistep chemoenzymatic retrosynthesis using a chemical synthesis planner. Chemical Science *14*, 6467-6475.


