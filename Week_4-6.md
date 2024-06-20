## Guidance
Answer the following questions considering the learning outcomes for
- [Week 4](https://learn.foundersandcoders.com/course/syllabus/developer/project-2-week-1/learning-outcomes/)
- [Week 5](https://learn.foundersandcoders.com/course/syllabus/developer/project-2-week-2/schedule/)
- [Week 6](https://learn.foundersandcoders.com/course/syllabus/developer/project-2-week-3/learning-outcomes/)

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.
# Week 4
## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> **[Learning outcomes...]**  
> [your evidence here]

 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> [**Learning outcome...**]  
> [your evidence here]

## Feedback (For CF's)
> [**Course Facilitator name**]  
> [*What went well*]  
> [*Even better if*]

---


# Week 5
## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> ** Implement navigation between different pages using React Router **  
> I used React Router on the frontend repo. I used CORS to connect the backend endpoints and giving permission for the frontend repo to access those routes. React Router was used to navigate between pages on the from end. I had to link the path endpoint to a component. I also managed to add a dynamic route. I used useParams() to extract the number from `/:id ` and then feed this through to functions like `fetchProductById()`.
<img width="1372" alt="Screenshot 2024-06-20 at 17 11 32" src="https://github.com/diddydeeable/Diana_ProgressLog/assets/112947016/30cb6bc9-d88d-48a1-9529-0157f4406860">

> ** I used the useContext API to store infomation about products and + or - quantity from the shopping cart **  
> I was having a lot of bugs but I eventually figured out that I was calling functions like `handleAddToCart()`from a utils folder, but this wasn't working, I needed to define it within the ShoppingCartContext as this function was affecting statevariables defined within the context. 
<img width="685" alt="Screenshot 2024-06-20 at 17 21 38" src="https://github.com/diddydeeable/Diana_ProgressLog/assets/112947016/a6e80552-5589-4a6c-83a2-e8fd7f74134b">

 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> ** I didn't encounter a need to use the  the useReducer hook and how it can aid in using useContext for state management, this is something I will need to read about and see where it can be useful. To my understanding, useReducer is a hook, simillar to useEffect, which return 2 things [
> [1] The current state.
> [2] The dispatch function (which is a function which updates the the state and rerenders the state variable.   I didn't see the benefit of using this over useEffect in the project. **  
> [your evidence here]

## Feedback (For CF's)
> [**Course Facilitator name**]  
> [*What went well*]  
> [*Even better if*]

---

# Week 6
## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> **[Learning outcomes...]**  
> [your evidence here]

 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> [**Learning outcome...**]  
> [your evidence here]

## Feedback (For CF's)
> [**Course Facilitator name**]  
> [*What went well*]  
> [*Even better if*]
