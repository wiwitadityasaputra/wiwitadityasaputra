
## Hi there 👋 welcome to my journey
### 2026
#### October   
- in progress

#### September
<details>
<summary> 💻 Create city-guru project</summary>
 
```markdown
city-guru is like mini geoguessr
pick your favorite country/city then slide-show will appear
and you should try to guess the location! (through google map)
```
[live](https://city-guru.vercel.app)
</details>

<details>
<summary> ❌ AWS Certified Developer</summary>

```markdown
I did the exam in early oct actually but i studied & practice in the hole september
yup, i fail in this exam my scored is 70% out of the 72% minimum requirement
i feel like i just need 2-3 correct answer to pass it
but yeah, fail is fail
```

##### Study
I watched the 16hours video from Andrew Brown [part1](https://www.youtube.com/watch?v=RrKRN9zRBWs&t=53s) & [part2](https://www.youtube.com/watch?v=eCopK1RoyFM)   
and also try my self his follow along material, that was great   

##### Practice
I practice a lot of things that i didn't understand before like elastic beanstalk, ecs, stepfunctions, cloudformation & codepipeline
i'm also able to make blue/green deployment, here is thing i did
* Prepare every needed things on cloudformation template   
  1. Parameter Store   
     paramter store is like your env var, api-key, db connection, versioning number & etc...
  2. Resources   
     my prebuild aws services like role, codecommit, ecr, ecs, taskdefinition, codepipeline & stepfunctions   
     i put everthing [here](https://github.com/wiwitadityasaputra/street-food/commit/0f429c8fdd9981395f963fb175715dcf6b6b2d51)
  3. Rules
* blue/green deployment   
  after succesfully deploy cloudformation.yaml‎ to cloudformation service   
  i will have 3 stepfunctions:    
  1. init services (run one time only)   
  2. for build image   
  3. for deployment    
  
  ###### initialization steps   
  first of all i need to run step function no 1 to make sure some services is available   
  such as: vpc, subnet, loadbalancer, security groups (need 2 for blue/green), security gropus inbound traffict role, task-definition, loadbalancer http/https listener, ecs service and route53    
  ###### build steps   
  usually we manage project repository on github because everybody familiar with github ui   
  when we are ready to deploy new changes, i should push my latest changes to   
  codecommit branch prod and then event bridge will know we have codecommit changes  
  and run step functions no 2   
  stepfunction will tell codepipeline to do deployment by running codebuild then codedepoy  
  in codebuiold we will build the docker image and push to ecr and update the paramter store   
  because we need to know where is the latest image   
  after successfully push new image     
  ###### deployment steps   
  before running codedeploy codepipeline will trigger Approval first  
  (i should use sns here to inform user about new deployment)    
  need human confirmation for deployment   
  let assume we got approve then we can deploy   
  we will run stepfunctions no 3   
  get the latest image from paramter store   
  register new task definition   
  create deployment group if not exist
  start blue/green deployment
  and will deregister/stop old task after some time    
  in case bad things happen before old task removed, i should manually change the load balancer target groups
  
##### Exercise
lets back to my aws developer examp progress   
i also bought practice exam from tutorialdojo   
its hard from begining but when i start study, understand the reason whay the answer is correct or wrong then i got pass of all exams preps   
i was confident enough to start the real exam   
then fail hehe
</details>


#### August
<details>
 <summary>
  ✅ AWS Certified Cloud Practitioner 
  </summary>

```markdown
AWS Certified Cloud Practitioner is like basic knowledge about aws services
basically itss just full of theory
i did watching the full video on skillbuilder.aws is really helpfull
and also try dump examp from some sites like: https://www.cloudcertprep.io & https://kananinirav.com
```
[my certificate](https://www.credly.com/badges/6ade8bfe-8701-4481-9d31-04092b49673b/public_url)
</details>

<details>
  <summary>
    💻 Create street-food project 
  </summary>
  
```markdown
street-food is simple CRUD app 
stacks: NextJS, ReactJS, bootstrap css & postgres
nothing special, ai could do better for sure, hehe
```
[repo](https://github.com/wiwitadityasaputra/street-food) [live](https://street-food-seven.vercel.app)
</details>

#### 2015 August - 2026 August   
- in progress
