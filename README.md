# contador-de-cliques
import React, { useState } from 'react';

// Componente Funcional Contador
const Contador = () => {
  // Definição do estado: 'count' é o valor, 'setCount' é a função que o altera
  const [count, setCount] = useState(0);

  // Função disparada pelo evento de clique
  const incrementarContador = () => {
    // Atualiza o estado somando 1 ao valor atual
    setCount(count + 1);
  };

  return (
    <div style={estilos.container}>
      <h1>Contador de Cliques</h1>
      <div style={estilos.card}>
        <h2>Valor atual: <span style={estilos.numero}>{count}</span></h2>
        <button onClick={incrementarContador} style={estilos.botao}>
          Clique aqui para incrementar
        </button>
      </div>
    </div>
  );
};

// Estilização simples inline para visualização
const estilos = {
  container: { textAlign: 'center', marginTop: '50px', fontFamily: 'Arial' },
  card: { border: '1px solid #ddd', padding: '20px', display: 'inline-block', borderRadius: '10px' },
  numero: { color: '#007bff' },
  botao: { padding: '10px 20px', fontSize: '16px', cursor: 'pointer', backgroundColor: '#28a745', color: 'white', border: 'none', borderRadius: '5px' }
};

export default Contador;
