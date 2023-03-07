<template>
    <div>
      <h1>Books Management System</h1>
      <br><br>
      <div class="container">
        <label>Book Name: </label>
        <input type="text" placeholder="Book Name" v-model="bName">
        <label>Author Name: </label>
        <input type="text" placeholder="Book Name" v-model="aName">
        <label>No of pages: </label>
        <input type="text" placeholder="Book Name" v-model="noOfpages">
        <button class="submit" @click="addBook()">Add Book</button>
        <hr>
       <table>
        <tr>
          <th>Id</th>
          <th>Book Name</th>
          <th>Author Name</th>
          <th>No Of Pages</th>
        </tr>
        <tbody>
          <tr v-for="item in books" :key="item.id">
            <td> {{ item.bId }} </td>
            <td> {{ item.bName }} </td>
            <td> {{ item.aName }} </td>
            <td> {{ item.noOfpages }} </td>
            <button class="edit" @click="editBook()">edit</button>
            <button class="delete" @click="deleteBook(item)">delete</button>
          </tr>
        </tbody>
       </table>
      </div>
    </div>
  </template>
  
  <script>
    export default {
      data() {
        return {
          // for books in tables
          bId: "",
          bName: "",
          aName: "",
          noOfpages: "",
          
          books: [
            {bId: 1, bName: "Harry Potter", aName: "J. K. Rowling", noOfpages: 100},
            {bId: 2, bName: "Alice's Adventures in Wonderland", aName: "Lewis Carroll", noOfpages: 100},
            {bId: 3, bName: "Rich Dad Poor Dad", aName: " Robert Kiyosaki, Sharon Lechter", noOfpages: 100}
          ]
        }
      },
      methods: {
        addBook() {
          this.books.push({
            bId: this.books.length + 1,
            bName: this.bName,
            aName: this.aName,
            noOfpages: this.noOfpages
          })
          this.bId = "";
          this.bName = "";
          this.aName = "";
          this.noOfpages = "";
          console.log("book addded");
        },
  
        deleteBook(object) {
          this.books = this.books.filter(o => o.bId != object.bId)
        },
  
        editBook() {
          console.log("edit books");
        },
      },
    }
  </script>
  
  <style>
  table {
    font-family: arial, sans-serif;
    border-collapse: collapse;
    width: 100%;
    border: 1px solid black;
  }
  .submit {
    background-color: dodgerblue;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    font-size: 14px;
    cursor: pointer;
  }
  input{
    margin-right: 20px;
  }
  </style>