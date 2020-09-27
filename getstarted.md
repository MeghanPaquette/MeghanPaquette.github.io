---
layout: page
title: Getting Started
subtitle: Added Per lab
---
<div class="pretty-text">

<h1>{{ page.title }}</h1>
  
{{ content }}
  
</div>



  
  


<style>

.pretty-text {
  margin-top: 100px;
  margin-bottom: 100px;
  padding-left: 30px;
  padding-right: 30px;
  text-align: justify;
}

.pretty-text p {
  line-height: 1.8;
  padding-bottom: 80px;
  }
  
.pretty-text h1 {
  color: darkblue;
  font-size: 40px;
}

.pretty-text h2 {
  color: darkblue;
  font-size: 30px;
  margin-top: 60px;
}

.pretty-text h3 {
  color: darkblue;
}

.pretty-text a {
  color: darkblue;
}
  
.pretty-text img {
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 5px;
  width: 400px;
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

.pretty-text img:hover {
  box-shadow: 0 0 3px 1px rgba(0, 140, 186, 0.5);
}

pre{
  font-family: Consolas, Menlo, Monaco, Lucida Console, Liberation Mono, DejaVu Sans Mono, Bitstream Vera Sans Mono, Courier New, monospace, serif;
  margin-bottom: 10px;
  padding: 5px;
  background-color: #eee;
  width: 750px!ie7;
  padding-bottom: 20px!ie7;
}
  
</style>

---
layout: nice-text
---
  
{{ content }}




<h2> Ireland vs France: Liquid Table Update </h2>

<table id="ire-v-fra">

<thead>
  <tr>
    <th>  <h3>  Ireland  </h3>  </th>
    <th>  <h3>  France  </h3>  </th>
  </tr>
</thead>

<tbody>

<tr>
  
  
  <td>
  
    
    <h4>  Strengths  </h4>
    <ul>
      
      {% for item in page.ireland.strengths %}
         <li>{{ item }}</li>
      {% endfor %}
      
    </ul>
    
    <br>

    <h4>  Weaknessess  </h4>
    <ul>
      
      {% for item in page.ireland.weaknesses %}
         <li>{{ item }}</li>
      {% endfor %}
      
    </ul>  
    
    
  </td>
  


  <td>
  
    <h4>  Strengths  </h4>
    <ul>
      
      {% for item in page.france.strengths %}
        <li>{{ item }}</li>
      {% endfor %}
      
    </ul>
    
    <br>
    
    <h4>  Weaknessess  </h4>
    <ul>
      
      {% for item in page.france.weaknesses %}
         <li>{{ item }}</li>
      {% endfor %}
      
    </ul>

  </td>
</tr> 

</table>


<br>

<hr>

<br>


<blockquote>
<pre>
<code>

    ###
    ###  LAYOUT INHERITANCE
    ###
    ###  pages built by adding elements 
    ###  to other page layouts 
    ###

          default.html layout 
          │
          └── nice-text.html layout 
              │
              └── liquid-table.html layout
                  # see liquid table below



          ###
          ###  default.html layout
          ###

          &lt;html>
          &lt;head>
            &lt;body>                                
              &lt;header>   

              &lbrace;&lbrace; content }}     

              &lt;footer>           
            &lt;/body>  
          &lt;/html>     

          ###
          ###  &lbrace;&lbrace;content}}
          ###  is replaced by
          ###  whatever content
          ###  is on the page that
          ###  uses the default.html 
          ###  template 
          ###



          ###
          ### nice-text.html layout
          ###

          ---
          layout: default
          ---

          &lt;div class="pretty-text">

          &lt;h1> &lbrace;&lbrace; page.title }} &lt;/h1>

          &lbrace;&lbrace; content }}

          &lt;/div>


          ###
          ### liquid-table.html layout
          ###

          ---
          layout: nice-text
          ---

          &lbrace;&lbrace; content }}

          #  liquid table starts here





    ###
    ###  LIQUID TABLE ADDED USING YAML DATA
    ###
    ###  liquid is a simple markup language that allows
    ###  web designers to separate page layouts from
    ###  page content without databases
    ###
    ###  &lbrace;%  function in liquid  %}
    ###  &lbrace;&lbrace;  variable in liquid  }}
    ###

        ###
        ###  YAML HEADER FOR PAGE
        ###

        ---
        layout: liquid-table
        title: 'Ireland or France?'
        Ireland:
          strengths:
          - Hiking and gorgeous green scenery
          - Nice locals
          - Music and entertainment
          weaknesses: 
          - rainy/cloudy weather
          - heavy food
          -  
        France:
          strengths: 
          - Fashion
          - Museums and Art
          - Eifel Tower, Versailles, etc. Lots of places to see. 
          weaknesses: 
          - Pickpockets
          - Not as Nice Locals
          - Lots of Tourists
        ---

       ###
       ###  LIQUID TAG TABLE IN LAYOUT
       ###
       ###  HTML ELEMENTS: 
       ###  &lt;thead> table header
       ###  &lt;tr>  table row 
       ###  &lt;td>  table cell (or data)
       ###  &lt;ul> unordered list
       ###  &lt;li> list item 
       ###

        &lt;h2> Ireland vs. France &lt;/h2>

        &lt;table id="ire-v-fra">

        &lt;thead>
          &lt;tr>
            &lt;th>  &lt;h3>  Ireland  &lt;/h3>  &lt;/th>
            &lt;th>  &lt;h3>  France  &lt;/h3>  &lt;/th>
          &lt;/tr>
        &lt;/thead>

        &lt;tbody>
        &lt;tr>
          &lt;td>
            &lt;h4>  Strengths  &lt;/h4>
            &lt;ul>

              ###  LIQUID LOOPS WITH YAML DATA
              ###  Ireland:
              ###    strengths:
              ###    - Hiking and gorgeous green scenery
              ###    - Nice locals
              ###    - Music and entertainment

              &lbrace;% for item in page.Ireland.strengths %}
                 &lt;li>  &lbrace;&lbrace; item }}  &lt;/li>
              &lbrace;% endfor %}

              ###    LIQUID LOOP CREATES HTML CODES:
              ###    &lt;li> Hiking and gorgeous green scenery &lt;/li>
              ###    &lt;li> Nice locals &lt;/li>
              ###    &lt;li> Music and entertainment &lt;/li>        

            &lt;/ul>
            &lt;br>
            &lt;h4>  Weaknessess  &lt;/h4>
            &lt;ul>

              &lbrace;% for item in page.Ireland.weaknesses %}
                 &lt;li>  &lbrace;&lbrace; item }}  &lt;/li>
              &lbrace;% endfor %}

            &lt;/ul>  
          &lt;/td>
          &lt;td>
            &lt;h4>  Strengths  &lt;/h4>
            &lt;ul>

              &lbrace;% for item in page.france.strengths %}
                &lt;li>  &lbrace;&lbrace; item }}  &lt;/li>
              &lbrace;% endfor %}

            &lt;/ul>
            &lt;br>
            &lt;h4>  Weaknessess  &lt;/h4>
            &lt;ul>

              &lbrace;% for item in page.france.weaknesses %}
                 &lt;li>  &lbrace;&lbrace; item }}  &lt;/li>
              &lbrace;% endfor %}

            &lt;/ul>
          &lt;/td>
        &lt;/tr> 
        &lt;/table>

</code>
</pre>
</blockquote>





<style>
  pre{
  font-family: Consolas, Menlo, Monaco, Lucida Console, Liberation Mono, DejaVu Sans Mono, Bitstream Vera Sans Mono, Courier New, monospace, serif;
  margin-bottom: 10px;
  padding: 5px;
  background-color: #eee;
  width: 750px!ie7;
  padding-bottom: 20px!ie7;
}

ui {
  padding-inline-start: 10px;
  }
  
table {
  margin-left: 20px;
  }
  
</style>
