<h1 style="background-color:Gainsboro;">Invoice Table:</h1><div style="margin-left:20px;">
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
        <td>mid</td>
        <td>int</td>
        <td>Moein id</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>code</td>
        <td>int</td>
        <td>Moein factor_No</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>type</td>
        <td>int</td>
        <td>
            <ul>
                <li>pre:  0</li>
                <li>buy:  1</li>
                <li>sell: 2</li>
            </ul>
        </td>
        <td>✗</td>
    </tr>
    <tr>
        <td>status</td>
        <td>int</td>
        <td>
            <ul>
                <li>draft:  0</li>
                <li>publish:  1</li>
            </ul>
        </td>
        <td>✓</td>
    </tr>
    <tr>
        <td>created_at</td>
        <td>string(iso-8601)</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>updated_at</td>
        <td>string(iso-8601)</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>info</td>
        <td>string(500)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>discount</td>
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
        <td>carry_price</td>
        <td>positive-int</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>driver_name</td>
        <td>string(100)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>driver_tel</td>
        <td>string(50)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>carry_info</td>
        <td>string(500)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>carry_vehicle</td>
        <td>string(50)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>carry_vehicle_plate</td>
        <td>string(50)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>carry_vehicle_color</td>
        <td>string(50)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>tel</td>
        <td>string(100)</td>
        <td>additional tel for customer</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>address</td>
        <td>string(255)</td>
        <td>additional address for customer</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>person</td>
        <td>int</td>
        <td>Person mid, customer</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>temp_person</td>
        <td>int</td>
        <td>TempPerson id, customer</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>visitor</td>
        <td>int</td>
        <td>Person mid</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>driver</td>
        <td>int</td>
        <td>Person mid</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>user</td>
        <td>int</td>
        <td>User id, read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>total</td>
        <td>int</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>items_sum</td>
        <td>int</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>items_total</td>
        <td>int</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>items_net</td>
        <td>int</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>items_discount</td>
        <td>int</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>remain</td>
        <td>int</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>tax</td>
        <td>int</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>tax_percent</td>
        <td>float</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>visitor_price</td>
        <td>int</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>visitor_percent</td>
        <td>float</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
</table>
</div>


<h1 style="background-color:Gainsboro;">InvoiceItem Table:</h1><div style="margin-left:20px;">
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
        <td>price</td>
        <td>positive-int</td>
        <td>unit price</td>
        <td>✓</td>
    </tr>
    <tr>
        <td>quantity1</td>
        <td>int</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>quantity2</td>
        <td>int</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>discount</td>
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
        <td>discount_per_item</td>
        <td>positive-int</td>
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
        <td>product</td>
        <td>int</td>
        <td>Product mid</td>
        <td>✓</td>
    </tr>
    <tr>
        <td>repository</td>
        <td>int</td>
        <td>Repository mid</td>
        <td>✓</td>
    </tr>
    <tr>
        <td>price_level</td>
        <td>int</td>
        <td>PriceLevel mid</td>
        <td>✓</td>
    </tr>
    <tr>
        <td>unit2_in_unit1</td>
        <td>int</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>quantity</td>
        <td>int</td>
        <td>q2 + (q1 * u2_in_u1)</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>sum</td>
        <td>int</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>net</td>
        <td>int</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>tax</td>
        <td>int</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>total</td>
        <td>int</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>visitor_price</td>
        <td>int</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>visitor_percent</td>
        <td>float</td>
        <td>read_only</td>
        <td>✗</td>
    </tr>
</table>
</div>


<div>
<h1 style="background-color:Gainsboro;">1- Creating An Invoice</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>POST</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/all_invoices</td>
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
    'status': 0,
    'discount': 1000,
    'discount_percent': 0.0,
    'carry_price': 100,
    'visitor': 109,
    'person': 78,
    'info': 'invoice information',
    'items': [
        {
            'price': 100,
            'quantity1': 0,
            'quantity2': 5,
            'discount': 0,
            'discount_percent': 0.0,
            'discount_per_item': 0,
            'info': 'some info',
            'product': 9,
            'repository': 1,
            'price_level': 1
        },
        {
            'price': 200,
            'quantity1': 0,
            'quantity2': 2,
            'discount': 40,
            'discount_percent': 10.0,
            'discount_per_item': 20,
            'product': 56,
            'repository': 2,
            'price_level': 1
        }
    ]
}

r = requests.post('http://domain/api/all_invoices', json=data)
</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">2- Listing Invoices:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/all_invoices</td>
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
        <td>status</td>
        <td>int</td>
        <td>invoice status</td>
    </tr>
</table>
    <h3>Example 1:</h3>

<pre><code>r = requests.get('http://domain/api/all_invoices')</code></pre>
    <h3>Example 2:</h3>
<pre><code>
params = {
    'limit': 50,
    'offset': 10,
    'status': 1
}

r = requests.get('http://domain/api/all_invoices', params=params)
</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">3- Retrieving An Invoice:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/all_invoices/{id}</td>
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
<pre><code>r = requests.get('http://domain/api/all_invoices/66')</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">4- Updating An Invoice:</h1>
<div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>PUT</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/all_invoices/{id}</td>
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
    'status': 1,
    'visitor': 109,
    'person': 78,
    'items': [
        {
            'price': 200,
            'quantity1': 0,
            'quantity2': 2,
            'discount': 0,
            'discount_percent': 0.0,
            'discount_per_item': 0,
            'product': 56,
            'repository': 2,
            'price_level': 1
        }
    ]
}

r = requests.put('http://domain/api/all_invoices/66', json=data)
</code></pre>
</div></div>

<div>
<h1 style="background-color:Gainsboro;">5- Deleting An Invoice:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>DELETE</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/all_invoices/{id}</td>
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
<pre><code>r = requests.delete('http://domain/api/all_invoices/66')</code></pre>
</div></div>