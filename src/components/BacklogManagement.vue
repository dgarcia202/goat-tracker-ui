<template>
    <div>
        <v-toolbar flat color="white">
        <v-toolbar-title>{{ title }}</v-toolbar-title>
        <v-divider
            class="mx-2"
            inset
            vertical
        ></v-divider>
        <v-spacer></v-spacer>
        </v-toolbar>
                
        <v-data-table
            :headers="headers"
            :items="rows"
            hide-actions
            class="elevation-1"
        >
            <template slot="items" slot-scope="props">
            <td class="text-xs-left">{{ props.item.code }}</td>
            <td class="text-xs-left">{{ props.item.name }}</td>
            <td class="text-xs-right">{{ props.item.estimation }}</td>
            <td class="text-xs-right">{{ props.item.completed }}</td>
            <td class="text-xs-left">{{ props.item.status }}</td>
            </template>
        </v-data-table>
    </div>
</template>
<script>
export default {
    name: 'BacklogManagement',
    data () {
      return {
        title: 'Release Backlog',
        headers: [
          {
            text: 'Feature',
            align: 'left',
            sortable: true,
            value: 'feature',
            width: '150px'
          },
          { text: 'Name', align: 'left', sortable: true, value: 'name', width: '650px' },
          { text: 'Estimation', align: 'right', value: 'estimation', width: '80px' },
          { text: '% Completed', align: 'right', value: 'completed', width: '80px' },
          { text: 'Status', value: 'status', width: '250px' }
        ],
        rows: [
         {
             code: '1232456',
             name: 'autheticated acces and role verification',
             estimation: 120,
             completed: 50,
             status: 'in progress'
         },
         {
             code: '1232456',
             name: 'autheticated acces and role verification',
             estimation: 120,
             completed: 50,
             status: 'in progress'
         },
         {
             code: '1232456',
             name: 'autheticated acces and role verification',
             estimation: 120,
             completed: 50,
             status: 'in progress'
         },
         {
             code: '1232456',
             name: 'autheticated acces and role verification',
             estimation: 120,
             completed: 50,
             status: 'in progress'
         },
         {
             code: '1232456',
             name: 'autheticated acces and role verification',
             estimation: 120,
             completed: 50,
             status: 'in progress'
         },
         {
             code: '1232456',
             name: 'autheticated acces and role verification',
             estimation: 120,
             completed: 50,
             status: 'in progress'
         },
         {
             code: '1232456',
             name: 'autheticated acces and role verification',
             estimation: 120,
             completed: 50,
             status: 'in progress'
         },
         {
             code: '1232456',
             name: 'autheticated acces and role verification',
             estimation: 120,
             completed: 50,
             status: 'in progress'
         }                                     
        ]
      }
    }    
}
</script>
