<h1 style="background-color:Gainsboro;">User Table</h1><div style="margin-left:20px;"> 
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
        <td>string(150)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>last_name</td>
        <td>string(150)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>email</td>
        <td>string(150)</td>
        <td></td>
        <td>✗</td>
    </tr>
    <tr>
        <td>username</td>
        <td>string(150)</td>
        <td></td>
        <td>✓</td>
    </tr>
    <tr>
        <td>password</td>
        <td>string(150)</td>
        <td>write_only</td>
        <td>✓</td>
    </tr>
    <tr>
        <td>person</td>
        <td>int</td>
        <td>Person mid, read_only</td>
        <td>✗</td>
    </tr>
</table>

</div>


<div><h1 style="background-color:Gainsboro;">1- Signing Up A User</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>POST</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/users/signup</td>
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
    'username': 'kavehkm',
    'password': 's3cret',
    'email': 'mehrbaniankaveh@gmail.com'
}

r = requests.post('http://domain/api/users/signup', json=data)</code></pre>
</div>
</div>



<div><h1 style="background-color:Gainsboro;">2- User SignIn</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>POST</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/users/signin</td>
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
    'username': 'kavehkm',
    'password': 's3cret'
}

r = requests.post('http://domain/api/users/signin', json=data)</code></pre>

<h3>Sample Result:</h3>

<pre><code>
print(r.json())
{
    "id": 14,
    "first_name": "kaveh",
    "last_name": "mehrbanian",
    "email": "mehrbaniankaveh@gmail.com",
    "username": "kavehkm",
    "person": 66,
    "groups": [],
    "permissions": [],
    "token": "b51297429d9d107a57488c1fa91d6c306e898729"
}
</code></pre>

<h3>Authorization:</h3>

<pre><code>
headers = {
    'Authorization': 'Token b51297429d9d107a57488c1fa91d6c306e898729'
}

r = requests.get/post/put/delete('endpoint', headers=headers, json=data, params=params)</code></pre>
</div>
</div>





<div><h1 style="background-color:Gainsboro;">3- Listing Users</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/users</td>
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
<pre><code>r = requests.get('http://domain/api/users')</code></pre>


<h3>Example 2:</h3>
    <pre><code>
params = {
    'limit': 50,
    'offset': 10
}

r = requests.get('http://domain/api/users', params=params)</code></pre>
</div>
</div>


<div><h1 style="background-color:Gainsboro;">4- Retrieving A User</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/users/{id}</td>
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

<pre><code>r = requests.get('http://domain/api/users/66')</code></pre>
</div>
</div>



<div><h1 style="background-color:Gainsboro;">5- Updating A User</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>PUT</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/users/{id}</td>
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
    'first_name': 'kaweh'
}

r = requests.put('http://domain/api/users/66', json=data)</code></pre>
</div>
</div>


<div><h1 style="background-color:Gainsboro;">6- Deleting A  User</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>DELETE</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/users/{id}</td>
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

<pre><code>r = requests.delete('http://domain/api/users/66')</code></pre>
</div>
</div>



<div><h1 style="background-color:Gainsboro;">7- Listing User Permissions</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>GET</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/users/{id}/permissions</td>
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

<pre><code>r = requests.get('http://domain/api/users/66/permissions')</code></pre>
</div>
</div>



<div><h1 style="background-color:Gainsboro;">8- Adding User Permissions</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>PUT</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/users/{id}/permissions</td>
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
    <h3>Example:</h3>

<pre><code>
data = {
    'permissions': [1, 2, 3]
}

r = requests.put('http://domain/api/users/66/permissions', json=data)</code></pre>
</div>
</div>


<div><h1 style="background-color:Gainsboro;">9- Removing User Permissions</h1><div style="margin-left:20px;"> 
<h3>Details:</h3>
    <table>
        <tr>
            <td><strong>Method</strong></td>
            <td>DELETE</td>
        </tr>
        <tr>
            <td><strong>Endpoint</strong></td>
            <td>/api/users/{id}/permissions</td>
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
    <h3>Example:</h3>

<pre><code>
data = {
    'permissions': [2, 3]
}

r = requests.delete('http://domain/api/users/66/permissions', json=data)</code></pre>
</div>
</div>