<script>
  // import * as d3 from "d3";
  // import { onMount } from "svelte";

  const colorFemenino = "#FE88D4";
  const colorMasculino = "#01CFFF";
  const colorOtro = "#FF9900";

  const colorCerca = "#52FF00";
  const colorMedio = "#FFD600";
  const colorLejos = "#FF0000";

  const persons = [
    {
      "Nombre Completo": "Tomás Gallo",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Tucumán, Yerba Buena",
      "Lugar de residencia actual": "Belgrano",
      "Distancia": "#FF0000",
    },
    {
      "Nombre Completo": "Tomas Curzio",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Buenos Aires, Zarate",
      "Lugar de residencia actual": "Palermo",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Iara Guglielmetti",
      Genero: "#FE88D4",
      "Lugar de nacimiento": "Buenos Aires, Tandil",
      "Lugar de residencia actual": "Nuñez",
      "Distancia": "#FFD600",
    },
    {
      "Nombre Completo": "Mariano Sanson",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Tucuman, Yerba Buena",
      "Lugar de residencia actual": "Belgrano",
      "Distancia": "#FF0000",
    },
    {
      "Nombre Completo": "Nicolas Wolodrasky",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Buenos Aires, Tigre",
      "Lugar de residencia actual": "Pacheco",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Carlos Ignacio Araujo",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Santa Fe, Rosario",
      "Lugar de residencia actual": "Chacarita",
      "Distancia": "#FFD600",
    },
    {
      "Nombre Completo": "Jaime Amigo",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Buenos Aires, CABA",
      "Lugar de residencia actual": "San Fernando",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Ivan Mondrzak",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Buenos Aires, CABA",
      "Lugar de residencia actual": "Palermo",
      "Distancia": 5,
    },
    {
      "Nombre Completo": "Federico Peitti",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Buenos Aires, CABA",
      "Lugar de residencia actual": "Coghlan",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Benjamin Toledo",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Corrientes, Corrientes",
      "Lugar de residencia actual": "Colegiales",
      "Distancia": "#FF0000",
    },
    {
      "Nombre Completo": "Mariana Zunino",
      Genero: "#FE88D4",
      "Lugar de nacimiento": "Buenos Aires, Mercedes",
      "Lugar de residencia actual": "Belgrano",
      "Distancia": "#FFD600",
    },
    {
      "Nombre Completo": "Emiliana Verdun",
      Genero: "#FF9900",
      "Lugar de nacimiento": "Mendoza, Godoy Cruz",
      "Lugar de residencia actual": "Recoleta",
      "Distancia": "#FF0000",
    },
    {
      "Nombre Completo": "Ezequiel grinblat",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Buenos Aires, Vicente López",
      "Lugar de residencia actual": "Vicente López",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Manuel Milde",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Misiones, Oberá",
      "Lugar de residencia actual": "Recoleta",
      "Distancia": "#FF0000",
    },
    {
      "Nombre Completo": "Felipe caracoix",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Buenos Aires, Tandil",
      "Lugar de residencia actual": "Recoleta",
      "Distancia": "#FFD600",
    },
    {
      "Nombre Completo": "Estanislao Rios Zgaib",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Rio Negro, Gral Roca",
      "Lugar de residencia actual": "Belgrano",
      "Distancia": "#FF0000",
    },
    {
      "Nombre Completo": "Maria Gimenez Costa",
      Genero: "#FE88D4",
      "Lugar de nacimiento": "Buenos Aires,",
      "Lugar de residencia actual": "Palermo",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Serena Marelli",
      Genero: "#FE88D4",
      "Lugar de nacimiento": "Buenos Aires, Haedo",
      "Lugar de residencia actual": "Haedo",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Valentina Vitetta",
      Genero: "#FE88D4",
      "Lugar de nacimiento": "Buenos Aires, CABA",
      "Lugar de residencia actual": "Versalles",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Joaquin Schanz",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Santa Fe, Rafaela",
      "Lugar de residencia actual": "Villa Urquiza",
      "Distancia": "#FFD600",
    },
    {
      "Nombre Completo": "Franco Setti",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Neuquén, Neuquén",
      "Lugar de residencia actual": "Recoleta",
      "Distancia": "#FF0000",
    },
    {
      "Nombre Completo": "Juana Copello",
      Genero: "#FE88D4",
      "Lugar de nacimiento": "Buenos Aires, Recoleta",
      "Lugar de residencia actual": "San Isidro",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Caterina Villegas",
      Genero: "#FE88D4",
      "Lugar de nacimiento": "Buenos Aires, Vicente López",
      "Lugar de residencia actual": "Olivos",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Camilo Suarez",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "San Juan, San Juan",
      "Lugar de residencia actual": "Belgrano",
      "Distancia": "#FF0000",
    },
    {
      "Nombre Completo": "Valentina Gayo",
      Genero: "#FE88D4",
      "Lugar de nacimiento": "Buenos Aires, CABA",
      "Lugar de residencia actual": "Palermo",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Isabel Nuñez",
      Genero: "#FE88D4",
      "Lugar de nacimiento": "Buenos Aires, Palermo",
      "Lugar de residencia actual": "Vicente Lopez",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Tomas Ward",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Buenos Aires, Tigre",
      "Lugar de residencia actual": "Rincon de Milberg",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Camila Cauzzo",
      Genero: "#FE88D4",
      "Lugar de nacimiento": "Buenos Aires, capital federal",
      "Lugar de residencia actual": "Villa Urquiza",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Catalina Dolhare",
      Genero: "#FE88D4",
      "Lugar de nacimiento": "Buenos Aires, CABA",
      "Lugar de residencia actual": "Belgrano",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Tadeo Yapoudjian",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "CABA",
      "Lugar de residencia actual": "Nuñez",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Guido David Salem",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "CABA",
      "Lugar de residencia actual": "Palermo",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Lara Barijhoff",
      Genero: "#FE88D4",
      "Lugar de nacimiento": "CABA",
      "Lugar de residencia actual": "Recoleta",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Lucas Brea",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Sao Paulo, Brasil",
      "Lugar de residencia actual": "Palermo",
      "Distancia": "#FF0000",
    },
    {
      "Nombre Completo": "Nazaret Seranusoglu",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Ciudad Autonoma de Buenos Aires",
      "Lugar de residencia actual": "Palermo",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Gonzalo Garcia Vence",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "Buenos Aires, Capital Federal",
      "Lugar de residencia actual": "Flores",
      "Distancia": "#52FF00",
    },
    {
      "Nombre Completo": "Juan Ignacio Castore",
      Genero: "#01CFFF",
      "Lugar de nacimiento": "San Juan, San Juan",
      "Lugar de residencia actual": "Recoleta",
      "Distancia": "#FF0000",
    },
  ];
  let plinko_adress = "https://proyecto2-wolodarsky-sanson.vercel.app/";

  
  let animate = false;
  let soundEnabled = true; // Variable para controlar si el sonido está activo

  let pelotas = []; // Array donde guardaremos la data
  // let colorGenero = d3 // Escala para genero
  //   .scaleOrdinal()
  //   .domain(["Femenino", "Masculino", "Otro"])
  //   .range(["#FE88D4", "#01CFFF", "#FF9900"]);

  // let Borde = d3
  //   .scaleOrdinal()
  //   .domain(["Cerca", "Medio", "Lejos"]) // Define el rango completo de valores posibles
  //   .range(["#29DD0B", "#FFD600", "#FF0000"]); // Define los colores correspondientes a cada intervalo

  // onMount(() => {
  //   animate = true;
  //   d3.csv("public/ENCUESTA.csv").then((data) => {
  //     console.log(data); // Verifica si los datos se están cargando correctamente
  //     // Mapear los datos del CSV para agregar los atributos necesarios a cada pelota
  //     pelotas = data.map((d) => ({
  //       nombreCompleto: d["Nombre"],
  //       genero: d.Genero,
  //       lugarNacimiento: d["LugarDeNacimiento"],
  //       color: colorGenero(d.Genero), // Asignar el color correspondiente al género
  //       borde: Borde(d["Distancia"]),
  //     }));
  //   });

  //   // Obtener el elemento de audio
  //   const neonSound = document.getElementById("Neon_Sound");

  //   // Reproducir el sonido al cargar la página
  //   neonSound.play();

  //   // Temporizador para detener el sonido después de 5 segundos
  //   setTimeout(() => {
  //     neonSound.pause();
  //   }, 5000);
  // });
</script>

<main>
  <section class="first_section">
    <div class="titulos">
      <audio
        id="Neon_Sound"
        src="public\sounds\Neon_Sound_Effect.mp3"
        autoplay
        loop
      ></audio>
      <div class="title">
        <h1 class:animate>
          <span>D</span>
          <span>E</span>

          <span class="invisible_char">x</span>

          <span>C</span>
          <span>A</span>
          <span>S</span>
          <span>A</span>

          <span class="invisible_char">x</span>

          <span>A</span>

          <span class="invisible_char">x</span>

          <span>L</span>
          <span>A</span>

          <span class="invisible_char">x</span>

          <span>F</span>
          <span>A</span>
          <span>C</span>
          <span>U</span>
          <span>L</span>
          <span>T</span>
          <span>A</span>
          <span>D</span>
        </h1>
      </div>
    </div>

    <h1 class="subtitle">
      UNA VISUALIZACION SOBRE LA URBANIZACION ESTUDIANTIL
    </h1>

    <div class="landing_grid">
      <svg width="235" height="356">
        {#each Array(24) as _, rowIndex}
          {#each Array(16) as _, colIndex}
            {#if rowIndex % 2 === 0}
              <circle
                cx={colIndex * 15 + 5}
                cy={rowIndex * 15 + 5}
                r="5"
                fill={colIndex % 2 === 0 ? "#E0E0E0" : "#1F2229"}
              />
            {:else}
              <circle
                cx={colIndex * 15 + 5}
                cy={rowIndex * 15 + 5}
                r="5"
                fill={colIndex % 2 === 0 ? "#1F2229" : "#E0E0E0"}
              />
            {/if}
          {/each}
        {/each}
      </svg>
    </div>
    <div class="baskets">
      {#each Array(5) as basket}
        <svg
          style="padding: 3px;"
          xmlns="http://www.w3.org/2000/svg"
          width="42"
          height="40"
          viewBox="0 0 42 40"
          fill="none"
        >
          <mask id="path-1-inside-1_139_1461" fill="white">
            <path
              d="M0 0H41.8391V19.0805C41.8391 30.634 32.4731 40 20.9195 40V40C9.36599 40 0 30.634 0 19.0805V0Z"
            />
          </mask>
          <path
            d="M0 0H41.8391H0ZM44.8391 19.0805C44.8391 32.2909 34.1299 43 20.9195 43C7.70914 43 -3 32.2909 -3 19.0805H3C3 28.9771 11.0229 37 20.9195 37C30.8162 37 38.8391 28.9771 38.8391 19.0805H44.8391ZM20.9195 43C7.70914 43 -3 32.2909 -3 19.0805V0H3V19.0805C3 28.9771 11.0229 37 20.9195 37V43ZM44.8391 0V19.0805C44.8391 32.2909 34.1299 43 20.9195 43V37C30.8162 37 38.8391 28.9771 38.8391 19.0805V0H44.8391Z"
            fill="#E0E0E0"
            mask="url(#path-1-inside-1_139_1461)"
          />
        </svg>
      {/each}
    </div>
  </section>

  <section class="second_section">
    <hr id="division" />
    <h1 style="margin: 2%; margin-bottom:3%">LEYENDA</h1>

    <div class="VisReference">
      <div class="first_column">
        <div class="GenderVis">
          <div class="circle_container">
            <div class="circle-color">
              <svg width="40" height="40">
                <circle cx="20" cy="20" r="20" fill={colorFemenino}>
                </circle></svg
              >
              <h4 style="color: {colorFemenino};">FEMENINO</h4>
            </div>

            <div class="circle-color">
              <svg width="40" height="40">
                <circle cx="20" cy="20" r="20" fill={colorMasculino}>
                </circle></svg
              >
              <h4 style="color: {colorMasculino};">MASCULINO</h4>
            </div>

            <div class="circle-color">
              <svg width="40" height="40">
                <circle cx="20" cy="20" r="20" fill={colorOtro}> </circle></svg
              >
              <h4 style="color: {colorOtro};">OTRO</h4>
            </div>
          </div>
        </div>

        <div class="InfoVis">
          <div class="hover_container">
            <svg class="svg_hover" width="50" height="50">
              <circle id="gradient_circle" cx="20" cy="20" r="20"> </circle>
              <path
                id="arrow"
                d="M2 1.99988L23.7222 8.38877L17.3333 13.4999L25 21.1665L21.1667 24.9999L13.5 17.3332L8.38889 23.7221L2 1.99988Z"
                fill="#E0E0E0"
                stroke="#15161A"
                stroke-width="2"
              />
            </svg>

            <div class="hovered_items">
              <div class="line_container">
                <hr id="hover_line" />
              </div>
              <p id="example_name">Nicolas Wolodarsky - Buenos Aires</p>
            </div>
          </div>
        </div>
      </div>

      <div class="second_column">
        <hr class="DistanceScale" style="order: 2;" />

        <div class="DistanceReferenceText" style="order: 1;">
          <p class="DistanceText">ROJO: MAS DE 800 KM</p>
          <p class="DistanceText">AMARILLO: ENTRE 400KM Y 800KM</p>
          <p class="DistanceText">VERDE: MENOS DE 400KM</p>
        </div>

        <div class="DistanceVis" style="order: 3;">
          <div class="landing_grid" style="padding-top: 0">
            <svg width="235" height="356">
              {#each Array(24) as _, rowIndex}
                {#each Array(16) as _, colIndex}
                  {#if rowIndex % 2 === 0}
                    <circle
                      cx={colIndex * 15 + 5}
                      cy={rowIndex * 15 + 5}
                      r="5"
                      fill={colIndex % 2 === 0 ? "#E0E0E0" : "#15161a"}
                    />
                  {:else}
                    <circle
                      cx={colIndex * 15 + 5}
                      cy={rowIndex * 15 + 5}
                      r="5"
                      fill={colIndex % 2 === 0 ? "#15161a" : "#E0E0E0"}
                    />
                  {/if}
                {/each}
              {/each}
            </svg>
          </div>
          <div class="baskets">
            {#each Array(5) as basket}
              <svg
                style="padding: 3px;"
                xmlns="http://www.w3.org/2000/svg"
                width="42"
                height="40"
                viewBox="0 0 42 40"
                fill="none"
              >
                <mask id="path-1-inside-1_139_1461" fill="white">
                  <path
                    d="M0 0H41.8391V19.0805C41.8391 30.634 32.4731 40 20.9195 40V40C9.36599 40 0 30.634 0 19.0805V0Z"
                  />
                </mask>
                <path
                  d="M0 0H41.8391H0ZM44.8391 19.0805C44.8391 32.2909 34.1299 43 20.9195 43C7.70914 43 -3 32.2909 -3 19.0805H3C3 28.9771 11.0229 37 20.9195 37C30.8162 37 38.8391 28.9771 38.8391 19.0805H44.8391ZM20.9195 43C7.70914 43 -3 32.2909 -3 19.0805V0H3V19.0805C3 28.9771 11.0229 37 20.9195 37V43ZM44.8391 0V19.0805C44.8391 32.2909 34.1299 43 20.9195 43V37C30.8162 37 38.8391 28.9771 38.8391 19.0805V0H44.8391Z"
                  fill="#E0E0E0"
                  mask="url(#path-1-inside-1_139_1461)"
                />
              </svg>
            {/each}
          </div>
        </div>
      </div>
    </div>

    <div class="circle_container" id="BorderReference">
      <div class="circle-color">
        <svg width="50" height="50">
          <circle
            cx="25"
            cy="25"
            r="20"
            fill="#e0e0e0"
            style="stroke: #FF0000; stroke-width: 3px;"
          >
          </circle></svg
        >
      </div>

      <div class="circle-color">
        <svg width="50" height="50">
          <circle
            cx="25"
            cy="25"
            r="20"
            fill="#e0e0e0"
            style="stroke: #FFD600; stroke-width: 3px;"
          >
          </circle></svg
        >
      </div>

      <div class="circle-color">
        <svg width="50" height="50">
          <circle
            cx="25"
            cy="25"
            r="20"
            fill="#e0e0e0"
            style="stroke: #29DD0B; stroke-width: 3px;"
          >
          </circle></svg
        >
      </div>
    </div>
  </section>

  <section class="third_section">
    <hr id="division" />
    <h1 id="PinkText">NUESTROS PROTAGONISTAS</h1>

    <div class="ParticleVis">
      {#each persons as persona}
        <div class="PersonVis">
          <div class="BallContainer">
            <svg width="50" height="50">
              <circle
                cx="25"
                cy="25"
                r="20"
                fill={persona.Genero}
                stroke={persona.Distancia}
                stroke-width="5px"
              >
              </circle></svg
            >
          </div>

          <div>
            <p class="Names" style="color: #e0e0e0;">
              {persona["Nombre Completo"]}
            </p>
          </div>
        </div>
      {/each}
    </div>
  </section>

  <section class="fourth_section">
    <hr id="division"/>
    <h1 style="margin: 2%;">RESULTADO FINAL</h1>
      <iframe
      src={plinko_adress}
      height="85%"
      width="50%"
      title="Prueba1"
      class="plinko_iframe"
      frameborder=0
    ></iframe>
  </section>
</main>

<style>
  :root {
    --BluePinkGradient: linear-gradient(to right, #01cfff, #fe88d4);
    --TrafficLightGradient: linear-gradient(
      to bottom,
      #29dd0b,
      #ffd600,
      #ff0000
    );
  }

  * {
    font-family: "Nunito";
  }

  section {
    height: 100vh;
    scroll-snap-align: start;
  }

  .first_section{
    background-color: #1f2229;
  }

  .titulos {
    display: flex;
    justify-content: center;
  }

  .invisible_char {
    visibility: hidden;
  }

  .title {
    margin-top: 50px;
    display: flex;
    justify-content: center;
    transform: skewY(-3.5deg);
    border: 4px solid #ffffff;
    padding: 20px 50px;
    border-radius: 10px;
    box-shadow:
      0 0 10px #01cfff,
      0 0 10px #fe88d4,
      inset 0 0 10px #fe88d4,
      inset 0 0 10px #fe88d4;
    animation: animate 1s linear infinite;
  }

  .subtitle {
    display: flex;
    justify-content: center;
    font-size: 18px;
    transform: skewY(-3.5deg);
    text-shadow:
      0 0 10px #01cfff,
      0 0 20px #fe88d4;
  }

  .landing_grid {
    display: flex;
    justify-content: center;
    padding-top: 20px;
    padding-bottom: 10px;
    /* border: 2px dotted lightblue; */
  }

  .baskets {
    display: flex;
    flex-direction: row;
    justify-content: center;
  }

  #division {
    height: 10px;
    background: var(--BluePinkGradient);
    border-width: 0;
    margin: 0;
  }

  .second_section {
    background-color: #1f2229;
  }

  .GenderVis {
    margin-bottom: 3%;
    /* border: 2px dotted green; */
  }

  .VisReference {
    display: flex;
    flex-direction: row;
    gap: 25%;
    /* border: 2px dotted red; */
    margin-left: 2%;
  }

  .second_column {
    display: flex;
    flex-direction: row;
    gap: 60px;
  }

  .second_column .DistanceReferenceText {
    align-self: center; /* Alinear este elemento verticalmente */
  }

  .circle_container {
    display: flex;
    flex-direction: row;
    padding-bottom: 20px;
  }

  .circle-color {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-right: 50px;
  }

  .hover_container {
    display: inline-block;
    position: relative;
    margin-left: 5%;
    justify-content: flex-start;
    align-items: center;
  }

  #arrow {
    position: absolute;
    bottom: 0;
    right: 0;
    transform: translate(52%, 52%);
  }

  .DistanceScale {
    transform: rotate(180deg);
    background-image: var(
      --TrafficLightGradient
    ); /* No sabemos por que esto funciona**/
    width: 10px;
    margin: 0;
    height: 85%;
    border: none;
  }

  .DistanceReferenceText {
    color: #e0e0e0;
    background-color: rgba(224, 224, 224, 0.1);
    border-width: 2px;
    border-style: solid;
    border-image: var(--BluePinkGradient);
    border-image-slice: 1;
    visibility: hidden;
    transform: translateY(-20px);
    transition:
      opacity 0.5s ease-out,
      transform 0.5s ease-out;
  }

  .DistanceText {
    margin: 10%;
  }

  .DistanceScale:hover + .DistanceReferenceText {
    visibility: visible;
    transform: translateY(0);
  }

  .svg_hover {
    margin-right: 40px;
  }

  #gradient_circle {
    fill: #e0e0e0;
  }

  .hovered_items {
    display: flex;
    justify-content: flex-start;
    visibility: visible;
    opacity: 0;
    position: absolute;
    top: 0%;
    left: 80%;
    transform: translateY(-50%);
    padding: 10px;
    white-space: nowrap;
  }

  .line_container {
    display: flex;
    align-items: center;
  }

  #hover_line {
    color: #e0e0e0;
    width: 250px;
    margin-right: 40px;
  }

  #example_name {
    color: #e0e0e0;
    font-size: 18px;
    margin: 0;
  }

  .svg_hover:hover + .hovered_items {
    opacity: 1;
    transform: translateX(0);
    transition:
      opacity 0.5s ease-out,
      transform 0.5s ease-out;
  }

  #BorderReference {
    padding-top: 20px;
    position: absolute;
    right: 0;
    padding-right: 46px;
  }

  .third_section {
    background-color: #1f2229;
  }

  #PinkText {
    text-shadow:
      0 0 10px #fe88d4,
      0 0 20px #fe88d4;
    margin: 2%;
  }

  .ParticleVis {
    display: grid;
    grid-template-columns: repeat(
      auto-fit,
      minmax(100px, 1fr)
    ); /* Ajusta el ancho de las columnas */
    grid-gap: 20px; /* Espacio entre elementos */
  }

  .PersonVis {
    text-align: center; /* Alinea el contenido al centro */
  }

  .BallContainer {
    display: flex;
    justify-content: center; /* Centra horizontalmente */
    align-items: center; /* Centra verticalmente */
  }

  .Names {
    text-align: center; /* Alinea el texto al centro */
  }

  .fourth_section {
    background-color: #1f2229;
  }

  .plinko_iframe{
    margin-left: 2%;
    align-self: center;
    justify-self: center;
  }

  /* Estilos de la animacion */
  .title:before {
    content: "";
    left: 0%;
    height: 0px;
    background: #ffffff;
    box-shadow:
      0 0 10px #01cfff,
      0 0 10px #fe88d4;
  }

  .title:after {
    background: #ffffff;
    box-shadow:
      0 0 10px #01cfff,
      0 0 10px #fe88d4;
  }

  h1 {
    font-size: 28px;
    color: #ffffff;
    text-shadow:
      0 0 10px #01cfff,
      0 0 20px #fe88d4;
  }

  h1 span {
    animation: animate 0.5s linear infinite;
  }

  h1 span:nth-child(1) {
    animation-delay: 0.25s;
  }

  h1 span:nth-child(2) {
    animation-delay: 0.2s;
  }

  h1 span:nth-child(3) {
    animation-delay: 0.35s;
  }

  @keyframes animate {
    0% {
      opacity: 1;
    }
    30% {
      opacity: 1;
    }
    40% {
      opacity: 0.5;
    }
    50% {
      opacity: 1;
    }
    100% {
      opacity: 1;
    }
  }
</style>
