# The Analysis 


## What are the skills most in demand for the top 3 most popular data roles?

To find the most demanded skills for the top 3 most popular data roles. I filtered out those positions by which ones were the most popular, and got the top 5 skills for these top 3 roles. This query highlights the most popular job titles and their top skills, showing which skills I should pay attention to depending on the role I'm targeting. 

View my notebook with detailed steps here: [2_Skill_Demand.ipynb](Project/2_Skill_Demand.ipynb).

### Visualize Data

```Python

fig, ax = plt.subplots(len(job_titles), 1)

for i, job_title in enumerate(job_titles):
    job_plot = df_skills_count[df_skills_count['job_title_short'] == job_title].head()
    job_plot.plot(kind= 'barh' , x= 'job_skills', y= 'skill_count'  ,ax= ax[i], title = job_title, legend= False)
    ax[i].invert_yaxis()
    fig.tight_layout()
    plt.show()
```


### Results

![Likelihood of Skills Requested in the Indian Job Postings](images/Project/images/result_1.png)
