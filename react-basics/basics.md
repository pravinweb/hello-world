# React Basics

### Updating Object State
Note: https://youtu.be/-yIsQPp31L0?t=294

##### Code
```
import React from 'react';
import {useState} from 'react';


const App = () => {
  
  const baseUser = {
    name: '',
    age: '',
    city: ''
  }
  const [user, setUser] = useState(baseUser);
  
  const handleChange = (e) => {
    setUser({...user, name: e.target.value}) 
  }
  
  return (
    <div>
      My User: {user.name} <br/>
      <input type="text" onChange={handleChange} /> 
    </div>
  )
}


export default App;
