<template>
  <div class="schedule-all row-max-grid">
    <div class="container">
      <table class="row-grid">
        <thead>
          <tr>
            <th scope="col">Days</th>

            <th scope="col">Class Name</th>
            <th scope="col">Age Group</th>
            <th scope="col">Class Time</th>
            <th scope="col">Studio</th>
            <th scope="col">Additional Information</th>
          </tr>
        </thead>

        <tbody v-for="item in schedule " :key="item.id">
          <tr>
            <td rowspan="4" class="day-txt">{{item.day}}</td>

            <td data-label="Class Name">{{item.className}}</td>
            <td data-label="Age">{{item.ageGroup}}</td>
            <td data-label="Class Time">{{item.timeStart +"-"+ item.timeEnd}}</td>
            <td data-label="Studio">{{item.studioNum}}</td>
            <td data-label="Add Info">{{item.addInformation}}</td>
          </tr>
          <!-- <tr>
            <td data-label="Class Name">{{item.className}}</td>
            <td data-label="Age">{{item.agegroup}}</td>
            <td data-label="Class Time">{{item.timeStart+ item.timeEnd}}</td>
            <td data-label="Studio">{{item.studioNum}}</td>
            <td data-label="Add Info">{{item.addInformation}}</td>
          </tr> -->
          <!-- <tr> -->
            <!-- <td rowspan="2" class="time-txt" >Late</td> -->
            <!-- <td data-label="Class Name" ></td>
       <td data-label="Age" class="freespace"> </td>
      <td data-label="Class Time" class="freespace"></td>
     <td data-label="Studio" class="freespace" ></td> -->
          <!-- </tr> -->
          <!-- <tr>
            <td data-label="Class Name">{{item.className}}</td>
            <td data-label="Age">{{item.ageGroup}}</td>
            <td data-label="Class time">{{item.timeStart+ item.timeEnd}}</td>
            <td data-label="Studio">{{item.studioNum}}</td>
            <td data-label="Add Info">{{item.addInformation}}</td>
          </tr> -->
          <!-- <tr>
      <td rowspan="4" class="day-txt">Tuseday</td>
     

      <td data-label="Class Name" >Ballet</td>
       <td data-label="Age" >(6-9)</td>
      <td data-label="Class Time" >4:30pm-5:30pm</td>
      <td data-label="Studio" >1</td>
                 <td data-label="Add Info" >Once a Week</td>
    </tr>
    <tr>
      <td data-label="Class Name" >Ballet</td>
       <td data-label="Age" >(10-18)</td>
      <td data-label="Class Time" >5:30pm-6:30pm</td>
      <td data-label="Studio" >1</td>
                 <td data-label="Add Info" >Once a Week</td>
    </tr>
    <tr>
     
       <td data-label="Class Name" >Ballet</td>
       <td data-label="Age" >(6-9)</td>
      <td data-label="Class Time" >4:30pm-5:30pm</td>
      <td data-label="Studio" >1</td>
                 <td data-label="Add Info" >Once a Week</td>
    </tr>
  <tr>
   
      <td data-label="Class Name" >Contemporary</td>
       <td data-label="Age" >8+</td>
      <td data-label="Class time" >6:30pm-7:30pm</td>
      <td data-label="Studio" >3</td>
                 <td data-label="Add Info" >Twice a Week</td>
    </tr>
    <tr>
      <td rowspan="4" class="day-txt">Wednesday</td>
     

      <td data-label="Class Name" >Ballet</td>
       <td data-label="Age" >(6-9)</td>
      <td data-label="Class Time" >4:30pm-5:30pm</td>
      <td data-label="Studio" >1</td>
                 <td data-label="Add Info" >Once a Week</td>
    </tr>
    <tr>
      <td data-label="Class Name" >Ballet</td>
       <td data-label="Age" >(10-18)</td>
      <td data-label="Class Time" >5:30pm-6:30pm</td>
      <td data-label="Studio" >1</td>
                 <td data-label="Add Info" >Once a Week</td>
    </tr>
    <tr>
     
       <td data-label="Class Name" >Ballet</td>
       <td data-label="Age" >(6-9)</td>
      <td data-label="Class Time" >4:30pm-5:30pm</td>
      <td data-label="Studio" >1</td>
                 <td data-label="Add Info" >Once a Week</td>
    </tr>
  <tr>
   
      <td data-label="Class Name" >Contemporary</td>
       <td data-label="Age" >8+</td>
      <td data-label="Class time" >6:30pm-7:30pm</td>
      <td data-label="Studio" >3</td>
                 <td data-label="Add Info" >Twice a Week</td>
    </tr> -->
        </tbody>
      </table>
      <div class="sche-note row-max-grid">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum autem
          facilis nesciunt esse adipisci voluptas similique delectus rem
          asperiores repellendus cumque blanditiis quaerat et error, nihil magni
          dicta laboriosam? Maxime.
        </p>
        <button class="btn btn-secondary row-grid">Download Schedule</button>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      schedule: [
        // {
        //   id: 1,
        //   day: "Monday",
        //   classname: "Ballet",
        //   agegroup: "8",
       
        //   endDate: "",
        //   startDate: "",
        //   studioNum: "3",
        //   timeEnd: "18:36",
        //   timeStart: "17:35",
        //      addInformation: "once a week ",
        // },
      ],
    };
  },
  methods: {
    async getSchedule() {
      // console.log(this.form);

      await axios.get("http://localhost:3001/schedule").then((res) => {
       this.schedule=res.data;
      });
    },
  },
  created() {
    this.getSchedule();
  },
};
</script>
