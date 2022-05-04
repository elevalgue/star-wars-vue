<template>
<div className='App'>
      <div className='searcher'>
        <h1 className='title'>Star Wars Browser</h1>
        <label htmlFor='name'>Label</label>
        <input
          type='text'
          name='name'
          id='name'
          placeholder='Darth Vader'
          value={searchInputValue}
          onChange={handleInputValue}
        />
        <button onClick={handleSearchButtonClick}>Button</button>
      </div>
      <ul>
        {searchResult.map((character, index) => (
          <li key={index}>
            <span>Nombre: {character.name}</span>
            <span>Género {character.gender}</span>
          </li>
        ))}
      </ul>
    </div>
</template>

<script>
export default {
  name: 'App',
  components: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
