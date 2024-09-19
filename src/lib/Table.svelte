<script>
  // Array passed as a prop to the component
  export let tableData = [];


  export let tableClass = "default-table-style";



</script>

<!-- Table Structure -->
<table class={tableClass}>
  <thead>
      <tr>
          <!-- Assuming your tableData contains objects with 'name', 'age', and 'action' keys -->
          <th>Name</th>
          <th>Email</th>
          <th>Phone</th>
          <th>Designation</th>
      </tr>
  </thead>
  <tbody>
      {#each tableData as row}
          <tr>
              <td>{row.name}</td>
              <td>{row.email}</td>
              <td>{row.phone}</td>
              <td>{row.designation}</td>


          </tr>
      {/each}
  </tbody>
</table>

<style>
  /* Add any specific styles here */
  .default-table-style {
      width: 100%;
      border-collapse: collapse;
  }
  .default-table-style th, .default-table-style td {
      border: 1px solid #ccc;
      padding: 8px;
  }
  .default-button-style {
      padding: 5px 10px;
      background-color: #007BFF;
      color: white;
      border: none;
      cursor: pointer;
  }
  .default-button-style:hover {
      background-color: #0056b3;
  }
</style>
