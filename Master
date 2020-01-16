noStroke();

//variables
//points
var points = 1;
//position of mouse
var startx = 0;
var starty = 0;
//thickness of track
var thickness = 55;
//status of game
//gamestatus = 0 (the game started)
//gamestatus = 1 (gameover screen)
//gamestatus = 2 (waiting for saucer to be clicked)
//gamestatus = 3 (title screen)
//gamestatus = 4 (instructions screen)
var gamestatus = 3;
//score
var score = 1;
//level
var level = 1;
//starting position of animated saucers
var starx1 = 100;
var stary1 = 73;
var starx2 = 70;
var stary2 = 300;
var starx3 = 300;
var stary3 = 150;
var starx4 = 300;
var stary4 = 300;


//saucer for game
var space = function(e, r) {
    var e;
    var r;
    noStroke();
    //bottom of saucer
    fill(111, 3, 133);
    ellipse(e, r, 18, 8);
    //top of saucer
    fill(255, 242, 0);
    ellipse(e, r - 4, 8, 8);
    
};

//animated saucers for title screen
var spaces = function(e, r, x) {
    var e;
    var r;
    noStroke();
    //bottom of saucer
    fill(172, 52, 199);
    ellipse(e, r, x * 2, x);
    //top of saucer
    fill(255, 242, 0);
    ellipse(e, r - 4, x, x);
    
};

//saucers appearing everywhere
var saucer = function (x, y, n) {
    var n;
    var x;
    var y;
    //outer ring of saucer
    fill(202, 141, 217);
    ellipse(x, y, n * 8, n * 8);
    //bubble of saucer
    fill(188, 216, 219);
    ellipse(x, y, n * 4, n * 4);
    //small lights on outside
    fill(247, 244, 198);
    ellipse(x - 5, y + 25, n, n);
    ellipse(x + 5, y + 25, n, n);
    ellipse(x - 5, y - 25, n, n);
    ellipse(x + 5, y - 25, n, n);
    ellipse(x + 25, y + 5, n, n);
    ellipse(x + 25, y - 5, n, n);
    ellipse(x - 25, y + 5, n, n);
    ellipse(x - 25, y - 5, n, n);
    //Xoltan's head
    fill(49, 158, 41);
    ellipse(x, y, n * 2, n * 2);
    //Xoltan's eye
    fill(0, 0, 0);
    ellipse(x, y - 2, n, n);
    
};

//draw loop
draw = function() {
    
    //Instructions Page
    if (gamestatus === 4) {
        background(0, 0, 0);
        //instructions
        fill(255, 255, 255);
        textSize(39);
        fill(240, 231, 51);
        text("Instructions", 100, 54);
        fill(107, 188, 189);
        textSize(17);
        text("Welcome to Xoltan Express, an exciting and", 41, 81);
        text("challenging racing game. Once the game has started,", 6, 98);
        text("left click on the small flying saucer, and begin", 37, 115);
        text("to move your cursor around the track. Be sure to", 25, 132);
        text("go counter-clockwise, or else, there are", 53, 149);
        text("consequences. Each rotation around the track will", 19, 166);
        text("award you with 12 points, and make the track", 37, 183);
        text("skinnier. If you exit the track or click the mouse", 30, 200);
        text("again, it's game over, and you restart.", 62, 217);
        fill(191, 107, 11);
        textSize(26);
        text("Good luck, and I hope you enjoy!", 15, 258);
        fill(166, 0, 255);
        rect(28, 302, 149, 41);
        rect(223, 302, 149, 41);
        fill(0, 0, 0);
        text("START", 59, 332);
        text("BACK", 263, 332);
        
    } 
    
    //Title Screen
    if (gamestatus === 3) {
        background(0, 0, 0);
        //stars
        fill(217, 255, 0);
        spaces(starx1, stary1, 12);
        spaces(starx2, stary2, 12);
        spaces(starx3, stary3, 12);
        spaces(starx4, stary4, 12);
        fill(219, 219, 65);
        textSize(41);
        text("XOLTAN EXPRESS", 15, 52);
        //cool dude
        fill(49, 158, 41);
        ellipse(200, 164, 62, 70);
        ellipse(200, 210, 20, 145);
        ellipse(200, 218, 94, 13);
        fill(217, 0, 245);
        ellipse(200, 141, 82, 32);
        fill(0, 0, 0);
        ellipse(200, 138, 59, 17);
        fill(49, 158, 41);
        ellipse(200, 136, 50, 23);
        ellipse(209, 138, 33, 18);
        ellipse(190, 138, 33, 18);
        fill(0, 0, 0);
        ellipse(200, 169, 28, 15);
        fill(255, 0, 0);
        ellipse(200, 185, 28, 15);
        fill(49, 158, 41);
        rect(183, 177, 31, 7);
        //start button
        fill(146, 209, 209);
        ellipse(200, 88, 100, 32);
        //instructions button
        ellipse(200, 332, 142, 40);
        //text
        textSize(20);
        fill(0, 0, 0);
        text("START", 168, 95);
        textSize(17);
        text("INSTRUCTIONS", 141, 338);
        starx1 = (starx1 + 1) % 400;
        stary1 = (stary1 + 2) % 400;
        starx2 = (starx2 + 3) % 400;
        stary2 = (stary2 + 1) % 400;
        starx3 = (starx3 + 2) % 400;
        stary3 = (stary3 + 1) % 400;
        starx4 = (starx4 + 2) % 400;
        stary4 = (stary4 + 2) % 400;
    }

    //Screen Where User Must Click Saucer To Start
    if (gamestatus === 2) {
        //track layout
        //background
        background(40, 47, 79);
        saucer(random(0, 400), random (0, 400), 9);
        //title
        fill(194, 207, 72);
        textSize(26);
        text("XOLTAN EXPRESS", 86, 36);
        //outer square of track
        fill(161, 155, 155);
        rect(50, 50, 300, 300);
        //inner square of track
        fill(40, 47, 79);
        rect(50 + thickness, 50 + thickness, 300 - (2 * thickness), 300 - (2 * thickness));
            
        fill(49, 158, 41);
        ellipse(200, 164, 62, 70);
        fill(217, 0, 245);
        ellipse(200, 141, 82, 32);
        fill(0, 0, 0);
        ellipse(200, 138, 59, 17);
        fill(49, 158, 41);
        ellipse(200, 136, 50, 23);
        ellipse(209, 138, 33, 18);
        ellipse(190, 138, 33, 18);
        fill(0, 0, 0);
        ellipse(200, 169, 28, 15);
        fill(255, 0, 0);
        ellipse(200, 185, 28, 15);
        fill(49, 158, 41);
        rect(183, 177, 31, 7);
        //car
        space(200, 80);
            
    }

    //Playing Screen
    if (gamestatus === 0) {
        if (startx > 190 && startx < 210 && starty > 70 && starty < 90) {
            //background
            background(40, 47, 79);  
            //points tally
            fill(255, 255, 255);
            textSize(20);
            text("Score:", 28, 38);
            text(score, 93, 38);
            text("Level:", 300, 38);
            text(level, 359, 38);
            //outer square of track
            fill(161, 155, 155);
            rect(50, 50, 300, 300);
            //inner square of track
            fill(40, 47, 79);
            rect(50 + thickness, 50 + thickness, 300 - (2 * thickness), 300 - (2 * thickness));
            //Xoltan
            fill(49, 158, 41);
            ellipse(200, 164, 62, 70);
            fill(217, 0, 245);
            ellipse(200, 141, 82, 32);
            fill(0, 0, 0);
            ellipse(200, 138, 59, 17);
            fill(49, 158, 41);
            ellipse(200, 136, 50, 23);
            ellipse(209, 138, 33, 18);
            ellipse(190, 138, 33, 18);
            fill(0, 0, 0);
            ellipse(200, 169, 28, 15);
            fill(255, 0, 0);
            ellipse(200, 185, 28, 15);
            fill(49, 158, 41);
            rect(183, 177, 31, 7);
            //car
            space(mouseX, mouseY);
            //points
            //for point 2
            if (mouseY > 105 && mouseX < 120 && points === 1) {
                points = points + 1;
            }
            //for point 3
            if (mouseY > 200 && mouseX < 120 && points === 2) {
                points = points + 1;
            }
            //for point 4
            if (mouseY > 295 && mouseX < 120 && points === 3) {
                points = points + 1;
            }
            //for point 5
            if (mouseY > 295 && mouseX > 120 && points === 4) {
                points = points + 1;
            }  
            //for point 6
            if (mouseY > 295 && mouseX > 200 && points === 5) {
                points = points + 1;
            } 
            //for point 7
            if (mouseY > 295 && mouseX > 295 && points === 6) {
                points = points + 1;
            }    
            //for point 8
            if (mouseY < 295 && mouseX > 295 && points === 7) {
                points = points + 1;
            }    
            //for point 9
            if (mouseY < 200 && mouseX > 295 && points === 8) {
                points = points + 1;
            }
            //for point 10
            if (mouseY < 105 && mouseX > 295 && points === 9) {
                points = points + 1;
                
            }    
            //for point 11
            if (mouseY < 105 && mouseX < 295 && points === 10) {
                points = points + 1;
            }  
            //for point 12
            if (mouseY < 105 && mouseX < 205 && points === 11) {
                points = points + 1;
            }    
            //exiting the track
            //left
            if (mouseX < 58) {
                gamestatus = 1;
            }
            //right        
            if (mouseX > 342) {
                gamestatus = 1;
            }
            //bottom
            if (mouseY > 350 - 4) {
                gamestatus = 1;
            }
            //top 
            if (mouseY < 50 + 8) { 
                gamestatus = 1;
            }
            //the insides of the track
            if (mouseY > 46 + thickness && mouseX > 42 + thickness && mouseY < 358 - thickness && mouseX < 358 - thickness) {
                gamestatus = 1;
            }
            //wrong way    
            if (mouseX > 230 && points <= 1) {
                textSize(40);
                textWidth(15);
                fill(255, 255, 255);
                text("WRONG WAY!", 60, 200);
                points = points - 1;
            }
            if (points < 0) {
                textSize(40);
                textWidth(15);
                fill(255, 255, 255);
                text("WRONG WAY!", 60, 200);
                points = points - 1;
            }
            if (score === -998) {
                gamestatus = 1;
            }
            if (points === 12) {
                thickness = thickness * 0.9;
                points = 1;
                level = level + 1;
            }
            score = points + ((level - 1) * 12);
        }        
    }

    //Gameover Screen
    if (gamestatus === 1) {
        background(0, 0, 0);
        fill(255, 255, 255);
        textSize(45);
        text("GAME OVER!", 58, 62);
        textSize(24);
        text("CLICK RESTART TO TRY AGAIN!", 17, 99);
        text("YOUR SCORE WAS:", 70, 343);
        text(score, 312, 344);
        text("HIGH SCORE: 208 BY NING", 45, 374);
        //cool dude
        fill(49, 158, 41);
        ellipse(200, 164, 62, 70);
        ellipse(200, 210, 20, 145);
        ellipse(200, 218, 94, 13);
        fill(217, 0, 245);
        ellipse(200, 141, 82, 32);
        fill(0, 0, 0);
        ellipse(200, 138, 59, 17);
        fill(49, 158, 41);
        ellipse(200, 136, 50, 23);
        ellipse(209, 138, 33, 18);
        ellipse(190, 138, 33, 18);
        fill(0, 0, 0);
        ellipse(200, 169, 28, 15);
        fill(255, 0, 0);
        ellipse(200, 185, 28, 15);
        fill(49, 158, 41);
        rect(183, 177, 31, 7);
    }
    
//FINALLY! END OF THE DRAW LOOP!
};


mousePressed = function() {
    var status; 
    if (gamestatus=== 3) {
        if (mouseX<250 && mouseX>150 && mouseY < 104 && mouseY > 72) {
            status = 2;
        }
    }
    if (gamestatus === 3) {
       if (mouseX > 129 && mouseX < 271 && mouseY > 312 && mouseY < 352) {
            status = 4;
        }
    }    
    if (gamestatus === 4) {
        if (mouseX > 28 && mouseX < 177 && mouseY > 302 && mouseY < 343) {
            status = 2;
        }
    }
    if (gamestatus === 4) {
        if (mouseX > 223 && mouseX < 372 && mouseY > 302 && mouseY < 343) {
            status = 3;
        }
    }
    if (gamestatus === 0) {
        status = 1;
    }
    if (gamestatus ===2) {
        startx=mouseX;
        starty=mouseY;
        status =0;    
    }
    gamestatus=status;
//end of the mousepressed loop
};
