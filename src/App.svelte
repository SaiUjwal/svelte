<script>
  import api from "./api.js";
  console.log(api);
  let keys = Object.keys(api[0]);

  function getIn() {
    alert(
      "row" +
        this.closest("tr").rowIndex +
        "      column" +
        this.closest("td").cellIndex
    );
  }
  function getDetails() {
    console.log(
      this,
      this.closest("tr").rowIndex,
      this.closest("td").cellIndex
    );
    alert(JSON.stringify(api[this.closest("tr").rowIndex - 1]));
  }
</script>

<style>
  td:hover {
    background-color: rgb(125, 233, 233);
    cursor: pointer;
  }
  #biodata {
    font-family: Arial, Helvetica, sans-serif;
    border-collapse: collapse;
    width: 100%;
    overflow: auto;
    display: block;
  }

  #biodata td,
  #biodata th {
    border: 1px solid #ddd;
    padding: 8px;
  }

  #biodata tr:nth-child(even) {
    background-color: #f2f2f2;
  }

  #biodata tr:hover {
    background-color: #ddd;
  }

  #biodata th {
    padding-top: 12px;
    padding-bottom: 12px;
    text-align: left;
    background-color: #4caf50;
    color: white;
  }

  .btn {
    background-color: #4caf50;
  }
</style>

<div>
  <table id="biodata">
    <tr>
      <th>Details</th>
      {#each keys as key}
        <th>{key}</th>
      {/each}
    </tr>
    {#each api as row, i}
      <tr>
        <td>
          <button class="btn" id="data1" on:click={getDetails}>{i + 1}
            row</button>
        </td>
        {#each Object.values(row) as cell}
          <td on:click={getIn}>{cell}</td>
        {/each}
        <td/>
      </tr>
    {/each}
  </table>
</div>
