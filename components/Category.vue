<template lang="pug">
.categories
  section.category-section
    - const categories = ['All','Mircale','Technology','Gapless Loop','無縫循環','Responsive Design','Built with Nuxt (Vuejs)','Malcolm Tan','陳策權'];
    each category, index in categories
      if index==0
        button.category.active= category
      else
        button.category= category
</template>
