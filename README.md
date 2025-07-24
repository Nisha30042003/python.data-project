# The Analysis

##  1.What are the most demanded skills for the top 3 most popular data roles?

To find the most demanded skills for the top 3 most popular data roles. I filtered out thoes positions by which ones were the most popular, abd got the top 5 skills for these top 3 roles. Thid query highlights the most popular job titles and their top skills, showing which skills I should pay attention to depending on the role I'm targeting.

View my notebook with detailed steps here:
[2_Skill_Demand.ipynb](1_Python_Project.ipynb\2_Skill_Demand.ipynb)

### Visualization of data

```python

fig, ax = plt.subplots(len(job_titles), 1)
sns.set_theme(style='ticks')

for i, job_title in enumerate(job_titles):
   df_plot = df_skills_perc[df_skills_perc['job_title_short'] == job_title].head(5)
   df_plot.plot(kind='barh', x='job_skills', y='skill_percent', ax=ax[i], title=job_title, legend=False)
    
fig.suptitle('skills requested in India for jon postings', fontsize=15)
fig.tight_layout(h_pad=0.5)
plt.show()

```

### Result

![Visualization of top skills for data jobs](1_Python_Project.ipynb/images/output.png)

### Insights

- SQL is the most requested skill for data analyst and data engineer, with it is in more than half pf the job postings for both the roles. For data scientist python is the most requessted ons, appering in 69% of the job postings.
- Python is a versatile skill, highly demanded across all three roles, but most prominently for data scientist and data engineer.
