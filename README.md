# Home-Credit-Final Sumbittion Versions
1. This competition was initiated by Home Credit Group, an international non-banking financial institution. The goal of this competition is to predict which customers are more likely to default on loans.

2. Feature engineering was conducted based on the competition data. The competition provided 465 native features including personal information (gender, age, education, etc.), consumption records (monthly consumption amount, reasons for consumption restrictions, etc.), and credit card information (issuing bank, level, etc.). We derived the following features based on these characteristics:

   - Aggregate Features: Aggregate features that summarize the consumption level of each user, reflecting the user's situation from different perspectives. For a continuous variable, we can take mean, std, min, max; for a discrete variable, we can take count, last, and nunique.
   
   - Diff Features: Statistic of the change in the user's historical consumption data, which can reflect whether there has been a change in behavioral patterns in the recent period.

3. In risk control issues, decision tree models usually perform well. Here, we used LightGBM and CatBoost models to solve this problem. These types of models have demonstrated excellent performance in various tasks and are well suited to the data characteristics of this competition. To improve the robustness of the model, we used groupkfold to divide the samples into five segments of test sets based on the week_num of the samples for thorough testing and to avoid overfitting.

4. In the competition, we made full use of the competition time, controlled the pace of the competition reasonably, actively discussed and formulated reasonable competition model iteration tasks, and organized brainstorming sessions to promote the progress of the competition. At the same time, we started developing the models to ensure that we could improve predictive accuracy as much as possible. In the end, we scored xxx points, achieving a ranking in the top 0.1%.
