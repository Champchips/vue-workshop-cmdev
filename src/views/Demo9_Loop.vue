<template>
  <div id="demo9">
    <h1>Demo9 : Loop</h1>
    <ul>
      <li v-for="(item, index) in ['Angular', 'Vue', 'React']" :key="index">
        {{ item }}
      </li>
    </ul>
    <hr />
    <!-- Destructuring -->
    <ul>
      <li v-for="({ name, price }, index) in SPAcouses" :key="index">
        Name: {{ name }} Price: {{ price }}
      </li>
    </ul>

    <hr />
    <input type="text" placeholder="Title" v-model="course.title" /><br />
    <input type="number" placeholder="Price" v-model="course.price" /><br />
    <button @click="addCourse">Submit</button>
    <!-- Dynamic -->
    <ul>
      <li v-for="(course, index) in dynamicCouses" :key="index">
        {{ course.title }}, Price: {{ course.price }}
        <button style="margin: 5px" @click="removeCourse(index)">Remove</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Demo9",
  methods: {
    addCourse() {
      this.dynamicCouses.push(this.course);
      this.course = { title: "", price: 0 };
    },
    removeCourse(index) {
      this.dynamicCouses.splice(index, 1);
    },
  },
  data() {
    return {
      course: { title: "", price: 0 },
      dynamicCouses: [],
      SPAcouses: [
        { name: "Angular", price: 10 },
        { name: "Vue", price: 15 },
        { name: "React", price: 20 },
      ],
    };
  },
};
</script>

<style></style>
