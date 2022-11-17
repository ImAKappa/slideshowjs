<script lang="ts">
  import { onMount } from 'svelte';

  onMount(() => {
    const pathHead = document.querySelector('.path-head');
    console.log(pathHead.getTotalLength()); 

    const pathBody = document.querySelector('.path-body');
    console.log(pathBody.getTotalLength());
  })

</script>


<!-- Created with Inkscape (http://www.inkscape.org/) -->
<svg id="svg9274" viewBox="0 0 259.3 435.88" version="1.1">
  <g id="layer1" transform="translate(-169.77 -382.33)">
    <g id="g9357" transform="translate(-256.58 42.426)">
      <!-- Head -->
      <path class="path-head" stroke="#ffffff" stroke-width="3" id="path9347" style="fill:#000000" d="m315.67 347.53c0 20.503-16.621 37.123-37.123 37.123-20.503 0-37.123-16.621-37.123-37.123 0-20.503 16.621-37.123 37.123-37.123 20.503 0 37.123 16.621 37.123 37.123z" transform="translate(294.11 29.495)" />
      <!-- Body -->
      <path class="path-body" stroke="#ffffff" stroke-width="3" id="path9349" d="m516.35 490.41s-30.339 157.53-36.871 168.19c-5.5865 9.1154-49.18 80.642-49.18 80.642-9.3065 15.26-0.48739 26.17 9.3724 31.862 8.3938 4.8456 26.437 3.6458 32.403-6.5301 0 0 48.366-75.267 53.643-91.5 3.6534-11.238 12.143-57.857 12.143-57.857s46.996 48.47 52.143 57.143c6.4876 10.933 18.571 87.143 18.571 87.143 2.8898 13.56 15.822 17.982 29.286 15.714 10.633-1.7908 21.753-8.9851 19.286-22.143 0 0-10.746-88.36-19.286-102.86-10.191-17.302-65-76.429-65-76.429l15.714-70s10.086 20.446 17.143 29.286c8.0255 10.053 58.571 39.286 58.571 39.286 4.6363 3.1097 15.133 1.3962 19.286-6.4286 3.3332-6.2806 3.1763-16.454-4.2857-21.429 0 0-41.655-26.151-51.429-34.286-10.87-9.03-32.86-69.27-32.86-69.27-6.8208-9.3864-16.151-19.742-32.143-20-16.119-0.26028-24.187 8.6196-31.429 13.571 0 0-61.747 45.105-67.857 54.286-6.1469 9.236-17.143 78.571-17.143 78.571-1.7236 7.9 1.3621 14.253 10.714 16.429 11.443 2.662 19.645-4.4634 20.714-10 0 0 7.0508-54.765 12.143-62.857 5.9288-9.4214 26.346-20.521 26.346-20.521z" style="fill:#000000"/>
    </g>
  </g>
  <metadata>
    <rdf:RDF>
      <cc:Work>
        <dc:format>image/svg+xml</dc:format>
        <dc:type rdf:resource="http://purl.org/dc/dcmitype/StillImage"/>
        <cc:license rdf:resource="http://creativecommons.org/licenses/publicdomain/"/>
        <dc:publisher>
          <cc:Agent rdf:about="http://openclipart.org/">
            <dc:title>Openclipart</dc:title>
          </cc:Agent>
        </dc:publisher>
      </cc:Work>
      <cc:License rdf:about="http://creativecommons.org/licenses/publicdomain/">
        <cc:permits rdf:resource="http://creativecommons.org/ns#Reproduction"/>
        <cc:permits rdf:resource="http://creativecommons.org/ns#Distribution"/>
        <cc:permits rdf:resource="http://creativecommons.org/ns#DerivativeWorks"/>
      </cc:License>
    </rdf:RDF>
  </metadata>
</svg>

<style>
.path-head {
  stroke-dasharray: 233;
  stroke-dashoffset: 233;
  animation: dashhead 5s linear infinite;
}

@keyframes dashhead {
  from {
    stroke-dashoffset: 233;
  }
  to {
    stroke-dashoffset: 0;
  }
}

.path-body {
  stroke-dasharray: 1697;
  stroke-dashoffset: 1697;
  animation: dashbody 5s linear infinite;
}

@keyframes dashbody {
  from {
    stroke-dashoffset: 1697;
  }
  to {
    stroke-dashoffset: 0;
  }
}
</style>