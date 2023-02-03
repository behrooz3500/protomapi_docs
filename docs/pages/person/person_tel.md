<h1 style="background-color:Gainsboro;">PersonTel Table</h1><div style="margin-left:20px;">
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
    <tr>
        <td>person</td>
        <td>int</td>
        <td>person mid</td>
        <td>✓</td>
    </tr>
</table>
</div>


<div>
<h1 style="background-color:Gainsboro;">1- Create A PersonTel</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>POST</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/person_tels</td>
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
    'tel': '123456789',
    'caption': 'mobile',
    'person': 100
}

r = requests.post('http://domain/api/person_tels', json=data)
</code></pre>
</div></div>



<div>
<h1 style="background-color:Gainsboro;">2- Listing PersonTels</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/person_tels</td>
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
</table>
<h5>Example 1:</h5>
<pre><code>r = requests.get('http://domain/api/person_tels')</code></pre>

<h5>Example 2:</h5>
<pre><code>
params = {
    'limit': 50,
    'offset': 10
}

r = requests.get('http://domain/api/person_tels', params=params)
</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">3- Retrieving PersonTel</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/person_tels/{mid}</td>
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
<h5>Example:</h5>
<pre><code>r = requests.get('http://domain/api/person_tels/66')</code></pre>
</div>
</div>

<div>
<h1 style="background-color:Gainsboro;">4- Updating PersonTel</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>PUT</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/person_tels/{mid}</td>
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
<h5>Example:</h5>
<pre><code>
data = {
    'tel': '0987654321'
}

r = requests.put('http://domain/api/person_tels/66', json=data)
</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">5- Deleting PersonTel</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>DELETE</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/person_tels/{mid}</td>
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
<h5>Example:</h5>
<pre><code>r = requests.delete('http://domain/api/person_tels/66')</code></pre>
</div></div>