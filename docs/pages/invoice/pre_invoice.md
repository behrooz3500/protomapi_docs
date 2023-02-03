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

<div>
<h1 style="background-color:Gainsboro;">1- Creating PreInvoice:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>POST</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/invoices/</td>
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
    'info': 'pre_invoice information',
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

r = requests.post('http://domain/api/invoices', json=data)
</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">2- Listing PreInvoices:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/pre_invoices</td>
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
        <td>pre_invoice status</td>
    </tr>
</table>
    <h3>Example 1:</h3>

<pre><code>r = requests.get('http://domain/api/pre_invoices')</code></pre>


<h3>Example 2:</h3>

<pre><code>
params = {
    'limit': 50,
    'offset': 10,
    'status': 1
}

r = requests.get('http://domain/api/pre_invoices', params=params)
</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">3- Retrievng A PreInvoice:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/pre_invoices/{id}</td>
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
<pre><code>r = requests.get('http://domain/api/pre_invoices/66')</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">4- Update A PreInvoice</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>PUT</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/pre_invoices/{id}</td>
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

r = requests.put('http://domain/api/pre_invoices/66', json=data)
</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">5- Deleting A PreInvoice:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>DELETE</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/pre_invoices/{id}</td>
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
<pre><code>r = requests.delete('http://domain/api/pre_invoices/66')</code></pre>
</div></div>



<div>
<h1 style="background-color:Gainsboro;">6- Searching For A PreInvoices:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/pre_invoices/search</td>
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
        <td>id</td>
        <td>int</td>
        <td>pre_invoice id</td>
    </tr>
    <tr>
        <td>mid</td>
        <td>int</td>
        <td>moein id </td>
    </tr>
    <tr>
        <td>code</td>
        <td>int</td>
        <td>moein code </td>
    </tr>
    <tr>
        <td>name</td>
        <td>string</td>
        <td>person name</td>
    </tr>
</table>
    <h3>Example 1:</h3>

<pre><code>
params = {
    'id': 66
}

r = requests.get('http://domain/api/pre_invoices/search', params=params)
</code></pre>
<h3>Example 2:</h3>
<pre><code>
params = {
    'name': 'kaveh mehrbanian'
}

r = requests.get('http://domain/api/pre_invoices/search', params=params)
</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">7- Listing PreInvoice Items:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/pre_invoices/{id}/items</td>
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
<pre><code>r = requests.get('http://domain/api/pre_invoices/66/items')</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">8- Adding A New Item To PreInvoices:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>POST</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/pre_invoices/{id}/items</td>
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
    'price': 1000,
    'quantity1': 0,
    'quantity2': 2,
    'discount': 0,
    'discount_percent': 0.0,
    'discount_per_item': 0,
    'info': 'some info about new item',
    'product': 20,
    'repository': 2,
    'price_level': 1
}

r = requests.post('http://domain/api/pre_invoices/66/items', json=data)
</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">9- Retrieving A PreInvoice Item: </h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td> /api/pre_invoices/{invoice_id}/items/{item_id}</td>
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
<pre><code>r = requests.get('http://domain/api/pre_invoices/66/items/6')</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">10- Updating A PreInvoice Item:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>PUT</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td> /api/pre_invoices/{invoice_id}/items/{item_id}</td>
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
    'price': 2000,
    'quantity2': 13,
    'info': 'some info about updated item'
}

r = requests.put('http://domain/api/pre_invoices/66/items/6', json=data)
</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">11- Deleting A PreInvoice Item:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>DELETE</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td> /api/pre_invoices/{invoice_id}/items/{item_id}</td>
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
<pre><code>r = requests.delete('http://domain/api/pre_invoices/66/items/6')</code></pre>
</div></div>