<h1 style="background-color:Gainsboro;">Barcode Table</h1><div style="margin-left:20px;"> 
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
        <td>text</td>
        <td>string(100)</td>
        <td>barcode value</td>
        <td>✓</td>
    </tr>
</table>
</div>


<div>
<h1 style="background-color:Gainsboro;">1- Creating A Barcode</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>POST</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/barcodes</td>
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
    'text': '123456789abcdef'
}

r = requests.post('http://domain/api/barcodes', json=data)
</code></pre>
</div>
</div>



<div>
<h1 style="background-color:Gainsboro;">2- Listing Barcodes</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/barcodes</td>
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
<pre><code>r = requests.get('http://domain/api/barcodes')</code></pre>

<h3>Example 2:</h3>
<pre><code>
params = {
    'limit': 50,
    'offset': 10
}

r = requests.get('http://domain/api/barcodes', params=params)
</code></pre>
</div>
</div>



<div>
<h1 style="background-color:Gainsboro;">3- Retrieving A Barcode</h1><div style="margin-left:20px;"> 
<table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/barcodes/{mid}</td>
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
<pre><code>r = requests.get('http://domain/api/barcodes/66')</code></pre>
</div>
</div>



<div><h1 style="background-color:Gainsboro;">4- Updating A Barcode</h1><div style="margin-left:20px;"> 
<table>
        <tr>
            <td><strong>Method</strong></td>
            <td>PUT</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/barcodes/{mid}</td>
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
    'text': 'somenewbarcodevalue'
}

r = requests.put('http://domain/api/barcodes/66', json=data)
</code></pre>
</div>
</div>


<div>
<h1 style="background-color:Gainsboro;">5- Deleting A Barcode</h1><div style="margin-left:20px;"> 
<table>
        <tr>
            <td><strong>Method</strong></td>
            <td>DELETE</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/barcodes/{mid}</td>
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
<pre><code>r = requests.delete('http://domain/api/barcodes/66')</code></pre>
</div>
</div>