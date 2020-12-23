<script>
import api from './api'
    let row=api;
    let value=" "
    let Header='';
    row.forEach((o) => {  
for (var peopleName in o) {
   Header+=peopleName ;
}});
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
                    <thead>
                        <tr>
                          
                          <th>{Header}</th>
                                        
                       
                        
                            
                        </tr>
                        
                           
                      </thead>
                    <tbody>
                       <tr>
                        {#each row as item}
                        <tr>
                          <td> {item.id }</td>
                          <td>{item.time}</td>
                          <td> {item. qrCode} </td>
                          <td>{item.name}</td>
                          <td>{item.comment}</td>
                          <td> {item. autoEntry} </td>
                          <td>{item.buildingId}</td>
                          <td> {item. address} </td>
                          <td>{item.category}</td>
                          <td>{item.vehicleNumber}</td>
                          <td> {item. validTill} </td>
                          <td>{item.imageUploaded}</td>
                          <td> {item. reference} </td>
                          <td>{item.active}</td>
                          <td>{item.mobile}</td>
                          <td> {item. contractorId} </td>
                          <td>{item.contractorName}</td>
                          <td> {item. idProof} </td>
                          <td>{item.imageData}</td>
                          <td>{item.gender}</td>
                          <td> {item. updatedOn} </td>
                          <td>{item.createdOn}</td>
                          <td> {item. createdBy} </td>
                          <td>{item.updatedBy}</td>
                          <td>{item.workerProfileVersion}</td>
                          <td> {item. contractorProfileVersion} </td>
                          <td>{item.sequence}</td>
                          <td> {item. categoryName} </td>
                          <td>{item.designationName}</td>
                          <td>{item.categoryId}</td>
                          <td> {item. designationId} </td>
                          <td>{item.fatherName}</td>
                          <td> {item. dob} </td>
                          <td>{item.faceTemplateUploaded}</td>
                          <td>{item.faceTemplate}</td>
                          <td> {item.templateCreateDate} </td>
                          <td>{item.relation}</td>
                          <td> {item. maritalStatus} </td>
                          <td>{item.aadharNo}</td>
                          <td>{item.activationDate}</td>
                          <td> {item. pf} </td>
                          <td>{item.uan}</td>
                          <td> {item. prefix} </td>
                          <td>{item.haveEmpId}</td>
                          <td>{item.phoneImage}</td>
                          <td> {item. projectId} </td>
                          <td>{item.stateId}</td>
                          <td> {item. stateName} </td>
                          <td>{item.pinCode}</td>
                          <td>{item.permanentAddress}</td>
                          <td> {item. displayName} </td>
                          <td>{item.projectAddress}</td>
                          <td> {item. projectDisplayName} </td>
                          </tr>
                        {/each}</tr>
                </tbody>
                </table>
                
                </div>
                <select bind:value>
                  {#each row as item}
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
           
         
       
