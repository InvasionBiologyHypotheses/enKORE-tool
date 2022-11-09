<script>
  import Grid from "gridjs-svelte";

  // import Datatable from "svelte-simple-datatables";

  export let data;

  // const settings = { columnFilter: true };
  // let rows;
  $: tableData = data.corpusData.results.bindings.map((x) => x.item.value);

  $: columns = data.corpusData.head.vars.map((x) => {
    return { name: x, data: (cell) => cell };
  });

  const datar = [
    { name: "John", email: "john@example.com" },
    { name: "Mark", email: "mark@gmail.com" },
  ];

  const columnur = [{ name: "EMAN" }, { name: "LIAME" }];
</script>

<Grid data={datar} columns={columnur} />

<Grid data={tableData} {columns} />
<!-- <Datatable {settings} data={data.corpusData.results.bindings} bind:dataRows={rows}>
  <thead>
    {#each data.corpusData.head.vars as v}
      <th data-key={v}>{v}</th>
    {/each}
  </thead>
  <tbody>
    {#if rows}
      {#each $rows as row}
        <tr>
          {#each data.corpusData.head.vars as v}
            <td>{row[v].value}</td>
          {/each}
        </tr>
      {/each}
    {/if}
  </tbody>
</Datatable> -->

<div class="devbox float top right">
  <details>
    <summary>tableData</summary>
    <pre>
      {JSON.stringify(tableData, null, 2)}
    </pre>
  </details>
  <details>
    <summary>columns</summary>
    <pre>
      {JSON.stringify(columns, null, 2)}
    </pre>
  </details>
  <details>
    <summary>raw data</summary>
    <pre>
      {JSON.stringify(data, null, 2)}
    </pre>
  </details>
</div>

<style>
  .devbox {
    max-width: 80vw;
  }
  .float {
    position: absolute;
  }
  .right {
    right: 0;
  }
  .top {
    top: 0;
  }
</style>
