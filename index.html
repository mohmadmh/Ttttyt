import React, { useState, useEffect, useCallback } from 'react';

const GRID_SIZE = 20;
const INITIAL_SNAKE = [[10, 10], [10, 11], [10, 12]];
const BASE_SPEED = 150;

export default function App() {
  const [snake, setSnake] = useState(INITIAL_SNAKE);
  const [food, setFood] = useState([5, 5]);
  const [direction, setDirection] = useState('UP');
  const [isGameOver, setIsGameOver] = useState(false);
  const [score, setScore] = useState(0);

  const moveSnake = useCallback(() => {
    if (isGameOver) return;
    const head = [...snake[0]];
    if (direction === 'UP') head[0] -= 1;
    if (direction === 'DOWN') head[0] += 1;
    if (direction === 'LEFT') head[1] -= 1;
    if (direction === 'RIGHT') head[1] += 1;

    if (head[0] < 0 || head[0] >= GRID_SIZE || head[1] < 0 || head[1] >= GRID_SIZE ||
        snake.some(s => s[0] === head[0] && s[1] === head[1])) {
      setIsGameOver(true);
      return;
    }

    const newSnake = [head, ...snake];
    if (head[0] === food[0] && head[1] === food[1]) {
      setScore(s => s + 10);
      setFood([Math.floor(Math.random() * GRID_SIZE), Math.floor(Math.random() * GRID_SIZE)]);
    } else {
      newSnake.pop();
    }
    setSnake(newSnake);
  }, [snake, direction, food, isGameOver]);

  useEffect(() => {
    const timer = setInterval(moveSnake, BASE_SPEED);
    return () => clearInterval(timer);
  }, [moveSnake]);

  useEffect(() => {
    const handleKeys = (e) => {
      if (e.key === 'ArrowUp' && direction !== 'DOWN') setDirection('UP');
      if (e.key === 'ArrowDown' && direction !== 'UP') setDirection('DOWN');
      if (e.key === 'ArrowLeft' && direction !== 'RIGHT') setDirection('LEFT');
      if (e.key === 'ArrowRight' && direction !== 'LEFT') setDirection('RIGHT');
    };
    window.addEventListener('keydown', handleKeys);
    return () => window.removeEventListener('keydown', handleKeys);
  }, [direction]);

  return (
    <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center', minHeight: '100vh', background: '#0f172a', color: 'white', fontFamily: 'sans-serif' }}>
      <h1>NEON SNAKE</h1>
      <p>Score: {score}</p>
      <div style={{ position: 'relative', width: GRID_SIZE * 20, height: GRID_SIZE * 20, background: '#1e293b', border: '5px solid #334155' }}>
        {snake.map((p, i) => (
          <div key={i} style={{ position: 'absolute', width: 20, height: 20, background: i === 0 ? '#10b981' : '#059669', top: p[0] * 20, left: p[1] * 20 }} />
        ))}
        <div style={{ position: 'absolute', width: 20, height: 20, background: '#f43f5e', borderRadius: '50%', top: food[0] * 20, left: food[1] * 20 }} />
        {isGameOver && (
          <div style={{ position: 'absolute', inset: 0, background: 'rgba(0,0,0,0.8)', display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center' }}>
            <h2>GAME OVER</h2>
            <button onClick={() => window.location.reload()} style={{ padding: '10px 20px', cursor: 'pointer' }}>Restart</button>
          </div>
        )}
      </div>
    </div>
  );
}
