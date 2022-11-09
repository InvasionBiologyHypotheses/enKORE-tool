<script>
  export let data;

  $: ({ countries } = data);
</script>

<table>
  <thead>
    <tr>
      <td>
        <p>Create Quickstatements by country</p>
      </td>
    </tr>
  </thead>
  <tbody>
    {#each $countries.data.locations as location}
      <tr>
        <td>
          <a href={location.countrycode}>{location.location}</a>
        </td>
      </tr>
    {/each}
  </tbody>
</table>

<details>
  <summary>raw data</summary>
  <pre>
    {JSON.stringify($countries.data, null, 2)}
  </pre>
</details>
