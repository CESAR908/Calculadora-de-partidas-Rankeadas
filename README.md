# Calculadora-de-partidas-Rankeadas
# CALCULADORA RANKEADAS

function calcularNivelRankeado(vitórias, derrotas) {
  let saldoVitorias = vitórias - derrotas;
  let nivel;

  if (vitórias < 10) {
    nivel = "Ferro";
  } else if (vitórias >= 11 && vitórias <= 20) {
    nivel = "Bronze";
  } else if (vitórias >= 21 && vitórias <= 50) {
    nivel = "Prata";
  } else if (vitórias >= 51 && vitórias <= 80) {
    nivel = "Ouro";
  } else if (vitórias >= 81 && vitórias <= 90) {
    nivel = "Diamante";
  } else if (vitórias >= 91 && vitórias <= 100) {
    nivel = "Lendário";
  } else if (vitórias >= 101) {
    nivel = "Imortal";
  }

  return {
    saldo: saldoVitorias,
    nivel: nivel
  };
}

let jogador = calcularNivelRankeado(85, 30);
console.log(`O Herói tem de saldo de ${jogador.saldo} está no nível de ${jogador.nivel}`);
