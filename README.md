# CHESS



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Online Chess Game</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="board"></div>

    <script src="chess.js"></script>
</body>
#board {
    display: grid;
    grid-template-columns: repeat(8, 1fr);
    grid-template-rows: repeat(8, 1fr);
    width: 400px;
    height: 400px;
}

.square {
    width: 50px;
    height: 50px;
    border: 1px solid #333;
    box-sizing: border-box;
}

.piece {
    width: 100%;
    height: 100%;
    background-size: cover;
}


// Chess logic goes here

document.addEventListener("DOMContentLoaded", function () {
    // Initialize the chessboard
    initializeBoard();
});

function initializeBoard() {
    const board = document.getElementById("board");

    for (let row = 0; row < 8; row++) {
        for (let col = 0; col < 8; col++) {
            const square = document.createElement("div");
            square.classList.add("square");
            square.dataset.row = row;
            square.dataset.col = col;
            square.addEventListener("click", handleSquareClick);
            board.appendChild(square);
        }
    }
}

function handleSquareClick(event) {
    // Handle square click event
    const clickedSquare = event.target;
    const row = clickedSquare.dataset.row;
    const col = clickedSquare.dataset.col;
    
    // Add your chess logic here
}
