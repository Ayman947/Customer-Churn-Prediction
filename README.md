# 📱👪📉 Telecom Customer Churn Prediction

**Background:** 
- Customer churn is the tendency of customers to cancel their subscriptions to a service they have been using.
- Customer churn rate is the percentage of churned customers within a predefined time interval.
- Churn rate is a very important indicator of customer satisfaction and the overall business wellness of the company.



**Problem:** 
- At the telecom company, the marketing department detected that they are losing many of their customers (i.e. high churn rate).
- So, they decided to launch retention campaigns, and to be efficient they need to target just the customers who have the tendency to churn.

![image.png](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAUcAAACaCAIAAAC1/B15AAAXUUlEQVR4nO2dfXBU1fnHz+5mX4KQIFGCZIO85oUXNUkhs4JBQ6m4OKPU2dIgHfCFsQPBzoioodMxTie2TYtSSTotNoVQhFHihLYk1SDUzkCUMYZaEgzUGWYTGF2JsIkk+3Z3T/+4v+5v2fuy59577r3L3ecz+QPuveec75693z335ZznMWGMEQAABsKstwAAACgDrgYAowGuBgCjAa4GAKMBrgYAowGuBgCjAa4GAKMBrgYAowGuBgCjAa4GAKMBrgYAowGuBgCjAa4GAKMBrgYAowGuBgCjAa4GAKMBrgYAowGuBgCjAa4GAKMBrgYAowGuBgCjAa4GAKNB39XHjh3bunXr8uXLV69e/eqrr54/f556E+J89NFHGzduNJlMJpNp2rRpO3bsGBwc1FLAyMhIc3PzXXfdxWpYvnz5u+++q6UAhNCnn34a7wSTyfT8889r/EUEg8Hm5uaKiop4J+zfv19LARkNpkdPT09hYSG3iZqaGr/fT7EhIYaHh91uN+/HrKur00AAxritrU2oq3t6ejQQ4Pf7PR4Pr4Bt27ZpIABj3NHRIdQJ3d3d2mjIZKi5urW1VfznY2BggFZbvHi9XnEBbrc7EAioqqGhoUFcQ0dHh6oCfD5ffn6+iACXy6V2J+zatUu8E9ra2lQVANBxdXt7u/gXyeLz+ag0x2V4eJhEgMfjUUkAxripqYlEg3qDld/vF7c0S1VVlUoCMMGPO0tXV5d6GgAKrk45SMZxuVzKm+NF6JqTS2trqxoC+vr6CAUghFQaLTds2EAoYNeuXWoIGBgYIO8EbW7KMhMKrha6leVFjauvrq4ucgEqnU9VVVXkAhoaGqgL6Onp0b0TJJ0Jmj3pyECUulrSGIUQys/Pp6I7EUknE1JhuJbqKKTCcE1+tcLS1NREV4CkgVqlTkgTYkNDocbGcY9nrKBg3OMJ7tjBnDyppQClrk75fIgL3cdmPp9PqgC3201RAMa4rq5Oqga6d9d+v1+qgEWLFlEUgAkeknEx4N11MBhYv/46Qty/8crKaH+/NiqUvq+W8SZW6vAuzmeffSa1SGdnJ0UB8jR8/vnnFAV88cUXUoucPXs2GAxS1CD1Pggh9Mknn1AUoD+h0Pg990QPHODdGTt9OrBgAXP8uAZClLq6t7dXapFLly4pbDSR0dFRGaVGRkYoajh79qzUIl999RVFATIuWJDcrhNiaGhIapGrV69SFKA7geXLcarbkNB3v4upnv+86DBjNCsri2JtFotFRim73U5Rw+TJk6UWyc3NpSjAarXKKEW3EyZOnCi1yJQpUygK0BfmyJHY6dMkR4Z+9jO1xSh1tcvlklqkqKhIYaOJzJs3T2oRl8vlcDgoaigvL5dahG4nzJgxQ0YRur8sFRUVUovMnz+fogB9ifzhD4RHRvftQ6GQqmKUuvrhhx+WWuS+++5T2Ggic+bMkVpk7dq1FAUghKqrq6UWWbJkCUUBxcXFUos888wzFAUghB566CGpRR544AG6GnQk9t575AdHz51TTwlCiueBk09BYamtraXylC8Rqc/hh4eH6QqQ+ghajVe1hDPb4lCf5xcIBCQJUONM0JHreXm8j755/9R+0UVhFkptba2OJxOWaCrq72lZJJlKjRkgkkylxjQYTDxdlEW96cO6MFZSQu7q2NWrqoqh4Gry80m9tQ3d3d0kAlSdB044GUa9lVuEk2FUnQdOOBnGeG+qQ42NhJYer6xUWwyd1R0k1+EtLS1U2hJCZAkki6qWxhgHAoGU80bVPptFlkCyUJ+BwyXlr1t7e7vaGnQgGCR0deSDD9TWQm0lps/nE/k6tVlV29PTI/Q0WKULby5CN/kul8vr9WogoK+vb9GiRbwaVFrUwUWoE8rLy9VekKsjzMmTKS0drK/XQIkJYyz+yyqJY8eOvfnmm4cPH46fyk8//fS6devovkkSp7Oz85133unt7WUYZtasWW63e/369XTf4ogzODh44MCB999//8qVK9nZ2ffee++6detkvAJUwrFjx956663ETvB4PFOnTtVMwNdff33o0KGurq6LFy/q1QnaEz11KrhsmdBea3OzbfNmDWRQdnWckZERu92upZkBIB3Ao6ORAwei+/fHJ6WYCgosjz9ufeopM9VJCiJIdnUwGDxx4sTFixcZhhE6hmT2GFvc6XQuXrxY6iSKI0eOHD9+nHeapNSJazabbfHixVLHscHBwfb29jNnzoyPj3MFMAwjScb06dMffPDBlStXkhdBCHV2dp44cYI3JJuMTigrK1uzZo2kL4IdjXk7QYaM6dOnV1dXS11+pzOhEL5yJXblCvZ68ZUrlqVLzXPmoP/N2MPXrrH/MN16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)

**Objective:** To determine the customers' tendency to churn.

**Question:** Who will churn and who will not?

**Analytics Solution / Methodology:** A supervised ML classification models will be built to predict the churn status of every customer.



  # **Data Sources**

  - [Data source: Name ](link)
  | Column | Description   | Example Values |
  |--------|---------------|----------------|
  |        |               |                |
  |        |               |                |
  |        |               |                |
  - Scripts





  # **Environment** & **Packages**

  | Package Name | Functionality                 |
  |--------------|-------------------------------|
  | Pandas       | Data Manipulation             |
  | numpy        | Numerical Calculations & Array Manipulations   |
  | json         | Handling Json Files           |
  | BeautifulSoup| Web scrapping                 |
  | requests     | Building APIs                 |
  | matplotlib   | Data Visualizatiom            |
  | seaborn      | Data Visualizatiom            |
  | Follium      | Geospatial Data Visualization |
  | sklearn      | Machine learning algorithms   |




  # **Data Cleansning & Preprocessing**

  -
  -
  -
  -



  # **EDA Insights**

  - ![Model_Insight_Description](link)
  - ![Model_Insight_Description](link)






  # **Modeling**

  - We've built **[[ML Algo]]** to predict **[[target]]** using **[[Inputs]]**.

  | HyperParameters | Values   |
  |-----------------|----------|
  |                 |          |
  |                 |          |

  - Our model's accuracy is **[[## %]]** (i.e For every 100 predictions, there are ## predictions are true.)

  - ![Model_Insight_Description](link)





  # **Final Results**

  - [Predicted Data Name](link)
  - ![Insight_Description](link)
  - [Dashboard Name](link)



  # **Recommendations**

  - csd
  - vdf



  # **Conclusion**

  - ###
  - ###


  # **Appendix**

  - (Code-Dashboard-Paper)
  - Presentation Storytelling


GRAMMERLY
