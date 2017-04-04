# MMM-vvsDeparture
A MagicMirror2 Module for public transport in Stuttgart, Germany

## Installation
Run these commands at the root of your magic mirror install.

```shell
cd modules
git clone https://github.com/wenzul/MMM-vvsDeparture
```

## Using the module
To use this module, add the following configuration block to the modules array in the `config/config.js` file:
```js
var config = {
    modules: [
        {
            module: 'MMM-vvsDeparture',
            config: {
                // See below for configurable options
            }
        }
    ]
}
```

Note that a `position` setting is not required.

### Configuration options
The following properties can be configured:

<table width="100%">
	<!-- why, markdown... -->
	<thead>
		<tr>
			<th>Option</th>
			<th width="100%">Description</th>
		</tr>
	<thead>
	<tbody>
		<tr>
			<td><code>station_id</code></td>
			<td>
        A value which represents the station id of the bus stop. Here is a full list of all station within the VVS public transport network you can find out yours (<a href="https://efa-api.asw.io/api/v1/station/">https://efa-api.asw.io/api/v1/station/</a>).
				<br><br><b>Possible values:</b> <code>integer</code>
				<br><b>Default value:</b> <code>5002201</code>
			</td>
		</tr>
		<tr>
			<td><code>station_name</code></td>
			<td>The displayed name for your bus stop.
			<br><br><b>Possible values:</b> <code>string</code>
			<br><b>Default value:</b> <code>Libanonstraße</code>
			</td>
		</tr>
		<tr>
			<td><code>maximumEntries</code></td>
      <td>Number of departure entries which will be shown.
      				<br><br><b>Possible values:</b> <code>integer</code>
				<br><b>Default value:</b> <code>6</code>
			</td>
		</tr>
		<tr>
			<td>
			    <code>reloadInterval</code>
			</td>
      <td> The refresh rate dparture entries will be updated in milliseconds. 
      				<br><br><b>Possible values:</b> <code>integer</code>
				<br><b>Default value:</b> <code>1 * 60 * 1000</code> e.q. one minute
			</td>
		</tr>
		<tr>
			<td>
			    <code>directions</code>
			</td>
            <td>Filter departures for directions.
      			<br><br><b>Possible values:</b> <code>array</code>
				<br><b>Default value:</b> <code>[]</code>
			</td>
		</tr>
	</tbody>
</table>

