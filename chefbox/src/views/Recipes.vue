<template>
<<<<<<< HEAD
  <div class="recipes">
      <form class="recipe-form">
        <label for="Rname">Recipe name:</label><br>
        <input type="text" id="Rname" name="Rname" value=""><br>
        <label for="ingrediants">Ingrediants:</label><br>
        <input type="text" id="ingrediants" name="lname" value=""><br>
        <label for="directions">Directions:</label><br>
        <input type="text" id="directions" name="directions" value=""><br><br>
        <input type="submit" value="Add recipe">
      </form>
  </div>
</template>
=======
  <div>
    <h1>Recipes</h1>
    <div v-for="recipe in recipes" :key="recipe._id">
      <h1>{{recipe.title}}</h1>
      <h3>{{recipe.description}}</h3>
      <p>{{recipe.directions}}</p>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      recipes: []
    };
  },
  methods: {
    getRecipes() {
      axios.get("http://localhost:5500/recipes").then(response => {
        return (this.recipes = response.data);
      });
    }
  },
  created: function() {
    this.getRecipes();
  }
};
</script>
>>>>>>> upstream/master
