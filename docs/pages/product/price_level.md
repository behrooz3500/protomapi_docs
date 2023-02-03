<h1 style="background-color:Gainsboro;">PriceLevel Table</h1><div style="margin-left:20px;"> 
<table>
    <tr>
        <td><strong>Attribute</strong></td>
        <td><strong>Type</strong></td>
        <td><strong>Description</strong></td>
        <td><strong>Required</strong></td>
    </tr>
    <tr>
        <td>mid</td>
        <td>int</td>
        <td>Moein id</td>
        <td>✓</td>
    </tr>
    <tr>
        <td>name</td>
        <td>string(50)</td>
        <td></td>
        <td>✓</td>
    </tr>
</table>
</div>


<div>
<h1 style="background-color:Gainsboro;">1- Creating A PriceLevel</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>POST</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/price_levels</td>
        </tr>
        <tr>
            <td><strong>Success code</strong></td>
            <td>201</td>
        </tr>
        <tr>
            <td><strong>Failure code</strong></td>
            <td>400</td>
        </tr>
    </table>
    <h3>Example:</h3>

<pre><code>
data = {
    'mid': 1000,
    'name': 'new price level'
}

r = requests.post('http://domain/api/price_levels', json=data)
</code></pre>
</div>
</div>



<div>
<h1 style="background-color:Gainsboro;">2- Listing PriceLevels</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/price_levels</td>
        </tr>
        <tr>
            <td><strong>Success code</strong></td>
            <td>200</td>
        </tr>
        <tr>
            <td><strong>Failure code</strong></td>
            <td>-</td>
        </tr>
    </table>
<h3>Parameters</h3>
<table>
    <tr>
        <td><strong>Param</strong></td>
        <td><strong>Type</strong></td>
        <td><strong>Description</strong></td>
    </tr>
    <tr>
        <td>limit</td>
        <td>int</td>
        <td>number per page</td>
    </tr>
    <tr>
        <td>offset</td>
        <td>int</td>
        <td>skip before beginning</td>
    </tr>
</table>
    <h3>Example 1:</h3>
<pre><code>r = requests.get('http://domain/api/price_levels')</code></pre>

<h3>Example 1:</h3>
<pre><code>
params = {
    'limit': 50,
    'offset': 10
}

r = requests.get('http://domain/api/price_levels', params=params)</code></pre>
</div>
</div>



<div><h1 style="background-color:Gainsboro;">3- Retrieving A PriceLevel</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/price_levels/{mid}</td>
        </tr>
        <tr>
            <td><strong>Success code</strong></td>
            <td>200</td>
        </tr>
        <tr>
            <td><strong>Failure code</strong></td>
            <td>404</td>
        </tr>
    </table>
    <h3>Example:</h3>

<pre><code>r = requests.get('http://domain/api/price_levels/66')</code></pre>
</div>
</div>



<div><h1 style="background-color:Gainsboro;">4- Updating A PriceLevel</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>PUT</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/price_levels/{mid}</td>
        </tr>
        <tr>
            <td><strong>Success code</strong></td>
            <td>200</td>
        </tr>
        <tr>
            <td><strong>Failure code</strong></td>
            <td>400</td>
        </tr>
    </table>
    <h3>Example:</h3>

<pre><code>
data = {
    'name': 'some new name'
    'parent': 400
}

r = requests.put('http://domain/api/price_levels/66', json=data)</code></pre>
</div>
</div>


<div>
<h1 style="background-color:Gainsboro;">5- Deleting A  PriceLevel</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>DELETE</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/price_levels/{mid}</td>
        </tr>
        <tr>
            <td><strong>Success code</strong></td>
            <td>204</td>
        </tr>
        <tr>
            <td><strong>Failure code</strong></td>
            <td>404</td>
        </tr>
    </table>
    <h3>Example:</h3>

<pre><code>r = requests.delete('http://domain/api/price_levels/66')</code></pre>
</div>
</div>