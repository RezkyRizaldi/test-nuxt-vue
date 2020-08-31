<template>
  <div id="app">
    <b-sidebar id="sidebar-1" toggleable="lg" title="Sidebar" text-variant="dark" shadow backdrop lazy @change="toggleBodyScrollbar">
      <div class="px-3">
        <nav class="py-2">
          <b-nav vertical>
            <b-nav-item active class="my-link" href="#link-0">Active</b-nav-item>
            <b-nav-item class="my-link" href="#link-1">Link</b-nav-item>
            <b-nav-item class="my-link" href="#link-2">Another Link</b-nav-item>
          </b-nav>
        </nav>
        <p>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Omnis sint saepe corporis iure voluptatum commodi! Facere molestias accusamus officia pariatur molestiae tempora ipsum mollitia dolorem officiis quibusdam suscipit, non illum cumque aut recusandae illo quidem accusantium ab nam fugit laudantium minima, earum, corporis enim. Natus molestias distinctio commodi non eius voluptatem recusandae laboriosam, impedit quisquam obcaecati aliquam sint totam unde dolore, consequatur, ipsa odit! Necessitatibus aliquam quod eos voluptate! Dolor, suscipit optio dignissimos, quisquam cum provident harum recusandae sint ad omnis modi, natus architecto vitae? Necessitatibus qui ipsam, obcaecati asperiores doloribus quia modi ratione eius accusamus autem quos odit unde quasi fugiat exercitationem pariatur aspernatur, est quidem adipisci, nobis debitis aperiam! Repellendus suscipit, labore sit ipsam ab sequi cumque quaerat quis ipsum aliquid nulla voluptatum tempora odio vero, expedita numquam vel ea explicabo quod ex. Voluptas sit distinctio iusto neque delectus eum voluptatum ut totam? Numquam dignissimos cum quam nemo sequi tempore illum, et facilis ipsam recusandae nisi deleniti expedita voluptatibus animi beatae iste sunt impedit reprehenderit ipsa neque delectus consequatur maxime illo unde. Sed ex qui officia ut placeat suscipit nam mollitia natus ratione delectus sit vero architecto distinctio quidem sint illo dignissimos quae culpa perferendis, autem recusandae optio quos repudiandae quisquam. Animi temporibus, esse est molestias earum excepturi cumque enim nesciunt, voluptates unde cupiditate quisquam quos optio odio omnis consequuntur incidunt eius explicabo harum labore. Accusamus, reprehenderit omnis aliquam cupiditate temporibus ut magni aspernatur voluptate libero odio, voluptatibus mollitia animi reiciendis odit quidem voluptas sed dolore ipsum veritatis eum explicabo perspiciatis atque. Unde suscipit provident debitis voluptatem similique quis, neque velit asperiores, magnam voluptates veniam ut optio sit, enim fuga reprehenderit perspiciatis corrupti dignissimos ipsum reiciendis? Deleniti, ratione laudantium assumenda exercitationem possimus sint magnam quas, delectus est eum dicta id minima praesentium quasi provident ipsam cupiditate expedita necessitatibus?
        </p>
      </div>
    </b-sidebar>
  </div>
</template>

<script>
  export default {
    el: '#app',
    methods: {
      toggleBodyScrollbar(visible) {
        const body = document.getElementsByTagName('body')[0];

        if(visible)
          body.classList.add("overflow-hidden");
        else
          body.classList.remove("overflow-hidden");
      }
    }
  }
</script>
