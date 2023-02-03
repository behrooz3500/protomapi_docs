<h1 style="background-color:Gainsboro;">Price Table</h1><div style="margin-left:20px;"> 
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
        <td>product</td>
        <td>int</td>
        <td>product mid</td>
        <td>✓</td>
    </tr>
    <tr>
        <td>price_level</td>
        <td>int</td>
        <td>price_level mid</td>
        <td>✓</td>
    </tr>
    <tr>
        <td>price_type</td>
        <td>int</td>
        <td>
            <ul>
                <li>buy:  1</li>
                <li>sell: 2</li>
            </ul>
        </td>
        <td>✓</td>
    </tr>
    <tr>
        <td>price</td>
        <td>positive-int</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>discount_percent</td>
        <td>float</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>discount_value</td>
        <td>positive-int</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>final_price</td>
        <td>positive-int</td>
        <td></td>
        <td>✓</td>
    </tr>
</table>
</div>


<div>
<h1 style="background-color:Gainsboro;">1- Creating A Price</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>POST</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/prices</td>
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
    'product': 500,
    'price_level': 1,
    'price_type': 2,
    'price': 1000000,
    'discount_percent': 10.0,
    'discount_value': 100000,
    'final_price': 900000
}

r = requests.post('http://domain/api/prices', json=data)</code></pre>
</div>
</div>



<div>
<h1 style="background-color:Gainsboro;">2- Listing Prices</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/prices</td>
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
<pre><code>r = requests.get('http://domain/api/prices')</code></pre>

<h3>Example 2:</h3>
<pre><code>
params = {
    'limit': 50,
    'offset': 10
}
r = requests.get('http://domain/api/prices', params=params)</code></pre>
</div>
</div>


<div><h1 style="background-color:Gainsboro;">3- Retrieving A Price</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/prices/{mid}</td>
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

<pre><code>r = requests.get('http://domain/api/prices/66')</code></pre>
</div>
</div>



<div><h1 style="background-color:Gainsboro;">4- Updating A Price</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>PUT</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/prices/{mid}</td>
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
    'discount_percent': 20.0,
    'discount_value': 200000
    'final_price': 800000
}

r = requests.put('http://domain/api/prices/66', json=data)</code></pre>
</div>
</div>


<div><h1 style="background-color:Gainsboro;">5- Deleting A  Price</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>DELETE</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/prices/{mid}</td>
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

<pre><code>
r = requests.delete('http://domain/api/prices/66')</code></pre>
</div>
</div>