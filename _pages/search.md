---
permalink: /search/
title: Search
---

{% capture initSearch %}

<form id="search-form" action="">
  <label class="label" for="search">Search term (accepts a regex):</label>
  <br/>
  <input class="input" id="search" type="text" name="search" 
        autofocus
        placeholder="e.g. Promise"
        autocomplete="off"/>
  <ul class="list  list--results" id="list">
  </ul>
</form>

<script type="text/javascript" src="{{site.baseurl}}assets/src/fetch.js"></script>
<script type="text/javascript" src="{{site.baseurl}}assets/src/search.js"></script>


<script type="text/javascript">
  const data = {
    dataSource: '{{site.url}}{{site.baseurl}}/assets/src/search.json',
    searchField: '#search',
    resultsList: '#list',
    siteURL: '/intro2sd-edwin-plasencia-hernandez-alu0101329888/'
  };
  const search = new JekyllSearch(data);
  search.init();
</script>

<noscript>Please enable JavaScript to use the search form.</noscript>

{% endcapture %}

{{ initSearch | lstrip }}

