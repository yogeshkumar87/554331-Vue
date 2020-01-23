<template>
  <div class="review-container">
    <div class="review-container-left_block">
      <div class="book-contents">{{ boookHeading }}</div>
      <StarRating
        v-model="rating"
        star-size="25"
        show-rating="true"
        read-only="true"
      />
      <p>{{ bookCaption }}</p>
    </div>
    <div class="review-container-right_block">
      <div class="review-heading">{{ reviewHeading }}</div>
      <div class="review-rating-block">
        <div class="review-rating-content">
          <StarRating
            v-model="rating"
            star-size="25"
            show-rating="true"
            read-only="true"
          />
          <p class="rating-heading">{{ ratingHeading }}</p>
        </div>
        <div class="description">{{ description }}</div>
      </div>
      <button class="add-review-button">{{ buttonText }}</button>
    </div>
  </div>
</template>

<script>
import StarRating from "vue-star-rating";
export default {
  name: "ReviewPage",
  components: { StarRating },
  data() {
    return {
      copyright: "Copyright to VueFest 2020",
      boookHeading: "Don't judge a book by it's cover",
      bookCaption: "You don't know the JS",
      reviewHeading: "Reviews Sections",
      ratingHeading: "rating-1",
      description: "Rating",
      buttonText: "Write a review",
      rating: 3
    };
  }
};
</script>

<style scoped>
.review-container {
  display: flex;
  justify-content: space-evenly;
  padding: 3rem 5rem;
  background-color: white;
}

.review-container-left_block {
  width: 40%;
  display: inline-block;
  justify-content: center;
  flex-direction: column;
}

.review-container-right_block {
  width: 60%;
}

.book-contents {
  text-align: center;
  background: #e2e2e2;
  padding: 10px;
  font-size: 14px;
  display: inline-block;
  width: 10%;
  line-height: 20px;
}

.review-heading {
  font-size: 20px;
  font-weight: bold;
  padding-bottom: 10px;
}
.review-rating-block {
  border: 1px solid #ffd800;
  padding: 5px;
}
.rating-heading {
  font-size: 20px;
  font-weight: 700px;
  padding-left: 30px;
}
.description {
  font-size: 20px;
  padding-top: 10px;
}
.review-rating-content {
  display: flex;
}
.add-review-button {
  appearance: none;
  background: transparent;
  border: 1px solid black;
  padding: 0;
  cursor: pointer;
  width: 20%;
  display: flex;
  background: #ffd800;
  padding: 8px;
  margin-top: 20px;
  justify-content: center;
}
.add-review-button:hover,
.add-review-button:focus {
  background-color: transparent;
  outline: none;
}
</style>
