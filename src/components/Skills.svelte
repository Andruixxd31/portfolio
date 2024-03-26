<script>
  import Skill from "../components/Skill.svelte";

  let skills = [
  {name: "Python", years: 5, src:"assets/langs_icons/python.svg"},
  {name: "C#", years: 18, src:"assets/langs_icons/csharp.svg"},
  {name: "C++", years: 5, src:"assets/langs_icons/cpp.svg"},
  {name: "Haskell", years: 5, src:"assets/langs_icons/haskell.svg"},
  {name: "Ruby", years: 5, src:"assets/langs_icons/ruby.svg"},
  {name: "JS", years: 2, src:"assets/langs_icons/js.svg"},
  {name: "React", years: 2, src:"assets/langs_icons/react.svg"},
  {name: "MongoDB", years: 2, src:"assets/langs_icons/mongodb.svg"},
  {name: "TypeScript", years: 2, src:"assets/langs_icons/typescript.svg"},
  {name: "Firebase", years: 2, src:"assets/langs_icons/firebase.svg"},
  {name: "Docker", years: 2, src:"assets/langs_icons/docker.svg"},
  {name: "Go", years: 4, src:"assets/langs_icons/go.svg"},
  ];
</script>

<style>
  .Skill-table {
    display: grid;
    grid-template-columns: repeat(6, 1fr);
    gap: 10px; 
  }
</style>

<div class="Skill-table">
  {#each skills as skill, indx}
    <Skill skill={skill} key={indx}/>
  {/each}
</div>
