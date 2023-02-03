<h1 style="background-color:Gainsboro;">Portion Table</h1><div style="margin-left:20px;">
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
        <td>person</td>
        <td>int</td>
        <td>person mid</td>
        <td>✓</td>
    </tr>
    <tr>
        <td>product</td>
        <td>int</td>
        <td>product mid</td>
        <td>✓</td>
    </tr>
    <tr>
        <td>percentage</td>
        <td>float</td>
        <td>percentage for person on product</td>
        <td>✓</td>
    </tr>
</table>
</div>


<div>
<h1 style="background-color:Gainsboro;">1- Creating A Portion:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>POST</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/portions</td>
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
    'person': 100,
    'product': 600,
    'percentage': 10.0
}

r = requests.post('http://domain/api/portions', json=data)
</code></pre>
</div></div>



<div><h1 style="background-color:Gainsboro;">2- Listing Portions:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/portions</td>
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
<pre><code>r = requests.get('http://domain/api/portions')</code></pre>

<h3>Example 2:</h3>
<pre><code>
params = {
    'limit': 50,
    'offset': 10
}

r = requests.get('http://domain/api/portions', params=params)
</code></pre>
</div></div>



<div><h1 style="background-color:Gainsboro;">3- Retrieving A Portion:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/portions/{mid}</td>
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
<pre><code>r = requests.get('http://domain/api/portions/66')</code></pre>
</div></div>



<div><h1 style="background-color:Gainsboro;">4- Updating A Portion:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>PUT</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/portions/{mid}</td>
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
    'percentage': 14.2
}

r = requests.put('http://domain/api/portions/66', json=data)</code></pre>
</div></div>



<div>
<h1 style="background-color:Gainsboro;">5- Deleting A Portion:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>DELETE</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/portions/{mid}</td>
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
<pre><code>r = requests.delete('http://domain/api/portions/66')</code></pre>
</div>
</div>