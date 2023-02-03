<h1 style="background-color:Gainsboro;">Log Table</h1><div style="margin-left:20px;">
<table>
    <tr>
        <td><strong>Attribute</strong</td>
        <td><strong>Type</strong</td>
        <td><strong>Description</strong</td>
        <td><strong>Required</strong</td>
    </tr>
    <tr>
        <td>id</td>
        <td>int</td>
        <td>primary_key, read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>action</td>
        <td>int</td>
        <td>
            <ul>
                <li>delete: 1</li>
                <li>insert: 2</li>
                <li>update: 3</li>
            </ul>
        </td>
        <td>✓</td>
    </tr>
    <tr>
        <td>subject</td>
        <td>int</td>
        <td>
            <ul>
                <li>person: 12</li>
                <li>pre_invoice: 100</li>
                <li>invoice: 102</li>
                <li>temp_person: 102</li>
            </ul>
        </td>
        <td>✓</td>
    </tr>
    <tr>
        <td>object_id</td>
        <td>int</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>mid</td>
        <td>int</td>
        <td></td>
        <td>✗</td>
    </tr>
</table>
</div>


<h1 style="background-color:Gainsboro;">LogMeta Table</h1><div style="margin-left:20px;">
<table>
    <tr>
        <td><strong>Attribute</strong</td>
        <td><strong>Type</strong</td>
        <td><strong>Description</strong</td>
        <td><strong>Required</strong</td>
    </tr>
    <tr>
        <td>id</td>
        <td>int</td>
        <td>primary_key, read_only</td>
        <td>✗</td>
    </tr>
    <tr>
        <td>key</td>
        <td>string(255)</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>value</td>
        <td>string(255)</td>
        <td></td>
        <td>✓</td>
    </tr>
</table>
</div>


<div>
<h1 style="background-color:Gainsboro;">1- Listing Logs:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/logs</td>
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
    <h3>Example:</h3>

<pre><code>r = requests.get('http://domain/api/logs')</code></pre>
</div></div>


<div>
<h1 style="background-color:Gainsboro;"> 2- Deleting A Log:</h1><div style="margin-left:20px;">
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>DELETE</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/logs/{id}</td>
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

<pre><code>r = requests.delete('http://domain/api/logs/66')</code></pre>
</div></div>
