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
> ** This week I made big progress on learning about SQL, it's syntax, and how to make SQl queries to access data from the database. Queries I made included and INSERT queries**
> <img 
<img width="698" alt="Screenshot 2024-06-20 at 17 37 14" src="https://github.com/diddydeeable/Diana_ProgressLog/assets/112947016/668fd81b-5615-4268-82de-e081fd48a1d8">
<img width="608" alt="Screenshot 2024-06-20 at 17 35 53" src="https://github.com/diddydeeable/Diana_ProgressLog/assets/112947016/65070562-3bfb-424b-aa34-5b8eac58cc77">

> ** I added some CRUD operations to the project. We can Create a user, Read information about a product**
> <img width="731" alt="Screenshot 2024-06-20 at 17 41 48" src="https://github.com/diddydeeable/Diana_ProgressLog/assets/112947016/8bcfd0f5-17e9-4f64-9672-c4dbd74514a2">


> I also gained a better understanding of relational data, including how to organize data into tables or 'entities.' With my team, I planned how the data would be stored and accessed across multiple tables. I learned that every table should have a primary key, and you can reference another table using a foreign key. Additionally, I learned that data with a many-to-many relationship requires an intermediary table to connect columns from different tables. We did this by creating an orders table to match up products (a product_id) with an order (an order_id), because an order can have several product ids. 
><img width="858" alt="Screenshot 2024-06-20 at 17 47 39" src="https://github.com/diddydeeable/Diana_ProgressLog/assets/112947016/e3262d57-4fb2-4bbc-b9e6-fd4730c429de">



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
> This week my team and I completed our project which was a book app. 
I tried to make code more modular and reusabile (K7, S1, S11) and as well as this I have solidified typescript skills (K7, S1, S11, S12). I did this by using custom hooks (custom state hooks for operations you often use.)
> Here is an example of a custom hook which fetches data. I now only have to call this once in my code and the result is stored in the FetchHookState.data.
```
import { useState, useEffect } from "react";
import { Books } from "../types/books";

// Defines the state types for the custom useFetch hook.
interface FetchHookState {
  isLoading: boolean;
  error: Error | null;
  data: books[] | null;
}

const useFetch = (url: string,): FetchHookState => {
  const [data, setData] = useState<Books[] | SingleReviewData | null>(
    null,
  );
  const [error, setError] = useState<Error | null>(null);
  const [isLoading, setIsLoading] = useState<boolean>(true);

  useEffect(() => {
    const fetchData = async () => {
      setIsLoading(true);
      try {
        const res = await fetch(url);

        if (!res.ok) throw new Error(res.statusText);

        const json = await res.json();

        setData(json.data ? json.data : []) 
       
        // eslint-disable-next-line @typescript-eslint/no-explicit-any
      } catch (error: any) {
        setError(error);
      } finally {
        setIsLoading(false);
      }
    };
    fetchData();
  }, [url]);

  return { isLoading, error, data };
};

export default useFetch;
```


 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
I struggled with validating inputs when people log in. 
I could not return the correct error message object. 

## Feedback (For CF's)
> [**Course Facilitator name**]  
> [*What went well*]  
> [*Even better if*]
