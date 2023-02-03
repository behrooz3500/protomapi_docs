<h1 style="background-color:Gainsboro;">PersonGroup Table</h1><div style="margin-left:20px;">
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
        <td>name</td>
        <td>string(50)</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>parent</td>
        <td>int</td>
        <td>person group mid</td>
        <td>✗</td>
    </tr>
</table>
</div>


<div>
<h1 style="background-color:Gainsboro;">1- Creating A PersonGroup:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>POST</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/person_groups</td>
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
    'name': 'new person group',
    'parent': 500
}

r = requests.post('http://domain/api/person_groups', json=data)
</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">2- Listing PersonGroups:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/person_groups</td>
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
<pre><code>r = requests.get('http://domain/api/person_groups')</code></pre>

<h5>Example 2:</h5>
<pre><code>
params = {
    'limit': 50,
    'offset': 10
}

r = requests.get('http://domain/api/person_groups', params=params)
</code></pre>
</div></div>



<div>
<h1 style="background-color:Gainsboro;">3- Retrieving A PersonGroup</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/person_groups/{mid}</td>
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

<pre><code>r = requests.get('http://domain/api/person_groups/66')</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">4- Updating A PersonGroup</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>PUT</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/person_groups/{mid}</td>
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
}

r = requests.put('http://domain/api/person_groups/66', json=data)
</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;">5- Deleting A PersonGroup</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>DELETE</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/person_groups/{mid}</td>
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

<pre><code>r = requests.delete('http://domain/api/person_groups/66')</code></pre>
</div></div>