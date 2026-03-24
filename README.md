# Joms Code

This is a repository for various projects.

## Snake Animation Snippet

```javascript
const canvas = document.getElementById('gameCanvas');
const context = canvas.getContext('2d');
let snake = [{ x: 10, y: 10 }];
let direction = { x: 1, y: 0 };

function updateSnake() {
  const head = { x: snake[0].x + direction.x, y: snake[0].y + direction.y };
  snake.unshift(head);
  snake.pop();
}

function drawSnake() {
  context.clearRect(0, 0, canvas.width, canvas.height);
  snake.forEach(segment => {
    context.fillStyle = 'green';
    context.fillRect(segment.x, segment.y, 10, 10);
  });
}

function gameLoop() {
  updateSnake();
  drawSnake();
  requestAnimationFrame(gameLoop);
}

gameLoop();
```

## Old Content

Content from the previous README restored here: 

### Old Content Placeholder

- This is where old content can go.

