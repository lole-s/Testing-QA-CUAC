<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 600">
  <style>
    .node {
      fill: #f1f1f1;
      stroke: #ccc;
      stroke-width: 2px;
      rx: 10px;
    }
    .edge {
      stroke: #666;
      stroke-width: 2px;
      marker-end: url(#arrowhead);
    }
    .arrowhead {
      fill: #666;
    }
    text {
      font-family: Arial, sans-serif;
      font-size: 14px;
      fill: #333;
    }
  </style>
  <defs>
    <marker id="arrowhead" markerWidth="10" markerHeight="7" refX="9" refY="3.5" orient="auto">
      <path d="M0,0 L0,7 L9,3.5 z" class="arrowhead" />
    </marker>
  </defs>
  <g transform="translate(50, 50)">
    <rect x="0" y="0" width="700" height="500" class="node" />
    <text x="350" y="30" text-anchor="middle">Ciclo de Vida del Desarrollo de Software</text>

    <g transform="translate(50, 100)">
      <rect x="0" y="0" width="150" height="80" class="node" />
      <text x="75" y="40" text-anchor="middle">Análisis de Requisitos</text>
    </g>
    <g transform="translate(250, 100)">
      <rect x="0" y="0" width="150" height="80" class="node" />
      <text x="75" y="40" text-anchor="middle">Diseño</text>
    </g>
    <g transform="translate(450, 100)">
      <rect x="0" y="0" width="150" height="80" class="node" />
      <text x="75" y="40" text-anchor="middle">Implementación</text>
    </g>
    <g transform="translate(150, 250)">
      <rect x="0" y="0" width="150" height="80" class="node" />
      <text x="75" y="40" text-anchor="middle">Pruebas</text>
    </g>
    <g transform="translate(350, 250)">
      <rect x="0" y="0" width="150" height="80" class="node" />
      <text x="75" y="40" text-anchor="middle">Despliegue</text>
    </g>
    <g transform="translate(550, 250)">
      <rect x="0" y="0" width="150" height="80" class="node" />
      <text x="75" y="40" text-anchor="middle">Mantenimiento</text>
    </g>

    <path d="M125,180 L125,250" class="edge" />
    <path d="M325,180 L325,250" class="edge" />
    <path d="M525,180 L525,250" class="edge" />
    <path d="M225,130 L225,180" class="edge" />
    <path d="M425,130 L425,180" class="edge" />
    <path d="M625,130 L625,180" class="edge" />
  </g>
</svg>