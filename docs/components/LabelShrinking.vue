<template>
  <div>
    <treeselect
      :multiple="true"
      :options="options"
      placeholder="Select your favourite(s)..."
      v-model="value"
      label="Test label"
      />
    <treeselect-value :value="value" />
  </div>
</template>

<script>
  export default {
    data: () => ({
      value: [ 'fruits' ],
      options: [ {
        id: 'fruits',
        label: 'Fruits',
        children: [ {
          id: 'apple',
          label: 'Apple 🍎',
          isNew: true,
        }, {
          id: 'grapes',
          label: 'Grapes 🍇',
        }, {
          id: 'pear',
          label: 'Pear 🍐',
        }, {
          id: 'strawberry',
          label: 'Strawberry 🍓',
        }, {
          id: 'watermelon',
          label: 'Watermelon 🍉',
        } ],
      }, {
        id: 'vegetables',
        label: 'Vegetables',
        children: [ {
          id: 'corn',
          label: 'Corn 🌽',
        }, {
          id: 'carrot',
          label: 'Carrot 🥕',
        }, {
          id: 'eggplant',
          label: 'Eggplant 🍆',
        }, {
          id: 'tomato',
          label: 'Tomato 🍅',
        } ],
      } ],
    }),
  }
</script>
