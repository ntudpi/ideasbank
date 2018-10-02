# ideasbank


## To use


For the table that you want to sort, put the id as `myTable` and add class `tablesorter`. After that, put the following code after the table
```
<script type="text/javascript" src="https://cdn.rawgit.com/ntudpi/ideasbank/gh-pages/tablesorter.js"></script>
<script type="text/javascript" src="https://cdn.rawgit.com/ntudpi/ideasbank/gh-pages/latest.js"></script> 
<script>    $(document).ready(function () {
        jQuery.tablesorter.addParser({
            id: "fancyNumber",
            is: function (s) {
                return /^[0-9]?[0-9,\.]*$/.test(s);
            },
            format: function (s) {
                return jQuery.tablesorter.formatFloat(s.replace(/,/g, ''));
            },
            type: "numeric"
        });

        $("#myTable").tablesorter({
            headers: { 0: { sorter: 'fancyNumber'} },
            widgets: ['zebra']
        });
    }); </script>
<script type="text/javascript" src="https://cdn.rawgit.com/ntudpi/ideasbank/gh-pages/jquery.tablesorter.min.js"></script>
<script type="text/javascript">
$(document).ready(function() 
    { 
        $("#myTable").tablesorter(); 
    } 
); 
</script>
<script type="text/javascript">
jQuery('#myTable').tablesorter();
</script>
```
