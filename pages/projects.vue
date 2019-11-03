<template>
  <main>
    <section>
        <h1>Projects</h1>
        <div v-for="project in githubProjects" :key="project.id" class="project">
            <h3>
                <a :href="project.html_url">{{ project.full_name }}</a>
                <a :href="project.html_url">{{ project.name }}</a>
            </h3>
            <p class="stars">stars: {{project.stargazers_count}} </p>
            <p>description: {{project.description}} </p>
            <p>home: {{project.homepage}} </p>
        </div>    
        <hr>
    </section>
    <aside>
        <h3>About</h3>
        <p>I am Hawk Philsworth. Lorem ipsum dolor sit amet consectetur adipisicing elit. Ea ratione vero facilis vitae quisquam labore, quasi enim, officiis at sapiente nobis itaque debitis, hic explicabo. Provident reprehenderit totam ducimus nobis!</p>
    </aside>
  </main>
</template>

<script>
    import { mapState } from 'vuex'
    
    export default {
        computed: {
            ...mapState([
                'githubProjects'
            ])
        }
    };
</script>

<style lang="scss" scoped>
main {
    width: 80vw;
    margin: 2% 8%;
    display: grid;
    grid-template-columns: 2fr 1fr;
    grid-template-rows: 1fr;
    grid-column-gap: 50px;
    grid-row-gap: 0px;
}

section { 
    background: white;
    color: black;
    padding: 30px;
    a {
        color: black;
    }

    grid-area: 1 / 1 / 2 / 2; 
}
aside { grid-area: 1 / 2 / 2 / 3; }

.stars {
    color: orangered;
}

.project {
    margin-bottom: 30px;
}
</style>