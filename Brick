// Draws one brick like the ones used on the 90s brick game cheapo consoles. It's a black border square with a smaller filled black square inside that has a transparent border.

function drawBrick(x, y, f) {
    const px = x * B;
    const py = y * B;
    cont.fillStyle = "#000";
    cont.fillRect(px, py, B, B);
    cont.fillStyle = "#9bbc0f";
    cont.fillRect(px + 1, py + 1, B - 2, B - 2);
    if (f) {
        cont.fillStyle = "#000";
        cont.fillRect(px + 2, py + 2, B - 4, B - 4);
    }
}

//TODO
function initialTetrisDraw() {
    cont.fillStyle = "#9bbc0f"; // There probably is a better 90s LCD codlor out there...
    cont.fillRect(0, 0, cv.width, cv.height);
    for (let y = 0; y < R; y++) {
        for (let x = 0; x < C; x++) {
            if (bd[y][x]) {
                drawBrick(x, y, 1);
            }
        }
    }
    p.s.forEach((r, dy) => {
        r.forEach((v, dx) => {
            if (v) {
                drawBrick(p.x + dx, p.y + dy, 1);
            }
        });
    });
}
