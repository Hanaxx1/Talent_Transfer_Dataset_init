<font size=6>**Talent Transfer Dataset** </font>
***
In an increasingly globalized world, the flow of human resources across international borders has become a common phenomenon. This indicates that talent is no longer confined to a specific region or country but moves globally, transcending national boundaries while retaining its cultural background. Considering the impact of talent on various fields such as science, technology, economy, and society, understanding talent migration and distribution has become a key factor for national competitiveness.

We employed a standard mapping framework to depict the global talent mobility trajectories, using national boundaries as the spatial measurement units. The scope of countries is based on the 193 member states included in the United Nations Blue Book (UN Blue Book). Additionally, we reorganized the data along a temporal axis, enabling researchers to analyze monthly or yearly mobility changes.

<font size=6>**Transfer Text Classification** </font>
***
Given the extensive temporal and spatial scales covered by the dataset, processing a large volume of data is essential to support the research. Therefore, large-scale text data sources are required, and these sources must be preprocessed to filter out texts containing migration information. This filtered data is then used to construct fine-tuning datasets and enhance the efficiency of subsequent information extraction by large language models.
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/232c8409e45c4b9781b03be4686e2efb.png#pic_center)

<font size=6>**Tuning And Infering LLMs** </font>
***
We fine-tune a cluster of large language models (including Mistral, Openchat, and Solar) to accept textual passages (e.g., website news summaries) along with task prompts (e.g., extracting migration information from the news) and generate precisely formatted responses.

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4452af45083e4f0ba2b4653473035eb0.png#pic_center)
Based on a two-step fine-tuning approach, our ensemble of large language models (LLMs) can identify and extract transfer-related features from the input text data, including the transfer subject, origin, destination, and timestamps. Additionally, recognized geographic entities (such as city names, organization names, landmarks, etc.) are normalized and mapped to the country level for extraction. 
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/981cbbc14e76440e81c4253880f6851e.png#pic_center)
Subsequently, we align the extraction results of different models within the LLM ensemble for the same text data. We retain only those outputs that are completely consistent across multiple models, discarding any results where discrepancies occur. 
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/5e2c69053daa43eebe1ceec61f8bc74c.png#pic_center)

<font size=6>**Data Mining** </font>
***
In this study, we conduct data mining on a talent migration dataset from various perspectives. Our analysis includes statistical evaluation of domain distribution, a global heatmap illustrating international interactions, analysis of migration flows across geographic regions, and examination of migration trajectories for key countries.

1. Domain name distribution statistics
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/cdcbaf45123c47caaac9b6b60790e396.png#pic_center)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/239f4bab29c94c9e83a0e8ddaabe15c9.png#pic_center)

 2. Synergistic effects
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/fc50ed3b7dda42adad2a5f5d2217fe93.jpeg#pic_center)![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/dc69758e27e94eef8d8634fff038b530.png#pic_center)
 3. Interactive transfer heat maps between countries

 4. Global transfer map
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/702a223bf1ff4b7cb9a86d9b1d742397.png#pic_center)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/15626545ab584c94902a759bf94e9150.png#pic_center)


 5. Focus countries talent fransfer trajectory
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/fc01d780ffa5479fa1f029b73f4684f2.png#pic_center)


