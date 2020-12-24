<script>



import api from './api'
    let s=api;
    let value=" ";
    let Data=''
    let Header=Object.keys(s[0])
    for(var x of s)
    Data+=Object.values(x);
    
      function handleClick() {
    alert(value);
    }
  </script>
    
    <!-- svelte-ignore component-name-lowercase --> 
 <div class="header">
    <h1 style="color:blue;">Table generation using svelte</h1>
    </div>
            <div class="main">
                <table>
                    
                        <tr>
                         {#each Header as header}
                          <th>{header}</th>       
                      {/each}     
                        </tr>

                        
                      <tr>
                          <td> {Data}</td>
                   </tr> 
                        
                        
                        
                      
                </table>
                
                </div>
                <select bind:value>
                  {#each s as item}
                    <option value={item.id}>{item.id}</option> 
                  {/each}
                </select>
                <button  on:click={handleClick}>
                  Click me
                </button>
          
          <!-- svelte-ignore a11y-missing-attribute -->
          <html>
          <style>
            table {
              font-family: arial;
              border-collapse: collapse;
              width: 150%;
            }
          
            td,th {
              border: 3px solid #ff3855;
              text-align: left;
              padding: 5px;
            }
          </style>
          </html>
           
         
       
