## Context API
https://medium.com/nerd-for-tech/using-context-api-in-react-with-functional-components-dbc653c7d485
https://medium.com/@danfyfe/using-react-context-with-functional-components-153cbd9ba214

### Why Context API?
- The Context API can be used to share data with multiple components, without having to pass data through props manually. 

### createContext
- The **createContext** function accepts an initial value, but this initial value is not required. After creating your context, that context now has two React components that are going to be used: Provider and Consumer.
```
import { createContext } from 'react';
export const AppContext = createContext();
```
### Flow
1. Create context using the **createContext** method.
2. Take your created context and wrap the context provider around your component tree.
3. Put any value you like on your context provider using the value prop.
4. Read that value within any component by using the context consumer.
```
import React, {useContext} from 'react';

export const UserContext = createContext();

export default const App = () => {
  return (
    <UserContext.Provider value="Reed">
      <User />
    </UserContext.Provider>
  )
}

const User = () => {
  const value = useContext(UserContext);  
    
  return <h1>{value}</h1>;git 
}
```