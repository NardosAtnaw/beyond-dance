<template>
  <div class="schedule-all1 row-grid">
     
    <div class="container1">
    
      <h3>CLASS / PROGRAM SCHEDULE<br/>
(August 29, 2022 - December 10, 2022)</h3>
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

        <tbody>
          <tr >
            <th class="day-txt">Monday</th>

            <tr  v-for="item in Monday" :key="item.id">
              <td class="freespace freespace2" ></td>
              <td data-label="Class Name">{{ item.className }}</td>
              <td data-label="Age">{{ item.ageGroup }}</td>
              <td data-label="Class Time">
                {{ item.timeStart + "-" + item.timeEnd }}
              </td>
              <td data-label="Studio">{{ item.studioNum }}</td>
              <td data-label="Add Info">{{ item.addInformation }}</td>
            </tr>
          </tr>
          <tr>
            <th  class="day-txt">Tuesday</th>

            <tr v-for="item in Tuesday" :key="item.id">
              <td class="freespace freespace2" ></td>
              <td data-label="Class Name">{{ item.className }}</td>
              <td data-label="Age">{{ item.ageGroup }}</td>
              <td data-label="Class Time">
                {{ item.timeStart + "-" + item.timeEnd }}
              </td>
              <td data-label="Studio">{{ item.studioNum }}</td>
              <td data-label="Add Info">{{ item.addInformation }}</td>
            </tr>
          </tr>
              <tr>
            <th  class="day-txt">Wednesday</th>

            <tr v-for="item in Wednesday" :key="item.id">
              <td class="freespace freespace2" ></td>
              <td data-label="Class Name">{{ item.className }}</td>
              <td data-label="Age">{{ item.ageGroup }}</td>
              <td data-label="Class Time">
                {{ item.timeStart + "-" + item.timeEnd }}
              </td>
              <td data-label="Studio">{{ item.studioNum }}</td>
              <td data-label="Add Info">{{ item.addInformation }}</td>
            </tr>
          </tr>
             <tr>
            <th class="day-txt">Thursday</th>

            <tr v-for="item in Thursday" :key="item.id">
              <td class="freespace freespace2" ></td>
              <td data-label="Class Name">{{ item.className }}</td>
              <td data-label="Age">{{ item.ageGroup }}</td>
              <td data-label="Class Time">
                {{ item.timeStart + "-" + item.timeEnd }}
              </td>
              <td data-label="Studio">{{ item.studioNum }}</td>
              <td data-label="Add Info">{{ item.addInformation }}</td>
            </tr>
          </tr>
               <tr>
            <th class="day-txt">Friday</th>

            <tr v-for="item in Friday" :key="item.id">
              <td class="freespace freespace2" ></td>
              <td data-label="Class Name">{{ item.className }}</td>
              <td data-label="Age">{{ item.ageGroup }}</td>
              <td data-label="Class Time">
                {{ item.timeStart + "-" + item.timeEnd }}
              </td>
              <td data-label="Studio">{{ item.studioNum }}</td>
              <td data-label="Add Info">{{ item.addInformation }}</td>
            </tr>
          </tr>
              <tr>
            <th class="day-txt">Saturday</th>

            <tr  v-for="item in Saturday" :key="item.id">
              <td class="freespace freespace2" ></td>
              <td data-label="Class Name">{{ item.className }}</td>
              <td data-label="Age">{{ item.ageGroup }}</td>
              <td data-label="Class Time">
                {{ item.timeStart + "-" + item.timeEnd }}
              </td>
              <td data-label="Studio">{{ item.studioNum }}</td>
              <td data-label="Add Info">{{ item.addInformation }}</td>
            </tr>
          </tr>
        </tbody>
      </table>
      <div class="sche-note row-grid">
        <p>
     Additional Notes:
Team classes in color with additional information  which say twice a week meet twice a week
Age group is in parenthesis next to class name
        </p>
        <button class="btn btn-secondary row-grid">
          <a href="../static/Schedule.png" target="_blank" >
          Download Schedule</a></button>
      </div>
    </div>
    <div class="container-sm">
    
    <h3>CLASS / PROGRAM SCHEDULE<br/>
(August 29, 2022 - December 10, 2022)</h3>
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

      <tbody>
        <tr >
          <th class="day-txt">Monday</th>

          <tr  v-for="item in Monday" :key="item.id">
            <td class="freespace freespace2" ></td>
            <td data-label="Class Name">{{ item.className }}</td>
            <td data-label="Age">{{ item.ageGroup }}</td>
            <td data-label="Class Time">
              {{ item.timeStart + "-" + item.timeEnd }}
            </td>
            <td data-label="Studio">{{ item.studioNum }}</td>
            <td data-label="Add Info">{{ item.addInformation }}</td>
          </tr>
        </tr>
        <tr>
            <th  class="day-txt">Tuesday</th>

            <tr v-for="item in Tuesday" :key="item.id">
              <td class="freespace freespace2" ></td>
              <td data-label="Class Name">{{ item.className }}</td>
              <td data-label="Age">{{ item.ageGroup }}</td>
              <td data-label="Class Time">
                {{ item.timeStart + "-" + item.timeEnd }}
              </td>
              <td data-label="Studio">{{ item.studioNum }}</td>
              <td data-label="Add Info">{{ item.addInformation }}</td>
            </tr>
          </tr>
        <tr>
          
        </tr>
      </tbody>
    </table>
    <div class="sche-note row-grid">
      <p>
   Additional Notes:
Team classes in color with additional information  which say twice a week meet twice a week
Age group is in parenthesis next to class name
      </p>
      <button class="btn btn-secondary row-grid">
        <a href="Schedule.png" target="_blank" download>
        Download Schedule</a></button>
    </div>
  </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      schedule: [],
      Monday: [],
      Tuesday: [],
      Wednesday: [],
      Thursday: [],
      Friday: [],
      Saturday: [],
    };
  },
  methods: {
    async getSchedule() {
      // console.log(this.form);

      await axios.get("https://www.beyonddancers.com/schedule").then((res) => {
        // this.schedule = res.data;
        this.sortArray(res.data);
        // console.log(this.sortArray(res.data));
      });
    },
    sortArray(ary) {
      ary.forEach((item) => {
        // console.log(item.day);
        switch (item.day) {
          case "Monday":
            this.Monday.push(item);
            break;
          case "Tuesday":
            this.Tuesday.push(item);
            break;
          case "Wednesday":
            this.Wednesday.push(item);
            break;
          case "Thursday":
            this.Thursday.push(item);
            break;
          case "Friday":
            this.Friday.push(item);
            // console.log(item.day);
            break;
          case "Saturday":
            this.Saturday.push(item);
            break;

          default:
            break;
        }
      });

      this.schedule.push(this.Monday);
      this.schedule.push(this.Tuesday);
      this.schedule.push(this.Wednesday);
      this.schedule.push(this.Thursday);
      this.schedule.push(this.Friday);
      this.schedule.push(this.Saturday);
      console.log(this.schedule);
      // return mergedAry
    },
  },
  created() {
    this.getSchedule();
    // this.sortArray()
  },
};
</script>
