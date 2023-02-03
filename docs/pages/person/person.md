<h1 style="background-color:Gainsboro;"> Person Table</h1>
<div style="margin-left:20px;">
<table>
    <tr>
        <td><strong>Attribute</strong</td>
        <td><strong>Type</strong</td>
        <td><strong>Description</strong</td>
        <td><strong>Required</strong</td>
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
        <td>first_name</td>
        <td>string(50)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>last_name</td>
        <td>string(50)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>name</td>
        <td>string(255)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>name_prefix</td>
        <td>string(50)</td>
        <td>mr, mrs, ...</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>economy_code</td>
        <td>string(50)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>national_code</td>
        <td>string(11)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>site</td>
        <td>string(200)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>email</td>
        <td>string(255)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>job</td>
        <td>string(50)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>info</td>
        <td>string(500)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>active</td>
        <td>bool</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>group</td>
        <td>int</td>
        <td>person group mid</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>buy_price_level</td>
        <td>int</td>
        <td>price level mid</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>sell_price_level</td>
        <td>int</td>
        <td>price level mid</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>company</td>
        <td>string(200)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>company_registration_code</td>
        <td>string(50)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>company_address</td>
        <td>string(200)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>province</td>
        <td>string(50)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>city</td>
        <td>string(50)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>zip_code</td>
        <td>string(50)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>address</td>
        <td>string(200)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>bank_account</td>
        <td>string(50)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>bank_cart</td>
        <td>string(50)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>visitor</td>
        <td>bool</td>
        <td>is visitor?</td>
        <td>✓</td>
    </tr>
    <tr>
        <td>visitor_percent</td>
        <td>float</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>courier</td>
        <td>bool</td>
        <td>is courier?</td>
        <td>✓</td>
    </tr>
    <tr>
        <td>delivery_price</td>
        <td>int</td>
        <td></td>
        <td>✗</td>
    </tr>
</table>
</div>


<div>
<h1 style="background-color:Gainsboro;">1- Creating A Person: </h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>POST</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/persons</td>
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
<h5>Example:</h5>
<pre><code>
data = {
    'mid': 1000,
    'code': 1000,
    'first_name': 'kaveh',
    'last_name': 'mehrbanian',
    'name': 'kaveh mehrbanian',
    'email': 'mehrbaniankaveh@gmail.com',
    'active': True,
    'group': 10,
    'sell_price_level': 1,
    'buy_price_level': 1,
    'address': 'some address',
    'visitor': True,
    'visitor_percent': 10.0,
    'courier': False,
}

r = requests.post('http://domain/api/persons', json=data)</code></pre>
</div></div>



<div>
<h1 style="background-color:Gainsboro;">2- Listing Persons: </h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/persons</td>
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
<h5>Parameters</h5>
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
        <td>group</td>
        <td>int</td>
        <td>person group mid</td>
    </tr>
    <tr>
        <td>visitor</td>
        <td>bool</td>
        <td></td>
    </tr>
    <tr>
        <td>courier</td>
        <td>bool</td>
        <td></td>
    </tr>
    
</table>
<h5>Example 1:</h5>
<pre><code>r = requests.get('http://domain/api/persons')</code></pre>

<h5>Example 2:</h5>
<pre><code>
params = {
    'limit': 50,
    'offset': 10
}

r = requests.get('http://domain/api/persons', params=params)
</code></pre>

<h5>Example 3:</h5>
<pre><code>
params = {
    'limit': 100,
    'group': 10,
    'active': True
}

r = requests.get('http://domain/api/persons', params=params)
</code></pre>

<h5>Example 4:</h5>
<pre><code>
params = {
    'visitor': True
}

r = requests.get('http://domain/api/persons', params=params)
</code></pre>

<h5>Example 5:</h5>
<pre><code>
params = {
    'active': True,
    'group': 20,
    'courier': False
}

r = requests.get('http://domain/api/persons', params=params)
</code></pre>
</div></div>



<div>
<h1 style="background-color:Gainsboro;">3- Retrieving A Person: </h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/persons/{mid}</td>
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

<pre><code>r = requests.get('http://domain/api/persons/66')</code></pre>
</div></div>



<div>
<h1 style="background-color:Gainsboro;">4- Updating A Person: </h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>PUT</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/persons/{mid}</td>
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
    'first_name': 'some first',
    'last_name': 'some last',
    'group': None
}

r = requests.put('http://domain/api/persons/66', json=data)
</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">5- Deleting A Person: </h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>DELETE</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/persons/{mid}</td>
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

<pre><code>r = requests.delete('http://domain/api/persons/66')</code></pre>
</div></div>



<div>
<h1 style="background-color:Gainsboro;">6- Searching For A Person: </h1>
<div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/persons/search</td>
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
<h5>Parameters</h5>
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
        <td>tels</td>
        <td>string</td>
        <td></td>
    </tr>
</table>
<h5>Example 1:</h5>
<pre><code>
params = {
    'q': 'some keyword'
}

r = requests.get('http://domain/api/persons/search', params=params)
</code></pre>

<h5>Example 2:</h5>
<pre><code>
params = {
    'tels': '123456789'
}

r = requests.get('http://domain/api/persons/search', params=params)
</code></pre>
</div></div>