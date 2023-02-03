<h1 style="background-color:Gainsboro;">Product Table</h1><div style="margin-left:20px;">
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
        <td>code</td>
        <td>int</td>
        <td>Moein code</td>
        <td>✓</td>
    </tr>
    <tr>
        <td>name</td>
        <td>string(255)</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>active</td>
        <td>bool</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>info</td>
        <td>string(500)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>category</td>
        <td>int</td>
        <td>product_category mid</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>unit_type</td>
        <td>int</td>
        <td>
            <ul>
                <li>single: 0</li>
                <li>dual1: 1</li>
                <li>dual2: 2</li>
            </ul>
        </td>
        <td>✓</td>
    </tr>
    <tr>
        <td>unit1</td>
        <td>string(50)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>unit2</td>
        <td>string(50)</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>unit2_in_unit1</td>
        <td>int</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>taxable</td>
        <td>bool</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>visitor_percent</td>
        <td>float</td>
        <td></td>
        <td>✗</td>
    </tr>
</table>
</div>


<h1 style="background-color:Gainsboro;">Quantity Table</h1><div style="margin-left:20px;">
<table>
    <tr>
        <td><strong>Attribute</strong></td>
        <td><strong>Type</strong></td>
        <td><strong>Description</strong></td>
        <td><strong>Required</strong></td>
    </tr>
    <tr>
        <td>quantity</td>
        <td>int</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>repository</td>
        <td>int</td>
        <td>repository mid</td>
        <td>✓</td>
    </tr>
</table>
</div>


<div>
<h1 style="background-color:Gainsboro;">1- Creating A Product</h1><div style="margin-left:20px;">  
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>POST</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/products</td>
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
    'code': 1000,
    'name': 'new product',
    'active': True,
    'info': 'some information about product',
    'category': 100,
    'unit_type': 0,
    'unit2': 'box',
    'taxable': True,
    'visitor_percent': 5.0
}

r = requests.post('http://domain/api/products', json=data)</code></pre>
</div>
</div>



<div><h1 style="background-color:Gainsboro;">2- Listing  Product</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/products</td>
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
    <tr>
        <td>active</td>
        <td>bool</td>
        <td></td>
    </tr>
    <tr>
        <td>category</td>
        <td>int</td>
        <td>product_category mid</td>
    </tr>
</table>
    <h3>Example 1:</h3>
<pre><code>r = requests.get('http://domain/api/products')</code></pre>

<h3>Example 2:</h3>
<pre><code>
params = {
    'limit': 50,
    'offset': 10
}

r = requests.get('http://domain/api/products', params=params)</code></pre>

<h3>Example 3:</h3>
<pre><code>
params = {
    'limit': 100,
    'category': 10,
    'active': True
}

r = requests.get('http://domain/api/products', params=params)</code></pre>
</div>
</div>


<div><h1 style="background-color:Gainsboro;">3- Retrieving A Product</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/products/{mid}</td>
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

<pre><code>r = requests.get('http://domain/api/products/66')</code></pre>
</div>
</div>



<div><h1 style="background-color:Gainsboro;">4- Updating A Product</h1><div style="margin-left:20px;">  
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>PUT</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/products/{mid}</td>
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
    'name': 'some new name',
    'info': 'new description',
    'category': None,
}

r = requests.put('http://domain/api/products/66', json=data)</code></pre>
</div>
</div>



<div><h1 style="background-color:Gainsboro;">5- Deleting A Product</h1><div style="margin-left:20px;">  
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>DELETE</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/products/{mid}</td>
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

<pre><code>r = requests.delete('http://domain/api/products/66')</code></pre>
</div>
</div>



<div><h1 style="background-color:Gainsboro;">6- Searching For A Product</h1><div style="margin-left:20px;">  
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/products/search</td>
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
        <td>q</td>
        <td>string</td>
        <td>all fields</td>
    </tr>
    <tr>
        <td>code</td>
        <td>int</td>
        <td></td>
    </tr>
    <tr>
        <td>name</td>
        <td>string</td>
        <td></td>
    </tr>
    <tr>
        <td>info</td>
        <td>string</td>
        <td></td>
    </tr>
    <tr>
        <td>barcodes</td>
        <td>string</td>
        <td></td>
    </tr>
</table>
    <h3>Example 1:</h3>
<pre><code>
params = {
    'q': 'some keyword'
}

r = requests.get('http://domain/api/products/search', params=params)</code></pre>

<h3>Example 2:</h3>
<pre><code>
params = {
    'barcodes': '123456'
}

r = requests.get('http://domain/api/products/search', params=params)</code></pre>
</div>
</div>



<div><h1 style="background-color:Gainsboro;">7- Listing Quantities</h1><div style="margin-left:20px;">  
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/products/{mid}/quantities</td>
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

<pre><code>r = requests.get('http://domain/api/products/66/quantities')</code></pre>
</div>
</div>


<div><h1 style="background-color:Gainsboro;">8- Updating A quantity</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>PUT</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/products/{mid}/quantities</td>
        </tr>
        <tr>
            <td><strong>Success code</strong></td>
            <td>200</td>
        </tr>
        <tr>
            <td><strong>Failure codes</strong></td>
            <td>400, 404</td>
        </tr>
    </table>
    <h3>Example 1:</h3>
<pre><code>
data = [
    {
        'repository': 1,
        'quantity': 1000
    }
]

r = requests.put('http://domain/api/products/66/quantities', json=data)</code></pre>

<h3>Example 2:</h3>
<pre><code>
data = [
    {
        'repository': 1,
        'quantity': 1000
    },
    {
        'repository': 2,
        'quantity, '2000,
    }
]

r = requests.put('http://domain/api/products/66/quantities', json=data)</code></pre>
</div>
</div>