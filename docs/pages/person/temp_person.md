<h1 style="background-color:Gainsboro;">TempPerson Table</h1><div style="margin-left:20px;">
<table>
    <tr>
        <td><strong>Attribute</strong></td>
        <td><strong>Type</strong></td>
        <td><strong>Description</strong></td>
        <td><strong>Required</strong></td>
    </tr>
    <tr>
        <td>id</td>
        <td>int</td>
        <td>primary_key, read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>first_name</td>
        <td>string(50)</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>last_name</td>
        <td>string(50)</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>name_prefix</td>
        <td>string(50)</td>
        <td></td>
        <td>✓</td>
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
        <td>bank_card</td>
        <td>string(50)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>remain</td>
        <td>int</td>
        <td>can be (-)negative or (+)positive</td>
        <td>✗</td>
    </tr>
</table>
</div>


<h1 style="background-color:Gainsboro;">TempPersonTel Table</h1><div style="margin-left:20px;">
<table>
    <tr>
        <td><strong>Attribute</strong></td>
        <td><strong>Type</strong></td>
        <td><strong>Description</strong></td>
        <td><strong>Required</strong></td>
    </tr>
    <tr>
        <td>id</td>
        <td>int</td>
        <td>primary_key, read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>tel</td>
        <td>string(50)</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>caption</td>
        <td>string(50)</td>
        <td>phone, mobile, fax, ...</td>
        <td>✗</td>
    </tr>
</table>
</div>



<div>
<h1 style="background-color:Gainsboro;"> 1-Creating A TempPerson</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>POST</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/temp_persons</td>
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
    'first_name': 'kaveh',
    'last_name': 'mehrbanian',
    'name_prefix': 'mr',
    'email': 'mehrbaniankaveh@gmail.com',
    'group': 10,
    'sell_price_level': 1,
    'buy_price_level': 1,
    'address': 'some address',
    'tels': [
        {'tel': '123456789', 'caption': 'mobile'},
        {'tel': '666777890', 'caption': 'desk'}
    ],
    'remain': -5500
}

r = requests.post('http://domain/api/temp_persons', json=data)
</code></pre>
</div>
</div>



<div>
<h1 style="background-color:Gainsboro;">2- Listing TempPersons</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/temp_persons</td>
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
<pre><code>r = requests.get('http://domain/api/temp_persons')</code></pre>
    <h3>Example 2:</h3>
<pre><code>
params = {
    'limit': 50,
    'offset': 10
}

r = requests.get('http://domain/api/temp_persons', params=params)
</code></pre>
</div>
</div>



<div>
<h1 style="background-color:Gainsboro;">3- Retrieving A TempPerson</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/temp_persons/{id}</td>
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

<pre><code>r = requests.get('http://domain/api/temp_persons/66')</code></pre>
</div>
</div>



<div>
<h1 style="background-color:Gainsboro;">4- Updating A TempPerson</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>PUT</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/temp_persons/{id}</td>
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

r = requests.put('http://domain/api/temp_persons/66', json=data)</code></pre>
</div>
</div>



<div>
<h1 style="background-color:Gainsboro;">5- Deleting A TempPerson</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>DELETE</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/temp_persons/{id}</td>
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
<pre><code>r = requests.delete('http://domain/api/temp_persons/66')</code></pre>
</div>
</div>



<div>
<h1 style="background-color:Gainsboro;">6- Converting A TempPerson</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>PUT</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/temp_persons/{id}/convert</td>
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
    'mid': 16,
    'code': 9
}

r = requests.put('http://domain/api/temp_persons/66/convert', json=data)</code></pre>
</div>
</div>