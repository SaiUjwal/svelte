<script>
  import api from "./api.js";
  console.log(api);
  let keys = Object.keys(api[0]);

  function getIn() {
    alert(
      "row" +
        this.closest("tr").rowIndex +
        "      column" +
        (this.closest("td").cellIndex + 1)
    );
  }
</script>

<style>
  td:hover {
    background-color: rgb(128, 231, 231);
    cursor: pointer;
  }
  #biodata {
    font-family: Arial, Helvetica, sans-serif;
    border-collapse: collapse;
    width: 100%;
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
</style>

<div>
  <table id="biodata">
    <tr>
      {#each keys as key}
        <th>{key}</th>
      {/each}
    </tr>
    {#each api as row}
      <tr>
        {#each Object.values(row) as cell}
          <td on:click={getIn}>{cell}</td>
        {/each}
      </tr>
    {/each}
  </table>
</div>
