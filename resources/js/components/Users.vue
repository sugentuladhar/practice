<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card card-default">
                    <div class="card-header">Profile Component</div>

                    <div class="card-body">
                        <table id="example2" class="table table-bordered table-striped">
                            <thead>
                                <tr>
                                    <th>Rendering engine</th>
                                    <th>Browser</th>
                                    <th>Platform(s)</th>
                                    <th>Engine version</th>
                                    <th>CSS grade</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td>Trident</td>
                                    <td>Internet
                                        Explorer 4.0
                                    </td>
                                    <td>Win 95+</td>
                                    <td> 4</td>
                                    <td>X</td>
                                </tr>
                            </tbody>
                            <tfoot>
                                <tr>
                                    <th>Rendering engine</th>
                                    <th>Browser</th>
                                    <th>Platform(s)</th>
                                    <th>Engine version</th>
                                    <th>CSS grade</th>
                                </tr>
                            </tfoot>
                        </table>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data(){
		    return{
                employees: [
                    {
                        Name: 'Tiger Nixon',
                        Position: 'System Architect',
                        Office: 'tokyo',
                        Age: '61',
                        StartDate: '2011/04/25',
                        Salary: '$320,800',
                    },
                ],
                name: '',
                position: '',
                office: '',
                age: '',
                startDate: '',
                salary: '',
                dataTable: null
            }
		},

		methods: {
		    addEmployee(){
			  this.dataTable.row.add([
			      this.name,
			      this.position,
			      this.office,
			      this.age,
			      this.startDate,
			      this.salary,
			  ]).draw(false);
		    }
		},

		mounted(){
		    this.dataTable = $('#example2').DataTable({
                                            'paging'      : true,
                                            'lengthChange': false,
                                            'searching'   : false,
                                            'ordering'    : true,
                                            'info'        : true,
                                            'autoWidth'   : false
                                            });
		}
    }
</script>
