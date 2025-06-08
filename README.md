# Main.js.2

window.onload = () => {
  const canvas = document.getElementById("tela");
  const ctx = canvas.getContext("2d");

  // Redimensiona o canvas para ocupar toda a tela
  function ajustarTamanho() {
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight - 60;
  }

  ajustarTamanho();
  window.addEventListener("resize", ajustarTamanho);

  // Exemplo: desenhar um ponto no clique
  canvas.addEventListener("click", (e) => {
    ctx.fillStyle = "red";
    ctx.beginPath();
    ctx.arc(e.offsetX, e.offsetY, 4, 0, 2 * Math.PI);
    ctx.fill();
  });
};
