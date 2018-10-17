<template>
  <div>
    <h-app-toolbar>
      <h-app-toolbar-container bgcolor="bg-primary" textcolor="text-white">
        <h-app-toolbar-navigation icon="fas fa-bars" textcolor="text-white"/>
        <h-app-toolbar-title title="My big music collection to sing"/>
        <h-app-toolbar-action>
          <h-fa-icon icon="fas fa-heart" textcolor="text-white" @click="iconClick"/>
          <h-fa-icon icon="fas fa-search" textcolor="text-white"/>
        </h-app-toolbar-action>
        <h-app-toolbar-menu>
          <h-menu-dropdown rtl icon="fas fa-ellipsis-v" textcolor="text-white">
            <h-menu-dropdown-item icon="fas fa-check-circle" text="You are correct." />
            <h-menu-dropdown-item icon="fas fa-handshake" text="You are in good hands"/>
          </h-menu-dropdown>
        </h-app-toolbar-menu>
      </h-app-toolbar-container>
    </h-app-toolbar>

    <h-search @search="onSearch" ref="search" :options="options"/>

    <div>
      <h1>Input Chips</h1>
      <h-input-chips v-model="chipsInput" float-label="My Chips"  left-icon="fas fa-camera-retro" helper-text="Type your chips" cleartext></h-input-chips>
    </div>

    <div class="col-6">
      <h1>List</h1>
      <h-list>
        <h-app-toolbar>
          <h-app-toolbar-container bgcolor="bg-primary" textcolor="text-white">
            <h-app-toolbar-navigation icon="fas fa-bars" textcolor="text-white"/>
            <h-app-toolbar-title title="Topics"/>
          </h-app-toolbar-container>
        </h-app-toolbar>
        <h-list-body>
          <h-list-item>
            <h-list-item-left icon="fas fa-film" text="Attractions"/>
          </h-list-item>
          <h-list-item>
            <h-list-item-left icon="fas fa-utensils" text="Dining"/>
          </h-list-item>
          <h-list-item>
            <h-list-item-left icon="fas fa-heart" text="Health"/>
          </h-list-item>
          <h-list-item>
            <h-list-item-left icon="fas fa-basketball-ball" text="Sports"/>
          </h-list-item>
          <h-list-item>
            <h-list-item-left icon="fas fa-plane" text="Travel"/>
          </h-list-item>
        </h-list-body>
      </h-list>
    </div>

    <div class="col-6" style="height: 450px;">
      <h1>table</h1>
      <h-table
        title="Users"
        :columns="tableColumns"
        :rows="tableData"
        lineheight="40px"
      >
      </h-table>
    </div>

  </div>
</template>

<script>

export default {
  components: {
  },
  data () {
    return {
      options: [],
      chipsInput: ['Clark', 'John'],
      tableData: [
        { number: 1, avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Smiley_icon.svg/768px-Smiley_i.png', country: 'USA', city: 'New York city' },
        { number: 2, avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/97/Classic_smiley.svg/1200px-Classic_smiley.svg.png', country: 'USA', city: 'New York city' },
        { number: 3, avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Smiley_icon.svg/768px-Smiley_i.png', country: 'USA', city: 'New York city' },
        { number: 4, avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/97/Classic_smiley.svg/1200px-Classic_smiley.svg.png', country: 'USA', city: 'New York city' },
        { number: 5, avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Smiley_icon.svg/768px-Smiley_i.png', country: 'USA', city: 'New York city' },
        { number: 6, avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/97/Classic_smiley.svg/1200px-Classic_smiley.svg.png', country: 'USA', city: 'New York city' },
        { number: 7, avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Smiley_icon.svg/768px-Smiley_i.png', country: 'USA', city: 'New York city' },
        { number: 8, avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/97/Classic_smiley.svg/1200px-Classic_smiley.svg.png', country: 'USA', city: 'New York city' },
        { number: 9, avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Smiley_icon.svg/768px-Smiley_i.png', country: 'USA', city: 'New York city' },
        { number: 10, avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/97/Classic_smiley.svg/1200px-Classic_smiley.svg.png', country: 'USA', city: 'New York city' },
        { number: 11, avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Smiley_icon.svg/768px-Smiley_i.png', country: 'USA', city: 'New York city' },
        { number: 12, avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/97/Classic_smiley.svg/1200px-Classic_smiley.svg.png', country: 'USA', city: 'New York city' },
        { number: 13, avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Smiley_icon.svg/768px-Smiley_i.png', country: 'USA', city: 'New York city' },
        { number: 14, avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/97/Classic_smiley.svg/1200px-Classic_smiley.svg.png', country: 'USA', city: 'New York city' },
        { number: 15, avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Smiley_icon.svg/768px-Smiley_i.png', country: 'USA', city: 'New York city' },
        { number: 16, avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/97/Classic_smiley.svg/1200px-Classic_smiley.svg.png', country: 'USA', city: 'New York city' }
      ],
      tableColumns: [
        {
          name: 'number',
          alignment: 'flex-justify-end'
        },
        {
          name: 'country',
          alignment: 'flex-justify-center'
        },
        {
          name: 'city'
        }
      ]
    }
  },
  methods: {
    onSearch (query) {
      this.options = []
      this.options.push({ avatar: 'avatar/turtle.png', text: 'Ninja Turtle', desc: 'I kill you' })
      this.options.push({ img: 'avatar/folder_open.jpeg', text: 'Photos', desc: 'Dez 12, 2017' })
      this.options.push({ icon: 'fas fa-volleyball-ball', text: 'Attractions', desc: 'Lets go to the movie?' })
    }
  }
}
</script>
