# React
 key-->KEYWORD is not for us to use it is used by the compiler to provide the uniqueness around the compiler.

1 file::   contact.js:::

const contacts = [
  {
    id: 1,
    name: "Beyonce",
    imgURL:
      "https://blackhistorywall.files.wordpress.com/2010/02/picture-device-independent-bitmap-119.jpg",
    phone: "+123 456 789",
    email: "b@beyonce.com"
  },
  {
    id: 2,
    name: "Jack Bauer",
    imgURL:
      "https://pbs.twimg.com/profile_images/625247595825246208/X3XLea04_400x400.jpg",
    phone: "+987 654 321",
    email: "jack@nowhere.com"
  }; 
  export default contacts;
  

2 file::  APP.jsx::

  import React from "react";
import Card from "./Card";
import contacts from "../contacts";-----------> here it get imported the (contacts)---> javascript file

function createCard(contacts) {
  return (
    <Card
      id={contacts.id}
      key={contacts.id}
      name={contacts.name}
      img={contacts.imgURL}
      tel={contacts.phone}
      email={contacts.email}
    />
  );
}
function App() {
  return (
    <div>
      <h1 className="heading">My Contacts</h1>
       {
        contacts.map(createCard)
        </div>
        );
        }
        export default App;


NOTE::
actually key is a special type property
key property for each react component is a special property and it's used to ensure the right order of items goes into the tree and it's used so that it can render of these 
component efficiently when they are being created from LOOP.
                                                       id={contacts.id}
                                                       key={contacts.id}
we can use same --->contacts.id<----- for both ID and KEY but
                                                    we cannot use key as------> props.key 
                                                    but we can use ID as-----> props.id
        
