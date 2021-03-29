<!--
REEMPLAZAR: Buscador-Ajax-similar-a-Google, TITULO, DESCRIPCION, DESCRIPCION2, DEMO, TECNOLOGIAS
-->
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/sergioalegre/Kubernetes">
    <img src="http://sergioalegre.es/logo.JPG" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center"><!-- TITULO -->Kubernetes e IaC</h3>

  <p align="center">
    <!-- DESCRIPCION -->Apuntes de los cursos y practicas de Kubernetes e IaC
    <br />
    <a href="https://github.com/sergioalegre/Kubernetes"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <!-- DEMO<a href="http://sergioalegre.es/Programacion/_BuscadorAJAX/">View Demo</a> -->
    ·
    <a href="https://github.com/sergioalegre/Kubernetes/issues">Report Bug</a>
    ·
    <a href="https://github.com/sergioalegre/Kubernetes/issues">Request Feature</a>
  </p>
</p>

## Kubernetes
<!-- DESCRIPCION2 --> <!-- DEMO -->
Kubernetes es un orquestador de contenedores de Google y es Open Source. Permite manejar aplicaciones dentro de contenedores a traves de varios servidores (físicos o virtuales).
<br />
**Funcionalidades**:
- Manejar muchos contenedores
<br />
- Alta disponibilidad
<br />
- Cero downtime (mediante replicas de la aplicación en diferentes nodos)
<br />
- Escalar aplicación (para absorver mas tráfico)
<br />
- Disaster recovery (ya que se basa en manifiestos declarativos)

<br />
<br />
En cuanto a **arquitectura** hay dos componentes, el Master y los Workers.
<br />
Los workers corren un agente llamado *kubelet*.
<br />
El Master tiene varios servicios:
<br />
- API SERVER: que los clientes interacciónen con el cluster (mediante WEB, API o comandos kubectl)
<br />
- Controller Manager: responsable de lo que pasa en el cluster. Revisa los contenedores que estan corriendo frente a los contenedores que deberian estar corriendo.
<br />
- Scheduler: recibe ordenes del Controller Manager responsable de mover pods entre Workers
<br />
- etcd: base de datos del estado y configuraciones.

<br />
<br />
**Pods**:
<br />
- Set de contenedores con una sola IP (comparten el namespace de red).
<br />
- Son volatiles: cuando actualizas el aplicativo se destruye el antiguo y crea uno nuevo. Por ello no hay que llamar a la IP del pod, hay que llamar a la IP del servicio.
<br />
- Overlay network: red de comunicacion entre pods de diferentes workers (para trabajar juntos)

<br />
<br />
**Servicios**:

<p align="center">
  <a href="https://github.com/sergioalegre/Kubernetes">
    <img src="http://sergioalegre.es/Programacion/_BuscadorAJAX/captura.PNG" alt="Logo" width="360" height="">
  </a>
</p>

## Contact
Email: sergio.alegre.arribas EN gmail.com
<br>
LinkedIn: https://www.linkedin.com/in/sergioalegre
<br>
My certificates: http://certificates.sergioalegre.es
<br>
Website: http://me.sergioalegre.es

### Built With
<!-- TECNOLOGIAS -->
* [kubernetes](kubernetes)
* [kubectl](kubectl)
* [minikube](minikube)
* [Azure-AKS](Azure-AKS)
* [Amazon-EKS](Amazon-EKS)
* [k3s](k3s)

## Getting Started
---

### Prerequisites
---

### Installation
---

## Usage
---

## Roadmap
---

## Contributing
Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License
Distributed under the MIT License. See `LICENSE` for more information.


[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/sergioalegre
