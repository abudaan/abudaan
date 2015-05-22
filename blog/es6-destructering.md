We want to pass a settings object to the constructor of the Data class.

The settings object:
<pre><code>{
  id: 1,
  name: 'John'
}
</code></pre>




Without destructering:

<pre><code>class Data{
  constructor(settings){
    this.id = settings.id;
    this.name = settings.name;
  }
}
</code></pre>


With destructering:

<pre><code>class Data{
  constructor(settings){
    ({id: this.id, name: this.name} = settings);
  }
}
</code></pre>