ballOut=true;
ballOut2=true;
kirmiziTakim=[];
maviTakim=[];redTeam  =[0,0,0,0,0,0];
blueTeam =[0,0,0,0,0,0];
redT=[];
blueT=[];

/* NOMBRE DEL HOST */
var roomName = "asadito REAL SOCCER";


/* CANTIDAD DE JUGADORES */
var maxPlayers = 12;



var roomPublic = false;

/* NOMBRE DEL BOT */
var playerName = "🏁 Áʀʙɪᴛʀᴏ ʙᴏᴛ 🤖";


var ModoChatPausado = [];
voteKickList=[];
 
/* STADIUM */
//Wartości dotyczą boiska na którym rozgrywany jest mecz - wartości domyślne to oficjalna mapa RS
var stadiumWidth = 1150;
var stadiumHeight = 600;
var radiusBall = 9.8;
var throwInLeeway = 350;
var greenLine = 510;
 
/* SETTINGS */
 
var triggerDistance = radiusBall + 15 + 0.01;
var outLineY = stadiumWidth - (radiusBall / 2) + 6;
stadiumWidth += (radiusBall / 2) + 6;
stadiumHeight += (radiusBall / 2) + 6;
var abuser = 0;
 
var Team = {
    SPECTATORS: 0,
    RED: 1,
    BLUE: 2
};
var lastScores = 0;
var lastTeamTouched = 0;
var lineBallPosition;
var exitingPos = null;
var previousBallPos;
var assistingTouch = "";
var lastPlayerTouched = "";
var lat = -34.5;
var long = -58.4;
var backMSG = false;
var lastCall;
var lastCall2;
var isBallUp = false;
var crossed = false;
var isTimeAddedShown = false;
var isTimeAddedShowndos = false;
var isTimeAddedShowntres = false;
var isTimeAddedShowncuatro = false;
var isTimeAddedShowncinco = false;
var isTimeAddedShownseis = false;
var isTimeAddedShownquince = false;
var isTimeAddedShownsiete = false;
var lineCrossedPlayers = [{name: "temp", times: 0}];
var isBallKickedOutside = false;
var previousPlayerTouched;
var timeOutside = 0;

// ANTI DU - con PlayerAuth
var auth = "qQCjJrMdze7OaXm4K6CClzD3GVWHEVBCh-D5BHz7F22";   // ID: GLH
var auth1 = "PEGAR-PUBLIC-ID";   // ID del jugador 1:
var auth2 = "PEGAR-PUBLIC-ID-2";   // ID del jugador 2:

var db = { p: { N: 6, kt: 2 }, log: [] }; function f(a, b, c) { for (var i = 0; i < a.length; i += 1) { if (a[i][b] === c) { return i; } } return -1; } function spammerosFilter(player, message) { if (player.id == 0) { return; } var ind = f(db.log, 'id', player.id); db.log[ind].lm.push({ ts: Date.now() }); if (db.log[ind].lm.length >= db.p.N) { db.log[ind].lm.splice(0, db.log[ind].lm.length - db.p.N); if (db.log[ind].lm.length / ((db.log[ind].lm[db.log[ind].lm.length - 1].ts - db.log[ind].lm[0].ts) / 30000) > db.p.kt) { room.kickPlayer(player.id, "[👎] ❌ 🚫 𝐏𝐑𝐎𝐇𝐈𝐁𝐈𝐃𝐎 𝐒𝐏𝐀𝐌𝐌𝐄𝐑𝐎𝐒 🚫 ❌ ", true); } } }
var room = HBInit({ roomName: roomName, maxPlayers: maxPlayers, public: roomPublic, playerName: playerName,token: "thr1.AAAAAFyRjgZMy18R2w9YjQ.-FYMqQV18YE", geo: {"code": "CX", "lat": lat, "lon": long }});
var RawRGLHMap=`
{

	"name" : "Real Soccer",

	"width" : 1400,

	"height" : 670,

	"bg" : { "type" : "grass", "width" : 1150, "height" : 600, "kickOffRadius" : 180, "color" : "6a9158" },

	"vertexes" : [
		/* 0 */ { "x" : 0, "y" : 700, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ] },
		/* 1 */ { "x" : 0, "y" : 180, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ] },
		/* 2 */ { "x" : 0, "y" : -180, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ] },
		/* 3 */ { "x" : 0, "y" : -700, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ] },
		/* 4 */ { "x" : 1150, "y" : 255, "cMask" : [ ] },
		/* 5 */ { "x" : 840, "y" : 255, "cMask" : [ ] },
		/* 6 */ { "x" : 1150, "y" : -255, "cMask" : [ ] },
		/* 7 */ { "x" : 840, "y" : -255, "cMask" : [ ] },
		/* 8 */ { "x" : 1150, "y" : 155, "cMask" : [ ] },
		/* 9 */ { "x" : 1030, "y" : 155, "cMask" : [ ] },
		/* 10 */ { "x" : 1150, "y" : -155, "cMask" : [ ] },
		/* 11 */ { "x" : 1030, "y" : -155, "cMask" : [ ] },
		/* 12 */ { "x" : 840, "y" : -135, "cMask" : [ ] },
		/* 13 */ { "x" : 840, "y" : 135, "cMask" : [ ] },
		/* 14 */ { "x" : -1150, "y" : -255, "cMask" : [ ] },
		/* 15 */ { "x" : -840, "y" : -255, "cMask" : [ ] },
		/* 16 */ { "x" : -1150, "y" : 255, "cMask" : [ ] },
		/* 17 */ { "x" : -840, "y" : 255, "cMask" : [ ] },
		/* 18 */ { "x" : -1150, "y" : -155, "cMask" : [ ] },
		/* 19 */ { "x" : -1030, "y" : -155, "cMask" : [ ] },
		/* 20 */ { "x" : -1150, "y" : 155, "cMask" : [ ] },
		/* 21 */ { "x" : -1030, "y" : 155, "cMask" : [ ] },
		/* 22 */ { "x" : -840, "y" : 135, "cMask" : [ ] },
		/* 23 */ { "x" : -840, "y" : -135, "cMask" : [ ] },
		/* 24 */ { "x" : 935, "y" : 4, "cMask" : [ ] },
		/* 25 */ { "x" : 935, "y" : -4, "cMask" : [ ] },
		/* 26 */ { "x" : -935, "y" : 4, "cMask" : [ ] },
		/* 27 */ { "x" : -935, "y" : -4, "cMask" : [ ] },
		/* 28 */ { "x" : -1150, "y" : 525, "bCoef" : 0, "cMask" : ["wall" ] },
		/* 29 */ { "x" : -1075, "y" : 600, "bCoef" : 0, "cMask" : ["wall" ] },
		/* 30 */ { "x" : -1075, "y" : -600, "bCoef" : 0, "cMask" : ["wall" ] },
		/* 31 */ { "x" : -1150, "y" : -525, "bCoef" : 0, "cMask" : ["wall" ] },
		/* 32 */ { "x" : 1075, "y" : 600, "bCoef" : 0, "cMask" : ["wall" ] },
		/* 33 */ { "x" : 1150, "y" : 525, "bCoef" : 0, "cMask" : ["wall" ] },
		/* 34 */ { "x" : 1150, "y" : -525, "bCoef" : 0, "cMask" : ["wall" ] },
		/* 35 */ { "x" : 1075, "y" : -600, "bCoef" : 0, "cMask" : ["wall" ] },
		
		/* 36 */ { "x" : -1150, "y" : 127, "cMask" : ["ball" ], "cGroup" : ["red","blue" ], "trait" : "line" },
		/* 37 */ { "x" : -1214, "y" : 124, "cMask" : ["ball" ], "cGroup" : ["red","blue" ], "trait" : "line" },
		/* 38 */ { "x" : -1150, "y" : -127, "cMask" : ["ball" ], "cGroup" : ["red","blue" ], "trait" : "line" },
		/* 39 */ { "x" : -1214, "y" : -124, "cMask" : ["ball" ], "cGroup" : ["red","blue" ], "trait" : "line" },
		/* 40 */ { "x" : 1150, "y" : 127, "cMask" : ["ball" ], "cGroup" : ["red","blue" ], "trait" : "line" },
		/* 41 */ { "x" : 1214, "y" : 124, "cMask" : ["ball" ], "cGroup" : ["red","blue" ], "trait" : "line" },
		/* 42 */ { "x" : 1150, "y" : -127, "cMask" : ["ball" ], "cGroup" : ["red","blue" ], "trait" : "line" },
		/* 43 */ { "x" : 1214, "y" : -124, "cMask" : ["ball" ], "cGroup" : ["red","blue" ], "trait" : "line" },
		
		/* 44 */ { "x" : 0, "y" : -4, "cMask" : [ ] },
		/* 45 */ { "x" : 0, "y" : 4, "cMask" : [ ] },
		/* 46 */ { "x" : 0, "y" : -4, "cMask" : [ ] },
		/* 47 */ { "x" : 0, "y" : 4, "cMask" : [ ] },
		/* 48 */ { "x" : -1214, "y" : 124, "cMask" : [ ] },
		/* 49 */ { "x" : -1250, "y" : 150, "cMask" : [ ] },
		/* 50 */ { "x" : -1214, "y" : -124, "cMask" : [ ] },
		/* 51 */ { "x" : -1250, "y" : -150, "cMask" : [ ] },
		/* 52 */ { "x" : 1214, "y" : 124, "cMask" : [ ] },
		/* 53 */ { "x" : 1250, "y" : 150, "cMask" : [ ] },
		/* 54 */ { "x" : 1214, "y" : -124, "cMask" : [ ] },
		/* 55 */ { "x" : 1250, "y" : -150, "cMask" : [ ] },
		/* 56 */ { "x" : -1185, "y" : 155, "bCoef" : -4.5, "cMask" : ["ball" ] },
		/* 57 */ { "x" : -1185, "y" : 255, "bCoef" : -4.5, "cMask" : ["ball" ] },
		/* 58 */ { "x" : 1185, "y" : 155, "bCoef" : -4.5, "cMask" : ["ball" ] },
		/* 59 */ { "x" : 1185, "y" : 255, "bCoef" : -4.5, "cMask" : ["ball" ] },
		/* 60 */ { "x" : -1185, "y" : -155, "bCoef" : -4.5, "cMask" : ["ball" ] },
		/* 61 */ { "x" : -1185, "y" : -255, "bCoef" : -4.5, "cMask" : ["ball" ] },
		/* 62 */ { "x" : 1185, "y" : -155, "bCoef" : -4.5, "cMask" : ["ball" ] },
		/* 63 */ { "x" : 1185, "y" : -255, "bCoef" : -4.5, "cMask" : ["ball" ] },
		/* 64 */ { "x" : 1158, "y" : -607, "bCoef" : -2.45, "cMask" : ["ball" ] },
		/* 65 */ { "x" : 1187, "y" : -578, "bCoef" : -2.45, "cMask" : ["ball" ] },
		/* 66 */ { "x" : 1158, "y" : 607, "bCoef" : -2.45, "cMask" : ["ball" ] },
		/* 67 */ { "x" : 1187, "y" : 578, "bCoef" : -2.45, "cMask" : ["ball" ] },
		/* 68 */ { "x" : -1158, "y" : 607, "bCoef" : -2.45, "cMask" : ["ball" ] },
		/* 69 */ { "x" : -1187, "y" : 578, "bCoef" : -2.45, "cMask" : ["ball" ] },
		/* 70 */ { "x" : -1158, "y" : -607, "bCoef" : -2.45, "cMask" : ["ball" ] },
		/* 71 */ { "x" : -1187, "y" : -578, "bCoef" : -2.45, "cMask" : ["ball" ] },
		/* 72 */ { "x" : -1190, "y" : -255, "bCoef" : -1, "cMask" : ["ball" ] },
		/* 73 */ { "x" : -1180, "y" : -255, "bCoef" : -1, "cMask" : ["ball" ] },
		/* 74 */ { "x" : -1190, "y" : -155, "bCoef" : -1, "cMask" : ["ball" ] },
		/* 75 */ { "x" : -1180, "y" : -155, "bCoef" : -1, "cMask" : ["ball" ] },
		/* 76 */ { "x" : -1190, "y" : 155, "bCoef" : -1, "cMask" : ["ball" ] },
		/* 77 */ { "x" : -1180, "y" : 155, "bCoef" : -1, "cMask" : ["ball" ] },
		/* 78 */ { "x" : -1190, "y" : 255, "bCoef" : -1, "cMask" : ["ball" ] },
		/* 79 */ { "x" : -1180, "y" : 255, "bCoef" : -1, "cMask" : ["ball" ] },
		/* 80 */ { "x" : 1190, "y" : -255, "bCoef" : -1, "cMask" : ["ball" ] },
		/* 81 */ { "x" : 1180, "y" : -255, "bCoef" : -1, "cMask" : ["ball" ] },
		/* 82 */ { "x" : 1190, "y" : -155, "bCoef" : -1, "cMask" : ["ball" ] },
		/* 83 */ { "x" : 1180, "y" : -155, "bCoef" : -1, "cMask" : ["ball" ] },
		/* 84 */ { "x" : 1190, "y" : 255, "bCoef" : -1, "cMask" : ["ball" ] },
		/* 85 */ { "x" : 1180, "y" : 255, "bCoef" : -1, "cMask" : ["ball" ] },
		/* 86 */ { "x" : 1190, "y" : 155, "bCoef" : -1, "cMask" : ["ball" ] },
		/* 87 */ { "x" : 1180, "y" : 155, "bCoef" : -1, "cMask" : ["ball" ] },
		/* 88 */ { "x" : -1148, "y" : -525, "cMask" : [ ] },
		/* 89 */ { "x" : 1148, "y" : -525, "cMask" : [ ] },
		/* 90 */ { "x" : -1148, "y" : 525, "cMask" : [ ] },
		/* 91 */ { "x" : 1148, "y" : 525, "cMask" : [ ] },
		/* 92 */ { "x" : -1150, "y" : -260, "cMask" : [ ] },
		/* 93 */ { "x" : -840, "y" : -600, "cMask" : [ ] },
		/* 94 */ { "x" : -1150, "y" : 260, "cMask" : [ ] },
		/* 95 */ { "x" : -840, "y" : 600, "cMask" : [ ] },
		/* 96 */ { "x" : 1150, "y" : -260, "cMask" : [ ] },
		/* 97 */ { "x" : 840, "y" : -600, "cMask" : [ ] },
		/* 98 */ { "x" : 1150, "y" : 260, "cMask" : [ ] },
		/* 99 */ { "x" : 840, "y" : 600, "cMask" : [ ] },
		/* 100 */ { "x" : -1416, "y" : -475, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 101 */ { "x" : -1300, "y" : -475, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["red" ] },
		/* 102 */ { "x" : -1300, "y" : 475, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["red" ] },
		/* 103 */ { "x" : -1416, "y" : 475, "bCoef" : 0, "cMask" : ["blue" ] },
		
		/* 104 */ { "x" : -1414, "y" : -475, "trait" : "kickOffBarrier" },
		/* 105 */ { "x" : -1300, "y" : -475, "trait" : "kickOffBarrier" },
		/* 106 */ { "x" : -1300, "y" : 475, "trait" : "kickOffBarrier" },
		/* 107 */ { "x" : -1416, "y" : 475, "trait" : "kickOffBarrier" },
		
		/* 108 */ { "x" : -1356, "y" : -76, "bCoef" : 0, "cMask" : ["blue" ], "color" : "6666FF" },
		/* 109 */ { "x" : -1356, "y" : 84, "bCoef" : 0, "cMask" : ["blue" ], "color" : "6666FF" },
		/* 110 */ { "x" : -1361, "y" : -76, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 111 */ { "x" : -1351, "y" : -76, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 112 */ { "x" : -1361, "y" : 84, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 113 */ { "x" : -1351, "y" : 84, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 114 */ { "x" : -1410, "y" : -76, "bCoef" : 0, "cMask" : ["red" ] },
		/* 115 */ { "x" : -1410, "y" : 84, "bCoef" : 0, "cMask" : ["red" ] },
		/* 116 */ { "x" : 1400, "y" : -475, "bCoef" : 0, "cMask" : ["red" ], "dist" : -1400 },
		/* 117 */ { "x" : 1300, "y" : -475, "bCoef" : 0, "cMask" : ["red" ], "cGroup" : ["blue" ] },
		/* 118 */ { "x" : 1300, "y" : 475, "bCoef" : 0, "cMask" : ["red" ], "cGroup" : ["blue" ] },
		/* 119 */ { "x" : 1400, "y" : 475, "bCoef" : 0, "cMask" : ["red" ], "dist" : -1400 },
		
		/* 120 */ { "x" : 1400, "y" : -475, "trait" : "kickOffBarrier", "dist" : -1400 },
		/* 121 */ { "x" : 1300, "y" : -475, "trait" : "kickOffBarrier" },
		/* 122 */ { "x" : 1300, "y" : 475, "trait" : "kickOffBarrier" },
		/* 123 */ { "x" : 1400, "y" : 475, "trait" : "kickOffBarrier", "dist" : -1400 },
		
		/* 124 */ { "x" : 1345, "y" : -82, "bCoef" : 0, "cMask" : ["red" ], "color" : "FF6666" },
		/* 125 */ { "x" : 1345, "y" : 78, "bCoef" : 0, "cMask" : ["red" ], "color" : "FF6666" },
		/* 126 */ { "x" : 1350, "y" : -82, "bCoef" : 0, "cMask" : ["red" ] },
		/* 127 */ { "x" : 1340, "y" : -82, "bCoef" : 0, "cMask" : ["red" ] },
		/* 128 */ { "x" : 1350, "y" : 78, "bCoef" : 0, "cMask" : ["red" ] },
		/* 129 */ { "x" : 1340, "y" : 78, "bCoef" : 0, "cMask" : ["red" ] },
		/* 130 */ { "x" : 1410, "y" : -82, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 131 */ { "x" : 1410, "y" : 78, "bCoef" : 0, "cMask" : ["blue" ] }

	],

	"segments" : [
		{ "v0" : 37, "v1" : 39, "color" : "FFFFFF", "bCoef" : 0.1, "cMask" : ["ball" ], "cGroup" : ["red","blue" ], "trait" : "line" },
		{ "v0" : 43, "v1" : 41, "color" : "FFFFFF", "bCoef" : 0.1, "cMask" : ["ball" ], "cGroup" : ["red","blue" ], "trait" : "line" },
		
		{ "v0" : 4, "v1" : 5, "color" : "C7E6BD", "cMask" : [ ] },
		{ "v0" : 5, "v1" : 7, "color" : "C7E6BD", "cMask" : [ ] },
		{ "v0" : 6, "v1" : 7, "color" : "C7E6BD", "cMask" : [ ] },
		{ "v0" : 8, "v1" : 9, "color" : "C7E6BD", "cMask" : [ ] },
		{ "v0" : 9, "v1" : 11, "color" : "C7E6BD", "cMask" : [ ] },
		{ "v0" : 10, "v1" : 11, "color" : "C7E6BD", "cMask" : [ ] },
		{ "v0" : 13, "v1" : 12, "curve" : 130, "color" : "C7E6BD", "cMask" : [ ], "curveF" : 0.4663076581549986 },
		{ "v0" : 14, "v1" : 15, "color" : "C7E6BD", "cMask" : [ ] },
		{ "v0" : 15, "v1" : 17, "color" : "C7E6BD", "cMask" : [ ] },
		{ "v0" : 16, "v1" : 17, "color" : "C7E6BD", "cMask" : [ ] },
		{ "v0" : 18, "v1" : 19, "color" : "C7E6BD", "cMask" : [ ] },
		{ "v0" : 19, "v1" : 21, "color" : "C7E6BD", "cMask" : [ ] },
		{ "v0" : 20, "v1" : 21, "color" : "C7E6BD", "cMask" : [ ] },
		{ "v0" : 23, "v1" : 22, "curve" : 130, "color" : "C7E6BD", "cMask" : [ ], "curveF" : 0.4663076581549986 },
		{ "v0" : 25, "v1" : 24, "curve" : 180, "color" : "C7E6BD", "cMask" : [ ], "curveF" : 6.123233995736766e-17 },
		{ "v0" : 27, "v1" : 26, "curve" : 180, "color" : "C7E6BD", "cMask" : [ ], "curveF" : 6.123233995736766e-17 },
		{ "v0" : 24, "v1" : 25, "curve" : 180, "color" : "C7E6BD", "cMask" : [ ], "curveF" : 6.123233995736766e-17 },
		{ "v0" : 26, "v1" : 27, "curve" : 180, "color" : "C7E6BD", "cMask" : [ ], "curveF" : 6.123233995736766e-17 },
		{ "v0" : 24, "v1" : 25, "curve" : 89.99999999999999, "color" : "C7E6BD", "cMask" : [ ], "curveF" : 1.0000000000000002 },
		{ "v0" : 26, "v1" : 27, "curve" : 89.99999999999999, "color" : "C7E6BD", "cMask" : [ ], "curveF" : 1.0000000000000002 },
		{ "v0" : 25, "v1" : 24, "curve" : 89.99999999999999, "color" : "C7E6BD", "cMask" : [ ], "curveF" : 1.0000000000000002 },
		{ "v0" : 27, "v1" : 26, "curve" : 89.99999999999999, "color" : "C7E6BD", "cMask" : [ ], "curveF" : 1.0000000000000002 },
		{ "v0" : 24, "v1" : 25, "color" : "C7E6BD", "cMask" : [ ] },
		{ "v0" : 26, "v1" : 27, "color" : "C7E6BD", "cMask" : [ ] },
		{ "v0" : 28, "v1" : 29, "curve" : 89.99999999999999, "color" : "C7E6BD", "bCoef" : 0, "cMask" : ["wall" ], "curveF" : 1.0000000000000002 },
		{ "v0" : 30, "v1" : 31, "curve" : 89.99999999999999, "color" : "C7E6BD", "bCoef" : 0, "cMask" : ["wall" ], "curveF" : 1.0000000000000002 },
		{ "v0" : 32, "v1" : 33, "curve" : 89.99999999999999, "color" : "C7E6BD", "bCoef" : 0, "cMask" : ["wall" ], "curveF" : 1.0000000000000002 },
		{ "v0" : 34, "v1" : 35, "curve" : 89.99999999999999, "color" : "C7E6BD", "bCoef" : 0, "cMask" : ["wall" ], "curveF" : 1.0000000000000002 },
		
		{ "v0" : 36, "v1" : 37, "color" : "FFFFFF", "cMask" : ["ball" ], "cGroup" : ["red","blue" ], "trait" : "line" },
		{ "v0" : 39, "v1" : 38, "color" : "FFFFFF", "cMask" : ["ball" ], "cGroup" : ["red","blue" ], "trait" : "line" },
		{ "v0" : 41, "v1" : 40, "color" : "FFFFFF", "cMask" : ["ball" ], "cGroup" : ["red","blue" ], "trait" : "line" },
		{ "v0" : 42, "v1" : 43, "color" : "FFFFFF", "cMask" : ["ball" ], "cGroup" : ["red","blue" ], "trait" : "line" },
		
		{ "v0" : 45, "v1" : 44, "curve" : 180, "color" : "C7E6BD", "cMask" : [ ], "curveF" : 6.123233995736766e-17 },
		{ "v0" : 46, "v1" : 47, "curve" : 180, "color" : "C7E6BD", "cMask" : [ ], "curveF" : 6.123233995736766e-17 },
		{ "v0" : 45, "v1" : 44, "curve" : 89.99999999999999, "color" : "C7E6BD", "cMask" : [ ], "curveF" : 1.0000000000000002 },
		{ "v0" : 46, "v1" : 47, "curve" : 89.99999999999999, "color" : "C7E6BD", "cMask" : [ ], "curveF" : 1.0000000000000002 },
		{ "v0" : 48, "v1" : 49, "color" : "FFFFFF", "cMask" : [ ] },
		{ "v0" : 50, "v1" : 51, "color" : "FFFFFF", "cMask" : [ ] },
		{ "v0" : 52, "v1" : 53, "color" : "FFFFFF", "cMask" : [ ] },
		{ "v0" : 54, "v1" : 55, "color" : "FFFFFF", "cMask" : [ ] },
		{ "v0" : 56, "v1" : 57, "curve" : 40, "color" : "BEB86C", "bCoef" : -4.7, "cMask" : ["ball" ], "curveF" : 2.7474774194546225 },
		{ "v0" : 59, "v1" : 58, "curve" : 40, "color" : "BEB86C", "bCoef" : -4.7, "cMask" : ["ball" ], "curveF" : 2.7474774194546225 },
		{ "v0" : 61, "v1" : 60, "curve" : 40, "color" : "BEB86C", "bCoef" : -4.7, "cMask" : ["ball" ], "curveF" : 2.7474774194546225 },
		{ "v0" : 62, "v1" : 63, "curve" : 40, "color" : "BEB86C", "bCoef" : -4.7, "cMask" : ["ball" ], "curveF" : 2.7474774194546225 },
		{ "v0" : 65, "v1" : 64, "curve" : 59.99999999999999, "color" : "BEB86C", "bCoef" : -2.45, "cMask" : ["ball" ], "curveF" : 1.7320508075688774 },
		{ "v0" : 66, "v1" : 67, "curve" : 59.99999999999999, "color" : "BEB86C", "bCoef" : -2.45, "cMask" : ["ball" ], "curveF" : 1.7320508075688774 },
		{ "v0" : 69, "v1" : 68, "curve" : 59.99999999999999, "color" : "BEB86C", "bCoef" : -2.45, "cMask" : ["ball" ], "curveF" : 1.7320508075688774 },
		{ "v0" : 70, "v1" : 71, "curve" : 59.99999999999999, "color" : "BEB86C", "bCoef" : -2.45, "cMask" : ["ball" ], "curveF" : 1.7320508075688774 },
		{ "v0" : 0, "v1" : 1, "vis" : false, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ] },
		{ "v0" : 1, "v1" : 2, "curve" : 180, "vis" : false, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["blueKO" ], "curveF" : 6.123233995736766e-17 },
		{ "v0" : 2, "v1" : 1, "curve" : 180, "vis" : false, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO" ], "curveF" : 6.123233995736766e-17 },
		{ "v0" : 2, "v1" : 3, "vis" : false, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ] },
		{ "v0" : 72, "v1" : 73, "bCoef" : -1, "cMask" : ["ball" ] },
		{ "v0" : 74, "v1" : 75, "bCoef" : -1, "cMask" : ["ball" ] },
		{ "v0" : 76, "v1" : 77, "bCoef" : -1, "cMask" : ["ball" ] },
		{ "v0" : 78, "v1" : 79, "bCoef" : -1, "cMask" : ["ball" ] },
		{ "v0" : 80, "v1" : 81, "bCoef" : -1, "cMask" : ["ball" ] },
		{ "v0" : 82, "v1" : 83, "bCoef" : -1, "cMask" : ["ball" ] },
		{ "v0" : 84, "v1" : 85, "bCoef" : -1, "cMask" : ["ball" ] },
		{ "v0" : 86, "v1" : 87, "bCoef" : -1, "cMask" : ["ball" ] },
		{ "v0" : 88, "v1" : 89, "color" : "5E844D", "cMask" : [ ] },
		{ "v0" : 90, "v1" : 91, "color" : "5E844D", "cMask" : [ ] },
		{ "v0" : 93, "v1" : 92, "curve" : 100, "color" : "5E844D", "cMask" : [ ], "curveF" : 0.83909963117728 },
		{ "v0" : 94, "v1" : 95, "curve" : 100, "color" : "5E844D", "cMask" : [ ], "curveF" : 0.83909963117728 },
		{ "v0" : 96, "v1" : 97, "curve" : 100, "color" : "5E844D", "cMask" : [ ], "curveF" : 0.83909963117728 },
		{ "v0" : 99, "v1" : 98, "curve" : 100, "color" : "5E844D", "cMask" : [ ], "curveF" : 0.83909963117728 },
		{ "v0" : 100, "v1" : 101, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "y" : -475 },
		{ "v0" : 101, "v1" : 102, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["red" ], "x" : -1300 },
		{ "v0" : 102, "v1" : 103, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "y" : 475 },
		
		{ "v0" : 104, "v1" : 105, "trait" : "kickOffBarrier", "y" : -475 },
		{ "v0" : 106, "v1" : 107, "trait" : "kickOffBarrier", "y" : 475 },
		
		{ "v0" : 108, "v1" : 109, "color" : "6666FF", "bCoef" : 1000000, "cMask" : ["blue" ] },
		{ "v0" : 110, "v1" : 111, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ] },
		{ "v0" : 112, "v1" : 113, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ] },
		{ "v0" : 114, "v1" : 115, "vis" : false, "bCoef" : 1000000, "cMask" : ["red" ], "x" : -1410 },
		{ "v0" : 116, "v1" : 117, "vis" : false, "bCoef" : 0, "cMask" : ["red" ], "y" : -475 },
		{ "v0" : 117, "v1" : 118, "vis" : false, "bCoef" : 0, "cMask" : ["red" ], "cGroup" : ["blue" ], "x" : 1300 },
		{ "v0" : 118, "v1" : 119, "vis" : false, "bCoef" : 0, "cMask" : ["red" ], "y" : 475 },
		
		{ "v0" : 120, "v1" : 121, "trait" : "kickOffBarrier", "y" : -475 },
		{ "v0" : 122, "v1" : 123, "trait" : "kickOffBarrier", "y" : 475 },
		
		{ "v0" : 124, "v1" : 125, "color" : "FF6666", "bCoef" : 1000000, "cMask" : ["red" ] },
		{ "v0" : 126, "v1" : 127, "vis" : false, "bCoef" : 0, "cMask" : ["red" ] },
		{ "v0" : 128, "v1" : 129, "vis" : false, "bCoef" : 0, "cMask" : ["red" ] },
		{ "v0" : 130, "v1" : 131, "vis" : false, "bCoef" : 1000000, "cMask" : ["blue" ], "x" : 1410 }

	],

	"planes" : [
		{ "normal" : [0,1 ], "dist" : -635, "bCoef" : 0, "cMask" : ["ball" ] },
		{ "normal" : [0,-1 ], "dist" : -635, "bCoef" : 0, "cMask" : ["ball" ] },
		{ "normal" : [0,1 ], "dist" : -675, "bCoef" : 0 },
		{ "normal" : [0,-1 ], "dist" : -675, "bCoef" : 0 },
		{ "normal" : [1,0 ], "dist" : -1214, "bCoef" : 0, "cMask" : ["ball" ] },
		{ "normal" : [-1,0 ], "dist" : -1214, "bCoef" : 0, "cMask" : ["ball" ] },
		{ "normal" : [1,0 ], "dist" : -1420, "bCoef" : 0 },
		{ "normal" : [-1,0 ], "dist" : -1420, "bCoef" : 0 }

	],

	"goals" : [
		{ "p0" : [-1161.3,-124 ], "p1" : [-1161.3,124 ], "team" : "red" },
		{ "p0" : [1161.3,124 ], "p1" : [1161.3,-124 ], "team" : "blue" }

	],

	"discs" : [
		{ "radius" : 9.8, "invMass" : 1.05, "cGroup" : ["ball","kick","score" ] },
		{ "radius" : 5, "invMass" : 0, "pos" : [-1150,127 ], "color" : "ffffff" },
		{ "radius" : 5, "invMass" : 0, "pos" : [-1150,-127 ], "color" : "ffffff" },
		{ "radius" : 5, "invMass" : 0, "pos" : [1150,127 ], "color" : "ffffff" },
		{ "radius" : 5, "invMass" : 0, "pos" : [1150,-127 ], "color" : "ffffff" },
		{ "radius" : 3, "invMass" : 0, "pos" : [-1250,150 ], "color" : "4a4e52", "bCoef" : 3, "cMask" : [ ] },
		{ "radius" : 3, "invMass" : 0, "pos" : [-1250,-150 ], "color" : "4a4e52", "bCoef" : 3, "cMask" : [ ] },
		{ "radius" : 3, "invMass" : 0, "pos" : [1250,150 ], "color" : "4a4e52", "bCoef" : 3, "cMask" : [ ] },
		{ "radius" : 3, "invMass" : 0, "pos" : [1250,-150 ], "color" : "4a4e52", "bCoef" : 3, "cMask" : [ ] },
		{ "radius" : 2, "invMass" : 0, "pos" : [-1150,-600 ], "bCoef" : -0.1, "cMask" : ["ball" ] },
		{ "radius" : 2, "invMass" : 0, "pos" : [-1150,600 ], "bCoef" : -0.1, "cMask" : ["ball" ] },
		{ "radius" : 2, "invMass" : 0, "pos" : [1150,-600 ], "bCoef" : -0.1, "cMask" : ["ball" ] },
		{ "radius" : 2, "invMass" : 0, "pos" : [1150,600 ], "bCoef" : -0.1, "cMask" : ["ball" ] }

	],

	"playerPhysics" : {
		"acceleration" : 0.12,
		"kickStrength" : 5.65

	},
	"ballPhysics" : "disc0",

	"spawnDistance" : 500,

	"redSpawnPoints" : [
		[ -217, -30
		],
		[ -217, 30
		],
		[ -217, 90
		],
		[ -217, -90
		],
		[ -217, 150
		],
		[ -217, -150
		],
		[ -110, 654
		],
		[ -70, 654
		],
		[ -30, 654
		]

	],

	"blueSpawnPoints" : [
		[ 217, -30
		],
		[ 217, 30
		],
		[ 217, 90
		],
		[ 217, -90
		],
		[ 217, 150
		],
		[ 217, -150
		],
		[ 110, 654
		],
		[ 70, 654
		],
		[ 30, 654
		]

	],

	"traits" : {
		"kickOffBarrier" : { "vis" : false, "bCoef" : 0.1, "cGroup" : ["redKO","blueKO" ], "cMask" : ["red","blue" ] },
		"line" : { "vis" : true, "cMask" : [ ] }

	}
}`;
var Futsalx4=`
{

	"name" : "ℱᴜᴛsᴀʟ​ ✘4 ; Bʏ ❕ℬ𝚊𝚣𝚒𝚗𝚐𝚊 & 𝙶𝙻𝙷",

	"width" : 800,

	"height" : 350,

	"spawnDistance" : 350,

	"bg" : { "type" : "hockey", "width" : 700, "height" : 320, "kickOffRadius" : 100, "cornerRadius" : 0 },

	"vertexes" : [
		/* 0 */ { "x" : 701, "y" : 320, "trait" : "ballArea" },
		/* 1 */ { "x" : 698, "y" : -317, "trait" : "ballArea" },
		
		/* 2 */ { "x" : 0, "y" : 350, "trait" : "kickOffBarrier" },
		/* 3 */ { "x" : 0, "y" : 100, "bCoef" : 0.15, "trait" : "kickOffBarrier", "color" : "F8F8F8", "vis" : true, "curve" : 180 },
		/* 4 */ { "x" : 0, "y" : -100, "bCoef" : 0.15, "trait" : "kickOffBarrier", "color" : "F8F8F8", "vis" : true, "curve" : 180 },
		/* 5 */ { "x" : 0, "y" : -349, "trait" : "kickOffBarrier" },
		
		/* 6 */ { "x" : -701, "y" : -80, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [-700,-80 ], "p0" : [-707.25,0 ] },
		/* 7 */ { "x" : -740, "y" : -80, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [-700,-80 ], "p0" : [-707.25,0 ] },
		/* 8 */ { "x" : -740, "y" : 80, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [-700,80 ], "p0" : [-707.25,0 ] },
		/* 9 */ { "x" : -701, "y" : 80, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [-700,80 ], "p0" : [-707.25,0 ] },
		/* 10 */ { "x" : 699, "y" : -80, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [700,-80 ] },
		/* 11 */ { "x" : 740, "y" : -80, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [700,-80 ] },
		/* 12 */ { "x" : 740, "y" : 80, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [700,80 ] },
		/* 13 */ { "x" : 699, "y" : 80, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [700,80 ] },
		
		/* 14 */ { "x" : -700, "y" : 80, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [-700,80 ], "p0" : [-707.25,0 ] },
		/* 15 */ { "x" : -700, "y" : 321, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8" },
		/* 16 */ { "x" : -700, "y" : -80, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [-700,-80 ], "p0" : [-707.25,0 ] },
		/* 17 */ { "x" : -700, "y" : -319, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8" },
		/* 18 */ { "x" : -700, "y" : 320, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea" },
		/* 19 */ { "x" : 701, "y" : 320, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea" },
		/* 20 */ { "x" : 700, "y" : 80, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "pos" : [700,80 ] },
		/* 21 */ { "x" : 700, "y" : 320, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea" },
		/* 22 */ { "x" : 700, "y" : -317, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8" },
		/* 23 */ { "x" : 700, "y" : -80, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [700,-80 ] },
		/* 24 */ { "x" : 698, "y" : -317, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea" },
		/* 25 */ { "x" : 698, "y" : -317, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea" },
		/* 26 */ { "x" : -701, "y" : -320, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0 },
		/* 27 */ { "x" : 698, "y" : -320, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0 },
		
		/* 28 */ { "x" : 0, "y" : -319, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier" },
		/* 29 */ { "x" : 0, "y" : -100, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier" },
		/* 30 */ { "x" : 0, "y" : 100, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier" },
		/* 31 */ { "x" : 0, "y" : 320, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier" },
		/* 32 */ { "x" : 0, "y" : -100, "bCoef" : 0.1, "cMask" : ["red","blue" ], "trait" : "kickOffBarrier", "vis" : true, "color" : "F8F8F8" },
		/* 33 */ { "x" : 0, "y" : 100, "bCoef" : 0.1, "cMask" : ["red","blue" ], "trait" : "kickOffBarrier", "vis" : true, "color" : "F8F8F8" },
		/* 34 */ { "x" : 0, "y" : 100, "trait" : "kickOffBarrier", "color" : "F8F8F8", "vis" : true, "curve" : -180 },
		/* 35 */ { "x" : 0, "y" : -100, "trait" : "kickOffBarrier", "color" : "F8F8F8", "vis" : true, "curve" : -180 },
		/* 36 */ { "x" : 0, "y" : 100, "trait" : "kickOffBarrier", "color" : "F8F8F8", "vis" : true, "curve" : 0 },
		/* 37 */ { "x" : 0, "y" : -100, "trait" : "kickOffBarrier", "color" : "F8F8F8", "vis" : true, "curve" : 0 },
		
		/* 38 */ { "x" : -708.5, "y" : 80, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "vis" : false, "pos" : [-700,80 ], "p0" : [-707.25,0 ] },
		/* 39 */ { "x" : -707.5, "y" : 321, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "vis" : false },
		/* 40 */ { "x" : -708.5, "y" : -319, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false, "curve" : 0 },
		/* 41 */ { "x" : -708.5, "y" : -80, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false, "curve" : 0, "pos" : [-700,-80 ], "p0" : [-707.25,0 ] },
		/* 42 */ { "x" : 705, "y" : -317, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false, "curve" : 0 },
		/* 43 */ { "x" : 705, "y" : -80, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false, "curve" : 0, "pos" : [700,-80 ] },
		/* 44 */ { "x" : 708, "y" : 80, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "vis" : false, "pos" : [700,80 ] },
		/* 45 */ { "x" : 708, "y" : 320, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "vis" : false },
		
		/* 46 */ { "x" : 0, "y" : -100, "bCoef" : 0.1, "trait" : "line" },
		/* 47 */ { "x" : 0, "y" : 100, "bCoef" : 0.1, "trait" : "line" },
		/* 48 */ { "x" : -700, "y" : -80, "bCoef" : 0.1, "trait" : "line", "p0" : [-707.25,0 ] },
		/* 49 */ { "x" : -700, "y" : 80, "bCoef" : 0.1, "trait" : "line", "p0" : [-707.25,0 ] },
		/* 50 */ { "x" : 700, "y" : -80, "bCoef" : 0.1, "trait" : "line" },
		/* 51 */ { "x" : 700, "y" : 80, "bCoef" : 0.1, "trait" : "line" },
		/* 52 */ { "x" : -700, "y" : 270, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : -90 },
		/* 53 */ { "x" : -470, "y" : 65, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 0 },
		/* 54 */ { "x" : -700, "y" : 307, "bCoef" : 0.1, "trait" : "line", "curve" : -90 },
		/* 55 */ { "x" : -686, "y" : 320, "bCoef" : 0.1, "trait" : "line", "curve" : -90 },
		/* 56 */ { "x" : -700, "y" : -270, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 90 },
		/* 57 */ { "x" : -470, "y" : -75, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 0 },
		/* 58 */ { "x" : -700, "y" : -305, "bCoef" : 0.1, "trait" : "line", "curve" : 90 },
		/* 59 */ { "x" : -687, "y" : -320, "bCoef" : 0.1, "trait" : "line", "curve" : 90 },
		/* 60 */ { "x" : 700, "y" : -303, "bCoef" : 0.1, "trait" : "line", "curve" : -90 },
		/* 61 */ { "x" : 684, "y" : -320, "bCoef" : 0.1, "trait" : "line", "curve" : -90 },
		/* 62 */ { "x" : 700, "y" : 306, "bCoef" : 0.1, "trait" : "line", "curve" : 90 },
		/* 63 */ { "x" : 687, "y" : 320, "bCoef" : 0.1, "trait" : "line", "curve" : 90 },
		/* 64 */ { "x" : 700, "y" : 270, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 90 },
		/* 65 */ { "x" : 470, "y" : 66, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 90 },
		/* 66 */ { "x" : 700, "y" : -270, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : -90 },
		/* 67 */ { "x" : 470, "y" : -74, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : -90 },
		/* 68 */ { "x" : 470, "y" : 66, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 0 },
		/* 69 */ { "x" : 470, "y" : -74, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 0 },
		/* 70 */ { "x" : -414, "y" : -3, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 71 */ { "x" : -414, "y" : -5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 72 */ { "x" : -414, "y" : -1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 73 */ { "x" : -414, "y" : -7, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 74 */ { "x" : -414, "y" : -6, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 75 */ { "x" : -414, "y" : -2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 76 */ { "x" : -414, "y" : -7.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 77 */ { "x" : -414, "y" : -0.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 78 */ { "x" : 398, "y" : -1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 79 */ { "x" : 398, "y" : -3, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 80 */ { "x" : 398, "y" : 1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 81 */ { "x" : 398, "y" : -5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 82 */ { "x" : 398, "y" : -4, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 83 */ { "x" : 398, "y" : 0, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 84 */ { "x" : 398, "y" : -5.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 85 */ { "x" : 398, "y" : 1.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 86 */ { "x" : -316.5, "y" : -3, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 87 */ { "x" : -316.5, "y" : -5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 88 */ { "x" : -316.5, "y" : -1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 89 */ { "x" : -316.5, "y" : -7, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 90 */ { "x" : -316.5, "y" : -6, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 91 */ { "x" : -316.5, "y" : -2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 92 */ { "x" : -316.5, "y" : -7.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 93 */ { "x" : -316.5, "y" : -0.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 94 */ { "x" : 300.5, "y" : -1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 95 */ { "x" : 300.5, "y" : -3, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 96 */ { "x" : 300.5, "y" : 1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 97 */ { "x" : 300.5, "y" : -5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 98 */ { "x" : 300.5, "y" : -4, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 99 */ { "x" : 300.5, "y" : 0, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 100 */ { "x" : 300.5, "y" : -5.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 101 */ { "x" : 300.5, "y" : 1.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 102 */ { "x" : -246, "y" : 305, "bCoef" : 0.1, "trait" : "line" },
		/* 103 */ { "x" : -246, "y" : 335, "bCoef" : 0.1, "trait" : "line" },
		/* 104 */ { "x" : -126, "y" : 305, "bCoef" : 0.1, "trait" : "line" },
		/* 105 */ { "x" : -126, "y" : 335, "bCoef" : 0.1, "trait" : "line" },
		/* 106 */ { "x" : 246, "y" : 305, "bCoef" : 0.1, "trait" : "line" },
		/* 107 */ { "x" : 246, "y" : 335, "bCoef" : 0.1, "trait" : "line" },
		/* 108 */ { "x" : 126, "y" : 305, "bCoef" : 0.1, "trait" : "line" },
		/* 109 */ { "x" : 126, "y" : 335, "bCoef" : 0.1, "trait" : "line" },
		/* 110 */ { "x" : -387, "y" : 320, "bCoef" : 0.1, "trait" : "line" },
		/* 111 */ { "x" : -387, "y" : 337, "bCoef" : 0.1, "trait" : "line" },
		/* 112 */ { "x" : -707, "y" : 123, "bCoef" : 0.1, "trait" : "line", "p0" : [-707.25,0 ] },
		/* 113 */ { "x" : -726, "y" : 123, "bCoef" : 0.1, "trait" : "line", "p0" : [-707.25,0 ] },
		/* 114 */ { "x" : 705, "y" : 123, "bCoef" : 0.1, "trait" : "line" },
		/* 115 */ { "x" : 724, "y" : 123, "bCoef" : 0.1, "trait" : "line" },
		/* 116 */ { "x" : -707, "y" : -123, "bCoef" : 0.1, "trait" : "line", "p0" : [-707.25,0 ] },
		/* 117 */ { "x" : -726, "y" : -123, "bCoef" : 0.1, "trait" : "line", "p0" : [-707.25,0 ] },
		/* 118 */ { "x" : 705, "y" : -123, "bCoef" : 0.1, "trait" : "line" },
		/* 119 */ { "x" : 724, "y" : -123, "bCoef" : 0.1, "trait" : "line" },
		/* 120 */ { "x" : -380, "y" : -320, "bCoef" : 0.1, "trait" : "line" },
		/* 121 */ { "x" : -380, "y" : -337, "bCoef" : 0.1, "trait" : "line" },
		/* 122 */ { "x" : 380, "y" : 320, "bCoef" : 0.1, "trait" : "line" },
		/* 123 */ { "x" : 380, "y" : 337, "bCoef" : 0.1, "trait" : "line" },
		/* 124 */ { "x" : 380, "y" : -320, "bCoef" : 0.1, "trait" : "line" },
		/* 125 */ { "x" : 380, "y" : -337, "bCoef" : 0.1, "trait" : "line" },
		
		/* 126 */ { "x" : 700, "y" : -317, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "vis" : false },
		/* 127 */ { "x" : 702, "y" : -80, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [700,-80 ], "vis" : false },
		/* 128 */ { "x" : 704, "y" : 80, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "pos" : [700,80 ], "vis" : false },
		/* 129 */ { "x" : 704, "y" : 320, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false },
		/* 130 */ { "x" : -704, "y" : 80, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [-700,80 ], "vis" : false, "p0" : [-707.25,0 ] },
		/* 131 */ { "x" : -703, "y" : 321, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "vis" : false },
		/* 132 */ { "x" : -704, "y" : -80, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [-700,-80 ], "vis" : false, "p0" : [-707.25,0 ] },
		/* 133 */ { "x" : -704, "y" : -319, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "vis" : false }

	],

	"segments" : [
		{ "v0" : 6, "v1" : 7, "curve" : 0, "color" : "F8F8F8", "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "pos" : [-700,-80 ], "y" : -80, "p0" : [-707.25,0 ] },
		{ "v0" : 7, "v1" : 8, "color" : "F8F8F8", "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "x" : -740, "p0" : [-707.25,0 ] },
		{ "v0" : 8, "v1" : 9, "curve" : 0, "color" : "F8F8F8", "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "pos" : [-700,80 ], "y" : 80, "p0" : [-707.25,0 ] },
		{ "v0" : 10, "v1" : 11, "curve" : 0, "color" : "F8F8F8", "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "pos" : [700,-80 ], "y" : -80 },
		{ "v0" : 11, "v1" : 12, "color" : "F8F8F8", "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "x" : 740 },
		{ "v0" : 12, "v1" : 13, "curve" : 0, "color" : "F8F8F8", "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "pos" : [700,80 ], "y" : 80 },
		
		{ "v0" : 2, "v1" : 3, "trait" : "kickOffBarrier" },
		{ "v0" : 3, "v1" : 4, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.15, "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier" },
		{ "v0" : 3, "v1" : 4, "curve" : -180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.15, "cGroup" : ["redKO" ], "trait" : "kickOffBarrier" },
		{ "v0" : 4, "v1" : 5, "trait" : "kickOffBarrier" },
		
		{ "v0" : 14, "v1" : 15, "vis" : true, "color" : "F8F8F8", "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -700 },
		{ "v0" : 16, "v1" : 17, "vis" : true, "color" : "F8F8F8", "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -700 },
		{ "v0" : 18, "v1" : 19, "vis" : true, "color" : "F8F8F8", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "y" : 320 },
		{ "v0" : 20, "v1" : 21, "vis" : true, "color" : "F8F8F8", "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 700 },
		{ "v0" : 22, "v1" : 23, "vis" : true, "color" : "F8F8F8", "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 700 },
		{ "v0" : 24, "v1" : 25, "vis" : true, "color" : "F8F8F8", "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 550, "y" : -240 },
		{ "v0" : 26, "v1" : 27, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "y" : -320 },
		
		{ "v0" : 28, "v1" : 29, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier" },
		{ "v0" : 30, "v1" : 31, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier" },
		
		{ "v0" : 38, "v1" : 39, "curve" : 0, "vis" : false, "color" : "F8F8F8", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -557.5 },
		{ "v0" : 40, "v1" : 41, "curve" : 0, "vis" : false, "color" : "F8F8F8", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -557.5 },
		{ "v0" : 42, "v1" : 43, "curve" : 0, "vis" : false, "color" : "F8F8F8", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 705 },
		{ "v0" : 44, "v1" : 45, "curve" : 0, "vis" : false, "color" : "F8F8F8", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 708 },
		
		{ "v0" : 46, "v1" : 47, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 0 },
		{ "v0" : 48, "v1" : 49, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -700, "p0" : [-707.25,0 ] },
		{ "v0" : 50, "v1" : 51, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 700 },
		{ "v0" : 52, "v1" : 53, "curve" : -90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 55, "v1" : 54, "curve" : -90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 56, "v1" : 57, "curve" : 90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 53, "v1" : 57, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -470 },
		{ "v0" : 59, "v1" : 58, "curve" : 90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 61, "v1" : 60, "curve" : -90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 63, "v1" : 62, "curve" : 90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 64, "v1" : 65, "curve" : 90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 66, "v1" : 67, "curve" : -90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 68, "v1" : 69, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 470 },
		{ "v0" : 71, "v1" : 70, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 70, "v1" : 71, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 73, "v1" : 72, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 72, "v1" : 73, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 75, "v1" : 74, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 74, "v1" : 75, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 77, "v1" : 76, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 76, "v1" : 77, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 79, "v1" : 78, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 78, "v1" : 79, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 81, "v1" : 80, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 80, "v1" : 81, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 83, "v1" : 82, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 82, "v1" : 83, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 85, "v1" : 84, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 84, "v1" : 85, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 87, "v1" : 86, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 86, "v1" : 87, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 89, "v1" : 88, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 88, "v1" : 89, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 91, "v1" : 90, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 90, "v1" : 91, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 93, "v1" : 92, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 92, "v1" : 93, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 95, "v1" : 94, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 94, "v1" : 95, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 97, "v1" : 96, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 96, "v1" : 97, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 99, "v1" : 98, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 98, "v1" : 99, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 101, "v1" : 100, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 100, "v1" : 101, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 102, "v1" : 103, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -240 },
		{ "v0" : 104, "v1" : 105, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -120 },
		{ "v0" : 106, "v1" : 107, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 240 },
		{ "v0" : 108, "v1" : 109, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 120 },
		{ "v0" : 110, "v1" : 111, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -381 },
		{ "v0" : 112, "v1" : 113, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -240, "y" : 123, "p0" : [-707.25,0 ] },
		{ "v0" : 114, "v1" : 115, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -240, "y" : 123 },
		{ "v0" : 116, "v1" : 117, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -240, "y" : -123, "p0" : [-707.25,0 ] },
		{ "v0" : 118, "v1" : 119, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -240, "y" : -123 },
		{ "v0" : 120, "v1" : 121, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -380 },
		{ "v0" : 122, "v1" : 123, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 380 },
		{ "v0" : 124, "v1" : 125, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 380 },
		
		{ "v0" : 126, "v1" : 127, "vis" : false, "color" : "F8F8F8", "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 553 },
		{ "v0" : 128, "v1" : 129, "vis" : false, "color" : "F8F8F8", "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 704 },
		{ "v0" : 130, "v1" : 131, "vis" : false, "color" : "F8F8F8", "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -553 },
		{ "v0" : 132, "v1" : 133, "vis" : false, "color" : "F8F8F8", "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -553 }

	],

	"goals" : [
		{ "p0" : [-706.25,-75 ], "p1" : [-706.25,80 ], "team" : "red" },
		{ "p0" : [706.25,80 ], "p1" : [706.25,-80 ], "team" : "blue" }

	],

	"discs" : [
		{ "radius" : 5, "pos" : [-700,80 ], "color" : "6666CC", "trait" : "goalPost", "y" : 80, "p0" : [-707.25,0 ] },
		{ "radius" : 5, "pos" : [-700,-80 ], "color" : "6666CC", "trait" : "goalPost", "y" : -80, "x" : -560, "p0" : [-707.25,0 ] },
		{ "radius" : 5, "pos" : [700,80 ], "color" : "6666CC", "trait" : "goalPost", "y" : 80 },
		{ "radius" : 5, "pos" : [700,-80 ], "color" : "6666CC", "trait" : "goalPost", "y" : -80 },
		
		{ "radius" : 3, "invMass" : 0, "pos" : [-700,320 ], "color" : "FFCC00", "bCoef" : 0.1, "trait" : "line" },
		{ "radius" : 3, "invMass" : 0, "pos" : [-700,-320 ], "color" : "FFCC00", "bCoef" : 0.1, "trait" : "line" },
		{ "radius" : 3, "invMass" : 0, "pos" : [700,-320 ], "color" : "FFCC00", "bCoef" : 0.1, "trait" : "line" },
		{ "radius" : 3, "invMass" : 0, "pos" : [700,320 ], "color" : "FFCC00", "bCoef" : 0.1, "trait" : "line" }

	],

	"planes" : [
		{ "normal" : [0,1 ], "dist" : -320, "bCoef" : 1, "trait" : "ballArea", "vis" : false, "curve" : 0 },
		{ "normal" : [0,-1 ], "dist" : -320, "bCoef" : 1, "trait" : "ballArea" },
		
		{ "normal" : [0,1 ], "dist" : -350, "bCoef" : 0.1 },
		{ "normal" : [0,-1 ], "dist" : -350, "bCoef" : 0.1 },
		{ "normal" : [1,0 ], "dist" : -760, "bCoef" : 0.1 },
		{ "normal" : [-1,0 ], "dist" : -760, "bCoef" : 0.1 },
		
		{ "normal" : [1,0 ], "dist" : -760, "bCoef" : 0.1, "trait" : "ballArea", "vis" : false, "curve" : 0 },
		{ "normal" : [-1,0 ], "dist" : -760, "bCoef" : 0.1, "trait" : "ballArea", "vis" : false, "curve" : 0 }

	],

	"traits" : {
		"ballArea" : { "vis" : false, "bCoef" : 1, "cMask" : ["ball" ] },
		"goalPost" : { "radius" : 8, "invMass" : 0, "bCoef" : 0.5 },
		"goalNet" : { "vis" : true, "bCoef" : 0.1, "cMask" : ["ball" ] },
		"line" : { "vis" : true, "bCoef" : 0.1, "cMask" : ["" ] },
		"kickOffBarrier" : { "vis" : false, "bCoef" : 0.1, "cGroup" : ["redKO","blueKO" ], "cMask" : ["red","blue" ] }

	},

	"playerPhysics" : {
		"bCoef" : 0,
		"acceleration" : 0.11,
		"kickingAcceleration" : 0.083,
		"kickStrength" : 5

	},

	"ballPhysics" : {
		"radius" : 6.25,
		"bCoef" : 0.4,
		"invMass" : 1.5,
		"damping" : 0.99,
		"color" : "FFCC00"

	}
}`;

var PensRedHandball=`
{

	"name" : "ᴘᴇɴᴀʟᴛʏ ʀᴇᴅ ᴛᴇᴀᴍ 🔴 | 𝐆𝐋𝐇 ( 𝑯𝒂𝒏𝒅𝒃𝒂𝒍𝒍 🤾 )",

	"width" : 790,

	"height" : 350,

	"spawnDistance" : 300,

	"redSpawnPoints" : [
		[ 45, -90
		],
		[ 45, -30
		],
		[ 45, 30
		],
		[ 45, 90
		]

	],

	"blueSpawnPoints" : [
		[ 773, -90
		],
		[ 773, -30
		],
		[ 773, 30
		],
		[ 773, 90
		]

	],

	"bg" : { "type" : "none", "width" : 0, "height" : 0, "kickOffRadius" : 0, "cornerRadius" : 0, "color" : "253D97" },

	"playerPhysics" : {
		"bCoef" : 0.5,
		"invMass" : 0.5,
		"damping" : 0.96,
		"acceleration" : 0.12,
		"kickingAcceleration" : 0.07,
		"kickingDamping" : 0.96,
		"kickStrength" : 5.65

	},

	"ballPhysics" : {
		"pos" : [ 397, 0
		],
		"radius" : 10,
		"color" : "fff100"

	},

	"vertexes" : [
		/* 0 */ { "x" : -174, "y" : -142, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["blueKO","redKO" ], "curve" : 235 },
		/* 1 */ { "x" : -176, "y" : 131, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["blueKO","redKO" ], "curve" : 235 },
		/* 2 */ { "x" : 937, "y" : -155, "bCoef" : 0, "cMask" : ["blue" ], "dist" : -1400 },
		/* 3 */ { "x" : 747, "y" : -156, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 4 */ { "x" : 747, "y" : 144, "bCoef" : 0, "cMask" : ["blue" ], "curve" : 0 },
		/* 5 */ { "x" : 936, "y" : 144, "bCoef" : 0, "cMask" : ["blue" ], "dist" : -1400, "curve" : 0 },
		
		/* 6 */ { "x" : 742, "y" : -156, "trait" : "kickOffBarrier", "cMask" : ["blue" ] },
		
		/* 7 */ { "x" : 858, "y" : -125, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 8 */ { "x" : 858, "y" : 115, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 9 */ { "x" : -477.93953763264415, "y" : 731, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		
		/* 10 */ { "x" : 395, "y" : -15, "trait" : "powerboost", "bCoef" : -2.2, "vis" : false, "cMask" : ["ball" ], "pos" : [955,0 ], "radius" : 10, "curve" : 216 },
		/* 11 */ { "x" : 395, "y" : 5, "trait" : "powerboost", "bCoef" : -2.2, "vis" : false, "cMask" : ["ball" ], "pos" : [955,0 ], "radius" : 10, "curve" : 216 },
		
		/* 12 */ { "x" : 576, "y" : 111.23596984067328, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["redKO" ], "vis" : false, "curve" : 0 },
		/* 13 */ { "x" : 576, "y" : -128.763613824687, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["redKO" ], "vis" : false, "curve" : 0 },
		/* 14 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 742, "y" : 144 },
		/* 15 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 742, "y" : 12 },
		/* 16 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 622, "y" : 12 },
		/* 17 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 742, "y" : -24 },
		/* 18 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 622, "y" : -24 },
		/* 19 */ { "bCoef" : -2.4, "cMask" : ["blue" ], "x" : 706.0188554822, "y" : 59.50390625 },
		/* 20 */ { "bCoef" : -2.4, "cMask" : ["blue" ], "x" : 706.0188554822, "y" : -71.49609375 },
		/* 21 */ { "bCoef" : 0, "cMask" : ["red" ], "x" : 177, "y" : 615, "curve" : -77 },
		/* 22 */ { "bCoef" : 0, "cMask" : ["red" ], "x" : 177, "y" : -625, "curve" : -77 },
		/* 23 */ { "x" : 576, "y" : 111.23596984067328, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "vis" : false, "curve" : 0, "radius" : 15, "pos" : [67,0 ], "_selected" : "segment" },
		/* 24 */ { "x" : 576, "y" : -128.763613824687, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "vis" : false, "curve" : 0, "radius" : 15, "pos" : [67,0 ], "_selected" : "segment" },
		/* 25 */ { "x" : 592, "y" : -224, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "curve" : -85, "color" : "E9CC6D" },
		
		/* 26 */ { "x" : 492, "y" : 316, "trait" : "line", "color" : "EF7E29" },
		
		/* 27 */ { "x" : 397, "y" : -19, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "FFFFFF", "radius" : 10 },
		/* 28 */ { "x" : 397, "y" : 11, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "FFFFFF", "radius" : 10 },
		
		/* 29 */ { "x" : 592, "y" : 90, "cMask" : ["red" ], "cGroup" : ["red" ], "trait" : "ballArea", "vis" : false, "color" : "E9CC6D" },
		/* 30 */ { "x" : 592, "y" : -98, "cMask" : ["red" ], "cGroup" : ["red" ], "trait" : "ballArea", "curve" : 0, "vis" : false, "color" : "E9CC6D" },
		
		/* 31 */ { "x" : 592, "y" : -224, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : -85, "color" : "88A9D9", "vis" : false },
		
		/* 32 */ { "x" : 592, "y" : 87.33920484545074, "cMask" : ["ball" ], "cGroup" : ["red" ], "trait" : "ballArea", "vis" : false, "color" : "FFFFFF", "curve" : 0 },
		/* 33 */ { "x" : 592, "y" : -98, "cMask" : ["ball" ], "cGroup" : ["red" ], "trait" : "ballArea", "curve" : 0, "vis" : false, "color" : "FFFFFF" },
		
		/* 34 */ { "x" : 592, "y" : 216, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "curve" : 0, "color" : "E9CC6D", "vis" : false },
		/* 35 */ { "x" : 592, "y" : -224, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : 0, "color" : "88A9D9", "vis" : false },
		
		/* 36 */ { "x" : 592, "y" : -98, "cMask" : ["ball" ], "cGroup" : ["red" ], "trait" : "ballArea", "curve" : 0, "vis" : false, "color" : "FFFFFF", "bCoef" : 1 },
		/* 37 */ { "x" : 592, "y" : -325, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "vis" : true, "color" : "FFFFFF", "bCoef" : 1 },
		/* 38 */ { "x" : 592, "y" : 315, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : true, "color" : "FFFFFF", "curve" : 0, "bCoef" : 1 },
		/* 39 */ { "x" : 592, "y" : 90, "cMask" : ["ball" ], "cGroup" : ["red" ], "trait" : "ballArea", "vis" : false, "color" : "FFFFFF", "curve" : 0, "bCoef" : 1 },
		
		/* 40 */ { "x" : 590, "y" : 216, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : 85, "color" : "2CAAFF" },
		/* 41 */ { "x" : 425, "y" : 106, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : 8, "color" : "2CAAFF" },
		/* 42 */ { "x" : 590, "y" : -224, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : -85, "color" : "2CAAFF" },
		/* 43 */ { "x" : 425, "y" : -114, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : 8, "color" : "2CAAFF" },
		
		/* 44 */ { "x" : 460.90125641831196, "y" : 301.9572422383344, "trait" : "line", "color" : "EF7E29" },
		/* 45 */ { "x" : 492, "y" : -324, "trait" : "line", "color" : "EF7E29" },
		/* 46 */ { "x" : 491.0899057985382, "y" : 316.2098043123669, "trait" : "line", "color" : "EF7E29" },
		/* 47 */ { "x" : 460.2378162708901, "y" : 302.93813422703, "trait" : "line", "color" : "EF7E29" },
		/* 48 */ { "x" : 462.713123102581, "y" : -310.762625798387, "trait" : "line", "color" : "EF7E29" },
		/* 49 */ { "x" : 444.78555149359147, "y" : 292.43458264259755, "trait" : "line", "color" : "EF7E29" },
		/* 50 */ { "x" : 408.18816225723685, "y" : 265.07561802353257, "trait" : "line", "color" : "EF7E29" },
		/* 51 */ { "x" : 371.05522503972065, "y" : 230.24226584512587, "trait" : "line", "color" : "EF7E29" },
		/* 52 */ { "x" : 313.982193163891, "y" : 54.49880675209518, "trait" : "line", "color" : "EF7E29" },
		/* 53 */ { "x" : 312.9981406555976, "y" : 36.50506230916902, "trait" : "line", "color" : "EF7E29" },
		/* 54 */ { "x" : 357.01407293866214, "y" : 209.2796018870813, "trait" : "line", "color" : "EF7E29" },
		/* 55 */ { "x" : 325.6930868351151, "y" : 139.43964430949083, "trait" : "line", "color" : "EF7E29" },
		/* 56 */ { "x" : 440.87812114968597, "y" : -301.1040865966373, "trait" : "line", "color" : "EF7E29" },
		/* 57 */ { "x" : 404.6441117593936, "y" : -273.26565259885837, "trait" : "line", "color" : "EF7E29" },
		/* 58 */ { "x" : 420.98876130101564, "y" : -286.396305985508, "trait" : "line", "color" : "EF7E29" },
		/* 59 */ { "x" : 385.5288007685749, "y" : -256.45907536158984, "trait" : "line", "color" : "EF7E29" },
		/* 60 */ { "x" : 318.09410267505655, "y" : 107.97650354787007, "trait" : "line", "color" : "EF7E29" },
		/* 61 */ { "x" : 315.0783239836344, "y" : 86.49214151361383, "trait" : "line", "color" : "EF7E29" },
		/* 62 */ { "x" : 424.7042731236562, "y" : 277.9899398735921, "trait" : "line", "color" : "EF7E29" },
		/* 63 */ { "x" : 312.7974096944257, "y" : 6.014029307165885, "trait" : "line", "color" : "EF7E29" },
		/* 64 */ { "x" : 388.85323292648945, "y" : 248.5221694256424, "trait" : "line", "color" : "EF7E29" },
		/* 65 */ { "x" : 346.4723211500617, "y" : 190.79991793630217, "trait" : "line", "color" : "EF7E29" },
		/* 66 */ { "x" : 334.3014196476447, "y" : 164.87947896203968, "trait" : "line", "color" : "EF7E29" },
		/* 67 */ { "x" : 369.959798881452, "y" : -239.95955080301712, "trait" : "line", "color" : "EF7E29" },
		/* 68 */ { "x" : 354.2090675592799, "y" : -216.80071524108587, "trait" : "line", "color" : "EF7E29" },
		/* 69 */ { "x" : 343.9115327471668, "y" : -198.18384046344227, "trait" : "line", "color" : "EF7E29" },
		/* 70 */ { "x" : 332.08295430734483, "y" : -172.10540622952055, "trait" : "line", "color" : "EF7E29" },
		/* 71 */ { "x" : 323.79714186893466, "y" : -148.55439605331273, "trait" : "line", "color" : "EF7E29" },
		/* 72 */ { "x" : 317.5867054225696, "y" : -121.0004307084653, "trait" : "line", "color" : "EF7E29" },
		/* 73 */ { "x" : 314.86063407766346, "y" : -98.47824680692861, "trait" : "line", "color" : "EF7E29" },
		/* 74 */ { "x" : 313.1595111996012, "y" : -70.46658362353033, "trait" : "line", "color" : "EF7E29" },
		/* 75 */ { "x" : 312.6360681855451, "y" : -18.493745891795022, "trait" : "line", "color" : "EF7E29" },
		/* 76 */ { "x" : 312.4419203601924, "y" : -47.984800562871555, "trait" : "line", "color" : "EF7E29" },
		
		/* 77 */ { "x" : 469, "y" : -12, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "FFFFFF" },
		/* 78 */ { "x" : 469, "y" : 4, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "FFFFFF" },
		
		/* 79 */ { "x" : 591.2715278479752, "y" : -95.9828225460283, "trait" : "ballArea" },
		
		/* 80 */ { "x" : 592.722625690124, "y" : 87.33920484545074, "trait" : "goalNet", "color" : "FFFFFF", "cMask" : ["blue","ball" ] },
		/* 81 */ { "x" : 622.7216858912061, "y" : 87.10174526602265, "trait" : "goalNet", "color" : "FFFFFF", "cMask" : ["blue","ball" ], "bCoef" : 0, "curve" : 0 },
		/* 82 */ { "x" : 622, "y" : -96.2202821254564, "trait" : "goalNet", "color" : "FFFFFF", "cMask" : ["blue","ball" ], "bCoef" : 0, "curve" : 0 },
		/* 83 */ { "x" : 591.2715278479752, "y" : -95.9828225460283, "trait" : "goalNet", "color" : "FFFFFF", "cMask" : ["blue","ball" ] },
		
		/* 84 */ { "x" : 591.2715278479752, "y" : -95.9828225460283, "trait" : "fieldArea" },
		
		/* 85 */ { "x" : 592, "y" : -95.9828225460283, "trait" : "line", "color" : "FFFFFF" },
		/* 86 */ { "x" : 592, "y" : 87.33920484545074, "trait" : "line", "color" : "FFFFFF" },
		/* 87 */ { "x" : 592, "y" : 58.69513806553215, "trait" : "line", "color" : "FFFFFF" },
		/* 88 */ { "x" : 592, "y" : -68.48451843730645, "trait" : "line", "color" : "FFFFFF" },
		/* 89 */ { "x" : 606.7221871172956, "y" : 87.22839037505096, "trait" : "line", "color" : "FFFFFF" },
		/* 90 */ { "x" : 609.2709639686243, "y" : -96.12529829368515, "trait" : "line", "color" : "FFFFFF" },
		/* 91 */ { "x" : -211, "y" : 301, "trait" : "line", "color" : "FFFFFF" },
		/* 92 */ { "x" : -211, "y" : 331, "trait" : "line", "color" : "FFFFFF" },
		/* 93 */ { "x" : 89, "y" : 301, "trait" : "line", "color" : "FFFFFF" },
		/* 94 */ { "x" : 89, "y" : 331, "trait" : "line", "color" : "FFFFFF" },
		/* 95 */ { "x" : -211, "y" : -339, "trait" : "line", "color" : "FFFFFF" },
		/* 96 */ { "x" : -211, "y" : -309, "trait" : "line", "color" : "FFFFFF" },
		/* 97 */ { "x" : 89, "y" : -339, "trait" : "line", "color" : "FFFFFF" },
		/* 98 */ { "x" : 89, "y" : -309, "trait" : "line", "color" : "FFFFFF" },
		/* 99 */ { "x" : 592, "y" : -55.95715121697479, "trait" : "line", "color" : "CF0000" },
		/* 100 */ { "x" : 592, "y" : -35.33277704328226, "trait" : "line", "color" : "CF0000" },
		/* 101 */ { "x" : 592, "y" : -10, "trait" : "line", "color" : "CF0000" },
		/* 102 */ { "x" : 592, "y" : 12, "trait" : "line", "color" : "CF0000" },
		/* 103 */ { "x" : 592, "y" : -95.9828225460283, "trait" : "line", "color" : "CF0000" },
		/* 104 */ { "x" : 592, "y" : -73.60211534710332, "trait" : "line", "color" : "CF0000" },
		/* 105 */ { "x" : 592, "y" : 66, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line", "color" : "CF0000" },
		/* 106 */ { "x" : 592, "y" : 90.08069095559071, "trait" : "line", "color" : "CF0000" },
		/* 107 */ { "x" : 592, "y" : 31, "trait" : "line", "color" : "CF0000" },
		/* 108 */ { "x" : 592, "y" : 46, "trait" : "line", "color" : "CF0000" },
		
		/* 109 */ { "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "x" : 591, "y" : -224, "vis" : false, "curve" : 0 },
		/* 110 */ { "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "x" : 592, "y" : 216, "vis" : false, "curve" : 0 },
		
		/* 111 */ { "x" : -715, "y" : 315, "trait" : "ballArea", "vis" : true, "color" : "ffffff", "curve" : 0, "bCoef" : 1 },
		
		/* 112 */ { "trait" : "line", "x" : -61, "y" : -75.65621948242188, "curve" : -180, "color" : "EF7E29" },
		/* 113 */ { "trait" : "line", "x" : -61, "y" : 88.34378051757812, "curve" : -180, "color" : "EF7E29" },
		
		/* 114 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 622, "y" : 82.00390625 },
		/* 115 */ { "x" : -715, "y" : 214.00781250000003, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "curve" : -85, "color" : "E9CC6D" },
		
		/* 116 */ { "x" : -615, "y" : -325, "trait" : "line", "color" : "EF7E29" },
		
		/* 117 */ { "x" : -520, "y" : 9.0078125, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "FFFFFF", "radius" : 10 },
		/* 118 */ { "x" : -520, "y" : -20.992187500000014, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "FFFFFF", "radius" : 10 },
		
		/* 119 */ { "x" : -715, "y" : -99.99218750000003, "cMask" : ["red" ], "cGroup" : ["red" ], "trait" : "ballArea", "vis" : false, "color" : "E9CC6D" },
		/* 120 */ { "x" : -715, "y" : 88.00781250000001, "cMask" : ["red" ], "cGroup" : ["red" ], "trait" : "ballArea", "curve" : 0, "vis" : false, "color" : "E9CC6D" },
		
		/* 121 */ { "x" : -715, "y" : 214.00781250000003, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : -85, "color" : "88A9D9", "vis" : false },
		
		/* 122 */ { "x" : -715, "y" : -97.33139234545078, "cMask" : ["ball" ], "cGroup" : ["red" ], "trait" : "ballArea", "vis" : false, "color" : "FFFFFF", "curve" : 0 },
		/* 123 */ { "x" : -715, "y" : 88.00781250000001, "cMask" : ["ball" ], "cGroup" : ["red" ], "trait" : "ballArea", "curve" : 0, "vis" : false, "color" : "FFFFFF" },
		
		/* 124 */ { "x" : -715, "y" : -225.99218750000006, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "curve" : 0, "color" : "E9CC6D", "vis" : false },
		/* 125 */ { "x" : -715, "y" : 214.00781250000003, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : 0, "color" : "88A9D9", "vis" : false },
		
		/* 126 */ { "x" : -715, "y" : 88.00781250000001, "cMask" : ["ball" ], "cGroup" : ["red" ], "trait" : "ballArea", "curve" : 0, "vis" : false, "color" : "FFFFFF", "bCoef" : 1 },
		/* 127 */ { "x" : -715, "y" : 315, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "vis" : true, "color" : "FFFFFF", "bCoef" : 1 },
		/* 128 */ { "x" : -715, "y" : -325, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : true, "color" : "FFFFFF", "curve" : 0, "bCoef" : 1 },
		/* 129 */ { "x" : -715, "y" : -99.99218750000003, "cMask" : ["ball" ], "cGroup" : ["red" ], "trait" : "ballArea", "vis" : false, "color" : "FFFFFF", "curve" : 0, "bCoef" : 1 },
		
		/* 130 */ { "x" : -713, "y" : -225.99218750000006, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : 85, "color" : "2CAAFF" },
		/* 131 */ { "x" : -548, "y" : -115.99218750000003, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : 8, "color" : "2CAAFF" },
		/* 132 */ { "x" : -713, "y" : 214.00781250000003, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : -85, "color" : "2CAAFF" },
		/* 133 */ { "x" : -548, "y" : 104.00781250000001, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : 8, "color" : "2CAAFF" },
		
		/* 134 */ { "x" : -583.901256418312, "y" : -311.94942973833446, "trait" : "line", "color" : "EF7E29" },
		/* 135 */ { "x" : -615, "y" : 315, "trait" : "line", "color" : "EF7E29" },
		/* 136 */ { "x" : -583.2378162708901, "y" : -312.93032172703005, "trait" : "line", "color" : "EF7E29" },
		/* 137 */ { "x" : -585.713123102581, "y" : 300.77043829838703, "trait" : "line", "color" : "EF7E29" },
		/* 138 */ { "x" : -567.7855514935915, "y" : -302.4267701425976, "trait" : "line", "color" : "EF7E29" },
		/* 139 */ { "x" : -531.1881622572369, "y" : -275.0678055235326, "trait" : "line", "color" : "EF7E29" },
		/* 140 */ { "x" : -494.05522503972065, "y" : -240.23445334512593, "trait" : "line", "color" : "EF7E29" },
		/* 141 */ { "x" : -436.982193163891, "y" : -64.4909942520952, "trait" : "line", "color" : "EF7E29" },
		/* 142 */ { "x" : -435.9981406555976, "y" : -46.497249809169034, "trait" : "line", "color" : "EF7E29" },
		/* 143 */ { "x" : -480.01407293866214, "y" : -219.27178938708136, "trait" : "line", "color" : "EF7E29" },
		/* 144 */ { "x" : -448.6930868351151, "y" : -149.43183180949086, "trait" : "line", "color" : "EF7E29" },
		/* 145 */ { "x" : -563.878121149686, "y" : 291.11189909663733, "trait" : "line", "color" : "EF7E29" },
		/* 146 */ { "x" : -527.6441117593936, "y" : 263.2734650988584, "trait" : "line", "color" : "EF7E29" },
		/* 147 */ { "x" : -543.9887613010156, "y" : 276.40411848550804, "trait" : "line", "color" : "EF7E29" },
		/* 148 */ { "x" : -508.5288007685749, "y" : 246.4668878615899, "trait" : "line", "color" : "EF7E29" },
		/* 149 */ { "x" : -441.09410267505655, "y" : -117.9686910478701, "trait" : "line", "color" : "EF7E29" },
		/* 150 */ { "x" : -438.0783239836344, "y" : -96.48432901361386, "trait" : "line", "color" : "EF7E29" },
		/* 151 */ { "x" : -547.7042731236562, "y" : -287.98212737359216, "trait" : "line", "color" : "EF7E29" },
		/* 152 */ { "x" : -435.7974096944258, "y" : -16.0062168071659, "trait" : "line", "color" : "EF7E29" },
		/* 153 */ { "x" : -511.85323292648945, "y" : -258.51435692564246, "trait" : "line", "color" : "EF7E29" },
		/* 154 */ { "x" : -469.4723211500618, "y" : -200.79210543630222, "trait" : "line", "color" : "EF7E29" },
		/* 155 */ { "x" : -457.3014196476447, "y" : -174.87166646203974, "trait" : "line", "color" : "EF7E29" },
		/* 156 */ { "x" : -492.9597988814521, "y" : 229.96736330301715, "trait" : "line", "color" : "EF7E29" },
		/* 157 */ { "x" : -477.2090675592799, "y" : 206.8085277410859, "trait" : "line", "color" : "EF7E29" },
		/* 158 */ { "x" : -466.9115327471668, "y" : 188.1916529634423, "trait" : "line", "color" : "EF7E29" },
		/* 159 */ { "x" : -455.08295430734483, "y" : 162.11321872952058, "trait" : "line", "color" : "EF7E29" },
		/* 160 */ { "x" : -446.79714186893466, "y" : 138.56220855331276, "trait" : "line", "color" : "EF7E29" },
		/* 161 */ { "x" : -440.5867054225696, "y" : 111.00824320846532, "trait" : "line", "color" : "EF7E29" },
		/* 162 */ { "x" : -437.86063407766346, "y" : 88.48605930692862, "trait" : "line", "color" : "EF7E29" },
		/* 163 */ { "x" : -436.1595111996012, "y" : 60.47439612353034, "trait" : "line", "color" : "EF7E29" },
		/* 164 */ { "x" : -435.6360681855451, "y" : 8.501558391795015, "trait" : "line", "color" : "EF7E29" },
		/* 165 */ { "x" : -435.4419203601924, "y" : 37.992613062871555, "trait" : "line", "color" : "EF7E29" },
		
		/* 166 */ { "x" : -592, "y" : 2.007812499999993, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "FFFFFF" },
		/* 167 */ { "x" : -592, "y" : -13.9921875, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "FFFFFF" },
		
		/* 168 */ { "x" : -714.2715278479752, "y" : 85.99063504602832, "trait" : "ballArea" },
		
		/* 169 */ { "x" : -715.722625690124, "y" : -97.33139234545078, "trait" : "goalNet", "color" : "FFFFFF", "cMask" : ["red","ball" ] },
		/* 170 */ { "x" : -745.7216858912061, "y" : -97.09393276602268, "trait" : "goalNet", "color" : "FFFFFF", "cMask" : ["blue" ], "bCoef" : 0, "curve" : 0 },
		/* 171 */ { "x" : -745, "y" : 86.22809462545641, "trait" : "goalNet", "color" : "FFFFFF", "cMask" : ["blue" ], "bCoef" : 0, "curve" : 0 },
		/* 172 */ { "x" : -714.2715278479752, "y" : 85.99063504602832, "trait" : "goalNet", "color" : "FFFFFF", "cMask" : ["red","ball" ] },
		
		/* 173 */ { "x" : -714.2715278479752, "y" : 85.99063504602832, "trait" : "fieldArea" },
		
		/* 174 */ { "x" : -715, "y" : 85.99063504602832, "trait" : "line", "color" : "FFFFFF" },
		/* 175 */ { "x" : -715, "y" : -97.33139234545078, "trait" : "line", "color" : "FFFFFF" },
		/* 176 */ { "x" : -715, "y" : -68.68732556553218, "trait" : "line", "color" : "FFFFFF" },
		/* 177 */ { "x" : -715, "y" : 58.49233093730646, "trait" : "line", "color" : "FFFFFF" },
		/* 178 */ { "x" : -729.7221871172956, "y" : -97.22057787505099, "trait" : "line", "color" : "FFFFFF" },
		/* 179 */ { "x" : -732.2709639686243, "y" : 86.13311079368516, "trait" : "line", "color" : "FFFFFF" },
		/* 180 */ { "x" : -715, "y" : 45.96496371697479, "trait" : "line", "color" : "CF0000" },
		/* 181 */ { "x" : -715, "y" : 25.340589543282263, "trait" : "line", "color" : "CF0000" },
		/* 182 */ { "x" : -715, "y" : 0.007812499999992895, "trait" : "line", "color" : "CF0000" },
		/* 183 */ { "x" : -715, "y" : -21.992187500000014, "trait" : "line", "color" : "CF0000" },
		/* 184 */ { "x" : -715, "y" : 85.99063504602832, "trait" : "line", "color" : "CF0000" },
		/* 185 */ { "x" : -715, "y" : 63.609927847103336, "trait" : "line", "color" : "CF0000" },
		/* 186 */ { "x" : -715, "y" : -75.99218750000003, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line", "color" : "CF0000" },
		/* 187 */ { "x" : -715, "y" : -100.07287845559074, "trait" : "line", "color" : "CF0000" },
		/* 188 */ { "x" : -715, "y" : -40.992187500000014, "trait" : "line", "color" : "CF0000" },
		/* 189 */ { "x" : -715, "y" : -55.992187500000014, "trait" : "line", "color" : "CF0000" },
		
		/* 190 */ { "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "x" : -714, "y" : 214.00781250000003, "vis" : false, "curve" : 0 },
		/* 191 */ { "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "x" : -715, "y" : -225.99218750000006, "vis" : false, "curve" : 0 },
		
		/* 192 */ { "x" : -715, "y" : 315, "trait" : "ballArea", "vis" : true, "color" : "ffffff", "curve" : 0, "bCoef" : 1 },
		/* 193 */ { "x" : 592, "y" : 315, "trait" : "ballArea", "vis" : true, "color" : "ffffff", "curve" : 0, "bCoef" : 1 },
		/* 194 */ { "x" : -715, "y" : -325, "trait" : "ballArea", "color" : "ffffff", "vis" : true, "curve" : 0, "bCoef" : 1 },
		/* 195 */ { "x" : 592, "y" : -325, "trait" : "ballArea", "curve" : 0, "vis" : true, "color" : "ffffff", "bCoef" : 1 },
		
		/* 196 */ { "x" : -61, "y" : 350, "trait" : "line", "color" : "EF7E29" },
		/* 197 */ { "x" : -61, "y" : -357, "trait" : "line", "color" : "EF7E29" }

	],

	"segments" : [
		{ "v0" : 0, "v1" : 1, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "x" : -1300, "curve" : 259.83403647248304, "cGroup" : ["blueKO","redKO" ] },
		{ "v0" : 2, "v1" : 3, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "y" : -150 },
		{ "v0" : 4, "v1" : 5, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "y" : 150, "curve" : 0 },
		{ "v0" : 7, "v1" : 8, "vis" : false, "bCoef" : 1000000, "cMask" : ["blue" ], "x" : 1410 },
		
		{ "v0" : 10, "v1" : 11, "curve" : 216, "trait" : "powerboost", "bCoef" : -2.2, "vis" : false, "cMask" : ["ball" ], "pos" : [955,0 ], "radius" : 10 },
		
		{ "v0" : 12, "v1" : 13, "curve" : 0, "vis" : false, "color" : "C7E6BD", "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["redKO" ], "x" : 1134 },
		{ "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "v0" : 14, "v1" : 15 },
		{ "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "v0" : 15, "v1" : 16, "y" : 18 },
		{ "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "v0" : 17, "v1" : 18, "y" : -18 },
		{ "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "v0" : 17, "v1" : 6 },
		{ "vis" : false, "bCoef" : -2.4, "cMask" : ["blue" ], "v0" : 19, "v1" : 20, "x" : 1233.0188554822 },
		{ "curve" : -79.41835780463073, "vis" : false, "bCoef" : 0, "cMask" : ["red" ], "v0" : 21, "v1" : 22 },
		{ "v0" : 23, "v1" : 24, "curve" : 0, "vis" : false, "color" : "C7E6BD", "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "x" : 1134, "radius" : 15, "pos" : [67,0 ], "_selected" : true },
		
		{ "v0" : 27, "v1" : 28, "curve" : 0, "vis" : true, "color" : "FFFFFF", "trait" : "line" },
		
		{ "v0" : 36, "v1" : 37, "curve" : 0, "vis" : true, "color" : "FFFFFF", "cMask" : ["ball" ], "trait" : "ballArea", "bCoef" : 1 },
		{ "v0" : 38, "v1" : 39, "vis" : true, "color" : "FFFFFF", "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "bCoef" : 1 },
		
		{ "v0" : 40, "v1" : 41, "curve" : 85, "vis" : true, "color" : "2CAAFF", "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ] },
		{ "v0" : 42, "v1" : 43, "curve" : -85, "vis" : true, "color" : "2CAAFF", "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ] },
		{ "v0" : 41, "v1" : 43, "curve" : 8, "vis" : true, "color" : "2CAAFF", "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ] },
		
		{ "v0" : 26, "v1" : 44, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 48, "v1" : 45, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 49, "v1" : 62, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 51, "v1" : 54, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 55, "v1" : 60, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 61, "v1" : 52, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 53, "v1" : 63, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 59, "v1" : 57, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 58, "v1" : 56, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 50, "v1" : 64, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 65, "v1" : 66, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 60, "v1" : 60, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 67, "v1" : 68, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 69, "v1" : 70, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 71, "v1" : 72, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 73, "v1" : 74, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 75, "v1" : 76, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 77, "v1" : 78, "curve" : 0, "vis" : true, "color" : "FFFFFF", "trait" : "line" },
		
		{ "v0" : 80, "v1" : 81, "color" : "FFFFFF", "trait" : "goalNet", "cMask" : ["blue","ball" ] },
		{ "v0" : 81, "v1" : 82, "curve" : 0, "color" : "FFFFFF", "trait" : "goalNet", "cMask" : ["red" ], "bCoef" : 0 },
		{ "v0" : 82, "v1" : 83, "color" : "FFFFFF", "trait" : "goalNet", "cMask" : ["blue","ball" ] },
		
		{ "v0" : 86, "v1" : 85, "curve" : 0, "vis" : true, "color" : "FFFFFF", "trait" : "line" },
		{ "v0" : 87, "v1" : 89, "curve" : 0, "vis" : true, "color" : "FFFFFF", "trait" : "line" },
		{ "v0" : 88, "v1" : 90, "curve" : 0, "vis" : true, "color" : "FFFFFF", "trait" : "line" },
		{ "v0" : 91, "v1" : 92, "curve" : 0, "vis" : true, "color" : "FFFFFF", "trait" : "line" },
		{ "v0" : 93, "v1" : 94, "curve" : 0, "vis" : true, "color" : "FFFFFF", "trait" : "line" },
		{ "v0" : 95, "v1" : 96, "curve" : 0, "vis" : true, "color" : "FFFFFF", "trait" : "line" },
		{ "v0" : 97, "v1" : 98, "curve" : 0, "vis" : true, "color" : "FFFFFF", "trait" : "line" },
		{ "v0" : 99, "v1" : 100, "curve" : 0, "vis" : true, "color" : "CF0000", "trait" : "line" },
		{ "v0" : 101, "v1" : 102, "curve" : 0, "vis" : true, "color" : "CF0000", "trait" : "line" },
		{ "v0" : 103, "v1" : 104, "curve" : 0, "vis" : true, "color" : "CF0000", "trait" : "line" },
		{ "v0" : 105, "v1" : 106, "curve" : 0, "vis" : true, "color" : "CF0000", "trait" : "line" },
		{ "v0" : 107, "v1" : 108, "curve" : 0, "vis" : true, "color" : "CF0000", "trait" : "line" },
		{ "vis" : true, "color" : "EF7E29", "trait" : "line", "v0" : 112, "v1" : 113, "curve" : 180 },
		{ "vis" : true, "color" : "EF7E29", "trait" : "line", "v0" : 113, "v1" : 112, "curve" : 184.01604679055436 },
		
		{ "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "v0" : 18, "v1" : 82, "x" : 1180 },
		{ "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "v0" : 16, "v1" : 114, "x" : 1180 },
		
		{ "v0" : 117, "v1" : 118, "curve" : 0, "vis" : true, "color" : "FFFFFF", "trait" : "line" },
		
		{ "v0" : 126, "v1" : 127, "curve" : 0, "vis" : true, "color" : "FFFFFF", "cMask" : ["ball" ], "trait" : "ballArea", "bCoef" : 1 },
		{ "v0" : 128, "v1" : 129, "vis" : true, "color" : "FFFFFF", "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "bCoef" : 1 },
		
		{ "v0" : 130, "v1" : 131, "curve" : 85, "vis" : true, "color" : "2CAAFF", "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ] },
		{ "v0" : 132, "v1" : 133, "curve" : -85, "vis" : true, "color" : "2CAAFF", "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ] },
		{ "v0" : 131, "v1" : 133, "curve" : 8, "vis" : true, "color" : "2CAAFF", "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ] },
		
		{ "v0" : 116, "v1" : 134, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 137, "v1" : 135, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 138, "v1" : 151, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 140, "v1" : 143, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 144, "v1" : 149, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 150, "v1" : 141, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 142, "v1" : 152, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 148, "v1" : 146, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 147, "v1" : 145, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 139, "v1" : 153, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 154, "v1" : 155, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 149, "v1" : 149, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 156, "v1" : 157, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 158, "v1" : 159, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 160, "v1" : 161, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 162, "v1" : 163, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 164, "v1" : 165, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "line" },
		{ "v0" : 166, "v1" : 167, "curve" : 0, "vis" : true, "color" : "FFFFFF", "trait" : "line" },
		
		{ "v0" : 169, "v1" : 170, "color" : "FFFFFF", "trait" : "goalNet", "cMask" : ["red","ball" ] },
		{ "v0" : 170, "v1" : 171, "curve" : 0, "color" : "FFFFFF", "trait" : "goalNet", "cMask" : ["blue" ], "bCoef" : 0 },
		{ "v0" : 171, "v1" : 172, "color" : "FFFFFF", "trait" : "goalNet", "cMask" : ["red","ball" ] },
		
		{ "v0" : 175, "v1" : 174, "curve" : 0, "vis" : true, "color" : "FFFFFF", "trait" : "line" },
		{ "v0" : 176, "v1" : 178, "curve" : 0, "vis" : true, "color" : "FFFFFF", "trait" : "line" },
		{ "v0" : 177, "v1" : 179, "curve" : 0, "vis" : true, "color" : "FFFFFF", "trait" : "line" },
		{ "v0" : 180, "v1" : 181, "curve" : 0, "vis" : true, "color" : "CF0000", "trait" : "line" },
		{ "v0" : 182, "v1" : 183, "curve" : 0, "vis" : true, "color" : "CF0000", "trait" : "line" },
		{ "v0" : 184, "v1" : 185, "curve" : 0, "vis" : true, "color" : "CF0000", "trait" : "line" },
		{ "v0" : 186, "v1" : 187, "curve" : 0, "vis" : true, "color" : "CF0000", "trait" : "line" },
		{ "v0" : 188, "v1" : 189, "curve" : 0, "vis" : true, "color" : "CF0000", "trait" : "line" },
		
		{ "v0" : 193, "v1" : 192, "curve" : 0, "vis" : true, "color" : "ffffff", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "y" : 290 },
		{ "v0" : 194, "v1" : 195, "vis" : true, "color" : "ffffff", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "y" : -320, "curve" : 0.09261129897399809 },
		
		{ "v0" : 196, "v1" : 197, "color" : "EF7E29", "trait" : "line", "x" : 840 }

	],

	"goals" : [
		{ "p0" : [592.1393591516376,-96.47239042901694 ], "p1" : [308.5412460785576,8.46728888038227 ], "team" : "red" },
		{ "p0" : [596.0888745458144,91.95874017803774 ], "p1" : [298.51678185229196,-23.848942732672967 ], "team" : "red" },
		{ "p0" : [602,-97.986883372199 ], "p1" : [602,92.011511591401 ], "team" : "blue" },
		{ "p0" : [-725,87.99469587219902 ], "p1" : [-725,-102.00369909140105 ], "team" : "red" }

	],

	"discs" : [
		{ "radius" : 5.352099039641226, "pos" : [592,-95.9828225460283 ], "color" : "FFFFFF", "cMask" : ["ball","blue","red" ], "trait" : "goalPost", "vis" : false },
		{ "radius" : 5.352099039641226, "pos" : [592,87.33920484545074 ], "color" : "FFFFFF", "bCoef" : 2, "cMask" : ["ball","blue","red" ], "trait" : "goalPost", "vis" : false },
		{ "radius" : 1.3, "invMass" : 0, "pos" : [622,-96 ], "color" : "000003", "cMask" : ["ball" ], "damping" : 0, "trait" : "goalPost", "bCoef" : 0 },
		{ "radius" : 1.3, "invMass" : 0, "pos" : [623,87 ], "color" : "000004", "cMask" : ["ball" ], "damping" : 0, "trait" : "goalPost", "bCoef" : 0 },
		
		{ "radius" : 4, "invMass" : 1.5, "pos" : [630,-86 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [633,-70 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [636,-56 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [635,-39 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [636,-22 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [635,-8 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [635,11 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [635,32 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [635,47 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [634,63 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [632,79 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		
		{ "radius" : 5.352099039641226, "pos" : [-715,85.99063504602832 ], "color" : "FFFFFF", "cMask" : ["ball","blue","red" ], "trait" : "goalPost", "vis" : false },
		{ "radius" : 5.352099039641226, "pos" : [-715,-97.33139234545078 ], "color" : "FFFFFF", "bCoef" : 2, "cMask" : ["ball","blue","red" ], "trait" : "goalPost", "vis" : false },
		{ "radius" : 1.3, "invMass" : 0, "pos" : [-745,86.00781250000001 ], "color" : "000003", "cMask" : ["ball" ], "damping" : 0, "trait" : "goalPost", "bCoef" : 0 },
		{ "radius" : 1.3, "invMass" : 0, "pos" : [-746,-96.99218750000003 ], "color" : "000004", "cMask" : ["ball" ], "damping" : 0, "trait" : "goalPost", "bCoef" : 0 },
		
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-753,76.0078125 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-756,60.0078125 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-759,46.0078125 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-758,29.0078125 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-759,12.0078125 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-758,-1.992187500000007 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-758,-20.992187500000014 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-758,-41.992187500000014 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-758,-56.992187500000014 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-757,-72.99218750000003 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-755,-88.99218750000003 ], "color" : "FFFFFF", "cMask" : ["ball" ], "damping" : 0.96 }

	],

	"joints" : [
		{ "d0" : 3, "d1" : 5, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 5, "d1" : 6, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 6, "d1" : 7, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 7, "d1" : 8, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 8, "d1" : 9, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 9, "d1" : 10, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 10, "d1" : 11, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 11, "d1" : 12, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 12, "d1" : 13, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 13, "d1" : 14, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 14, "d1" : 15, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 15, "d1" : 4, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 18, "d1" : 20, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 20, "d1" : 21, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 21, "d1" : 22, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 22, "d1" : 23, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 23, "d1" : 24, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 24, "d1" : 25, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 25, "d1" : 26, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 26, "d1" : 27, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 27, "d1" : 28, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 28, "d1" : 29, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 29, "d1" : 30, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 30, "d1" : 19, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" }
	],

	"planes" : [
		{ "normal" : [0,1 ], "dist" : -328, "bCoef" : 0, "trait" : "ballArea" },
		{ "normal" : [0,-1 ], "dist" : -320, "bCoef" : 0, "trait" : "ballArea" },
		
		{ "normal" : [0,1 ], "dist" : -368, "bCoef" : 0 },
		{ "normal" : [0,-1 ], "dist" : -355, "bCoef" : 0 },
		{ "normal" : [1,0 ], "dist" : -1767, "bCoef" : 0, "cMask" : ["ball" ] },
		{ "normal" : [-1,0 ], "dist" : -653, "bCoef" : 0, "cMask" : ["ball" ] },
		{ "normal" : [1,0 ], "dist" : -185, "bCoef" : 0 },
		{ "normal" : [-1,0 ], "dist" : -902, "bCoef" : 0 }

	],

	"traits" : {
		"ballArea" : { "vis" : false, "bCoef" : 0, "cMask" : ["ball" ] },
		"goalPost" : { "radius" : 5, "invMass" : 0, "bCoef" : 2 },
		"stanchion" : { "radius" : 3, "invMass" : 0, "bCoef" : 3, "cMask" : ["none" ] },
		"cornerflag" : { "radius" : 3, "invMass" : 0, "bCoef" : 0.5, "color" : "FFFF00", "cGroup" : [ ] },
		"reargoalNetleft" : { "vis" : true, "bCoef" : 0.1, "cMask" : ["ball","red","blue" ], "curve" : 10, "color" : "C7E6BD" },
		"reargoalNetright" : { "vis" : true, "bCoef" : 0.1, "cMask" : ["ball","red","blue" ], "curve" : -10, "color" : "C7E6BD" },
		"sidegoalNet" : { "vis" : true, "bCoef" : 1, "cMask" : ["ball","red","blue" ], "color" : "C7E6BD" },
		"kickOffBarrier" : { "vis" : false, "bCoef" : 0.1, "cGroup" : ["redKO","blueKO" ], "cMask" : ["red","blue" ] },
		"line" : { "vis" : true, "cMask" : [ ], "color" : "C7E6BD" },
		"tunnel" : { "vis" : true, "cMask" : ["red","blue" ], "color" : "000000" },
		"advertising" : { "vis" : true, "cMask" : ["red","blue" ], "color" : "333333" },
		"teambench" : { "vis" : true, "cMask" : [ ], "color" : "000000" },
		"manager" : { "radius" : 15, "vis" : true, "cMask" : ["red","blue" ], "invMass" : 0, "color" : "333333" },
		"physio" : { "radius" : 15, "vis" : true, "cMask" : ["red","blue" ], "invMass" : 0, "color" : "666666" },
		"redsubs" : { "radius" : 15, "vis" : true, "cMask" : ["red","blue" ], "invMass" : 0, "color" : "E56E56" },
		"bluesubs" : { "radius" : 15, "vis" : true, "cMask" : ["red","blue" ], "invMass" : 0, "color" : "5689E5" }

	}
}`;
var PensRedFutsalx3x4=`
{

	"name" : "ᴘᴇɴᴀʟᴛʏ ʀᴇᴅ ᴛᴇᴀᴍ 🔴 | 𝐆𝐋𝐇 ( 𝐹𝑢𝑡𝑠𝑎𝑙 𝑥3 / 𝑥4 )",

	"width" : 800,

	"height" : 270,

	"spawnDistance" : 300,

	"redSpawnPoints" : [
		[ 88, -90
		],
		[ 88, -30
		],
		[ 88, 30
		],
		[ 88, 90
		]

	],

	"blueSpawnPoints" : [
		[ 735, -90
		],
		[ 735, -30
		],
		[ 735, 30
		],
		[ 735, 90
		]

	],

	"bg" : { "type" : "hockey", "width" : 550, "height" : 240, "kickOffRadius" : 0, "cornerRadius" : 0, "color" : "253D97" },

	"playerPhysics" : {
		"bCoef" : 0.5,
		"invMass" : 0.5,
		"damping" : 0.96,
		"acceleration" : 0.12,
		"kickingAcceleration" : 0.07,
		"kickingDamping" : 0.96,
		"kickStrength" : 5.65

	},

	"ballPhysics" : {
		"pos" : [ 376, 0
		],
		"radius" : 6.25,
		"color" : "fff100"

	},

	"vertexes" : [
		/* 0 */ { "x" : -219, "y" : -138, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["blueKO","redKO" ], "curve" : 235 },
		/* 1 */ { "x" : -221, "y" : 135, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["blueKO","redKO" ], "curve" : 235 },
		/* 2 */ { "x" : 892, "y" : -151, "bCoef" : 0, "cMask" : ["blue" ], "dist" : -1400 },
		/* 3 */ { "x" : 702, "y" : -152, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 4 */ { "x" : 702, "y" : 148, "bCoef" : 0, "cMask" : ["blue" ], "curve" : 0 },
		/* 5 */ { "x" : 891, "y" : 148, "bCoef" : 0, "cMask" : ["blue" ], "dist" : -1400, "curve" : 0 },
		
		/* 6 */ { "x" : 697, "y" : -152, "trait" : "kickOffBarrier", "cMask" : ["blue" ] },
		
		/* 7 */ { "x" : 813, "y" : -121, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 8 */ { "x" : 813, "y" : 119, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 9 */ { "x" : -522.9395376326441, "y" : 735, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		
		/* 10 */ { "x" : 373, "y" : -6.25, "trait" : "powerboost", "bCoef" : -2.2, "vis" : false, "cMask" : ["ball" ], "pos" : [955,0 ], "radius" : 10, "curve" : 216 },
		/* 11 */ { "x" : 373, "y" : 6.25, "trait" : "powerboost", "bCoef" : -2.2, "vis" : false, "cMask" : ["ball" ], "pos" : [955,0 ], "radius" : 10, "curve" : 216 },
		
		/* 12 */ { "x" : 531, "y" : 115.23596984067328, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["redKO" ], "vis" : false, "curve" : 0 },
		/* 13 */ { "x" : 531, "y" : -124.76361382468701, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["redKO" ], "vis" : false, "curve" : 0 },
		/* 14 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 697, "y" : 148 },
		/* 15 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 697, "y" : 16 },
		/* 16 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 590, "y" : 16 },
		/* 17 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 697, "y" : -20 },
		/* 18 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 590, "y" : -20 },
		/* 19 */ { "bCoef" : -2.4, "cMask" : ["blue" ], "x" : 661.0188554822, "y" : 63.50390625 },
		/* 20 */ { "bCoef" : -2.4, "cMask" : ["blue" ], "x" : 661.0188554822, "y" : -67.49609375 },
		/* 21 */ { "bCoef" : 0, "cMask" : ["red" ], "x" : 132, "y" : 619, "curve" : -77 },
		/* 22 */ { "bCoef" : 0, "cMask" : ["red" ], "x" : 132, "y" : -621, "curve" : -77 },
		/* 23 */ { "x" : 531, "y" : 115.23596984067328, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "vis" : false, "curve" : 0, "radius" : 15, "pos" : [67,0 ] },
		/* 24 */ { "x" : 531, "y" : -124.76361382468701, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "vis" : false, "curve" : 0, "radius" : 15, "pos" : [67,0 ] },
		
		/* 25 */ { "x" : 590, "y" : -92.2202821254564, "trait" : "goalNet", "color" : "FFFFFF", "cMask" : ["blue" ], "bCoef" : 0, "curve" : 0 },
		
		/* 26 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 590, "y" : 86.00390625 },
		
		/* 27 */ { "x" : 550, "y" : 239, "trait" : "ballArea" },
		/* 28 */ { "x" : 550, "y" : -241, "trait" : "ballArea" },
		
		/* 29 */ { "x" : -550, "y" : -81, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [-700,-80 ] },
		/* 30 */ { "x" : -590, "y" : -81, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [-700,-80 ] },
		/* 31 */ { "x" : -590, "y" : 79, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [-700,80 ] },
		/* 32 */ { "x" : -550, "y" : 79, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [-700,80 ] },
		/* 33 */ { "x" : 550, "y" : -81, "cMask" : ["blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [700,-80 ], "bCoef" : 0.1 },
		/* 34 */ { "x" : 590, "y" : -81, "cMask" : ["blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [700,-80 ], "bCoef" : 0.1 },
		/* 35 */ { "x" : 590, "y" : 79, "cMask" : ["blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [700,80 ], "bCoef" : 0.1 },
		/* 36 */ { "x" : 550, "y" : 79, "cMask" : ["blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [700,80 ], "bCoef" : 0.1 },
		
		/* 37 */ { "x" : -550, "y" : 79, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [-700,80 ] },
		/* 38 */ { "x" : -550, "y" : 239, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8" },
		/* 39 */ { "x" : -550, "y" : -81, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [-700,-80 ] },
		/* 40 */ { "x" : -550, "y" : -241, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8" },
		/* 41 */ { "x" : -550, "y" : 240, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea" },
		/* 42 */ { "x" : 550, "y" : 240, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea" },
		/* 43 */ { "x" : 550, "y" : 79, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "pos" : [700,80 ] },
		/* 44 */ { "x" : 550, "y" : 239, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea" },
		/* 45 */ { "x" : 550, "y" : -241, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8" },
		/* 46 */ { "x" : 550, "y" : -81, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [700,-80 ] },
		/* 47 */ { "x" : 550, "y" : -241, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea" },
		/* 48 */ { "x" : 550, "y" : -241, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea" },
		/* 49 */ { "x" : -550, "y" : -240, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0 },
		/* 50 */ { "x" : 550, "y" : -240, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0 },
		/* 51 */ { "x" : -557.5, "y" : 79, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "vis" : false, "pos" : [-700,80 ] },
		/* 52 */ { "x" : -557.5, "y" : 239, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "vis" : false },
		/* 53 */ { "x" : -557.5, "y" : -241, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false, "curve" : 0 },
		/* 54 */ { "x" : -557.5, "y" : -81, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false, "curve" : 0, "pos" : [-700,-80 ] },
		
		/* 55 */ { "x" : 0, "y" : -80, "bCoef" : 0.1, "trait" : "line", "curve" : -180 },
		/* 56 */ { "x" : 0, "y" : 80, "bCoef" : 0.1, "trait" : "line", "curve" : -180 },
		/* 57 */ { "x" : -550, "y" : -81, "bCoef" : 0.1, "trait" : "line" },
		/* 58 */ { "x" : -550, "y" : 79, "bCoef" : 0.1, "trait" : "line" },
		/* 59 */ { "x" : 550, "y" : -81, "bCoef" : 0.1, "trait" : "line" },
		/* 60 */ { "x" : 550, "y" : 79, "bCoef" : 0.1, "trait" : "line" },
		/* 61 */ { "x" : -550, "y" : 199, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : -90 },
		/* 62 */ { "x" : -390, "y" : 69, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 0 },
		/* 63 */ { "x" : -550, "y" : 225, "bCoef" : 0.1, "trait" : "line", "curve" : -90 },
		/* 64 */ { "x" : -536, "y" : 239, "bCoef" : 0.1, "trait" : "line", "curve" : -90 },
		/* 65 */ { "x" : -550, "y" : -201, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 90 },
		/* 66 */ { "x" : -390, "y" : -71, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 0 },
		/* 67 */ { "x" : -550, "y" : -227, "bCoef" : 0.1, "trait" : "line", "curve" : 90 },
		/* 68 */ { "x" : -536, "y" : -241, "bCoef" : 0.1, "trait" : "line", "curve" : 90 },
		/* 69 */ { "x" : -381, "y" : -241, "bCoef" : 0.1, "trait" : "line" },
		/* 70 */ { "x" : 550, "y" : -227, "bCoef" : 0.1, "trait" : "line", "curve" : -90 },
		/* 71 */ { "x" : 536, "y" : -240, "bCoef" : 0.1, "trait" : "line", "curve" : -90 },
		/* 72 */ { "x" : 550, "y" : 225, "bCoef" : 0.1, "trait" : "line", "curve" : 90 },
		/* 73 */ { "x" : 536, "y" : 240, "bCoef" : 0.1, "trait" : "line", "curve" : 90 },
		/* 74 */ { "x" : 550, "y" : 199, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 90 },
		/* 75 */ { "x" : 390, "y" : 69, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 90 },
		/* 76 */ { "x" : 550, "y" : -201, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : -90 },
		/* 77 */ { "x" : 390, "y" : -71, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : -90 },
		/* 78 */ { "x" : 390, "y" : 69, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 0 },
		/* 79 */ { "x" : 390, "y" : -71, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 0 },
		/* 80 */ { "x" : -375, "y" : 0, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 81 */ { "x" : -375, "y" : -2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 82 */ { "x" : -375, "y" : 2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 83 */ { "x" : -375, "y" : -4, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 84 */ { "x" : -375, "y" : -3, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 85 */ { "x" : -375, "y" : 1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 86 */ { "x" : -375, "y" : -4.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 87 */ { "x" : -375, "y" : 2.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 88 */ { "x" : 375, "y" : 0, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 89 */ { "x" : 375, "y" : -2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 90 */ { "x" : 375, "y" : 2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 91 */ { "x" : 375, "y" : -4, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 92 */ { "x" : 375, "y" : -3, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 93 */ { "x" : 375, "y" : 1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 94 */ { "x" : 375, "y" : -4.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 95 */ { "x" : 375, "y" : 2.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 96 */ { "x" : -277.5, "y" : 0, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 97 */ { "x" : -277.5, "y" : -2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 98 */ { "x" : -277.5, "y" : 2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 99 */ { "x" : -277.5, "y" : -4, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 100 */ { "x" : -277.5, "y" : -3, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 101 */ { "x" : -277.5, "y" : 1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 102 */ { "x" : -277.5, "y" : -4.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 103 */ { "x" : -277.5, "y" : 2.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 104 */ { "x" : 277.5, "y" : 0, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 105 */ { "x" : 277.5, "y" : -2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 106 */ { "x" : 277.5, "y" : 2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 107 */ { "x" : 277.5, "y" : -4, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 108 */ { "x" : 277.5, "y" : -3, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 109 */ { "x" : 277.5, "y" : 1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 110 */ { "x" : 277.5, "y" : -4.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 111 */ { "x" : 277.5, "y" : 2.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 112 */ { "x" : -240, "y" : 223, "bCoef" : 0.1, "trait" : "line" },
		/* 113 */ { "x" : -240, "y" : 255, "bCoef" : 0.1, "trait" : "line" },
		/* 114 */ { "x" : -120, "y" : 223, "bCoef" : 0.1, "trait" : "line" },
		/* 115 */ { "x" : -120, "y" : 255, "bCoef" : 0.1, "trait" : "line" },
		/* 116 */ { "x" : 240, "y" : 223, "bCoef" : 0.1, "trait" : "line" },
		/* 117 */ { "x" : 240, "y" : 255, "bCoef" : 0.1, "trait" : "line" },
		/* 118 */ { "x" : 120, "y" : 223, "bCoef" : 0.1, "trait" : "line" },
		/* 119 */ { "x" : 120, "y" : 255, "bCoef" : 0.1, "trait" : "line" },
		/* 120 */ { "x" : -381, "y" : 239, "bCoef" : 0.1, "trait" : "line" },
		/* 121 */ { "x" : -381, "y" : 255, "bCoef" : 0.1, "trait" : "line" },
		/* 122 */ { "x" : -556, "y" : 122, "bCoef" : 0.1, "trait" : "line" },
		/* 123 */ { "x" : -575, "y" : 122, "bCoef" : 0.1, "trait" : "line" },
		/* 124 */ { "x" : 556, "y" : 122, "bCoef" : 0.1, "trait" : "line" },
		/* 125 */ { "x" : 575, "y" : 122, "bCoef" : 0.1, "trait" : "line" },
		/* 126 */ { "x" : -556, "y" : -124, "bCoef" : 0.1, "trait" : "line" },
		/* 127 */ { "x" : -575, "y" : -124, "bCoef" : 0.1, "trait" : "line" },
		/* 128 */ { "x" : 556, "y" : -124, "bCoef" : 0.1, "trait" : "line" },
		/* 129 */ { "x" : 575, "y" : -124, "bCoef" : 0.1, "trait" : "line" },
		/* 130 */ { "x" : -381, "y" : -241, "bCoef" : 0.1, "trait" : "line" },
		/* 131 */ { "x" : -381, "y" : -257, "bCoef" : 0.1, "trait" : "line" },
		/* 132 */ { "x" : 381, "y" : 239, "bCoef" : 0.1, "trait" : "line" },
		/* 133 */ { "x" : 381, "y" : 255, "bCoef" : 0.1, "trait" : "line" },
		/* 134 */ { "x" : 381, "y" : -241, "bCoef" : 0.1, "trait" : "line" },
		/* 135 */ { "x" : 381, "y" : -257, "bCoef" : 0.1, "trait" : "line" },
		
		/* 136 */ { "x" : -553, "y" : 79, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [-700,80 ], "vis" : false },
		/* 137 */ { "x" : -553, "y" : 239, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "vis" : false },
		/* 138 */ { "x" : -553, "y" : -81, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [-700,-80 ], "vis" : false },
		/* 139 */ { "x" : -553, "y" : -241, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "vis" : false },
		
		/* 140 */ { "bCoef" : 0.1, "trait" : "line", "x" : 0, "y" : 269.75390625 },
		/* 141 */ { "bCoef" : 0.1, "trait" : "line", "x" : 0, "y" : -271.24609375 }

	],

	"segments" : [
		{ "v0" : 0, "v1" : 1, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "x" : -1300, "curve" : 259.83403647248304, "cGroup" : ["blueKO","redKO" ] },
		{ "v0" : 2, "v1" : 3, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "y" : -150 },
		{ "v0" : 4, "v1" : 5, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "y" : 150, "curve" : 0 },
		{ "v0" : 7, "v1" : 8, "vis" : false, "bCoef" : 1000000, "cMask" : ["blue" ], "x" : 1410 },
		
		{ "v0" : 10, "v1" : 11, "curve" : 240.69576377250274, "trait" : "powerboost", "bCoef" : -2.2, "vis" : false, "cMask" : ["ball" ], "pos" : [955,0 ], "radius" : 10 },
		
		{ "v0" : 12, "v1" : 13, "curve" : 0, "vis" : false, "color" : "C7E6BD", "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["redKO" ], "x" : 1134 },
		{ "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "v0" : 14, "v1" : 15 },
		{ "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "v0" : 15, "v1" : 16, "y" : 18 },
		{ "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "v0" : 17, "v1" : 18, "y" : -18 },
		{ "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "v0" : 17, "v1" : 6 },
		{ "vis" : false, "bCoef" : -2.4, "cMask" : ["blue" ], "v0" : 19, "v1" : 20, "x" : 1233.0188554822 },
		{ "curve" : -86.23178411629446, "vis" : false, "bCoef" : 0, "cMask" : ["red" ], "v0" : 21, "v1" : 22 },
		{ "v0" : 23, "v1" : 24, "curve" : 0, "vis" : false, "color" : "C7E6BD", "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "x" : 1134, "radius" : 15, "pos" : [67,0 ] },
		{ "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "v0" : 18, "v1" : 25, "x" : 1180 },
		{ "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "v0" : 16, "v1" : 26, "x" : 1180 },
		
		{ "v0" : 29, "v1" : 30, "curve" : 0, "color" : "F8F8F8", "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "pos" : [-700,-80 ], "y" : -80 },
		{ "v0" : 30, "v1" : 31, "color" : "F8F8F8", "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "x" : -590 },
		{ "v0" : 31, "v1" : 32, "curve" : 0, "color" : "F8F8F8", "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "pos" : [-700,80 ], "y" : 80 },
		{ "v0" : 33, "v1" : 34, "curve" : 0, "color" : "F8F8F8", "cMask" : ["blue","ball" ], "trait" : "goalNet", "pos" : [700,-80 ], "y" : -80, "bCoef" : 0.1 },
		{ "v0" : 34, "v1" : 35, "color" : "F8F8F8", "cMask" : ["ball" ], "trait" : "goalNet", "x" : 590, "curve" : 0, "bCoef" : 0.1 },
		{ "v0" : 35, "v1" : 36, "curve" : 0, "color" : "F8F8F8", "cMask" : ["blue","ball" ], "trait" : "goalNet", "pos" : [700,80 ], "y" : 80, "bCoef" : 0.1 },
		
		{ "v0" : 37, "v1" : 38, "vis" : true, "color" : "F8F8F8", "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -550 },
		{ "v0" : 39, "v1" : 40, "vis" : true, "color" : "F8F8F8", "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -550 },
		{ "v0" : 41, "v1" : 42, "vis" : true, "color" : "F8F8F8", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "y" : 240 },
		{ "v0" : 43, "v1" : 44, "vis" : true, "color" : "F8F8F8", "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 550 },
		{ "v0" : 45, "v1" : 46, "vis" : true, "color" : "F8F8F8", "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 550 },
		{ "v0" : 47, "v1" : 48, "vis" : true, "color" : "F8F8F8", "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 550, "y" : -240 },
		{ "v0" : 49, "v1" : 50, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "y" : -240 },
		{ "v0" : 51, "v1" : 52, "curve" : 0, "vis" : false, "color" : "F8F8F8", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -557.5 },
		{ "v0" : 53, "v1" : 54, "curve" : 0, "vis" : false, "color" : "F8F8F8", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -557.5 },
		
		{ "v0" : 55, "v1" : 56, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 0 },
		{ "v0" : 57, "v1" : 58, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -550 },
		{ "v0" : 59, "v1" : 60, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 550 },
		{ "v0" : 61, "v1" : 62, "curve" : -90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 64, "v1" : 63, "curve" : -90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 65, "v1" : 66, "curve" : 90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 62, "v1" : 66, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 68, "v1" : 67, "curve" : 90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 71, "v1" : 70, "curve" : -90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 73, "v1" : 72, "curve" : 90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 74, "v1" : 75, "curve" : 90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 76, "v1" : 77, "curve" : -90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 78, "v1" : 79, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 390 },
		{ "v0" : 81, "v1" : 80, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 80, "v1" : 81, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 83, "v1" : 82, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 82, "v1" : 83, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 85, "v1" : 84, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 84, "v1" : 85, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 87, "v1" : 86, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 86, "v1" : 87, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 89, "v1" : 88, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 88, "v1" : 89, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 91, "v1" : 90, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 90, "v1" : 91, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 93, "v1" : 92, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 92, "v1" : 93, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 95, "v1" : 94, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 94, "v1" : 95, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 97, "v1" : 96, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 96, "v1" : 97, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 99, "v1" : 98, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 98, "v1" : 99, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 101, "v1" : 100, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 100, "v1" : 101, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 103, "v1" : 102, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 102, "v1" : 103, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 105, "v1" : 104, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 104, "v1" : 105, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 107, "v1" : 106, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 106, "v1" : 107, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 109, "v1" : 108, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 108, "v1" : 109, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 111, "v1" : 110, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 110, "v1" : 111, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 112, "v1" : 113, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -240 },
		{ "v0" : 114, "v1" : 115, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -120 },
		{ "v0" : 116, "v1" : 117, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 240 },
		{ "v0" : 118, "v1" : 119, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 120 },
		{ "v0" : 120, "v1" : 121, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -381 },
		{ "v0" : 122, "v1" : 123, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -240, "y" : 123 },
		{ "v0" : 124, "v1" : 125, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -240, "y" : 123 },
		{ "v0" : 126, "v1" : 127, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -240, "y" : -123 },
		{ "v0" : 128, "v1" : 129, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -240, "y" : -123 },
		{ "v0" : 130, "v1" : 131, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -381 },
		{ "v0" : 132, "v1" : 133, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 381 },
		{ "v0" : 134, "v1" : 135, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 381 },
		
		{ "v0" : 136, "v1" : 137, "vis" : false, "color" : "F8F8F8", "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -553 },
		{ "v0" : 138, "v1" : 139, "vis" : false, "color" : "F8F8F8", "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -553 },
		
		{ "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "v0" : 56, "v1" : 140 },
		{ "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "v0" : 55, "v1" : 141 },
		{ "curve" : -180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "v0" : 55, "v1" : 56 },
		{ "curve" : -180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "v0" : 56, "v1" : 55 }

	],

	"goals" : [
		{ "p0" : [551.1393591516376,-79.47239042901694 ], "p1" : [267.5412460785576,25.46728888038227 ], "team" : "red" },
		{ "p0" : [557.0888745458144,85.95874017803774 ], "p1" : [259.51678185229196,-29.848942732672967 ], "team" : "red" },
		{ "p0" : [-556.25,-81 ], "p1" : [-556.25,79 ], "team" : "red" },
		{ "p0" : [556.25,79 ], "p1" : [556.25,-81 ], "team" : "blue" }

	],

	"discs" : [
		{ "radius" : 5, "pos" : [-550,79 ], "color" : "6666CC", "trait" : "goalPost", "y" : 80 },
		{ "radius" : 5, "pos" : [-550,-81 ], "color" : "6666CC", "trait" : "goalPost", "y" : -80, "x" : -560 },
		{ "radius" : 5, "pos" : [550,80 ], "color" : "6666CC", "trait" : "goalPost", "y" : 80 },
		{ "radius" : 5, "pos" : [550,-80 ], "color" : "6666CC", "trait" : "goalPost", "y" : -80 },
		
		{ "radius" : 3, "invMass" : 0, "pos" : [-550,239 ], "color" : "FFCC00", "bCoef" : 0.1, "trait" : "line" },
		{ "radius" : 3, "invMass" : 0, "pos" : [-550,-241 ], "color" : "FFCC00", "bCoef" : 0.1, "trait" : "line" },
		{ "radius" : 3, "invMass" : 0, "pos" : [550,-240 ], "color" : "FFCC00", "bCoef" : 0.1, "trait" : "line" },
		{ "radius" : 3, "invMass" : 0, "pos" : [550,240 ], "color" : "FFCC00", "bCoef" : 0.1, "trait" : "line" }

	],

	"planes" : [
		{ "normal" : [1,0 ], "dist" : -1812, "bCoef" : 0, "cMask" : ["ball" ] },
		{ "normal" : [-1,0 ], "dist" : -608, "bCoef" : 0, "cMask" : ["ball" ] },
		{ "normal" : [1,0 ], "dist" : -230, "bCoef" : 0 },
		{ "normal" : [-1,0 ], "dist" : -857, "bCoef" : 0 },
		
		{ "normal" : [0,1 ], "dist" : -241, "bCoef" : 1, "trait" : "ballArea", "vis" : false, "curve" : 0 },
		{ "normal" : [0,-1 ], "dist" : -240, "bCoef" : 1, "trait" : "ballArea" },
		
		{ "normal" : [0,1 ], "dist" : -271, "bCoef" : 0.1 },
		{ "normal" : [0,-1 ], "dist" : -269, "bCoef" : 0.1 },
		
		{ "normal" : [1,0 ], "dist" : -622, "bCoef" : 0.1, "trait" : "ballArea", "vis" : false, "curve" : 0 }

	],

	"traits" : {
		"ballArea" : { "vis" : false, "bCoef" : 0, "cMask" : ["ball" ] },
		"goalPost" : { "radius" : 5, "invMass" : 0, "bCoef" : 2 },
		"stanchion" : { "radius" : 3, "invMass" : 0, "bCoef" : 3, "cMask" : ["none" ] },
		"cornerflag" : { "radius" : 3, "invMass" : 0, "bCoef" : 0.5, "color" : "FFFF00", "cGroup" : [ ] },
		"reargoalNetleft" : { "vis" : true, "bCoef" : 0.1, "cMask" : ["ball","red","blue" ], "curve" : 10, "color" : "C7E6BD" },
		"reargoalNetright" : { "vis" : true, "bCoef" : 0.1, "cMask" : ["ball","red","blue" ], "curve" : -10, "color" : "C7E6BD" },
		"sidegoalNet" : { "vis" : true, "bCoef" : 1, "cMask" : ["ball","red","blue" ], "color" : "C7E6BD" },
		"kickOffBarrier" : { "vis" : false, "bCoef" : 0.1, "cGroup" : ["redKO","blueKO" ], "cMask" : ["red","blue" ] },
		"line" : { "vis" : true, "cMask" : [ ], "color" : "C7E6BD" },
		"tunnel" : { "vis" : true, "cMask" : ["red","blue" ], "color" : "000000" },
		"advertising" : { "vis" : true, "cMask" : ["red","blue" ], "color" : "333333" },
		"teambench" : { "vis" : true, "cMask" : [ ], "color" : "000000" },
		"manager" : { "radius" : 15, "vis" : true, "cMask" : ["red","blue" ], "invMass" : 0, "color" : "333333" },
		"physio" : { "radius" : 15, "vis" : true, "cMask" : ["red","blue" ], "invMass" : 0, "color" : "666666" },
		"redsubs" : { "radius" : 15, "vis" : true, "cMask" : ["red","blue" ], "invMass" : 0, "color" : "E56E56" },
		"bluesubs" : { "radius" : 15, "vis" : true, "cMask" : ["red","blue" ], "invMass" : 0, "color" : "5689E5" }

	}
}`;
var MiniRS=`
{

	"name" : "Mɪɴɪ 𝐑𝐒 ʙʏ 𝒓𝒔𝒌 & 𝐆𝐋𝐇",

	"width" : 940,

	"height" : 380,

	"spawnDistance" : 350,

	"bg" : { "type" : "hockey", "width" : 700, "height" : 320, "kickOffRadius" : 80, "cornerRadius" : 0 },

	"playerPhysics" : {
		"bCoef" : 0.1,
		"invMass" : 0.7,
		"acceleration" : 0.11,
		"kickingAcceleration" : 0.05,
		"kickStrength" : 5.67

	},

	"ballPhysics" : {
		"radius" : 9.9,
		"bCoef" : 0.5,
		"invMass" : 1,
		"damping" : 0.99,
		"color" : "FFDD00",
		"cMask" : [ "all"
		],
		"cGroup" : [ "ball"
		]

	},

	"vertexes" : [
		/* 0 */ { "x" : 700, "y" : 206, "trait" : "line", "color" : "FFDD00" },
		/* 1 */ { "x" : 491, "y" : 206, "trait" : "line", "color" : "FFDD00" },
		/* 2 */ { "x" : 700, "y" : -206, "trait" : "line", "color" : "FFDD00" },
		/* 3 */ { "x" : 491, "y" : -206, "trait" : "line", "color" : "FFDD00" },
		/* 4 */ { "x" : 700, "y" : 125, "trait" : "line", "color" : "004DFF" },
		/* 5 */ { "x" : 614, "y" : 125, "trait" : "line", "color" : "004DFF" },
		/* 6 */ { "x" : 700, "y" : -125, "trait" : "line", "color" : "004DFF" },
		/* 7 */ { "x" : 614, "y" : -125, "trait" : "line", "color" : "004DFF" },
		/* 8 */ { "x" : 491, "y" : -90, "trait" : "line", "curve" : -130, "color" : "004DFF" },
		/* 9 */ { "x" : 491, "y" : 79, "trait" : "line", "curve" : -130, "color" : "004DFF" },
		/* 10 */ { "x" : -700, "y" : -206, "trait" : "line", "color" : "FFDD00" },
		/* 11 */ { "x" : -491, "y" : -206, "trait" : "line", "color" : "FFDD00" },
		/* 12 */ { "x" : -700, "y" : 206, "trait" : "line", "color" : "FFDD00" },
		/* 13 */ { "x" : -491, "y" : 206, "trait" : "line", "color" : "FFDD00" },
		/* 14 */ { "x" : -700, "y" : -125, "trait" : "line", "color" : "F00000" },
		/* 15 */ { "x" : -614, "y" : -125, "trait" : "line", "color" : "F00000" },
		/* 16 */ { "x" : -700, "y" : 125, "trait" : "line", "color" : "F00000" },
		/* 17 */ { "x" : -614, "y" : 125, "trait" : "line", "color" : "F00000" },
		/* 18 */ { "x" : -491, "y" : 85, "trait" : "line", "curve" : -130, "color" : "F00000" },
		/* 19 */ { "x" : -491, "y" : -89, "trait" : "line", "curve" : -130, "color" : "F00000" },
		/* 20 */ { "x" : 556, "y" : 4.5, "trait" : "line", "color" : "2e2604" },
		/* 21 */ { "x" : 556, "y" : -4.5, "trait" : "line", "color" : "2e2604" },
		/* 22 */ { "x" : -553, "y" : 4.5, "trait" : "line", "color" : "2e2604" },
		/* 23 */ { "x" : -553, "y" : -4.5, "trait" : "line", "color" : "2e2604" },
		
		/* 24 */ { "x" : -700, "y" : -320, "bCoef" : 2, "cMask" : ["ball" ], "color" : "FFFFFF", "vis" : false },
		/* 25 */ { "x" : -700, "y" : -386, "cMask" : ["ball" ], "vis" : false },
		/* 26 */ { "x" : -700, "y" : -320, "bCoef" : 2, "cMask" : ["ball" ], "color" : "FFFFFF", "vis" : false },
		/* 27 */ { "x" : -700, "y" : -386, "cMask" : ["ball" ], "vis" : false },
		/* 28 */ { "x" : 700, "y" : -320, "bCoef" : 2, "cMask" : ["ball" ], "color" : "FFFFFF", "vis" : false },
		/* 29 */ { "x" : 700, "y" : -390, "cMask" : ["ball" ], "vis" : false },
		/* 30 */ { "x" : 700, "y" : 390, "bCoef" : 2, "cMask" : ["ball" ], "color" : "FFFFFF", "vis" : false },
		/* 31 */ { "x" : 700, "y" : 320, "cMask" : ["ball" ], "vis" : false },
		/* 32 */ { "x" : -700, "y" : 390, "bCoef" : 2, "cMask" : ["ball" ], "color" : "FFFFFF", "vis" : false },
		/* 33 */ { "x" : -700, "y" : 320, "cMask" : ["ball" ], "vis" : false },
		/* 34 */ { "x" : -969, "y" : -123, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 35 */ { "x" : -822, "y" : -124, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 36 */ { "x" : -822, "y" : 123, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 37 */ { "x" : -967, "y" : 123, "bCoef" : 0, "cMask" : ["blue" ] },
		
		/* 38 */ { "x" : -969, "y" : -123, "trait" : "kickOffBarrier" },
		/* 39 */ { "x" : -822, "y" : -123, "trait" : "kickOffBarrier" },
		/* 40 */ { "x" : -822, "y" : 123, "trait" : "kickOffBarrier" },
		/* 41 */ { "x" : -969, "y" : 123, "trait" : "kickOffBarrier" },
		
		/* 42 */ { "x" : -909, "y" : -83, "bCoef" : 0, "cMask" : ["blue" ], "color" : "2257D2" },
		/* 43 */ { "x" : -909, "y" : 77, "bCoef" : 0, "cMask" : ["blue" ], "color" : "2257D2" },
		/* 44 */ { "x" : -914, "y" : -83, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 45 */ { "x" : -904, "y" : -83, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 46 */ { "x" : -914, "y" : 77, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 47 */ { "x" : -904, "y" : 77, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 48 */ { "x" : -959, "y" : -83, "bCoef" : 0, "cMask" : ["red" ] },
		/* 49 */ { "x" : -959, "y" : 77, "bCoef" : 0, "cMask" : ["red" ] },
		/* 50 */ { "x" : 969, "y" : -123, "bCoef" : 0, "cMask" : ["red" ] },
		/* 51 */ { "x" : 822, "y" : -123, "bCoef" : 0, "cMask" : ["red" ] },
		/* 52 */ { "x" : 822, "y" : 123, "bCoef" : 0, "cMask" : ["red" ] },
		/* 53 */ { "x" : 969, "y" : 123, "bCoef" : 0, "cMask" : ["red" ] },
		
		/* 54 */ { "x" : 969, "y" : -123, "trait" : "kickOffBarrier" },
		/* 55 */ { "x" : 823, "y" : -123, "trait" : "kickOffBarrier" },
		/* 56 */ { "x" : 822, "y" : 123, "trait" : "kickOffBarrier" },
		/* 57 */ { "x" : 969, "y" : 123, "trait" : "kickOffBarrier" },
		
		/* 58 */ { "x" : 911, "y" : -90, "bCoef" : 0, "cMask" : ["red" ], "color" : "FF2121" },
		/* 59 */ { "x" : 911, "y" : 70, "bCoef" : 0, "cMask" : ["red" ], "color" : "FF2121" },
		/* 60 */ { "x" : 916, "y" : -90, "bCoef" : 0, "cMask" : ["red" ] },
		/* 61 */ { "x" : 906, "y" : -90, "bCoef" : 0, "cMask" : ["red" ] },
		/* 62 */ { "x" : 916, "y" : 70, "bCoef" : 0, "cMask" : ["red" ] },
		/* 63 */ { "x" : 906, "y" : 70, "bCoef" : 0, "cMask" : ["red" ] },
		/* 64 */ { "x" : 961, "y" : -90, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 65 */ { "x" : 961, "y" : 70, "bCoef" : 0, "cMask" : ["blue" ] },
		
		/* 66 */ { "x" : -720, "y" : 236, "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "curve" : -40, "color" : "FFDD00" },
		/* 67 */ { "x" : -720, "y" : 152, "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "curve" : -40, "color" : "FFDD00" },
		/* 68 */ { "x" : -720, "y" : -152, "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "curve" : -40, "color" : "FFDD00" },
		/* 69 */ { "x" : -720, "y" : -236, "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "curve" : -40, "color" : "FFDD00" },
		/* 70 */ { "x" : 720, "y" : -236, "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "curve" : -40, "color" : "FFDD00" },
		/* 71 */ { "x" : 720, "y" : -152, "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "curve" : -40, "color" : "FFDD00" },
		/* 72 */ { "x" : 720, "y" : 152, "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "curve" : 40, "color" : "FFDD00" },
		/* 73 */ { "x" : 720, "y" : 236, "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "curve" : 40, "color" : "FFDD00" },
		/* 74 */ { "x" : -700, "y" : 83.5, "bCoef" : 1.1, "cMask" : ["ball","red","blue" ], "trait" : "line", "color" : "F00000", "curve" : 0 },
		/* 75 */ { "x" : -760, "y" : 82, "bCoef" : 1.1, "cMask" : ["ball","red","blue" ], "trait" : "line", "color" : "F00000", "vis" : false, "curve" : 12 },
		/* 76 */ { "x" : -700, "y" : -83.5, "bCoef" : 1.1, "cMask" : ["ball","red","blue" ], "trait" : "line", "color" : "F00000", "curve" : 0 },
		/* 77 */ { "x" : -760, "y" : -82, "bCoef" : 1.1, "cMask" : ["ball","red","blue" ], "trait" : "line", "color" : "F00000", "vis" : false, "curve" : 12 },
		/* 78 */ { "x" : -760, "y" : 82, "trait" : "line", "color" : "ffffff" },
		/* 79 */ { "x" : -760, "y" : -82, "trait" : "line", "color" : "ffffff" },
		/* 80 */ { "x" : -760, "y" : 82, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "line", "color" : "FFF7F7", "vis" : true, "curve" : 10 },
		/* 81 */ { "x" : -760, "y" : -82, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "line", "color" : "FFF7F7", "vis" : true, "curve" : 10 },
		/* 82 */ { "x" : 703.01261034953, "y" : -83.5, "bCoef" : 1.1, "cMask" : ["ball","red","blue" ], "trait" : "line", "color" : "004DFF", "curve" : 0 },
		/* 83 */ { "x" : 761, "y" : -82, "bCoef" : 1.1, "cMask" : ["ball","red","blue" ], "trait" : "line", "color" : "004DFF", "vis" : false, "curve" : 12 },
		/* 84 */ { "x" : 701, "y" : 83.5, "bCoef" : 1.1, "cMask" : ["ball","red","blue" ], "trait" : "line", "color" : "004DFF", "curve" : 0 },
		/* 85 */ { "x" : 761, "y" : 82, "bCoef" : 1.1, "cMask" : ["ball","red","blue" ], "trait" : "line", "color" : "004DFF", "vis" : false, "curve" : 12 },
		/* 86 */ { "x" : 761, "y" : -82, "trait" : "line", "color" : "ffffff" },
		/* 87 */ { "x" : 761, "y" : 82, "trait" : "line", "color" : "ffffff" },
		/* 88 */ { "x" : 761, "y" : -82, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "line", "color" : "FFF7F7", "vis" : true, "curve" : 10 },
		/* 89 */ { "x" : 761, "y" : 82, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "line", "color" : "FFF7F7", "vis" : true, "curve" : 10 },
		
		/* 90 */ { "x" : 0, "y" : -80, "cMask" : ["red" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "color" : "585757", "vis" : false, "curve" : 0 },
		/* 91 */ { "x" : 0, "y" : -390, "trait" : "kickOffBarrier", "color" : "585757", "vis" : false, "curve" : 0 },
		/* 92 */ { "x" : -1, "y" : 390, "cMask" : ["red" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "color" : "585757", "vis" : false, "curve" : 0 },
		/* 93 */ { "x" : 0, "y" : 80, "trait" : "kickOffBarrier", "color" : "585757", "vis" : false, "curve" : 0 },
		
		/* 94 */ { "x" : -491, "y" : -206, "trait" : "line", "color" : "FFDD00" },
		/* 95 */ { "x" : -491, "y" : 206, "trait" : "line", "color" : "FFDD00" },
		/* 96 */ { "x" : 491, "y" : 206, "trait" : "line", "color" : "FFDD00" },
		/* 97 */ { "x" : 491, "y" : -206, "trait" : "line", "color" : "FFDD00" },
		/* 98 */ { "x" : -700, "y" : 320, "trait" : "line", "color" : "FFDD00" },
		/* 99 */ { "x" : -700, "y" : -320, "trait" : "line", "color" : "FFDD00" },
		/* 100 */ { "x" : 700, "y" : 320, "trait" : "line", "color" : "FFDD00" },
		/* 101 */ { "x" : 700, "y" : -320, "trait" : "line", "color" : "FFDD00" },
		
		/* 102 */ { "x" : 0, "y" : 81, "trait" : "kickOffBarrier", "color" : "fcfcfc", "vis" : false },
		
		/* 103 */ { "x" : 0, "y" : -5, "trait" : "line", "color" : "FFDD00" },
		/* 104 */ { "x" : 0, "y" : 3, "trait" : "line", "color" : "FFDD00" },
		/* 105 */ { "x" : 0, "y" : -5, "trait" : "line", "color" : "FFDD00" },
		/* 106 */ { "x" : 0, "y" : 3, "trait" : "line", "color" : "FFDD00" },
		
		/* 107 */ { "x" : -30, "y" : -49, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "curve" : 0 },
		/* 108 */ { "x" : -30, "y" : 34, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "curve" : 0 },
		/* 109 */ { "x" : 30, "y" : -49, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO" ], "trait" : "kickOffBarrier", "curve" : 0 },
		/* 110 */ { "x" : 30, "y" : 34, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO" ], "trait" : "kickOffBarrier", "curve" : 0, "color" : "FFFFFF" },
		/* 111 */ { "x" : 80.5, "y" : 3, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "color" : "eec215", "vis" : true, "curve" : 12 },
		/* 112 */ { "x" : -80.5, "y" : 4, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "color" : "eec215", "vis" : true, "curve" : -12 },
		/* 113 */ { "x" : 72, "y" : 34, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "curve" : -160.5, "vis" : true, "color" : "eec215" },
		/* 114 */ { "x" : -72, "y" : 35, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "curve" : -160.5, "vis" : true, "color" : "eec215" },
		/* 115 */ { "x" : 78.8, "y" : -19, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "color" : "eec215", "vis" : true, "curve" : 12 },
		/* 116 */ { "x" : -78.8, "y" : -18, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "color" : "eec215", "vis" : true, "curve" : -12 },
		/* 117 */ { "x" : 63, "y" : -49, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "curve" : 154, "vis" : true, "color" : "eec215" },
		/* 118 */ { "x" : -64, "y" : -49, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "curve" : 154, "vis" : true, "color" : "eec215" },
		/* 119 */ { "x" : 63, "y" : -49, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO" ], "trait" : "kickOffBarrier", "curve" : 0, "vis" : true, "color" : "004dff" },
		/* 120 */ { "x" : 72, "y" : 34, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO" ], "trait" : "kickOffBarrier", "curve" : 0, "vis" : true, "color" : "004dff" },
		/* 121 */ { "x" : -64, "y" : -49, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "curve" : 0, "vis" : true, "color" : "f73131" },
		/* 122 */ { "x" : -72, "y" : 35, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "curve" : 0, "vis" : true, "color" : "f73131" },
		/* 123 */ { "x" : 0, "y" : -80, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "vis" : true, "color" : "FFDD00" },
		/* 124 */ { "x" : 0, "y" : -320, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "vis" : true, "color" : "FFDD00" },
		/* 125 */ { "x" : 0, "y" : 320, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "vis" : true, "color" : "FFDD00" },
		/* 126 */ { "x" : 0, "y" : 80, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "vis" : true, "color" : "FFDD00" },
		
		/* 127 */ { "x" : 0, "y" : -80, "trait" : "line", "color" : "FFDD00" },
		/* 128 */ { "x" : 0, "y" : 80, "trait" : "line", "color" : "FFDD00" },
		/* 129 */ { "x" : -700, "y" : 294, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "FFDD00" },
		/* 130 */ { "x" : -675, "y" : 320, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "FFDD00" },
		/* 131 */ { "x" : -672.85422349049, "y" : -320, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "FFDD00" },
		/* 132 */ { "x" : -700, "y" : -295.14627021274, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "FFDD00" },
		/* 133 */ { "x" : 671.84288219525, "y" : 320, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "FFDD00" },
		/* 134 */ { "x" : 700, "y" : 294.15582349306, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "FFDD00" },
		/* 135 */ { "x" : 700, "y" : -293.03342928015, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "FFDD00" },
		/* 136 */ { "x" : 673.92337307118, "y" : -320, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "FFDD00" },
		/* 137 */ { "x" : -712, "y" : -318, "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line", "curve" : 45, "color" : "FFDD00" },
		/* 138 */ { "x" : -740, "y" : -298, "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line", "curve" : 45, "color" : "FFDD00" },
		/* 139 */ { "x" : -740, "y" : 298, "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line", "curve" : 45, "color" : "FFDD00" },
		/* 140 */ { "x" : -712, "y" : 318, "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line", "curve" : 45, "color" : "FFDD00" },
		/* 141 */ { "x" : 712, "y" : 318, "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line", "curve" : 45, "color" : "FFDD00" },
		/* 142 */ { "x" : 740, "y" : 298, "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line", "curve" : 45, "color" : "FFDD00" },
		/* 143 */ { "x" : 740, "y" : -298, "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line", "curve" : 45, "color" : "FFDD00" },
		/* 144 */ { "x" : 712, "y" : -318, "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line", "curve" : 45, "color" : "FFDD00" },
		
		/* 145 */ { "x" : 761, "y" : -82, "bCoef" : 1.1, "cMask" : ["ball" ], "vis" : false, "curve" : 0 },
		/* 146 */ { "x" : 777, "y" : -82, "bCoef" : 1.1, "cMask" : ["ball" ], "vis" : false, "curve" : 0 },
		/* 147 */ { "x" : 761, "y" : 82, "bCoef" : 1.1, "cMask" : ["ball" ], "vis" : false, "curve" : 0 },
		/* 148 */ { "x" : 778, "y" : 82, "bCoef" : 1.1, "cMask" : ["ball" ], "vis" : false, "curve" : 0 },
		/* 149 */ { "x" : -760, "y" : -82, "bCoef" : 1.1, "cMask" : ["ball" ], "vis" : false, "curve" : 0 },
		/* 150 */ { "x" : -776, "y" : -82, "bCoef" : 1.1, "cMask" : ["ball" ], "vis" : false, "curve" : 0 },
		/* 151 */ { "x" : -776, "y" : 82, "bCoef" : 1.1, "cMask" : ["ball" ], "vis" : false, "curve" : 0 },
		/* 152 */ { "x" : -760, "y" : 82, "bCoef" : 1.1, "cMask" : ["ball" ], "vis" : false, "curve" : 0 },
		/* 153 */ { "x" : -700, "y" : -320, "bCoef" : 1.2, "cMask" : ["ball" ], "curve" : 0, "color" : "222223" },
		/* 154 */ { "x" : 700, "y" : -320, "bCoef" : 1.2, "cMask" : ["ball" ], "curve" : 0, "color" : "222223" },
		/* 155 */ { "x" : -700, "y" : 320, "bCoef" : 1.2, "cMask" : ["ball" ], "curve" : 0, "color" : "222223" },
		/* 156 */ { "x" : 700, "y" : 320, "bCoef" : 1.2, "cMask" : ["ball" ], "curve" : 0, "color" : "222223" },
		/* 157 */ { "x" : -682, "y" : -323, "bCoef" : -5, "cMask" : ["ball" ], "color" : "FFFFFF", "vis" : false },
		/* 158 */ { "x" : -682, "y" : -389, "bCoef" : -5, "cMask" : ["ball" ], "vis" : false },
		/* 159 */ { "x" : -682, "y" : 390, "bCoef" : -5, "cMask" : ["ball" ], "color" : "FFFFFF", "vis" : false },
		/* 160 */ { "x" : -682, "y" : 324, "bCoef" : -5, "cMask" : ["ball" ], "vis" : false },
		/* 161 */ { "x" : 682, "y" : 325.00001268704, "bCoef" : -5, "cMask" : ["ball" ], "color" : "FFFFFF", "vis" : false },
		/* 162 */ { "x" : 682, "y" : 390.99998652002, "bCoef" : -5, "cMask" : ["ball" ], "vis" : false },
		/* 163 */ { "x" : 682, "y" : -389.99998731296, "bCoef" : -5, "cMask" : ["ball" ], "color" : "FFFFFF", "vis" : false },
		/* 164 */ { "x" : 682, "y" : -324.00001347998, "bCoef" : -5, "cMask" : ["ball" ], "vis" : false }

	],

	"segments" : [
		{ "v0" : 0, "v1" : 1, "color" : "FFDD00", "trait" : "line", "y" : 206 },
		{ "v0" : 1, "v1" : 3, "color" : "e9cc6e", "trait" : "line", "x" : 840 },
		{ "v0" : 2, "v1" : 3, "color" : "FFDD00", "trait" : "line", "y" : -206 },
		{ "v0" : 4, "v1" : 5, "color" : "004DFF", "trait" : "line", "y" : 150 },
		{ "v0" : 5, "v1" : 7, "color" : "FFDD00", "trait" : "line", "x" : 1030 },
		{ "v0" : 6, "v1" : 7, "color" : "004DFF", "trait" : "line", "y" : -150 },
		{ "v0" : 8, "v1" : 9, "curve" : -130, "color" : "004DFF", "trait" : "line", "x" : 840 },
		{ "v0" : 10, "v1" : 11, "color" : "FFDD00", "trait" : "line", "y" : -206 },
		{ "v0" : 11, "v1" : 13, "color" : "e9cc6e", "trait" : "line", "x" : -840 },
		{ "v0" : 12, "v1" : 13, "color" : "FFDD00", "trait" : "line", "y" : 206 },
		{ "v0" : 14, "v1" : 15, "color" : "F00000", "trait" : "line", "y" : -150 },
		{ "v0" : 15, "v1" : 17, "color" : "FFDD00", "trait" : "line", "x" : -1030 },
		{ "v0" : 16, "v1" : 17, "color" : "F00000", "trait" : "line", "y" : 150 },
		{ "v0" : 18, "v1" : 19, "curve" : -130, "color" : "F00000", "trait" : "line", "x" : -491 },
		{ "v0" : 20, "v1" : 21, "curve" : -180, "color" : "2e2604", "trait" : "line", "x" : 935 },
		{ "v0" : 22, "v1" : 23, "curve" : -180, "color" : "2e2604", "trait" : "line", "x" : -935 },
		{ "v0" : 20, "v1" : 21, "curve" : 180, "color" : "2e2604", "trait" : "line", "x" : 935 },
		{ "v0" : 22, "v1" : 23, "curve" : 180, "color" : "2e2604", "trait" : "line", "x" : -935 },
		{ "v0" : 20, "v1" : 21, "curve" : 90, "color" : "2e2604", "trait" : "line", "x" : 935 },
		{ "v0" : 22, "v1" : 23, "curve" : 90, "color" : "2e2604", "trait" : "line", "x" : -935 },
		{ "v0" : 20, "v1" : 21, "curve" : -90, "color" : "2e2604", "trait" : "line", "x" : 935 },
		{ "v0" : 22, "v1" : 23, "curve" : -90, "color" : "2e2604", "trait" : "line", "x" : -935 },
		{ "v0" : 20, "v1" : 21, "color" : "2e2604", "trait" : "line", "x" : 935 },
		{ "v0" : 22, "v1" : 23, "color" : "2e2604", "trait" : "line", "x" : -935 },
		
		{ "v0" : 25, "v1" : 24, "curve" : 10, "vis" : false, "color" : "FFFFFF", "cMask" : ["ball" ] },
		{ "v0" : 27, "v1" : 26, "curve" : 10, "vis" : false, "color" : "FFFFFF", "cMask" : ["ball" ] },
		{ "v0" : 29, "v1" : 28, "curve" : 10, "vis" : false, "color" : "FFFFFF", "cMask" : ["ball" ] },
		{ "v0" : 31, "v1" : 30, "curve" : 10, "vis" : false, "color" : "FFFFFF", "cMask" : ["ball" ] },
		{ "v0" : 33, "v1" : 32, "curve" : 10, "vis" : false, "color" : "FFFFFF", "cMask" : ["ball" ] },
		{ "v0" : 34, "v1" : 35, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ] },
		{ "v0" : 35, "v1" : 36, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ] },
		{ "v0" : 36, "v1" : 37, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ] },
		
		{ "v0" : 38, "v1" : 39, "trait" : "kickOffBarrier" },
		{ "v0" : 40, "v1" : 41, "trait" : "kickOffBarrier" },
		
		{ "v0" : 42, "v1" : 43, "color" : "2257D2", "bCoef" : 1000000, "cMask" : ["blue" ] },
		{ "v0" : 44, "v1" : 45, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ] },
		{ "v0" : 46, "v1" : 47, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ] },
		{ "v0" : 48, "v1" : 49, "vis" : false, "bCoef" : 1000000, "cMask" : ["red" ] },
		{ "v0" : 50, "v1" : 51, "vis" : false, "bCoef" : 0, "cMask" : ["red" ] },
		{ "v0" : 51, "v1" : 52, "vis" : false, "bCoef" : 0, "cMask" : ["red" ] },
		{ "v0" : 52, "v1" : 53, "vis" : false, "bCoef" : 0, "cMask" : ["red" ] },
		
		{ "v0" : 54, "v1" : 55, "trait" : "kickOffBarrier" },
		{ "v0" : 56, "v1" : 57, "trait" : "kickOffBarrier" },
		
		{ "v0" : 58, "v1" : 59, "color" : "FF2121", "bCoef" : 1000000, "cMask" : ["red" ] },
		{ "v0" : 60, "v1" : 61, "vis" : false, "bCoef" : 0, "cMask" : ["red" ] },
		{ "v0" : 62, "v1" : 63, "vis" : false, "bCoef" : 0, "cMask" : ["red" ] },
		{ "v0" : 64, "v1" : 65, "vis" : false, "bCoef" : 1000000, "cMask" : ["blue" ] },
		
		{ "v0" : 66, "v1" : 67, "curve" : -40, "vis" : true, "color" : "FFDD00", "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "x" : -720 },
		{ "v0" : 68, "v1" : 69, "curve" : -40, "vis" : true, "color" : "FFDD00", "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "x" : -730 },
		{ "v0" : 70, "v1" : 71, "curve" : -40, "vis" : true, "color" : "FFDD00", "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "x" : 720 },
		
		{ "v0" : 75, "v1" : 77, "curve" : 12, "vis" : false, "color" : "FFFFFF", "cMask" : ["ball" ], "trait" : "reargoalNetleft", "x" : -760 },
		
		{ "v0" : 74, "v1" : 75, "curve" : 0, "color" : "F00000", "bCoef" : 1.1, "cMask" : ["ball","red","blue" ], "trait" : "sidegoalNet" },
		{ "v0" : 76, "v1" : 77, "curve" : 0, "color" : "F00000", "bCoef" : 1.1, "cMask" : ["ball","red","blue" ], "trait" : "sidegoalNet" },
		
		{ "v0" : 80, "v1" : 81, "curve" : 10, "vis" : true, "color" : "FFF7F7", "cMask" : ["ball" ], "trait" : "reargoalNetleft", "x" : -760 },
		{ "v0" : 83, "v1" : 85, "curve" : 12, "vis" : false, "color" : "FFFFFF", "cMask" : ["ball" ], "trait" : "reargoalNetleft", "x" : 760 },
		
		{ "v0" : 82, "v1" : 83, "curve" : 0, "color" : "004DFF", "bCoef" : 1.1, "cMask" : ["ball","red","blue" ], "trait" : "sidegoalNet" },
		{ "v0" : 84, "v1" : 85, "curve" : 0, "color" : "004DFF", "bCoef" : 1.1, "cMask" : ["ball","red","blue" ], "trait" : "sidegoalNet" },
		
		{ "v0" : 88, "v1" : 89, "curve" : 10, "vis" : true, "color" : "FFF7F7", "cMask" : ["ball" ], "trait" : "reargoalNetleft", "x" : 760 },
		
		{ "v0" : 90, "v1" : 91, "curve" : 0, "vis" : false, "color" : "585757", "trait" : "kickOffBarrier", "x" : 0 },
		{ "v0" : 92, "v1" : 93, "curve" : 0, "vis" : false, "color" : "585757", "trait" : "kickOffBarrier", "x" : 0 },
		
		{ "v0" : 94, "v1" : 95, "color" : "FFDD00", "trait" : "line", "x" : -840 },
		{ "v0" : 96, "v1" : 97, "color" : "FFDD00", "trait" : "line", "x" : 840 },
		{ "v0" : 98, "v1" : 99, "vis" : true, "color" : "FFDD00", "trait" : "line" },
		{ "v0" : 100, "v1" : 101, "vis" : true, "color" : "FFDD00", "trait" : "line" },
		{ "v0" : 103, "v1" : 104, "curve" : -180, "color" : "FFDD00", "trait" : "line" },
		{ "v0" : 105, "v1" : 106, "curve" : 180, "color" : "FFDD00", "trait" : "line" },
		{ "v0" : 103, "v1" : 104, "curve" : -90, "color" : "FFDD00", "trait" : "line" },
		{ "v0" : 105, "v1" : 106, "curve" : 90, "color" : "FFDD00", "trait" : "line" },
		
		{ "v0" : 107, "v1" : 108, "curve" : 0, "vis" : false, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "x" : -10 },
		{ "v0" : 109, "v1" : 110, "curve" : 0, "vis" : false, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO" ], "trait" : "kickOffBarrier", "x" : 10 },
		{ "v0" : 111, "v1" : 112, "vis" : false, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "y" : 5 },
		{ "v0" : 113, "v1" : 114, "vis" : false, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "y" : 35 },
		{ "v0" : 115, "v1" : 116, "vis" : false, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "y" : -20 },
		{ "v0" : 117, "v1" : 118, "vis" : false, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "y" : -50 },
		{ "v0" : 114, "v1" : 113, "curve" : -129.997900266, "vis" : true, "color" : "FFDD00", "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier" },
		{ "v0" : 118, "v1" : 117, "curve" : 103.422024528, "vis" : true, "color" : "FFDD00", "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier" },
		{ "v0" : 119, "v1" : 120, "curve" : 64.5746162722, "vis" : true, "color" : "004dff", "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO" ], "trait" : "kickOffBarrier", "x" : 200 },
		{ "v0" : 121, "v1" : 122, "curve" : -60.1197451124, "vis" : true, "color" : "f73131", "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "x" : -200 },
		{ "v0" : 116, "v1" : 112, "curve" : -12, "vis" : true, "color" : "FFDD00", "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "x" : -180 },
		{ "v0" : 115, "v1" : 111, "curve" : 12, "vis" : true, "color" : "FFDD00", "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "x" : 180 },
		{ "v0" : 123, "v1" : 124, "curve" : 0, "vis" : true, "color" : "FFDD00", "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier" },
		{ "v0" : 125, "v1" : 126, "curve" : 0, "vis" : true, "color" : "FFDD00", "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier" },
		
		{ "v0" : 127, "v1" : 128, "vis" : true, "color" : "FFDD00", "trait" : "line" },
		{ "v0" : 129, "v1" : 130, "curve" : 90, "color" : "FFDD00", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line" },
		{ "v0" : 131, "v1" : 132, "curve" : 90, "color" : "FFDD00", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line" },
		{ "v0" : 133, "v1" : 134, "curve" : 90, "color" : "FFDD00", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line" },
		{ "v0" : 135, "v1" : 136, "curve" : 90, "color" : "FFDD00", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line" },
		{ "v0" : 137, "v1" : 138, "curve" : 45, "vis" : true, "color" : "FFDD00", "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line" },
		{ "v0" : 139, "v1" : 140, "curve" : 45, "vis" : true, "color" : "FFDD00", "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line" },
		{ "v0" : 141, "v1" : 142, "curve" : 45, "vis" : true, "color" : "FFDD00", "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line" },
		{ "v0" : 143, "v1" : 144, "curve" : 45, "vis" : true, "color" : "FFDD00", "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line" },
		
		{ "v0" : 145, "v1" : 146, "curve" : 0, "vis" : false, "color" : "f9f6e8", "bCoef" : 1.1, "cMask" : ["ball" ], "y" : -82 },
		{ "v0" : 147, "v1" : 148, "curve" : 0, "vis" : false, "color" : "f9f6e8", "bCoef" : 1.1, "cMask" : ["ball" ], "y" : 82 },
		{ "v0" : 149, "v1" : 150, "curve" : 0, "vis" : false, "color" : "f9f6e8", "bCoef" : 1.1, "cMask" : ["ball" ], "y" : -82 },
		{ "v0" : 151, "v1" : 152, "curve" : 0, "vis" : false, "color" : "f9f6e8", "bCoef" : 1.1, "cMask" : ["ball" ], "y" : 82 },
		
		{ "v0" : 73, "v1" : 72, "curve" : 40, "vis" : true, "color" : "FFDD00", "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "x" : 720 },
		
		{ "v0" : 153, "v1" : 154, "curve" : 0, "vis" : true, "color" : "222223", "bCoef" : 1.2, "cMask" : ["ball" ], "y" : -320 },
		{ "v0" : 155, "v1" : 156, "curve" : 0, "vis" : true, "color" : "222223", "bCoef" : 1.2, "cMask" : ["ball" ] },
		{ "v0" : 158, "v1" : 157, "curve" : 10, "vis" : false, "color" : "FFFFFF", "bCoef" : -5, "cMask" : ["ball" ] },
		{ "v0" : 160, "v1" : 159, "curve" : 10, "vis" : false, "color" : "FFFFFF", "bCoef" : -5, "cMask" : ["ball" ], "x" : -682 },
		{ "v0" : 162, "v1" : 161, "curve" : 10, "vis" : false, "color" : "FFFFFF", "bCoef" : -5, "cMask" : ["ball" ], "x" : 682 },
		{ "v0" : 164, "v1" : 163, "curve" : 10, "vis" : false, "color" : "FFFFFF", "bCoef" : -5, "cMask" : ["ball" ], "x" : 682 }

	],

	"goals" : [
		{ "p0" : [-710,-82 ], "p1" : [-710,82 ], "team" : "red" },
		{ "p0" : [711,82 ], "p1" : [711,-82 ], "team" : "blue" }

	],

	"discs" : [
		{ "radius" : 3, "invMass" : 0, "pos" : [-700,-320 ], "color" : "FFFF00", "trait" : "cornerflag" },
		{ "radius" : 3, "invMass" : 0, "pos" : [700,320 ], "color" : "FFFF00", "trait" : "cornerflag" },
		{ "radius" : 3, "invMass" : 0, "pos" : [700,-320 ], "color" : "FFFF00", "trait" : "cornerflag" },
		{ "radius" : 3, "invMass" : 0, "pos" : [-700,320 ], "color" : "FFFF00", "trait" : "cornerflag" },
		
		{ "radius" : 5, "pos" : [-700,83.5 ], "color" : "f73131", "trait" : "goalPost" },
		{ "radius" : 5, "pos" : [-700,-83.5 ], "color" : "f73131", "trait" : "goalPost" },
		{ "radius" : 5, "pos" : [700,-83.5 ], "color" : "004DFF", "trait" : "goalPost" },
		{ "radius" : 5, "pos" : [700,83.5 ], "color" : "004DFF", "trait" : "goalPost" }

	],

	"planes" : [
		{ "normal" : [0,1 ], "dist" : -346, "bCoef" : 0, "trait" : "ballArea" },
		{ "normal" : [0,-1 ], "dist" : -346, "bCoef" : 0, "trait" : "ballArea" },
		
		{ "normal" : [0,1 ], "dist" : -390, "bCoef" : 0 },
		{ "normal" : [0,-1 ], "dist" : -392, "bCoef" : 0 },
		
		{ "normal" : [1,0 ], "dist" : -763, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea" },
		{ "normal" : [-1,0 ], "dist" : -763, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false, "curve" : 0 },
		
		{ "normal" : [1,0 ], "dist" : -970, "bCoef" : 0 },
		{ "normal" : [-1,0 ], "dist" : -971, "bCoef" : 0 }

	],

	"traits" : {
		"ballArea" : { "vis" : false, "bCoef" : 0, "cMask" : ["ball" ] },
		"goalPost" : { "radius" : 5, "invMass" : 0, "bCoef" : 2 },
		"stanchion" : { "radius" : 3, "invMass" : 0, "bCoef" : 3, "cMask" : ["none" ] },
		"cornerflag" : { "radius" : 3, "invMass" : 0, "bCoef" : 0.5, "color" : "FFFF00", "cGroup" : [ ] },
		"reargoalNetleft" : { "vis" : true, "bCoef" : 0.1, "cMask" : ["ball","red","blue" ], "curve" : 10, "color" : "C7E6BD" },
		"reargoalNetright" : { "vis" : true, "bCoef" : 0.1, "cMask" : ["ball","red","blue" ], "curve" : -10, "color" : "C7E6BD" },
		"sidegoalNet" : { "vis" : true, "bCoef" : 1, "cMask" : ["ball","red","blue" ], "color" : "C7E6BD" },
		"kickOffBarrier" : { "vis" : false, "bCoef" : 0.1, "cGroup" : ["redKO","blueKO" ], "cMask" : ["red","blue" ] },
		"line" : { "vis" : true, "cMask" : [ ], "color" : "C7E6BD" },
		"tunnel" : { "vis" : true, "cMask" : ["red","blue" ], "color" : "000000" },
		"advertising" : { "vis" : true, "cMask" : ["red","blue" ], "color" : "333333" },
		"teambench" : { "vis" : true, "cMask" : [ ], "color" : "000000" },
		"manager" : { "radius" : 15, "vis" : true, "cMask" : ["red","blue" ], "invMass" : 0, "color" : "333333" },
		"physio" : { "radius" : 15, "vis" : true, "cMask" : ["red","blue" ], "invMass" : 0, "color" : "666666" },
		"redsubs" : { "radius" : 15, "vis" : true, "cMask" : ["red","blue" ], "invMass" : 0, "color" : "E56E56" },
		"bluesubs" : { "radius" : 15, "vis" : true, "cMask" : ["red","blue" ], "invMass" : 0, "color" : "5689E5" }

	}
}`;

var CarrerasGLH=`
{

	"name" : "🏁 𝙲𝙰𝚁𝚁𝙴𝚁𝙰𝚂 🏎",

	"width" : 15000,

	"height" : 800,

	"bg" : { "type" : "hockey", "width" : 5, "height" : 5 },

	"vertexes" : [
		/* 0 */ { "x" : -14575, "y" : -200, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		/* 1 */ { "x" : -14575, "y" : 200, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		/* 2 */ { "x" : -14585, "y" : 200, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 3 */ { "x" : -14565, "y" : 200, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 4 */ { "x" : -14585, "y" : -200, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 5 */ { "x" : -14565, "y" : -200, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 6 */ { "x" : -14575, "y" : 201, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 7 */ { "x" : -14575, "y" : 800, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 8 */ { "x" : -14575, "y" : -201, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 9 */ { "x" : -14575, "y" : -800, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 10 */ { "x" : -14575, "y" : 215, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 11 */ { "x" : -13175, "y" : 100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 12 */ { "x" : -14575, "y" : -215, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 13 */ { "x" : -13175, "y" : -100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 14 */ { "x" : -13000, "y" : -250, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 15 */ { "x" : -13000, "y" : 250, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 16 */ { "x" : -13769, "y" : 150, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 17 */ { "x" : -11950, "y" : 150, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 18 */ { "x" : -12250, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 19 */ { "x" : -13769, "y" : -150, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 20 */ { "x" : -11950, "y" : -150, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 21 */ { "x" : -10535, "y" : -150, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 22 */ { "x" : -10535, "y" : 150, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 23 */ { "x" : -11760, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 24 */ { "x" : -10770, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 25 */ { "x" : -9160, "y" : 100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 26 */ { "x" : -9160, "y" : -100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 27 */ { "x" : -10300, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 28 */ { "x" : -9340, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 29 */ { "x" : -7777, "y" : 130, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 30 */ { "x" : -7777, "y" : -130, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 31 */ { "x" : -8920, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 32 */ { "x" : -7910, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 33 */ { "x" : -7160, "y" : 50, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 34 */ { "x" : -7160, "y" : -50, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 35 */ { "x" : -5200, "y" : 50, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 36 */ { "x" : -5200, "y" : -50, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 37 */ { "x" : -7185, "y" : -75, "bCoef" : -2.4, "cMask" : ["red" ] },
		/* 38 */ { "x" : -7185, "y" : 75, "bCoef" : -2.4, "cMask" : ["red" ] },
		/* 39 */ { "x" : -5080, "y" : 50, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 40 */ { "x" : -4765, "y" : 50, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 41 */ { "x" : -5080, "y" : -50, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 42 */ { "x" : -4765, "y" : -50, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 43 */ { "x" : -4765, "y" : -265, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 44 */ { "x" : -4765, "y" : -365, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 45 */ { "x" : -5080, "y" : -150, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 46 */ { "x" : -5200, "y" : -150, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 47 */ { "x" : -4965, "y" : -265, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 48 */ { "x" : -4965, "y" : -365, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 49 */ { "x" : -5200, "y" : 560, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 50 */ { "x" : -5080, "y" : 560, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 51 */ { "x" : -4730, "y" : 560, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 52 */ { "x" : -4850, "y" : 560, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 53 */ { "x" : -4850, "y" : 320, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 54 */ { "x" : -4730, "y" : 320, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 55 */ { "x" : -4500, "y" : 320, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 56 */ { "x" : -4380, "y" : 320, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 57 */ { "x" : -4180, "y" : 320, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 58 */ { "x" : -4060, "y" : 320, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 59 */ { "x" : -4180, "y" : -375, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 60 */ { "x" : -4060, "y" : -375, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 61 */ { "x" : -3750, "y" : -375, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 62 */ { "x" : -3630, "y" : -375, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 63 */ { "x" : -3750, "y" : -150, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 64 */ { "x" : -3630, "y" : -150, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 65 */ { "x" : -3530, "y" : 50, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 66 */ { "x" : -3530, "y" : -50, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 67 */ { "x" : -2675, "y" : 50, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 68 */ { "x" : -2675, "y" : -50, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 69 */ { "x" : -2175, "y" : -250, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 70 */ { "x" : -2175, "y" : 250, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 71 */ { "x" : -1900, "y" : 440, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 72 */ { "x" : -2020, "y" : 130, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 73 */ { "x" : -1900, "y" : -440, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 74 */ { "x" : -2020, "y" : -130, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 75 */ { "x" : -1195, "y" : 200, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 76 */ { "x" : -1195, "y" : -40, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 77 */ { "x" : -990, "y" : 538.75, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 78 */ { "x" : -980, "y" : 290, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 79 */ { "x" : -222, "y" : 362.75, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 80 */ { "x" : -278, "y" : 228.75, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 81 */ { "x" : 6.25, "y" : -412.25, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 82 */ { "x" : 111.25, "y" : -252.25, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 83 */ { "x" : 571, "y" : -246.25, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 84 */ { "x" : 645, "y" : -83.25, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 85 */ { "x" : 1040, "y" : -477.25, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 86 */ { "x" : 1024, "y" : -251.25, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 87 */ { "x" : 1407, "y" : 317.75, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 88 */ { "x" : 1484, "y" : 135.75, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 89 */ { "x" : -4880, "y" : 445, "bCoef" : -2.4, "cMask" : ["red" ] },
		/* 90 */ { "x" : -4700, "y" : 445, "bCoef" : -2.4, "cMask" : ["red" ] },
		/* 91 */ { "x" : 2100, "y" : 100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 92 */ { "x" : 2100, "y" : -100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 93 */ { "x" : 2850, "y" : 100, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 94 */ { "x" : 2850, "y" : -100, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 95 */ { "x" : 2750, "y" : -250, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 96 */ { "x" : 2750, "y" : 250, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 97 */ { "x" : 2875, "y" : 460, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 98 */ { "x" : 2875, "y" : -460, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 99 */ { "x" : 4035, "y" : 100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 100 */ { "x" : 4035, "y" : -100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 101 */ { "x" : 4900, "y" : 100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 102 */ { "x" : 4900, "y" : -100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 103 */ { "x" : 6300, "y" : 100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 104 */ { "x" : 6300, "y" : -100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 105 */ { "x" : 5120, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 106 */ { "x" : 6090, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 107 */ { "x" : 7670, "y" : 100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 108 */ { "x" : 7670, "y" : -100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 109 */ { "x" : 6520, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 110 */ { "x" : 7480, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 111 */ { "x" : 7870, "y" : -600, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 112 */ { "x" : 7870, "y" : 600, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 113 */ { "x" : 7670, "y" : 700, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 114 */ { "x" : 8070, "y" : 700, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 115 */ { "x" : 8070, "y" : 100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 116 */ { "x" : 7670, "y" : -700, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 117 */ { "x" : 8070, "y" : -700, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 118 */ { "x" : 8070, "y" : -100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 119 */ { "x" : 8270, "y" : 600, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 120 */ { "x" : 8270, "y" : -600, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 121 */ { "x" : 8470, "y" : -700, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 122 */ { "x" : 8470, "y" : -50, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 123 */ { "x" : 8470, "y" : 700, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 124 */ { "x" : 8470, "y" : 50, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 125 */ { "x" : 10850, "y" : 100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 126 */ { "x" : 10850, "y" : -100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 127 */ { "x" : 11300, "y" : 100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 128 */ { "x" : 11300, "y" : -100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 129 */ { "x" : 10980, "y" : -90, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 130 */ { "x" : 10980, "y" : 90, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 131 */ { "x" : 11170, "y" : 90, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 132 */ { "x" : 11170, "y" : -90, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 133 */ { "x" : 12110, "y" : 15, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 134 */ { "x" : 12110, "y" : -15, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 135 */ { "x" : 12280, "y" : 15, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 136 */ { "x" : 12280, "y" : -15, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 137 */ { "x" : 12300, "y" : 35, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 138 */ { "x" : 12300, "y" : 240, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 139 */ { "x" : 12330, "y" : 240, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 140 */ { "x" : 12330, "y" : 35, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 141 */ { "x" : 8850, "y" : 50, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 142 */ { "x" : 8700, "y" : -50, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 143 */ { "x" : 8700, "y" : -700, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 144 */ { "x" : 10600, "y" : -700, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 145 */ { "x" : 8800, "y" : -275, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 146 */ { "x" : 10400, "y" : -275, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 147 */ { "x" : 10600, "y" : -100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 148 */ { "x" : 10400, "y" : 150, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 149 */ { "x" : -4215, "y" : 250, "bCoef" : -2.4, "cMask" : ["red" ] },
		/* 150 */ { "x" : -4025, "y" : 250, "bCoef" : -2.4, "cMask" : ["red" ] },
		/* 151 */ { "x" : 8060, "y" : 100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 152 */ { "x" : 8080, "y" : 100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 153 */ { "x" : 8060, "y" : -100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 154 */ { "x" : 8080, "y" : -100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 155 */ { "x" : 7870, "y" : 700, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 156 */ { "x" : 8270, "y" : 700, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 157 */ { "x" : 7870, "y" : -700, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 158 */ { "x" : 8270, "y" : -700, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 159 */ { "x" : 8065, "y" : -99, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 160 */ { "x" : 8065, "y" : 99, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 161 */ { "x" : 8075, "y" : -99, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 162 */ { "x" : 8075, "y" : 99, "bCoef" : 0.1, "cMask" : ["blue" ] },
		/* 163 */ { "x" : -12400, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 164 */ { "x" : -12600, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 165 */ { "x" : 12396, "y" : 158, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 166 */ { "x" : 12396, "y" : 218, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 167 */ { "x" : 12426, "y" : 218, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 168 */ { "x" : 12426, "y" : 198, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 169 */ { "x" : 12426, "y" : 158, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 170 */ { "x" : 12426, "y" : 173, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 171 */ { "x" : 10600, "y" : 150, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 172 */ { "x" : 10600, "y" : 100, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 173 */ { "x" : 8800, "y" : -50, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 174 */ { "x" : 8850, "y" : -50, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 175 */ { "x" : -3775, "y" : -350, "bCoef" : -2.4, "cMask" : ["red" ] },
		/* 176 */ { "x" : -3605, "y" : -350, "bCoef" : -2.4, "cMask" : ["red" ] },
		/* 177 */ { "x" : 3560, "y" : -210, "bCoef" : -2.3, "cMask" : ["red" ] },
		/* 178 */ { "x" : 3560, "y" : 210, "bCoef" : -2.3, "cMask" : ["red" ] },
		/* 179 */ { "x" : -11660, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 180 */ { "x" : -10870, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 181 */ { "x" : -10200, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 182 */ { "x" : -9440, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 183 */ { "x" : -8820, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 184 */ { "x" : -8010, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 185 */ { "x" : 5220, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 186 */ { "x" : 5990, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 187 */ { "x" : 6620, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 188 */ { "x" : 7380, "y" : 0, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 189 */ { "bCoef" : 0.1, "cMask" : ["red" ], "x" : 12406.75, "y" : 198 },
		/* 190 */ { "x" : 12442, "y" : 158, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 191 */ { "x" : 12442, "y" : 218, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 192 */ { "x" : 12472, "y" : 218, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 193 */ { "x" : 12526, "y" : 158, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 194 */ { "x" : 12526, "y" : 218, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 195 */ { "x" : 12486, "y" : 218, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 196 */ { "x" : 12486, "y" : 158, "bCoef" : 0.1, "cMask" : ["red" ] },
		/* 197 */ { "bCoef" : 0.1, "cMask" : ["red" ], "x" : 12526, "y" : 190 },
		/* 198 */ { "bCoef" : 0.1, "cMask" : ["red" ], "x" : 12486, "y" : 190 }

	],

	"segments" : [
		{ "v0" : 0, "v1" : 1, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "color" : "28EE9B" },
		{ "v0" : 2, "v1" : 3, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 4, "v1" : 5, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 6, "v1" : 7, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 8, "v1" : 9, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 11, "v1" : 10, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 12, "v1" : 13, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 14, "v1" : 15, "bCoef" : 0.1, "curve" : 75, "curveF" : 1.3032253728412058, "cMask" : ["red" ] },
		{ "v0" : 17, "v1" : 16, "bCoef" : 0.1, "curve" : 80.00000000000001, "curveF" : 1.19175359259421, "cMask" : ["red" ] },
		{ "v0" : 18, "v1" : 15, "bCoef" : 0.1, "curve" : 50, "curveF" : 2.1445069205095586, "cMask" : ["red" ] },
		{ "v0" : 14, "v1" : 18, "bCoef" : 0.1, "curve" : 50, "curveF" : 2.1445069205095586, "cMask" : ["red" ] },
		{ "v0" : 19, "v1" : 20, "bCoef" : 0.1, "curve" : 80.00000000000001, "curveF" : 1.19175359259421, "cMask" : ["red" ] },
		{ "v0" : 20, "v1" : 21, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 22, "v1" : 17, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 23, "v1" : 24, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 24, "v1" : 23, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 25, "v1" : 22, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 21, "v1" : 26, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 28, "v1" : 27, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 27, "v1" : 28, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 29, "v1" : 25, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 26, "v1" : 30, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 32, "v1" : 31, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 31, "v1" : 32, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 29, "v1" : 33, "bCoef" : 0.1, "curve" : 20, "curveF" : 5.671281819617709, "cMask" : ["red" ] },
		{ "v0" : 34, "v1" : 30, "bCoef" : 0.1, "curve" : 20, "curveF" : 5.671281819617709, "cMask" : ["red" ] },
		{ "v0" : 33, "v1" : 35, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 34, "v1" : 36, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 37, "v1" : 38, "bCoef" : -2.4, "vis" : false, "cMask" : ["red" ] },
		{ "v0" : 39, "v1" : 40, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 41, "v1" : 42, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 43, "v1" : 42, "bCoef" : 0.1, "curve" : 180, "curveF" : 6.123233995736766e-17, "cMask" : ["red" ] },
		{ "v0" : 44, "v1" : 40, "bCoef" : 0.1, "curve" : 180, "curveF" : 6.123233995736766e-17, "cMask" : ["red" ] },
		{ "v0" : 41, "v1" : 45, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 36, "v1" : 46, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 45, "v1" : 47, "bCoef" : 0.1, "curve" : 89.99999999999999, "curveF" : 1.0000000000000002, "cMask" : ["red" ] },
		{ "v0" : 47, "v1" : 43, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 44, "v1" : 48, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 46, "v1" : 48, "bCoef" : 0.1, "curve" : 89.99999999999999, "curveF" : 1.0000000000000002, "cMask" : ["red" ] },
		{ "v0" : 35, "v1" : 49, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 39, "v1" : 50, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 51, "v1" : 49, "bCoef" : 0.1, "curve" : 180, "curveF" : 6.123233995736766e-17, "cMask" : ["red" ] },
		{ "v0" : 52, "v1" : 50, "bCoef" : 0.1, "curve" : 180, "curveF" : 6.123233995736766e-17, "cMask" : ["red" ] },
		{ "v0" : 52, "v1" : 53, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 51, "v1" : 54, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 54, "v1" : 55, "bCoef" : 0.1, "curve" : 180, "curveF" : 6.123233995736766e-17, "cMask" : ["red" ] },
		{ "v0" : 53, "v1" : 56, "bCoef" : 0.1, "curve" : 180, "curveF" : 6.123233995736766e-17, "cMask" : ["red" ] },
		{ "v0" : 57, "v1" : 56, "bCoef" : 0.1, "curve" : 180, "curveF" : 6.123233995736766e-17, "cMask" : ["red" ] },
		{ "v0" : 58, "v1" : 55, "bCoef" : 0.1, "curve" : 180, "curveF" : 6.123233995736766e-17, "cMask" : ["red" ] },
		{ "v0" : 57, "v1" : 59, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 58, "v1" : 60, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 60, "v1" : 61, "bCoef" : 0.1, "curve" : 180, "curveF" : 6.123233995736766e-17, "cMask" : ["red" ] },
		{ "v0" : 59, "v1" : 62, "bCoef" : 0.1, "curve" : 180, "curveF" : 6.123233995736766e-17, "cMask" : ["red" ] },
		{ "v0" : 61, "v1" : 63, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 62, "v1" : 64, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 65, "v1" : 63, "bCoef" : 0.1, "curve" : 89.99999999999999, "curveF" : 1.0000000000000002, "cMask" : ["red" ] },
		{ "v0" : 66, "v1" : 64, "bCoef" : 0.1, "curve" : 89.99999999999999, "curveF" : 1.0000000000000002, "cMask" : ["red" ] },
		{ "v0" : 65, "v1" : 67, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 66, "v1" : 68, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 70, "v1" : 69, "bCoef" : 0.1, "curve" : 150, "curveF" : 0.2679491924311227, "cMask" : ["red" ] },
		{ "v0" : 70, "v1" : 69, "bCoef" : 0.1, "curve" : 100, "curveF" : 0.83909963117728, "cMask" : ["red" ] },
		{ "v0" : 71, "v1" : 67, "bCoef" : 0.1, "curve" : 50, "curveF" : 2.1445069205095586, "cMask" : ["red" ] },
		{ "v0" : 72, "v1" : 71, "bCoef" : 0.1, "curve" : -135, "curveF" : -0.414213562373095, "cMask" : ["red" ] },
		{ "v0" : 68, "v1" : 73, "bCoef" : 0.1, "curve" : 50, "curveF" : 2.1445069205095586, "cMask" : ["red" ] },
		{ "v0" : 73, "v1" : 74, "bCoef" : 0.1, "curve" : -135, "curveF" : -0.414213562373095, "cMask" : ["red" ] },
		{ "v0" : 72, "v1" : 75, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 74, "v1" : 76, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 75, "v1" : 77, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 76, "v1" : 78, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 77, "v1" : 79, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 78, "v1" : 80, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 80, "v1" : 81, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 79, "v1" : 82, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 81, "v1" : 83, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 82, "v1" : 84, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 83, "v1" : 85, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 84, "v1" : 86, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 86, "v1" : 87, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 85, "v1" : 88, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 89, "v1" : 90, "bCoef" : -2.4, "vis" : false, "cMask" : ["red" ] },
		{ "v0" : 87, "v1" : 91, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 88, "v1" : 92, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 91, "v1" : 93, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 92, "v1" : 94, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 95, "v1" : 96, "bCoef" : 0.1, "curve" : -140, "curveF" : -0.36397023426620234, "cMask" : ["red" ] },
		{ "v0" : 97, "v1" : 93, "bCoef" : 0.1, "curve" : -115, "curveF" : -0.6370702608074934, "cMask" : ["red" ] },
		{ "v0" : 94, "v1" : 98, "bCoef" : 0.1, "curve" : -115, "curveF" : -0.6370702608074934, "cMask" : ["red" ] },
		{ "v0" : 97, "v1" : 99, "bCoef" : 0.1, "curve" : 32, "curveF" : 3.4874144438409087, "cMask" : ["red" ] },
		{ "v0" : 100, "v1" : 98, "bCoef" : 0.1, "curve" : 32, "curveF" : 3.4874144438409087, "cMask" : ["red" ] },
		{ "v0" : 99, "v1" : 101, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 100, "v1" : 102, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 103, "v1" : 101, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 102, "v1" : 104, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 105, "v1" : 106, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 106, "v1" : 105, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 107, "v1" : 103, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 104, "v1" : 108, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 109, "v1" : 110, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 110, "v1" : 109, "bCoef" : 0.1, "curve" : 65, "curveF" : 1.5696855771174902, "cMask" : ["red" ] },
		{ "v0" : 111, "v1" : 112, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 107, "v1" : 113, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 113, "v1" : 114, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 114, "v1" : 115, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 108, "v1" : 116, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 116, "v1" : 117, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 117, "v1" : 118, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 119, "v1" : 120, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 117, "v1" : 121, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 121, "v1" : 122, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 114, "v1" : 123, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 123, "v1" : 124, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 127, "v1" : 125, "bCoef" : 0.1, "curve" : 150, "curveF" : 0.2679491924311227, "cMask" : ["red" ] },
		{ "v0" : 126, "v1" : 128, "bCoef" : 0.1, "curve" : 150, "curveF" : 0.2679491924311227, "cMask" : ["red" ] },
		{ "v0" : 129, "v1" : 130, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 131, "v1" : 132, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 129, "v1" : 132, "bCoef" : 0.1, "curve" : 180, "curveF" : 6.123233995736766e-17, "cMask" : ["red" ] },
		{ "v0" : 131, "v1" : 130, "bCoef" : 0.1, "curve" : 180, "curveF" : 6.123233995736766e-17, "cMask" : ["red" ] },
		{ "v0" : 127, "v1" : 133, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 128, "v1" : 134, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 133, "v1" : 135, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 134, "v1" : 136, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 137, "v1" : 138, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 139, "v1" : 138, "bCoef" : 0.1, "curve" : 180, "curveF" : 6.123233995736766e-17, "cMask" : ["red" ] },
		{ "v0" : 139, "v1" : 140, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 135, "v1" : 137, "bCoef" : 0.1, "curve" : 89.99999999999999, "curveF" : 1.0000000000000002, "cMask" : ["red" ] },
		{ "v0" : 136, "v1" : 140, "bCoef" : 0.1, "curve" : 89.99999999999999, "curveF" : 1.0000000000000002, "cMask" : ["red" ] },
		{ "v0" : 124, "v1" : 141, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 122, "v1" : 142, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 142, "v1" : 143, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 143, "v1" : 144, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 145, "v1" : 146, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 126, "v1" : 147, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 148, "v1" : 146, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 147, "v1" : 144, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 35, "v1" : 39, "bCoef" : 0.1, "cMask" : ["blue" ] },
		{ "v0" : 36, "v1" : 41, "bCoef" : 0.1, "cMask" : ["blue" ] },
		{ "v0" : 149, "v1" : 150, "bCoef" : -2.4, "vis" : false, "cMask" : ["red" ] },
		{ "v0" : 151, "v1" : 152, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 153, "v1" : 154, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 68, "v1" : 67, "bCoef" : 0.1, "cMask" : ["blue" ], "color" : "28EE9B" },
		{ "v0" : 94, "v1" : 93, "bCoef" : 0.1, "cMask" : ["blue" ], "color" : "28EE9B" },
		{ "v0" : 112, "v1" : 155, "bCoef" : 0.1, "cMask" : ["blue" ], "color" : "28EE9B" },
		{ "v0" : 119, "v1" : 156, "bCoef" : 0.1, "cMask" : ["blue" ], "color" : "28EE9B" },
		{ "v0" : 111, "v1" : 157, "bCoef" : 0.1, "cMask" : ["blue" ], "color" : "28EE9B" },
		{ "v0" : 120, "v1" : 158, "bCoef" : 0.1, "cMask" : ["blue" ], "color" : "28EE9B" },
		{ "v0" : 159, "v1" : 160, "bCoef" : 0.1, "cMask" : ["blue" ], "color" : "28EE9B" },
		{ "v0" : 161, "v1" : 162, "bCoef" : 0.1, "cMask" : ["blue" ], "color" : "28EE9B" },
		{ "v0" : 122, "v1" : 124, "bCoef" : 0.1, "cMask" : ["blue" ], "color" : "28EE9B" },
		{ "v0" : 134, "v1" : 133, "bCoef" : 0.1, "cMask" : ["blue" ], "color" : "28EE9B" },
		{ "v0" : 70, "v1" : 69, "bCoef" : 0.1, "curve" : 125.00000000000001, "curveF" : 0.5205670505517462, "cMask" : ["red" ] },
		{ "v0" : 163, "v1" : 15, "bCoef" : 0.1, "curve" : 40.107699911994004, "curveF" : 2.739463601532566, "cMask" : ["red" ] },
		{ "v0" : 14, "v1" : 163, "bCoef" : 0.1, "curve" : 40.107699911994004, "curveF" : 2.739463601532566, "cMask" : ["red" ] },
		{ "v0" : 164, "v1" : 15, "bCoef" : 0.1, "curve" : 40.107699911994004, "curveF" : 2.739463601532566, "cMask" : ["red" ] },
		{ "v0" : 14, "v1" : 164, "bCoef" : 0.1, "curve" : 40.107699911994004, "curveF" : 2.739463601532566, "cMask" : ["red" ] },
		{ "v0" : 165, "v1" : 166, "bCoef" : 0.1, "cMask" : ["red" ], "color" : "FFFFFF" },
		{ "v0" : 166, "v1" : 167, "bCoef" : 0.1, "cMask" : ["red" ], "color" : "FFFFFF", "y" : 180 },
		{ "v0" : 167, "v1" : 168, "bCoef" : 0.1, "cMask" : ["red" ], "color" : "FFFFFF", "x" : 12500 },
		{ "v0" : 165, "v1" : 169, "bCoef" : 0.1, "cMask" : ["red" ], "color" : "FFFFFF", "y" : 120 },
		{ "v0" : 169, "v1" : 170, "bCoef" : 0.1, "cMask" : ["red" ], "color" : "FFFFFF", "x" : 12500 },
		{ "v0" : 148, "v1" : 171, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 171, "v1" : 172, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 172, "v1" : 125, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 145, "v1" : 173, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 173, "v1" : 174, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 174, "v1" : 141, "bCoef" : 0.1, "cMask" : ["red" ] },
		{ "v0" : 175, "v1" : 176, "bCoef" : -2.4, "vis" : false, "cMask" : ["red" ] },
		{ "v0" : 177, "v1" : 178, "bCoef" : -2.3, "vis" : false, "cMask" : ["red" ] },
		{ "v0" : 132, "v1" : 129, "bCoef" : 0.1, "curve" : 180, "curveF" : 6.123233995736766e-17, "cMask" : ["red" ] },
		{ "v0" : 179, "v1" : 180, "bCoef" : 0.1, "curve" : 54.99999999999999, "curveF" : 1.920982126971166, "cMask" : ["red" ], "color" : "212356" },
		{ "v0" : 180, "v1" : 179, "bCoef" : 0.1, "curve" : 54.99999999999999, "curveF" : 1.920982126971166, "cMask" : ["red" ], "color" : "212356" },
		{ "v0" : 181, "v1" : 182, "bCoef" : 0.1, "curve" : 54.99999999999999, "curveF" : 1.920982126971166, "cMask" : ["red" ], "color" : "212356" },
		{ "v0" : 182, "v1" : 181, "bCoef" : 0.1, "curve" : 54.99999999999999, "curveF" : 1.920982126971166, "cMask" : ["red" ], "color" : "212356" },
		{ "v0" : 183, "v1" : 184, "bCoef" : 0.1, "curve" : 54.99999999999999, "curveF" : 1.920982126971166, "cMask" : ["red" ], "color" : "212356" },
		{ "v0" : 184, "v1" : 183, "bCoef" : 0.1, "curve" : 54.99999999999999, "curveF" : 1.920982126971166, "cMask" : ["red" ], "color" : "212356" },
		{ "v0" : 185, "v1" : 186, "bCoef" : 0.1, "curve" : 54.99999999999999, "curveF" : 1.920982126971166, "cMask" : ["red" ], "color" : "212356" },
		{ "v0" : 186, "v1" : 185, "bCoef" : 0.1, "curve" : 54.99999999999999, "curveF" : 1.920982126971166, "cMask" : ["red" ], "color" : "212356" },
		{ "v0" : 187, "v1" : 188, "bCoef" : 0.1, "curve" : 54.99999999999999, "curveF" : 1.920982126971166, "cMask" : ["red" ], "color" : "212356" },
		{ "v0" : 188, "v1" : 187, "bCoef" : 0.1, "curve" : 54.99999999999999, "curveF" : 1.920982126971166, "cMask" : ["red" ], "color" : "212356" },
		{ "color" : "FFFFFF", "bCoef" : 0.1, "cMask" : ["red" ], "v0" : 168, "v1" : 189, "y" : 160 },
		{ "v0" : 190, "v1" : 191, "bCoef" : 0.1, "cMask" : ["red" ], "color" : "FFFFFF" },
		{ "v0" : 191, "v1" : 192, "bCoef" : 0.1, "cMask" : ["red" ], "color" : "FFFFFF", "y" : 180 },
		{ "v0" : 193, "v1" : 194, "bCoef" : 0.1, "cMask" : ["red" ], "color" : "FFFFFF" },
		{ "v0" : 195, "v1" : 196, "bCoef" : 0.1, "cMask" : ["red" ], "color" : "FFFFFF" },
		{ "color" : "FFFFFF", "bCoef" : 0.1, "cMask" : ["red" ], "v0" : 197, "v1" : 198, "y" : 160 }

	],

	"planes" : [
		{ "normal" : [1,0 ], "dist" : -15000, "bCoef" : 0.1 },
		{ "normal" : [0,1 ], "dist" : -800, "bCoef" : 0.1 },
		{ "normal" : [0,-1 ], "dist" : -800, "bCoef" : 0.1 },
		{ "normal" : [-1,0 ], "dist" : -15000, "bCoef" : 0.1 }

	],

	"goals" : [
		

	],

	"discs" : [
		{ "pos" : [-1700,0 ], "speed" : [4,0 ], "radius" : 20, "bCoef" : 0.1, "invMass" : 1e-9, "damping" : 1, "color" : "0", "cGroup" : ["wall" ] },
		{ "pos" : [8996.25,-356.25 ], "radius" : 75, "bCoef" : 0.7, "invMass" : 0, "damping" : 0, "color" : "742C62", "cMask" : ["red" ] },
		{ "pos" : [8835.25,-514.25 ], "radius" : 75, "bCoef" : 0.7, "invMass" : 0, "damping" : 0, "color" : "401D37", "cMask" : ["red" ] },
		{ "pos" : [9081.25,-611.25 ], "radius" : 75, "bCoef" : 0.7, "invMass" : 0, "damping" : 0, "color" : "6F3B62", "cMask" : ["red" ] },
		{ "pos" : [9282.25,-448.25 ], "radius" : 75, "bCoef" : 0.7, "invMass" : 0, "damping" : 0, "color" : "5A214C", "cMask" : ["red" ] },
		{ "pos" : [9513.25,-362.25 ], "radius" : 75, "bCoef" : 0.7, "invMass" : 0, "damping" : 0, "color" : "6F3B62", "cMask" : ["red" ] },
		{ "pos" : [9445.25,-612.25 ], "radius" : 75, "bCoef" : 0.7, "invMass" : 0, "damping" : 0, "color" : "401D37", "cMask" : ["red" ] },
		{ "pos" : [9720,-517.25 ], "radius" : 75, "bCoef" : 0.7, "invMass" : 0, "damping" : 0, "color" : "742C62", "cMask" : ["red" ] },
		{ "pos" : [9875,-356.25 ], "radius" : 75, "bCoef" : 0.7, "invMass" : 0, "damping" : 0, "color" : "401D37", "cMask" : ["red" ] },
		{ "pos" : [9933,-613.25 ], "radius" : 75, "bCoef" : 0.7, "invMass" : 0, "damping" : 0, "color" : "5A214C", "cMask" : ["red" ] },
		{ "pos" : [10182,-520.25 ], "radius" : 75, "bCoef" : 0.7, "invMass" : 0, "damping" : 0, "color" : "401D37", "cMask" : ["red" ] },
		{ "pos" : [10175,-358.25 ], "radius" : 75, "bCoef" : 0.7, "invMass" : 0, "damping" : 0, "color" : "742C62", "cMask" : ["red" ] },
		{ "pos" : [10434.5,-465.25 ], "radius" : 75, "bCoef" : 0.7, "invMass" : 0, "damping" : 0, "color" : "5A214C", "cMask" : ["red" ] },
		{ "pos" : [-13210,285 ], "radius" : 40, "bCoef" : 0.7, "invMass" : 0, "damping" : 0, "color" : "0", "cMask" : ["red" ] },
		{ "pos" : [-13210,-285 ], "radius" : 40, "bCoef" : 0.7, "invMass" : 0, "damping" : 0, "color" : "0", "cMask" : ["red" ] }

	],

	"playerPhysics" : {
		"damping" : 0.9995,
		"acceleration" : 0.025,
		"kickingAcceleration" : 0.0175,
		"kickingDamping" : 0.9995,
		"kickStrength" : 0

	},

	"spawnDistance" : 14900,

	"traits" : {
		

	}
}`;

var MundialitoGLH=`
{

	"name" : "🥅 𝐌𝐔𝐍𝐃𝐈𝐀𝐋𝐈𝐓𝐎 ⚽",

	"width" : 620,

	"height" : 400,

	"redSpawnPoints" : [
		[ -562, 0
		]

	],

	"blueSpawnPoints" : [
		[ 28, -139
		],
		[ 72, -120
		],
		[ 107, -94
		],
		[ 133, -54
		],
		[ 133, 0
		],
		[ 133, 54
		],
		[ 107, 94
		],
		[ 72, 120
		],
		[ 28, 139
		]

	],

	"bg" : { "type" : "grass", "width" : 0, "height" : 0, "kickOffRadius" : 0, "color" : "558d74" },

	"vertexes" : [
		/* 0 */ { "x" : -570, "y" : 161, "bCoef" : 2.1, "cMask" : ["blue","ball" ], "cGroup" : ["ball" ] },
		/* 1 */ { "x" : -570, "y" : 92, "bCoef" : 0.1, "cMask" : ["blue","ball" ], "color" : "2e2b8f" },
		/* 2 */ { "x" : -570, "y" : -92, "bCoef" : 0.1, "cMask" : ["blue","ball" ], "color" : "2e2b8f" },
		/* 3 */ { "x" : 569, "y" : 169, "bCoef" : 2.1, "cMask" : ["red","ball" ] },
		/* 4 */ { "x" : 569, "y" : -91, "bCoef" : 2.1, "cMask" : ["red","ball" ] },
		/* 5 */ { "x" : -598, "y" : -91, "bCoef" : 0.1, "cMask" : ["ball" ], "color" : "2e2b8f" },
		/* 6 */ { "x" : -597, "y" : 91, "bCoef" : 0.1, "cMask" : ["ball" ], "color" : "2e2b8f" },
		/* 7 */ { "x" : -621, "y" : 163, "bCoef" : 2.1, "cMask" : ["blue","ball" ] },
		/* 8 */ { "x" : 619, "y" : 169, "bCoef" : 2.1, "cMask" : ["red","ball" ] },
		/* 9 */ { "x" : 569, "y" : -160, "bCoef" : 2.1, "cMask" : ["red","ball" ] },
		/* 10 */ { "x" : 619, "y" : -160, "bCoef" : 2.1, "cMask" : ["red","ball" ] },
		/* 11 */ { "x" : -570, "y" : -160, "bCoef" : 2.1, "cMask" : ["blue","ball" ] },
		/* 12 */ { "x" : -620, "y" : -159, "bCoef" : 2.1, "cMask" : ["blue","ball" ] },
		/* 13 */ { "x" : 569, "y" : 169, "bCoef" : 2.1, "cMask" : ["red","ball" ] },
		/* 14 */ { "x" : 569, "y" : 90, "bCoef" : 2.1, "cMask" : ["red","ball" ] },
		/* 15 */ { "x" : 570, "y" : -106, "bCoef" : 2.1, "cMask" : ["red","ball" ] },
		/* 16 */ { "x" : 569, "y" : -158, "bCoef" : 2.1, "cMask" : ["red","ball" ] },
		/* 17 */ { "x" : 569, "y" : -90, "bCoef" : 2.1, "cMask" : ["ball" ], "color" : "ffffff" },
		/* 18 */ { "x" : 569, "y" : 89, "bCoef" : 2.1, "cMask" : ["ball" ], "color" : "ffffff" },
		/* 19 */ { "x" : -570, "y" : -159, "bCoef" : 2.1, "cMask" : ["blue" ], "color" : "ffffff", "curve" : 90 },
		/* 20 */ { "x" : -470, "y" : -84, "bCoef" : 2.1, "cMask" : ["blue" ], "color" : "ffffff", "curve" : 90 },
		/* 21 */ { "x" : -570, "y" : 160, "bCoef" : 2.1, "cMask" : ["blue" ], "color" : "ffffff", "curve" : 90 },
		/* 22 */ { "x" : -470, "y" : 84, "bCoef" : 2.1, "cMask" : ["blue" ], "color" : "ffffff", "curve" : 90 },
		/* 23 */ { "x" : 570, "y" : -160, "bCoef" : 2.1, "cMask" : ["red","blue" ] },
		/* 24 */ { "x" : 569, "y" : 168, "bCoef" : 2.1, "cMask" : ["red","blue" ] },
		/* 25 */ { "x" : -570, "y" : -92, "bCoef" : 2.1, "cMask" : ["blue","ball" ], "cGroup" : ["ball" ] },
		/* 26 */ { "x" : 569, "y" : 169, "bCoef" : 4, "cMask" : ["red","ball" ], "cGroup" : ["ball" ], "curve" : 0, "color" : "ffffff" },
		/* 27 */ { "x" : 569, "y" : -159, "bCoef" : 4, "cMask" : ["red","ball" ], "cGroup" : ["ball" ], "curve" : 0, "color" : "ffffff" },
		/* 28 */ { "x" : -570, "y" : -160, "bCoef" : 2.1, "cMask" : ["blue","ball" ] },
		/* 29 */ { "x" : 570.5, "y" : -269, "cMask" : ["red","ball" ], "cGroup" : ["red" ], "color" : "ffffff" },
		/* 30 */ { "x" : 570.5, "y" : 270, "cMask" : ["red","ball" ], "color" : "ffffff" },
		/* 31 */ { "x" : -570, "y" : 268, "cMask" : ["blue","ball" ], "color" : "ffffff" },
		/* 32 */ { "x" : -570, "y" : -269, "cMask" : ["blue","ball" ], "cGroup" : ["red" ], "color" : "ffffff" },
		/* 33 */ { "x" : -570, "y" : -160, "bCoef" : 2.1, "cMask" : ["blue","ball" ] },
		/* 34 */ { "x" : -570, "y" : -92, "bCoef" : 2.1, "cMask" : ["blue","ball" ], "cGroup" : ["ball" ] },
		/* 35 */ { "x" : -570, "y" : -160, "bCoef" : 2.1, "cMask" : ["blue","ball" ] },
		/* 36 */ { "x" : -436, "y" : -20, "bCoef" : 2.1, "cMask" : [ ], "color" : "ffffff" },
		/* 37 */ { "x" : -436, "y" : 20, "bCoef" : 2.1, "cMask" : [ ], "color" : "ffffff" },
		/* 38 */ { "x" : -570, "y" : -233, "bCoef" : 2.1, "cMask" : [ ], "color" : "fdd947", "curve" : 90 },
		/* 39 */ { "x" : -406, "y" : -84, "bCoef" : 2.1, "cMask" : [ ], "color" : "fdd947", "curve" : 90 },
		/* 40 */ { "x" : -406, "y" : -84, "bCoef" : 2.1, "cMask" : [ ] },
		/* 41 */ { "x" : -408, "y" : 85, "bCoef" : 2.1, "cMask" : [ ] },
		/* 42 */ { "x" : -570, "y" : 233, "bCoef" : 2.1, "cMask" : [ ], "color" : "fdd947", "curve" : 90 },
		/* 43 */ { "x" : -408, "y" : 85, "bCoef" : 2.1, "cMask" : [ ], "color" : "fdd947", "curve" : 90 },
		/* 44 */ { "x" : -570, "y" : -165, "color" : "ffffff" },
		/* 45 */ { "x" : -570, "y" : -92, "cMask" : [ ], "color" : "ffffff" },
		/* 46 */ { "x" : 569, "y" : -106, "bCoef" : 6, "cMask" : ["ball" ] },
		/* 47 */ { "x" : 569, "y" : 106, "bCoef" : 6, "cMask" : ["ball" ] },
		/* 48 */ { "x" : -570, "y" : 92, "cMask" : [ ], "color" : "ffffff" },
		/* 49 */ { "x" : -570, "y" : 268, "cMask" : ["blue","ball" ], "color" : "ffffff" },
		/* 50 */ { "x" : 0, "y" : 270, "bCoef" : 2.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ] },
		/* 51 */ { "x" : 0, "y" : -269, "bCoef" : 2.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ] },
		/* 52 */ { "x" : 0, "y" : -268, "bCoef" : 2.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ] },
		/* 53 */ { "x" : 0, "y" : 269, "bCoef" : 2.1, "cMask" : ["wall" ], "color" : "ffffff" },
		/* 54 */ { "x" : -406, "y" : -84, "bCoef" : 2.1, "cMask" : [ ], "color" : "fdd947" },
		/* 55 */ { "x" : -408, "y" : 84, "bCoef" : 2.1, "cMask" : [ ], "color" : "fdd947" },
		/* 56 */ { "x" : 0, "y" : 50.33332824707031, "bCoef" : 0.1, "cMask" : ["wall" ], "cGroup" : ["redKO","blueKO" ], "color" : "ffffff" },
		/* 57 */ { "x" : 0, "y" : -50, "bCoef" : 2.1, "cMask" : ["wall" ], "color" : "ffffff" },
		/* 58 */ { "x" : 0, "y" : -269.6666717529297, "bCoef" : 0.1, "cMask" : ["wall" ], "cGroup" : ["redKO","blueKO" ], "color" : "ffffff" },
		/* 59 */ { "x" : 0, "y" : 50.33332824707031, "bCoef" : 0.1, "cMask" : ["wall" ], "cGroup" : ["redKO","blueKO" ], "color" : "ffffff" },
		/* 60 */ { "x" : 0, "y" : -50, "bCoef" : 2.1, "cMask" : ["wall" ], "color" : "ffffff" },
		/* 61 */ { "bCoef" : 4, "cMask" : ["ball" ], "x" : 490, "y" : -267.49609375, "curve" : 0, "color" : "ffffff" },
		/* 62 */ { "x" : 490, "y" : 269.00390625, "curve" : 0, "color" : "ffffff", "bCoef" : 4 }

	],

	"segments" : [
		{ "v0" : 0, "v1" : 1, "bCoef" : 2.1, "vis" : false, "cMask" : ["blue","ball" ], "x" : -570 },
		{ "v0" : 6, "v1" : 5, "bCoef" : 0.1, "curve" : 29.999999999999996, "curveF" : 3.7320508075688776, "cMask" : ["ball" ], "color" : "2e2b8f" },
		{ "v0" : 6, "v1" : 1, "bCoef" : 0.1, "cMask" : ["ball" ], "color" : "2e2b8f" },
		{ "v0" : 5, "v1" : 2, "bCoef" : 0.1, "cMask" : ["ball" ], "color" : "2e2b8f" },
		{ "v0" : 0, "v1" : 7, "bCoef" : 2.1, "vis" : false, "cMask" : ["blue","ball" ] },
		{ "v0" : 3, "v1" : 8, "bCoef" : 2.1, "vis" : false, "cMask" : ["red","ball" ] },
		{ "v0" : 9, "v1" : 10, "bCoef" : 2.1, "vis" : false, "cMask" : ["red","ball" ] },
		{ "v0" : 11, "v1" : 12, "bCoef" : 2.1, "vis" : false, "cMask" : ["blue","ball" ] },
		{ "v0" : 13, "v1" : 14, "bCoef" : 2.1, "vis" : false, "cMask" : ["red","ball" ], "color" : "CCCCFF" },
		{ "v0" : 15, "v1" : 16, "bCoef" : 2.1, "vis" : false, "cMask" : ["red","ball" ], "color" : "CCCCFF" },
		{ "v0" : 17, "v1" : 18, "bCoef" : 2.1, "cMask" : ["ball" ], "color" : "ffffff" },
		{ "v0" : 19, "v1" : 20, "bCoef" : 2.1, "curve" : 90, "curveF" : 1.1716157205240172, "cMask" : ["blue" ], "color" : "ffffff" },
		{ "v0" : 22, "v1" : 21, "bCoef" : 2.1, "curve" : 90, "curveF" : 1.0000000000000002, "cMask" : ["blue" ], "color" : "ffffff" },
		{ "v0" : 20, "v1" : 22, "bCoef" : 2.1, "cMask" : ["blue" ], "color" : "ffffff" },
		{ "v0" : 29, "v1" : 27, "bCoef" : 2.1, "vis" : false, "cMask" : ["red","ball" ] },
		{ "v0" : 26, "v1" : 30, "bCoef" : 2.1, "vis" : false, "cMask" : ["red","ball" ] },
		{ "v0" : 0, "v1" : 31, "bCoef" : 2.1, "vis" : false, "cMask" : ["blue","ball" ], "x" : -570 },
		{ "v0" : 32, "v1" : 33, "bCoef" : 2.1, "vis" : false, "cMask" : ["blue","ball" ], "x" : -570 },
		{ "v0" : 34, "v1" : 35, "bCoef" : 2.1, "vis" : false, "cMask" : ["blue","ball" ], "x" : -570 },
		{ "v0" : 36, "v1" : 37, "bCoef" : 2.1, "cMask" : [ ], "color" : "ffffff" },
		{ "v0" : 38, "v1" : 39, "bCoef" : 2.1, "curve" : 90, "curveF" : 1.0000000000000002, "cMask" : [ ], "color" : "fdd947" },
		{ "v0" : 40, "v1" : 41, "bCoef" : 2.1, "cMask" : [ ], "color" : "FFFF" },
		{ "v0" : 43, "v1" : 42, "bCoef" : 2.1, "curve" : 90, "curveF" : 1.0000000000000002, "cMask" : [ ], "color" : "fdd947" },
		{ "v0" : 31, "v1" : 30, "cMask" : ["redKO","blueKO" ], "cGroup" : ["ball" ], "color" : "ffffff" },
		{ "v0" : 30, "v1" : 18, "bCoef" : 2.1, "cMask" : ["ball" ], "color" : "ffffff" },
		{ "v0" : 17, "v1" : 29, "bCoef" : 2.1, "color" : "ffffff" },
		{ "v0" : 32, "v1" : 29, "cMask" : ["ball" ], "cGroup" : ["red" ], "color" : "ffffff" },
		{ "v0" : 32, "v1" : 44, "color" : "ffffff", "x" : -570 },
		{ "v0" : 44, "v1" : 45, "color" : "ffffff", "x" : -570 },
		{ "v0" : 1, "v1" : 31, "bCoef" : 2.1, "color" : "33FF00", "x" : -570 },
		{ "v0" : 47, "v1" : 46, "bCoef" : 6, "curve" : 63.89006659739183, "curveF" : 1.6037560959448722, "cMask" : ["ball" ], "color" : "901010" },
		{ "v0" : 48, "v1" : 49, "color" : "ffffff", "x" : -570 },
		{ "v0" : 54, "v1" : 55, "bCoef" : 2.1, "cMask" : [ ], "color" : "fdd947" },
		{ "v0" : 56, "v1" : 53, "bCoef" : 0.1, "cMask" : ["wall" ], "cGroup" : ["redKO","blueKO" ], "color" : "ffffff" },
		{ "v0" : 56, "v1" : 56, "vis" : false, "cMask" : ["ball" ] },
		{ "v0" : 58, "v1" : 57, "bCoef" : 0.1, "cMask" : ["wall" ], "cGroup" : ["redKO","blueKO" ], "color" : "ffffff" },
		{ "v0" : 57, "v1" : 56, "bCoef" : 2.1, "curve" : 178.85793417458243, "curveF" : 0.009966734462186898, "cMask" : ["wall" ], "color" : "ffffff" },
		{ "v0" : 59, "v1" : 60, "bCoef" : 2.1, "curve" : 178.85793417458243, "curveF" : 0.009966734462186898, "cMask" : ["wall" ], "color" : "ffffff" },
		{ "curve" : 0, "color" : "ffffff", "bCoef" : 4, "cMask" : ["ball" ], "v0" : 27, "v1" : 61 },
		{ "curve" : 0, "color" : "ffffff", "v0" : 26, "v1" : 62, "bCoef" : 4 },
		{ "color" : "ffffff", "bCoef" : 2.1, "cMask" : [ ], "v0" : 48, "v1" : 45, "x" : -570 }

	],

	"planes" : [
		{ "normal" : [0,1 ], "dist" : -270, "bCoef" : 2.1, "cMask" : ["ball" ] },
		{ "normal" : [0,-1 ], "dist" : -270, "bCoef" : 2.1, "cMask" : ["ball" ] },
		{ "normal" : [0,1 ], "dist" : -305, "bCoef" : 2.1, "cMask" : ["red","blue" ] },
		{ "normal" : [0,-1 ], "dist" : -297, "bCoef" : 2.1, "cMask" : ["red","blue" ] },
		{ "normal" : [1,0 ], "dist" : -620, "bCoef" : 2.1, "cMask" : ["red","blue" ] },
		{ "normal" : [-1,0 ], "dist" : -617, "bCoef" : 2.1, "cMask" : ["red","blue" ] }

	],

	"goals" : [
		{ "p0" : [-580,-90 ], "p1" : [-580,90 ], "team" : "red" }

	],

	"discs" : [
		{ "color" : "DDDDDD", "cGroup" : ["ball","kick","score" ] },
		{ "pos" : [-570,92 ], "radius" : 8, "bCoef" : 2.1, "invMass" : 0, "color" : "8b88ff" },
		{ "pos" : [-570,-92 ], "radius" : 8, "bCoef" : 2.1, "invMass" : 0, "color" : "8b88ff" }

	],

	"playerPhysics" : {
		"bCoef" : 0.1

	},
	"ballPhysics" : "disc0",
	"traits" : {
		

	}
}`;
var Futsalx3=`
{

	"name" : "\ud835\udcd5\ud835\ude6a\ud835\ude69\ud835\ude68\ud835\ude56\ud835\ude61 \ud835\udc99\u01b7 \ufe54\ud835\udcd1\ud835\udd02 \ud835\ude71\ud835\ude8a\ud835\udea3\ud835\ude92\ud835\ude97\ud835\ude90\ud835\ude8a\u2757 \u0026 \ud835\udc06\ud835\udc0b\ud835\udc07",

	"width" : 620,

	"height" : 270,

	"spawnDistance" : 350,

	"bg" : { "type" : "hockey", "width" : 550, "height" : 240, "kickOffRadius" : 80, "cornerRadius" : 0 },

	"vertexes" : [
		/* 0 */ { "x" : 550, "y" : 240, "trait" : "ballArea" },
		/* 1 */ { "x" : 550, "y" : -240, "trait" : "ballArea" },
		
		/* 2 */ { "x" : 0, "y" : 270, "trait" : "kickOffBarrier" },
		/* 3 */ { "x" : 0, "y" : 80, "bCoef" : 0.15, "trait" : "kickOffBarrier", "color" : "F8F8F8", "vis" : true, "curve" : 180 },
		/* 4 */ { "x" : 0, "y" : -80, "bCoef" : 0.15, "trait" : "kickOffBarrier", "color" : "F8F8F8", "vis" : true, "curve" : 180 },
		/* 5 */ { "x" : 0, "y" : -270, "trait" : "kickOffBarrier" },
		
		/* 6 */ { "x" : -550, "y" : -80, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [-700,-80 ] },
		/* 7 */ { "x" : -590, "y" : -80, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [-700,-80 ] },
		/* 8 */ { "x" : -590, "y" : 80, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [-700,80 ] },
		/* 9 */ { "x" : -550, "y" : 80, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [-700,80 ] },
		/* 10 */ { "x" : 550, "y" : -80, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [700,-80 ] },
		/* 11 */ { "x" : 590, "y" : -80, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [700,-80 ] },
		/* 12 */ { "x" : 590, "y" : 80, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [700,80 ] },
		/* 13 */ { "x" : 550, "y" : 80, "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "curve" : 0, "color" : "F8F8F8", "pos" : [700,80 ] },
		
		/* 14 */ { "x" : -550, "y" : 80, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [-700,80 ] },
		/* 15 */ { "x" : -550, "y" : 240, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8" },
		/* 16 */ { "x" : -550, "y" : -80, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [-700,-80 ] },
		/* 17 */ { "x" : -550, "y" : -240, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8" },
		/* 18 */ { "x" : -550, "y" : 240, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea" },
		/* 19 */ { "x" : 550, "y" : 240, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea" },
		/* 20 */ { "x" : 550, "y" : 80, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "pos" : [700,80 ] },
		/* 21 */ { "x" : 550, "y" : 240, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea" },
		/* 22 */ { "x" : 550, "y" : -240, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8" },
		/* 23 */ { "x" : 550, "y" : -80, "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [700,-80 ] },
		/* 24 */ { "x" : 550, "y" : -240, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea" },
		/* 25 */ { "x" : 550, "y" : -240, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea" },
		/* 26 */ { "x" : -550, "y" : -240, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0 },
		/* 27 */ { "x" : 550, "y" : -240, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0 },
		
		/* 28 */ { "x" : 0, "y" : -240, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier" },
		/* 29 */ { "x" : 0, "y" : -80, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier" },
		/* 30 */ { "x" : 0, "y" : 80, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier" },
		/* 31 */ { "x" : 0, "y" : 240, "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier" },
		/* 32 */ { "x" : 0, "y" : -80, "bCoef" : 0.1, "cMask" : ["red","blue" ], "trait" : "kickOffBarrier", "vis" : true, "color" : "F8F8F8" },
		/* 33 */ { "x" : 0, "y" : 80, "bCoef" : 0.1, "cMask" : ["red","blue" ], "trait" : "kickOffBarrier", "vis" : true, "color" : "F8F8F8" },
		/* 34 */ { "x" : 0, "y" : 80, "trait" : "kickOffBarrier", "color" : "F8F8F8", "vis" : true, "curve" : -180 },
		/* 35 */ { "x" : 0, "y" : -80, "trait" : "kickOffBarrier", "color" : "F8F8F8", "vis" : true, "curve" : -180 },
		/* 36 */ { "x" : 0, "y" : 80, "trait" : "kickOffBarrier", "color" : "F8F8F8", "vis" : true, "curve" : 0 },
		/* 37 */ { "x" : 0, "y" : -80, "trait" : "kickOffBarrier", "color" : "F8F8F8", "vis" : true, "curve" : 0 },
		
		/* 38 */ { "x" : -557.5, "y" : 80, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "vis" : false, "pos" : [-700,80 ] },
		/* 39 */ { "x" : -557.5, "y" : 240, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "vis" : false },
		/* 40 */ { "x" : -557.5, "y" : -240, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false, "curve" : 0 },
		/* 41 */ { "x" : -557.5, "y" : -80, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false, "curve" : 0, "pos" : [-700,-80 ] },
		/* 42 */ { "x" : 557.5, "y" : -240, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false, "curve" : 0 },
		/* 43 */ { "x" : 557.5, "y" : -80, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false, "curve" : 0, "pos" : [700,-80 ] },
		/* 44 */ { "x" : 557.5, "y" : 80, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "vis" : false, "pos" : [700,80 ] },
		/* 45 */ { "x" : 557.5, "y" : 240, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "vis" : false },
		
		/* 46 */ { "x" : 0, "y" : -80, "bCoef" : 0.1, "trait" : "line" },
		/* 47 */ { "x" : 0, "y" : 80, "bCoef" : 0.1, "trait" : "line" },
		/* 48 */ { "x" : -550, "y" : -80, "bCoef" : 0.1, "trait" : "line" },
		/* 49 */ { "x" : -550, "y" : 80, "bCoef" : 0.1, "trait" : "line" },
		/* 50 */ { "x" : 550, "y" : -80, "bCoef" : 0.1, "trait" : "line" },
		/* 51 */ { "x" : 550, "y" : 80, "bCoef" : 0.1, "trait" : "line" },
		/* 52 */ { "x" : -550, "y" : 200, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : -90 },
		/* 53 */ { "x" : -390, "y" : 70, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 0 },
		/* 54 */ { "x" : -550, "y" : 226, "bCoef" : 0.1, "trait" : "line", "curve" : -90 },
		/* 55 */ { "x" : -536, "y" : 240, "bCoef" : 0.1, "trait" : "line", "curve" : -90 },
		/* 56 */ { "x" : -550, "y" : -200, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 90 },
		/* 57 */ { "x" : -390, "y" : -70, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 0 },
		/* 58 */ { "x" : -550, "y" : -226, "bCoef" : 0.1, "trait" : "line", "curve" : 90 },
		/* 59 */ { "x" : -536, "y" : -240, "bCoef" : 0.1, "trait" : "line", "curve" : 90 },
		/* 60 */ { "x" : -381, "y" : -240, "bCoef" : 0.1, "trait" : "line" },
		/* 61 */ { "x" : 550, "y" : -226, "bCoef" : 0.1, "trait" : "line", "curve" : -90 },
		/* 62 */ { "x" : 536, "y" : -240, "bCoef" : 0.1, "trait" : "line", "curve" : -90 },
		/* 63 */ { "x" : 550, "y" : 226, "bCoef" : 0.1, "trait" : "line", "curve" : 90 },
		/* 64 */ { "x" : 536, "y" : 240, "bCoef" : 0.1, "trait" : "line", "curve" : 90 },
		/* 65 */ { "x" : 550, "y" : 200, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 90 },
		/* 66 */ { "x" : 390, "y" : 70, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 90 },
		/* 67 */ { "x" : 550, "y" : -200, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : -90 },
		/* 68 */ { "x" : 390, "y" : -70, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : -90 },
		/* 69 */ { "x" : 390, "y" : 70, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 0 },
		/* 70 */ { "x" : 390, "y" : -70, "bCoef" : 0.1, "trait" : "line", "color" : "F8F8F8", "curve" : 0 },
		/* 71 */ { "x" : -375, "y" : 1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 72 */ { "x" : -375, "y" : -1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 73 */ { "x" : -375, "y" : 3, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 74 */ { "x" : -375, "y" : -3, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 75 */ { "x" : -375, "y" : -2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 76 */ { "x" : -375, "y" : 2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 77 */ { "x" : -375, "y" : -3.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 78 */ { "x" : -375, "y" : 3.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 79 */ { "x" : 375, "y" : 1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 80 */ { "x" : 375, "y" : -1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 81 */ { "x" : 375, "y" : 3, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 82 */ { "x" : 375, "y" : -3, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 83 */ { "x" : 375, "y" : -2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 84 */ { "x" : 375, "y" : 2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 85 */ { "x" : 375, "y" : -3.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 86 */ { "x" : 375, "y" : 3.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 87 */ { "x" : -277.5, "y" : 1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 88 */ { "x" : -277.5, "y" : -1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 89 */ { "x" : -277.5, "y" : 3, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 90 */ { "x" : -277.5, "y" : -3, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 91 */ { "x" : -277.5, "y" : -2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 92 */ { "x" : -277.5, "y" : 2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 93 */ { "x" : -277.5, "y" : -3.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 94 */ { "x" : -277.5, "y" : 3.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 95 */ { "x" : 277.5, "y" : 1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 96 */ { "x" : 277.5, "y" : -1, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 97 */ { "x" : 277.5, "y" : 3, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 98 */ { "x" : 277.5, "y" : -3, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 99 */ { "x" : 277.5, "y" : -2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 100 */ { "x" : 277.5, "y" : 2, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 101 */ { "x" : 277.5, "y" : -3.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 102 */ { "x" : 277.5, "y" : 3.5, "bCoef" : 0.1, "trait" : "line", "curve" : 180 },
		/* 103 */ { "x" : -240, "y" : 224, "bCoef" : 0.1, "trait" : "line" },
		/* 104 */ { "x" : -240, "y" : 256, "bCoef" : 0.1, "trait" : "line" },
		/* 105 */ { "x" : -120, "y" : 224, "bCoef" : 0.1, "trait" : "line" },
		/* 106 */ { "x" : -120, "y" : 256, "bCoef" : 0.1, "trait" : "line" },
		/* 107 */ { "x" : 240, "y" : 224, "bCoef" : 0.1, "trait" : "line" },
		/* 108 */ { "x" : 240, "y" : 256, "bCoef" : 0.1, "trait" : "line" },
		/* 109 */ { "x" : 120, "y" : 224, "bCoef" : 0.1, "trait" : "line" },
		/* 110 */ { "x" : 120, "y" : 256, "bCoef" : 0.1, "trait" : "line" },
		/* 111 */ { "x" : -381, "y" : 240, "bCoef" : 0.1, "trait" : "line" },
		/* 112 */ { "x" : -381, "y" : 256, "bCoef" : 0.1, "trait" : "line" },
		/* 113 */ { "x" : -556, "y" : 123, "bCoef" : 0.1, "trait" : "line" },
		/* 114 */ { "x" : -575, "y" : 123, "bCoef" : 0.1, "trait" : "line" },
		/* 115 */ { "x" : 556, "y" : 123, "bCoef" : 0.1, "trait" : "line" },
		/* 116 */ { "x" : 575, "y" : 123, "bCoef" : 0.1, "trait" : "line" },
		/* 117 */ { "x" : -556, "y" : -123, "bCoef" : 0.1, "trait" : "line" },
		/* 118 */ { "x" : -575, "y" : -123, "bCoef" : 0.1, "trait" : "line" },
		/* 119 */ { "x" : 556, "y" : -123, "bCoef" : 0.1, "trait" : "line" },
		/* 120 */ { "x" : 575, "y" : -123, "bCoef" : 0.1, "trait" : "line" },
		/* 121 */ { "x" : -381, "y" : -240, "bCoef" : 0.1, "trait" : "line" },
		/* 122 */ { "x" : -381, "y" : -256, "bCoef" : 0.1, "trait" : "line" },
		/* 123 */ { "x" : 381, "y" : 240, "bCoef" : 0.1, "trait" : "line" },
		/* 124 */ { "x" : 381, "y" : 256, "bCoef" : 0.1, "trait" : "line" },
		/* 125 */ { "x" : 381, "y" : -240, "bCoef" : 0.1, "trait" : "line" },
		/* 126 */ { "x" : 381, "y" : -256, "bCoef" : 0.1, "trait" : "line" },
		
		/* 127 */ { "x" : 553, "y" : -240, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "vis" : false },
		/* 128 */ { "x" : 553, "y" : -80, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [700,-80 ], "vis" : false },
		/* 129 */ { "x" : 553, "y" : 80, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "pos" : [700,80 ], "vis" : false },
		/* 130 */ { "x" : 553, "y" : 240, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false },
		/* 131 */ { "x" : -553, "y" : 80, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [-700,80 ], "vis" : false },
		/* 132 */ { "x" : -553, "y" : 240, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "vis" : false },
		/* 133 */ { "x" : -553, "y" : -80, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "pos" : [-700,-80 ], "vis" : false },
		/* 134 */ { "x" : -553, "y" : -240, "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "F8F8F8", "vis" : false }

	],

	"segments" : [
		{ "v0" : 6, "v1" : 7, "curve" : 0, "color" : "F8F8F8", "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "pos" : [-700,-80 ], "y" : -80 },
		{ "v0" : 7, "v1" : 8, "color" : "F8F8F8", "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "x" : -590 },
		{ "v0" : 8, "v1" : 9, "curve" : 0, "color" : "F8F8F8", "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "pos" : [-700,80 ], "y" : 80 },
		{ "v0" : 10, "v1" : 11, "curve" : 0, "color" : "F8F8F8", "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "pos" : [700,-80 ], "y" : -80 },
		{ "v0" : 11, "v1" : 12, "color" : "F8F8F8", "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "x" : 590 },
		{ "v0" : 12, "v1" : 13, "curve" : 0, "color" : "F8F8F8", "cMask" : ["red","blue","ball" ], "trait" : "goalNet", "pos" : [700,80 ], "y" : 80 },
		
		{ "v0" : 2, "v1" : 3, "trait" : "kickOffBarrier" },
		{ "v0" : 3, "v1" : 4, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.15, "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier" },
		{ "v0" : 3, "v1" : 4, "curve" : -180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.15, "cGroup" : ["redKO" ], "trait" : "kickOffBarrier" },
		{ "v0" : 4, "v1" : 5, "trait" : "kickOffBarrier" },
		
		{ "v0" : 14, "v1" : 15, "vis" : true, "color" : "F8F8F8", "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -550 },
		{ "v0" : 16, "v1" : 17, "vis" : true, "color" : "F8F8F8", "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -550 },
		{ "v0" : 18, "v1" : 19, "vis" : true, "color" : "F8F8F8", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "y" : 240 },
		{ "v0" : 20, "v1" : 21, "vis" : true, "color" : "F8F8F8", "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 550 },
		{ "v0" : 22, "v1" : 23, "vis" : true, "color" : "F8F8F8", "bCoef" : 1.15, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 550 },
		{ "v0" : 24, "v1" : 25, "vis" : true, "color" : "F8F8F8", "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 550, "y" : -240 },
		{ "v0" : 26, "v1" : 27, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "y" : -240 },
		
		{ "v0" : 28, "v1" : 29, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier" },
		{ "v0" : 30, "v1" : 31, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier" },
		
		{ "v0" : 38, "v1" : 39, "curve" : 0, "vis" : false, "color" : "F8F8F8", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -557.5 },
		{ "v0" : 40, "v1" : 41, "curve" : 0, "vis" : false, "color" : "F8F8F8", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -557.5 },
		{ "v0" : 42, "v1" : 43, "curve" : 0, "vis" : false, "color" : "F8F8F8", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 557.5 },
		{ "v0" : 44, "v1" : 45, "curve" : 0, "vis" : false, "color" : "F8F8F8", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 557.5 },
		
		{ "v0" : 46, "v1" : 47, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 0 },
		{ "v0" : 48, "v1" : 49, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -550 },
		{ "v0" : 50, "v1" : 51, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 550 },
		{ "v0" : 52, "v1" : 53, "curve" : -90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 55, "v1" : 54, "curve" : -90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 56, "v1" : 57, "curve" : 90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 53, "v1" : 57, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 59, "v1" : 58, "curve" : 90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 62, "v1" : 61, "curve" : -90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 64, "v1" : 63, "curve" : 90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 65, "v1" : 66, "curve" : 90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 67, "v1" : 68, "curve" : -90, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line" },
		{ "v0" : 69, "v1" : 70, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 390 },
		{ "v0" : 72, "v1" : 71, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 71, "v1" : 72, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 74, "v1" : 73, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 73, "v1" : 74, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 76, "v1" : 75, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 75, "v1" : 76, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 78, "v1" : 77, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 77, "v1" : 78, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -375 },
		{ "v0" : 80, "v1" : 79, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 79, "v1" : 80, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 82, "v1" : 81, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 81, "v1" : 82, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 84, "v1" : 83, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 83, "v1" : 84, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 86, "v1" : 85, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 85, "v1" : 86, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 375 },
		{ "v0" : 88, "v1" : 87, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 87, "v1" : 88, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 90, "v1" : 89, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 89, "v1" : 90, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 92, "v1" : 91, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 91, "v1" : 92, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 94, "v1" : 93, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 93, "v1" : 94, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -277.5 },
		{ "v0" : 96, "v1" : 95, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 95, "v1" : 96, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 98, "v1" : 97, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 97, "v1" : 98, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 100, "v1" : 99, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 99, "v1" : 100, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 102, "v1" : 101, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 101, "v1" : 102, "curve" : 180, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 277.5 },
		{ "v0" : 103, "v1" : 104, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -240 },
		{ "v0" : 105, "v1" : 106, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -120 },
		{ "v0" : 107, "v1" : 108, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 240 },
		{ "v0" : 109, "v1" : 110, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 120 },
		{ "v0" : 111, "v1" : 112, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -381 },
		{ "v0" : 113, "v1" : 114, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -240, "y" : 123 },
		{ "v0" : 115, "v1" : 116, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -240, "y" : 123 },
		{ "v0" : 117, "v1" : 118, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -240, "y" : -123 },
		{ "v0" : 119, "v1" : 120, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -240, "y" : -123 },
		{ "v0" : 121, "v1" : 122, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : -381 },
		{ "v0" : 123, "v1" : 124, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 381 },
		{ "v0" : 125, "v1" : 126, "curve" : 0, "vis" : true, "color" : "F8F8F8", "bCoef" : 0.1, "trait" : "line", "x" : 381 },
		
		{ "v0" : 127, "v1" : 128, "vis" : false, "color" : "F8F8F8", "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 553 },
		{ "v0" : 129, "v1" : 130, "vis" : false, "color" : "F8F8F8", "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "x" : 553 },
		{ "v0" : 131, "v1" : 132, "vis" : false, "color" : "F8F8F8", "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -553 },
		{ "v0" : 133, "v1" : 134, "vis" : false, "color" : "F8F8F8", "bCoef" : 0, "cMask" : ["ball" ], "trait" : "ballArea", "x" : -553 }

	],

	"goals" : [
		{ "p0" : [-556.25,-80 ], "p1" : [-556.25,80 ], "team" : "red" },
		{ "p0" : [556.25,80 ], "p1" : [556.25,-80 ], "team" : "blue" }

	],

	"discs" : [
		{ "radius" : 5, "pos" : [-550,80 ], "color" : "6666CC", "trait" : "goalPost", "y" : 80 },
		{ "radius" : 5, "pos" : [-550,-80 ], "color" : "6666CC", "trait" : "goalPost", "y" : -80, "x" : -560 },
		{ "radius" : 5, "pos" : [550,80 ], "color" : "6666CC", "trait" : "goalPost", "y" : 80 },
		{ "radius" : 5, "pos" : [550,-80 ], "color" : "6666CC", "trait" : "goalPost", "y" : -80 },
		
		{ "radius" : 3, "invMass" : 0, "pos" : [-550,240 ], "color" : "FFCC00", "bCoef" : 0.1, "trait" : "line" },
		{ "radius" : 3, "invMass" : 0, "pos" : [-550,-240 ], "color" : "FFCC00", "bCoef" : 0.1, "trait" : "line" },
		{ "radius" : 3, "invMass" : 0, "pos" : [550,-240 ], "color" : "FFCC00", "bCoef" : 0.1, "trait" : "line" },
		{ "radius" : 3, "invMass" : 0, "pos" : [550,240 ], "color" : "FFCC00", "bCoef" : 0.1, "trait" : "line" }

	],

	"planes" : [
		{ "normal" : [0,1 ], "dist" : -240, "bCoef" : 1, "trait" : "ballArea", "vis" : false, "curve" : 0 },
		{ "normal" : [0,-1 ], "dist" : -240, "bCoef" : 1, "trait" : "ballArea" },
		
		{ "normal" : [0,1 ], "dist" : -270, "bCoef" : 0.1 },
		{ "normal" : [0,-1 ], "dist" : -270, "bCoef" : 0.1 },
		{ "normal" : [1,0 ], "dist" : -620, "bCoef" : 0.1 },
		{ "normal" : [-1,0 ], "dist" : -620, "bCoef" : 0.1 },
		
		{ "normal" : [1,0 ], "dist" : -620, "bCoef" : 0.1, "trait" : "ballArea", "vis" : false, "curve" : 0 },
		{ "normal" : [-1,0 ], "dist" : -620, "bCoef" : 0.1, "trait" : "ballArea", "vis" : false, "curve" : 0 }

	],

	"traits" : {
		"ballArea" : { "vis" : false, "bCoef" : 1, "cMask" : ["ball" ] },
		"goalPost" : { "radius" : 8, "invMass" : 0, "bCoef" : 0.5 },
		"goalNet" : { "vis" : true, "bCoef" : 0.1, "cMask" : ["ball" ] },
		"line" : { "vis" : true, "bCoef" : 0.1, "cMask" : ["" ] },
		"kickOffBarrier" : { "vis" : false, "bCoef" : 0.1, "cGroup" : ["redKO","blueKO" ], "cMask" : ["red","blue" ] }

	},

	"playerPhysics" : {
		"bCoef" : 0,
		"acceleration" : 0.11,
		"kickingAcceleration" : 0.083,
		"kickStrength" : 5

	},

	"ballPhysics" : {
		"radius" : 6.25,
		"bCoef" : 0.4,
		"invMass" : 1.5,
		"damping" : 0.99,
		"color" : "FFCC00"

	}
}`;
var Handball=`
{

	"name" : "🤾 𝙷𝙰𝙽𝙳𝙱𝙰𝙻𝙻 𝚋𝚢 𝐆𝐋𝐇",

	"width" : 790,

	"height" : 350,

	"spawnDistance" : 350,

	"redSpawnPoints" : [
		[ -102, -50
		],
		[ -102, 50
		],
		[ -268, 0
		],
		[ -650, 0
		]

	],

	"blueSpawnPoints" : [
		[ 102, -50
		],
		[ 102, 50
		],
		[ 268, 0
		],
		[ 650, 0
		]

	],

	"bg" : { "type" : "none", "width" : 653, "height" : 320, "kickOffRadius" : 0, "cornerRadius" : 0, "color" : "253D97" },

	"vertexes" : [
		/* 0 */ { "x" : -653, "y" : -89.24707947723184, "cMask" : ["blue" ], "cGroup" : ["blue" ], "trait" : "ballArea", "color" : "e56d56", "vis" : false },
		
		/* 1 */ { "x" : 0, "y" : 320, "trait" : "kickOffBarrier", "color" : "E9CC6D", "vis" : true },
		/* 2 */ { "x" : 0, "y" : 80, "cMask" : ["red" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "color" : "F26949", "vis" : true },
		/* 3 */ { "x" : 0, "y" : -80, "cMask" : ["red" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "color" : "F26949", "vis" : true },
		
		/* 4 */ { "x" : -653, "y" : -220, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blue" ], "curve" : 85, "color" : "E9CC6D", "vis" : false },
		/* 5 */ { "x" : -653, "y" : 220, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : -85, "color" : "E9CC6D", "vis" : false },
		/* 6 */ { "x" : 653, "y" : -220, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "curve" : -85, "color" : "E9CC6D" },
		/* 7 */ { "x" : 553, "y" : 320, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 61, "color" : "EF7E29" },
		/* 8 */ { "x" : -458, "y" : -15, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "color" : "ffffff" },
		/* 9 */ { "x" : -458, "y" : 15, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "color" : "ffffff" },
		/* 10 */ { "x" : 458, "y" : -15, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "ffffff" },
		/* 11 */ { "x" : 458, "y" : 15, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "ffffff" },
		/* 12 */ { "x" : -800, "y" : -120, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 13 */ { "x" : -700, "y" : -120, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 14 */ { "x" : -700, "y" : 120, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 15 */ { "x" : -800, "y" : 120, "bCoef" : 0, "cMask" : ["blue" ] },
		
		/* 16 */ { "x" : -798, "y" : -120, "trait" : "kickOffBarrier" },
		/* 17 */ { "x" : -700, "y" : -120, "trait" : "kickOffBarrier" },
		/* 18 */ { "x" : -700, "y" : 120, "trait" : "kickOffBarrier" },
		/* 19 */ { "x" : -800, "y" : 120, "trait" : "kickOffBarrier" },
		
		/* 20 */ { "x" : -740, "y" : -80, "bCoef" : 0, "cMask" : ["blue" ], "color" : "6666FF" },
		/* 21 */ { "x" : -740, "y" : 80, "bCoef" : 0, "cMask" : ["blue" ], "color" : "6666FF" },
		/* 22 */ { "x" : -745, "y" : -80, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 23 */ { "x" : -735, "y" : -80, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 24 */ { "x" : -745, "y" : 80, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 25 */ { "x" : -735, "y" : 80, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 26 */ { "x" : -790, "y" : -80, "bCoef" : 0, "cMask" : ["red" ] },
		/* 27 */ { "x" : -790, "y" : 80, "bCoef" : 0, "cMask" : ["red" ] },
		/* 28 */ { "x" : 800, "y" : -120, "bCoef" : 0, "cMask" : ["red" ] },
		/* 29 */ { "x" : 700, "y" : -120, "bCoef" : 0, "cMask" : ["red" ], "curve" : 0 },
		/* 30 */ { "x" : 700, "y" : 120, "bCoef" : 0, "cMask" : ["red" ], "curve" : 0 },
		/* 31 */ { "x" : 800, "y" : 120, "bCoef" : 0, "cMask" : ["red" ] },
		
		/* 32 */ { "x" : 801, "y" : -120, "trait" : "kickOffBarrier" },
		/* 33 */ { "x" : 700, "y" : -120, "trait" : "kickOffBarrier" },
		/* 34 */ { "x" : 700, "y" : 120, "trait" : "kickOffBarrier" },
		/* 35 */ { "x" : 801, "y" : 120, "trait" : "kickOffBarrier" },
		
		/* 36 */ { "x" : 740, "y" : -80, "bCoef" : 0, "cMask" : ["red" ], "color" : "FF6666" },
		/* 37 */ { "x" : 740, "y" : 80, "bCoef" : 0, "cMask" : ["red" ], "color" : "FF6666" },
		/* 38 */ { "x" : 745, "y" : -80, "bCoef" : 0, "cMask" : ["red" ] },
		/* 39 */ { "x" : 735, "y" : -80, "bCoef" : 0, "cMask" : ["red" ] },
		/* 40 */ { "x" : 745, "y" : 80, "bCoef" : 0, "cMask" : ["red" ] },
		/* 41 */ { "x" : 735, "y" : 80, "bCoef" : 0, "cMask" : ["red" ] },
		/* 42 */ { "x" : 790, "y" : -80, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 43 */ { "x" : 790, "y" : 80, "bCoef" : 0, "cMask" : ["blue" ] },
		
		/* 44 */ { "x" : 0, "y" : 320, "trait" : "kickOffBarrier", "color" : "E9CC6D", "vis" : true },
		/* 45 */ { "x" : 0, "y" : -80, "cMask" : ["red","blue" ], "cGroup" : ["redKO","blueKO" ], "trait" : "kickOffBarrier", "color" : "585757", "vis" : true, "curve" : 0 },
		/* 46 */ { "x" : 0, "y" : -354, "trait" : "kickOffBarrier", "color" : "585757", "vis" : true, "curve" : 0 },
		/* 47 */ { "x" : 0, "y" : 320, "trait" : "kickOffBarrier", "color" : "E9CC6D", "vis" : true, "curve" : 0 },
		/* 48 */ { "x" : 0, "y" : 80, "cMask" : ["red" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "color" : "EF7E29", "vis" : true, "curve" : 0 },
		/* 49 */ { "x" : 0, "y" : 354, "cMask" : ["red" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "color" : "585757", "vis" : true, "curve" : 0 },
		/* 50 */ { "x" : 0, "y" : 80, "trait" : "kickOffBarrier", "color" : "585757", "vis" : true, "curve" : 0 },
		
		/* 51 */ { "x" : 653, "y" : 94, "cMask" : ["red" ], "cGroup" : ["red" ], "trait" : "ballArea", "vis" : false, "color" : "E9CC6D" },
		/* 52 */ { "x" : 653, "y" : -94, "cMask" : ["red" ], "cGroup" : ["red" ], "trait" : "ballArea", "curve" : 0, "vis" : false, "color" : "E9CC6D" },
		
		/* 53 */ { "x" : 653, "y" : -220, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : -85, "color" : "88A9D9", "vis" : false },
		
		/* 54 */ { "x" : -653, "y" : 320, "trait" : "ballArea", "vis" : true, "color" : "ffffff", "curve" : 0 },
		/* 55 */ { "x" : -653, "y" : 94, "trait" : "ballArea", "vis" : false, "color" : "ffffff" },
		/* 56 */ { "x" : -653, "y" : -89.24707947723184, "cMask" : ["ball" ], "cGroup" : ["blue" ], "trait" : "ballArea", "color" : "ffffff", "vis" : false },
		/* 57 */ { "x" : -653, "y" : -320, "cMask" : ["ball" ], "trait" : "ballArea", "color" : "ffffff", "vis" : true },
		
		/* 58 */ { "x" : -653, "y" : 220, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : -85, "color" : "E9CC6D", "vis" : false },
		
		/* 59 */ { "x" : 653, "y" : 320, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : true, "color" : "FFFFFF", "curve" : 0 },
		/* 60 */ { "x" : 653, "y" : 91.33920484545074, "cMask" : ["ball" ], "cGroup" : ["red" ], "trait" : "ballArea", "vis" : false, "color" : "FFFFFF", "curve" : 0 },
		/* 61 */ { "x" : 653, "y" : -94, "cMask" : ["ball" ], "cGroup" : ["red" ], "trait" : "ballArea", "curve" : 0, "vis" : false, "color" : "FFFFFF" },
		/* 62 */ { "x" : 653, "y" : -320, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "vis" : true, "color" : "FFFFFF" },
		
		/* 63 */ { "x" : 653, "y" : 220, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "curve" : 0, "color" : "E9CC6D", "vis" : false },
		/* 64 */ { "x" : 653, "y" : -220, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : 0, "color" : "88A9D9", "vis" : false },
		
		/* 65 */ { "x" : 653, "y" : -94, "cMask" : ["ball" ], "cGroup" : ["red" ], "trait" : "ballArea", "curve" : 0, "vis" : false, "color" : "FFFFFF" },
		/* 66 */ { "x" : 653, "y" : -320, "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "vis" : true, "color" : "FFFFFF" },
		/* 67 */ { "x" : 653, "y" : 320, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : true, "color" : "FFFFFF", "curve" : 0 },
		/* 68 */ { "x" : 653, "y" : 94, "cMask" : ["ball" ], "cGroup" : ["red" ], "trait" : "ballArea", "vis" : false, "color" : "FFFFFF", "curve" : 0 },
		/* 69 */ { "x" : -653, "y" : 94.08069095559071, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false },
		/* 70 */ { "x" : -653, "y" : 320, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false },
		/* 71 */ { "x" : -653, "y" : -320, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false },
		/* 72 */ { "x" : -653, "y" : -89.24707947723184, "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "vis" : false },
		
		/* 73 */ { "x" : 651, "y" : 220, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : 85, "color" : "2CAAFF" },
		/* 74 */ { "x" : 486, "y" : 110, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : 8, "color" : "2CAAFF" },
		/* 75 */ { "x" : 651, "y" : -220, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : -85, "color" : "2CAAFF" },
		/* 76 */ { "x" : 486, "y" : -110, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : 8, "color" : "2CAAFF" },
		/* 77 */ { "x" : -651, "y" : -220, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : 85, "color" : "2CAAFF" },
		/* 78 */ { "x" : -483, "y" : -101, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : 8, "color" : "2CAAFF" },
		/* 79 */ { "x" : -651, "y" : 220, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : -85, "color" : "2CAAFF" },
		/* 80 */ { "x" : -483, "y" : 99, "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ], "curve" : 8, "color" : "2CAAFF" },
		/* 81 */ { "x" : 521.901256418312, "y" : 305.9572422383344, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 82 */ { "x" : -553, "y" : 320, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : -61, "color" : "EF7E29" },
		/* 83 */ { "x" : -553, "y" : -320, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 61, "color" : "EF7E29" },
		/* 84 */ { "x" : -522.0946317738246, "y" : -306.85287598443875, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 85 */ { "x" : -506.1420251852333, "y" : -296.7757654754572, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 86 */ { "x" : -469.7255367603498, "y" : -269.1764681158355, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 8.088971148362203, "color" : "EF7E29" },
		/* 87 */ { "x" : -432.82271686760123, "y" : -234.09941957482695, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 8.088971148362203, "color" : "EF7E29" },
		/* 88 */ { "x" : -376.9078647720215, "y" : -57.98404915925913, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 89 */ { "x" : -376.04228885079664, "y" : -39.98421647278644, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 90 */ { "x" : -418.91986908926475, "y" : -213.0447750469475, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 91 */ { "x" : -388.05932760879983, "y" : -143.0001405310138, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 92 */ { "x" : -506.1420251852333, "y" : 296.7757654754572, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 13.235175487479236, "color" : "EF7E29" },
		/* 93 */ { "x" : -522.0946317738246, "y" : 306.85287598443875, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 13.235175487479236, "color" : "EF7E29" },
		/* 94 */ { "x" : -469.7255367603498, "y" : 269.1764681158355, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 95 */ { "x" : -486.1562730031999, "y" : 282.1992379255447, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 96 */ { "x" : -450.5, "y" : 252.49609375, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 97 */ { "x" : -380.6676342406169, "y" : -111.48765640168591, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 98 */ { "x" : -377.7933553715835, "y" : -89.98390663292105, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 99 */ { "x" : -486.1562730031999, "y" : -282.1992379255447, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "color" : "EF7E29" },
		/* 100 */ { "x" : -376.04228885079664, "y" : -9.492522744034375, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "color" : "EF7E29" },
		/* 101 */ { "x" : -450.5, "y" : -252.49609375, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "color" : "EF7E29" },
		/* 102 */ { "x" : -408.5, "y" : -194.49609375, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "color" : "EF7E29" },
		/* 103 */ { "x" : -396.5, "y" : -168.49609375, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "color" : "EF7E29" },
		/* 104 */ { "x" : -434.82271686760123, "y" : 236.09941957482695, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 105 */ { "x" : -418.91986908926475, "y" : 213.0447750469475, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 106 */ { "x" : -408.5, "y" : 194.49609375, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 107 */ { "x" : -396.5, "y" : 168.49609375, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 108 */ { "x" : -388.05932760879983, "y" : 145.0001405310138, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 109 */ { "x" : -381.6676342406169, "y" : 117.48765640168591, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 110 */ { "x" : -378.7933553715835, "y" : 94.98390663292105, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 111 */ { "x" : -376.9078647720215, "y" : 66.98404915925913, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 112 */ { "x" : -376.04228885079664, "y" : 15.015783527213557, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 113 */ { "x" : -376.04228885079664, "y" : 44.507477255965625, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "color" : "EF7E29" },
		/* 114 */ { "x" : 553, "y" : -320, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : -61, "color" : "EF7E29" },
		/* 115 */ { "x" : 552.0899057985382, "y" : 320.2098043123669, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 61, "color" : "EF7E29" },
		/* 116 */ { "x" : 521.2378162708901, "y" : 306.93813422703, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 117 */ { "x" : 523.713123102581, "y" : -306.762625798387, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 13.235175487479236, "color" : "EF7E29" },
		/* 118 */ { "x" : 505.78555149359147, "y" : 296.43458264259755, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 119 */ { "x" : 469.18816225723685, "y" : 269.07561802353257, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 8.088971148362203, "color" : "EF7E29" },
		/* 120 */ { "x" : 432.0552250397206, "y" : 234.24226584512587, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 8.088971148362203, "color" : "EF7E29" },
		/* 121 */ { "x" : 374.98219316389105, "y" : 58.49880675209518, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 122 */ { "x" : 373.9981406555976, "y" : 40.50506230916902, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 123 */ { "x" : 418.0140729386622, "y" : 213.2796018870813, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 124 */ { "x" : 386.69308683511514, "y" : 143.43964430949083, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 125 */ { "x" : 501.878121149686, "y" : -297.1040865966373, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 13.235175487479236, "color" : "EF7E29" },
		/* 126 */ { "x" : 465.6441117593936, "y" : -269.26565259885837, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 127 */ { "x" : 481.98876130101564, "y" : -282.396305985508, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 128 */ { "x" : 446.5288007685749, "y" : -252.45907536158984, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 129 */ { "x" : 379.0941026750565, "y" : 111.97650354787007, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 130 */ { "x" : 376.07832398363433, "y" : 90.49214151361383, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 131 */ { "x" : 485.7042731236562, "y" : 281.9899398735921, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "color" : "EF7E29" },
		/* 132 */ { "x" : 373.7974096944257, "y" : 10.014029307165885, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "color" : "EF7E29" },
		/* 133 */ { "x" : 449.8532329264895, "y" : 252.5221694256424, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "color" : "EF7E29" },
		/* 134 */ { "x" : 407.4723211500617, "y" : 194.79991793630217, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "color" : "EF7E29" },
		/* 135 */ { "x" : 395.30141964764476, "y" : 168.87947896203968, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "color" : "EF7E29" },
		/* 136 */ { "x" : 430.959798881452, "y" : -235.9595508030171, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 137 */ { "x" : 415.2090675592799, "y" : -212.80071524108587, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 138 */ { "x" : 404.91153274716675, "y" : -194.18384046344227, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 139 */ { "x" : 393.08295430734483, "y" : -168.10540622952055, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 140 */ { "x" : 384.7971418689347, "y" : -144.55439605331273, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 141 */ { "x" : 378.5867054225696, "y" : -117.0004307084653, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 142 */ { "x" : 375.8606340776635, "y" : -94.47824680692861, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 143 */ { "x" : 374.15951119960124, "y" : -66.46658362353033, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 144 */ { "x" : 373.6360681855451, "y" : -14.493745891795022, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "EF7E29" },
		/* 145 */ { "x" : 373.44192036019246, "y" : -43.984800562871555, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "color" : "EF7E29" },
		/* 146 */ { "x" : 530, "y" : -8, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "ffffff" },
		/* 147 */ { "x" : 530, "y" : 8, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "ffffff" },
		/* 148 */ { "x" : -530, "y" : -8, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "ffffff" },
		/* 149 */ { "x" : -530, "y" : 8, "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "curve" : 0, "color" : "ffffff" },
		
		/* 150 */ { "x" : -653, "y" : 94.08069095559071, "trait" : "ballArea" },
		
		/* 151 */ { "x" : -653, "y" : -89.24707947723184, "trait" : "goalNet", "color" : "FFFFFF" },
		/* 152 */ { "x" : -683, "y" : -89.24707947723184, "trait" : "goalNet", "color" : "FFFFFF", "cMask" : ["blue" ] },
		/* 153 */ { "x" : -683, "y" : 94.08069095559071, "trait" : "goalNet", "color" : "FFFFFF", "cMask" : ["blue" ] },
		/* 154 */ { "x" : -653, "y" : 94.08069095559071, "trait" : "goalNet", "color" : "FFFFFF" },
		
		/* 155 */ { "x" : -653, "y" : 94.08069095559071, "trait" : "fieldArea" },
		
		/* 156 */ { "x" : -653, "y" : 91.08069095559071, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line", "color" : "FFFFFF", "vis" : true },
		/* 157 */ { "x" : -653, "y" : -92.24707947723184, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line", "color" : "FFFFFF", "vis" : true },
		/* 158 */ { "x" : -653, "y" : -60.60211534710332, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line", "color" : "FFFFFF" },
		/* 159 */ { "x" : -653, "y" : -51.95715121697479, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line" },
		/* 160 */ { "x" : -653, "y" : -31.332777043282263, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line" },
		/* 161 */ { "x" : -653, "y" : -6, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line" },
		/* 162 */ { "x" : -653, "y" : 16, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line" },
		/* 163 */ { "x" : -653, "y" : 66.58152539066732, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line", "color" : "FFFFFF" },
		
		/* 164 */ { "x" : -667, "y" : -89.24707947723184, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "goalNet", "color" : "FFFFFF" },
		
		/* 165 */ { "x" : -671, "y" : 94.08069095559071, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "color" : "FFFFFF" },
		
		/* 166 */ { "x" : -653, "y" : -84.22648952079584, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line" },
		/* 167 */ { "x" : -653, "y" : -69.60211534710332, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line", "color" : "FFFFFF" },
		/* 168 */ { "x" : -653, "y" : 70, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line", "color" : "FFFFFF" },
		/* 169 */ { "x" : -653, "y" : 94.08069095559071, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line" },
		
		/* 170 */ { "x" : 652.2715278479752, "y" : -91.9828225460283, "trait" : "ballArea" },
		
		/* 171 */ { "x" : 653.722625690124, "y" : 91.33920484545074, "trait" : "goalNet", "color" : "FFFFFF" },
		/* 172 */ { "x" : 683.721685891206, "y" : 91.10174526602265, "trait" : "goalNet", "color" : "FFFFFF", "cMask" : ["red" ] },
		/* 173 */ { "x" : 682.2705880490571, "y" : -92.2202821254564, "trait" : "goalNet", "color" : "FFFFFF", "cMask" : ["red" ] },
		/* 174 */ { "x" : 652.2715278479752, "y" : -91.9828225460283, "trait" : "goalNet", "color" : "FFFFFF" },
		
		/* 175 */ { "x" : 652.2715278479752, "y" : -91.9828225460283, "trait" : "fieldArea" },
		
		/* 176 */ { "x" : 653, "y" : -91.9828225460283, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line", "color" : "FFFFFF", "vis" : true, "curve" : 0 },
		/* 177 */ { "x" : 653, "y" : 91.33920484545074, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line", "color" : "FFFFFF", "vis" : true, "curve" : 0 },
		/* 178 */ { "x" : 653, "y" : 62.69513806553215, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line", "color" : "FFFFFF" },
		/* 179 */ { "x" : 653, "y" : -64.48451843730645, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line", "color" : "FFFFFF" },
		
		/* 180 */ { "x" : 667.7221871172956, "y" : 91.22839037505096, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "goalNet", "color" : "FFFFFF" },
		
		/* 181 */ { "x" : 670.2709639686243, "y" : -92.12529829368515, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "color" : "FFFFFF" },
		/* 182 */ { "x" : -150, "y" : 305, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "color" : "FFFFFF" },
		/* 183 */ { "x" : -150, "y" : 335, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "color" : "FFFFFF" },
		/* 184 */ { "x" : 150, "y" : 305, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "color" : "FFFFFF" },
		/* 185 */ { "x" : 150, "y" : 335, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "color" : "FFFFFF" },
		/* 186 */ { "x" : -150, "y" : -335, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "color" : "FFFFFF" },
		/* 187 */ { "x" : -150, "y" : -305, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "color" : "FFFFFF" },
		/* 188 */ { "x" : 150, "y" : -335, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "color" : "FFFFFF" },
		/* 189 */ { "x" : 150, "y" : -305, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "color" : "FFFFFF" },
		
		/* 190 */ { "x" : -653, "y" : 35, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line" },
		/* 191 */ { "x" : -653, "y" : 50, "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line" },
		/* 192 */ { "x" : 653, "y" : -51.95715121697479, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line" },
		/* 193 */ { "x" : 653, "y" : -31.332777043282263, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line" },
		/* 194 */ { "x" : 653, "y" : -6, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line" },
		/* 195 */ { "x" : 653, "y" : 16, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line" },
		/* 196 */ { "x" : 653, "y" : -91.9828225460283, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line" },
		/* 197 */ { "x" : 653, "y" : -69.60211534710332, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line", "color" : "FFFFFF" },
		/* 198 */ { "x" : 653, "y" : 70, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line", "color" : "FFFFFF" },
		/* 199 */ { "x" : 653, "y" : 94.08069095559071, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line" },
		/* 200 */ { "x" : 653, "y" : 35, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line" },
		/* 201 */ { "x" : 653, "y" : 50, "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line" },
		
		/* 202 */ { "x" : 0, "y" : 80, "cMask" : ["red" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "color" : "F26949", "vis" : true, "curve" : 0 },
		/* 203 */ { "x" : 0, "y" : -80, "cMask" : ["red" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "color" : "F26949", "vis" : true, "curve" : 0 },
		/* 204 */ { "x" : 0, "y" : 354, "trait" : "kickOffBarrier", "color" : "EF7E29", "vis" : true, "curve" : 0 },
		/* 205 */ { "x" : 0, "y" : 80, "cMask" : ["red" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "color" : "EF7E29", "vis" : true, "curve" : 0 },
		/* 206 */ { "x" : 0, "y" : -354, "trait" : "kickOffBarrier", "color" : "EF7E29", "vis" : true, "curve" : 0 },
		/* 207 */ { "x" : 0, "y" : -80, "cMask" : ["red" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "color" : "EF7E29", "vis" : true, "curve" : 0 },
		
		/* 208 */ { "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blue" ], "x" : -800, "y" : -220, "vis" : false, "curve" : 0 },
		/* 209 */ { "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blue" ], "x" : -653, "y" : -220, "vis" : false, "curve" : 0 },
		/* 210 */ { "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blue" ], "x" : -800, "y" : 220, "vis" : false, "curve" : 0 },
		/* 211 */ { "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blue" ], "x" : -653, "y" : 220, "vis" : false, "curve" : 0 },
		/* 212 */ { "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "x" : 652, "y" : -220, "vis" : false, "curve" : 0 },
		/* 213 */ { "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "x" : 799, "y" : -220, "vis" : false, "curve" : 0 },
		/* 214 */ { "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "x" : 653, "y" : 220, "vis" : false, "curve" : 0 },
		/* 215 */ { "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "x" : 799, "y" : 220, "vis" : false, "curve" : 0 },
		
		/* 216 */ { "x" : -653, "y" : 320, "trait" : "ballArea", "vis" : true, "color" : "ffffff", "curve" : 0 },
		/* 217 */ { "x" : 653, "y" : 320, "trait" : "ballArea", "vis" : true, "color" : "ffffff", "curve" : 0 },
		/* 218 */ { "x" : -653, "y" : -320, "trait" : "ballArea", "color" : "ffffff", "vis" : true, "curve" : 0 },
		/* 219 */ { "x" : 653, "y" : -320, "trait" : "ballArea", "curve" : 0, "vis" : true, "color" : "ffffff" }

	],

	"segments" : [
		{ "v0" : 2, "v1" : 3, "curve" : 180, "vis" : true, "color" : "F26949", "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier" },
		{ "v0" : 2, "v1" : 3, "curve" : -180, "vis" : true, "color" : "F26949", "cGroup" : ["redKO" ], "trait" : "kickOffBarrier" },
		
		{ "v0" : 4, "v1" : 0, "curve" : 0, "vis" : false, "color" : "E9CC6D", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blue" ] },
		{ "v0" : 8, "v1" : 9, "curve" : 0, "vis" : true, "color" : "ffffff", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "x" : -458 },
		{ "v0" : 10, "v1" : 11, "curve" : 0, "vis" : true, "color" : "ffffff", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "x" : 462 },
		{ "v0" : 12, "v1" : 13, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ] },
		{ "v0" : 13, "v1" : 14, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ] },
		{ "v0" : 14, "v1" : 15, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ] },
		
		{ "v0" : 16, "v1" : 17, "trait" : "kickOffBarrier" },
		{ "v0" : 18, "v1" : 19, "trait" : "kickOffBarrier" },
		
		{ "v0" : 20, "v1" : 21, "color" : "6666FF", "bCoef" : 1000000, "cMask" : ["blue" ] },
		{ "v0" : 22, "v1" : 23, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ] },
		{ "v0" : 24, "v1" : 25, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ] },
		{ "v0" : 26, "v1" : 27, "vis" : false, "bCoef" : 1000000, "cMask" : ["red" ] },
		{ "v0" : 28, "v1" : 29, "vis" : false, "bCoef" : 0, "cMask" : ["red" ] },
		{ "v0" : 29, "v1" : 30, "vis" : false, "bCoef" : 0, "cMask" : ["red" ], "curve" : 0 },
		{ "v0" : 30, "v1" : 31, "vis" : false, "bCoef" : 0, "cMask" : ["red" ] },
		
		{ "v0" : 32, "v1" : 33, "trait" : "kickOffBarrier" },
		{ "v0" : 34, "v1" : 35, "trait" : "kickOffBarrier" },
		
		{ "v0" : 36, "v1" : 37, "color" : "FF6666", "bCoef" : 1000000, "cMask" : ["red" ] },
		{ "v0" : 38, "v1" : 39, "vis" : false, "bCoef" : 0, "cMask" : ["red" ] },
		{ "v0" : 40, "v1" : 41, "vis" : false, "bCoef" : 0, "cMask" : ["red" ] },
		{ "v0" : 42, "v1" : 43, "vis" : false, "bCoef" : 1000000, "cMask" : ["blue" ] },
		
		{ "v0" : 45, "v1" : 46, "curve" : 0, "vis" : true, "color" : "585757", "trait" : "kickOffBarrier", "x" : 0 },
		{ "v0" : 49, "v1" : 50, "curve" : 0, "vis" : true, "color" : "585757", "trait" : "kickOffBarrier", "x" : 0 },
		
		{ "v0" : 54, "v1" : 55, "vis" : true, "color" : "ffffff", "trait" : "ballArea" },
		{ "v0" : 56, "v1" : 57, "vis" : true, "color" : "ffffff", "cMask" : ["ball" ], "trait" : "ballArea" },
		
		{ "v0" : 58, "v1" : 55, "curve" : 0, "vis" : false, "color" : "E9CC6D", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blue" ] },
		
		{ "v0" : 59, "v1" : 60, "vis" : true, "color" : "FFFFFF", "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0, "x" : 653, "y" : 320 },
		{ "v0" : 61, "v1" : 62, "curve" : 0, "vis" : true, "color" : "FFFFFF", "cMask" : ["ball" ], "trait" : "ballArea" },
		
		{ "v0" : 63, "v1" : 60, "curve" : 0, "vis" : false, "color" : "E9CC6D", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "x" : 653 },
		{ "v0" : 64, "v1" : 61, "curve" : 0, "vis" : false, "color" : "E9CC6D", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ] },
		
		{ "v0" : 65, "v1" : 66, "curve" : 0, "vis" : true, "color" : "FFFFFF", "cMask" : ["ball" ], "trait" : "ballArea" },
		{ "v0" : 67, "v1" : 68, "vis" : true, "color" : "FFFFFF", "cMask" : ["ball" ], "trait" : "ballArea", "curve" : 0 },
		{ "v0" : 69, "v1" : 70, "vis" : false, "color" : "ffffff", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea" },
		{ "v0" : 71, "v1" : 72, "vis" : false, "color" : "ffffff", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea" },
		
		{ "v0" : 73, "v1" : 74, "curve" : 85, "vis" : true, "color" : "2CAAFF", "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ] },
		{ "v0" : 75, "v1" : 76, "curve" : -85, "vis" : true, "color" : "2CAAFF", "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ] },
		{ "v0" : 74, "v1" : 76, "curve" : 8, "vis" : true, "color" : "2CAAFF", "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ] },
		{ "v0" : 77, "v1" : 78, "curve" : 85, "vis" : true, "color" : "2CAAFF", "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ] },
		{ "v0" : 79, "v1" : 80, "curve" : -85, "vis" : true, "color" : "2CAAFF", "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ] },
		{ "v0" : 78, "v1" : 80, "curve" : 8, "vis" : true, "color" : "2CAAFF", "bCoef" : 1, "cMask" : ["blue","red" ], "cGroup" : ["blue","red" ] },
		{ "v0" : 7, "v1" : 81, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 83, "v1" : 84, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 85, "v1" : 99, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 87, "v1" : 90, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 91, "v1" : 97, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 98, "v1" : 88, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 89, "v1" : 100, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 96, "v1" : 94, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 95, "v1" : 92, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 93, "v1" : 82, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 86, "v1" : 101, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 102, "v1" : 103, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 97, "v1" : 97, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 104, "v1" : 105, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 106, "v1" : 107, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 108, "v1" : 109, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 110, "v1" : 111, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 112, "v1" : 113, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		{ "v0" : 117, "v1" : 114, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 118, "v1" : 131, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 120, "v1" : 123, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 124, "v1" : 129, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 130, "v1" : 121, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 122, "v1" : 132, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 128, "v1" : 126, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 127, "v1" : 125, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 119, "v1" : 133, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 134, "v1" : 135, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 129, "v1" : 129, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 136, "v1" : 137, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 138, "v1" : 139, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 140, "v1" : 141, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 142, "v1" : 143, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 144, "v1" : 145, "curve" : 0, "vis" : true, "color" : "EF7E29", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 146, "v1" : 147, "curve" : 0, "vis" : true, "color" : "ffffff", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "x" : 530 },
		{ "v0" : 148, "v1" : 149, "curve" : 0, "vis" : true, "color" : "ffffff", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "x" : -530 },
		
		{ "v0" : 151, "v1" : 152, "color" : "FFFFFF", "trait" : "goalNet" },
		{ "v0" : 152, "v1" : 153, "curve" : 0, "color" : "FFFFFF", "trait" : "goalNet", "cMask" : ["blue" ] },
		{ "v0" : 153, "v1" : 154, "color" : "FFFFFF", "trait" : "goalNet" },
		
		{ "v0" : 157, "v1" : 156, "curve" : 0, "vis" : true, "color" : "FFFFFF", "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line", "x" : -550 },
		{ "v0" : 159, "v1" : 160, "curve" : 0, "vis" : true, "color" : "CF0000", "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line" },
		{ "v0" : 161, "v1" : 162, "curve" : 0, "vis" : true, "color" : "CF0000", "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line" },
		
		{ "v0" : 158, "v1" : 164, "curve" : 0, "vis" : true, "color" : "FFFFFF", "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "goalNet" },
		
		{ "v0" : 163, "v1" : 165, "curve" : 0, "vis" : true, "color" : "FFFFFF", "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ] },
		
		{ "v0" : 166, "v1" : 167, "curve" : 0, "vis" : true, "color" : "CF0000", "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line" },
		{ "v0" : 168, "v1" : 169, "curve" : 0, "vis" : true, "color" : "CF0000", "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line" },
		
		{ "v0" : 171, "v1" : 172, "color" : "FFFFFF", "trait" : "goalNet" },
		{ "v0" : 172, "v1" : 173, "curve" : 0, "color" : "FFFFFF", "trait" : "goalNet", "cMask" : ["red" ] },
		{ "v0" : 173, "v1" : 174, "color" : "FFFFFF", "trait" : "goalNet" },
		
		{ "v0" : 177, "v1" : 176, "curve" : 0, "vis" : true, "color" : "FFFFFF", "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line", "x" : 653 },
		
		{ "v0" : 178, "v1" : 180, "curve" : 0, "vis" : true, "color" : "FFFFFF", "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "goalNet" },
		
		{ "v0" : 179, "v1" : 181, "curve" : 0, "vis" : true, "color" : "FFFFFF", "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ] },
		{ "v0" : 182, "v1" : 183, "curve" : 0, "vis" : true, "color" : "FFFFFF", "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "x" : -150 },
		{ "v0" : 184, "v1" : 185, "curve" : 0, "vis" : true, "color" : "FFFFFF", "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "x" : 150 },
		{ "v0" : 186, "v1" : 187, "curve" : 0, "vis" : true, "color" : "FFFFFF", "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "x" : -150 },
		{ "v0" : 188, "v1" : 189, "curve" : 0, "vis" : true, "color" : "FFFFFF", "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "x" : 150 },
		
		{ "v0" : 190, "v1" : 191, "curve" : 0, "vis" : true, "color" : "CF0000", "bCoef" : 0.1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "trait" : "line" },
		{ "v0" : 192, "v1" : 193, "curve" : 0, "vis" : true, "color" : "CF0000", "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line", "x" : 653 },
		{ "v0" : 194, "v1" : 195, "curve" : 0, "vis" : true, "color" : "CF0000", "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line", "x" : 653 },
		{ "v0" : 196, "v1" : 197, "curve" : 0, "vis" : true, "color" : "CF0000", "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line", "x" : 653 },
		{ "v0" : 198, "v1" : 199, "curve" : 0, "vis" : true, "color" : "CF0000", "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line", "x" : 653 },
		{ "v0" : 200, "v1" : 201, "curve" : 0, "vis" : true, "color" : "CF0000", "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["redKO" ], "trait" : "line", "x" : 653 },
		
		{ "v0" : 203, "v1" : 202, "vis" : true, "color" : "F26949", "bCoef" : 0.1, "cMask" : ["red" ], "cGroup" : ["blueKO" ], "trait" : "kickOffBarrier", "curve" : 0 },
		{ "v0" : 204, "v1" : 205, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "kickOffBarrier" },
		{ "v0" : 206, "v1" : 207, "curve" : 0, "vis" : true, "color" : "EF7E29", "trait" : "kickOffBarrier" },
		
		{ "curve" : 0, "vis" : false, "color" : "2CAAFF", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blue" ], "v0" : 208, "v1" : 209, "y" : -220 },
		{ "curve" : 0, "vis" : false, "color" : "2CAAFF", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blue" ], "v0" : 210, "v1" : 211, "y" : 220 },
		{ "curve" : 0, "vis" : false, "color" : "2CAAFF", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "v0" : 212, "v1" : 213, "y" : -220 },
		{ "curve" : 0, "vis" : false, "color" : "2CAAFF", "bCoef" : 1, "cMask" : ["red" ], "cGroup" : ["red" ], "v0" : 214, "v1" : 215, "y" : 220 },
		
		{ "v0" : 217, "v1" : 216, "curve" : 0, "vis" : true, "color" : "ffffff", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "y" : 290 },
		{ "v0" : 218, "v1" : 219, "vis" : true, "color" : "ffffff", "bCoef" : 1, "cMask" : ["ball" ], "trait" : "ballArea", "y" : -290, "curve" : 0 }

	],

	"goals" : [
		{ "p0" : [-661.6,96 ], "p1" : [-661.6,-94 ], "team" : "red" },
		{ "p0" : [661.6,-93.986883372199 ], "p1" : [661.6,96.011511591401 ], "team" : "blue" }

	],

	"discs" : [
		{ "radius" : 5.352099039641226, "pos" : [-653,94.08069095559071 ], "color" : "FFFFFF", "cMask" : ["ball","blue","red" ], "trait" : "goalPost", "vis" : false },
		{ "radius" : 5.352099039641226, "pos" : [-653,-89.24707947723184 ], "color" : "FFFFFF", "bCoef" : 0.5, "cMask" : ["ball","blue","red" ], "trait" : "goalPost", "vis" : false },
		{ "radius" : 5.352099039641226, "pos" : [653,-91.9828225460283 ], "color" : "FFFFFF", "cMask" : ["ball","blue","red" ], "trait" : "goalPost", "vis" : false },
		{ "radius" : 5.352099039641226, "pos" : [653,91.33920484545074 ], "color" : "FFFFFF", "bCoef" : 0.5, "cMask" : ["ball","blue","red" ], "trait" : "goalPost", "vis" : false },
		{ "radius" : 1.3, "invMass" : 0, "pos" : [-683,-89 ], "color" : "000001", "cMask" : ["ball" ], "damping" : 0, "trait" : "goalPost", "bCoef" : 0 },
		{ "radius" : 1.3, "invMass" : 0, "pos" : [-682,94 ], "color" : "000002", "cMask" : ["ball" ], "damping" : 0, "trait" : "goalPost", "bCoef" : 0 },
		{ "radius" : 1.3, "invMass" : 0, "pos" : [683,-92 ], "color" : "000003", "cMask" : ["ball" ], "damping" : 0, "trait" : "goalPost", "bCoef" : 0 },
		{ "radius" : 1.3, "invMass" : 0, "pos" : [684,91 ], "color" : "000004", "cMask" : ["ball" ], "damping" : 0, "trait" : "goalPost", "bCoef" : 0 },
		
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-690,-77 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-690,-63 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-691,-44 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-691,-30 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-691,-13 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-691,2 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-692,17 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-692,33 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-692,50 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-691,67 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [-690,82 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [691,-82 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [694,-66 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [697,-52 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [696,-35 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [697,-18 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [696,-4 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [696,15 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [696,36 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [696,51 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [695,67 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 },
		{ "radius" : 4, "invMass" : 1.5, "pos" : [693,83 ], "color" : "ffffff", "cMask" : ["ball" ], "damping" : 0.96 }

	],


	"joints" : [
		{ "d0" : 5, "d1" : 9, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 9, "d1" : 10, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 10, "d1" : 11, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 11, "d1" : 12, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 12, "d1" : 13, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 13, "d1" : 14, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 14, "d1" : 15, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 15, "d1" : 16, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 16, "d1" : 17, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 17, "d1" : 18, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 18, "d1" : 19, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 19, "d1" : 6, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 7, "d1" : 20, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 20, "d1" : 21, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 21, "d1" : 22, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 22, "d1" : 23, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 23, "d1" : 24, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 24, "d1" : 25, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 25, "d1" : 26, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 26, "d1" : 27, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 27, "d1" : 28, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 28, "d1" : 29, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 29, "d1" : 30, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" },
		{ "d0" : 30, "d1" : 8, "length" : 0.0000001, "strength" : 0.1, "color" : "EBEBEB" }

	],

	"planes" : [
		{ "normal" : [0,1 ], "dist" : -320, "trait" : "ballArea" },
		{ "normal" : [0,-1 ], "dist" : -320, "trait" : "ballArea" },
		
		{ "normal" : [0,1 ], "dist" : -354, "bCoef" : 0.1 },
		{ "normal" : [0,-1 ], "dist" : -354, "bCoef" : 0.1 },
		{ "normal" : [1,0 ], "dist" : -800, "bCoef" : 0 },
		{ "normal" : [-1,0 ], "dist" : -800, "bCoef" : 0 }

	],

	"traits" : {
		"ballArea" : { "vis" : false, "bCoef" : 1, "cMask" : ["ball" ] },
		"goalPost" : { "radius" : 8, "invMass" : 0, "bCoef" : 0.5 },
		"goalNet" : { "vis" : true, "bCoef" : 0.1, "cMask" : ["ball" ] },
		"kickOffBarrier" : { "vis" : false, "bCoef" : 0.1, "cGroup" : ["redKO","blueKO" ], "cMask" : ["red","blue" ] }

	},

	"ballPhysics" : {
		"radius" : 8.6,
		"color" : "fff100",
		"bCoef" : 0.4

	},

	"playerPhysics" : {
		"radius" : 15,
		"kickStrength" : 6.15,
		"bCoef" : 0.01

	}
}`;
var pensred = `{

	"name" : "ᴘᴇɴᴀʟᴛʏ ʀᴇᴅ ᴛᴇᴀᴍ 🔴 | 𝐆𝐋𝐇",

	"width" : 1500,

	"height" : 734,

	"spawnDistance" : 300,

	"redSpawnPoints" : [
		[ 63, -33
		],
		[ 63, 33
		],
		[ 63, -99
		],
		[ 63, 99
		]

	],

	"blueSpawnPoints" : [
		[ 1376, 0
		],
		[ 1376, -48
		],
		[ 1376, 48
		],
		[ 1376, 96
		]

	],

	"bg" : { "type" : "grass", "width" : 1150, "height" : 600, "kickOffRadius" : 180, "cornerRadius" : 0, "color" : "6a9158" },

	"playerPhysics" : {
		"bCoef" : 0.5,
		"invMass" : 0.5,
		"damping" : 0.96,
		"acceleration" : 0.12,
		"kickingAcceleration" : 0.07,
		"kickingDamping" : 0.96,
		"kickStrength" : 5.65

	},

	"ballPhysics" : {
		"pos" : [ 935, 0
		],
		"radius" : 10

	},

	"vertexes" : [
		/* 0 */ { "x" : 1150, "y" : 337, "trait" : "line", "color" : "b3d4a7" },
		/* 1 */ { "x" : 840, "y" : 337, "trait" : "line", "color" : "b3d4a7" },
		/* 2 */ { "x" : 1150, "y" : -337, "trait" : "line", "color" : "b3d4a7" },
		/* 3 */ { "x" : 840, "y" : -337, "trait" : "line", "color" : "b3d4a7" },
		/* 4 */ { "x" : 1150, "y" : 198, "trait" : "line", "color" : "b3d4a7" },
		/* 5 */ { "x" : 1031, "y" : 198, "trait" : "line", "color" : "b3d4a7" },
		/* 6 */ { "x" : 1150, "y" : -198, "trait" : "line", "color" : "b3d4a7" },
		/* 7 */ { "x" : 1029, "y" : -198, "trait" : "line", "color" : "b3d4a7" },
		/* 8 */ { "x" : 840, "y" : -170, "trait" : "line", "curve" : -110, "color" : "b3d4a7" },
		/* 9 */ { "x" : 840, "y" : 170, "trait" : "line", "curve" : -110, "color" : "b3d4a7" },
		/* 10 */ { "x" : -1150, "y" : -337, "trait" : "line", "color" : "b3d4a7" },
		/* 11 */ { "x" : -840, "y" : -337, "trait" : "line", "color" : "b3d4a7" },
		/* 12 */ { "x" : -1150, "y" : 337, "trait" : "line", "color" : "b3d4a7" },
		/* 13 */ { "x" : -840, "y" : 337, "trait" : "line", "color" : "b3d4a7" },
		/* 14 */ { "x" : -1150, "y" : -198, "trait" : "line", "color" : "b3d4a7" },
		/* 15 */ { "x" : -1030, "y" : -198, "trait" : "line", "color" : "b3d4a7" },
		/* 16 */ { "x" : -1150, "y" : 198, "trait" : "line", "color" : "b3d4a7" },
		/* 17 */ { "x" : -1030, "y" : 198, "trait" : "line", "color" : "b3d4a7" },
		/* 18 */ { "x" : -840, "y" : 170, "trait" : "line", "curve" : -110, "color" : "b3d4a7" },
		/* 19 */ { "x" : -840, "y" : -170, "trait" : "line", "curve" : -110, "color" : "b3d4a7" },
		/* 20 */ { "x" : 935, "y" : 4, "trait" : "line", "color" : "a7cf9b" },
		/* 21 */ { "x" : 935, "y" : -4, "trait" : "line", "color" : "a7cf9b" },
		/* 22 */ { "x" : -935, "y" : 4, "trait" : "line", "color" : "a7cf9b" },
		/* 23 */ { "x" : -935, "y" : -4, "trait" : "line", "color" : "a7cf9b" },
		/* 24 */ { "x" : -1150, "y" : 574, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "b3d4a7" },
		/* 25 */ { "x" : -1125, "y" : 599, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "b3d4a7" },
		/* 26 */ { "x" : -1125, "y" : -600, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "b3d4a7" },
		/* 27 */ { "x" : -1150, "y" : -575, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "b3d4a7" },
		/* 28 */ { "x" : 1124, "y" : 600, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "b3d4a7" },
		/* 29 */ { "x" : 1150, "y" : 574, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "b3d4a7" },
		/* 30 */ { "x" : 1150, "y" : -574, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "b3d4a7" },
		/* 31 */ { "x" : 1124, "y" : -600, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "curve" : 0, "color" : "b3d4a7" },
		/* 32 */ { "x" : 0, "y" : -4, "trait" : "line", "color" : "b3d4a7" },
		/* 33 */ { "x" : 0, "y" : 4, "trait" : "line", "color" : "b3d4a7" },
		/* 34 */ { "x" : 0, "y" : -4, "trait" : "line", "color" : "b3d4a7" },
		/* 35 */ { "x" : 0, "y" : 4, "trait" : "line", "color" : "b3d4a7" },
		/* 36 */ { "x" : -1170, "y" : 150, "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "curve" : 40, "color" : "546f48" },
		/* 37 */ { "x" : -1170, "y" : 250, "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "curve" : 40, "color" : "546f48" },
		/* 38 */ { "x" : 1170, "y" : 150, "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "curve" : -40, "color" : "546f48" },
		/* 39 */ { "x" : 1170, "y" : 250, "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "curve" : -40, "color" : "546f48" },
		/* 40 */ { "x" : -1170, "y" : -150, "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "curve" : -40, "color" : "546f48" },
		/* 41 */ { "x" : -1170, "y" : -250, "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "curve" : -40, "color" : "546f48" },
		/* 42 */ { "x" : 1170, "y" : -150, "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "curve" : 40, "color" : "546f48" },
		/* 43 */ { "x" : 1170, "y" : -250, "bCoef" : -4.5, "cMask" : ["ball" ], "trait" : "line", "curve" : 40, "color" : "546f48" },
		/* 44 */ { "x" : 1161, "y" : -599, "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line", "curve" : -60, "color" : "546f48" },
		/* 45 */ { "x" : 1189, "y" : -579, "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line", "curve" : -60, "color" : "546f48" },
		/* 46 */ { "x" : 1161, "y" : 599, "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line", "curve" : 60, "color" : "546f48" },
		/* 47 */ { "x" : 1189, "y" : 579, "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line", "curve" : 60, "color" : "546f48" },
		/* 48 */ { "x" : -1162, "y" : 599, "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line", "curve" : -60, "color" : "546f48" },
		/* 49 */ { "x" : -1190, "y" : 579, "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line", "curve" : -60, "color" : "546f48" },
		/* 50 */ { "x" : -1162, "y" : -600, "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line", "curve" : 60, "color" : "546f48" },
		/* 51 */ { "x" : -1190, "y" : -580, "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line", "curve" : 60, "color" : "546f48" },
		
		/* 52 */ { "x" : -1177, "y" : -250, "bCoef" : 0, "cMask" : ["ball" ] },
		/* 53 */ { "x" : -1177, "y" : -150, "cMask" : ["ball" ] },
		
		/* 54 */ { "x" : -1170, "y" : 250, "bCoef" : -5, "cMask" : ["ball" ], "trait" : "line", "curve" : -40, "color" : "546f48" },
		
		/* 55 */ { "x" : -1177, "y" : 250, "bCoef" : 0, "cMask" : ["ball" ] },
		
		/* 56 */ { "x" : -1170, "y" : 150, "bCoef" : -5, "cMask" : ["ball" ], "trait" : "line", "curve" : -40, "color" : "546f48" },
		
		/* 57 */ { "x" : -1177, "y" : 150, "cMask" : ["ball" ] },
		/* 58 */ { "x" : 1177, "y" : -250, "bCoef" : 0, "cMask" : ["ball" ] },
		/* 59 */ { "x" : 1177, "y" : -150, "cMask" : ["ball" ] },
		
		/* 60 */ { "x" : 1170, "y" : -150, "bCoef" : -5, "cMask" : ["ball" ], "trait" : "line", "curve" : -40, "color" : "546f48" },
		/* 61 */ { "x" : 1170, "y" : -250, "bCoef" : -5, "cMask" : ["ball" ], "trait" : "line", "curve" : -40, "color" : "546f48" },
		
		/* 62 */ { "x" : 1177, "y" : 250, "bCoef" : 0, "cMask" : ["ball" ] },
		/* 63 */ { "x" : 1177, "y" : 150, "cMask" : ["ball" ] },
		
		/* 64 */ { "x" : 1170, "y" : 250, "bCoef" : -5, "cMask" : ["ball" ], "trait" : "line", "curve" : -40, "color" : "546f48" },
		/* 65 */ { "x" : 1170, "y" : 150, "bCoef" : -5, "cMask" : ["ball" ], "trait" : "line", "curve" : -40, "color" : "546f48" },
		/* 66 */ { "x" : 0, "y" : 180, "cMask" : ["ball" ], "cGroup" : ["ball" ], "trait" : "line", "color" : "b3d4a7", "vis" : true, "curve" : 0 },
		/* 67 */ { "x" : 0, "y" : -180, "cMask" : ["ball" ], "cGroup" : ["ball" ], "trait" : "line", "color" : "b3d4a7", "vis" : true, "curve" : 0 },
		/* 68 */ { "x" : -818, "y" : -600, "trait" : "line", "curve" : 90, "color" : "638750" },
		/* 69 */ { "x" : -1150, "y" : -347, "trait" : "line", "curve" : 90, "color" : "638750" },
		/* 70 */ { "x" : -1150, "y" : 347, "trait" : "line", "color" : "638750" },
		/* 71 */ { "x" : -820, "y" : 600, "trait" : "line", "color" : "638750" },
		/* 72 */ { "x" : 820, "y" : 600, "trait" : "line", "color" : "638750" },
		/* 73 */ { "x" : 1150, "y" : 347, "trait" : "line", "color" : "638750" },
		/* 74 */ { "x" : 820, "y" : -600, "trait" : "line", "curve" : -90, "color" : "638750" },
		/* 75 */ { "x" : 1150, "y" : -347, "trait" : "line", "curve" : -90, "color" : "638750" },
		/* 76 */ { "x" : 1150, "y" : -525, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "curve" : 0, "color" : "638750" },
		/* 77 */ { "x" : -1150, "y" : -525, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "curve" : 0, "color" : "638750" },
		/* 78 */ { "x" : 1150, "y" : 525, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "curve" : 0, "color" : "638750" },
		/* 79 */ { "x" : -1150, "y" : 525, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "curve" : 0, "color" : "638750" },
		/* 80 */ { "x" : -1150, "y" : -600, "trait" : "line", "color" : "b3d4a7" },
		/* 81 */ { "x" : -1150, "y" : 600, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "FFFF00" },
		/* 82 */ { "x" : 1150, "y" : 600, "trait" : "line", "color" : "b3d4a7" },
		/* 83 */ { "x" : 1150, "y" : -600, "trait" : "line", "color" : "b3d4a7" },
		
		/* 84 */ { "x" : -113, "y" : -138, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["blueKO","redKO" ], "curve" : 235 },
		/* 85 */ { "x" : -115, "y" : 135, "bCoef" : 0, "cMask" : ["blue" ], "cGroup" : ["blueKO","redKO" ], "curve" : 235 },
		/* 86 */ { "x" : 1495, "y" : -150, "bCoef" : 0, "cMask" : ["blue" ], "dist" : -1400 },
		/* 87 */ { "x" : 1300, "y" : -150, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 88 */ { "x" : 1300, "y" : 150, "bCoef" : 0, "cMask" : ["blue" ], "curve" : 0 },
		/* 89 */ { "x" : 1489, "y" : 150, "bCoef" : 0, "cMask" : ["blue" ], "dist" : -1400, "curve" : 0 },
		
		/* 90 */ { "x" : 1300, "y" : -150, "trait" : "kickOffBarrier", "cMask" : ["blue" ] },
		
		/* 91 */ { "x" : 1448, "y" : -120, "bCoef" : 0, "cMask" : ["blue" ] },
		/* 92 */ { "x" : 1448, "y" : 120, "bCoef" : 0, "cMask" : ["blue" ] },
		
		/* 93 */ { "x" : 1150, "y" : -120.92552225676228, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "b3d4a7", "curve" : 0 },
		/* 94 */ { "x" : 1212.8375029631984, "y" : -120.92552225676228, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "ffffff", "curve" : 0 },
		/* 95 */ { "x" : 1150.1431278225696, "y" : 116.05779951814779, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "ffffff", "curve" : 0 },
		/* 96 */ { "x" : 1212.9145962189946, "y" : 116.05779951814779, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "ffffff", "curve" : 0 },
		
		/* 97 */ { "x" : 1150, "y" : 116.05779951814779, "bCoef" : 0, "cMask" : ["wall" ], "curve" : 0, "color" : "b3d4a7" },
		/* 98 */ { "x" : 1259, "y" : -148.867722739, "bCoef" : 0, "cMask" : ["wall" ], "color" : "ffffff" },
		/* 99 */ { "x" : 1259.5, "y" : 144, "bCoef" : 0, "cMask" : ["wall" ], "color" : "ffffff" },
		
		/* 100 */ { "x" : 1213.8375029631984, "y" : -118.92552225676228, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "6a9158", "curve" : 0 },
		
		/* 101 */ { "x" : 1260, "y" : -146.867722739, "bCoef" : 0, "cMask" : ["wall" ], "color" : "6a9158" },
		
		/* 102 */ { "x" : 1211.8375029631984, "y" : -122.92552225676228, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "6a9158", "curve" : 0 },
		
		/* 103 */ { "x" : 1258, "y" : -150.867722739, "bCoef" : 0, "cMask" : ["wall" ], "color" : "6a9158" },
		
		/* 104 */ { "x" : 1214.9145962189946, "y" : 114.05779951814779, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "6a9158", "curve" : 0 },
		
		/* 105 */ { "x" : 1261.5, "y" : 142, "bCoef" : 0, "cMask" : ["wall" ], "color" : "6a9158" },
		
		/* 106 */ { "x" : 1213.9145962189946, "y" : 119.05779951814779, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "6a9158", "curve" : 0 },
		
		/* 107 */ { "x" : 1260.5, "y" : 147, "bCoef" : 0, "cMask" : ["wall" ], "color" : "6a9158" },
		
		/* 108 */ { "x" : 1150, "y" : -120, "bCoef" : 0.5, "cMask" : ["blue","ball" ], "trait" : "line", "color" : "C7E6BD", "curve" : 0 },
		/* 109 */ { "x" : 1213, "y" : -120, "bCoef" : 0, "cMask" : ["blue","ball" ], "trait" : "line", "color" : "ffffff", "curve" : 0 },
		/* 110 */ { "x" : 1150, "y" : 116, "bCoef" : 0.5, "cMask" : ["blue","ball" ], "trait" : "line", "color" : "ffffff", "curve" : 0 },
		/* 111 */ { "x" : 1213, "y" : 116, "bCoef" : 0, "cMask" : ["blue","ball" ], "trait" : "line", "color" : "ffffff", "curve" : 0 },
		/* 112 */ { "x" : -1150, "y" : 118.00879788978456, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "b3d4a7", "curve" : 0 },
		/* 113 */ { "x" : -1213.3215131279903, "y" : 117.74394897515494, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "ffffff", "curve" : 0 },
		/* 114 */ { "x" : -1149.628852252629, "y" : -118.97302216202547, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "ffffff", "curve" : 0 },
		/* 115 */ { "x" : -1212.3997630875529, "y" : -119.23759275268432, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "ffffff", "curve" : 0 },
		
		/* 116 */ { "x" : -1150, "y" : -118.97241890367377, "bCoef" : 0, "cMask" : ["wall" ], "curve" : 0, "color" : "b3d4a7" },
		/* 117 */ { "x" : -1259.6013715431845, "y" : 145.49133453725509, "bCoef" : 0, "cMask" : ["wall" ], "color" : "ffffff" },
		/* 118 */ { "x" : -1258.866981665902, "y" : -147.37589424369935, "bCoef" : 0, "cMask" : ["wall" ], "color" : "ffffff" },
		
		/* 119 */ { "x" : -1214.3130746008003, "y" : 115.73975191756831, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "6a9158", "curve" : 0 },
		
		/* 120 */ { "x" : -1260.5929330159947, "y" : 143.48713747966846, "bCoef" : 0, "cMask" : ["wall" ], "color" : "6a9158" },
		
		/* 121 */ { "x" : -1212.3299516551804, "y" : 119.74814603274154, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "6a9158", "curve" : 0 },
		
		/* 122 */ { "x" : -1258.6098100703748, "y" : 147.4955315948417, "bCoef" : 0, "cMask" : ["wall" ], "color" : "6a9158" },
		
		/* 123 */ { "x" : -1214.4081749675327, "y" : -117.24604016227767, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "6a9158", "curve" : 0 },
		
		/* 124 */ { "x" : -1260.8753935458817, "y" : -145.3843416532927, "bCoef" : 0, "cMask" : ["wall" ], "color" : "6a9158" },
		
		/* 125 */ { "x" : -1213.3871097379695, "y" : -122.24178092786758, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "6a9158", "curve" : 0 },
		
		/* 126 */ { "x" : -1259.8543283163185, "y" : -150.3800824188826, "bCoef" : 0, "cMask" : ["wall" ], "color" : "6a9158" },
		
		/* 127 */ { "x" : -1150.4806674009055, "y" : 117.08328385388425, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "C7E6BD", "curve" : 0 },
		/* 128 */ { "x" : -1213.4801078094943, "y" : 116.81775004310506, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "ffffff", "curve" : 0 },
		/* 129 */ { "x" : -1149.485969316082, "y" : -118.91461989892463, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "ffffff", "curve" : 0 },
		/* 130 */ { "x" : -1212.4854097246707, "y" : -119.1801537097038, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "ffffff", "curve" : 0 },
		
		/* 131 */ { "x" : 80.06046236735585, "y" : 736, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 132 */ { "x" : 80.06046236735585, "y" : 724, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		
		/* 133 */ { "x" : -1150, "y" : -602, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "cornerflag", "curve" : 0, "color" : "D7D7D9" },
		/* 134 */ { "x" : -1150, "y" : -620.49609375, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "cornerflag", "curve" : 0, "color" : "D7D7D9" },
		
		/* 135 */ { "x" : -1148, "y" : -620.49609375, "bCoef" : 0, "cMask" : ["wall" ] },
		/* 136 */ { "x" : -1148, "y" : -602, "bCoef" : 0, "cMask" : ["wall" ] },
		/* 137 */ { "x" : -70, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "color" : "ffffff" },
		/* 138 */ { "x" : -90, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "color" : "ffffff" },
		/* 139 */ { "x" : -70, "y" : 687, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "color" : "ffffff" },
		/* 140 */ { "x" : -110, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 141 */ { "x" : -130, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 142 */ { "x" : -150, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 143 */ { "x" : -170, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 144 */ { "x" : -190, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 145 */ { "x" : -210, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 146 */ { "x" : -230, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 147 */ { "x" : -250, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 148 */ { "x" : -287.01500879340676, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "color" : "ffffff" },
		/* 149 */ { "x" : -286.93953763264415, "y" : 687, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "color" : "ffffff" },
		/* 150 */ { "x" : -270, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "color" : "ffffff" },
		/* 151 */ { "x" : -286.93953763264415, "y" : 736, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "vis" : false },
		/* 152 */ { "x" : -286.93953763264415, "y" : 724, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 153 */ { "x" : -286.93953763264415, "y" : 710, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 154 */ { "x" : -286.93953763264415, "y" : 698, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 155 */ { "x" : -70, "y" : 734.04149391746, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 156 */ { "x" : -70, "y" : 722.0417049239776, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 157 */ { "x" : -70, "y" : 710, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 158 */ { "x" : -70, "y" : 698, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 159 */ { "x" : 297, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "color" : "ffffff" },
		/* 160 */ { "x" : 277, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "color" : "ffffff" },
		/* 161 */ { "x" : 297, "y" : 687, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "color" : "ffffff" },
		/* 162 */ { "x" : 257, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 163 */ { "x" : 237, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 164 */ { "x" : 217, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 165 */ { "x" : 197, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 166 */ { "x" : 177, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 167 */ { "x" : 157, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 168 */ { "x" : 137, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 169 */ { "x" : 117, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 170 */ { "x" : 79.98499120659324, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "color" : "ffffff" },
		/* 171 */ { "x" : 80.06046236735585, "y" : 687, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "color" : "ffffff" },
		/* 172 */ { "x" : 97, "y" : 667, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "color" : "ffffff" },
		/* 173 */ { "x" : 80.06046236735585, "y" : 736, "bCoef" : 10, "cGroup" : ["all" ] },
		/* 174 */ { "x" : 80.06046236735585, "y" : 724, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 175 */ { "x" : 80.06046236735585, "y" : 710, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 176 */ { "x" : 80.06046236735585, "y" : 698, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 177 */ { "x" : 297, "y" : 734.04149391746, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "vis" : false },
		/* 178 */ { "x" : 297, "y" : 722.0417049239776, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 179 */ { "x" : 297, "y" : 710, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		/* 180 */ { "x" : 297, "y" : 698, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		
		/* 181 */ { "x" : 1149.968665547433, "y" : -618.9686646206542, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "cornerflag", "curve" : 0, "color" : "D7D7D9" },
		/* 182 */ { "x" : 1150.0694602019682, "y" : -600.4728455134504, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "cornerflag", "curve" : 0, "color" : "D7D7D9" },
		
		/* 183 */ { "x" : 1148.069489899352, "y" : -600.4619464927276, "bCoef" : 0, "cMask" : ["wall" ] },
		/* 184 */ { "x" : 1147.9686952448167, "y" : -618.9577655999315, "bCoef" : 0, "cMask" : ["wall" ] },
		
		/* 185 */ { "x" : 1158, "y" : -623, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "curve" : 0, "color" : "beff28" },
		
		/* 186 */ { "x" : 1168, "y" : -623, "bCoef" : 0, "cMask" : ["wall" ], "color" : "ff3034" },
		
		/* 187 */ { "x" : 1149, "y" : -623, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "beff28" },
		/* 188 */ { "x" : 1158, "y" : -619.3999938964844, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "curve" : 0, "color" : "beff28" },
		
		/* 189 */ { "x" : 1149, "y" : -619.3999938964844, "bCoef" : 0, "cMask" : ["wall" ], "color" : "ff3034" },
		
		/* 190 */ { "x" : 1168, "y" : -619.3999938964844, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "beff28" },
		
		/* 191 */ { "x" : 1149.7396826762401, "y" : 597.9263578863065, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "cornerflag", "curve" : 0, "color" : "D7D7D9" },
		/* 192 */ { "x" : 1153.08526210564, "y" : 579.1424902194007, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "cornerflag", "curve" : 0, "color" : "D7D7D9" },
		
		/* 193 */ { "x" : 1155.0010783610655, "y" : 579.7166400913391, "bCoef" : 0, "cMask" : ["wall" ] },
		/* 194 */ { "x" : 1151.7040246689874, "y" : 598.3023373212908, "bCoef" : 0, "cMask" : ["wall" ] },
		
		/* 195 */ { "x" : 1161.6678517948505, "y" : 578.0712784773244, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "curve" : 0, "color" : "beff28" },
		
		/* 196 */ { "x" : 1171.2713154212654, "y" : 580.8593757453787, "bCoef" : 0, "cMask" : ["wall" ], "color" : "ff3034" },
		
		/* 197 */ { "x" : 1153.0247345310775, "y" : 575.5619909360759, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "beff28" },
		/* 198 */ { "x" : 1160.6641350766317, "y" : 581.528531244323, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "curve" : 0, "color" : "beff28" },
		
		/* 199 */ { "x" : 1152.0210178128586, "y" : 579.0192437030742, "bCoef" : 0, "cMask" : ["wall" ], "color" : "ff3034" },
		
		/* 200 */ { "x" : 1170.2675987030466, "y" : 584.316628512377, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "beff28" },
		
		/* 201 */ { "x" : -1152.8011166944932, "y" : 581.2713204942369, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "cornerflag", "curve" : 0, "color" : "D7D7D9" },
		/* 202 */ { "x" : -1150.0489225384003, "y" : 599.5615066971152, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "cornerflag", "curve" : 0, "color" : "D7D7D9" },
		
		/* 203 */ { "x" : -1152.026657561816, "y" : 599.8591040377528, "bCoef" : 0, "cMask" : ["wall" ] },
		/* 204 */ { "x" : -1154.7788517179088, "y" : 581.5689178348746, "bCoef" : 0, "cMask" : ["wall" ] },
		
		/* 205 */ { "x" : -1162.170956870286, "y" : 578.11573185304, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "curve" : 0, "color" : "beff28" },
		
		/* 206 */ { "x" : -1152.4133863896525, "y" : 575.9271664975008, "bCoef" : 0, "cMask" : ["wall" ], "color" : "ff3034" },
		
		/* 207 */ { "x" : -1170.9527703028564, "y" : 580.085440673025, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "beff28" },
		/* 208 */ { "x" : -1161.383072006498, "y" : 581.6284631816164, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "curve" : 0, "color" : "beff28" },
		
		/* 209 */ { "x" : -1170.1648854390683, "y" : 583.5981720016015, "bCoef" : 0, "cMask" : ["wall" ], "color" : "ff3034" },
		
		/* 210 */ { "x" : -1151.6255015258641, "y" : 579.4398978260773, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "beff28" },
		/* 211 */ { "x" : -1159, "y" : -623, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "curve" : 0, "color" : "beff28", "radius" : 20 },
		
		/* 212 */ { "x" : -1149, "y" : -623, "bCoef" : 0, "cMask" : ["wall" ], "color" : "ff3034", "radius" : 20 },
		
		/* 213 */ { "x" : -1168, "y" : -623, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "beff28", "radius" : 20 },
		/* 214 */ { "x" : -1159, "y" : -619.3999938964844, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "curve" : 0, "color" : "beff28", "radius" : 20 },
		
		/* 215 */ { "x" : -1168, "y" : -619.3999938964844, "bCoef" : 0, "cMask" : ["wall" ], "color" : "ff3034", "radius" : 20 },
		
		/* 216 */ { "x" : -1149, "y" : -619.3999938964844, "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "color" : "beff28", "radius" : 20 },
		
		/* 217 */ { "x" : -199, "y" : 711, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "curve" : -400 },
		/* 218 */ { "x" : -199, "y" : 700, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "curve" : -400 },
		/* 219 */ { "x" : 164, "y" : 704, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "curve" : -400 },
		/* 220 */ { "x" : 166, "y" : 696, "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "curve" : -400 },
		
		/* 221 */ { "x" : 936.0539164518007, "y" : -13, "trait" : "powerboost", "bCoef" : -2.2, "vis" : false, "cMask" : ["ball" ], "pos" : [935,0 ], "radius" : 10 },
		/* 222 */ { "x" : 935.9681020082038, "y" : 13, "trait" : "powerboost", "bCoef" : -2.2, "vis" : false, "cMask" : ["ball" ], "pos" : [935,0 ], "radius" : 10 },
		
		/* 223 */ { "x" : 1134, "y" : 116.23596984067328, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["redKO" ], "vis" : false, "curve" : 0 },
		/* 224 */ { "x" : 1134, "y" : -123.76361382468703, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["redKO" ], "vis" : false, "curve" : 0 },
		/* 225 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 1300, "y" : 150 },
		/* 226 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 1300, "y" : 18 },
		/* 227 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 1240, "y" : 18 },
		/* 228 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 1300, "y" : -18 },
		/* 229 */ { "bCoef" : 0, "cMask" : ["blue" ], "x" : 1240, "y" : -18 },
		/* 230 */ { "bCoef" : -2.4, "cMask" : ["blue" ], "x" : 1233.0188554822, "y" : 65.50390625 },
		/* 231 */ { "bCoef" : -2.4, "cMask" : ["blue" ], "x" : 1233.0188554822, "y" : -65.49609375 },
		/* 232 */ { "bCoef" : 0, "cMask" : ["red" ], "x" : 735, "y" : 620, "curve" : -74, "vis" : false },
		/* 233 */ { "bCoef" : 0, "cMask" : ["red" ], "x" : 735, "y" : -620, "curve" : -74 },
		/* 234 */ { "x" : 1134, "y" : 116.23596984067328, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "vis" : false, "curve" : 0, "radius" : 15, "pos" : [67,0 ] },
		/* 235 */ { "x" : 1134, "y" : -123.76361382468703, "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "vis" : false, "curve" : 0, "radius" : 15, "pos" : [67,0 ] },
		/* 236 */ { "bCoef" : 0, "cMask" : ["red" ], "x" : 735, "y" : 661, "vis" : false },
		/* 237 */ { "bCoef" : 0, "cMask" : ["red" ], "x" : 735, "y" : -664 }

	],

	"segments" : [
		{ "v0" : 0, "v1" : 1, "color" : "b3d4a7", "trait" : "line", "y" : 250 },
		{ "v0" : 1, "v1" : 3, "color" : "b3d4a7", "trait" : "line", "x" : 840 },
		{ "v0" : 2, "v1" : 3, "color" : "b3d4a7", "trait" : "line", "y" : -250 },
		{ "v0" : 4, "v1" : 5, "color" : "b3d4a7", "trait" : "line", "y" : 195 },
		{ "v0" : 5, "v1" : 7, "color" : "b3d4a7", "trait" : "line", "x" : 1030 },
		{ "v0" : 6, "v1" : 7, "color" : "b3d4a7", "trait" : "line", "y" : -150 },
		{ "v0" : 8, "v1" : 9, "curve" : -110, "color" : "b3d4a7", "trait" : "line", "x" : 840 },
		{ "v0" : 10, "v1" : 11, "color" : "b3d4a7", "trait" : "line", "y" : -337 },
		{ "v0" : 11, "v1" : 13, "color" : "b3d4a7", "trait" : "line", "x" : -840 },
		{ "v0" : 12, "v1" : 13, "color" : "b3d4a7", "trait" : "line", "y" : 250 },
		{ "v0" : 14, "v1" : 15, "color" : "b3d4a7", "trait" : "line", "y" : -150 },
		{ "v0" : 15, "v1" : 17, "color" : "b3d4a7", "trait" : "line", "x" : -1030 },
		{ "v0" : 16, "v1" : 17, "color" : "b3d4a7", "trait" : "line", "y" : 150 },
		{ "v0" : 18, "v1" : 19, "curve" : -110, "color" : "b3d4a7", "trait" : "line", "x" : -840 },
		{ "v0" : 20, "v1" : 21, "curve" : -180, "color" : "a7cf9b", "trait" : "line", "x" : 935 },
		{ "v0" : 22, "v1" : 23, "curve" : -180, "color" : "a7cf9b", "trait" : "line", "x" : -935 },
		{ "v0" : 20, "v1" : 21, "curve" : 180, "color" : "a7cf9b", "trait" : "line", "x" : 935 },
		{ "v0" : 22, "v1" : 23, "curve" : 180, "color" : "a7cf9b", "trait" : "line", "x" : -935 },
		{ "v0" : 20, "v1" : 21, "curve" : 90, "color" : "a7cf9b", "trait" : "line", "x" : 935 },
		{ "v0" : 22, "v1" : 23, "curve" : 90, "color" : "a7cf9b", "trait" : "line", "x" : -935 },
		{ "v0" : 20, "v1" : 21, "curve" : -90, "color" : "a7cf9b", "trait" : "line", "x" : 935 },
		{ "v0" : 22, "v1" : 23, "curve" : -90, "color" : "a7cf9b", "trait" : "line", "x" : -935 },
		{ "v0" : 20, "v1" : 21, "color" : "a7cf9b", "trait" : "line", "x" : 935 },
		{ "v0" : 22, "v1" : 23, "color" : "a7cf9b", "trait" : "line", "x" : -935 },
		{ "v0" : 24, "v1" : 25, "curve" : 90, "color" : "b3d4a7", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line" },
		{ "v0" : 26, "v1" : 27, "curve" : 90, "color" : "b3d4a7", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line" },
		{ "v0" : 28, "v1" : 29, "curve" : 90, "color" : "b3d4a7", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line" },
		{ "v0" : 30, "v1" : 31, "curve" : 90, "color" : "b3d4a7", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line" },
		{ "v0" : 32, "v1" : 33, "curve" : -180, "color" : "b3d4a7", "trait" : "line" },
		{ "v0" : 34, "v1" : 35, "curve" : 180, "color" : "b3d4a7", "trait" : "line" },
		{ "v0" : 32, "v1" : 33, "curve" : -90, "color" : "b3d4a7", "trait" : "line" },
		{ "v0" : 34, "v1" : 35, "curve" : 90, "color" : "b3d4a7", "trait" : "line" },
		{ "v0" : 36, "v1" : 37, "curve" : 40, "vis" : true, "color" : "546f48", "bCoef" : -4.7, "cMask" : ["ball" ], "trait" : "line", "x" : -1220 },
		{ "v0" : 38, "v1" : 39, "curve" : -40, "vis" : true, "color" : "546f48", "bCoef" : -4.7, "cMask" : ["ball" ], "trait" : "line", "x" : 1220 },
		{ "v0" : 40, "v1" : 41, "curve" : -40, "vis" : true, "color" : "546f48", "bCoef" : -4.7, "cMask" : ["ball" ], "trait" : "line", "x" : -1220 },
		{ "v0" : 42, "v1" : 43, "curve" : 40, "vis" : true, "color" : "546f48", "bCoef" : -4.7, "cMask" : ["ball" ], "trait" : "line", "x" : 1220 },
		{ "v0" : 44, "v1" : 45, "curve" : -60, "vis" : true, "color" : "546f48", "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line" },
		{ "v0" : 46, "v1" : 47, "curve" : 60, "vis" : true, "color" : "546f48", "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line" },
		{ "v0" : 48, "v1" : 49, "curve" : -60, "vis" : true, "color" : "546f48", "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line" },
		{ "v0" : 50, "v1" : 51, "curve" : 60, "vis" : true, "color" : "546f48", "bCoef" : -2.45, "cMask" : ["ball" ], "trait" : "line" },
		
		{ "v0" : 41, "v1" : 52, "vis" : true, "bCoef" : 0, "cMask" : ["ball" ] },
		{ "v0" : 40, "v1" : 53, "vis" : true, "cMask" : ["ball" ] },
		{ "v0" : 57, "v1" : 56, "vis" : true, "cMask" : ["ball" ] },
		{ "v0" : 55, "v1" : 54, "vis" : true, "cMask" : ["ball" ] },
		{ "v0" : 63, "v1" : 65, "vis" : true, "color" : "000000", "cMask" : ["ball" ] },
		{ "v0" : 62, "v1" : 64, "vis" : true, "color" : "000000", "cMask" : ["ball" ] },
		{ "v0" : 58, "v1" : 61, "vis" : true, "color" : "000000", "cMask" : ["ball" ] },
		{ "v0" : 59, "v1" : 60, "vis" : true, "color" : "000000", "cMask" : ["ball" ] },
		
		{ "v0" : 67, "v1" : 66, "vis" : true, "color" : "b3d4a7", "bCoef" : 0.1, "cMask" : ["ball" ], "cGroup" : ["ball" ], "trait" : "line", "x" : 0 },
		{ "v0" : 68, "v1" : 69, "curve" : 90, "vis" : true, "color" : "638750", "trait" : "line" },
		{ "v0" : 70, "v1" : 71, "curve" : 90, "vis" : true, "color" : "638750", "trait" : "line" },
		{ "v0" : 72, "v1" : 73, "curve" : 90, "vis" : true, "color" : "638750", "trait" : "line" },
		{ "v0" : 74, "v1" : 75, "curve" : -90, "vis" : true, "color" : "638750", "trait" : "line" },
		{ "v0" : 76, "v1" : 77, "curve" : 0, "vis" : true, "color" : "638750", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "y" : -525 },
		{ "v0" : 78, "v1" : 79, "curve" : 0, "vis" : true, "color" : "638750", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "y" : 525 },
		{ "v0" : 80, "v1" : 81, "vis" : true, "color" : "b3d4a7", "trait" : "line" },
		{ "v0" : 81, "v1" : 82, "vis" : true, "color" : "b3d4a7", "trait" : "line", "y" : 600 },
		{ "v0" : 80, "v1" : 83, "vis" : true, "color" : "b3d4a7", "trait" : "line", "y" : -600 },
		{ "v0" : 82, "v1" : 83, "vis" : true, "color" : "b3d4a7", "trait" : "line" },
		
		{ "v0" : 84, "v1" : 85, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "x" : -1300, "curve" : 259.83403647248304, "cGroup" : ["blueKO","redKO" ] },
		{ "v0" : 86, "v1" : 87, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "y" : -150 },
		{ "v0" : 88, "v1" : 89, "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "y" : 150, "curve" : 0 },
		{ "v0" : 91, "v1" : 92, "vis" : false, "bCoef" : 1000000, "cMask" : ["blue" ], "x" : 1410 },
		{ "v0" : 93, "v1" : 97, "curve" : 0, "vis" : true, "color" : "b3d4a7", "bCoef" : 0, "cMask" : ["wall" ], "x" : 1150 },
		{ "v0" : 94, "v1" : 98, "curve" : 0, "vis" : true, "color" : "ffffff", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 96, "v1" : 99, "curve" : 0, "vis" : true, "color" : "ffffff", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 100, "v1" : 101, "curve" : 0, "vis" : true, "color" : "6a9158", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 102, "v1" : 103, "curve" : 0, "vis" : true, "color" : "6a9158", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 104, "v1" : 105, "curve" : 0, "vis" : true, "color" : "6a9158", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 106, "v1" : 107, "curve" : 0, "vis" : true, "color" : "6a9158", "bCoef" : 0, "cMask" : ["wall" ] },
		
		{ "v0" : 109, "v1" : 111, "curve" : 0, "color" : "ffffff", "cMask" : ["blue","ball" ], "trait" : "reargoalNetleft", "x" : -242, "bCoef" : 0 },
		
		{ "v0" : 108, "v1" : 109, "curve" : 0, "color" : "ffffff", "cMask" : ["blue","ball" ], "trait" : "sidegoalNet", "bCoef" : 0.5 },
		{ "v0" : 110, "v1" : 111, "curve" : 0, "color" : "ffffff", "cMask" : ["blue","ball" ], "trait" : "sidegoalNet", "bCoef" : 0.5 },
		
		{ "v0" : 112, "v1" : 116, "curve" : 0, "vis" : true, "color" : "b3d4a7", "bCoef" : 0, "cMask" : ["wall" ], "x" : -1150 },
		{ "v0" : 113, "v1" : 117, "curve" : 0, "vis" : true, "color" : "ffffff", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 115, "v1" : 118, "curve" : 0, "vis" : true, "color" : "ffffff", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 119, "v1" : 120, "curve" : 0, "vis" : true, "color" : "6a9158", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 121, "v1" : 122, "curve" : 0, "vis" : true, "color" : "6a9158", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 123, "v1" : 124, "curve" : 0, "vis" : true, "color" : "6a9158", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 125, "v1" : 126, "curve" : 0, "vis" : true, "color" : "6a9158", "bCoef" : 0, "cMask" : ["wall" ] },
		
		{ "v0" : 128, "v1" : 130, "curve" : 0, "color" : "ffffff", "cMask" : ["ball" ], "trait" : "reargoalNetleft", "x" : -242 },
		
		{ "v0" : 127, "v1" : 128, "curve" : 0, "color" : "ffffff", "cMask" : ["ball" ], "trait" : "sidegoalNet" },
		{ "v0" : 129, "v1" : 130, "curve" : 0, "color" : "ffffff", "cMask" : ["ball" ], "trait" : "sidegoalNet" },
		
		{ "v0" : 131, "v1" : 132, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "x" : -286.93953763264415 },
		
		{ "v0" : 133, "v1" : 134, "curve" : 0, "vis" : true, "color" : "D7D7D9", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "cornerflag" },
		
		{ "v0" : 135, "v1" : 136, "curve" : 0, "vis" : true, "color" : "6a9158", "bCoef" : 0, "cMask" : ["wall" ], "x" : 717 },
		{ "v0" : 137, "v1" : 138, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		{ "v0" : 137, "v1" : 139, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "x" : -70 },
		{ "v0" : 140, "v1" : 141, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "y" : 667 },
		{ "v0" : 142, "v1" : 143, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "y" : 667 },
		{ "v0" : 144, "v1" : 145, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "y" : 667 },
		{ "v0" : 146, "v1" : 147, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "y" : 667 },
		{ "v0" : 148, "v1" : 149, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		{ "v0" : 148, "v1" : 150, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		{ "v0" : 151, "v1" : 152, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "x" : -286.93953763264415 },
		{ "v0" : 153, "v1" : 154, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "x" : -286.93953763264415 },
		{ "v0" : 155, "v1" : 156, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "x" : -70 },
		{ "v0" : 157, "v1" : 158, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "x" : -70 },
		{ "v0" : 159, "v1" : 160, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		{ "v0" : 159, "v1" : 161, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "x" : -70 },
		{ "v0" : 162, "v1" : 163, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "y" : 667 },
		{ "v0" : 164, "v1" : 165, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "y" : 667 },
		{ "v0" : 166, "v1" : 167, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "y" : 667 },
		{ "v0" : 168, "v1" : 169, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "y" : 667 },
		{ "v0" : 170, "v1" : 171, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		{ "v0" : 170, "v1" : 172, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		{ "v0" : 175, "v1" : 176, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "x" : -286.93953763264415 },
		{ "v0" : 177, "v1" : 178, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "x" : -70 },
		{ "v0" : 179, "v1" : 180, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ], "x" : -70 },
		
		{ "v0" : 181, "v1" : 182, "curve" : 0, "vis" : true, "color" : "D7D7D9", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "cornerflag" },
		
		{ "v0" : 183, "v1" : 184, "curve" : 0, "vis" : true, "color" : "6a9158", "bCoef" : 0, "cMask" : ["wall" ], "x" : 717 },
		{ "v0" : 185, "v1" : 186, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 185, "v1" : 186, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 186, "v1" : 186, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ], "x" : -1148 },
		
		{ "v0" : 185, "v1" : 187, "vis" : true, "color" : "beff28", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line" },
		
		{ "v0" : 188, "v1" : 189, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 188, "v1" : 189, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 189, "v1" : 189, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ] },
		
		{ "v0" : 188, "v1" : 190, "vis" : true, "color" : "beff28", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line" },
		
		{ "v0" : 191, "v1" : 192, "curve" : 0, "vis" : true, "color" : "D7D7D9", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "cornerflag" },
		
		{ "v0" : 193, "v1" : 194, "curve" : 0, "vis" : true, "color" : "6a9158", "bCoef" : 0, "cMask" : ["wall" ], "x" : 717 },
		{ "v0" : 195, "v1" : 196, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 195, "v1" : 196, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 196, "v1" : 196, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ], "x" : -1148 },
		
		{ "v0" : 195, "v1" : 197, "vis" : true, "color" : "beff28", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line" },
		
		{ "v0" : 198, "v1" : 199, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 198, "v1" : 199, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 199, "v1" : 199, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ] },
		
		{ "v0" : 198, "v1" : 200, "vis" : true, "color" : "beff28", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line" },
		
		{ "v0" : 201, "v1" : 202, "curve" : 0, "vis" : true, "color" : "D7D7D9", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "cornerflag" },
		
		{ "v0" : 203, "v1" : 204, "curve" : 0, "vis" : true, "color" : "6a9158", "bCoef" : 0, "cMask" : ["wall" ], "x" : 717 },
		{ "v0" : 205, "v1" : 206, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 205, "v1" : 206, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 206, "v1" : 206, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ], "x" : -1148 },
		
		{ "v0" : 205, "v1" : 207, "vis" : true, "color" : "beff28", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line" },
		
		{ "v0" : 208, "v1" : 209, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 208, "v1" : 209, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ] },
		{ "v0" : 209, "v1" : 209, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ] },
		
		{ "v0" : 208, "v1" : 210, "vis" : true, "color" : "beff28", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line" },
		
		{ "v0" : 211, "v1" : 212, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ], "radius" : 20 },
		{ "v0" : 211, "v1" : 212, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ], "radius" : 20 },
		{ "v0" : 212, "v1" : 212, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ], "x" : -1148, "radius" : 20 },
		
		{ "v0" : 211, "v1" : 213, "vis" : true, "color" : "beff28", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "radius" : 20 },
		
		{ "v0" : 214, "v1" : 215, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ], "radius" : 20 },
		{ "v0" : 214, "v1" : 215, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ], "radius" : 20 },
		{ "v0" : 215, "v1" : 215, "curve" : 0, "vis" : true, "color" : "ff3034", "bCoef" : 0, "cMask" : ["wall" ], "radius" : 20 },
		
		{ "v0" : 214, "v1" : 216, "vis" : true, "color" : "beff28", "bCoef" : 0, "cMask" : ["wall" ], "trait" : "line", "radius" : 20 },
		
		{ "v0" : 217, "v1" : 218, "curve" : -328.13941952332465, "vis" : false, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		{ "v0" : 219, "v1" : 220, "curve" : -336.8674849233308, "vis" : false, "color" : "ffffff", "bCoef" : 0.001, "cMask" : ["wall" ], "cGroup" : ["all" ] },
		
		{ "v0" : 221, "v1" : 222, "curve" : 180, "trait" : "powerboost", "bCoef" : -2.2, "vis" : false, "cMask" : ["ball" ], "pos" : [935,0 ], "radius" : 10 },
		
		{ "v0" : 223, "v1" : 224, "curve" : 0, "vis" : false, "color" : "C7E6BD", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["redKO" ], "x" : 1134 },
		{ "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "v0" : 225, "v1" : 226 },
		{ "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "v0" : 226, "v1" : 227, "y" : 18 },
		{ "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "v0" : 228, "v1" : 229, "y" : -18 },
		{ "vis" : false, "bCoef" : 0, "cMask" : ["blue" ], "v0" : 228, "v1" : 90 },
		{ "vis" : false, "bCoef" : -2.4, "cMask" : ["blue" ], "v0" : 230, "v1" : 231, "x" : 1233.0188554822 },
		{ "curve" : -74, "vis" : false, "bCoef" : 0, "cMask" : ["red" ], "v0" : 232, "v1" : 233 },
		{ "v0" : 234, "v1" : 235, "curve" : 0, "vis" : false, "color" : "C7E6BD", "bCoef" : 1, "cMask" : ["blue" ], "cGroup" : ["blueKO" ], "x" : 1134, "radius" : 15, "pos" : [67,0 ] },
		{ "curve" : 0, "vis" : false, "color" : "6a9158", "bCoef" : 0, "cMask" : ["red" ], "v0" : 232, "v1" : 236 },
		{ "curve" : 0, "vis" : false, "color" : "6a9158", "bCoef" : 0, "cMask" : ["red" ], "v0" : 233, "v1" : 237 }

	],

	"goals" : [
		{ "p0" : [-1161.3,115 ], "p1" : [-1161.3,-116.89189189189187 ], "team" : "red" },
		{ "p0" : [1161.3,115.16891891891896 ], "p1" : [1161.3,-117.98923923923925 ], "team" : "blue" },
		{ "p0" : [1151.8187001142282,-121.478062190417 ], "p1" : [1014.199602660217,-101.29539394052615 ], "team" : "red" },
		{ "p0" : [1150.6265801259315,120.98565833533654 ], "p1" : [1026.839502692259,95.22488810287489 ], "team" : "red" },
		{ "p0" : [1033.9035938100174,-105.6225399413513 ], "p1" : [859.239486391142,-8.193337031992414 ], "team" : "red" },
		{ "p0" : [1032.296032056326,94.29163507192908 ], "p1" : [859.2170868190889,-5.926520547252252 ], "team" : "red" }

	],

	"discs" : [
		{ "radius" : 5, "pos" : [1150,-119 ], "trait" : "goalPost" },
		{ "radius" : 5, "pos" : [1150,116 ], "trait" : "goalPost" },
		
		{ "radius" : 3, "invMass" : 0, "pos" : [1260.5,144 ], "color" : "4a4e52", "cMask" : ["ball" ] },
		{ "radius" : 3, "invMass" : 0, "pos" : [1259.5,-148 ], "color" : "4a4e52", "cMask" : ["ball" ] },
		
		{ "radius" : 5, "pos" : [-1150,116.08750755868094 ], "trait" : "goalPost" },
		{ "radius" : 5, "pos" : [-1150,-118.91461989892463 ], "trait" : "goalPost" },
		
		{ "radius" : 3, "invMass" : 0, "pos" : [-1259.8669727834986,-147.38010906609267 ], "color" : "4a4e52", "cMask" : ["ball" ] },
		{ "radius" : 3, "invMass" : 0, "pos" : [-1260.0977098047515,144.62151209452182 ], "color" : "4a4e52", "cMask" : ["ball" ] },
		
		{ "radius" : 1.5, "pos" : [-1150.5542972394846,-600.1732586129118 ], "color" : "13181C", "trait" : "cornerflag", "curve" : 0 },
		{ "radius" : 1.5, "pos" : [1150.4457027605154,-600.1732586129118 ], "color" : "13181C", "trait" : "cornerflag", "curve" : 0 },
		{ "radius" : 1.5, "pos" : [1148.8518594069587,599.6163281131223 ], "color" : "13181C", "trait" : "cornerflag", "curve" : 0 },
		{ "radius" : 1.5, "pos" : [-1149.6336058891993,599.8040409312609 ], "color" : "13181C", "trait" : "cornerflag", "curve" : 0 },
		
		{ "radius" : 15, "invMass" : 1e-27, "pos" : [-181,705 ], "color" : "4D4C48", "bCoef" : 1000, "cMask" : ["red" ], "cGroup" : ["wall" ], "damping" : 1, "speed" : [0,-0.5 ] },
		{ "radius" : 15, "invMass" : 1e-27, "pos" : [185,705 ], "color" : "403F45", "bCoef" : 1000, "cMask" : ["red" ], "cGroup" : ["wall" ], "damping" : 1, "speed" : [0,-0.5 ] }

	],

	"planes" : [
		{ "normal" : [0,1 ], "dist" : -635, "bCoef" : 0, "trait" : "ballArea" },
		{ "normal" : [0,-1 ], "dist" : -635, "bCoef" : 0, "trait" : "ballArea" },
		
		{ "normal" : [0,1 ], "dist" : -665, "bCoef" : 0 },
		{ "normal" : [0,-1 ], "dist" : -660, "bCoef" : 0 },
		{ "normal" : [1,0 ], "dist" : -1220, "bCoef" : 0, "cMask" : ["ball" ] },
		{ "normal" : [-1,0 ], "dist" : -1220, "bCoef" : 0, "cMask" : ["ball" ] },
		{ "normal" : [1,0 ], "dist" : -117, "bCoef" : 0 },
		{ "normal" : [-1,0 ], "dist" : -1492, "bCoef" : 0 }

	],

	"traits" : {
		"ballArea" : { "vis" : false, "bCoef" : 0, "cMask" : ["ball" ] },
		"goalPost" : { "radius" : 5, "invMass" : 0, "bCoef" : 2 },
		"stanchion" : { "radius" : 3, "invMass" : 0, "bCoef" : 3, "cMask" : ["none" ] },
		"cornerflag" : { "radius" : 3, "invMass" : 0, "bCoef" : 0.5, "color" : "FFFF00", "cGroup" : [ ] },
		"reargoalNetleft" : { "vis" : true, "bCoef" : 0.1, "cMask" : ["ball","red","blue" ], "curve" : 10, "color" : "C7E6BD" },
		"reargoalNetright" : { "vis" : true, "bCoef" : 0.1, "cMask" : ["ball","red","blue" ], "curve" : -10, "color" : "C7E6BD" },
		"sidegoalNet" : { "vis" : true, "bCoef" : 1, "cMask" : ["ball","red","blue" ], "color" : "C7E6BD" },
		"kickOffBarrier" : { "vis" : false, "bCoef" : 0.1, "cGroup" : ["redKO","blueKO" ], "cMask" : ["red","blue" ] },
		"line" : { "vis" : true, "cMask" : [ ], "color" : "C7E6BD" },
		"tunnel" : { "vis" : true, "cMask" : ["red","blue" ], "color" : "000000" },
		"advertising" : { "vis" : true, "cMask" : ["red","blue" ], "color" : "333333" },
		"teambench" : { "vis" : true, "cMask" : [ ], "color" : "000000" },
		"manager" : { "radius" : 15, "vis" : true, "cMask" : ["red","blue" ], "invMass" : 0, "color" : "333333" },
		"physio" : { "radius" : 15, "vis" : true, "cMask" : ["red","blue" ], "invMass" : 0, "color" : "666666" },
		"redsubs" : { "radius" : 15, "vis" : true, "cMask" : ["red","blue" ], "invMass" : 0, "color" : "E56E56" },
		"bluesubs" : { "radius" : 15, "vis" : true, "cMask" : ["red","blue" ], "invMass" : 0, "color" : "5689E5" }

	}
}`;

// trusted admin list
const CensurarMensajes = ['R.S C.O.N T.I.A', 'r.s c.o.n t.i.a'];

// trusted admin list
const trustBanList = ['Áʀʙɪᴛʀᴏ ʙᴏᴛ', '🏁 Áʀʙɪᴛʀᴏ ʙᴏᴛ 🤖'];
let connections = []
 

room.setCustomStadium(RawRGLHMap);
room.setScoreLimit(3);
room.setTimeLimit(3);
room.setTeamsLock(true);
room.setTeamColors(1, 60, 0xFFFFFF, [0xFF4D40, 0xFF4D40, 0xFF4D40]);
room.setTeamColors(2, 60, 0xFFFFFF, [0x0080ff, 0x0080ff, 0x0080ff]);


function clonekick(player){
    players = room.getPlayerList();
    for (i = 0; i < players.length-1; i++){
        if (player.name == players[i].name){
            room.kickPlayer(player.id,"𝚈𝚊 𝚎𝚡𝚒𝚜𝚝𝚎 𝚞𝚗 𝚓𝚞𝚐𝚊𝚍𝚘𝚛 𝚌𝚘𝚗 𝚎𝚜𝚎 𝚗𝚘𝚖𝚋𝚛𝚎 ⚊ 𝐃𝐔",false);
        }
    }
}
 
var ScoresNumbers = '0️⃣1️⃣2️⃣3️⃣4️⃣5️⃣6️⃣7️⃣8️⃣9️⃣';
var boldedNumbers = '𝟎𝟏𝟐𝟑𝟒𝟓𝟔𝟕𝟖𝟗';
var circledNumbers = '🄋⓵⓶⓷⓸⓹⓺⓻⓼⓽';
 
function boldedNumber(num){
    var result = '';
    var reversedDigits = [];
    do{
        reversedDigits.push(num % 10);
        num = Math.floor(num / 10);
    }while(num > 0);
    for (var i = reversedDigits.length; i-- > 0; ){
        result += boldedNumbers.substr(reversedDigits[i]*2, 2);
    }
   
    return result;
}

function scorerNumber(num){
    var result = '';
    var reversedDigits = [];
    do{
        reversedDigits.push(num % 10);
        num = Math.floor(num / 10);
    }while(num > 0);
    for (var i = reversedDigits.length; i-- > 0; ){
        result += ScoresNumbers.substr(reversedDigits[i]*3, 3);
    }
   
    return result;
}

 
function circledNumber(num){
    var result = '';
    var reversedDigits = [];
    do{
        reversedDigits.push(num % 10);
        num = Math.floor(num / 10);
    }while(num > 0);
    for (var i = reversedDigits.length; i-- > 0; ){
        if(reversedDigits[i] == 0){
            result += circledNumbers.substr(reversedDigits[i], 2);
        }else{
            result += circledNumbers.substr(1+reversedDigits[i], 1);
        }
    }
   
    return result;
}
 
 
/*
    Functions
*/
// If there are no admins left in the room give admin to one of the remaining players.
function CensuradorDeSpammeros(message) {
    if (CensurarMensajes.includes(message)) {
        return true;
    }else return false;
}

function checkBanedAdmins(player) {
    if (trustBanList.includes(player.name)) {
        room.kickPlayer(player.id,"𝙰𝙲𝙲𝙴𝚂𝙾 𝙳𝙴𝙽𝙴𝙶𝙰𝙳𝙾 🚫", true);
    }
}

function updateAdmins() {
  // Get all players except the host (id = 0 is always the host)
  var players = room.getPlayerList().filter((player) => player.id != 0 );
  if ( players.length == 0 ){room.stopGame();} // No players left, do nothing.
  if ( players.find((player) => player.admin) != null ) return; // There's an admin left so do nothing.
  room.setPlayerAdmin(players[0].id, true); // Give admin to the first non admin player in the list
}
setInterval(function(){room.clearBans(); room.sendChat('Limpié los bans!'); },1800000);
setInterval(function(player, message){
var isRoomMuted = false;
        isRoomMuted = false;
        mutedPlayers = [];
    room.sendChat('Desmutee a todos los jugadores'); },1800000);
setInterval(function(){            
            room.setPlayerAdmin(room.getPlayerList().filter((player) => player.admin == true && player.id != 0)[0].id, false);
            room.setPlayerAdmin(room.getPlayerList().filter((player) => player.id != 0)[2].id, true); 
            room.sendChat('toma admin pibe'); },5400000);
setInterval(function(player, message){
    room.sendAnnouncement("lol Xd", player, 0xffcd2c, "normal", 0);
function initPlayerStats(player){
}
 
 
 
/*
for commands
*/
 
function swapFun(player){
    if (player.admin == true){
        if (room.getScores() == null) {
            players = room.getPlayerList();
            for (i = 0; i < players.length; i++){
                if (players[i].team == 1){
                    room.setPlayerTeam(players[i].id, 2);
                }
                else if (players[i].team == 2){
                    room.setPlayerTeam(players[i].id, 1);
                }
            }
        }
    }
}
 
 
function pushMuteFun(player, message){ // !mute Anddy

    // Prevent somebody to talk in the room (uses the nickname, not the id)
    // need to be admin
    if (player.admin == true){
        if (!(mutedPlayers.includes(message.substr(6)))) mutedPlayers.push(message.substr(6));
    }
}

var isRoomMuted = false;
function UnmuteAll(player, message){ // !mute Anddy
    // Prevent somebody to talk in the room (uses the nickname, not the id)
    // need to be admin
    if (player.admin == true){
        isRoomMuted = false;
        mutedPlayers = [];
        room.sendChat("[💬] " + player.name + " ha desmuteado a todos los jugadores.");
    }
}  
 
function gotMutedFun(player){
    if (mutedPlayers.includes(player.name)){
        return true;
    }
}
function unmuteFun(player, message){ // !unmute Anddy
    // Allow somebody to talk if he has been muted
    // need to be admin
    if (player.admin == true){
        pos = mutedPlayers.indexOf(message.substr(9));
        mutedPlayers.splice(pos, 1);
    }
}
 
function confirmFun(player, message){ // !confirm aaa
    // Prevent somebody to talk in the room (uses the nickname, not the id)
    // need to be admin
    let GLH2015 = message.substr(9);
    let account = HackHax.find(a => a.GLH2015 === GLH2015);
    if (account !== undefined) {
        account.playerId = player.id;
room.sendAnnouncement("[" + player.name + "] " + account.GrandesLigas + " ha accedido a su cuenta.", null, 0x66FFAD, "bold", 0);
room.sendAnnouncement("⚠ PARA VER TUS ESTADÍSTICAS DEBES PONER:", player.id, 0xffcd48, "bold", 0);
room.sendAnnouncement("                   ⬇   ⬇   ⬇   ⬇   ⬇   ⬇   ⬇   ⬇   ⬇ ", player.id, 0xffcd48, "bold", 0);
room.sendAnnouncement("                 '!stats " + account.GrandesLigas + "' (sin las comillas)", player.id, 0xdfff48, "normal", 0);
        confirmedPlayers.add(player.id);
        if (stats.hasOwnProperty(account.GrandesLigas)){}
        else {stats[account.GrandesLigas] = [0, 0, 0, 0, 0, 0, 1000, "D", "D", "D", "D", "D"];}
    }
    return false;
}

function chatasbotFun(player, message){
    if (player.admin == true){
    messagetext = message.substr(11)
    room.sendChat(messagetext);
    return false;
}
}  
 
function adminFun(player, message){ // !admin Andis
    // Gives admin to the person who type this password
 
    room.setPlayerAdmin(player.id, true);
    return false; // The message won't be displayed
}
 
function resignFun(player, message){
    room.setPlayerAdmin(player.id, false);
    updateAdmins();
}
 
function CamisetasFun(player) { // !camisetas
    room.sendAnnouncement("| !laliga | !seriea | !serieb | !premierleague | !bundesliga | !eredivisie | !ligue1 |  !superlig | !campeonatoruso | !1hnl | !premierucrania | !superligasuiza | !nb1 ⚽ ✦", player.id, 0xFF6F00, "bold", 0);
    room.sendAnnouncement("✦ ⚽  !paises | !superliga | !ascenso | !brasileirao | !campeonatouruguayo | !ligaparaguaya | !ligaaguila | !ligapro | !liga1peru | !campeonatochileno | !ligaboliviana | !ligamx | !mls | !fantasmas | !amateurs", player.id, 0xFF6F00, "bold", 0);
}
function SuperligaFun(player) { // !superliga
    room.sendAnnouncement("🅰 SUPERLIGA: | !BOC | !RIV | !SLO | !RAC | !IND | !HUR | !GIM | !EST | !NOB | !CEN", player.id, 0xADF4FF, "bold", 0); 
    room.sendAnnouncement("| !BAND | !LAN | !UNI | !CSF | !ALD | !AAAJ | !ATU | !TAL | !ARSE | !DYJ | !CCS", player.id, 0xADF4FF, "bold", 0); 
    room.sendAnnouncement("| !GOD | !VEL | !PAT", player.id, 0xADF4FF, "bold", 0); 
}
function LigaUruguayaFun(player) { // !campeonatouruguayo
    room.sendAnnouncement('(🇺🇾) CAMPEONATO URUGUAYO: | !NAC | !PEN | !DAN | !RAM | !RIU | !WAN | !TOR | !CRL | !DFS', player.id, 0x69CDFF, "bold", 0); 
}
function LaLigaFun(player) { // !laliga
    room.sendAnnouncement('(🇪🇸) LALIGA: | !RMA | !BAR | !ATM | !VAL | !BET | !GET | !LEV | !RAY | !ATH | !RCDE', player.id, 0xFF2A00, "bold", 0); 
}
function SerieATIMFun(player) { // !seriea
    room.sendAnnouncement('(🇮🇹) SERIE A: | !JUV | !ACM | !INT | !ROM | !NAP | !LAZ | !FIO | !ATA', player.id, 0x6699FF, "bold", 0);
}
function PremierLeagueFun(player) { // !premierleague
    room.sendAnnouncement('(🇬🇧) PREMIER LEAGUE: | !TOT | !LIV| !ARS | !CHE| !MUN | !MCI | !AVL | !WBA | !FUL | !LEI ', player.id, 0xFFFFFF, "bold", 0); 
    room.sendAnnouncement('| !SOU | !WAT | !CRY | !EVE | !NEW | !WHU | !WOL | !HUL', player.id, 0xFFFFFF, "bold", 0); 
}
function PaisesFun(player) { // !paises
    room.sendAnnouncement('(🌎) PAISES: | !BRA | !ARG | !URU | !CHI | !COL | !PER | !PGY | !ECU | !VEN | !BOL | !ALE | !ITA', player.id, 0x5793FA, "bold", 0);  
    room.sendAnnouncement('| !ESP | !FRA | !POR | !ING | !HOL | !CRO | !BELG | !NGA | !JAP | !USA | !QAT | !CNO | !CSU | !AUT | !NZE | !RUS', player.id, 0x5793FA, "bold", 0); 
}
function BundesligaFun(player) { // !bundesliga
    room.sendAnnouncement('(🇩🇪) BUNDESLIGA: | !BVB | !FCB | !B𝟎𝟒 | !RBL | !HSV', player.id, 0xF5FAF8, "bold", 0); 
}
function Ligue1Fun(player) { // !ligue1
    room.sendAnnouncement('(🇫🇷) LIGUE 1: | !PSG | !OGC | !OM | !OL | !ASM | !FCN | !REN | !STE', player.id, 0x3744FA, "bold", 0); 
}
function RiverFun(player) { // !RIV
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('riv/titular/red | riv/titular/blue | riv/alternativa/red |riv/alternativa/blue | riv/alternativa/red/2009 | riv/alternativa/blue/2009', player.id, 0x6BFFB5, "normal", 0);
}
function RIVTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, -144, 0x0e0e0e, [0xFFFFFF, 0xff2c30, 0xFFFFFF]);
    }
}
function RIVTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, -144, 0x0e0e0e, [0xFFFFFF, 0xff2c30, 0xFFFFFF]);
    }
}
function RIVAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xFFFFFF, [0x7F1A28, 0x371315, 0x7F1A28]);
    }
}
function RIVAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xFFFFFF, [0x7F1A28, 0x371315, 0x7F1A28]);
    }
}
function RIVAlternativa2009RedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 27, 0xffffff, [0x151515, 0xE01D1B, 0x151515]);
    }
}
function RIVAlternativa2009BlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 27, 0xffffff, [0x151515, 0xE01D1B, 0x151515]);
    }
}
function BocaFun(player) { // !BOC
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x0061ce, "bold", 0);
    room.sendAnnouncement('boc/titular/red | boc/titular/blue | boc/alternativa/red |boc/alternativa/blue', player.id, 0x0061ce, "bold", 0);
    room.sendAnnouncement('boc/alternativa/red/2013 |boc/alternativa/blue/2013', player.id, 0x0061ce, "bold", 0);
}
function BOCTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0xFFFFFF, [0x021AA1, 0xFFE808, 0x021AA1]);
    }
}
function BOCTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0xFFFFFF, [0x021AA1, 0xFFE808, 0x021AA1]);
    }
}
function BOCAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0x001B88, [0xFFFFFF, 0xEDAF00, 0xFFFFFF]);
    }
}
function BOCAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0x001B88, [0xFFFFFF, 0xEDAF00, 0xFFFFFF]);
    }
}
function BOCAlternativa2013RedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0x2b2c41 , [0xF699AC]);
    }
}
function BOCAlternativa2013BlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0x2b2c41 , [0xF699AC]);
    }
}
function SanLorenzoFun(player) { // !SLO
    room.sendAnnouncement('San Lorenzo | 🇦🇷', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('slo/titular/red | slo/titular/blue | slo/alternativa/red | slo/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function SLOTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xFFFFFF, [0x1C3585, 0xFD131E, 0x1C3585]);
    }
}
function SLOTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xFFFFFF, [0x1C3585, 0xFD131E, 0x1C3585]);
    }
}
function SLOAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0x1e2631, [0xF2F3F7, 0xEB212F, 0x1B3146]);
    }
}
function SLOAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0x1e2631, [0xF2F3F7, 0xEB212F, 0x1B3146]);
    }
}
function RacingFun(player) { // !RAC
    room.sendAnnouncement('Racing Club | 🇦🇷', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('rac/titular/red | rac/titular/blue | rac/alternativa/red | rac/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function RACTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0x141414, [0x5BB8F5, 0xFFFFFF, 0x5BB8F5]);
    }
}
function RACTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0x141414, [0x5BB8F5, 0xFFFFFF, 0x5BB8F5]);
    }
}
function RACAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xb2a16c, [0x18191D]);
    }
}
function RACAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xb2a16c, [0x18191D]);
    }
}
function IndependienteFun(player) { // !IND
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('ind/titular/red | ind/titular/blue | ind/alternativa/red | ind/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function CAITitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 60, 0xffffff, [0xeb0421]);
    }
}
function CAITitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 60, 0xffffff, [0xeb0421]);
    }
}
function CAIAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 60, 0xe60828, [0xF8F7F3]);
    }
}
function CAIAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 60, 0xe60828, [0xF8F7F3]);
    }
}
function AtleticoMadridFun(player) { // !ATM
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('atm/titular/red | atm/titular/blue | atm/alternativa/red | atm/alternativa/blue | atm/tercera/red | atm/tercera/blue', player.id, 0x6BFFB5, "normal", 0);
}
function ATMTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xB5B9C9, [0xFFFAFB, 0xF41819, 0xFFFAFB]);
    }
}
function ATMTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xB5B9C9, [0xFFFAFB, 0xF41819, 0xFFFAFB]);
    }
}
function ATMAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xe61711, [0x201F24]);
    }
}
function ATMAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xe61711, [0x201F24]);
    }
}
function ATMTerceraRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 152, 0x0a243f, [0xAFD4EB, 0xA6CFE8]);
    }
}
function ATMTerceraBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 152, 0x0a243f, [0xAFD4EB, 0xA6CFE8]);
    }
}
function BarcelonaFun(player) { // !BAR
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('bar/titular/red | bar/titular/blue | bar/alternativa/red | bar/alternativa/blue | bar/tercera/red | bar/tercera/blue', player.id, 0x6BFFB5, "normal", 0);
}
function BARTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xffda26, [0xBC223B, 0x1D397A, 0xBC223B]);
    }
}
function BARTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xffda26, [0xBC223B, 0x1D397A, 0xBC223B]);
    }
}
function BARAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 60, 0x22285a, [0xFADA3C]);
    }
}
function BARAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 60, 0x22285a, [0xFADA3C]);
    }
}
function BARTerceraRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 60, 0x23285a, [0x4ED9CB, 0x36CCBC]);
    }
}
function BARTerceraBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 60, 0x23285a, [0x4ED9CB, 0x36CCBC]);
    }
}
function RealMadridFun(player) { // !RMA
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('rma/titular/red | rma/titular/blue | rma/alternativa/red | rma/alternativa/blue | rma/tercera/red | rma/tercera/blue', player.id, 0x6BFFB5, "normal", 0);
}
function RMATitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xc3af69, [0xFDFDFD]);
    }
}
function RMATitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xc3af69, [0xFDFDFD]);
    }
}
function RMAAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 243, 0xcebc77, [0x1C2E4D, 0x1C2E4D, 0x233B58]);
    }
}
function RMAAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 243, 0xcebc77, [0x1C2E4D, 0x1C2E4D, 0x233B58]);
    }
}
function RMATerceraRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0x002957, [0x6EE2C8]);
    }
}
function RMATerceraBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0x002957, [0x6EE2C8]);
    }
}
function InterMilanFun(player) { // !INT
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('int/titular/red | int/titular/blue | int/alternativa/red | int/alternativa/blue | int/tercera/red/1997 | int/tercera/blue/1997', player.id, 0x6BFFB5, "normal", 0);
}
function INTTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xFFFFFF, [0x0082E1, 0x0C161E, 0x0082E1]);
    }
}
function INTTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xFFFFFF, [0x0082E1, 0x0C161E, 0x0082E1]);
    }
}
function INTAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0x000000, [0x7DEDDF]);
    }
}
function INTAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0x000000, [0x7DEDDF]);
    }
}
function INTTercera1997RedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0xffb700, [0x3C4144, 0x655F63, 0x3C4144]);
    }
}
function INTTercera1997BlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0xffb700, [0x3C4144, 0x655F63, 0x3C4144]);
    }
}
function MilanFun(player) { // !ACM
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('acm/titular/red | acm/titular/blue | acm/alternativa/red | acm/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function MILTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xf9f9f9, [0xE7002E, 0x242223, 0xE7002E]);
    }
}
function MILTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xf9f9f9, [0xE7002E, 0x242223, 0xE7002E]);
    }
}
function MILAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xa61726, [0xFAFAFA]);
    }
}
function MILAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xa61726, [0xFAFAFA]);
    }
}
function LiverpoolFun(player) { // !LIV
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('liv/titular/red | liv/titular/blue | liv/alternativa/red | liv/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function LIVTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xF7F7F7, [0xA80617, 0xB60D1F, 0xA80617]);
    }
}
function LIVTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xF7F7F7, [0xA80617, 0xB60D1F, 0xA80617]);
    }
}
function LIVAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xd91f29, [0xEBEBF0, 0xF7F7FC, 0xEBEBF0]);
    }
}
function LIVAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xd91f29, [0xEBEBF0, 0xF7F7FC, 0xEBEBF0]);
    }
}
function ArgentinaFun(player) { // !ARG
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('arg/titular/red | arg/titular/blue | arg/alternativa/red | arg/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function ARGTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0x04455c, [0xBCEAEF, 0xFBF6F9, 0xBCEAEF]);
    }
}
function ARGTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0x04455c, [0xBCEAEF, 0xFBF6F9, 0xBCEAEF]);
    }
}
function ARGAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 60, 0x80cfca, [0x0D444B, 0x22383C, 0x1E3539]);
    }
}
function ARGAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 60, 0x80cfca, [0x0D444B, 0x22383C, 0x1E3539]);
    }
}
function BrasilFun(player) { // !BRA
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('bra/titular/red | bra/titular/blue | bra/alternativa/red | bra/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function BRATitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0x019054, [0xF6DC3E]);
    }
}
function BRATitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0x019054, [0xF6DC3E]);
    }
}
function BRAAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 60, 0xfdda01, [0x0853B7, 0x086ACC]);
    }
}
function BRAAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 60, 0xfdda01, [0x0853B7, 0x086ACC]);
    }
}
function ChileFun(player) { // !CHI
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('chi/titular/red | chi/titular/blue', player.id, 0x6BFFB5, "normal", 0);
}
function CHITitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 60, 0xFFFFFF, [0xFF3829]);
    }
}
function CHITitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 60, 0xFFFFFF, [0xFF3829]);
    }
}
function UruguayFun(player) { // !URU
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('uru/titular/red | uru/titular/blue | uru/alternativa/red | uru/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function URUTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0x000000, [0x8ABBE4]);
    }
}
function URUTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0x000000, [0x8ABBE4]);
    }
}
function URUAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0x000000, [0xFCFBFB]);
    }
}
function URUAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0x000000, [0xFCFBFB]);
    }
}
function FranciaFun(player) { // !FRA
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('fra/titular/red | fra/titular/blue | fra/alternativa/red | fra/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function FRATitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 240, 0xf9f9f9, [0x1F273A, 0x1F273A, 0x3C87D9]);
    }
}
function FRATitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 240, 0xf9f9f9, [0x1F273A, 0x1F273A, 0x3C87D9]);
    }
}
function FRAAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 240, 0x171f47, [0xF1F2F4]);
    }
}
function FRAAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 240, 0x171f47, [0xF1F2F4]);
    }
}
function BayernFun(player) { // !FCB
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('fcb/titular/red | fcb/titular/blue | fcb/alternativa/red | fcb/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function FCBTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xFFFFFF, [0xF3000E]);
    }
}
function FCBTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xFFFFFF, [0xF3000E]);
    }
}
function FCBAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0x62676a, [0xF6F8FC]);
    }
}
function FCBAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0x62676a, [0xF6F8FC]);
    }
}
function BorussiaFun(player) { // !BVB
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('bvb/titular/red | bvb/titular/blue | bvb/alternativa/red | bvb/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function BorussiaTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0x1f191a, [0xFFDB00]);
    }
}
function BorussiaTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0x1f191a, [0xFFDB00]);
    }
}
function BorussiaAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xcecfd1, [0x252525]);
    }
}
function BorussiaAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xcecfd1, [0x252525]);
    }
}
function JuventusFun(player) { // !JUV
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('juv/titular/red | juv/titular/blue | juv/alternativa/red | juv/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function JuventusTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 360, 0x9D9FA6, [0xF4F5F6, 0x222424]);
    }
}
function JuventusTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 360, 0x9D9FA6, [0xF4F5F6, 0x222424]);
    }
}
function JuventusAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0xd31218, [0xF9F4EE, 0xF6EDE5]);
    }
}
function JuventusAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0xd31218, [0xF9F4EE, 0xF6EDE5]);
    }
}
function EstudiantesFun(player) { // !EST
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('est/titular/red | est/titular/blue | est/alternativa/red | est/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function EstudiantesTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0x000000, [0xDB1719, 0xFFFFFF, 0xDB1719]);
    }
}
function EstudiantesTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0x000000, [0xDB1719, 0xFFFFFF, 0xDB1719]);
    }
}
function EstudiantesAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 243, 0xFFFFFF, [0x1C1C1E, 0x1C1C1E, 0xC80F22]);
    }
}
function EstudiantesAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 243, 0xFFFFFF, [0x1C1C1E, 0x1C1C1E, 0xC80F22]);
    }
}
function ManUnitedFun(player) { // !MUN
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('mun/titular/red | mun/titular/blue | mun/alternativa/red | mun/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function ManUnitedTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0xfdfdfd, [0xF40022]);
    }
}
function ManUnitedTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0xfdfdfd, [0xF40022]);
    }
}
function ManUnitedAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0x191816, [0xE1D2BF]);
    }
}
function ManUnitedAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0x231f20, [0xF5EAD4]);
    }
}
function ManCityFun(player) { // !MCI
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('mci/titular/red | mci/titular/blue | mci/alternativa/red | mci/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function ManCityTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0xFFFFFF, [0x92D5F5]);
    }
}
function ManCityTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0xFFFFFF, [0x92D5F5]);
    }
}
function ManCityAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 33, 0xf8d711, [0x242424, 0x242424, 0xF58371]);
    }
}
function ManCityAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 33, 0xf8d711, [0x242424, 0x242424, 0xF58371]);
    }
}
function ChelseaFun(player) { // !CHE
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('che/titular/red | che/titular/blue | che/alternativa/red | che/alternativa/blue | che/tercera/red | che/tercera/blue | che/cuarta/red | che/cuarta/blue', player.id, 0x6BFFB5, "normal", 0);
}
function ChelseaTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, -45, 0xFFFFFF, [0x3F60E3, 0x3F60E3, 0x33499F]);
    }
}
function ChelseaTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, -45, 0xFFFFFF, [0x3F60E3, 0x3F60E3, 0x33499F]);
    }
}
function ChelseaAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 52, 0x003b7d, [0xF8F8F8]);
    }
}
function ChelseaAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 52, 0x003b7d, [0xF8F8F8]);
    }
}
function AlemaniaFun(player) { // !ALE
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('ale/titular/red | ale/titular/blue', player.id, 0x6BFFB5, "normal", 0);
}
function AlemaniaTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0x24201d, [0xFFFFFF]);
    }
}
function AlemaniaTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0x24201d, [0xFFFFFF]);
    }
}
function EspanaFun(player) { // !ESP
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('esp/titular/red | esp/titular/blue | esp/alternativa/red | esp/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function EspanaTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0xffdd0e, [0xF81C1E]);
    }
}
function EspanaTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0xffdd0e, [0xF81C1E]);
    }
}
function EspanaAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0xfd2721, [0xE5E6E7]);
    }
}
function EspanaAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0xfd2721, [0xE5E6E7]);
    }
}
function PortugalFun(player) { // !POR
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('por/titular/red | por/titular/blue', player.id, 0x6BFFB5, "normal", 0);
}
function PortugalTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0xf4b568, [0xF31633]);
    }
}
function PortugalTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0xf4b568, [0xF31633]);
    }
}
function NacionalFun(player) { // !NAC
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('nac/titular/red | nac/titular/blue | nac/alternativa/red | nac/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function NacionalTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xf9020a, [0xFAF9FF]);
    }
}
function NacionalTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xf9020a, [0xFAF9FF]);
    }
}
function NacionalAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 50, 0xf9020a, [0x003361, 0xFFFFFF, 0x003361]);
    }
}
function NacionalAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 50, 0xf9020a, [0x003361, 0xFFFFFF, 0x003361]);
    }
}
function PenarolFun(player) { // !PEN
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('pen/titular/red | pen/titular/blue | pen/alternativa/red | pen/alternativa/blue | pen/tercera/red | pen/tercera/blue', player.id, 0x6BFFB5, "normal", 0);
}
function PenarolTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xFFFFFF, [0xfbd029, 0x241f23, 0xfbd029]);
    }
}
function PenarolTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xFFFFFF, [0xfbd029, 0x241f23, 0xfbd029]);
    }
}
function PenarolAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0x0D0D0D, [0xd2ff68]);
    }
}
function PenarolAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0x0D0D0D, [0xd2ff68]);
    }
}
function PenarolTerceraRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0x252427, [0x656069]);
    }
}
function PenarolTerceraBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0x252427, [0x656069]);
    }
}
function DanubioFun(player) { // !DAN
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('dan/titular/red | dan/titular/blue', player.id, 0x6BFFB5, "normal", 0);
}
function DanubioTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 50, 0xdb0d24, [0xFFFFFF, 0x131514, 0xFFFFFF]);
    }
}
function DanubioTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 50, 0xdb0d24, [0xFFFFFF, 0x131514, 0xFFFFFF]);
    }
}
function RamplaJrsFun(player) { // !RAM
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('ram/titular/red | ram/titular/blue', player.id, 0x6BFFB5, "normal", 0);
}
function RamplaJrsTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xFFFFFF, [0xFF2E3B, 0x1D836D, 0xFF2E3B]);
    }
}
function RamplaJrsTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xFFFFFF, [0xFF2E3B, 0x1D836D, 0xFF2E3B]);
    }
}
function HolandaFun(player) { // !HOL
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('hol/titular/red | hol/titular/blue | hol/alternativa/red | hol/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function HolandaTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 240, 0x200801, [0xF85404, 0xF85404, 0xF75E21]);
    }
}
function HolandaTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 240, 0x200801, [0xF85404, 0xF85404, 0xF75E21]);
    }
}
function HolandaAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0x0d285f, [0x4ECDE4, 0x47BAD9, 0x3CA1C7]);
    }
}
function HolandaAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0x0d285f, [0x4ECDE4, 0x47BAD9, 0x3CA1C7]);
    }
}
function ItaliaFun(player) { // !ITA
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('ita/titular/red | ita/titular/blue | ita/alternativa/red | ita/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function ItaliaTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xf9f9f9, [0x0269DC]);
    }
}
function ItaliaTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xf9f9f9, [0x0269DC]);
    }
}
function ItaliaAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0x053da7, [0xF0F1F1]);
    }
}
function ItaliaAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0x053da7, [0xF0F1F1]);
    }
}
function InglaterraFun(player) { // !ING
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('ing/titular/red | ing/titular/blue | ing/alternativa/red | ing/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function InglaterraTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xdc1413, [0xF3F4F9]);
    }
}
function InglaterraTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xdc1413, [0xF3F4F9]);
    }
}
function InglaterraAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xfbf9f9, [0xDB141F]);
    }
}
function InglaterraAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xfbf9f9, [0xDB141F]);
    }
}
function ParisFun(player) { // !PSG
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('psg/titular/red | psg/titular/blue | psg/alternativa/red | psg/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function PSGTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xf3f3f3, [0x293359, 0xE71B38, 0x293359]);
    }
}
function PSGTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xf3f3f3, [0x293359, 0xE71B38, 0x293359]);
    }
}
function PSGAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0x0e0e0e, [0xFB503D]);
    }
}
function PSGAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0x0e0e0e, [0xFB503D]);
    }
}
function RiverURUFun(player) { // !RIU
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('riu/titular/red | riu/titular/blue | riu/alternativa/red | riu/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function RiverURUTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 360, 0x000000, [0xFFFFFF, 0xD20502, 0xFFFFFF]);
    }
}
function RiverURUTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 360, 0x000000, [0xFFFFFF, 0xD20502, 0xFFFFFF]);
    }
}
function RiverURUAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xFFFFFF, [0xFE0002]);
    }
}
function RiverURUAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xFFFFFF, [0xFE0002]);
    }
}
function MontevideoCityTorqueFun(player) { // !TOR
    room.sendAnnouncement('Montevideo City Torque | 🇺🇾', player.id, 0x6BFFB5, "bold", 0);
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('tor/titular/red | tor/titular/blue | tor/alternativa/red | tor/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function MontevideoCityTorqueTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 60, 0xFFFFFF, [0x8fd1ff]);
    }
}
function MontevideoCityTorqueTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 60, 0xFFFFFF, [0x8fd1ff]);
    }
}
function MontevideoCityTorqueAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0x1D1D1D, [0xFFFFFF, 0xE8E7EA, 0xFFFFFF]);
    }
}
function MontevideoCityTorqueAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0x1D1D1D, [0xFFFFFF, 0xE8E7EA, 0xFFFFFF]);
    }
}
function MontevideoWanderersFun(player) { // !WAN
    room.sendAnnouncement('Montevideo Wanderers| 🇺🇾', player.id, 0x6BFFB5, "bold", 0);
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('wan/titular/red | wan/titular/blue | wan/alternativa/red | wan/alternativa/blue | wan/tercera/red | wan/tercera/blue', player.id, 0x6BFFB5, "normal", 0);
}
function MontevideoWanderersTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0xB8B8B8, [0xFFFFFF, 0x000000, 0xFFFFFF]);
    }
}
function MontevideoWanderersTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0xB8B8B8, [0xFFFFFF, 0x000000, 0xFFFFFF]);
    }
}
function MontevideoWanderersAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0x000000, [0x78DEF9, 0xA6E2F9, 0x78DEF9]);
    }
}
function MontevideoWanderersAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0x000000, [0x78DEF9, 0xA6E2F9, 0x78DEF9]);
    }
}
function MontevideoWanderersTerceraRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0x000000, [0xFFFFFF, 0xF1F1F1, 0xFFFFFF]);
    }
}
function MontevideoWanderersTerceraBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0x000000, [0xFFFFFF, 0xF1F1F1, 0xFFFFFF]);
    }
}
function CerroLargoFun(player) { // !CRL
    room.sendAnnouncement('Cerro Largo | 🇺🇾', player.id, 0x6BFFB5, "bold", 0);
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('crl/titular/red | crl/titular/blue | crl/alternativa/red |crl/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function CerroLargoTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 180, 0x1f1e26, [0xFFFFFF, 0x2454DF, 0xFFFFFF]);
    }
}
function CerroLargoTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 180, 0x1f1e26, [0xFFFFFF, 0x2454DF, 0xFFFFFF]);
    }
}
function CerroLargoAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 61, 0x1f1e26, [0x0098CA]);
    }
}
function CerroLargoAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 61, 0x1f1e26, [0x0098CA]);
    }
}
function DefensorSportingFun(player) { // !DFS
    room.sendAnnouncement('Defensor Sporting | 🇺🇾', player.id, 0x6BFFB5, "bold", 0);
    room.sendAnnouncement('Puedes elegir entre:', player.id, 0x6BFFB5, "normal", 0);
    room.sendAnnouncement('dfs/titular/red | dfs/titular/blue | dfs/alternativa/red | dfs/alternativa/blue', player.id, 0x6BFFB5, "normal", 0);
}
function DefensorSportingTitularRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 60, 0xFFFFFF, [0x6D4DB4]);
    }
}
function DefensorSportingTitularBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 60, 0xFFFFFF, [0x6D4DB4]);
    }
}
function DefensorSportingAlternativaRedFun(player){
    if (player.admin == true){
        room.setTeamColors(1, 90, 0x402E6B, [0xFFFFFF, 0x6D4DB4, 0xFFFFFF]);
    }
}
function DefensorSportingAlternativaBlueFun(player){
    if (player.admin == true){
        room.setTeamColors(2, 90, 0x402E6B, [0xFFFFFF, 0x6D4DB4, 0xFFFFFF]);
    }
}



function ReglasFun(player) { // !reglas
    room.sendAnnouncement("📜 REGLAS DE LOS PENALES:", player.id, 0x00FFBB, "normal", 0);
    room.sendAnnouncement("⒈ Sólo puede haber un arquero.", player.id, 0x00FFBB, "normal", 1);
    room.sendAnnouncement("⒉ Los jugadores deben patear en orden.", player.id, 0x00FFBB, "normal", 0);
    room.sendAnnouncement("⒊ El jugador 𝐍𝐎 puede  ″𝙰𝙼𝙰𝙶𝙰𝚁″ en la ejecución del penal.​​", player.id, 0x00FFBB, "normal", 0);
    room.sendAnnouncement("👨‍⚖️ Si incumple con ésta regla, deberá ejecutar nuevamente el penal. ⚖​", player.id, 0x00FFBB, "normal", 0);
    room.sendAnnouncement("⒋ Si un equipo tiene menos de 4 jugadores, tienen derecho a decidir si uno de ellos patea dos veces o eligen a un espectador.", player.id, 0x00FFBB, "normal", 0);
    room.sendAnnouncement("⒌ No vale invadir el área mientras un jugador está por patear.", player.id, 0x00FFBB, "normal", 0);
    room.sendAnnouncement("⒍ Si se ejecutaron todos los penales y aún persiste el empate:", player.id, 0x00FFBB, "normal", 0);
    room.sendAnnouncement("Los arqueros deberán enfrentarse entre ellos hasta 5̲ v̲e̲c̲e̲s̲ c̲o̲m̲o̲ m̲á̲x̲i̲m̲o̲.", player.id, 0x00FFBB, "normal", 0);
    room.sendAnnouncement("Y si el empate persiste, t̲o̲d̲o̲s̲ l̲o̲s̲ j̲u̲g̲a̲d̲o̲r̲e̲s̲ d̲e̲b̲e̲r̲á̲n̲ p̲a̲t̲e̲a̲r̲ l̲o̲s̲ p̲e̲n̲a̲l̲e̲s̲ n̲u̲e̲v̲a̲m̲e̲n̲t̲e̲.", player.id, 0x00FFBB, "normal", 0);
}
function putPauseFun() { // p
    room.pauseGame(true);
}

function unPauseFun() { // !p
    room.pauseGame(false);
}
function helpFun(player) { // !help
    room.sendAnnouncement('💬  Comandos disponibles: "!confirm", "!afk", "afks", "!confirmed_players", "!stats Nickname", "!elohelp", "!eloranking", "!ranking", "!goleadores", "!asistidores"', player.id, 0xFF003C, "normal", 0);
    room.sendAnnouncement('💬  "!pregunta", "!poss", "!adminhelp", "!gkhelp", "!scripts", "!avatars" "!rankhelp", "!nv", "!adormir", "!acomer", "!registrarme",  "!mapas" y "!camisetas".', player.id, 0xFF003C, "normal", 0);
}
    colors = {
        "red": 15729691,
        "green": 10812739,
        "black": 0,
        "transparent": -1,
        "blue": 367351,
        "yellow": 16771089,
        "orange": 16737796,
        "purple": 14886893,
        "white": 16777215,
        "gold": 14140044
    };
function bosshaftColor (player, message) {
    if (player.admin == true){
    let e = message.split(/ +/).slice(1);
    return room.setDiscProperties(0, {
        color: e[0]
    }), !1
}}
function bosshaftColorString (player, message) {
    if (player.admin == true){
    let e = message.split(/ +/).slice(1);
    return (colors.hasOwnProperty(e[0].toLowerCase()) ? room.setDiscProperties(0, {
        color: colors[e[0].toLowerCase()]
    }) : room.sendAnnouncement("Ese color no es válido! Los colores que puedes utilizar son: red/blue/green/yellow/orange/black/white/purple/gold/transparent", player.id, 0x66FFAD, "bold", 0))
}}

function PelotaFun(player) { // !pelota
    if (player.admin == true){
    room.sendAnnouncement('!ball + red/blue/green/yellow/orange/black/white/purple/gold/transparent (sin el + ni el slash)', player.id, 0xFF003C, "normal", 0);
    room.sendAnnouncement('!customball + color (En decimal) | Página para transformar colores: https://convertingcolors.com/', player.id, 0xFF003C, "normal", 0);
}
}
function NumeroUnoFun(player) { // !1
    room.sendAnnouncement('🔢  𝟭         ౹         𝟏          𝟷          𝟣         １         ߗ1𐰯¹₁⥠↿˥⒈         𝟏        𝟷𐰯 І        Ι         Ӏ        ᅵ        𝗹        ।         ⅂        𐐑        ⓵        ①         ➀         ➊          para más ve a https://tell.wtf', player.id, 0xFF003C, "normal", 0);
}
function NumeroDosFun(player) { // !1
    room.sendAnnouncement('🔢  𝟮        Ƨ        2️⃣        ౽        ੨        ૨        ২        २        ௨        𝟐        ２        2        ᒿ        𝟤        ᒾ        ²        ₂        շ        𝟸        ᘖ        𝟚        Ձ        ⒉        ƻ        Չ        Զ        ϩ        ⓶        ②        ➁        ❷        ㈃        ⒛ para más ve a https://tell.wtf', player.id, 0xFF003C, "normal", 0);
}
function NumeroTresFun(player) { // !1
    room.sendAnnouncement('🔢  Ʒ        3        3️⃣        ३        ੩        ʒ        ӡ        Ӡ        ᴣ        ᶾ        э        Э        ℈        ぅ        う        ㄋ        ȝ        Ȝ        𝟯        𝟥        з        ɜ        ᴈ        ᢃ        ౩        ⓷        ③        ➂        ❸        ੩        ૩        ३ para más ve a https://tell.wtf', player.id, 0xFF003C, "normal", 0);
}
function NumeroCuatroFun(player) { // !1
    room.sendAnnouncement('🔢  𝟰        ㏣        ㍜        𝟒        ４        𝟺        𝟦        4        ₄        ⁴        Ϥ        կ        Կ        Ч        ч        ɥ        ౺        ⒋ para más ve a https://tell.wtf', player.id, 0xFF003C, "normal", 0);
}
function NumeroCincoFun(player) { // !1
    room.sendAnnouncement('🔢  Ƽ        ƽ        𐐠        𐑈        𝟱        𝟓        ５        ㏤        5        ㍝        5️⃣        𝟻        5        ₅        ⁵        ⒌ para más ve a https://tell.wtf', player.id, 0xFF003C, "normal", 0);
}
function NumeroSeisFun(player) { // !1
    room.sendAnnouncement('🔢  𝟲        𝟔        ６        𝟼        ㏥        ㍞        6        𝟨        ₆        ⁶        𝟞        ⒍        ⑥        ⓺        ➅        ➏        ❻        ɓ        ꕃ para más ve a https://tell.wtf', player.id, 0xFF003C, "normal", 0);
}
function NumeroSieteFun(player) { // !1
    room.sendAnnouncement('🔢  ⅂        𐐑        ヿ        ⏋        ⌉        𝟳        𝟕        𝟟        7        𝟽        ７        ⁊        ₇        ⁷        𝟩        7️⃣        ⒎        ꔔ para más ve a https://tell.wtf', player.id, 0xFF003C, "normal", 0);
}
function NumeroOchoFun(player) { // !1
    room.sendAnnouncement('🔢  𝟴        𝟖        8        𝟪        ৪        ⁸        ₈        ８        𐌚        𝟾        ꖉ        ⊟        𝛉        ⒏        ㏧        ㍠        8️⃣ para más ve a https://tell.wtf', player.id, 0xFF003C, "normal", 0);
}
function NumeroNueveFun(player) { // !1
    room.sendAnnouncement('🔢  𝟵        𝟗        9        𝟿        ９        𝟫        ⁹        ₉        ୨        ց        ɡ        ᕤ        ⒐        9        ㏨        ㍡        9️⃣        𝟡        ۹        ٩        ᑫ        ᑴ para más ve a https://tell.wtf', player.id, 0xFF003C, "normal", 0);
}
function NumeroDiezFun(player) { // !1
    room.sendAnnouncement('🔢  ⒑        🔟        ⑩        ➉        ➓        ❿        ю        Ю        ㍢        ㏩        ⑽ para más ve a https://tell.wtf', player.id, 0xFF003C, "normal", 0);
}

function RegistrarmeFun(player) { // !registrarme
    playerName = player.name.replace(/ /g,"_");
    room.sendAnnouncement("[💻] @" + playerName + " ➡ Registrate ahora en http://bit.ly/2JJ78O1 para poder ver tus estadísticas. 📊", player.id, 0xFFE600, "normal", 0);
    room.sendAnnouncement("𝘚𝘰́𝘭𝘰 𝘢𝘯̃𝘢𝘥𝘪𝘮𝘰𝘴 𝘫𝘶𝘨𝘢𝘥𝘰𝘳𝘦𝘴 𝘳𝘦𝘨𝘪𝘴𝘵𝘳𝘢𝘥𝘰𝘴 𝘭𝘰𝘴 𝘥𝘪́𝘢𝘴 𝐒𝐀𝐁𝐀𝐃𝐎𝐒 𝘺 𝐃𝐎𝐌𝐈𝐍𝐆𝐎𝐒", player.id, 0xEB172D, "bold", 0);
}
function EstadiosFun(player) { // !estadios
    room.sendAnnouncement('🏟 Puedes seleccionar: !bombonera | !monumental', player.id, 0xFF003C, "normal", 0);

}
function ScriptsDisponiblesFun(player) { // !scripts
    playerName = player.name.replace(/ /g,"_");
    room.sendAnnouncement("[💻] @" + playerName + " para ver los scripts disponibles ve a ➡ http://bit.ly/2XOVKoT ⬅", player.id, 0xFFE600, "normal", 0);
}
function AvataresDisponiblesFun(player) { // !avatar
    playerName = player.name.replace(/ /g,"_");
    room.sendChat("[🔢🔤] @" + playerName + " para ver símbolos para tu avatar ve a:  ➡ https://tell.wtf ⬅");
    room.sendChat("@" + playerName + " y para ver números para tu avatar también puedes poner !1, !2, !3, etc (hasta !10)");
}

function MapasFun(player) { // !mapas
    room.sendAnnouncement('REAL SOCCER ⚽: !rs - !entrenamiento - !pensred - !pensblue', player.id, 0xd32668, "normal", 0);
    room.sendAnnouncement('TENIS 🎾: !tenis', player.id, 0xdc4253, "normal", 0);
    room.sendAnnouncement('VOLLEYBALL 🏐: !voley - !voleibol', player.id, 0xef7b2a, "normal", 0);
    room.sendAnnouncement('FUTSAL ⚽: !futx1 - !futx3 - !futx4 - !pensredfutsalx3 - !pensbluefutsalx3', player.id, 0xf99c1e, "normal", 0);
    room.sendAnnouncement('HANDBALL 🤾: !handball - !pensredhandball - !pensbluehandball', player.id, 0xe25c79, "normal", 0);
    room.sendAnnouncement('RANDOM 🎲: !big - !mundialito - !sniper - !carreras - !escuela - !skate', player.id, 0xcb1dd5, "normal", 0);
}

function adminHelpFun(player) {
    if (player.admin == true){
    room.sendAnnouncement('💬  Comandos disponibles: "!mute Player", "!unmute Player", "!unmuteall", "!clearbans", "!rr", "!kickafks", "!resign", "!pelota" y "!swap" (Para cambiar de equipos).', player.id, 0xFF6600, "normal", 0);
}}
 
 
function gkHelpFun() { // !gkhelp
    room.sendChat('💬  El jugador más atrasado en el saque inicial se establecerá como arquero! (Escribe "!gk" si el bot se equivoca).')
}
function rankHelpFun() { // !gkhelp
    room.sendChat("💬  Consigue puntos en el host! Gol: 2 pts, Asistencia: 1 pts, Victoria: 3 pts, Valla invicta: 3 pts, Derrota: -3 pts, Gol en contra: -2 pts.")
}
function eloHelpFun() {
    room.sendChat("💬 ¡Consigue puntos por ganar partidos! Los puntos se calculan utilizando el sistema elo.")
}
 
function statsFun(player, message){
    if (stats.hasOwnProperty(message.substr(7))){
    ps = stats[message.substr(7)]; // stands for playerstats
    var TotalDePartidosJugados = ps[2] + ps[3]
    var PromedioDeVictorias = ps[2] / TotalDePartidosJugados
    var PorcentajeDeVictorias = PromedioDeVictorias * 100
    var PromedioDeGoles = ps[0] / TotalDePartidosJugados
    var PromedioDeAsistencias = ps[1] / TotalDePartidosJugados
    var Goles = ps[0] * 2
    var Asistencias = ps[1] * 2
    var Victoria = ps[2] * 5
    var VallaInvicta = ps[5] * 3
    var Derrota = ps[3] * 1
    var GolesEnContra = ps[4] * 2
    var PuntosTotales = Goles + Asistencias + Victoria + VallaInvicta - Derrota - GolesEnContra 
    room.sendAnnouncement(message.substr(7) + ": ⚽ Goles: " + ps[0] + ", ➗ ⚽ Promedio de Gol: " + PromedioDeGoles.toFixed(2) + ", 👟 Asistencias: " + ps[1]  + ", ➗ 👟 Promedio de Asistencias: " + PromedioDeAsistencias.toFixed(2) + ",  ❌ Goles en contra: " + ps[4] + ", ✔️ Vallas invictas: " + ps[5] + ",  🏆 Victorias: " + ps[2] + ",  📊 Porcentaje de Victorias: " + PorcentajeDeVictorias.toFixed(2) + "% , 👎 Derrotas: " + ps[3] + ", 💎 ELO: " + ps[6] + " , 🌟 Puntos: " + PuntosTotales, player.id, 0xFFE121, "normal", 0);
    if (ps[7] !== "D" &&  ps[8] !== "D" && ps[9] !== "D" && ps[10] !== "D" && ps[11] !== "D"){room.sendAnnouncement("🎮 Últimos 5 partidos de " + message.substr(7) + ": " + ps[7] + " - " + ps[8] + " - " + ps[9] + " - " + ps[10] + " - " + ps[11], player.id, 0xFFE121, "normal", 0);}
    if (ps[7] !== "D" &&  ps[8] !== "D" && ps[9] !== "D" && ps[10] !== "D" && ps[11] == "D"){room.sendAnnouncement("🎮 Últimos 4 partidos de " + message.substr(7) + ": " + ps[7] + " - " + ps[8] + " - " + ps[9] + " - " + ps[10], player.id, 0xFFE121, "normal", 0);}
    if (ps[7] !== "D" &&  ps[8] !== "D" && ps[9] !== "D" && ps[10] == "D" && ps[11] == "D"){room.sendAnnouncement("🎮 Últimos 3 partidos de " + message.substr(7) + ": " + ps[7] + " - " + ps[8] + " - " + ps[9], player.id, 0xFFE121, "normal", 0);}
    if (ps[7] !== "D" &&  ps[8] !== "D" && ps[9] == "D" && ps[10] == "D" && ps[11] == "D"){room.sendAnnouncement("🎮 Últimos 2 partidos de " + message.substr(7) + ": " + ps[7] + " - " + ps[8], player.id, 0xFFE121, "normal", 0);}
    if (ps[7] !== "D" &&  ps[8] == "D" && ps[9] == "D" && ps[10] == "D" && ps[11] == "D"){room.sendAnnouncement("🎮 Último partido de " + message.substr(7) + ": " + ps[7], player.id, 0xFFE121, "normal", 0);}
    } else{     room.sendAnnouncement("Para ver tus estadísticas debes escribir: !stats NickConElQueTeRegistraste", player.id, 0x63EBE2, "bold", 0);
room.sendAnnouncement("Si aún no te has registrado puedes escribir !registrarme y te dará el link al que tienes debes ir para poder registrarte. Ten en cuenta que sólo añaden jugadores registrados los días Sábados y Domingos. ", player.id, 0xEB172D, "bold", 0);}
}


function clearbansFun(player){ // !clear
    if (player.admin == true){ room.clearBans(); room.sendChat("💎 Los bans han sido reseteados.");}
}
function MinirsFun(player){
    if (player.admin == true){
	realMap2=true;
        room.stopGame();
        room.setCustomStadium(MiniRS);        
        room.startGame() ;
    }
}
function PenalesRedHandballFun(player){
    if (player.admin == true){
        room.stopGame();
        room.setCustomStadium(PensRedHandball);        
        room.startGame() ;
    }
}

function PenalesRedFutsalx3Fun(player){
    if (player.admin == true){
        room.stopGame();
        room.setCustomStadium(PensRedFutsalx3x4);        
        room.startGame() ;
    }
}



function RealSoccer2020Fun(player){
    if (player.admin == true){
	realMap=true;
        room.stopGame();
    room.setScoreLimit(0);
    room.setTimeLimit(0);
        room.setCustomStadium(RawRGLHMap);        
        room.startGame() ;
    }
}



function Futsalx4Fun(player){
    if (player.admin == true){
        room.stopGame();
        room.setCustomStadium(Futsalx4);        
        room.startGame() ;
    }
}

function Futsalx3Fun(player){
    if (player.admin == true){
        room.stopGame();
        room.setCustomStadium(Futsalx3);        
        room.startGame() ;
    }
}


function CarrerasFun(player){
    if (player.admin == true){
        room.stopGame();
        room.setCustomStadium(CarrerasGLH);        
        room.startGame() ;
    }
}

function MundialitoFun(player){
    if (player.admin == true){
        room.stopGame();
        room.setCustomStadium(MundialitoGLH);        
        room.startGame() ;
    }
}

function HandballFun(player){
    if (player.admin == true){
        room.stopGame();
        room.setCustomStadium(Handball);        
        room.startGame() ;
    }
}

function PenaltyRedFun(player){
    if (player.admin == true){
        room.stopGame();
        room.setCustomStadium(pensred);        
        room.startGame() ;
    room.sendChat( "Pᴀʀᴀ ᴠᴇʀ ʟᴀs ʀᴇɢʟᴀs ᴇsᴄʀɪʙᴇ:  !𝚛𝚎𝚐𝚕𝚊𝚜"  );

    }
}
 
function resetFun(player){
    if (player.admin == true){
        room.stopGame();
        room.startGame();
    }
}
 
function gkFun(player){ // !gk
 
    if (room.getScores() != null && room.getScores().time < 60){
        if (player.team == 1) {
            gk[0] = player;
        }
        else if (player.team == 2){
            gk[1] = player;
        }
    }
    return;
}
 
 
function closeFun(player){
    if (player.name == "Pajero"){ // artificially generate an error in order to close the room
        stats.crash();
    }
}


function leaveFun(player, message) {
if (message == "!nv")
room.kickPlayer(player.id, "nv kerido", false);
else if (message == "!adormir")
room.kickPlayer(player.id, "q sueñes con los angelitos cra", false);
else if (message == "!bb")
room.kickPlayer(player.id, "baibai 👋", false);
else if (message == "!acomer")
room.kickPlayer(player.id, "esta!!!!!!!!! 🍽", false);
}
 
 
/*
    For ranking
*/
 
function rankingCalc(player){
    var name = player;
    players = Object.keys(stats);
    account = players.find(a => a === name)
    if (account !== undefined){
    return stats[name][0] * 2 + stats[name][1] * 2 +
            stats[name][2] * 5 + stats[name][5] * 3 -
            stats[name][3] * 3 - stats[name][4] * 2;
    }
    else {return 0;}
}
 
function ranking(player, message){
 
    var overall = [];
    players = Object.keys(stats);
    for (var i = 0; i < players.length; i++) {
        score = rankingCalc(players[i])
        // Gol: 2 pts, Asistencia: 2 pts, Victoria: 5 pts, Valla Invicta: 3 pts, Derrota: -3 pts, Gol en Contra: -2 pts
        overall.push({name: players[i], value: score});
    }
    overall.sort(function(a,b){
        return b.value - a.value;
    })
    let top30 = overall.splice(0, 30);
    let pos = 1;
    if (top30.length) {
    room.sendAnnouncement("💎 𝐑 𝐀 𝐍 𝐊 𝐈 𝐍 𝐆 [𝚃𝙾𝙿𝟹𝟶] 💎: ", player.id, 0xFFE121, "normal", 0);
    }
    while (top30.length) {
    let tmp = top30.splice(0, 5);
    let message = tmp.map(e => `${pos++}) ${e.name}: ${e.value}`).join(", ");
    room.sendAnnouncement(message, player.id, 0xFFE121, "normal", 0);

    }
    room.sendAnnouncement("[🔝] Ver TOP #30 de cada temporada | 🔗 LINK http://bit.ly/2RAwUJy", player.id, 0x30ff83, "bold", 0);
}
 
function eloCalc(player){
    var name = player;
    return stats[name][6];
}

function GoleadoresCalc(player){
    var name = player;
    players = Object.keys(stats);
    account = players.find(a => a === name)
    if (account !== undefined){
    return stats[name][0] * 1;
    }
    else {return 0;}
}
 
function TopGoleadores(player, message){
 
    var overall = [];
    players = Object.keys(stats);
    for (var i = 0; i < players.length; i++) {
        score = GoleadoresCalc(players[i])
        // Gol: 2 pts, Asistencia: 2 pts, Victoria: 5 pts, Valla Invicta: 3 pts, Derrota: -3 pts, Gol en Contra: -2 pts
        overall.push({name: players[i], value: score});
    }
    overall.sort(function(a,b){
        return b.value - a.value;
    })
    let top30 = overall.splice(0, 30);
    let pos = 1;
    if (top30.length) {
    room.sendAnnouncement("[⚽] 💎 MÁXIMOS GOLEADORES 💎: ", player.id, 0xFFE121, "bold", 0);
    }
    while (top30.length) {
    let tmp = top30.splice(0, 5);
    let message = tmp.map(e => `${pos++}) ${e.name}: ${e.value}`).join(", ");
    room.sendAnnouncement(message, player.id, 0xFFE121, "normal", 0);

    }
    room.sendAnnouncement("Para que tus goles sumen a las estadísticas debes registrarte en: http://bit.ly/2JJ78O1", player.id, 0x30ff83, "bold", 0);
}

function AsistidoresCalc(player){
    var name = player;
    players = Object.keys(stats);
    account = players.find(a => a === name)
    if (account !== undefined){
    return stats[name][1] * 1;
    }
    else {return 0;}
}
 
function TopAsistidores(player, message){
 
    var overall = [];
    players = Object.keys(stats);
    for (var i = 0; i < players.length; i++) {
        score = AsistidoresCalc(players[i])
        // Gol: 2 pts, Asistencia: 2 pts, Victoria: 5 pts, Valla Invicta: 3 pts, Derrota: -3 pts, Gol en Contra: -2 pts
        overall.push({name: players[i], value: score});
    }
    overall.sort(function(a,b){
        return b.value - a.value;
    })
    let top30 = overall.splice(0, 30);
    let pos = 1;
    if (top30.length) {
    room.sendAnnouncement("[👟] 💎 MÁXIMOS ASISTIDORES 💎: ", player.id, 0xFFE121, "bold", 0);
    }
    while (top30.length) {
    let tmp = top30.splice(0, 5);
    let message = tmp.map(e => `${pos++}) ${e.name}: ${e.value}`).join(", ");
    room.sendAnnouncement(message, player.id, 0xFFE121, "normal", 0);

    }
    room.sendAnnouncement("Para que tus asistencias sumen a las estadísticas debes registrarte en: http://bit.ly/2JJ78O1", player.id, 0x30ff83, "bold", 0);
}
 
function eloranking(player, message){
 
    var overall = [];
    players = Object.keys(stats);
    for (var i = 0; i < players.length; i++) {
        score = eloCalc(players[i])
        // Gol: 2 pts, Asistencia: 1 pts, Victoria: 3 pts, Valla invicta: 3 pts, Derrota: -3 pts, Gol en contra: -2 pts
        overall.push({name: players[i], value: score});
    }
    overall.sort(function(a,b){
        return b.value - a.value;
    })
    let top15 = overall.splice(0, 15);
    let pos = 1;
    if (top15.length) {
    room.sendAnnouncement("💎 ELO Ranking [TOP15]: ", player.id, 0xFFE121, "bold", 0);
    }
    while (top15.length) {
    let tmp = top15.splice(0, 5);
    let message = tmp.map(e => `${pos++}) ${e.name}: ${e.value}`).join(", ");
    room.sendAnnouncement(message, player.id, 0xFFE121, "bold", 0);
    }
}

 
function whichTeam(){ // gives the players in the red or blue team
    var players = room.getPlayerList();
    var redTeam = players.filter(player => player.team == 1);
    var blueTeam = players.filter(player => player.team == 2);
    return [redTeam, blueTeam]
}
function afkFun(player, message){ // !classic
    if (afkPlayerIDs.has(player.id)){
        afkPlayerIDs.delete(player.id);
        room.sendChat("💎 " + player.name + " volvió! y está listo para jugar!");}
    else {afkPlayerIDs.add(player.id); room.setPlayerTeam(player.id, 0);room.sendAnnouncement("[💤] " + player.name + " se encuentra actualmente 𝐀𝐅𝐊❗❗ ⏱ ⌨", null, 0xff8400, 'normal', 2);}
}
 
function afksFun(player, message){ // !huge
    afkPlayers_list = room.getPlayerList().filter((x) => afkPlayerIDs.has(x.id));
    afkPlayers_list_string = afkPlayers_list.map(x => x.name).join(", ");
    if (afkPlayers_list == "") {
        room.sendChat("💎 No hay jugadores AFK en este host!");
    }
    else {
        room.sendChat("💎 Jugadores AFK: " + afkPlayers_list_string);
    }
}
 
function kickafksFun(player, message){ // !huge
    if (player.admin == true){
        afksPlayers = room.getPlayerList().filter((x) => afkPlayerIDs.has(x.id));
        for(var i=0;i<afksPlayers.length;i++){room.kickPlayer(afksPlayers[i].id,"AFK!",false);}
    }
}
 
function saveStatsFun(){
    var val = JSON.stringify(stats);
    window.localStorage.setItem("stats", val);
    return false;
}
 
function getAverageRank(team){
    average = 0;
    for (var i = 0; i < team.length; i++) {
        if (team[i].name !== undefined){
        average += rankingCalc(team[i].name);}
    }
    return average / team.length;
}
 
 
 
function getRatingDelta(redTeam, blueTeam, redGameResult, blueGameResult) {
 
    redAverage = getAverageRank(redTeam);
    blueAverage = getAverageRank(blueTeam);
 
  var redChanceToWin = 1 / ( 1 + Math.pow(10, (blueAverage - redAverage) / 400));
    var blueChanceToWin = 1 - redChanceToWin;
 
  return [Math.round(32 * (redGameResult - redChanceToWin)), Math.round(32 * (blueGameResult - blueChanceToWin))];
}
 
function updateElo(redTeam, blueTeam, redGameResult, blueGameResult){
    if (redTeam.length == blueTeam.length && redTeam.length == '4' && blueTeam.length == '4'){
        [redDelta, blueDelta] = getRatingDelta(redTeam, blueTeam, redGameResult, blueGameResult)
        for (var i = 0; i < redTeam.length; i++) {
            let account3 = HackHax.find(a => a.playerId === redTeam[i].id);
            if (account3 !== undefined) {stats[account3.GrandesLigas][6] += redDelta;} else{};
            let account4 = HackHax.find(a => a.playerId === blueTeam[i].id);
            if (account4 !== undefined) {stats[account4.GrandesLigas][6] += blueDelta;} else{};
        }
        return redDelta;
    }
    return 0;
}
 
 
function confirmedPlayersFun(player, message){ // !huge
    confirmedPlayers_list = room.getPlayerList().filter((x) => confirmedPlayers.has(x.id));
    confirmedPlayers_list_string = confirmedPlayers_list.map(x => x.name).join(", ");
    if (confirmedPlayers_list == "") {
        room.sendChat("💎 Actualmente no hay jugadores registrados!");
    }
    else {
        room.sendChat("💎 Jugadores registrados: " + confirmedPlayers_list_string);
    }
}


function setpasswordFun(player, message){  //!set_password  !confirm
    if (player.admin == true){
    code = message.substr(14)
    room.setPassword(code);
    room.sendChat("💎 Host bloqueado.");
    return false;
    }
}
 
function clearpasswordFun(player, message){  //!clear_password
    if (player.admin == true){
    room.setPassword();
    room.sendChat("💎 Host desbloqueado.");
    return false;
    }
}
 
 
function backaccountFun(player, message){  //!back876 waffle 10 2 3 2 1 1 1000
    if (player.admin == true){
    var playername = message.substring(message.lastIndexOf(":") + 1,message.lastIndexOf(";"));
    var index = message.substr( message.lastIndexOf(";") + 1 ).split(" ");
    var goals = index[1]
    var assists = index[2]
    var wins = index[3]
    var losses = index[4]
    var og = index[5]
    var cs = index[6]
    var elo = index[7]
    var ws1 = index[8]
    var ws2 = index[9]
    var ws3 = index[10]
    var ws4 = index[11]
    var ws5 = index[12]
    stats[playername] = [parseInt(goals), parseInt(assists), parseInt(wins), parseInt(losses), parseInt(og), parseInt(cs), parseInt(elo), ws1, ws2, ws3, ws4, ws5];  // goals, assists, wins, losses, og, cs, elo
    saveStatsFun();
    return false;
    }
}
 
function addaccountFun(player, message){ //!addaccount Waffle aaa
    var playername = message.substring(message.lastIndexOf(":") + 1,message.lastIndexOf(";"));
    var index = message.substr( message.lastIndexOf(";") + 1 ).split(" ");
    var GLH2015 = index[index.length - 1]
    HackHax.push({GrandesLigas: playername,GLH2015: GLH2015});
    if (stats.hasOwnProperty(playername)){}
    else {stats[playername] = [0, 0, 0, 0, 0, 0, 1000, "D", "D", "D", "D", "D"];}
    saveStatsFun();
    return false;
}
 

function pmFun(player, message){ //!pv
    var pm = message.substr(4);
    var index = message.split(" ").slice(1);
    var playerID = index[0]
    var message2 = message.substr(4).substr(3);
    var message3 = "[✉🔒 PV] ㅡ 👤 By " + player.name + " (ID: " + player.id + ") : " + message2;
    console.log(playerID);
    console.log(index);
    console.log(message);
    console.log(message2);
    console.log(message3);
    room.sendAnnouncement(message3, parseInt(playerID), 0x8271ff, "bold", 2);
    var players = room.getPlayerList().filter((player) => player.id != 0 );
    if ( players.find((player => player.id === playerID))) {room.sendAnnouncement("❌ Ese User ID no funciona!, Escribe # para ver el ID del jugador.", player.id, 0x19FF85, "normal", 0);}
    else {room.sendAnnouncement("[📨] Mensaje Privado enviado con éxito! ✅", player.id, 0x19FF85, "normal", 0);};
    return false;
}
 
 
function isGk(){ // gives the mosts backward players before the first kickOff
    var players = room.getPlayerList();
    var min = players[0];
    min.position = {x: room.getBallPosition().x + 60}
    var max = min;
 
    for (var i = 0; i < players.length; i++) {
        if (players[i].position != null){
            if (min.position.x > players[i].position.x) min = players[i];
            if (max.position.x < players[i].position.x) max = players[i];
        }
    }
    return [min, max]
}
 
 
 
 
 
function updateWinLoseStats(winners, losers){
    if (redTeam.length == blueTeam.length && redTeam.length == '4' && blueTeam.length == '4'){
    for (var i = 0; i < winners.length; i++) {
        let account = HackHax.find(a => a.playerId === winners[i].id);
        if (account !== undefined) {stats[account.GrandesLigas][2] += 1;} else{};
    }
    for (var i = 0; i < losers.length; i++) {
        let account1 = HackHax.find(a => a.playerId === losers[i].id);
        if (account1 !== undefined) {stats[account1.GrandesLigas][3] += 1;} else{};
    }
}
}
 
function updateWinLoseStreakStats(winners, losers){
    if (redTeam.length == blueTeam.length && redTeam.length == '4' && blueTeam.length == '4'){
    for (var i = 0; i < winners.length; i++) {
        let account = HackHax.find(a => a.playerId === winners[i].id);
        if (account !== undefined) {
            if (stats[account.GrandesLigas][10] == "🏆 VICTORIA"){ stats[account.GrandesLigas][11] = "🏆 VICTORIA"; } else if (stats[account.GrandesLigas][10] == "👎 DERROTA"){ stats[account.GrandesLigas][11] = "👎 DERROTA"; } else{};
            if (stats[account.GrandesLigas][9] == "🏆 VICTORIA"){ stats[account.GrandesLigas][10] = "🏆 VICTORIA"; } else if (stats[account.GrandesLigas][9] == "👎 DERROTA"){ stats[account.GrandesLigas][10] = "👎 DERROTA"; } else{};
            if (stats[account.GrandesLigas][8] == "🏆 VICTORIA"){ stats[account.GrandesLigas][9] = "🏆 VICTORIA"; } else if (stats[account.GrandesLigas][8] == "👎 DERROTA"){ stats[account.GrandesLigas][9] = "👎 DERROTA"; } else{};
            if (stats[account.GrandesLigas][7] == "🏆 VICTORIA"){ stats[account.GrandesLigas][8] = "🏆 VICTORIA"; } else if (stats[account.GrandesLigas][7] == "👎 DERROTA"){ stats[account.GrandesLigas][8] = "👎 DERROTA"; } else{};
            stats[account.GrandesLigas][7] = "🏆 VICTORIA";} else{};
    }
    for (var i = 0; i < losers.length; i++) {
        let account1 = HackHax.find(a => a.playerId === losers[i].id);
        if (account1 !== undefined) {
            if (stats[account1.GrandesLigas][10] == "🏆 VICTORIA"){ stats[account1.GrandesLigas][11] = "🏆 VICTORIA"; } else if (stats[account1.GrandesLigas][10] == "👎 DERROTA"){ stats[account1.GrandesLigas][11] = "👎 DERROTA"; } else{};
            if (stats[account1.GrandesLigas][9] == "🏆 VICTORIA"){ stats[account1.GrandesLigas][10] = "🏆 VICTORIA"; } else if (stats[account1.GrandesLigas][9] == "👎 DERROTA"){ stats[account1.GrandesLigas][10] = "👎 DERROTA"; } else{};
            if (stats[account1.GrandesLigas][8] == "🏆 VICTORIA"){ stats[account1.GrandesLigas][9] = "🏆 VICTORIA"; } else if (stats[account1.GrandesLigas][8] == "👎 DERROTA"){ stats[account1.GrandesLigas][9] = "👎 DERROTA"; } else{};
            if (stats[account1.GrandesLigas][7] == "🏆 VICTORIA"){ stats[account1.GrandesLigas][8] = "🏆 VICTORIA"; } else if (stats[account1.GrandesLigas][7] == "👎 DERROTA"){ stats[account1.GrandesLigas][8] = "👎 DERROTA"; } else{};
            stats[account1.GrandesLigas][7] = "👎 DERROTA";} else{};
    }
    }
}
 
function initBallCarrying(redTeam, blueTeam){
    var ballCarrying = new Map();
    var playing = redTeam.concat(blueTeam);
    for (var i = 0; i < playing.length; i++) {
        ballCarrying.set(playing[i].name, [0, playing[i].team]); // secs, team, %
    }
    return ballCarrying;
}
 
 
 
function updateTeamPoss(value){
    if (value[1] == 1) redPoss += value[0];
    if (value[1] == 2) bluePoss += value[0];
}
 
var bluePoss;
var redPoss;
var timeOnHalves;
function PosesionBalonFun(player, message){
    if (room.getScores() == null) return false;
    bluePoss = 0;
    redPoss = 0
    ballCarrying.forEach(updateTeamPoss);
    var redPossPercent = Math.round((redPoss / (redPoss + bluePoss + 0.000001)) * 100);
    var bluePossPercent = Math.round((bluePoss / (redPoss + bluePoss + 0.000001)) * 100);
    room.sendAnnouncement("⛹ Posesión del balón:  Tᴇᴀᴍ Rᴇᴅ 🔴 " + boldedNumber(redPossPercent) + "% - " + boldedNumber(bluePossPercent) + "% Tᴇᴀᴍ Bʟᴜᴇ 🔵 " , player.id, 0x33FFB4, "normal", 0);
   
    var timeOnRedHalf = Math.round((timeOnHalves[0] / (timeOnHalves[0] + timeOnHalves[1] + 0.000001)) * 100);
    var timeOnBlueHalf = Math.round((timeOnHalves[1] / (timeOnHalves[0] + timeOnHalves[1] + 0.000001)) * 100);
    room.sendAnnouncement("◧ Balón en campo de: Tᴇᴀᴍ Rᴇᴅ 🔴 " + boldedNumber(timeOnRedHalf) + "% - " + boldedNumber(timeOnBlueHalf) + "% Tᴇᴀᴍ Bʟᴜᴇ 🔵 " , player.id, 0x33FFB4, "normal", 0);
}
 
function teamPossFun(player, message){
    if (room.getScores() == null) return false;
    bluePoss = 0;
    redPoss = 0
    ballCarrying.forEach(updateTeamPoss);
    var redPossPercent = Math.round((redPoss / (redPoss + bluePoss + 0.000001)) * 100);
    var bluePossPercent = Math.round((bluePoss / (redPoss + bluePoss + 0.000001)) * 100);
    room.sendChat("⛹ Posesión del balón:  Tᴇᴀᴍ Rᴇᴅ 🔴 " + boldedNumber(redPossPercent) + "% - " + boldedNumber(bluePossPercent) + "% Tᴇᴀᴍ Bʟᴜᴇ 🔵 ");
   
    var timeOnRedHalf = Math.round((timeOnHalves[0] / (timeOnHalves[0] + timeOnHalves[1] + 0.000001)) * 100);
    var timeOnBlueHalf = Math.round((timeOnHalves[1] / (timeOnHalves[0] + timeOnHalves[1] + 0.000001)) * 100);
    room.sendChat("◧ Balón en campo de: Tᴇᴀᴍ Rᴇᴅ 🔴 " + boldedNumber(timeOnRedHalf) + "% - " + boldedNumber(timeOnBlueHalf) + "% Tᴇᴀᴍ Bʟᴜᴇ 🔵 ");
} 
 
/*
For the game
*/
 
 
 
// Calculate the distance between 2 points
function pointDistance(p1, p2) {
    var d1 = p1.x - p2.x;
    var d2 = p1.y - p2.y;
    return Math.sqrt(d1 * d1 + d2 * d2);
}
 
function isOvertime(){
    scores = room.getScores();
    if (scores != null){
        if (scores.timeLimit != 0){
            if (scores.time > scores.timeLimit){
                if (scores.red == 0 && hasFinished == false){
                    let account = HackHax.find(a => a.playerId === gk[0].id);
                    if (account !== undefined) {
                    stats[account.GrandesLigas][5] += 1;}else{};
                    let account1 = HackHax.find(a => a.playerId === gk[1].id);
                    if (account1 !== undefined) {
                    stats[account1.GrandesLigas][5] += 1;}else{};
                    hasFinished = true;
                }
            }
        }
    }
}
// return: the name of the team who took a goal
var team_name = team => team == 1 ? "𝐑𝐄𝐃 🔴" : "𝐁𝐋𝐔𝐄 🔵";
 
var team_color = team => team == 1 ? "𝐑𝐄𝐃 🔴" : "𝐁𝐋𝐔𝐄 🔵";
 
// return: whether it's an OG
var isOwnGoal = (team, player) => team != player.team ? " [Gol en contra]" : "";
 
// return: a better display of the second when a goal is scored
var floor = s => s < 10 ? "0" + s : s;
 
// return: whether there's an assist
//var playerTouchedTwice = playerList => playerList[0].team == playerList[1].team ? " (" + playerList[1].name + ")" : "";
 
playerTouchedTwice = function(playerList){
    let account = HackHax.find(a => a.playerId === playerList[1].id);
    if (playerList[0].team == playerList[1].team && account !== undefined){ return " (" + playerList[1].name + "[" + account.GrandesLigas + "]" + ")"; }
    else if (playerList[0].team == playerList[1].team && account == undefined){ return " (" + playerList[1].name + ")"; }
    else{ return "";};
 
}
 
 
 
var stats;
if (!(localStorage.getItem("stats"))){
 stats = {};
} else {stats = JSON.parse(localStorage.getItem("stats"));}
window.setInterval(saveStatsFun, 240);
/* window.setInterval(saveStatsFun, 240); */
var mutedPlayers = []; // Array where will be added muted players
const confirmedPlayers = new Set()
const afkPlayerIDs = new Set()
var init = "init"; // Smth to initialize smth
init.id = 0; // Faster than getting host's id with the method
init.name = "init";
var temp2 = false;
var scorers ; // Map where will be set all scorers in the current game (undefined if reset or end)
var whoTouchedLast; // var representing the last player who touched the ball
var whoTouchedBall = [init, init]; // Array where will be set the 2 last players who touched the ball
var gk = [init, init];
var goalScored = false;
let HackHax = [];
 
HackHax.push({GrandesLigas: "\ud83d\udc4e \u0043\u0075\u0065\u006e\u0074\u0061 \u006e\u006f \u0064\u0065\u0074\u0065\u0063\u0074\u0061\u0064\u0061",GLH2015: "\u0065\u0072\u0072\u006f\u0072\u0064\u0065\u0067\u006c\u0068"}); 
HackHax.push({GrandesLigas: "\u0056\u0065\u0072\u0063\u0068\u0069\u006e\u0069",GLH2015: "\u0063\u0072\u0061\u0073\u0068\u0031\u0030"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0074 \u006c\u0061\u006e\u0067\u0075\u0061\u0067\u0065",GLH2015: "\u006d\u0061\u0074\u0068\u0065\u0075\u0073\u0039\u0038"});
HackHax.push({GrandesLigas: "\u0041\u0070\u0070\u006c\u0065\u004a\u0061\u0063\u006b",GLH2015: "\u0061\u0070\u0061\u0072\u0061\u0074\u006f"});
HackHax.push({GrandesLigas: "\u006e\u0064\u0065\u0041",GLH2015: "\u006d\u0061\u006d\u0061\u0073\u0061\u0061\u006d\u0061\u0073\u0061\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0044\u006f\u006e",GLH2015: "\u0073\u0074\u0065\u0066\u0061\u006e\u006f\u0031\u0039\u0039\u0037"});
HackHax.push({GrandesLigas: "\u004c\u0061 \u004a\u006f\u0079\u0069\u0074\u0061",GLH2015: "\u0073\u0061\u006e\u006d\u0061\u0072\u0074\u0069\u006e\u0030\u0038"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0072\u0069\u0073\u0073\u0061\ud83c\udf3c\ud83d\udc95",GLH2015: "\u0037\u0037\u0035\u0035\u0037\u0031\u0035\u0031"});
HackHax.push({GrandesLigas: "\u0052\u0061\u006d\u0061",GLH2015: "\u0046\u0072\u0065\u0074\u0073\u004f\u006e\u0046\u0069\u0072\u0065\u0031\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0e25\u2113\u044d\u0497\u0e40\u0e23 \u043c\u0e25\u00a2 \u0e25\u2113\u2113\u0e40\u0e23\u2020\u044d\u044f \u0023\u0038",GLH2015: "\u0031\u0034\u002f\u0030\u0033\u002f\u0032\u0030\u0030\u0037\u004d\u0061\u0074"});
HackHax.push({GrandesLigas: "\u0053\u0065\u0072\u0067\u0069\u006f",GLH2015: "\u0061\u006b\u0061\u0073\u0075\u006e\u0061"});
HackHax.push({GrandesLigas: "\u0070\u0078\u0072\u0078\u007a",GLH2015: "\u006d\u0061\u0074\u0068\u0065\u0075\u0073"});
HackHax.push({GrandesLigas: "\u0047\u006f\u0074\u0061\u006d\u0061\u006e\u006f",GLH2015: "\u006c\u006f\u006d\u0069\u0074\u006f\u0070\u0071\u006d\u0074\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u006e\u0061\u0063\u0068\u006f",GLH2015: "\u0072\u006f\u006e\u0061\u006c\u0064\u006f\u0061\u0067\u0075\u0065\u0072\u006f\u0031"});
HackHax.push({GrandesLigas: "\u0042\u0049\u004c\u004c",GLH2015: "\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u006d\u00f6\u0074\u006f\u0072\u0068\u0065\u0061\u0064 \u00b7 \u0073\u0075\u0074",GLH2015: "\u0074\u006f\u006d\u0061\u0073\u0067\u0032\u0030\u0030\u0030"});
HackHax.push({GrandesLigas: "\u004c\u0061\u006e\u007a\u0069\u006c\u006c\u006f\u0074\u0061",GLH2015: "\u0061\u0061\u0061\u006a\u0065\u006c\u0062\u0069\u0063\u0068\u006f"});
HackHax.push({GrandesLigas: "\u0073\u0074\u0075\u0061\u006e\u0069\u006f",GLH2015: "\u0068\u0061\u0078\u0062\u0061\u006c\u006c\u0031\u0038"});
HackHax.push({GrandesLigas: "\u006b\u0061\u00f1\u006f\u006e",GLH2015: "\u006b\u0061\u00f1\u006f\u006e\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004f\u0074\u0061\u006d\u0065\u006e\u0064\u0069",GLH2015: "\u006f\u0074\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0053\u006f\u0068\u0054\u0061\u0070\u0061",GLH2015: "\u0076\u0069\u007a\u0061\u0071\u0032\u0031\u0037"});
HackHax.push({GrandesLigas: "\u0073\u0065\u0075\u006c\u0061",GLH2015: "\u0073\u0065\u0075\u006c\u0061"});
HackHax.push({GrandesLigas: "\u0052\u006f\u0064\u0072\u0069 \u0044\u0065 \u0050\u0061\u0075\u006c",GLH2015: "\u0034\u0033\u0039\u0037\u0031\u0034\u0039\u0039"});
HackHax.push({GrandesLigas: "\u0042\u0065\u0073\u0073\u0065\u0072\u006b \u0052\u0045\u0044",GLH2015: "\u0062\u0061\u0074\u0061\u0074\u0061"});
HackHax.push({GrandesLigas: "\u0072\u0079\u0075\u0064\u0061\u006e",GLH2015: "\u0063\u006f\u0064\u0065\u0062\u0072\u0065\u0061\u006b\u0065\u0072"});
HackHax.push({GrandesLigas: "\u0048\u0065\u006e\u0072\u0069\u0071\u0075\u0065",GLH2015: "\u006d\u0069\u0062\u0072\u0039\u0038"});
HackHax.push({GrandesLigas: "\u0078\u004d\u006f\u0069\u0074\u0061",GLH2015: "\u0033\u0030\u0031\u0031\u0039\u0038"});
HackHax.push({GrandesLigas: "\u004f\u0054 \u007c\u007c \u0042\u006c\u0061\u0063\u006b",GLH2015: "\u0072\u0069\u0076\u0065\u0072\u0070\u006c\u0061\u0074\u0065"});
HackHax.push({GrandesLigas: "\u0045\u006e\u007a\u006f",GLH2015: "\u0062\u006f\u0063\u0061\u0032\u0037\u0074\u0069\u0074\u0075\u006c\u006f\u0073\u0040"});
HackHax.push({GrandesLigas: "\u0043\u0041\u0049\u007c\ud835\udcdc\ud835\udcf2\ud835\udce1\ud835\udcf2\ud835\udd01 \u2022 \u039b\u004a\u04b2",GLH2015: "\u0067\u0061\u0067\u0061\u0031\u0032\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0073\u0074\u0072\u0065\u0078",GLH2015: "\u0062\u0065\u006d\u0031\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0053\u006c\u0064\u0073",GLH2015: "\u006e\u0061\u007a\u0068\u006f\u007a\u006b\u006f\u0031"});
HackHax.push({GrandesLigas: "\u004f\u0073\u0063\u0061\u0072",GLH2015: "\u006d\u006f\u0072\u006f\u0063\u0068\u0069\u0074\u0061\u0031"});
HackHax.push({GrandesLigas: "\u004d\u006f\u0072\u0072\u006f\u0044\u0069\u0061\u0062\u006c\u006f",GLH2015: "\u0061\u0073\u0064\u0066\u0067\u0068\u006a\u006b\u006c\u00f1\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0038\u0039"});
HackHax.push({GrandesLigas: "\u0074\u006f\u006d",GLH2015: "\u0061\u0073\u0064\u0073\u0061\u0061\u0073\u0064"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0065\u006c\u006a\u0075\u0065\u0067\u0061",GLH2015: "\u006c\u006f\u006c\u0061\u0073\u006f\u0039\u0038"});
HackHax.push({GrandesLigas: "\u0052\u006f\u0076\u0069\u0063\u0074\u006f\u0072",GLH2015: "\u006c\u0061\u0063\u0061\u0063\u0061\u0034\u0033"});
HackHax.push({GrandesLigas: "\u004f\u0073\u0063\u0061\u0072 \u0052\u006f\u006d\u0065\u0072\u006f",GLH2015: "\u0053\u0061\u006e\u006c\u006f\u0072\u0065\u006e\u007a\u006f\u0037"});
HackHax.push({GrandesLigas: "\u0041\u006c\u0062\u0065\u0072\u0074\u006f\u0031\u0032\u0036\u0035",GLH2015: "\u0037\u0034\u0037\u0071\u0061\u006e\u0074\u0061\u0073"});
HackHax.push({GrandesLigas: "\u0053\u0068\u0061\u0072\u0061",GLH2015: "\u0062\u006f\u0063\u0061\u006a\u0075\u006e\u0069\u006f\u0072\u0073\u0034\u0031\u0034\u0039\u0030\u0039\u0038\u0036"});
HackHax.push({GrandesLigas: "\u0045\u006c \u0052\u0061\u0079\u006f",GLH2015: "\u0061\u0063\u0061\u0064\u0065\u006d\u0069\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0053\u0061\u0072\u0069\u0065\u006c",GLH2015: "\u0031\u0032\u0033\u0034\u0035"});
HackHax.push({GrandesLigas: "\u0064\u0066\u0066\u0073",GLH2015: "\u0064\u0061\u006e\u0069\u0065\u006c\u0033\u0030"});
HackHax.push({GrandesLigas: "\u0048\u0065\u0072\u0063\u0075\u006c\u0065\u0073",GLH2015: "\u0048\u0065\u006e\u0072\u0069\u0071\u0075\u0065\u0031\u0039\u0030\u0031"});
HackHax.push({GrandesLigas: "\u0054\u0048\u0045 \u0053\u0054\u0055\u0052\u0044\u0045",GLH2015: "\u0064\u0061\u006e\u0069\u0065\u006c\u0032\u0030\u0031\u0039"});
HackHax.push({GrandesLigas: "\u0053\u0063\u006f\u0063\u0063\u006f",GLH2015: "\u0063\u006f\u0063\u006f\u0032"});
HackHax.push({GrandesLigas: "\u0077\u0061\u0074\u0061\u0066\u0061\u006b",GLH2015: "\u0034\u0032\u0032\u0034\u0038\u0038\u0037\u0035"});
HackHax.push({GrandesLigas: "\u0047\u006f\u006e\u007a\u0061\u0030\u0032",GLH2015: "\u0067\u006f\u006e\u007a\u0061\u006c\u006f\u0030\u0032\u0030\u0031\u0030\u0034"});
HackHax.push({GrandesLigas: "\u0074\u0072\u0069\u0073\u0074\u0065\u007a\u0061\u006f",GLH2015: "\u0070\u0065\u0070\u0065\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0053\u0065\u006e\u0069\u006f\u0072\u0050\u0061\u0074\u0061\u0074\u0061",GLH2015: "\u006d\u0061\u0074\u0069\u0064\u0061\u0076\u0069\u0064\u0031\u0030"});
HackHax.push({GrandesLigas: "\u004c\u0075\u0069\u0064\u006a\u0079",GLH2015: "\u006c\u0075\u0069\u0064\u006a\u0079\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0057\u0061\u006e\u0063\u0068\u006f\u0070\u0065",GLH2015: "\u0077\u0061\u006e\u0063\u0068\u006f\u0070\u0065\u0031"});
HackHax.push({GrandesLigas: "\u0073\u006f\u0075\u006c",GLH2015: "\u0074\u006f\u006d\u0061\u0073\u0069\u0074\u006f\u0032\u0030\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0043\u0068\u0072\u0065\u0073",GLH2015: "\u0067\u006f\u0074\u006f\u0073\u006c\u0065\u0065\u0070"});
HackHax.push({GrandesLigas: "\u0052\u0045\u004c\u0041\u004d\u0050\u0041\u0047\u004f",GLH2015: "\u0052\u0045\u004c\u0041\u004d\u0050\u0041\u0047\u004f\u0031\u0032\u0033\u0035"});
HackHax.push({GrandesLigas: "\u004c\u0065\u006d\u006f\u006e \u0058\u0065\u006e\u0065\u0069\u007a\u0065",GLH2015: "\u0062\u006f\u0063\u0061\u006d\u0061\u006e\u0064\u0061"});
HackHax.push({GrandesLigas: "\u0075\u0074\u0069\u006d\u006f\u0031\u0030\u0072\u006f\u006d\u0061\u006e",GLH2015: "\u006e\u0061\u0063\u0068\u006f\u0073\u0031\u0064"});
HackHax.push({GrandesLigas: "\u006e\u0061\u0078\u006f",GLH2015: "\u006e\u0061\u0078\u006f\u006d\u0061\u006e\u005f\u0031\u0039\u0039\u0035"});
HackHax.push({GrandesLigas: "\u0064\u0065 \u006c\u0069\u0067\u0074",GLH2015: "\u0063\u0061\u0063\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0053\u0065\u006d\u0069 \u004e\u006f\u006f\u0062",GLH2015: "\u0041\u006c\u0064\u0072\u0069\u006e\u0031\u0039\u0036\u0039\u0072\u0063\u0040\u0067\u006d\u0061\u0069\u006c\u002e\u0063\u006f\u006d"});
HackHax.push({GrandesLigas: "\u0072\u0061\u006d\u0061\u002d\u0073\u0068\u0069\u006e\u0079",GLH2015: "\u0047\u004f\u004b\u0055\u0073\u0073\u0034"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0072\u0063\u0054\u0065\u0072\u0053\u0074\u0065\u0067\u0065\u006e\u0031",GLH2015: "\u006d\u0061\u0063\u0068\u0061\u0064\u0069\u006e\u0068\u006f\u0031"});
HackHax.push({GrandesLigas: "\u0045\u0053\u0054\u0052\u0045\u004c\u0041\u0053 \u006c \u0044\u0079\u0062\u0061\u006c\u0061\u0070\u0072\u006f\u0032\u0033\u0034",GLH2015: "\u006d\u0061\u0063\u0068\u0061\u0064\u0069\u006e\u0068\u006f"});
HackHax.push({GrandesLigas: "\u0066\u0065\u006c\u0069\u0064\u0069\u0072\u0061",GLH2015: "\u0066\u0065\u006c\u0069\u0031\u0031\u0030\u0033"});
HackHax.push({GrandesLigas: "\u0072\u0061\u007a\u0072",GLH2015: "\u0078\u0064\u0078\u0064\u0034\u0035\u0036"});
HackHax.push({GrandesLigas: "\u0061\u0072\u0079\u0061\u006e\u007c",GLH2015: "\u004b\u0061\u006c\u0064\u0075\u006e\u0069\u0063\u006f\u0034\u0037\u0035\u0036"});
HackHax.push({GrandesLigas: "\u0041\u006e\u0067\u0065\u006c\u0069\u0063\u0068\u0061\u0064",GLH2015: "\u0063\u0065\u0070\u0069\u0074\u0061"});
HackHax.push({GrandesLigas: "\u0066\u0065\u0072\u006e\u0061\u006e\u0064\u0069\u0074\u006f \u006b\u0069\u0074 \u006b\u0061\u0074",GLH2015: "\u006a\u0075\u0076\u0065\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0045\u002e \u0042\u0061\u0072\u0063\u006f",GLH2015: "\u0063\u0061\u0070\u0069\u0074\u0061\u006e\u0061\u007a\u006f"});
HackHax.push({GrandesLigas: "\u0064\u006f\u0075\u0067\u006c\u0069\u0074\u0061\u0073\u0073\u0073 \u003b \u0069\u0075\u0074",GLH2015: "\u0063\u006c\u0061\u0076\u0065\u006c\u0073\u0061\u0032\u0032"});
HackHax.push({GrandesLigas: "\u0042\u0065\u0072\u0062\u0061\u0075 \u0055\u0050",GLH2015: "\u0066\u0061\u0063\u0075\u006e\u0064\u006f\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0038"});
HackHax.push({GrandesLigas: "\u0057\u0065\u006c\u006d\u0061\u0061",GLH2015: "\u0057\u0065\u006c\u006d\u0061\u0061\u0068\u0078"});
HackHax.push({GrandesLigas: "\u013b\u03ad\u03ce\u03ac\u03ae\u0111\u03cc\u03ce\u015f\u0137\u03af",GLH2015: "\u0042\u0075\u0073\u0074\u0061\u006d\u0061\u006e\u0074\u0065\u0031\u0033"});
HackHax.push({GrandesLigas: "\u0054\u0061\u006b\u0075\u0072\u0061",GLH2015: "\u0053\u0069\u0065\u006d\u0070\u0072\u0065\u0073\u0065\u0072\u0065\u006c\u0061\u0070\u0061\u006e\u0074\u0065\u0072\u0061\u006e\u0065\u0067\u0072\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0073\u0068\u0061\u006e\u0067\u0061\u0069\u0078\u006f\u0078\u006f",GLH2015: "\u0031\u0033\u0030\u0036\u0032\u0030\u0030\u0032"});
HackHax.push({GrandesLigas: "\u0053\u0061\u006d\u0074\u0061\u0078",GLH2015: "\u0073\u0061\u006e\u0074\u0069\u0031\u0039\u0039\u0034\u0073\u006c"});
HackHax.push({GrandesLigas: "\u004a\u006f\u0068\u0061\u006e\u006e \u0042\u002e \u0047\u0075\u00f0\u006d\u0075\u006e\u0064\u0073\u0073\u006f\u006e \u0044\u0048",GLH2015: "\u0068\u0061\u0078\u0062\u0061\u006c\u006c\u0037"});
HackHax.push({GrandesLigas: "\u004f\u0053\u004f",GLH2015: "\u006e\u0065\u0074\u0077\u0065\u0062\u0031\u0039\u0039\u0033"});
HackHax.push({GrandesLigas: "\u0065\u0072\u0061 \u0069\u0073\u0074\u0065\u0066\u0069",GLH2015: "\u0065\u006c\u0071\u0075\u0065\u0073\u0069\u0067\u0075\u0065\u0035"});
HackHax.push({GrandesLigas: "\u004d\u0065\u0063\u0068\u0061\u0031\u0031\u0032",GLH2015: "\u0062\u0074\u0034\u0036"});
HackHax.push({GrandesLigas: "\u006d\u0065\u0073\u0073\u0069\u0061\u0073",GLH2015: "\u0045\u007a\u0065\u0071\u0075\u0069\u0065\u006c\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0047\u006f\u006e\u007a\u0061\u006c\u006f \u004d\u0061\u0072\u006f\u006e\u0069 \u0023\u0032\u0030 \ud835\udd38\u211d\ud835\udd3e",GLH2015: "\u0031\u0034\u002f\u0030\u0033\u002f\u0032\u0030\u0030\u0037\u004d\u0061\u0074\u0065\u006f"});
HackHax.push({GrandesLigas: "\u004a\u0075\u006c\u0069\u0061\u006e \u00c1\u006c\u0076\u0061\u0072\u0065\u007a",GLH2015: "\u0066\u006f\u0072\u0074\u006e\u0069\u0074\u0065\u0032\u0031"});
HackHax.push({GrandesLigas: "\u0053\u0068\u0063\u0068\u0065\u0072\u0062\u0069\u006e\u0061",GLH2015: "\u0063\u0068\u0065\u0072\u006e\u006f\u0062\u0079\u006c"});
HackHax.push({GrandesLigas: "\u0044\u002e \u0056\u0061\u006e \u0064\u0065 \u0042\u0065\u0065\u006b \u0023\u0031\u0030 \u004c\u0044\u0052",GLH2015: "\u0069\u006e\u0074\u0065\u0072\u0035\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0050\u0069\u0063\u0068\u0069",GLH2015: "\u0062\u0061\u0074\u0065\u006c\u0066\u0069\u006c\u0031"});
HackHax.push({GrandesLigas: "\u0042\u0069\u007a\u0065\u0072\u0061",GLH2015: "\u0070\u0061\u006d\u0062\u0069\u006c\u006f\u0063\u006f"});
HackHax.push({GrandesLigas: "\u005b\u004b\u0061\u0073\u0070\u0061\u0072\u006f\u0076\u005d",GLH2015: "\u004b\u0034\u0073\u0050\u0031\u0039\u0038\u0036"});
HackHax.push({GrandesLigas: "\u0043\u0068\u006f\u006f\u0073\u0065 \u0061 \u006e\u0069\u0063\u006b\u006e\u0061\u006d\u0065",GLH2015: "\u006c\u0075\u007a\u0075\u0067\u0061\u006d\u0065\u0073"});
HackHax.push({GrandesLigas: "\u004d\u006f\u007a\u007a\u0069",GLH2015: "\u0054\u006f\u006d\u006d\u0079\u004d\u006f\u007a\u007a\u0069\u0031\u0032"});
HackHax.push({GrandesLigas: "\u004a\u0046 \u004d\u0061\u0072\u0074\u0069\u006e\u0065\u007a",GLH2015: "\u0068\u006f\u006c\u0061\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u2727\u005f\u0052\u0065\u0075\u0073",GLH2015: "\u0068\u006f\u006c\u0061\u0061\u0061"});
HackHax.push({GrandesLigas: "\u0043\u0061\u006c\u00ed\u0067\u0075\u006c\u0061",GLH2015: "\u0068\u006f\u006c\u0061\u006b\u0061\u0073\u0065\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0072\u0061\u0076\u0069\u006c\u0068\u0061",GLH2015: "\u006d\u006f\u0069\u0073\u0065\u0073\u0064\u0064\u0062\u0039\u0039"});
HackHax.push({GrandesLigas: "\u0043\u0043\u002d\u0042\u0079\u004e",GLH2015: "\u0043\u0043\u0042\u0059\u004e\u002a"});
HackHax.push({GrandesLigas: "\u002d\u004d\u006f\u0072\u0072\u006f\u0044\u0069\u0061\u0062\u006c\u006f\u0027",GLH2015: "\u0031\u0032\u0033\u0036\u0035\u0034"});
HackHax.push({GrandesLigas: "\u0079\u0075\u006e\u0067 \u006e\u006f\u0074\u0065\u006b\u0069\u006e\u0068\u006f",GLH2015: "\u0079\u0075\u006e\u0067\u006e\u006f\u0074\u0065\u006b\u0069\u006e\u0068\u006f\u0065\u0073\u006c\u0061\u006f\u006e\u0064\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0073\u0065\u0072\u0067\u0069\u006e\u0068\u006f\u005f\u0062\u006f\u0068\u0065\u006d\u0069\u006f",GLH2015: "\u0073\u0065\u0072\u0073\u0065\u0072\u0073\u0065\u0072\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0046\u0061\u0072\u0061\u006f\u006e\u0065",GLH2015: "\u0063\u0075\u006c\u0070\u0061\u0062\u006c\u0065\u0073"});
HackHax.push({GrandesLigas: "\u0074\u0061\u006e \u0062\u0069\u006f\u006e\u0069\u0063\u0061",GLH2015: "\u0070\u0069\u006b\u0061\u0063\u0068\u0075"});
HackHax.push({GrandesLigas: "\u0041\u0075\u0067\u0075\u0073\u0074\u006f\u0021",GLH2015: "\u0052\u0065\u006e\u0061\u0074\u0061\u0035\u0031\u0037"});
HackHax.push({GrandesLigas: "\u0041\u006c\u0074\u006f \u0050\u20ac\u0072\u0072\u006f \u2563 \u0049\u0055\u0054 \u2665 \u0037\u0049",GLH2015: "\u0041\u006c\u0074\u006f \u0050\u0065\u0072\u0072\u006f"});
HackHax.push({GrandesLigas: "\u30c8\u30d3\u30a2\u30b9\u30e2\u30e9\u30f3",GLH2015: "\u0061\u0067\u006f\u0073\u0074\u0069\u006e\u0061\u0031\u0034"});
HackHax.push({GrandesLigas: "\u0046\u006f\u006e\u0074\u0061\u006e\u0061 \u0023\u0032\u0031",GLH2015: "\u0070\u0065\u006c\u006f\u0074\u0075\u0064\u0069\u0074\u006f\u0032\u0032"});
HackHax.push({GrandesLigas: "\u0054\u0069\u006f\u004a\u0075\u0061\u006e",GLH2015: "\u0077\u006e\u0072\u0069\u0063\u006f\u0039\u0039"});
HackHax.push({GrandesLigas: "\u004c\u006f\u0064\u0065",GLH2015: "\u0034\u0035\u0030\u0035\u0032\u0034\u0035\u0038"});
HackHax.push({GrandesLigas: "\u0044\u0061\u0076\u0069\u0064\u0065 \u004d\u006f\u0073\u0063\u0061\u0072\u0064\u0065\u006c\u006c\u0069",GLH2015: "\u0033\u0031\u0031\u0030\u0030\u0034"});
HackHax.push({GrandesLigas: "\u006b\u0069\u0077\u0069",GLH2015: "\u0072\u0065\u0061\u006c\u0066\u0072\u006f"});
HackHax.push({GrandesLigas: "\u0050\u0061\u0075\u006c\u006f\u0053\u0069\u006c\u0061\u0073",GLH2015: "\u0045\u007a\u0065\u0034\u0031\u0033\u0038\u0039\u0037\u0032\u0034"});
HackHax.push({GrandesLigas: "\u0053\u0061\u006e\u0074\u0069 \u0046\u0072\u0065\u006e\u0063\u0068",GLH2015: "\u0053\u0061\u006e\u0074\u0069\u0061\u0067\u006f"});
HackHax.push({GrandesLigas: "\u0050\u0061\u0064\u0072\u0065 \u0047\u0072\u0061\u0073\u0073\u0069",GLH2015: "\u0054\u0061\u006c\u006c\u0065\u0072\u0065\u0073\u0030\u0032"});
HackHax.push({GrandesLigas: "\u0077\u0061\u0073\u0061\u0079\u0031\u0039\u0039\u0032",GLH2015: "\u006c\u0065\u0061\u006e\u0064\u0072\u006f\u0077\u0061\u0073\u0061\u0079\u0031\u0031"});
HackHax.push({GrandesLigas: "\u006e\u0065\u0065\u0065\u0079\u006a\u0072",GLH2015: "\u004d\u0065\u006c\u006c\u0061\u006d\u006f\u0072\u0061\u0066\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0042\u0061\u0072\u0074\u0072\u0061",GLH2015: "\u0061\u0073\u0071\u0077\u0065\u0072\u0033\u0033"});
HackHax.push({GrandesLigas: "\u0053\u0061\u006e\u0074\u0069\u0047\u0061\u0072\u0061\u0069\u0073",GLH2015: "\u004d\u0061\u0067\u0061\u0072\u0061\u0069\u0073\u0034\u0036"});
HackHax.push({GrandesLigas: "\u0056\u0045\u004c\u0045\u005a \u0041\u0052",GLH2015: "\u0063\u0034\u0063\u0034\u0070\u0065\u0064\u006f\u0063\u0075\u006c\u006f\u0070\u0069\u0073"});
HackHax.push({GrandesLigas: "\u0042\u0065\u0073\u0074\u0069\u0061 \u0064\u0065\u006c \u006c\u0061\u0070\u0069\u007a",GLH2015: "\u0074\u0068\u0069\u0061\u0067\u006f\u0065\u006c\u0070\u0072\u006f\u0032\u0032"});
HackHax.push({GrandesLigas: "\u0056\u0052\u0036",GLH2015: "\u006e\u006f\u0073\u0065\u0076\u0072\u0036"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0072\u0069\u0061\u006e\u006f \u0044\u0069\u0061\u007a",GLH2015: "\u0072\u0075\u006d\u0061\u006e\u0069\u0061\u0031"});
HackHax.push({GrandesLigas: "\u0042\u0075\u006d\u0070",GLH2015: "\u0062\u0075\u006d\u0070\u0033\u0036\u0031\u0036"});
HackHax.push({GrandesLigas: "\u0052\u006f\u0072\u0073\u0063\u0068\u0061\u0063\u0068",GLH2015: "\u0073\u006c\u006f\u0077\u0062\u0072\u0061\u0069\u006e\u0065\u0064"});
HackHax.push({GrandesLigas: "\u0064\u0061\u0072\u006b\u006f",GLH2015: "\u0064\u006f\u0072\u006b\u006f"});
HackHax.push({GrandesLigas: "\u1d31\u1d30\u1d2e\u1d31\u1d3f\u1d33",GLH2015: "\u0073\u0043\u0068\u0061\u0074\u007a\u0073\u0063\u0068\u006e\u0065\u0069\u0064\u0045\u0038\u0033\u0072"});
HackHax.push({GrandesLigas: "\u006d\u0061\u006e\u00e9",GLH2015: "\u0062\u006b\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0054\u0061\u0067\u006c\u0069\u0061\u0066\u0069\u0063\u006f",GLH2015: "\u0034\u0032\u0036\u0035\u0032\u0031\u0032\u0030"});
HackHax.push({GrandesLigas: "\u0050\u0061\u006e\u0063\u0068\u006f",GLH2015: "\u0069\u0061\u006d\u006c\u0061\u0070\u0061\u0063\u0069\u006f\u006e\u0035\u0031\u0035\u0031"});
HackHax.push({GrandesLigas: "\u0043\u006f\u0075\u0074\u0069\u0069\u0069\u0069",GLH2015: "\u0052\u0061\u006d\u0069\u0072\u006f\u0032\u0030\u0030\u0036"});
HackHax.push({GrandesLigas: "\u0045\u0052\u0049\u0043\u004b \u004a\u0045\u0053\u0055\u0043\u0052\u0049\u0053\u0054\u004f \u0050\u0055\u004c\u0047\u0041\u0052",GLH2015: "\u0044\u0069\u0072\u0074\u006a\u0075\u006d\u0070\u0031\u0036"});
HackHax.push({GrandesLigas: "\u0044\u0045\u004d\u0041",GLH2015: "\u0064\u0065\u006d\u0061"});
HackHax.push({GrandesLigas: "\u0042\u006f\u0074\u0069\u0074\u0061",GLH2015: "\u0063\u0075\u0065\u0072\u0076\u006f\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0073\u006f\u0073\u0061",GLH2015: "\u0031\u0035\u0039\u0038\u0037\u0034"});
HackHax.push({GrandesLigas: "\u004e\u0069\u0067\u0065\u006c \u0046\u0061\u0072\u0061\u0067\u0065",GLH2015: "\u0038\u0038\u0038\u0038\u0038"});
HackHax.push({GrandesLigas: "\u0042\u0065\u006e \u0053\u0069\u006d\u006d\u006f\u006e\u0073",GLH2015: "\u0061\u006e\u0069\u006d\u0065\u0066\u0061\u006e"});
HackHax.push({GrandesLigas: "\u0032\u0037",GLH2015: "\u0074\u0077\u0065\u006e\u0074\u0079\u0073\u0065\u0076\u0065\u006e"});
HackHax.push({GrandesLigas: "\u0062\u0065\u0073\u0074",GLH2015: "\u0032\u0033\u0034\u0030"});
HackHax.push({GrandesLigas: "\u0042\u0065\u0074\u006f\u0046\u006f\u0072\u0050\u0072\u0065\u0073\u0069\u0064\u0065\u006e\u0074\u0032\u0030\u0032\u0030",GLH2015: "\u0065\u0062\u006b\u0031\u0039\u0039\u0036"});
HackHax.push({GrandesLigas: "\u0061\u006e\u0074",GLH2015: "\u0073\u0074\u0069\u0063\u006b\u0061\u0072\u0065\u006e\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0063\u0068\u0061\u0064",GLH2015: "\u0070\u0075\u0073\u0073"});
HackHax.push({GrandesLigas: "\u0062\u0072\u0061\u0064",GLH2015: "\u0063\u006f\u0063\u006b\u0069\u006e\u0061\u0073\u0073"});
HackHax.push({GrandesLigas: "\u0043\u0061\u006c\u0075\u006d\u0065\u006e\u0074",GLH2015: "\u004d\u0055\u0032\u0030\u0030\u0034"});
HackHax.push({GrandesLigas: "\u0068\u0065\u006e\u0072\u0079 \u0062\u0075\u0072\u0072\u0069\u0073",GLH2015: "\u0077\u006f\u006d\u0062\u0061\u0074"});
HackHax.push({GrandesLigas: "\u0047\u006f\u006e\u007a\u0061\u006c\u006f\u0076\u0069\u0063\u0068 \u0053\u0046",GLH2015: "\u0076\u0069\u0076\u0061\u0062\u006f\u0063\u0061\u0032\u0032"});
HackHax.push({GrandesLigas: "\u0050\u002e\u0050\u006f\u006e\u0063\u0065",GLH2015: "\u0041\u007a\u0063\u0075\u0065\u006e\u0061\u0067\u0061\u0032\u0032\u0037\u0030"});
HackHax.push({GrandesLigas: "\u0043\u0072\u0065\u006c\u0076",GLH2015: "\u0021\u0061\u006c\u0076\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0056\u0061\u006e \u0050\u0065\u0072\u0073\u0069\u0065",GLH2015: "\u0063\u0068\u0069\u0071\u0075\u0069\u0074\u006f\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0044\u006f\u0073\u0065\u0069\u0074",GLH2015: "\u004d\u0069\u006c\u006c\u006f\u0032\u0030\u0030\u0034"});
HackHax.push({GrandesLigas: "\u0067\u0065\u006f\u0066\u0066",GLH2015: "\u006d\u0061\u006d\u0061"});
HackHax.push({GrandesLigas: "\u0057\u0065\u0073\u0074",GLH2015: "\u0037\u0036\u0035\u0036"});
HackHax.push({GrandesLigas: "\u0070\u0072\u0065\u0073\u0074\u0069\u0067\u0065",GLH2015: "\u006e\u006f\u0070\u0072\u0065\u0066\u0065\u0072\u0065\u006e\u0063\u0065"});
HackHax.push({GrandesLigas: "\u0062\u0075\u0072\u0072",GLH2015: "\u0062\u0030\u0072\u0072"});
HackHax.push({GrandesLigas: "\u004c\u0075\u006b\u0061\u0073",GLH2015: "\u0068\u0079\u0070\u0065\u0072\u0062\u0069\u0069\u0072\u0064"});
HackHax.push({GrandesLigas: "\u0053\u002e\u0052\u0061\u006d\u006f\u0073",GLH2015: "\u0053\u0065\u0072\u0067\u0069\u006f\u0052\u0034\u0052\u004d\u0061\u0064\u0072\u0069\u0064"});
HackHax.push({GrandesLigas: "\u2295\u0161\u03b1\u006d\u03b1",GLH2015: "\u0031\u0033\u0035\u0032\u0034\u0036\u0073\u0061"});
HackHax.push({GrandesLigas: "\u0066\u0065\u006e\u0065\u0072\u0069\u0061",GLH2015: "\u0062\u0069\u006b\u006f"});
HackHax.push({GrandesLigas: "\u0042\u0069\u0067\u0066\u0061\u0074\u0073\u006e\u006f\u006f\u007a\u0079",GLH2015: "\u006f\u0070\u0065\u006e\u0073\u0065\u0073\u0061\u006d\u0065"});
HackHax.push({GrandesLigas: "\u004c\u0075\u0063\u0069\u0061\u006e\u006f",GLH2015: "\u0078\u0071\u0065\u0066\u0037"});
HackHax.push({GrandesLigas: "\u004b\u0065\u0076\u0069\u006e\u006d\u0033\u0031",GLH2015: "\u006f\u0073\u0075"});
HackHax.push({GrandesLigas: "\u004c\u0069\u006e\u0064\u0072\u006f\u0073",GLH2015: "\u006b\u0061\u006c\u0065\u0073\u0068\u0061\u006b\u0065"});
HackHax.push({GrandesLigas: "\u0043\u006f\u006d\u0070\u0061\u0073\u0073",GLH2015: "\u0067\u0061\u0079\u0067\u0061\u0079\u0061\u0073\u0073\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0044\u0065\u0072\u0072\u0069\u0063\u006b \u0052\u006f\u0073\u0065",GLH2015: "\u0072\u0065\u0069\u007a\u0065\u0032\u0037"});
HackHax.push({GrandesLigas: "\u0041\u006e\u0074",GLH2015: "\u006f\u0077\u006e\u0069\u0074\u0034\u0031"});
HackHax.push({GrandesLigas: "\u0050\u0061\u006e\u0064\u0061",GLH2015: "\u0031\u0032\u0032\u0037\u0072\u0067"});
HackHax.push({GrandesLigas: "\u0053\u0074\u0061\u0072\u0063\u0072\u0075\u0073\u0068\u0065\u0064",GLH2015: "\u0063\u006f\u0063\u006f\u0063\u0068\u0061\u006e\u0065\u006c"});
HackHax.push({GrandesLigas: "\u006a\u0075\u0061\u006e\u0063\u0068\u0069\u0062\u0072\u0065\u0072\u006f\u0040\u0067\u006d\u0061\u0069\u006c\u002e\u0063\u006f\u006d",GLH2015: "\u007a\u0061\u0072\u0061\u0063\u0068\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0061\u006d\u006f\u0072\u0069\u006e\u0030\u0034",GLH2015: "\u0061\u006d\u006f\u0072\u0069\u006e\u0031\u0038\u0039\u0031"});
HackHax.push({GrandesLigas: "\u0064\u007a\u0065\u006b\u006f",GLH2015: "\u0042\u004f\u0073\u006e\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0070\u0069\u0078\u0065\u006c",GLH2015: "\u006e\u0069\u0067\u0067\u0065\u0072\u0073\u0073\u006d\u0065\u006c\u006c\u0062\u0061\u0064"});
HackHax.push({GrandesLigas: "\u006b\u006e\u006f\u0077\u006c\u0065\u0064\u0067\u0065",GLH2015: "\u0070\u0075\u0072\u0070\u006c\u0065\u0076\u0061\u0073\u0065"});
HackHax.push({GrandesLigas: "\u004b\u0065\u0069\u0073\u007a\u0065\u0072",GLH2015: "\u0045\u007a\u0065\u0034\u0031\u0033\u0038\u0039\u0037\u0032\u0034"});
HackHax.push({GrandesLigas: "\u0071\u0075\u0065\u0073\u0069\u0074\u006f",GLH2015: "\u0070\u0061\u0063\u0068\u0075\u0064\u0075\u0076\u0061"});
HackHax.push({GrandesLigas: "\u0053\u0065\u00f1\u006f\u0072 \u0046\u0050",GLH2015: "\u0064\u0061\u006e\u0069\u006c\u006f"});
HackHax.push({GrandesLigas: "\u004e\u0061\u0078\u006f\u0023\u0037",GLH2015: "\u006d\u0065\u0067\u0061\u0072\u0072\u0061\u0070\u0074\u006f\u0072\u0039\u0039"});
HackHax.push({GrandesLigas: "\u0074\u006f\u0074\u006f\u0069\u0073\u0031\u0033\u0033\u0037",GLH2015: "\u0034\u0030\u0031\u0031\u0035\u0030\u0032\u0031\u0032\u0031\u0032\u0031\u006e"});
HackHax.push({GrandesLigas: "\u0059\u006f\u0075\u006e\u0067\u005f\u004a\u0069\u006a\u006f",GLH2015: "\u0063\u0068\u0065\u006c\u0069\u0074\u006f\u0065\u006c\u006d\u0061\u0073\u0067\u0072\u0061\u006e\u0064\u0065"});
HackHax.push({GrandesLigas: "\u0053\u0068\u0061\u006c\u007a\u0065\u006b",GLH2015: "\u0034\u0038\u0039\u0037\u0035\u0034\u0034\u0032"});
HackHax.push({GrandesLigas: "\u0042\u006c\u0061\u006e\u004b",GLH2015: "\u0074\u006f\u006d\u0061\u0073\u0072\u006f\u0073\u0061\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0047\u0069\u006e\u006b\u0073",GLH2015: "\u0067\u0069\u006e\u006b\u0073"});
HackHax.push({GrandesLigas: "\u0050\u0050\u0042 \u002d \u0043\u0061\u0072\u006c\u006f\u0073 \u0053\u0061\u006e\u0063\u0068\u0065\u007a",GLH2015: "\u0061\u0075\u0064\u0069\u006c\u0065\u0064\u0031\u0033\u0033\u0036"});
HackHax.push({GrandesLigas: "\u211b\u20ac\u0058\ud83d\udc32",GLH2015: "\u006a\u0075\u006c\u0069\u006f\u0032\u0030\u0030\u0037"});
HackHax.push({GrandesLigas: "\u0070\u0065\u0072\u0067\u0061\u0064\u006f\u0075\u0067\u006c\u0061\u0073",GLH2015: "\u0031\u0032\u0033\u006d\u0061\u006d\u0061\u0061"});
HackHax.push({GrandesLigas: "\u0041\u0070\u0070\u006c\u0065\u004a\u0061\u0063\u006b",GLH2015: "\u006e\u006f\u0075\u0073\u0065\u0073\u006c\u006f\u0071\u0075\u0065\u006e\u0064\u006f\u0065\u006e\u006c\u006f\u0073\u0070\u006f\u006f\u0070\u0073"});
HackHax.push({GrandesLigas: "\u0076\u0069\u0063\u0074\u006f\u0072",GLH2015: "\u006a\u0065\u0073\u0075\u0073\u0063\u0068\u006f\u0072\u006f\u0075"});
HackHax.push({GrandesLigas: "\u0048\u006f\u006e\u0067\u006f",GLH2015: "\u0074\u0062\u0061\u0062\u0062\u0065\u006c"});
HackHax.push({GrandesLigas: "\u0053\u006e\u006f\u0077\u0047\u0030\u0044\u0031\u0032\u0033",GLH2015: "\u0073\u006e\u006f\u0077\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0047\u0072\u0065\u006d\u0069\u0073\u0074\u0061 \u004c\u006f\u006b\u006f",GLH2015: "\u0036\u0036\u0038\u0039"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0074\u0073\u0061\u006e\u0074\u0073\u0069\u006c\u006c",GLH2015: "\u006d\u0074\u0031\u0039\u0037\u0037\u0030\u0034"});
HackHax.push({GrandesLigas: "\u0063\u0068\u0065\u0064\u0069\u0061\u006b",GLH2015: "\u0067\u0075\u0073\u0074\u0061\u0076\u006f\u0030\u0031\u0030\u0032"});
HackHax.push({GrandesLigas: "\u0046\u0065\u006c\u0069 \u004e\u0061\u0063\u0069\u006f\u006e\u0061\u006c",GLH2015: "\u0072\u0061\u0074\u0061\u0074\u0061\u0074\u0061"});
HackHax.push({GrandesLigas: "\u0049\u0073\u0068\u0069\u006b\u0061\u0077\u0061",GLH2015: "\u0041\u0062\u0032\u0036\u0030\u0031\u0039\u0034\u0032\u0039"});
HackHax.push({GrandesLigas: "\u004c\u0061\u0073\u0063\u0061 \u0064\u0065 \u0054\u0069\u006a\u006f\u006c\u006f",GLH2015: "\u0032\u0039\u0031\u0031\u0030\u0032\u0032\u0035"});
HackHax.push({GrandesLigas: "\u266b\u002d\u004b\u0065\u006e \u0057\u0065\u0073\u0074\u002d\u266a",GLH2015: "\u006b\u0065\u006b\u0061\u0072\u0061\u006a\u006f\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0049\u0073\u006c\u0061\u0073 \u0056\u00ed\u0072\u0067\u0065\u006e\u0065\u0073",GLH2015: "\u0073\u0068\u0075\u0072\u0069\u0032\u0030\u0030\u0036"});
HackHax.push({GrandesLigas: "\u0056\u0049\u0054\u004f\u0052\u0052\u0052\u0052\u0052\u0052\u0052\u0052\u0052\u0044\u004f\u004d\u0041\u0055\u004c",GLH2015: "\u0070\u0069\u006e\u0074\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0053\u0074\u0072\u006f\u0079\u0065\u006e\u0073",GLH2015: "\u0034\u0030\u0036\u0031\u0038\u0031\u0034\u0038"});
HackHax.push({GrandesLigas: "\u004b\u0069\u004b\u0069",GLH2015: "\u006b\u0069\u006b\u0069\u006c\u006f\u0063\u006f\u0032\u0032"});
HackHax.push({GrandesLigas: "\u03c1\u0065\u0072\u0079 \u2078 \u007c \u0041\u0044\u0056",GLH2015: "\u0049\u006d\u006f\u0072\u0074\u0061\u006c\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0054\u0048\u0042",GLH2015: "\u0032\u0031\u0034\u0031\u0032\u0031\u0032"});
HackHax.push({GrandesLigas: "\u004d\u0069\u0074\u006f\u0062\u006f\u0074\u006d\u0075\u0063\u0061",GLH2015: "\u0032\u0030\u0030\u0036"});
HackHax.push({GrandesLigas: "\u0063\u006f\u006c\u0069\u0070\u0061\u0074\u006f",GLH2015: "\u006a\u006f\u0061\u0071\u0075\u0069\u006e\u0075\u0064\u0065\u0063\u0068\u0069\u006c\u0065\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0061\u006c\u0062\u006f\u006f\u0073\u0063\u0061\u0072",GLH2015: "\u006f\u0073\u0063\u0061\u0072\u0069\u0074\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0067         \u0067",GLH2015: "\u006d\u0069\u0047\u004c\u0048\u0061\u0078\u0032\u0030\u0031\u0036\u0065\u0073\u0075\u006e\u0068\u0075"});
HackHax.push({GrandesLigas: "\u0050\u0069\u0070\u006f",GLH2015: "\u0051\u0065\u0073\u0061\u0065\u006e\u0064\u0065\u0063\u006c\u0061\u0076\u0065\u0035"});
HackHax.push({GrandesLigas: "\u0066\u0072\u0061\u006e\u007e",GLH2015: "\u0052\u0069\u0076\u0065\u0072\u0070\u006c\u0061\u0074\u0065"});
HackHax.push({GrandesLigas: "\u0493\u1d0f\u0280\u1d07 \u2082\u2084\uff0f\u2087 \u029f\u0280\u1d18",GLH2015: "\u0066\u006f\u0072\u0065\u006c\u0061\u006e\u0075\u0031\u0034\u0037"});
HackHax.push({GrandesLigas: "\u0032\u0034\u0030\u0036\u0035\u0037\u0033\u0034",GLH2015: "\u0032\u0034\u0030\u0036\u0035\u0037\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0041\u0067\u0075\u0073\u0066\u0065\u0072\u0030\u0033",GLH2015: "\u0034\u0035\u0035\u0031\u0038\u0031\u0030\u0036"});
HackHax.push({GrandesLigas: "\u007c\u0044\u0079\u0062\u0061\u006c\u0061\u007c \u0023\u0049\u0030",GLH2015: "\u0072\u0063\u006c\u0061\u006b\u0064\u0031\u0038\u0038\u0039"});
HackHax.push({GrandesLigas: "\u0041\u006c\u0074\u00f8 \u0050\u20ac\u0072\u0072\u00f8 \u221a\u0042\u0056\u0042\u221a \u0037\u0049",GLH2015: "\u0041\u006c\u0074\u006f \u0050\u20ac\u0072\u0072\u006f"});
HackHax.push({GrandesLigas: "\u006c\u0065\u0070\u0072\u006f\u0073\u006f",GLH2015: "\u006c\u0065\u0070\u0072\u006f\u0073\u006f"});
HackHax.push({GrandesLigas: "\u0053\u006f\u006e\u007c\u0023\u0033\u0031\u0e30",GLH2015: "\u004d\u0061\u0072\u0063\u0065\u006c\u0069\u006e\u0068\u006f\u0032\u0030\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0066\u0061\u0069\u0074\u0068",GLH2015: "\u0063\u0061\u0074\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0061\u0073\u0064\u0064\u0064\u0064",GLH2015: "\u0052\u0069\u0076\u0065\u0072\u0070\u006c\u0031\u0039"});
HackHax.push({GrandesLigas: "\u0043\u006f\u0075\u0054\u0069\u0069\u0069\u0069",GLH2015: "\u0072\u0061\u006d\u0069\u0032\u0030\u0030\u0036"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0072\u0063\u0054\u0065\u0072\u0053\u0074\u0065\u0067\u0065\u006e\u0031",GLH2015: "\u0054\u0065\u0072\u0053\u0074\u0065\u0067\u0065\u006e"});
HackHax.push({GrandesLigas: "\u0041\u0072\u0064\u0061 \u0054\u0075\u0072\u0061\u006e",GLH2015: "\u0061\u006c\u0061\u0073\u0061\u0072\u0067\u0065\u006e\u0074\u0069\u006e\u0061\u0073\u0031"});
HackHax.push({GrandesLigas: "\u0062\u0065\u0072\u0075\u0062\u0069",GLH2015: "\u0066\u0061\u0063\u0075\u0032\u0030\u0030\u0036"});
HackHax.push({GrandesLigas: "\u0042\u0045\u0043\u004b \u0042\u0045\u004d \u0042\u004f\u004c\u0041\u0044\u004f",GLH2015: "\u0062\u0065\u006c\u0069\u006e\u0068\u0061\u0030\u0031"});
HackHax.push({GrandesLigas: "\u0052\u0069\u0063\u0063\u0069\u0061\u0072\u0064\u0065\u006c\u006c\u0069 \u0062\u0068\u0074",GLH2015: "\u0072\u0069\u0063\u0061\u0072\u0067\u0065\u006e\u0032"});
HackHax.push({GrandesLigas: "\u004d\u006f\u006c\u0069\u006e\u0061 \u0023\u0031\u0030",GLH2015: "\u0073\u0061\u006e\u0074\u006f\u0073\u0032\u0030\u0031\u0033"});
HackHax.push({GrandesLigas: "\u0044\u0042\u0038",GLH2015: "\u0076\u0031\u0033\u0031\u0076\u0031\u0033\u0031"});
HackHax.push({GrandesLigas: "\u004d\u0065\u0073\u0073\u0049\u004f",GLH2015: "\u0037\u0037\u0037\u0039\u0030\u0030\u0030\u0039"});
HackHax.push({GrandesLigas: "\u006e\u0069\u0063\u006f",GLH2015: "\u0063\u0061\u0063\u0061"});
HackHax.push({GrandesLigas: "\u0048\u006f\u0075\u0073\u0065 \u006f\u0066 \u0042\u0061\u006c\u006c\u006f\u006f\u006e\u0073",GLH2015: "\u0070\u0069\u0072\u006c\u006f\u0035"});
HackHax.push({GrandesLigas: "\u004d\u0065\u0073\u0073\u0069 \u0044\u0061 \u0042\u0065\u0073\u0074",GLH2015: "\u0046\u0043\u0042\u0032\u0030\u0031\u0033"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0074\u0074",GLH2015: "\u0042\u0072\u0069\u0061\u006e\u0036\u0031\u0032\u0030\u0032"});
HackHax.push({GrandesLigas: "\u004c\u0068\u006d\u0061\u007a\u007a\u0069",GLH2015: "\u006d\u006f\u0074\u006f\u0072\u006f\u006c\u0061\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0041\u006e\u0074\u0068\u006f\u006e\u0079   \u00ae    \u0035\u0042",GLH2015: "\u0033\u0030\u0037\u0033\u0035\u0031\u0035\u0035"});
HackHax.push({GrandesLigas: "\u0043\u006f\u0072\u006c\u0065\u006f\u006e\u0065",GLH2015: "\u006c\u0061\u0073\u0074\u006f\u006e\u0069\u006e\u0061\u0073"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0062\u0069\u0053\u0045\u004d\u0067\u006f\u006c",GLH2015: "\u004d\u0069\u006e\u006f\u0074\u0061\u0075\u0072\u006f\u0032\u0031"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0074\u0068\u0065\u0075\u0068\u0073\u0078",GLH2015: "\u0031\u0034\u0037\u0032\u0035\u0038\u0033\u0036\u0039\u006d"});
HackHax.push({GrandesLigas: "\u0046\u0065\u0064\u0065 \u0056\u0061\u006c\u0076\u0065\u0072\u0064\u0065",GLH2015: "\u0070\u0061\u006a\u0061\u0072\u0069\u0074\u006f\u0076\u0061\u006c\u0076\u0065\u0072\u0064\u0065"});
HackHax.push({GrandesLigas: "\u004e\u004d \u002d \u0043\u0065\u0072\u0075\u0074\u0074\u0069",GLH2015: "\u0072\u0069\u0076\u0065\u0072\u0070\u006c\u0061\u0074\u0065\u0031\u0030"});
HackHax.push({GrandesLigas: " \u0039\u0030\u0073 \u0048\u0049\u0050 \u0048\u004f\u0050",GLH2015: "\u0070\u0065\u0064\u0072\u0069\u0074\u006f"});
HackHax.push({GrandesLigas: "\u0041\u006c\u006d\u0061\u0064\u0061\u002e \u273f",GLH2015: "\u0062\u0075\u0066\u0066\u0061\u0063\u0063"});
HackHax.push({GrandesLigas: "\u0043\u002e \u0050\u0061\u0076\u00f3\u006e",GLH2015: "\u0063\u0061\u0063\u0061\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0158\u00d8\u0147\u0394\u0141\u0110\u0197\u0147\u0126\u00d8 \ud835\udfcf\ud835\udff6",GLH2015: "\u0068\u006f\u006c\u0061\u0071\u0075\u0065\u0068\u0061\u0063\u0065"});
HackHax.push({GrandesLigas: "\u0050\u0069\u0063\u0068\u0069",GLH2015: "\u0062\u0061\u0074\u0065\u006c\u0066\u0069\u006c\u0034"});
HackHax.push({GrandesLigas: "\u0065\u006d\u0070\u0061\u006e\u0061\u0064\u0069\u0074\u0061",GLH2015: "\u006d\u0065\u0064\u0061\u006c\u006c\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: " \u0493\u026a\u029f\u029c\u1d0f \u1d05\u1d07 \u1d05\u1d07\u1d1c\u0073 \u2729 \u0043\u004e\u0052",GLH2015: "\u0064\u0061\u006e\u0069\u0065\u006c\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0073\u0070\u006f\u006f\u0074\u0063\u0078",GLH2015: "\u006d\u006f\u0073\u0074\u0072\u006f\u0036\u0034"});
HackHax.push({GrandesLigas: "\u004a\u0065\u0073\u00fa\u0073 \u0074\u0065 \u0061\u006d\u0061 \u271d\ud83d\udc96",GLH2015: "\u0072\u0065\u0079\u0064\u0065\u0063\u006f\u0070\u0061\u0073\u0075\u006e\u006f\u0073\u006f\u006c\u006f"});
HackHax.push({GrandesLigas: "\u0046\u002e \u0064\u0065 \u004a\u006f\u006e\u0067",GLH2015: "\u0032\u0033\u0064\u0069\u0063\u0069\u0065\u006d\u0062\u0072\u0065"});
HackHax.push({GrandesLigas: "\u2c63\u039b\u1e46\u0110\u1e52\u1e5c\u2c63\u039b",GLH2015: "\u0065\u0064\u0075\u0075\u0067\u0061\u0062\u0069\u0069"});
HackHax.push({GrandesLigas: "\u004e\u0065\u0077 \u0041\u0072\u006d\u0061\u0067\u0065\u0064\u006f\u006e",GLH2015: "\u0031\u0030\u0031\u0030\u0032\u0030\u0030\u0037"});
HackHax.push({GrandesLigas: "\u0037\u0070\u006f",GLH2015: "\u006d\u0061\u0074\u0068"});
HackHax.push({GrandesLigas: "\u002d\u002d\u002d\u005f\u005f\u005f\u002d\u002d\u002d",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0035"});
HackHax.push({GrandesLigas: "\u0046\u0065\u006e\u0072\u0069\u0073",GLH2015: "\u0048\u0075\u0072\u0061\u0063\u0061\u006e\u0032\u0033\u0031\u0038"});
HackHax.push({GrandesLigas: "\u0076\u0065\u0072\u0063\u0069\u006e\u0067\u00e9\u0074\u006f\u0072\u0069\u0078",GLH2015: "\u0063\u0061\u006c\u0076\u0065\u006e\u0074\u0065\u0039\u0036"});
HackHax.push({GrandesLigas: "\u0049\u006e\u0066\u006c\u0075\u0065\u006e\u007a\u0061\u2122",GLH2015: "\u0032\u0034\u0030\u0031"});
HackHax.push({GrandesLigas: "\u002e\u003a\u0051\u0055\u0045\u0053\u0054\u0045\u0052\u0033\u003a\u002e",GLH2015: "\u006a\u0061\u0076\u0069\u0065\u0072\u006f\u006d\u0061\u0072\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0056\u0061\u006e \u0044\u0069\u006a\u006b",GLH2015: "\u0073\u0065\u0062\u0061\u0076\u0061\u0032\u0032"});
HackHax.push({GrandesLigas: "\u0061\u006e\u006f\u006e",GLH2015: "\u007a\u0065\u0072\u006f\u006e\u0069\u006e\u0065"});
HackHax.push({GrandesLigas: "\u0043\u0061\u0076\u0061\u006c\u006f",GLH2015: "\u006f\u006c\u0061\u0076\u0061\u0063"});
HackHax.push({GrandesLigas: "\u0057\u0061\u006c\u0064\u0065\u0061\u006c\u0067\u006f",GLH2015: "\u0069\u0064\u0065\u006e\u0074\u0069\u0064\u0061\u0064"});
HackHax.push({GrandesLigas: "\u003a\u0029",GLH2015: "\u004a\u0069\u006a\u0061\u0064\u006f\u0072"});
HackHax.push({GrandesLigas: "\u0054\u0068\u0065\u004d\u0061\u006c\u0064\u0069\u0074\u0061",GLH2015: "\u006c\u006f\u006c\u0069\u0074\u0061\u0035\u0035\u0035\u0035"});
HackHax.push({GrandesLigas: "\u0021\u002d\u004c\u0075\u0063\u0068\u006f\u002d\u0021",GLH2015: "\u006c\u0075\u0069\u0073\u0072\u0069\u006f\u0073\u0065\u0063\u006f"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0067\u006f \u006d\u0061\u006c\u0064\u0069\u0076\u0069\u0061",GLH2015: "\u0063\u0068\u0065\u006c\u0069\u0074\u006f\u0065\u006e\u0062\u0075\u006c\u006c\u0061"});
HackHax.push({GrandesLigas: "\u004b\u006f\u006b\u0061\u004b\u006f\u006c\u0061",GLH2015: "\u0032\u0033\u0034\u0035\u0034\u0035"});
HackHax.push({GrandesLigas: "\u0062\u0069\u0072\u0075\u003c\u0033",GLH2015: "\u006c\u0069\u0063\u006f\u006c\u0069\u006e\u0069\u0031"});
HackHax.push({GrandesLigas: "\u0051\u0075\u0069\u006e\u0074\u0065\u0072\u006f",GLH2015: "\u0041\u0072\u0069\u006d\u0061\u006d\u0075\u0079\u0071\u0075\u0065\u0072\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0041\u002e \u0055\u0073\u0075\u0072\u0069\u0061\u0067\u0061",GLH2015: "\u004c\u006f\u0063\u006f\u0073\u0039\u0039"});
HackHax.push({GrandesLigas: "\u0070\u006f\u0079\u006f",GLH2015: "\u0064\u0061\u0073\u0065\u0067\u0075\u0072\u0061\u0039\u0035"});
HackHax.push({GrandesLigas: "\u0042\u0041\u0052\u0042\u0041 \u0052\u0045\u0054\u0049\u0052\u0041\u0044\u0041",GLH2015: "\u0065\u006c\u006d\u006f\u006e\u006f\u006d\u0061\u0072\u0069\u006f"});
HackHax.push({GrandesLigas: "\u0061\u006b",GLH2015: "\u0070\u0061\u0071\u0075\u0065\u006c\u0061\u0071\u0075\u0065\u0072\u0069"});
HackHax.push({GrandesLigas: "\u0070\u0069\u0063\u006f\u006c\u0069\u006e\u0068\u006f",GLH2015: "\u0070\u0069\u0063\u006f\u0070\u0061\u0072\u0061\u006f\u0039\u0038\u0037\u0037"});
HackHax.push({GrandesLigas: "\u004c\u0065\u0061\u006e\u0048",GLH2015: "\u0044\u0065\u006e\u0061\u0073\u0063\u0061\u0072\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0048\u0075\u0067\u006f \u0042\u006f\u0073\u0073 \u00ae",GLH2015: "\u0061\u0062\u0063\u0064\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0064\u0065\u006d\u006f\u006e\u0069\u0063\u0073\u0075",GLH2015: "\u0061\u007a\u0075\u006c\u0069\u0074\u006f\u0032\u0033\u0031"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0073 \u006d\u0061\u006c\u006f \u0071\u0075\u0065 \u0068\u0069\u0067\u0075\u0061\u0069\u006e",GLH2015: "\u004a\u006f\u0065\u006c\u0061\u0072\u0069\u0065\u006c\u0070\u0061\u005a"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0072\u0071\u0075\u0069\u0074\u006f\u0073",GLH2015: "\u0063\u0070\u0075\u0031\u0035\u0033\u0037"});
HackHax.push({GrandesLigas: "\u0044\u0065\u006d\u0070\u0073\u0065\u0079",GLH2015: "\u0062\u006f\u0063\u0061\u0063\u0061\u006d\u0070\u0065\u006f\u006e\u0039\u0039\u0039"});
HackHax.push({GrandesLigas: "\u004f\u0073\u006f \u0054\u0054\u0056",GLH2015: "\u0074\u0061\u0074\u0061\u006e\u0033\u0039\u0032"});
HackHax.push({GrandesLigas: "\u0054\u004f\u0054\u0054\u0049\u004d\u0049\u0054\u004f",GLH2015: "\u0031\u0039\u0030\u0034\u0032\u0030\u0030\u0036"});
HackHax.push({GrandesLigas: "\u004c\u0075\u0069\u0064\u006a\u0079",GLH2015: "\u0076\u0061\u0073\u0063\u006f\u0064\u0061\u0067\u0061\u006d\u0061"});
HackHax.push({GrandesLigas: "\u004c\u0075\u0069\u0064\u006a\u0079",GLH2015: "\u006c\u0075\u0069\u0064\u006a\u0079\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0048\u0047 \u002d \u004d\u0065\u0073\u0073\u0069",GLH2015: "\u0065\u006c\u0063\u0068\u006f\u0072\u0069\u007a\u006f\u0035"});
HackHax.push({GrandesLigas: "\u004a\u006f\u00e3\u006f \u0046\u00e9\u006c\u0069\u0078",GLH2015: "\u0061\u006c\u0061\u0073\u0061\u0072\u0067\u0065\u006e\u0074\u0069\u006e\u0061\u0073\u0039\u0039"});
HackHax.push({GrandesLigas: "\u0059\u0075\u0079\u0061 \u004f\u0073\u0061\u006b\u006f",GLH2015: "\u0031\u0038\u0030\u0038"});
HackHax.push({GrandesLigas: "\u0454\u006c \u03c1\u0454\u0442\u0069\u0e23\u03c3 \ud835\udfd9\ud835\udfd8 \ud835\udd38\ud835\udd63\ud835\udd58",GLH2015: "\u0041\u0072\u0063\u0065\u004d\u0061\u0074\u0065\u006f"});
HackHax.push({GrandesLigas: "\u0053\u0069\u0072\u0042\u0075\u0073\u0071\u0075\u0065\u0074\u0073\u0035",GLH2015: "\u0034\u0034\u0030\u0030\u0033\u0035\u0034\u0035\u004d\u0061\u0072\u0063\u006f\u0073"});
HackHax.push({GrandesLigas: "\u0074\u006f\u0072\u0061\u006e\u007a\u006f",GLH2015: "\u0061\u0067\u0075\u0061\u006e\u0074\u0065\u0068\u0075\u0072\u0061\u0063\u0061\u006e\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0056\u0061\u006c\u0064\u0065\u0069\u0072 \u0064\u0061 \u0031\u0030",GLH2015: "\u0061\u0064\u0073\u0063\u0031\u0039\u0038\u0039"});
HackHax.push({GrandesLigas: "\u006b\u006c\u006f\u0073\u0065",GLH2015: "\u006c\u006f\u0073\u0064\u0065\u0061\u0062\u0061\u006a\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0041\u002e \u0044\u0075\u0072\u0061\u006e\u0074",GLH2015: "\u0062\u006f\u0063\u0061\u006a\u0075\u006e\u0069\u006f\u0072\u0073"});
HackHax.push({GrandesLigas: "\u0050\u006a\u0061\u006e\u0069\u0063",GLH2015: "\u0072\u0069\u0071\u0075\u0065\u006c\u006d\u0065"});
HackHax.push({GrandesLigas: "\u0050\u006a\u0061\u006e\u0069\u0063",GLH2015: "\u0072\u006f\u006d\u0061\u006e\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0042\u0065\u0062\u0065\u006c\u006f\u0039\u0039",GLH2015: "\u0073\u0074\u0072\u0061\u0074\u006f\u0063\u0061\u0073\u0074\u0065\u0072"});
HackHax.push({GrandesLigas: "\u004f\u004f\u0046",GLH2015: "\u0061\u0067\u006f\u0073\u0074\u0069\u006e\u0061\u0031\u0034"});
HackHax.push({GrandesLigas: "\u0077\u0065\u006c\u006d\u0061\u0073\u0069\u0074\u0061\u003b\u003b",GLH2015: "\u0042\u0065\u0061\u0073\u0073"});
HackHax.push({GrandesLigas: "\u0047\u0070\u0052\u006f",GLH2015: "\u0074\u006f\u0062\u0069\u0061\u0073\u0079\u0065"});
HackHax.push({GrandesLigas: "\u004e\u0061\u0063\u0069\u006f\u006e\u0061\u006c \u0065\u006c \u006d\u0061\u0073 \u0067\u0072\u0061\u006e\u0064\u0065",GLH2015: "\u0061\u006c\u0075\u006b\u0069\u0069\u0069\u0069\u0069"});
HackHax.push({GrandesLigas: "\u0042\u0069\u006c\u0061\u0072\u0064\u0069\u0073\u0074\u0061 \u0064\u0065 \u0042\u0069\u006c\u0061\u0072\u0064\u006f",GLH2015: "\u0072\u0069\u0076\u0065\u0072\u0070\u006c\u0061\u0074\u0065\u0031"});
HackHax.push({GrandesLigas: "\u0050\u0061\u0076\u0061\u0072\u0064 \u2606",GLH2015: "\u006c\u0061\u0075\u0074\u0061\u0072\u006f"});
HackHax.push({GrandesLigas: "\u0047\u0049\u004e\u004f",GLH2015: "\u0062\u0075\u0067\u0065\u0073\u0070\u0072\u0069\u0076\u0069"});
HackHax.push({GrandesLigas: "\u0074\u0075\u0062\u006f",GLH2015: "\u0062\u0061\u0074\u0061\u0074\u0069\u006e\u0068\u0061\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0043\u004c\u004f\u0056\u0045\u0052",GLH2015: "\u0072\u0069\u0076\u0065\u0072\u005f\u0032\u0030\u0031\u0033"});
HackHax.push({GrandesLigas: "\ud835\udddd\ud835\udc0d\u026a\u0063\u0454\u029f\u029f\u026a",GLH2015: "\u0065\u006c\u006c\u006f\u0063\u006f\u0032\u0030\u0030\u0031"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0072\u0063\u006f\u0073 \u0023\u0031\u0030",GLH2015: "\u0052\u0046\u004c\u0048\u004c\u0038\u0036\u0035"});
HackHax.push({GrandesLigas: "\u004c\u0075\u0063\u0061\u0073 \u0046\u0069\u0065\u006c",GLH2015: "\u0030\u0032\u0030\u0033\u006c\u0075\u0063\u0061\u0073"});
HackHax.push({GrandesLigas: "\u0053\u0065\u00f1\u006f\u0072 \u0058",GLH2015: "\u006c\u0033\u0033\u0074\u0073\u0075\u0070\u0061\u0068\u0034\u0078\u0030\u0072"});
HackHax.push({GrandesLigas: "\u0049\u0053\u0047 \u00b0 \u0049\u0041\u004e",GLH2015: "\u0032\u0036\u006a\u0075\u006c\u0069\u006f\u0032\u0030\u0030\u0032"});
HackHax.push({GrandesLigas: "\u0073\u0061\u0063 \u0069\u0073\u0063\u006f",GLH2015: "\u006a\u0072\u0072\u0032\u0030\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0065\u0073\u0031",GLH2015: "\u0064\u0061\u0073\u0065\u0067\u0075\u0072\u0061\u0039\u0035"});
HackHax.push({GrandesLigas: "\u004a\u006f\u0068\u006e \u0046\u0072\u0075\u0073\u0063\u0069\u0061\u006e\u0074\u0065",GLH2015: "\u0072\u0069\u0076\u0065\u0072\u0074\u0065\u0061\u006d\u006f"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0062\u0079 \u0023\u0035",GLH2015: "\u0067\u0061\u0074\u0075\u0072\u0072\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0050\u0061\u0076\u006f\u006e\u0063\u0069\u006e\u0068\u006f",GLH2015: "\u0061\u0067\u0075\u0073\u0032\u0030\u0030\u0038"});
HackHax.push({GrandesLigas: "\u0056\u006f\u006c\u0061\u006e\u0074\u0065 \u004d\u0061\u0072\u0072\u0065\u006e\u0074\u006f",GLH2015: "\u0044\u0061\u006e\u0039\u0039\u0031\u0036\u0035\u0039\u0031\u0030\u0035\u0069\u0065\u006c"});
HackHax.push({GrandesLigas: "\u006b\u0069\u006e\u0064\u0065\u0072 \u0041\u004c\u004b",GLH2015: "\u0074\u0061\u006c\u006c\u0065\u0072\u0065\u0073"});
HackHax.push({GrandesLigas: "\ud835\udce1\ud835\udcee\ud835\udcf5\ud835\udcea\ud835\udcfd\ud835\udcf8\ud835\udcfb",GLH2015: "\u0071\u0071\u0071\u0077\u0077\u0077\u0065\u0065"});
HackHax.push({GrandesLigas: "\u0070\u006f\u0062\u006c\u0061",GLH2015: "\u0070\u006f\u0072\u006f\u0074\u006f\u0073\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0048\u0075\u006e\u0074\u0065",GLH2015: "\u0062\u006f\u0063\u0061\u006a\u0075\u006e\u0069\u006f\u0072\u0073\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0063\u0072\u0075\u0079\u0066\u0066",GLH2015: "\u006d\u0061\u0074\u0069\u0061\u0073\u0073\u0032\u0030\u0031\u0034"});
HackHax.push({GrandesLigas: "\u0070\u0069\u0070\u0061 \u002d\u0074\u0046",GLH2015: "\u0070\u0061\u0074\u0065\u0074\u0061"});
HackHax.push({GrandesLigas: "\u0052\u0075\u0073\u0068",GLH2015: "\u0046\u0065\u0072\u006e\u0061\u006e\u0064\u006f\u0074\u006f\u006c\u0075\u006e\u0061\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0041\u0064\u0061\u0069\u006c\u0073\u006f\u006e",GLH2015: "\u0034\u0030\u0034\u0030\u0072\u0065\u0069"});
HackHax.push({GrandesLigas: "\u0046\u006c\u03c3\u0079\u0064 \u2729 \u002d\u004c\u03c3\u03c1\u03b1\u0064\u0072\u0065",GLH2015: "\u006d\u0061\u0078\u0069\u006d\u0075\u0073"});
HackHax.push({GrandesLigas: "\u005a\u0075\u006b\u006f",GLH2015: "\u006d\u0061\u0074\u0069\u0032\u0037\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0073\u006f\u006c\u0064\u0061\u006e\u006f \u0064\u0065 \u0038 \u0073\u0069\u006c\u0065\u006e\u0063\u0065",GLH2015: "\u006c\u0061\u0075\u0074\u0061\u0072\u006f\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0044\u0072\u006f\u006e\u0065",GLH2015: "\u0070\u0069\u0063\u0061\u0064\u006f"});
HackHax.push({GrandesLigas: "\u0044\u0061\u006c\u0065\u0078",GLH2015: "\u0044\u0061\u006c\u0065\u0078\u0078"});
HackHax.push({GrandesLigas: "\u0063\u0065\u006e\u0074\u0075",GLH2015: "\u0068\u0061\u0078\u0062\u0061\u006c\u006c\u0032\u0030\u0031\u0035"});
HackHax.push({GrandesLigas: "\u006d\u0061\u006c\u0064\u0069\u006e\u0069",GLH2015: "\u0062\u0075\u0066\u0066\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0065\u006c\u0070\u0061\u0070\u0069\u0072\u0069\u006b\u006f\u0068\u0068",GLH2015: "\u0063\u0075\u0061\u0064\u0072\u006f\u0033\u0030\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0070\u006c\u0061\u0079\u0061\u006c\u0061\u0067\u006f",GLH2015: "\u0068\u0078\u0062\u006c\u006c\u0040\u0038\u0036"});
HackHax.push({GrandesLigas: "\u0053\u0061\u006e\u0074\u0061 \u004b\u0072\u006f\u006f\u0073",GLH2015: "\u004e\u0069\u0072\u0076\u0061\u006e\u0061\u0031\u0035"});
HackHax.push({GrandesLigas: "\u0050\u006c\u0061\u0079\u0061\u006c\u0061\u0067\u006f",GLH2015: "\u0039\u0039\u0035\u0036\u0036\u0033\u0033\u0037\u0032\u0032\u0038\u0038"});
HackHax.push({GrandesLigas: "\u0404\u3057\u005f\u15f0\u0404\u054f\u054f\u00ed\u15cb\u054f",GLH2015: "\u0062\u006f\u0063\u0061\u0032\u0037\u0074\u0069\u0074\u0075\u006c\u006f\u0073\u0040"});
HackHax.push({GrandesLigas: "\ud835\udce1\ud835\udcee\ud835\udcf5\ud835\udcea\ud835\udcfd\ud835\udcf8\ud835\udcfb",GLH2015: "\u0078\u0064\u006c\u006f\u006c\u0064\u0064"});
HackHax.push({GrandesLigas: "\u0052\u0045\u004c\u0041\u004d\u0050\u0041\u0047\u004f",GLH2015: "\u0034\u0033\u0035\u0033\u0032\u0034\u0035"});
HackHax.push({GrandesLigas: "\u0280\u1d0d\u007c\u26a1\u26a1\u0158\u20ac\u0141\u0394\u039c\u01a4\u0394\u01e4\u00d8\u26a1\u26a1\u007c\u004d\u0045\u004e\u0047\u0041\u004f",GLH2015: "\u0052\u0045\u004c\u0041\u004d\u0050\u0041\u0047\u004f\u0031\u0032\u0033\u0035\u0034\u0033\u0035\u0036\u0036\u0034\u0036\u0035"});
HackHax.push({GrandesLigas: "\u004a\u0061\u0068\u0065\u0065\u0064",GLH2015: "\u0033\u0039\u0036\u0035\u0032\u0030\u0030\u0031\u0074"});
HackHax.push({GrandesLigas: "\u0041\u0073\u0061 \u004e\u006f\u0074\u0075\u0072\u006e\u0061",GLH2015: "\u0061\u0073\u0061\u006e\u006f\u0074\u0075\u0072\u006e\u0061\u0031\u0032\u0033\u0034\u0035\u0036"});
HackHax.push({GrandesLigas: "\u0043\u0069\u0065\u0067\u006f",GLH2015: "\u0063\u0069\u0065\u0067\u006f"});
HackHax.push({GrandesLigas: "\u0070\u0061\u0074\u0061\u0063\u006f\u006e",GLH2015: "\u004d\u0061\u0064\u0065\u0072\u0061\u0031"});
HackHax.push({GrandesLigas: "\u0054\u002e \u0041\u0073\u0061\u006e\u006f",GLH2015: "\u006a\u0061\u0070\u006f\u006e"});
HackHax.push({GrandesLigas: "\u00c9\u0072\u0069\u006b\u0061 \u0023\u0039\u0039\u0e30",GLH2015: "\u004d\u0061\u0072\u0063\u0065\u006c\u0069\u006e\u0068\u006f\u0032\u0030\u0030\u0030"});
HackHax.push({GrandesLigas: "\u004c\u0043\u0044\u0054\u004d",GLH2015: "\u006e\u006f\u0063\u0068\u0069\u0068\u006f\u0074\u0039\u0035"});
HackHax.push({GrandesLigas: "\u0069\u0061\u0438",GLH2015: "\u0069\u0061\u006e\u0038\u0030\u0030\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0043\u0072\u0069\u006e\u0067\u0065",GLH2015: "\u0076\u006f\u006b\u0061\u006d\u006f\u0072\u0069\u0073\u0074\u0065\u0065\u006e\u006d\u0061\u0064\u0072\u0069\u0064"});
HackHax.push({GrandesLigas: "\ud835\ude1d\ud835\ude22\ud835\ude2f \ud835\ude17\ud835\ude26\ud835\ude33\ud835\ude34\ud835\ude2a\ud835\ude26",GLH2015: "\u0043\u0068\u0069\u0071\u0075\u0069\u0074\u006f\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0043\u0072\u0069\u0073\u0074\u0069\u0061\u006e\u006f \u0052\u006f\u006e\u0061\u006c\u0064\u006f",GLH2015: "\u006b\u0061\u0069\u006f\u0031\u0032\u0035"});
HackHax.push({GrandesLigas: "\u0041\u0064\u006f\u006c\u0066\u006f \u0047\u0061\u0069\u0063\u0068",GLH2015: "\u0072\u006f\u006a\u006f\u006d\u0061\u006e\u0064\u0061"});
HackHax.push({GrandesLigas: "\u0042\u0061\u0073\u0065\u0062\u0061\u006c\u006c\u0046\u0075\u0072\u0069\u0065\u0073",GLH2015: "\u0063\u0061\u006c\u0061\u006d\u0061\u0072\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0056\u0061\u006e \u0064\u0065 \u0042\u0065\u0065\u006b",GLH2015: "\u0061\u006a\u0061\u0078"});
HackHax.push({GrandesLigas: "\u004c\u002e \u004d\u0061\u0072\u0074\u0069\u006e\u0065\u007a",GLH2015: "\u0072\u0061\u0063\u0069\u006e\u0067\u0032\u0030\u0031\u0034"});
HackHax.push({GrandesLigas: "\u0044\u0065\u0077",GLH2015: "\u0064\u0075\u0072\u0061\u007a\u006e\u006f\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0063\u0061\u007a\u0061\u0064\u006f\u0072",GLH2015: "\u006d\u0069\u0063\u006b\u006a\u0061\u0067\u0067\u0065\u0072\u0039\u0037\u006f\u006b"});
HackHax.push({GrandesLigas: "\u0050\u0049\u0050\u0045",GLH2015: "\u0070\u0069\u0070\u0065\u0031\u0032"});
HackHax.push({GrandesLigas: "\ua731\u1d00\u1d04 \u2606 \ua730\u1d0f\u0280\u1d07 \u00b2\u2074\u002f\u2077 \ud83d\udc3a",GLH2015: "\u0063\u006f\u006e\u0074\u0072\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u006b\u0061\u00f1\u006f\u006e",GLH2015: "\u006b\u0061\u00f1\u006f\u006e\u0031\u0032\u0033\u0071"});
HackHax.push({GrandesLigas: "\u0070\u006f\u0062\u006c\u0065\u0074\u0065",GLH2015: "\u0073\u0061\u006e\u006c\u006f\u0072\u0065\u006e\u007a\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0046\u0065\u0064\u0065\u0072\u0069\u0063\u006f",GLH2015: "\u0063\u0061\u0063\u0061\u0031\u0035\u0039\u0038\u0037\u0034\u0036\u0033\u0032"});
HackHax.push({GrandesLigas: "\u0045\u0074\u006f\u0045\u0054\u0072\u0061\u0073\u0068\u004c\u006f\u0054\u0075\u0079\u006f\u0045\u0042\u0061\u0073\u0075\u0072\u0061",GLH2015: "\u0068\u006f\u006c\u0061"});
HackHax.push({GrandesLigas: "\u0074\u0069\u0074\u0061\u006d\u0061\u0072",GLH2015: "\u0074\u0069\u0074\u0061\u006d\u0061\u0072"});
HackHax.push({GrandesLigas: "\u0053\u0061\u006e\u0074\u0061 \u004b\u0072\u006f\u006f\u0073",GLH2015: "\u0031\u0039\u0039\u0036"});
HackHax.push({GrandesLigas: "\u0053\u0061\u006e\u0074\u0061 \u004b\u0072\u006f\u006f\u0073",GLH2015: "\u0031\u0036\u0031\u0030\u0039\u0036"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0075\u0078\u006f\u004a\u0065\u0061\u006e\u0023\u0033\u0030\u0050\u0052\u0041\u0055\u004d",GLH2015: "\u0067\u0072\u0065\u006d\u0069\u006f\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0053\u004e\u0030\u0057",GLH2015: "\u0066\u0061\u0063\u0075\u006e\u0064\u006f\u0071\u0075\u0061\u0067\u006c\u0069\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004d\u0065\u0072\u0069\u0063\u0072\u0069\u0073\u006d\u0061\u0048",GLH2015: "\u0068\u0075\u007a\u0065\u0072\u0031"});
HackHax.push({GrandesLigas: "\u0053\u0068\u0065\u0063\u006b\u0061\u0061",GLH2015: "\u0073\u006f\u0079\u0065\u006c\u0075\u006e\u006f"});
HackHax.push({GrandesLigas: "\u007a\u0061\u0070\u0061\u0074\u006f",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0036"});
HackHax.push({GrandesLigas: "\u0064\u0065\u0072\u0073\u0075",GLH2015: "\u0073\u0065\u0072\u0076\u0034\u0033\u0032\u0031"});
HackHax.push({GrandesLigas: "\u0044\u0065\u006c \u0050\u0069\u0065\u0072\u006f \u003b",GLH2015: "\u0070\u0069\u0063\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0059\u0065\u0073",GLH2015: "\u0036\u0039\u0036\u0039"});
HackHax.push({GrandesLigas: "\u006b\u0075\u006e",GLH2015: "\u0042\u006f\u0063\u0061\u0063\u0061\u006d\u0070\u0065\u006f\u006e\u0031\u0036"});
HackHax.push({GrandesLigas: "\u0045\u006c \u0046\u006c\u0061\u0063\u006f",GLH2015: "\u0068\u0075\u006e\u0074\u0065\u0062\u006f\u0062\u006f"});
HackHax.push({GrandesLigas: "\u0054\u007a\u0061\u006f",GLH2015: "\u0037\u0038\u0039\u0034"});
HackHax.push({GrandesLigas: "\u004b\u0041\u0052\u004c\u0049\u0054\u004f\u0053",GLH2015: "\u0062\u0075\u0066\u0061\u006e\u0064\u0061\u0032\u0030\u0030\u0037"});
HackHax.push({GrandesLigas: "\u0065\u0072\u0061 \u0069\u0073\u0074\u0065\u0066\u0069",GLH2015: "\u0079\u006f\u0066\u0065\u0072\u006c\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0053\u0078\u0065\u0074\u0065\u0072",GLH2015: "\u0030\u0038\u0030\u0034\u006b\u0061\u006b\u0061"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0062\u0069\u0047\u0030\u004c",GLH2015: "\u0066\u0072\u0061\u006e\u0063\u006f\u0031\u0030"});
HackHax.push({GrandesLigas: "\u006b\u0069\u0064 \u0063\u0075\u0064\u0069",GLH2015: "\u006e\u0069\u006b\u006f\u0063\u0068\u0061\u0076\u0065\u0073\u0032\u0030\u0031\u0031"});
HackHax.push({GrandesLigas: "\u006e\u0069\u0063\u006f\u0063\u0075\u0064\u0069",GLH2015: "\u0074\u006f\u0064\u006f\u0032\u0030\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0043\u0061\u0072\u0065\u0074\u0061\u0073",GLH2015: "\u0076\u0065\u0072\u0064\u0065\u0076\u0065\u0072\u0064\u0065"});
HackHax.push({GrandesLigas: "\u0053\u0031\u006d\u0070\u006c\u0065",GLH2015: "\u006a\u0075\u006c\u0069\u0074\u006f\u0064\u006f\u006d\u0069\u006e\u0067\u0075\u0065\u007a\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0049\u004c\u004c \u0054\u004f\u004d\u0049\u0043",GLH2015: "\u0063\u006f\u006e\u0074\u0072\u0061\u0073\u0065\u00f1\u0061\u0031\u0037"});
HackHax.push({GrandesLigas: "\u004c\u0065\u006f",GLH2015: "\u006c\u0075\u0067\u0061\u006e\u006f\u0031\u0079\u0032"});
HackHax.push({GrandesLigas: "\u0059\u0075\u0073\u006f\u0076",GLH2015: "\u0063\u0061\u006e\u0061\u006c\u006c\u0061\u0072\u0063\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0042\u0055\u0052\u0052\u0055\u0043\u0048\u0041\u0047\u0041",GLH2015: "\u0033\u0031\u0031\u0030\u0030\u0034"});
HackHax.push({GrandesLigas: "\u0069\u006e\u0073\u0074\u0061",GLH2015: "\u0070\u0069\u006e\u0074\u006f\u0070\u0065\u0071\u0075\u0065\u006e\u006f"});
HackHax.push({GrandesLigas: "\u014a\u0407\u00c7\u041a\u0418\u1eaa\u039c\u0116\u002f\u002f\ud835\udc08\ud835\udc1d\ud835\udc0c\u002f\u002f",GLH2015: "\u0069\u0076\u0061\u006e\u0063\u0068\u006f\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0038\u0039"});
HackHax.push({GrandesLigas: "\u004a\u0065\u0066\u006f\u006c\u0061",GLH2015: "\u0067\u006f\u0064\u0030\u0031\u0031\u0030\u0032\u0030\u0030\u0033"});
HackHax.push({GrandesLigas: "\u0043\u0075\u006c\u006f",GLH2015: "\u0071\u0071\u0061\u0061\u007a\u007a"});
HackHax.push({GrandesLigas: "\u006b\u0061\u0079\u006b\u00e3\u006f",GLH2015: "\u0030\u0038\u0030\u0034\u006b\u0061\u0079\u006b\u0061\u006f"});
HackHax.push({GrandesLigas: "\ud83d\udc8e\ud835\udc71\ud835\udc90\ud835\udc97\ud835\udc86\ud835\udc8f\ud835\udc74\ud835\udc82\ud835\udc8f\ud835\udc90\ud835\udc94\ud83d\udc8e",GLH2015: "\u0045\u0064\u0067\u0061\u0072\u0031\u0031\u0035\u0037\u0039\u0037\u0030\u0039\u0037\u0034"});
HackHax.push({GrandesLigas: "\u0043\u0053 \u0041\u006c\u0066\u0072\u0065\u0064\u006f\u0044\u0069\u0073\u0074\u0065\u0066\u0061\u006e\u006f",GLH2015: "\u0030\u0033\u0030\u0033\u0034\u0035\u0036\u0061"});
HackHax.push({GrandesLigas: "\u0052\u0061\u004d\u0069\u0041\u0072\u0047",GLH2015: "\u0061\u0076\u0069\u006f\u006e\u0065\u0073\u0031"});
HackHax.push({GrandesLigas: "\u0041\u0050\u0052  \u006c\u00e9\u0077\u0061\u006e",GLH2015: "\u006c\u0061\u0075\u0074\u0061\u0072\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0044\u0061\u0076\u0069\u007a\u0069\u006e\u0068\u006f\u0030",GLH2015: "\u006d\u0061\u006d\u0061\u0065\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u006c\u0065\u0077\u0061\u006e",GLH2015: "\u0073\u0068\u0061\u0072\u006b\u0073"});
HackHax.push({GrandesLigas: "\u004c\u0069\u006d\u0041",GLH2015: "\u0032\u0033\u0030\u0035"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0072\u0063\u006f\u0070\u006f\u006c\u006f",GLH2015: "\u0074\u0069\u006d\u0061\u006f\u0065\u006f\u0030"});
HackHax.push({GrandesLigas: "\u0066\u0062\u0065\u0072\u006e\u0061\u0072\u0064\u0065\u0073\u0063\u0068\u0069",GLH2015: "\u0064\u006f\u0077\u006e"});
HackHax.push({GrandesLigas: "\u006d\u0065\u0072\u0076\u0069\u0073",GLH2015: "\u0066\u0061\u0063\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0043\u0076\u0069\u0074\u0061\u006e\u0069\u0063\u0068",GLH2015: "\u0063\u0076\u0069\u0074\u0061\u006e\u0069\u0063\u0068"});
HackHax.push({GrandesLigas: "\u0052\u006f\u006d\u0061\u0072\u0069\u006f",GLH2015: "\u0068\u0061\u0078\u0062\u0061\u006c\u006c\u0031"});
HackHax.push({GrandesLigas: "\u004c\u004e\u0043 \u004c\u0075\u0063\u0061\u0073 \u004d\u0061\u0072\u0074\u0069\u006e\u0065\u007a",GLH2015: "\u0073\u0061\u0076\u006f\u0072\u0061"});
HackHax.push({GrandesLigas: "\u0046\u0061\u0062\u0072\u0069",GLH2015: "\u0067\u0069\u006d\u006e\u0061\u0073\u0069\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0045\u006c \u0043\u0068\u006f\u006c\u006f",GLH2015: "\u006d\u0061\u0072\u0063\u0065\u006c\u006f\u0073"});
HackHax.push({GrandesLigas: "\u0043\u0072\u0065\u0073\u0070\u006f",GLH2015: "\u006c\u0061\u0075\u0072\u0065\u0061\u006e\u006f\u0031\u0030"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0075\u0072\u0069 \u0041\u0066\u0066\u006f\u006e\u0073\u006f",GLH2015: "\u0068\u006f\u006d\u0065\u0072\u006f"});
HackHax.push({GrandesLigas: "\u0061\u006d\u0062\u0072\u006f\u007a\u007a\u0069\u006f",GLH2015: "\u006f\u0072\u006c\u0061\u006e\u0064\u006f"});
HackHax.push({GrandesLigas: "\u0045\u0075\u0073\u0065\u0062\u0069\u006f \u0042\u0031 \u004c\u0055\u0054",GLH2015: "\u0062\u0065\u0062\u0065\u0032\u0030\u0030\u0030"});
HackHax.push({GrandesLigas: "\u004e\u0069\u0063\u006f",GLH2015: "\u0050\u0065\u006c\u0075\u006c\u006c\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0053\u0068\u0061\u0066\u0074",GLH2015: "\u006a\u006f\u0072\u0067\u0069\u0074\u006f"});
HackHax.push({GrandesLigas: "\u0061\u006c\u006d\u0061\u0064\u0061 \u273f",GLH2015: "\u0061\u006c\u006d\u0061\u0064\u0061\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004b\u0072\u006f\u0073",GLH2015: "\u006f\u0073\u0074\u0061\u0063\u0075\u0073\u0031\u0035"});
HackHax.push({GrandesLigas: "\u0068\u0076\u0069\u0074\u0073\u0065\u0072\u006b",GLH2015: "\u004d\u0061\u006e\u0073\u0069\u006c\u006c\u0061\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0068\u0076\u0069\u0074\u0073\u0065\u0072\u006b",GLH2015: "\u006d\u0061\u006e\u0073\u0069\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0070\u006f\u0072\u006f\u0074\u006f \u004c\u0054\u0048\u0043",GLH2015: "\u0070\u006f\u0072\u006f\u0074\u006f\u0078"});
HackHax.push({GrandesLigas: "\u004c\u006f\u0063\u0041\u006e\u0064\u0065\u0072\u0073\u006f\u006e",GLH2015: "\u0061\u006e\u0064\u0065\u0072\u0031\u0030\u0031\u0039\u0031\u0040"});
HackHax.push({GrandesLigas: "\u004d\u0056",GLH2015: "\u006d\u0061\u0072\u0074\u0069\u006e\u0076\u0069\u0070"});
HackHax.push({GrandesLigas: "\u0045\u0072\u006c\u0069\u006e\u0067 \u0042\u0072\u0061\u0075\u0074 \u0048\u00e5\u006c\u0061\u006e\u0064",GLH2015: "\u006e\u006f\u0072\u0077\u0061\u0079\u006b\u0069\u006e\u0067"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0072\u006f",GLH2015: "\u0063\u0061\u0072\u0070\u0039\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0065\u006c\u0070\u0061\u0070\u0069\u0072\u0069\u006b\u006f\u0068\u0068",GLH2015: "\u0063\u0075\u0061\u0064\u0072\u006f\u0033\u0030\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0043\u0068\u0072\u0065\u0073",GLH2015: "\u0067\u0074\u0073\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u002d\u0041\u0072\u0069\u0069\u266a",GLH2015: "\u0073\u0061\u006c\u0069\u0064\u0061\u0031\u0032\u0033\u0034\u0035"});
HackHax.push({GrandesLigas: "\u0052\u0041\u0046\u0041 \u0047\u0041\u0052\u0043\u0049\u0041",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0034\u0033\u0032\u0031"});
HackHax.push({GrandesLigas: "\u0041\u006c\u0062\u0065\u0072\u0074\u006f",GLH2015: "\u0037\u0035\u0037\u002d\u0033\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0072\u00e2\u0070\u0074\u006f\u0072",GLH2015: "\u0061\u006c\u0064\u006f\u0073\u0069\u0076\u0069\u0031\u0039\u0031\u0033"});
HackHax.push({GrandesLigas: "\u254b\u06de\u1e4a\u1e6b\u1e08\u1e52\u053c\u1f0e\u1e64\u06de\u254b",GLH2015: "\u0032\u0035\u0032\u0035\u0031\u0033\u0031\u0035"});
HackHax.push({GrandesLigas: "\u0049\u0063\u0061\u0072\u0064\u0069",GLH2015: "\u0049\u0063\u0061\u0072\u0064\u0069\u0039\u0038"});
HackHax.push({GrandesLigas: "\u004c\u002e \u004d\u0061\u0072\u0074\u0069\u006e\u0065\u007a",GLH2015: "\u0065\u007a\u0065\u0031\u0039\u0039\u0038"});
HackHax.push({GrandesLigas: "\u006b\u0072\u006f\u0073\u0073\u0031\u0032\u0033",GLH2015: "\u006f\u0073\u0074\u0061\u0063\u0075\u0073\u0031\u0035\u0032\u0032"});
HackHax.push({GrandesLigas: "\u0053\u0070\u0065\u0063\u0074\u0072\u006f\u0077",GLH2015: "\u0032\u0032\u0030\u0039\u0035\u0036"});
HackHax.push({GrandesLigas: "\u006b\u0072\u006f\u0073",GLH2015: "\u006f\u0073\u0074\u0061\u0063\u0075\u0073\u0031\u0035"});
HackHax.push({GrandesLigas: "\u0057\u006f\u006f\u0064\u0073",GLH2015: "\u0050\u0041\u0043\u0041\u005a\u0031\u0033\u0035"});
HackHax.push({GrandesLigas: "\u0069\u006c\u006c\u0074\u006f\u006d\u0069\u0063",GLH2015: "\u0031\u0031\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0049\u0067\u006e\u0061\u0053\u0063\u006f\u0063\u0063\u006f",GLH2015: "\u0069\u0067\u006e\u0061\u0063\u0069\u006f\u0032\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0045\u0073\u0070\u0061\u0072\u0074\u0061\u0063\u006f",GLH2015: "\u006d\u006f\u0074\u006f\u0072\u0070\u0073\u0069\u0063\u006f"});
HackHax.push({GrandesLigas: "\u0042\u0061\u0063\u0068\u0061\u0074\u0065\u0072\u006f \u002d\u0046\u0061\u0053",GLH2015: "\u0068\u0061\u0078\u0032\u0030\u0030\u0031"});
HackHax.push({GrandesLigas: "\u0050\u006f\u007a\u0065",GLH2015: "\u0061\u0073\u0065\u0069\u006c\u0061\u0070\u006f\u0072\u0072\u0061"});
HackHax.push({GrandesLigas: "\uff33\uff29\uff2d\uff2f\uff2e\uff2e",GLH2015: "\u006c\u0065\u0061\u006e\u0064\u0072\u006f\u006e\u0070\u006c\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0044\u0065\u006c\u0067\u0061\u0064\u0069\u006c\u006c\u006f",GLH2015: "\u0030\u0031\u0031\u0033\u0032\u0035\u0039\u0035\u0039\u0039\u0038"});
HackHax.push({GrandesLigas: "\u20ab\u0454 \u006a\u00f8\u2229\u0067",GLH2015: "\u006b\u006c\u0065\u0062\u0065\u0072\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u004e\u0065\u006f\u0073",GLH2015: "\u0064\u0069\u0065\u0067\u006f\u0061\u006e\u0064\u0072\u0065\u0073\u0031"});
HackHax.push({GrandesLigas: "\u0054\u0061\u006b\u0065\u007a",GLH2015: "\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0042\u0061\u006d\u0062\u006f\u0075\u006e\u006f\u0075",GLH2015: "\u0061\u0062\u0063\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0041\u0067\u0075\u0073\u0046\u0065\u0072",GLH2015: "\u006a\u0061\u007a\u006d\u0069\u006e\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0044\u004f\u0055",GLH2015: "\u0065\u006c\u0062\u0061\u0072\u0074\u006f\u0062\u0061\u0072\u0074\u0032\u0030\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0070\u0075\u0072\u0065\u0054\u006f\u0075\u0063\u0061\u006e",GLH2015: "\u0042\u006f\u0063\u0061\u004a\u0075\u006e\u0069\u006f\u0072\u0073\u0031\u0032\u0035\u0038"});
HackHax.push({GrandesLigas: "\u0063\u006c\u006f\u006e\u0061\u007a\u0065\u0070\u0075\u006e\u006b",GLH2015: "\u0063\u006c\u006f\u006e\u0061\u007a\u0065\u0070\u0075\u006e\u006b"});
HackHax.push({GrandesLigas: "\u0045\u006c \u0050\u0061\u006c\u006f\u0073",GLH2015: "\u0041\u0070\u0061\u0067\u0034\u0065\u006c\u0063\u0065\u006c\u0075\u006c\u0061\u0072"});
HackHax.push({GrandesLigas: "\u0047\u0061\u006e\u006e\u0069\u0063\u0075\u0073",GLH2015: "\u0073\u006f\u006c\u006c\u0079\u0034\u006c\u0069\u0066\u0065\u0032\u0031\u0033"});
HackHax.push({GrandesLigas: "\u0076\u006f\u006c\u0074\u0072\u006f\u006e",GLH2015: "\u006d\u0065\u0073\u0074\u0061\u006c\u006c\u0061"});
HackHax.push({GrandesLigas: "\u004d\u0065\u006d\u00e9",GLH2015: "\u0031\u0031\u0030\u0037\u0031\u0039\u0039\u0039"});
HackHax.push({GrandesLigas: "\u0053\u0065\u0062\u0061\u0068",GLH2015: "\u006d\u006f\u006e\u006f\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0072\u0069\u006f \u0047\u00f6\u0074\u007a\u0065",GLH2015: "\u0031\u0032\u0033\u0033\u0032\u0031\u0034\u0035\u0036\u0037"});
HackHax.push({GrandesLigas: "\u0050\u0061\u0062\u006c\u006f\u0032\u0038",GLH2015: "\u0063\u006f\u006e\u0074\u0072\u0061\u0073\u0065\u00f1\u0061\u0064\u0069\u0066\u0069\u0063\u0069\u006c\u0039\u0037"});
HackHax.push({GrandesLigas: "\u0076\u0065\u0067\u0065\u0074\u0074\u0069",GLH2015: "\u0061\u0076\u0065\u006c\u006c\u0061\u006e\u0065\u0064\u0061\u0037\u0034\u0037"});
HackHax.push({GrandesLigas: "\u0054\u0079\u006c\u0065\u0072\u0336\u0043\u0336\u0336\u0047\u0336",GLH2015: "\u0031\u0032\u0066\u0074\u0031\u0034"});
HackHax.push({GrandesLigas: "\u0044\u0065\u006c\u0061\u006e\u0074\u0065\u0072\u006f \u004d\u0061\u0074\u0061\u0064\u006f\u0072",GLH2015: "\u0064\u0065\u006c\u0061\u006e\u0074\u0065\u0072\u006f\u006d\u0061\u0074\u0061\u0064\u006f\u0072\u0032\u0030\u0030\u0036"});
HackHax.push({GrandesLigas: "\u0066\u0061\u0063\u0063\u0075",GLH2015: "\u0077\u0077"});
HackHax.push({GrandesLigas: "\u2584\ufe3b\u253b\u2550\u2533\u4e00",GLH2015: "\u006d\u0061\u0072\u0063\u0065\u006c\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0053\u0075\u0061\u0072\u0065\u007a\u0021",GLH2015: "\u0034\u0036\u0033\u0039\u0033\u0030\u0039\u0033\u006c\u006f\u0070\u0065\u007a"});
HackHax.push({GrandesLigas: "\u0048\u0065\u0072\u006d\u0065\u0073",GLH2015: "\u004d\u0061\u006e\u0075\u0065\u006c\u0036\u0039\u0031"});
HackHax.push({GrandesLigas: "\u004d\u006f\u006e\u006e",GLH2015: "\u0062\u0061\u0074\u0061\u0074\u0061\u0032"});
HackHax.push({GrandesLigas: "\u0073\u006f\u006d\u0065\u0074\u0068\u0069\u006e\u0067",GLH2015: "\u0074\u0061\u0074\u0069\u0074\u0061\u0074\u006f"});
HackHax.push({GrandesLigas: "\u004c\u0075\u0069\u0073 \u004d\u0069\u0067\u0075\u0065\u006c",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0038\u0039\u0066\u0063\u0062"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0063 \u0061\u006c\u006c\u0069\u0073\u0074\u0065\u0072 \u0072\u006d \u0063\u0066",GLH2015: "\u006c\u006f\u0064\u0065\u0069\u0072\u006f\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0056\u1d00\u0274 \u0050\u1d07\u0280\u0073\u026a\u1d07",GLH2015: "\u006c\u0075\u0063\u0061\u0073\u0031\u0038"});
HackHax.push({GrandesLigas: "\u0050\u006f\u0063\u0068\u0069",GLH2015: "\u0034\u0035\u0031\u0031\u0037\u0037\u0036\u0036"});
HackHax.push({GrandesLigas: "\u25b8\ud835\udcdf\u1d0f\u1d04\u029c\u026a\u25c2",GLH2015: "\u0062\u0061\u0075\u0071\u0075\u0069\u006b"});
HackHax.push({GrandesLigas: "\u0048\u0069\u0067\u0075\u0061\u0069\u006e",GLH2015: "\u0068\u0069\u0067\u0075\u0061\u0069\u006e\u0032\u0030\u0030\u0036"});
HackHax.push({GrandesLigas: "\u0066\u0069\u0064\u0065\u006f",GLH2015: "\u0072\u0075\u0073\u0069\u006f\u0037\u0030\u006c\u006f\u0078"});
HackHax.push({GrandesLigas: "\u0049\u0438 \u0043\u006f\u043c\u0069\u0438\u0067",GLH2015: "\u0061\u0062\u0075\u0065\u006c\u006f\u0070\u0065\u0064\u0072\u006f\u0031"});
HackHax.push({GrandesLigas: "\u004b\u0075\u0072\u0074",GLH2015: "\u0070\u0061\u006e\u0074\u0065\u0072\u0061\u0031"});
HackHax.push({GrandesLigas: "\u0041\u0069\u006d\u0061\u0072",GLH2015: "\u0063\u0061\u0075\u0074\u0065\u0031\u0032\u0031\u0034"});
HackHax.push({GrandesLigas: "\u2112\ud835\udcca\ud835\udcbe\ud835\udcc8 \u2133\ud835\udcbe\u210a\ud835\udcca\u212f\ud835\udcc1",GLH2015: "\u0065\u0064\u0075\u0061\u006e\u0073\u0031\u0032\u0033\u0034\u0035"});
HackHax.push({GrandesLigas: "\u0272\u03b1\u2661\u10dd\u0069",GLH2015: "\u0065\u0071\u0075\u0069\u0073\u0064\u0065\u0078\u0064"});
HackHax.push({GrandesLigas: "\u004c\u0065\u006f \u0046\u0065\u0072\u006e\u0061\u006e\u0064\u0065\u007a",GLH2015: "\u0063\u0072\u0069\u0078\u0061\u007a\u0075\u006c\u0032\u0032"});
HackHax.push({GrandesLigas: "\u0046\u0061\u0076\u0069\u006f",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0038\u0039\u0064\u006b"});
HackHax.push({GrandesLigas: "\u00c9\u0072\u0069\u006b\u0061",GLH2015: "\u006b\u006c\u0033\u0062\u0073\u006f\u006e\u0031\u0035"});
HackHax.push({GrandesLigas: "\u0198\u1d1c\u0280\u1d1b",GLH2015: "\u0072\u006f\u006f\u006d\u006f\u006e\u0066\u0069\u0072\u0065\u0037\u0038"});
HackHax.push({GrandesLigas: "\u004a\u0061\u0076\u0061",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0038\u0039"});
HackHax.push({GrandesLigas: "\u0044\u0061\u006d\u006f\u006e \u004d\u0061\u006e\u0065\u006c\u0065",GLH2015: "\u0072\u006f\u006a\u006f\u0073\u006f\u0073\u006d\u0069\u0076\u0069\u0064\u0061\u0032"});
HackHax.push({GrandesLigas: "\u004a\u0075\u0061\u006e\u0063\u0069\u0074\u006f",GLH2015: "\u0032\u0030\u0030\u0039"});
HackHax.push({GrandesLigas: "\u006c\u0075\u0063\u0065\u0072\u006f",GLH2015: "\u0070\u0069\u0063\u0061\u0063\u0068\u0075"});
HackHax.push({GrandesLigas: "\u0045\u006c\u0055\u006c\u0074\u0069\u006d\u006f\u0034\u0031",GLH2015: "\u0065\u0066\u0062\u0069\u0073\u0068\u0069\u0032\u0031"});
HackHax.push({GrandesLigas: "\u0053\u0069\u006e \u004e\u0069\u0063\u006b",GLH2015: "\u0045\u0073\u0074\u0072\u0065\u006c\u006c\u0061\u0073\u0038"});
HackHax.push({GrandesLigas: "\u169b\u1ddd\u1680\u0363\u1680\u036b\u0191\u027e\u0105\u0572\u00e7\u04bd\u0282\u00e7\u0585\u1680\u036d\u1680\u036a\u169c\u0364 \u0031\u20df\u0030",GLH2015: "\u006d\u0061\u0074\u0068\u0069\u0032\u0031\u0033\u0033"});
HackHax.push({GrandesLigas: "\u004d\u0069\u006b\u0065\u004d\u004a\u0042",GLH2015: "\u0068\u006f\u006c\u0061\u0071\u0075\u0065\u0068\u0061\u0063\u0065\u0031"});
HackHax.push({GrandesLigas: "\u004e\u0065\u0073\u0074\u0061",GLH2015: "\u0064\u006f\u0077\u006e\u0031\u0033\u0033"});
HackHax.push({GrandesLigas: "\u0052\u006f\u0062\u0062\u0069\u0065",GLH2015: "\u0031\u0062\u0032\u0062\u0033\u0062\u0034\u0062"});
HackHax.push({GrandesLigas: "\u004f\u006e\u0069\u0069 \u0043\u0068\u0061\u006e",GLH2015: "\u0074\u0069\u0067\u0072\u0065\u006e\u0065\u0067\u0072\u006f\u0034\u0036\u0034\u0033"});
HackHax.push({GrandesLigas: "\u004c\u0075\u0063\u0069",GLH2015: "\u0076\u0065\u006e\u0067\u0061\u006e\u007a\u0061\u0031"});
HackHax.push({GrandesLigas: "\u0043\u006c\u0065\u0061\u0072\u006c\u0079\u0053\u0068\u006f\u0063\u006b\u0065\u0064",GLH2015: "\u0076\u0065\u0067\u0065\u0074\u0074\u0061\u0037\u0037\u0037"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0072\u0069\u006f \u0052\u0069\u0073\u0073\u006f",GLH2015: "\u0070\u006c\u0061\u007a\u0061\u0063\u006f\u006c\u006f\u006e\u0069\u0061"});
HackHax.push({GrandesLigas: "\u0073\u0061\u006e\u0074\u0061\u0066\u0065\u0073\u0069\u006e\u0075\u0077\u0075",GLH2015: "\u0031\u0031\u0030\u0032\u0032\u0030\u0030\u0035"});
HackHax.push({GrandesLigas: "\u0054\u0068\u0065 \u0053\u0063\u0069\u0065\u006e\u0063\u0065\u002d\u0057\u0061\u006c\u006c \u0053\u0074\u0072\u0065\u0065\u0074",GLH2015: "\u0065\u0073\u0074\u0065\u006c\u0061\u0072\u0036\u0033\u0032\u0031"});
HackHax.push({GrandesLigas: "\u006a\u0075\u0062\u0061\u006c\u0069\u0073\u0073\u006f\u006e",GLH2015: "\u0074\u0065\u0061\u006d\u006f\u0069\u006e\u0074\u0065\u0072\u0032\u0030\u0030\u0036"});
HackHax.push({GrandesLigas: "\u004a\u1d1c\u0299\u1d00\u029f\u026a\u0073\u0073\u1d0f\u0274",GLH2015: "\u0030\u0030\u0031\u0039\u0038\u0038"});
HackHax.push({GrandesLigas: "\u0044\u0065\u006d\u0070\u0068\u0069\u0073\u004d\u0065\u0070\u0061\u0079",GLH2015: "\u0068\u0075\u0067\u0075\u0069\u0074\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004c\u0041\u0055\u0054\u0049\u0052\u0045\u0058",GLH2015: "\u0031\u0032\u0033\u0032\u0031"});
HackHax.push({GrandesLigas: "\u004c\u002e\u0050\u0061\u0072\u0065\u0064\u0065\u0073",GLH2015: "\u0074\u0065\u006d\u0070\u006f\u0072\u0061\u006c\u0030\u0031"});
HackHax.push({GrandesLigas: "\u0063\u0061\u0073\u0065\u0074\u0074\u0061",GLH2015: "\u006c\u006f\u006c\u0031\u0032\u0033\u0034\u0035"});
HackHax.push({GrandesLigas: "\ud835\udc69\ud835\udc90\ud835\udc8d\ud835\udc94\ud835\udc90\ud835\udc8f\ud835\udc82\ud835\udc93\ud835\udc90",GLH2015: "\u006a\u006f\u0061\u0070\u0061\u0074\u0072\u0069\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u005a\u0061\u0072\u0061\u0063\u0068\u0069\u0074\u006f",GLH2015: "\u006c\u0061\u0063\u0061\u0064\u0065\u0072\u0063"});
HackHax.push({GrandesLigas: "\u0048\u0067\u0061\u006e\u0069\u0073",GLH2015: "\u0074\u006f\u0062\u0069\u0061\u0073\u0062\u006f\u006d\u0062\u006c\u0061\u006e"});
HackHax.push({GrandesLigas: "\u004d\u0069\u006e\u0067\u006f\u006c\u0065 \u0053\u0054",GLH2015: "\u0078\u0078\u006c\u0065\u006f\u006e\u006e\u0061\u0078\u0078\u0031"});
HackHax.push({GrandesLigas: "\u004c\u0065\u0063\u0068\u0075\u0073\u0061",GLH2015: "\u0070\u0065\u0064\u0072\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004f\u0063\u0074\u0061",GLH2015: "\u004d\u0049\u006d\u0061\u006d\u0061\u006d\u0065\u0061\u006d\u0061"});
HackHax.push({GrandesLigas: "\u004a\u0061\u0076\u0069",GLH2015: "\u006a\u0061\u0076\u0069\u0074\u006f\u0062\u006f\u006c\u0073\u006f\u0039\u0039"});
HackHax.push({GrandesLigas: "\u0057\u0075 \u004c\u0065\u0069",GLH2015: "\u0070\u006f\u006c\u006f\u006e\u0067\u006f\u0030\u0039"});
HackHax.push({GrandesLigas: "\u00c1\u006e\u0067\u0065\u006c \u0052\u006f\u006d\u0065\u0072\u006f \u0039\u0032 \u0055\u0054",GLH2015: "\u0063\u0069\u0063\u006c\u006f\u006e\u0031\u0030\u0030"});
HackHax.push({GrandesLigas: "\ud83d\udc14",GLH2015: "\u006e\u0069\u006e\u0069\u0074\u006f\u006e\u0074\u006f"});
HackHax.push({GrandesLigas: "\u0053\u0065\u0062\u0061\u0073\u0074\u0069\u00e1\u006e \u0050\u0069\u00f1\u0065\u0072\u0061",GLH2015: "\u0073\u0065\u0062\u0061\u0076\u0061\u0033\u0033\u0033"});
HackHax.push({GrandesLigas: "\u0064\u0075\u0073\u0074  \u0027\u044f\u0046",GLH2015: "\u0034\u0035\u0038\u0033\u0038\u0030\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0075\u0077\u0075",GLH2015: "\u0038\u0034\u0038\u0038\u0037\u0034\u0039\u0037"});
HackHax.push({GrandesLigas: "\u0046\u0072\u0075\u0074\u0069\u006c\u006c\u0069\u0074\u0061",GLH2015: "\u0053\u006f\u0079\u0064\u0065\u0072\u0069\u0076\u0065\u0072"});
HackHax.push({GrandesLigas: "\u002d\ud835\udc9c\ud835\udc5f\ud835\udc56\ud835\udc56\u266a",GLH2015: "\u0063\u0061\u0069\u0035\u0032\u0037\u0036"});
HackHax.push({GrandesLigas: "\u004a\u006f\u0073\u0065\u0068",GLH2015: "\u0031\u0032\u0033\u0033\u0032\u0031"});
HackHax.push({GrandesLigas: "\u0048\u006f\u006c\u0061 \u003a\u0044",GLH2015: "\u0067\u0061\u0073\u0074\u0069\u0069\u0032\u0030\u0030\u0034"});
HackHax.push({GrandesLigas: "\u004d\u0069\u006e\u0069\u0063\u006b",GLH2015: "\u0034\u0038\u0034\u0038\u0033\u0037\u0039\u0034\u006c\u0065\u006f"});
HackHax.push({GrandesLigas: "\u003c\u003d \u0053\u006b\u0075\u006c\u006c\u0069\u0065 \u003d\u003e",GLH2015: "\u006c\u006f\u006c\u0037\u0039\u0038\u0037\u0039\u0038"});
HackHax.push({GrandesLigas: "\ud835\udc03\ud835\udc0e\ud835\udc14\u0032",GLH2015: "\u0062\u0061\u0072\u0074\u0032\u0036"});
HackHax.push({GrandesLigas: "\u006c\u0075\u0063\u0063\u0068\u0065\u0074\u0074\u0031",GLH2015: "\u0032\u0030\u0030\u0033\u006d\u0061\u0074\u0065\u006f"});
HackHax.push({GrandesLigas: "\u0047\u0065\u006e\u0061\u0048\u0027",GLH2015: "\u006c\u006f\u006c\u0061\u007a\u006f\u0030\u0030\u0030\u0030"});
HackHax.push({GrandesLigas: "\ud835\udc06\u0e25\u0432\u044f\u00fd\u044d\u2113 \ud835\udc01\u0e25\u0e23\u2020\u0e4f\u0e23",GLH2015: "\u0063\u0061\u006d\u0069\u0074\u006f"});
HackHax.push({GrandesLigas: "\ud835\uddd9\ud835\uddf2\ud835\uddf1\ud835\uddf2\ud835\uddff\ud835\uddf6\ud835\uddf0\ud835\uddfc \u2022 \ud835\udc08\ud835\udc1d\ud835\udc0c",GLH2015: "\u0066\u0065\u0064\u0065\u0072\u0069\u0063\u006f\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0054\u006f\u0074\u006f \u0053\u0061\u006c\u0076\u0069\u006f",GLH2015: "\u0054\u006f\u0074\u006f\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0056\u0065\u006c\u0061\u0072\u0067",GLH2015: "\u0067\u0074\u0061\u0031\u0033\u0035\u0037\u0039"});
HackHax.push({GrandesLigas: "\u0044\u0061\u0076\u0069\u0064 \u0053\u0069\u006c\u0076\u0061 \u0023",GLH2015: "\u0071\u0075\u0065\u0073\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004b\u0065\u0076\u0069\u006e \u0044\u0065 \u0042\u0072\u0075\u0079\u006e\u0065 \u0031\u0037",GLH2015: "\u004a\u0075\u0061\u006e\u0069\u0074\u0061\u0031\u0032\u0039\u0039"});
HackHax.push({GrandesLigas: "\u0045\u006c \u0050\u0065\u0070\u0065 \u0053\u0061\u006e\u0064",GLH2015: "\u0077\u0065\u0072\u0073\u0064\u0066\u0078\u0063\u0076\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0050\u0065\u0072\u006f\u0073\u0076\u0061\u006c\u0064\u006f",GLH2015: "\u0067\u0061\u0062\u0030\u0032\u0032\u0030\u0030\u0037"});
HackHax.push({GrandesLigas: "\u004b\u0068\u0065\u0072\u0065\u0076",GLH2015: "\u006b\u0068\u0065\u0072\u0065\u0076\u0070\u0069\u0063\u0061\u006e\u0074\u0065"});
HackHax.push({GrandesLigas: "\u0048\u0065\u006e\u0072\u0079",GLH2015: "\u0066\u0061\u0063\u0075\u006e\u0064\u006f"});
HackHax.push({GrandesLigas: "\ud835\ude77\u1d07\u0274\u0280\u028f",GLH2015: "\u0068\u0065\u006e\u0072\u0079"});
HackHax.push({GrandesLigas: "\u0070\u0069\u0074\u0069\u0074\u006f",GLH2015: "\u0052\u0075\u0073\u006b\u0069\u006e\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0054\u0045\u0054 \u2601 \ud835\udcf6\ud835\udcea\ud835\udcf7\ud835\udcfd\ud835\udcee\ud835\udcf0\ud835\udcea \u2601",GLH2015: "\u006e\u0069\u0063\u006f\u006c\u0061\u0073\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0061\u0067\u0075\u0073",GLH2015: "\u0075\u0073\u0075\u0061\u0072\u0069\u006f\u002e\u0032"});
HackHax.push({GrandesLigas: "\u0064\u0065 \u0072\u006f\u0073\u0073\u0069 \u0028\u006c\u0065\u0073\u0069\u006f\u006e\u0061\u0064\u006f\u0029",GLH2015: "\u0065\u0073\u0063\u0075\u0065\u006c\u0061"});
HackHax.push({GrandesLigas: "\u0049\u006e\u0069\u0073\u004b",GLH2015: "\u004c\u0041\u004b\u004f\u0050"});
HackHax.push({GrandesLigas: "\u0066\u0072\u0061\u006e\u006e \u2022 \u0053\u0043\u0054",GLH2015: "\u0063\u0075\u0065\u0072\u0076\u006f\u0062\u0065\u006e\u0031\u0030"});
HackHax.push({GrandesLigas: "\u2131\u0280\u0061\u0274\u0274 \u26bd",GLH2015: "\u0066\u0072\u0061\u006e\u0063\u006f\u0070\u006f\u006e\u0066\u0069\u006c"});
HackHax.push({GrandesLigas: "\u00c9\u0064\u0065\u0072 \u004d\u0069\u006c\u0069\u0074\u00e3\u006f",GLH2015: "\u006d\u0061\u0072\u0063\u0061\u0064\u006f\u0070\u0065\u0073"});
HackHax.push({GrandesLigas: "\u004d\u0065\u006d\u0070\u0068\u0069\u0073 \u0044\u0065\u0070\u0061\u0079",GLH2015: "\u006e\u0069\u0063\u006f\u0037\u0061\u0073\u0065"});
HackHax.push({GrandesLigas: "\u0048\u0061\u0069\u006c\u0065",GLH2015: "\u0043\u004f\u0052\u0055\u0053\u0043\u0041\u004e\u0054"});
HackHax.push({GrandesLigas: "\ud835\udce5\ud835\udc86\ud835\udc8d\ud835\udc82\ud835\udc93\ud835\udc88",GLH2015: "\u0067\u0074\u0061\u0031\u0033\u0035\u0037\u0039\u0031\u0031"});
HackHax.push({GrandesLigas: "\u004d\u0069\u006c\u006b\u0079 \u0057\u0061\u0079",GLH2015: "\u0068\u006f\u006c\u0061\u0073\u0075\u0074\u0069\u006f"});
HackHax.push({GrandesLigas: "\u002d\u0047\u006f\u006e\uc870",GLH2015: "\u0066\u0065\u0072\u0072\u0069\u0073\u0074\u0061"});
HackHax.push({GrandesLigas: "\u0061\u0075\u0074\u0075\u006d\u006e",GLH2015: "\u0063\u0061\u0063\u0061\u0064\u0065\u0067\u0061\u0074\u006f\u0031\u0034"});
HackHax.push({GrandesLigas: "\u002d\u0047\u0068\u006f\u006e\uc870",GLH2015: "\u0072\u0065\u0073\u0075\u0063\u0074\u0069\u006e\u0067"});
HackHax.push({GrandesLigas: "\u002d\ud835\udc6e\ud835\udc89\ud835\udc90\ud835\udc8f\u002d",GLH2015: "\u0061\u0048\u0061"});
HackHax.push({GrandesLigas: "\u0043\u0030\u004b\u0031\u0054\u0034",GLH2015: "\u0061\u0072\u0067\u0065\u006e\u0074\u0069\u006e\u0061\u0074\u006f\u0074\u006f\u0031\u0032"});
HackHax.push({GrandesLigas: "\uff24\uff21\uff2e\uff2e\uff25\uff33",GLH2015: "\u0074\u006f\u0062\u0069\u0061\u0073\u0063\u006f\u0072\u0069\u0061\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0065\u006c\u0070\u0075\u006c\u0067\u0061",GLH2015: "\u0049\u006e\u0064\u0065\u0070\u0065\u006e\u0064\u0069\u0065\u006e\u0074\u0065\u0031\u0032\u0033\u0034\u0035\u0036"});
HackHax.push({GrandesLigas: "\u0054\u0061\u006e\u006e\u0075 \u0054\u0075\u0076\u00e1",GLH2015: "\u0076\u0065\u006c\u0065\u007a\u0061\u006e\u006f"});
HackHax.push({GrandesLigas: "\u0045\u006c \u0043\u0065\u006a\u0061\u0073",GLH2015: "\u0074\u0075\u0074\u0065\u0063\u0061\u0070\u006f"});
HackHax.push({GrandesLigas: "\ud835\udc08\ud835\udc27\ud835\udc2f\ud835\udc1a\u0301\ud835\udc25\ud835\udc22\ud835\udc1d\ud835\udc28",GLH2015: "\u0073\u0065\u006c\u006f\u006d\u0065\u0072\u0065\u0063\u0065\u0031\u0038"});
HackHax.push({GrandesLigas: "\u0074\u006f\u006d\u006d\u0079\u006b\u0075\u0075\u006e",GLH2015: "\u0074\u0074\u006f\u006d\u006d\u0079\u0031\u0039\u0039\u0039"});
HackHax.push({GrandesLigas: "\ud83d\udc58",GLH2015: "\ud83d\udc58"});
HackHax.push({GrandesLigas: "\u004e\u0069\u0063\u006f \u0054\u004d",GLH2015: "\u0034\u0034\u0030\u0032\u0032\u0032\u0033\u0033"});
HackHax.push({GrandesLigas: "\u0044\u0075\u0061\u006c \ud83c\udf1f",GLH2015: "\u0063\u0061\u0063\u0068\u0065\u0074\u0069\u006e\u0039"});
HackHax.push({GrandesLigas: "\ud835\udd0f\ud835\udd2c\ud835\udd2e\ud835\udd32\ud835\udd26\ud835\udd31\ud835\udd2c \u210c\ud835\udd07",GLH2015: "\u004c\u004f\u0053 \u0070\u0065\u0074\u0065\u0073"});
HackHax.push({GrandesLigas: "\u004c\u0065\u0061\u006e\u0074 \u007c \u0057\u0055",GLH2015: "\u0073\u0061\u006e\u0074\u0079\u0074\u0068\u006f\u006d\u0061\u0073\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\ud835\udda6\u028f\u0274\ud835\udebb\u1d1c\u0280\u0299\u1d0f",GLH2015: "\u0063\u0061\u006d\u0069\u0074\u006f\u006f"});
HackHax.push({GrandesLigas: "\ud835\udc6e\ud835\ude3a\ud835\ude2f\u26a1\ud835\udc7b\ud835\ude36\ud835\ude33\ud835\ude23\ud835\ude30",GLH2015: "\u0067\u0079\u006e\u0031\u0039\u0037\u0039"});
HackHax.push({GrandesLigas: "\ud835\udd3c\ud835\udd5d \ud835\udd44\ud835\udd56\ud835\udd5f\ud835\udd60\ud835\udd63",GLH2015: "\u0045\u006c \u006d\u0069\u006c\u006c\u006f"});
HackHax.push({GrandesLigas: "\ud835\udd3c\ud835\ude95\u005f\ud835\udd44\ud835\ude8e\ud835\ude97\ud835\ude98\ud835\ude9b",GLH2015: "\u0045\u006c \u006d\u0069\u006c\u006c\u006f\u006e\u0061\u0072\u0069\u006f"});
HackHax.push({GrandesLigas: "\u004e\u006f\u0058",GLH2015: "\u0066\u0075\u0074\u0062\u006f\u006c\u0061\u0064\u0069\u0064\u0061\u0073"});
HackHax.push({GrandesLigas: "\u0053\u0074\u0072\u006f\u006f\u0074",GLH2015: "\u006a\u0065\u0072\u006f\u0034\u0032\u0034\u0031"});
HackHax.push({GrandesLigas: "\u004c\u0075\u0063\u0068\u0069\u0061\u006e\u006f",GLH2015: "\u0072\u006f\u0062\u0065\u0072\u0066\u0061\u0063\u0075\u0031\u0032"});
HackHax.push({GrandesLigas: "\u007a\u0065 \u0072\u006f\u0062\u0065\u0072\u0074\u006f\u0027",GLH2015: "\u0068\u0065\u0072\u006e\u0061\u006e\u0032\u0037\u0030\u0033\u0039\u0035"});
HackHax.push({GrandesLigas: "\u0045\u006c \u004a\u0041\u004a\u0041\u0053",GLH2015: "\u006c\u006c\u006f\u0073\u0065\u0072\u006c\u006f\u006c"});
HackHax.push({GrandesLigas: "\u0046\u0069\u006c\u0069",GLH2015: "\u0076\u0061\u006c\u0065\u006e\u0076\u0061\u006c\u0030\u0038"});
HackHax.push({GrandesLigas: "\u0074\u0072\u0061\u006e\u003b",GLH2015: "\u0073\u0061\u006e\u006a\u0075\u0061\u006e\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0063\u0068\u0065\u006c\u006f",GLH2015: "\u0063\u006f\u006e\u0074\u0072\u0061\u0073\u0065\u00f1\u0061\u0068\u0061\u0078\u0062\u0061\u006c\u006c"});
HackHax.push({GrandesLigas: "\u0063\u0068\u0065\u006c\u006f\ud835\ude0f\ud835\ude1b\ud835\ude0e",GLH2015: "\u0063\u006f\u006e\u0074\u0072\u0061\u0073\u0065\u00f1\u0061\u0068\u0061\u0078\u0062\u0061\u006c\u006c\u0031"});
HackHax.push({GrandesLigas: "\u0050\u0061\u0062\u006c\u006f\u0032\u0038",GLH2015: "\u0074\u006f\u006d\u0062\u0061\u0073\u0069\u006e\u0063\u0065\u0030\u0038"});
HackHax.push({GrandesLigas: "\u00b9\u004d\u0065\u006e\u0064\u006f\u007c\u004e\u006f\u006f\u0062\u00b9 \u00ac \u004a \u00ac",GLH2015: "\u007a\u006f\u0072\u0072\u006f\u0070\u0076\u0070\u0067\u0061\u006d\u0065\u0072\u0040\u0067\u006d\u0061\u0069\u006c\u002e\u0063\u006f\u006d"});
HackHax.push({GrandesLigas: "\u00b9\u2133\u1d07\u0274\u1d05\u1d0f\u007c\ud835\udca9\u1d0f\u1d0f\u0299\u00b9 \u00ac \u004a \u00ac",GLH2015: "\u0030\u0030\u0033\u0034\u0037\u0035\u007a\u0072"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0074\u006f\u0073\u0063\u0072\u0069\u006d",GLH2015: "\u006a\u0061\u006e\u0075\u0074\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0041\u006c\u0066\u006f\u006e\u0073\u0069\u006e",GLH2015: "\u006c\u0069\u0063\u0068\u0061\u006c\u006f\u0070\u0065\u007a\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004d\u0061\u006e\u0064\u0072\u0061\u006b\u0065",GLH2015: "\u0063\u0061\u007a\u0061\u0064\u006f\u0072\u0031"});
HackHax.push({GrandesLigas: "\u0068\u0075\u006e\u0074\u0065\u006c\u0061\u0061\u0072",GLH2015: "\u0063\u0068\u0065\u006c\u0073\u0061\u0031"});
HackHax.push({GrandesLigas: "\ud835\udc3f\ud835\udc4e\ud835\udc5a\ud835\udc4f\ud835\udc5c\ud835\udc5f\ud835\udc54\u210e\ud835\udc56\ud835\udc5b\ud835\udc56 \u30c4",GLH2015: "\u0068\u0061\u0072\u0074\u006d\u0061\u006e\u006e"});
HackHax.push({GrandesLigas: "\u0042\u006f\u006f\u006d\u0065\u0072\u004a",GLH2015: "\u0050\u0045\u0052\u0052\u0049\u0054\u004f\u0050\u0041\u0050\u0055\u0052\u0052\u0049\u0050\u0041\u0050\u0041"});
HackHax.push({GrandesLigas: "\u0076\u0069\u006e\u006e\u0069",GLH2015: "\u0053\u0069\u006c\u0076\u006f\u006e\u0065\u0079\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0043\u0068\u00e9\u0072\u0079\u0073\u0068\u0065\u0076 \u0041\u0054\u004d",GLH2015: "\u0054\u0069\u0061\u0067\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0044\u006f\u006f\u006d \u0046\u0075\u0074\u0075\u0072\u0065",GLH2015: "\u0036\u0037\u006d\u0070"});
HackHax.push({GrandesLigas: "\u0061\u0072\u0066\u0061",GLH2015: "\u0028\u0066\u0061\u0062\u0031\u0030\u006e\u0031\u0063\u0030\u0029"});
HackHax.push({GrandesLigas: "\u0043\u0065\u0070\u0061",GLH2015: "\u0053\u0065\u0072\u0065\u0061\u006c\u0065\u0073\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0052\u006f\u006a\u006f",GLH2015: "\u0072\u006f\u006a\u006f\u0063\u0061\u0070\u006f\u0031"});
HackHax.push({GrandesLigas: "\u0050\u0075\u0079\u006f\u006c",GLH2015: "\u004d\u0061\u0074\u0069\u0061\u0073\u0033\u0032"});
HackHax.push({GrandesLigas: "\u0048\u0065\u0074\u0066\u0069\u0065\u006c\u0064",GLH2015: "\u0066\u0068\u0063\u0072\u0032\u0033\u0039\u0039"});
HackHax.push({GrandesLigas: "\u0050\u0072\u006f\u0066\u0065\u0073\u006f\u0072",GLH2015: "\u0061\u0073\u0064\u0061\u0073\u0064"});
HackHax.push({GrandesLigas: "\u004c\u0075\u0063\u0068\u0069\u006d\u0062\u006f",GLH2015: "\u006c\u0075\u0063\u0068\u0069\u006d\u0062\u006f\u0039\u0039"});
HackHax.push({GrandesLigas: "\ud835\udd6d\ud835\udd70\ud835\udd79\ud835\udd75\ud835\udd6c",GLH2015: "\u0062\u0065\u006e\u006a\u0061\u006d\u0069\u006e\u0063\u0061\u0072\u0064\u006f\u007a\u006f"});
HackHax.push({GrandesLigas: "\u0066\u0065\u0064\u0065\u005f\u0048\u0054\u0047",GLH2015: "\u0061\u0072\u0064\u0075\u0069\u006e\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0054\u0068\u0065\u0065\u0075\u0053",GLH2015: "\u0031\u0038\u0030\u0034\u0030\u0030\u0074\u0065\u0074\u0065\u0075"});
HackHax.push({GrandesLigas: "\u0072\u0069\u006a\u006b\u0061\u0061\u0072\u0064",GLH2015: "\u0075\u006e\u0069\u006f\u006e\u0073\u0061\u006e\u0074\u0061\u0066\u0065\u0032\u0032"});
HackHax.push({GrandesLigas: "\u0042\u0065\u006e\u007a\u0065\u006d\u0061",GLH2015: "\u0062\u0065\u006e\u007a\u0033\u006d\u0034"});
HackHax.push({GrandesLigas: "\u0048\u0061\u0072\u0061\u006d\u0062\u0065",GLH2015: "\u0031\u0032\u0033\u006d\u006f\u0072\u0072\u0069\u0073"});
HackHax.push({GrandesLigas: "\u0063\u0061\u00ed\u0063\u006f",GLH2015: "\u0039\u0036\u0031\u0034\u0030\u0030\u0036\u0030"});
HackHax.push({GrandesLigas: "\u0043\u0068\u0075\u006b\u0079\u006c\u006c\u006f\u0037",GLH2015: "\u0066\u0061\u0073\u006f\u0074\u0069\u006e\u0074\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0043\u0068\u00e9\u0072\u0079\u0073\u0068\u0065\u0076",GLH2015: "\u0061\u0067\u0075\u0073\u0074\u0069\u006e\u0061"});
HackHax.push({GrandesLigas: "\ud835\udc6a\u029c\u1d07\u0301\u0280\u028f\u0073\u029c\u1d07\u1d20",GLH2015: "\u0041\u0067\u0075\u0073\u0074\u0069\u006e\u0061\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0046\u0069\u0076\u0065\u0053\u006b\u0069\u006c\u006c\u0073",GLH2015: "\u0066\u0075\u0072\u0069\u006f\u0073\u006f\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0053\u03b1\u03b7\u0074\u0069\u002d\u0047 \u002f \u0046\u00dc",GLH2015: "\u006a\u0075\u0067\u0061\u0064\u006f\u0072\u0038"});
HackHax.push({GrandesLigas: "\u0073\u006b\u006f\u0072\u0070\u0073",GLH2015: "\u006d\u0061\u0072\u0069\u006f\u0032\u0030\u0030\u0033"});
HackHax.push({GrandesLigas: "\u0045\u0076\u006f",GLH2015: "\u0071\u0077\u0065\u0072\u0074\u0079"});
HackHax.push({GrandesLigas: "\u006b\u0030\u0066\u0065\u0065",GLH2015: "\u006d\u0061\u0078\u0069\u006d\u006f\u0031\u0035\u0037\u0038\u0039"});
HackHax.push({GrandesLigas: "\u0050\u0069\u006a\u0061\u006e\u006f\u0076\u0069\u0063\u0068",GLH2015: "\u006c\u0061\u006d\u0061\u0074\u0061\u006e\u007a\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\ud835\udc0c\ud835\udc1a\ud835\udc31\ud835\udc22\ud835\udc7a\ud835\udc72\ua589 \u268a \ud835\udcd6\ud835\udce1\ud835\udcd4",GLH2015: "\u0073\u0075\u0070\u0065\u0072\u006d\u0061\u006e\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0053\u006f\u0075\u006c\u006f\u006d\u0068\u0065\u0064 \u0041\u006c\u002d\u0050\u0069\u00f1\u0061",GLH2015: "\u0053\u006f\u0075\u006c\u006f"});
HackHax.push({GrandesLigas: "\u0050\u1d00\u1d05\u0280\u1d07 \u0047\u0280\u1d00\u0073\u0073\u026a \u271d",GLH2015: "\u0050\u0061\u0064\u0072\u0065\u0067\u0072\u0061\u0073\u0073\u006f"});
HackHax.push({GrandesLigas: "\u0073\u006f\u006c\u007a\u0069",GLH2015: "\u0073\u006f\u006c\u0063\u0069\u0074\u006f\u0032\u0031"});
HackHax.push({GrandesLigas: "\u0053\u006f\u0075\u006c\u006f\u0034\u0034\u0032\u0033",GLH2015: "\u0036\u0038\u0033\u0038\u0038\u0039\u0036"});
HackHax.push({GrandesLigas: "\u0065\u0074\u006f\u0027\u006f",GLH2015: "\u0064\u0065\u006c\u0062\u0061\u006a\u006f\u0031\u0032\u0033\u0061"});
HackHax.push({GrandesLigas: "\u005a\u0061\u0062\u006f\u006c\u006f\u0074\u006e\u0079",GLH2015: "\u0064\u0065\u006d\u0034\u0037\u0037\u0032\u0035"});
HackHax.push({GrandesLigas: "\u0078\u0044",GLH2015: "\u0054\u0045\u004d\u0050\u004f\u0052\u0041\u004c\u0030\u0031\u0032"});
HackHax.push({GrandesLigas: "\u004d\u026a\u1d1b\u1d0f\u0299\u1d0f\u1d1b\u1d0d\u1d1c\u1d04\u1d00",GLH2015: "\u0037\u0039\u0031\u0030\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0042\u0061\u0064\u0041\u0063\u0074\u006f\u0072",GLH2015: "\u006c\u0075\u0063\u0061\u0031\u0031\u0032\u0032\u0033\u0033"});
HackHax.push({GrandesLigas: "\u0050\u0065\u006c\u006c\u0069\u0073\u0074\u0072\u0069",GLH2015: "\u0065\u006c\u0076\u0065\u0072\u0067\u006f\u0074\u0061\u0073\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\ud835\ude76\ud835\ude9e\ud835\ude92\ud835\ude8d\ud835\ude98\u002e \ud83d\udc3b",GLH2015: "\u0041\u006d\u0061\u0072\u0069\u006c\u006c\u006f"});
HackHax.push({GrandesLigas: "\u0054\u006f\u0064\u006f\u0050\u006f\u0064\u0065\u0072\u006f\u0073\u006f",GLH2015: "\u0072\u006f\u0064\u0072\u0069\u0067\u006f\u0073\u006f\u0039\u0039"});
HackHax.push({GrandesLigas: "\ud835\udde7\u1d0f\u1d05\u043e\u01a4\u043e\u1d05\u025b\u0280\u043e\ud835\udc60\u043e",GLH2015: "\u0063\u0061\u006c\u006c\u0065\u0066\u0061\u006c\u0073\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\ud835\ude4f\ud835\ude64\ud835\ude59\ud835\ude64\ud835\udc43\ud835\udc5c\ud835\udc51\ud835\udc52\ud835\udc5f\ud835\udc5c\ud835\udc60\ud835\udc5c",GLH2015: "\u0072\u006f\u0072\u006f\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0066\u0072\u0065\u006e\u006b\u0069\u0065",GLH2015: "\u0076\u0069\u007a\u0063\u0061\u0063\u0068\u0061\u0031\u0034"});
HackHax.push({GrandesLigas: "\ud835\udcaf\u1d0f\u0257\u1d0f\ud835\udcab\u1d0f\u0257\u1d07\u1d19\u1d0f\u0073\u1d0f",GLH2015: "\u0034\u0035\u0036\u0032"});
HackHax.push({GrandesLigas: "\u0050\u0061\u0075\u006c",GLH2015: "\u0050\u0061\u0075\u006c\u0031\u0039"});
HackHax.push({GrandesLigas: "\u005b\ud835\udc12\ud835\udc21\ud835\udc1e\ud835\udc25\ud835\udc1d\ud835\udc28\ud835\udc2b\u005d \u2022 \ud835\udc08\ud835\udc1d\ud835\udc0c",GLH2015: "\u0042\u0061\u0073\u006f\u0063\u006f\u006e\u0063\u006f\u0063\u0061\u0035\u0034"});
HackHax.push({GrandesLigas: "\u004c\u006f\u0074\u0068\u0061\u0072 \u004d\u0061\u0074\u0074\u0068\u0061\u00fc\u0073",GLH2015: "\u0076\u0061\u006c\u0075\u0033\u0030\u0030\u0033"});
HackHax.push({GrandesLigas: "\u0053\u0075\u0070\u0065\u0072\u0042\u0061\u006c\u006c",GLH2015: "\u0079\u006f\u005f\u0065\u005f\u006c\u0033\u0036"});
HackHax.push({GrandesLigas: "\ud835\udd4d\ud835\uddee\u006e \u2119\ud835\udc52\u0280\u0073\u0131\ud835\udc52",GLH2015: "\u0061\u0067\u0075\u0073\u0074\u0069\u006e\u0061\u006c\u0075\u0063\u0061\u0073\u0031\u0038"});
HackHax.push({GrandesLigas: "\u0043\u0075\u0072\u0075\u0063\u0068\u0065\u0074",GLH2015: "\u0031\u0030\u0031\u0035\u0032\u0039"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0072\u0072\u0069\u006e\u0063\u0068\u0061",GLH2015: "\u0067\u0061\u0072\u0072\u0069\u006e\u0063\u0068\u0061\u0037\u0037\u0037"});
HackHax.push({GrandesLigas: "\u0049\u0061\u006e\u0062\u0069\u0073\u0069\u006f",GLH2015: "\u006d\u0061\u0074\u0075\u0074\u0065\u0032\u0030\u0030\u0035"});
HackHax.push({GrandesLigas: "\u004b\u0061\u0079\u006e",GLH2015: "\u0072\u006f\u006a\u006f\u002e\u0063\u0061\u0070\u006f\u002e\u0031"});
HackHax.push({GrandesLigas: "\u0042\u0041\u004b\u0055\u004e\u0049\u004e",GLH2015: "\u0034\u0031\u0038\u0038\u0038\u0035\u0068\u0061\u0078\u0062\u0061\u006c\u006c"});
HackHax.push({GrandesLigas: "\ud835\udc06\u1d00\u0280\u0280\u0069\u0273\ud835\ude24\u029c\u1d00",GLH2015: "\u0067\u0061\u0072\u0072\u0069\u006e\u0063\u0068\u0061\u0031\u0032\u0031\u0034"});
HackHax.push({GrandesLigas: "\u2605 \ud835\udc01\ud835\udc00\ud835\udc0a\ud835\udc14\ud835\udc0d\ud835\udc08\ud835\udc0d \u2605",GLH2015: "\u0064\u0034\u0031\u0038\u0038\u0038\u0066\u0035"});
HackHax.push({GrandesLigas: "\u0070\u0e04\u00a2\u0ed0\u005f\u0e04\u0e53\u0ed0\u0072\u0ed0\u015e\u0ed0\u005f\ud83c\udf08",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0038\u0039\u0066\u0065\u0064\u0065"});
HackHax.push({GrandesLigas: "\u0041\u006c\u0065\u006a\u0061\u006e\u0064\u0072\u006f",GLH2015: "\u0068\u0061\u0078\u0065\u0072"});
HackHax.push({GrandesLigas: "\u0070\u0061\u0072\u006b",GLH2015: "\u0073\u0072\u0064\u0031\u0030\u0039\u0030\u0072\u0077"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0074\u0068\u0065\u0075\u0073 \u0073\u002e",GLH2015: "\u0031\u0038\u0030\u0034\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0042\u0065\u006e\u006a\u0061\u0043\u005f\u0030\u0032",GLH2015: "\u0062\u0065\u006e\u006a\u0061\u0063\u0061\u0072\u0064\u006f\u007a\u006f"});
HackHax.push({GrandesLigas: "\u0069\u006f",GLH2015: "\u0074\u0075\u006d\u0061\u006d\u0061\u0032\u0032"});
HackHax.push({GrandesLigas: "\ud835\udcd9\u07ce\u1d00\u0274\u0063\u0069\u1d1b\u006f",GLH2015: "\u006a\u0075\u0061\u006e\u0063\u0069\u0074\u006f\u0032\u0030\u0030\u0039"});
HackHax.push({GrandesLigas: "\u004a\u0061\u0070\u0061\u006e",GLH2015: "\u0031\u0032\u0033\u0034\u006a\u0061\u0070\u0061\u006e"});
HackHax.push({GrandesLigas: "\u0052\u006f\u0062\u0065\u0072\u0074 \u0053\u006b\u006f\u0076",GLH2015: "\u0072\u0073\u006b\u006f\u0076\u0032\u0039"});
HackHax.push({GrandesLigas: "\u0053\u0069\u0063\u0061\u0072\u0069\u006f \u0044\u0065\u004d\u0065\u006e\u0074\u0061",GLH2015: "\u0053\u0069\u0063\u0061\u0072\u0069\u006f\u0031\u0030"});
HackHax.push({GrandesLigas: "\u006a\u0061\u006d\u0069\u0072",GLH2015: "\u0031\u0038\u0030\u0034\u0039\u0032"});
HackHax.push({GrandesLigas: "\u0044\u0079\u006c\u0061\u006e",GLH2015: "\u0062\u006f\u0063\u0061\u006a\u0075\u006e\u0069\u006f\u0072\u0073\u0032\u0030\u0030\u0034"});
HackHax.push({GrandesLigas: "\ud835\udcd9\u1d00\u006d\u0069\u0280",GLH2015: "\u0031\u0038\u0030\u0034\u0039\u0032\u0066"});
HackHax.push({GrandesLigas: "\u004e\u0065\u0079\u004d\u0031\u0054\u004f\u006f\u0066\u0069\u0063\u0069\u0061\u006c",GLH2015: "\u006e\u0061\u0074\u0061\u006e\u0061\u0065\u006c\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0050\u0065\u0072\u0069\u0063\u006f\u0074\u0065",GLH2015: "\u0061\u0067\u0075\u0073\u0074\u0069\u006e"});
HackHax.push({GrandesLigas: "\u0077\u0068\u006f\u003f",GLH2015: "\u006f\u006c\u0061\u006b\u0065\u0061\u0073\u0065\u0034\u0035"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0074\u006c",GLH2015: "\u0073\u006f\u0079\u0065\u006c\u006d\u0065\u006a\u006f\u0072\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0053\u0061\u006b\u303d",GLH2015: "\u0044\u0069\u006e\u006f\u0031\u0032\u0033\u0034\u0035\u0036"});
HackHax.push({GrandesLigas: "\u0053\u006f\u006e \u0048\u0065\u0075\u006e\u0067\u002d\u004d\u0069\u006e",GLH2015: "\u0031\u0032\u0033\u0031\u0032\u0033\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0070\u0065\u0064\u0072\u006f",GLH2015: "\u006c\u0069\u006e\u0063\u0065"});
HackHax.push({GrandesLigas: "\u0053\u0065\u0067\u0068\u006f\u006e\u0069\u006f\u271e\u2122",GLH2015: "\u0032\u0035\u0033\u0033\u0036\u0032"});
HackHax.push({GrandesLigas: "\u0061\u0062\u006f\u0075\u0074\u0072\u0069\u006b\u0061",GLH2015: "\u0065\u006c\u0075\u006c\u0074\u0069\u006d\u006f\u0032\u0032"});
HackHax.push({GrandesLigas: "\u006d\u0061\u006e\u1d05\u0072\u0061\u1d0b\u0065",GLH2015: "\u0063\u0061\u007a\u0061\u0064\u006f\u0072\u0031\u0039"});
HackHax.push({GrandesLigas: "\u004d\u0061\u006e\u0069\u0061\u0063",GLH2015: "\u0061\u006c\u0065\u0078\u0069\u0073\u0032\u0030\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0053\u0063\u0069\u0066\u0066\u006f",GLH2015: "\u0054\u0061\u006c\u0061\u006d\u006f\u006e\u0074\u0069\u0031\u0038\u0038\u0039"});
HackHax.push({GrandesLigas: "\u004e\u0065\u0079",GLH2015: "\u0046\u0065\u0072\u006d\u0069\u006e"});
HackHax.push({GrandesLigas: "\u0043\u0040\u0024\u0050\u0045\u0052",GLH2015: "\u0061\u0073\u0065\u0073\u0064\u0065\u006c\u0073\u0075\u0072\u0031\u0033"});
HackHax.push({GrandesLigas: "\u0059\u0065\u004b\u0061",GLH2015: "\u006f\u0072\u0074\u0065\u0067\u0061\u0073\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0047\u0065\u0072\u0073\u006f\u006e",GLH2015: "\u0067\u0032\u0032\u0033\u0033\u0032\u0030\u0033\u0030"});
HackHax.push({GrandesLigas: "\u0050\u006f\u0064\u006f\u006c\u0073\u006b\u0069 \u006c\u006c",GLH2015: "\u006e\u0061\u0030\u0035\u006c\u0075\u0032\u0032"});
HackHax.push({GrandesLigas: "\u006c\u0069\u0072\u0069\u0063\u0073",GLH2015: "\u0065\u0064\u0069\u0066\u0069\u0065\u0072\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0050\u006f\u1d05\u006f\u006c\u0073\u006b\u0069 \u2d4a\u2d4a",GLH2015: "\u0050\u006f\u0064\u006f\u006c\u0073\u006b\u0069 \u006c\u006c"});
HackHax.push({GrandesLigas: "\u004c\u0075\u006b\u0069\u0074\u0061\u0073",GLH2015: "\u0031\u0035\u0034\u0030\u0030\u0032\u0035\u0030\u0034"});
HackHax.push({GrandesLigas: "\u0062\u0072\u007a",GLH2015: "\u0068\u006f\u006c\u0061\u0078\u0064\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u1d1b\u006f\u1d0d",GLH2015: "\u006d\u0061\u0073\u0068\u0061\u006b\u0065"});
HackHax.push({GrandesLigas: "\u0042\u0061\u0069\u0061\u006e\u006f",GLH2015: "\u0061\u0031\u0032\u0031\u0030\u0031\u0039\u0039\u0038"});
HackHax.push({GrandesLigas: "\u004d\u0061\u007a\u007a\u006f\u006c\u0061",GLH2015: "\u0074\u0075\u0076\u0069\u0065\u006a\u0061"});
HackHax.push({GrandesLigas: "\u1d18\u029f\u1d00\u028f\u1d00\u029f\u1d00\u0262\u1d0f",GLH2015: "\u0070\u006c\u0061\u0079\u0069\u0074\u0061\u0037"});
HackHax.push({GrandesLigas: "\u005b\u002e\u002e\u002e\u002e\u002e\u002e\u002e\u005d",GLH2015: "\u0064\u0061\u006e\u0074\u0065 \u0031\u0035\u0036\u0031"});
HackHax.push({GrandesLigas: "\u0068\u0061\u0073\u0062\u006f\u006c",GLH2015: "\u0031\u0035\u0039\u0037\u0035\u0033\u0031\u0032\u0033\u0037\u0038\u0039"});
HackHax.push({GrandesLigas: "\u0052\u006f\u0063\u0069\u006f",GLH2015: "\u0065\u0073\u0070\u0069\u006e\u006f\u0073\u0061"});
HackHax.push({GrandesLigas: "\u006c\u0075\u006b\u0069",GLH2015: "\u0066\u0075\u0074\u0062\u006f\u006c\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0052\u0075\u0069 \u0043\u006f\u0073\u0074\u0061",GLH2015: "\u0073\u0065\u0062\u0061\u0076\u0061\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0052\u006f\u006e\u0061\u006c\u0064\u006f",GLH2015: "\u0076\u0069\u006c\u006c\u0061\u0037\u0034\u0031\u0032"});
HackHax.push({GrandesLigas: "\ud83d\udc8e\u003d\u004d\u0061\u0067\u006e\u0069\u0066\u0069\u0063\u0030\u0032\u0033\u003d\ud83d\udc8e",GLH2015: "\u006d\u0061\u0067\u006e\u0069\u0066\u0069\u0063"});
HackHax.push({GrandesLigas: "\u0045\u0064\u0075 \u004d\u0065\u0067\u0061 \u0021",GLH2015: "\u0047\u0061\u0062\u0072\u0069\u0065\u006c\u0038\u0035"});
HackHax.push({GrandesLigas: "\u006d\u0069\u006e\u0068\u0061",GLH2015: "\u0062\u006f\u0063\u0068\u0069\u006e\u0068\u0061"});
HackHax.push({GrandesLigas: "\ud83d\udc4b\u004d\u00e3\u006f\ud83d\udc4b",GLH2015: "\u0072\u0061\u006d\u006f\u006e\u0038\u0035\u0035\u0033\u0032\u0039\u0032\u0036"});
HackHax.push({GrandesLigas: "\u004e\u0069\u006b\u0065",GLH2015: "\u0043\u0061\u0072\u0074\u0075\u0063\u0068\u0065\u0072\u0061\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0044\u0075\u006b\u0069",GLH2015: "\u006d\u0061\u0072\u0074\u0069\u006e\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004e\u0065\u006f \u0050\u0069\u0073\u0074\u006f\u006c\u0061",GLH2015: "\u004e\u0047\u0041\u0036\u0036\u0037"});
HackHax.push({GrandesLigas: "\u0065\u006b\u0030\u002e\u002d",GLH2015: "\u0076\u0061\u006e\u0063\u0068\u0069\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u004a\u0046\u0051\u0031\u0030",GLH2015: "\u0063\u0065\u006c\u006c\u0070\u0068\u006f\u006e\u0065\u0031\u0034"});
HackHax.push({GrandesLigas: "\u0063\u0072\u006f\u0063\u0072\u0061\u0078\u006b\u0065\u0072",GLH2015: "\u0061\u0072\u0072\u0065\u006c\u006f\u0063\u006f"});
HackHax.push({GrandesLigas: "\ud835\udd72\ud835\udd86\ud835\udd87\ud835\udd8e\ud835\udd8c\ud835\udd94\ud835\udd91 \u06f9",GLH2015: "\u006d\u0061\u006d\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0043\u0280\u1d1c\u028f\ufb00",GLH2015: "\u0063\u0063\u0061\u0073\u0062\u0037\u0061\u006e\u006f\u0073"});
HackHax.push({GrandesLigas: "\u0063\u0061\u0072\u006c\u0069\u0074\u006f\u0073 \u0074\u0065\u0076\u0065\u007a",GLH2015: "\u006c\u006f\u0075\u0063\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0076\u0069",GLH2015: "\u0063\u0068\u0069\u0063\u0068\u0065\u0070\u0072\u006f"});
HackHax.push({GrandesLigas: "\u0064\u0065\u006c\u0061\u0063\u0072\u0075\u007a",GLH2015: "\u006c\u006f\u0075\u0063\u006f\u0035\u0034\u0033"});
HackHax.push({GrandesLigas: "\u0262\u1d00\u0299\u026a\ud835\udc06\ud835\udc0e\ud835\udc0b",GLH2015: "\u0076\u0069\u0074\u006f\u0072\u0031"});
HackHax.push({GrandesLigas: "\u0047\u0041\u0042\u0049\u0047\u004f\u004c\u0024",GLH2015: "\u0076\u0069\u0074\u006f\u0072\u0076\u0069\u0074\u006f\u0072"});
HackHax.push({GrandesLigas: "\u0043\u0072\u006f\u0061\u0074\u006f",GLH2015: "\u0031\u0032\u0033\u0034\u0071\u0077\u0065\u0072"});
HackHax.push({GrandesLigas: "\u0ca0\u005f\u0ca0",GLH2015: "\u006a\u006f\u0061\u0073"});
HackHax.push({GrandesLigas: "\u0053\u0070\u0065\u006e\u0064\u004b\u006f",GLH2015: "\u0068\u006f\u006c\u0061\u0061\u006d\u0069\u0067\u006f\u0073"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0067\u006f \u0076\u0061\u006c\u0064\u0069\u0076\u0069\u0061",GLH2015: "\u0061\u0079\u006d\u0061\u0067\u006f"});
HackHax.push({GrandesLigas: "\u0071\u0065\u0071",GLH2015: "\u006c\u0069\u0063\u0068\u006f\u0032\u0039\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0050\u1d07\u0280\u026a\u1d04\u1d0f\u1d1b\u1d07",GLH2015: "\u0061\u0067\u0075\u0073\u0031\u0034\u0035\u0032"});
HackHax.push({GrandesLigas: "\u0043\u006f\u0072\u0072\u0065\u006e\u0074\u0065",GLH2015: "\u0030\u0035\u0034\u0034\u0070\u006d\u0032\u0030\u0031\u0038"});
HackHax.push({GrandesLigas: "\u0021",GLH2015: "\u006d\u0061\u0074\u0063\u0061\u0070\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u004f\u0072\u0074\u0065\u0067\u0061",GLH2015: "\u0061\u006d\u006e\u0069\u006f\u0074\u0069\u0063\u006f"});
HackHax.push({GrandesLigas: "\u006b\u0061\u0072\u0061\u0062\u0061\u0074\u0069\u0063",GLH2015: "\u0069\u006b\u0065\u0072\u0070\u0061\u0062\u006c\u006f\u0032"});
HackHax.push({GrandesLigas: "\u0070\u0072\u0069\u006e\u0063\u0069\u0070\u0065",GLH2015: "\u006d\u0069\u006e\u006f\u006b\u0069\u0061\u0078\u0064"});
HackHax.push({GrandesLigas: "\u0067\u0061\u0062\u0069\u0067\u0061\u006c",GLH2015: "\u0067\u0061\u0062\u0069\u0067\u006f\u006c\u0031\u0032\u0031\u0034"});
HackHax.push({GrandesLigas: "\u004d\u0061\u006e\u0061\u006f\u0073 \u0055\u0076\u0061",GLH2015: "\u0075\u0076\u0061\u006d\u0061\u006e\u0061\u006f\u0073"});
HackHax.push({GrandesLigas: "\u004c\u0075\u0063\u0061\u0073 \u0048\u006f\u0079\u006f\u0073",GLH2015: "\u0067\u0075\u0069\u0064\u006f\u0031\u0037\u0030\u0033"});
HackHax.push({GrandesLigas: "\u004d\u0069\u006c\u0061\u006e\u0042\u0061\u0072\u006f\u0073",GLH2015: "\u004e\u0065\u006b\u006f\u006b\u0075\u0032\u0030"});
HackHax.push({GrandesLigas: "\u004e\u006f\u0048\u0061\u0061\u0072",GLH2015: "\u0065\u006c\u0064\u0069\u0065\u0067\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004d\u0069\u006c\u006f",GLH2015: "\u006d\u0063\u0031\u0039\u0030\u0033\u0031\u0039\u0039\u0039"});
HackHax.push({GrandesLigas: "\u0050\u0061\u0067\u006e\u0069\u0065\u007a",GLH2015: "\u0067\u0061\u0062\u0072\u0069\u0065\u006c\u0031\u0035"});
HackHax.push({GrandesLigas: "\u004a\u0075\u0065\u0076\u0065\u0073",GLH2015: "\u0061\u0073\u0064\u0061\u0073\u0064\u0061\u0073\u0074\u0072\u006f\u0079\u0065\u0072"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0069\u0063\u0068",GLH2015: "\u0067\u0061\u0073\u0032\u0032\u0039\u0033"});
HackHax.push({GrandesLigas: "\u0044\u006f\u006e\u006e\u0069\u0065 \u0044\u0061\u0072\u006b\u006f",GLH2015: "\u006d\u0063\u0063\u0061\u0063\u006f\u0031\u0032"});
HackHax.push({GrandesLigas: "\u006b\u0069\u006c\u0069\u0061\u006e \u0065\u006d\u0062\u0061\u0070\u00e9",GLH2015: "\u0063\u0063\u0039\u0039"});
HackHax.push({GrandesLigas: "\ud835\udc13\ud835\udc2b\ud835\udc28\ud835\udc32 \ud835\udc01\ud835\udc28\ud835\udc25\ud835\udc2d\ud835\udc28\ud835\udc27",GLH2015: "\u006d\u0030\u0072\u0067\u0075\u0065"});
HackHax.push({GrandesLigas: "\u004d\u0072\u0053\u006e\u0069\u0063\u006b\u0065\u0072",GLH2015: "\u0061\u006c\u006d\u0065\u006c\u006f\u0030\u0035\u0034\u0036"});
HackHax.push({GrandesLigas: "\u0042\u0072\u0069\u0074\u0069\u0073\u0068",GLH2015: "\u0061\u0066\u0061\u0067\u0075\u0073"});
HackHax.push({GrandesLigas: "\u0065\u006c\u005f\u0063\u0068\u0069\u006e\u006f\u002e\u0033\u0031",GLH2015: "\u0065\u006c\u0063\u0068\u0069\u006e\u006f\u0031\u0032"});
HackHax.push({GrandesLigas: "\ud835\uddd9\ud835\uddf2\ud835\uddf1\ud835\uddf2\ud835\uddff\ud835\uddf6\ud835\uddf0\ud835\uddfc \u2022 \u0044\u0072\u004d",GLH2015: "\u0035\u0032\u0038\u0030\u0036\u0038\u0035\u0038"});
HackHax.push({GrandesLigas: "\u006b\u0069\u0072\u0069\u0074\u006f",GLH2015: "\u0073\u0065\u0069\u006c\u0061"});
HackHax.push({GrandesLigas: "\u0047\u0041\u0042\u0049 \u0048\u0041\u0055\u0043\u0048\u0045",GLH2015: "\u004b\u0055\u004b\u0049\u0054\u0041\u0032\u0030\u0030\u0030"});
HackHax.push({GrandesLigas: "\u004a\u1d0f\u0053\u1d07\u0048",GLH2015: "\u0031\u0032\u0033\u0033\u0032\u0031\u0061\u0061"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0074\u006f\u0053\u006f\u0072\u0065\u0074\u0069\u0074\u006f",GLH2015: "\u0054\u006f\u0072\u0069\u006e\u006f\u0046\u0043"});
HackHax.push({GrandesLigas: "\u0045\u0072\u0075\u0064\u0069\u0074\u006f \u00bb \u0058",GLH2015: "\u0048\u0061\u0078\u0062\u0061\u006c\u006c\u0065\u0072\u0075\u0032\u0030\u0031\u0038"});
HackHax.push({GrandesLigas: "\u006d\u0065\u0073\u0069\u0074\u0061",GLH2015: "\u006d\u0065\u0073\u0069\u0074\u0061\u0065\u006c\u006d\u0065\u006a\u006f\u0072"});
HackHax.push({GrandesLigas: "\u0054\u0061\u006e\u006b\u0061\u0072\u0064\u0065\u0063",GLH2015: "\u0063\u0068\u006f\u006b\u006b\u0065\u0031\u0039\u0039\u0038"});
HackHax.push({GrandesLigas: "\u0048\u006f\u006d \u0054\u0061\u006e\u006b\u0073",GLH2015: "\u006d\u0061\u0072\u0069\u006f\u0062\u0072\u006f\u0073\u0031"});
HackHax.push({GrandesLigas: "\u00d0\u006a\u00df\u00f0\u00a2\u0068\u00e5",GLH2015: "\u0062\u0072\u0069\u0073\u0061\u0074\u0065\u0061\u006d\u006f\u0031\u0034"});
HackHax.push({GrandesLigas: "\ud835\ude4e\ud835\ude6a\ud835\ude65\ud835\ude5a\ud835\ude67\ud835\ude09\ud835\ude22\ud835\ude2d\ud835\ude2d",GLH2015: "\u0053\u0050\u0033\u0032"});
HackHax.push({GrandesLigas: "\u006c\u0065\u006e\u0064\u0061\u0072\u0069\u006f\u0068\u0061\u0078",GLH2015: "\u006c\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0038\u0039"});
HackHax.push({GrandesLigas: "\u004c\u006f\u0071\u0075\u0069\u0074\u006f \u0048\u0044",GLH2015: "\u0062\u0069\u007a\u0061\u006e\u0074\u0069\u006e\u0061"});
HackHax.push({GrandesLigas: "\u0044\u0072\u0061\u0063\u006f\u0075\u0031\u0032",GLH2015: "\u0061\u0075\u0064\u0069\u0066\u006f\u006e\u006f\u0031\u0032"});
HackHax.push({GrandesLigas: "\u006c\u0065\u006e\u0064\u0061\u0072\u0072\u0069\u006f\u0068\u0061\u0078",GLH2015: "\u006c\u0065\u006e\u0064\u0061\u0072\u0069\u006f\u0068\u0061\u0078"});
HackHax.push({GrandesLigas: "\u004e\u0055\u0050\u0044\u0045\u0041",GLH2015: "\u004e\u0055\u0050\u0044\u0045\u0041\u0031"});
HackHax.push({GrandesLigas: "\u0046\u0072\u0065\u0064\u0065\u0073",GLH2015: "\u006c\u0061\u0071\u0075\u0065\u0076\u006f\u0073\u0079\u0061\u0073\u0061\u0062\u0065\u0073\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0050\u0065\u0072\u0072\u0069\u0074\u006f \u0042\u0075\u0065\u006e\u0069\u0074\u006f",GLH2015: "\u006c\u0075\u0063\u0068\u0069\u006d\u0062\u006f"});
HackHax.push({GrandesLigas: "\u00be",GLH2015: "\u0031\u0031\u0036\u0032\u0030\u0039\u0039\u0036\u0036\u0037"});
HackHax.push({GrandesLigas: "\u00b7\u0050\u0061\u0075\u006c\u006f \u0044\u0079\u0062\u0061\u006c\u0061\u00b7",GLH2015: "\u006a\u0075\u0061\u0071\u0075\u0069\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0063\u0065\u006f",GLH2015: "\u006d\u0061\u0063\u0065\u006f\u0070\u006c\u0065\u0078"});
HackHax.push({GrandesLigas: "\u0045\u0064\u0075 \u004d\u0065\u0067\u0061 \u0021\u0023\u0031\u0038\u0036\u0034",GLH2015: "\u006d\u0075\u006e\u0064\u006f\u0063\u0061\u006e\u0069\u0062\u0061\u006c"});
HackHax.push({GrandesLigas: "\u0047\u1d00\u0299\u026a\ud835\udc06\ud835\udfce\ud835\udc0b",GLH2015: "\u0066\u0072\u0061\u006e\u0063\u006f\u0031\u0030\u0039\u0038\u0039\u0030\u0031\u0032"});
HackHax.push({GrandesLigas: "\u004e\u0061\u0062\u006f\u2122",GLH2015: "\u004d\u0061\u0072\u0069\u0061\u006e\u0069\u0074\u0061\u0031"});
HackHax.push({GrandesLigas: "\u0054\u0065\u005a\u0075\u0044\u006f",GLH2015: "\u0031\u0034\u0037\u0038\u0035\u0032"});
HackHax.push({GrandesLigas: "\u004d\u006f\u006e\u0074\u006f\u0079\u0061",GLH2015: "\u004d\u006f\u006e\u0074\u006f\u0079\u0061"});
HackHax.push({GrandesLigas: "\u006a\u0065\u0061\u006e",GLH2015: "\u0061\u0073\u0072\u006f\u006d\u0061\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0065\u0075\u0067",GLH2015: "\u0042\u006e\u006a\u006d\u0065\u006e\u0061\u0063\u0030\u0039\u0040\u0031"});
HackHax.push({GrandesLigas: "\u005b\u002e\u002e\u002e\u002e\u005d",GLH2015: "\u0064\u0061\u006e\u0074\u0065 \u0065\u006c  \u006d\u0065\u006a\u006f\u0072"});
HackHax.push({GrandesLigas: "\u0046\u006f\u0072\u0065\u0073\u0074\u0065\u0072",GLH2015: "\u0074\u006f\u006d\u0061\u0073\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0062\u0065\u0063\u006b\u0065\u006e",GLH2015: "\u0069\u006e\u0063\u006f\u0072\u0072\u0065\u0063\u0074\u0061\u0031"});
HackHax.push({GrandesLigas: "\u0047\u0072\u0069\u007a\u0069",GLH2015: "\u006c\u0075\u006e\u0061\u0063\u0068\u006f\u0039"});
HackHax.push({GrandesLigas: "\u0063\u0075\u0063\u0075\u006d\u0075\u0065\u006c\u006f",GLH2015: "\u006d\u0061\u006d\u0061\u0070\u0061\u0070\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0061\u006c\u0063\u0065",GLH2015: "\u0073\u006f\u0079\u0064\u0065\u006c\u0072\u006f\u006a\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0061\u006e\u0067\u0065\u006c\u0066\u006f\u0074\u0032",GLH2015: "\u0032\u0039\u0033\u0032\u0061\u006e\u0067\u0065\u006c"});
HackHax.push({GrandesLigas: "\u0046\u0065\u006c\u0070\u0068\u0069\u0065\u0072",GLH2015: "\u0066\u0065\u006c\u0069\u0070\u0065\u0070\u0065\u0032"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0072\u0074\u0069\u006e\u0065\u0065\u006c",GLH2015: "\u0063\u0072\u0061\u006e\u0062\u0065\u0072\u0072\u0069\u0065\u0031\u0032\u0031\u0030\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0064\u006f\u006d\u0069\u006e\u0069\u0063",GLH2015: "\u0074\u0068\u0069\u0065\u006d"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0062\u0069\u0067\u006f\u006c",GLH2015: "\u0061\u0061\u0061\u0061\u0061\u0031\u0031\u0031\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0050\u0045\u0052\u0052\u0045\u004f \u0053\u0055\u0043\u0049\u004f",GLH2015: "\u0070\u0065\u0072\u0072\u0065\u006f\u0073\u0075\u0063\u0069\u006f"});
HackHax.push({GrandesLigas: "\u0064\u006f\u0075\u0072\u0061\u0064\u006f",GLH2015: "\u006c\u0075\u0069\u007a\u0064\u006f\u0075\u0072\u0061\u0064\u006f\u006d\u0061\u0074\u0068\u0065\u0075\u0073\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0052 \u0075 \u0064 \u0079",GLH2015: "\u0047\u0061\u006c\u006c\u0061\u0072\u0064\u006f"});
HackHax.push({GrandesLigas: "\u004b \u004e\u0061\u0076\u0061\u0073 \u0031\u0034",GLH2015: "\u0043\u006f\u0073\u0063\u0075"});
HackHax.push({GrandesLigas: "\u0046\u0061\u0074\u0069\u0067\u0061",GLH2015: "\u0056\u0069\u0064\u0065\u006c\u0061"});
HackHax.push({GrandesLigas: "\u0045\u006d\u0069\u006c\u0069\u0061\u006e\u006f",GLH2015: "\u0065\u006d\u0069\u0032\u0031"});
HackHax.push({GrandesLigas: "\u0052\u0069\u0075 \u0050\u0061\u0074\u0072\u0069\u0063\u0069\u006f",GLH2015: "\u006d\u0061\u0064\u0065\u0072\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0050\u0069\u0065\u0073\u0065\u006c\u0031\u0033",GLH2015: "\u0063\u0068\u0061\u006e\u0063\u006c\u0065\u0074\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0056\u0061\u006e \u0064\u0065 \u0062\u0065\u0065\u006b\u002e \ud83c\udf40",GLH2015: "\u0073\u0061\u0064\u0066\u0064\u0073\u0066\u0035\u0073\u0064\u0066\u0073\u0064\u0066"}); 
HackHax.push({GrandesLigas: "\u0054\u0049 \u002d \u0065\u006c \u0073\u0069\u0063\u0061\u0072\u0069\u006f \u0041\u006d\u0065\u006c",GLH2015: "\u0054\u006f\u0062\u0069\u0061\u0073\u0032\u0030\u0030\u0031\u0031\u0034"});
HackHax.push({GrandesLigas: "\u0070\u0069\u0072\u0075\u006c\u006f",GLH2015: "\u0043\u0068\u0061\u0063\u0061\u0072\u0069\u0074\u0061\u0038"});
HackHax.push({GrandesLigas: "\u0041\u006e\u0067\u0065\u006c\u0069\u0063\u0069",GLH2015: "\u0062\u0061\u0072\u0063\u0065\u006c\u006f\u006e\u0061\u0065\u006c\u006d\u0061\u0073\u006b\u0061"});
HackHax.push({GrandesLigas: "\u0052\u006f\u0064\u0072\u0079\u0067\u006f",GLH2015: "\u0068\u0061\u0067\u0069\u0032\u0030\u0031\u0035"});
HackHax.push({GrandesLigas: "\u0262\u1d00\u0299\u026a \u029c\u1d00\u1d1c\u1d04\u029c\u1d07",GLH2015: "\u0067\u0061\u0062\u0069\u0068\u0061\u0075\u0063\u0068\u0065"});
HackHax.push({GrandesLigas: "\u0042\u006f\u006f\u006d\u0061\u0067\u0069\u0063\u006f \u2665",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0038\u0039\u0063\u0063"});
HackHax.push({GrandesLigas: "\u2666 \u004b\u0079\u007a\u0072\u006b \u003b \u2666",GLH2015: "\u0065\u006c\u0073\u006d\u0069\u006c\u006f\u0073\u0074\u0065\u0072"});
HackHax.push({GrandesLigas: "\u0064\u006f\u006d\u0065",GLH2015: "\u0031\u0031\u0032\u0033\u0034\u0039\u0033\u0034\u006d"});
HackHax.push({GrandesLigas: "\u0052\u0061\u0073\u0074\u0061\u0042\u0061\u0072\u0062\u0069\u0065",GLH2015: "\u0052\u0069\u0076\u0065\u0072\u0050\u006c\u0061\u0074\u0065\u0031"});
HackHax.push({GrandesLigas: "\u006a\u0061\u0063\u006b\u0065\u0079",GLH2015: "\u0032\u0031\u0030\u0038\u0030\u0031"});
HackHax.push({GrandesLigas: "\u0044\u006f\u006e\u0069\u0074\u0061\u0073",GLH2015: "\u0044\u006f\u006e\u0069\u0074\u0061\u0065\u0056\u0065\u0072\u0069\u0074\u0061\u0065"});
HackHax.push({GrandesLigas: "\ud83d\udc18 \u004d\u03b1\u044f\u0063\u0454\u006c \u0044\u0454\u0455\u03b1\u03b9\u0069\u006c\u006c\u0443 \u26a1",GLH2015: "\u0069\u0076\u0061\u006e\u0065\u006c\u0063\u0061\u0070\u006f"});
HackHax.push({GrandesLigas: "\u0071\u0074",GLH2015: "\u0032\u0030\u0032\u0030\u0071\u0074"});
HackHax.push({GrandesLigas: "\u0065\u0076\u0065\u0072\u0074\u006f\u006e\u0073",GLH2015: "\u0072\u0061\u006d\u0069\u0072\u006f\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0046\u1d00\u1d20\u026a\u1d0f",GLH2015: "\u0031\u0032\u0032\u0032\u0064\u006b"});
HackHax.push({GrandesLigas: "\u004c\u0069\u0074\u0074\u006c\u0065\u0044\u0061\u0072\u006b\u0056\u0069\u0063\u0065",GLH2015: "\u0073\u006f\u006e\u0069\u0063\u0032\u0030\u0031\u0033"});
HackHax.push({GrandesLigas: "\u0052\u1d0f\u0274\u1d00\u029f\u1d05\u1d0f",GLH2015: "\u0074\u0072\u0069\u0070\u006c\u0065\u0070\u0075\u0065\u0072\u006b\u006f\u0031\u0032"});
HackHax.push({GrandesLigas: "\u004f\u1d1b\u1d00\u1d0d\u1d07\u0274\u1d05\u026a",GLH2015: "\u0065\u006d\u0075\u0073\u0065\u006f\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0044\u0072\u0061\u006b\u006f\u006f\u005f\u0031\u0030",GLH2015: "\u0046\u0065\u0072\u006e\u0061\u0067\u006f\u006c\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0056\u0065\u0072\u00f3\u006e \u2757 \u004c\u0065\u0067\u0065\u006e\u0064",GLH2015: "\u0062\u006f\u0074\u0061\u0066\u006f\u0067\u006f"});
HackHax.push({GrandesLigas: "\u0046\u1d00\u0299\u0280\u026a",GLH2015: "\u0066\u0061\u0062\u0072\u0069\u0074\u006f\u0071\u0070"});
HackHax.push({GrandesLigas: "\u0074\u0068\u0069\u0061\u0067\u006f\u0061\u0063\u0075",GLH2015: "\u0034\u0037\u0033\u0030\u0036\u0036\u0030\u0038"});
HackHax.push({GrandesLigas: "\u0070\u0061\u006d\u0065",GLH2015: "\u0039\u0031\u0032\u0031\u0038"});
HackHax.push({GrandesLigas: "\u004b\u006f\u006c\u0061\u0072\u006f\u0076",GLH2015: "\u0032\u0034\u0036\u0037\u0036"});
HackHax.push({GrandesLigas: "\u0042\u0075\u006c\u0067\u0061\u0072\u0069\u0061",GLH2015: "\u0061\u0067\u0075\u0061\u006e\u0074\u0065\u0072\u0069\u0076\u0065\u0072"});
HackHax.push({GrandesLigas: "\u0050\u0069\u0061\u0074\u0074\u0069",GLH2015: "\u006c\u0061\u0061\u0075\u0072\u0065\u0061\u006e\u006f\u0031\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0072\u0072\u0061\u0066\u0061 \u0053\u0061\u006e\u0063\u0068\u0065\u007a",GLH2015: "\u0034\u0032\u0035\u0039\u0036\u0037\u0039\u0039"});
HackHax.push({GrandesLigas: "\u0046\u0061\u0079\u007a\u0075\u006c\u0069\u006e",GLH2015: "\u0031\u0032\u0033\u0074\u006f\u006d\u0069"});
HackHax.push({GrandesLigas: "\u0044\u0065\u0073\u0075\u006b\u0069\u006e\u0068\u006f",GLH2015: "\u0044\u0069\u0061\u0062\u006c\u006f\u0031\u0030"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0074\u0074",GLH2015: "\u003d\u0031\u0032\u0033\u0034\u0035\u0036\u0037"});
HackHax.push({GrandesLigas: "\u0052\u006f\u0064\u0072\u0069\u0067\u006f \u0041\u006d\u0061\u0072\u0061\u006c\u300e\u0049\u0030\u300f",GLH2015: "\u006c\u0061\u0075\u0074\u0061\u0032\u0030\u0030\u0036"});
HackHax.push({GrandesLigas: "\u0068\u0061\u0076\u0065",GLH2015: "\u0068\u0061\u0076\u0065\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0044\u0065\u0061\u004e",GLH2015: "\u0068\u0061\u0078\u0032\u0030\u0033\u0035"});
HackHax.push({GrandesLigas: "\u0070\u0072\u0065\u0064\u0069\u0067\u0065\u0072",GLH2015: "\u0070\u0065\u0072\u0072\u006f"});
HackHax.push({GrandesLigas: "\u006c\u0061\u0075\u0074\u0061",GLH2015: "\u006d\u0061\u0074\u0061\u0064\u006f\u0072"});
HackHax.push({GrandesLigas: "\u0030\u0030\u002d\u0043\u0078\u0073\u0056\u0072",GLH2015: "\u0063\u0065\u0073\u0061\u0072\u002e\u0032\u0038\u0030\u0033"});
HackHax.push({GrandesLigas: "\u1d07\u029f\u1d18\u1d1c\u029f\u0262\u1d00",GLH2015: "\u0050\u0065\u006e\u0065\u006c\u006f\u006c\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004b\u0065\u0069\u0074\u0061",GLH2015: "\u0065\u006c\u0062\u0061\u0072\u0074\u006f\u0062\u0061\u0072\u0074\u0032\u0036"});
HackHax.push({GrandesLigas: "\u0043\u0068\u0061\u006e\u006f\u0021",GLH2015: "\u0048\u006f\u006c\u0061\u004d\u0069\u0056\u0069\u0064\u0061\u0021"});
HackHax.push({GrandesLigas: "\u004c\u1d0f\u1d05\u1d07",GLH2015: "\u004c\u0075\u0063\u0061\u0073\u0031\u0039\u0039\u0038"});
HackHax.push({GrandesLigas: "\u0053\u0048\u0045\u0053\u0048\u004f \u007e",GLH2015: "\u0031\u0033\u0031\u0033\u0031\u0033"});
HackHax.push({GrandesLigas: "\u0063\u007a\u0065\u0072\u0072\u006f",GLH2015: "\u0073\u0065\u0072\u0072\u006f"});
HackHax.push({GrandesLigas: "\u0063\u0061\u006e\u0067\u0065\u006c\u0065",GLH2015: "\u0067\u0069\u0061\u006e\u006c\u0075\u0063\u0061\u0073"});
HackHax.push({GrandesLigas: "\u005a\u006c\u0061\u0074\u0061\u006e\u004b\u0072\u0065\u0073\u0073",GLH2015: "\u006d\u0061\u0078\u0069\u006b\u0061\u0070\u006f\u0031"});
HackHax.push({GrandesLigas: "\u0045\u007a\u0067\u0075\u0061\u0072\u0065\u006e\u007a\u0061\u0024",GLH2015: "\u0032\u0030\u0030\u0035"});
HackHax.push({GrandesLigas: "\u0066\u0065\u0072",GLH2015: "\u0067\u0075\u0073\u0074\u0061\u0076\u006f\u0031\u0037\u0030\u0035"});
HackHax.push({GrandesLigas: "\u004d\u006f\u0074\u006f\u006c\u0069\u006e",GLH2015: "\u004f\u0074\u0072\u0061\u0063\u006f\u006e\u0074\u0072\u0061\u0073\u0065\u006e\u0061\u0039\u0039"});
HackHax.push({GrandesLigas: "\u0067\u0075\u0061\u0072\u0064\u0061\u0062\u0061\u0072\u0072\u006f \u0064\u0065 \u0066\u0061\u006c\u0063\u006f\u006e",GLH2015: "\u0067\u0075\u0061\u0072\u0064\u0061\u0062\u0061\u0072\u0072\u006f"});
HackHax.push({GrandesLigas: "\u0050\u0065\u0070\u0065 \u0047\u0072\u0069\u006c\u006c\u006f",GLH2015: "\u0034\u0033\u0032\u0031"});
HackHax.push({GrandesLigas: "\u0048\u0065\u006c\u0069\u0075\u006d",GLH2015: "\u0043\u0068\u0061\u006d\u006f\u0072\u0072\u006f\u0034\u0038\u0038"});
HackHax.push({GrandesLigas: "\u002d\u0045\u006c \u0053\u0068\u0061\u0061\u0072\u0061\u0077\u0079",GLH2015: "\u0063\u006c\u0061\u0066\u0061\u0063\u006d\u0061\u0072\u0032\u0030\u0030\u0032"});
HackHax.push({GrandesLigas: "\u006d\u0079\u0063\u0072\u0077\u005f\u006d\u0061\u0074\u0069",GLH2015: "\u0051\u0075\u0069\u006e\u0074\u0065\u006c\u0061\u0031\u0033\u0032\u0032"});
HackHax.push({GrandesLigas: "\u004c\u1d00\u0073\u1d04\u1d00 \u1d05\u1d07 \u0054\u026a\u1d0a\u1d0f\u029f\u1d0f",GLH2015: "\u0032\u0039\u0031\u0031\u0030\u0032\u0032\u0035\u0032\u0039\u0067"});
HackHax.push({GrandesLigas: "\u1d07\u1d1c\u0262",GLH2015: "\u0065\u0075\u0067\u0039\u0036"});
HackHax.push({GrandesLigas: "\u0042\u1d0f\u1d0f\u1d0d\u1d00\u0262\u026a\u1d04\u1d0f \u2665",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0037\u0038\u0039\u0063\u0063"});
HackHax.push({GrandesLigas: "\u0052\u0065\u0070\u006c\u0069\u006b",GLH2015: "\u0048\u006f\u006c\u0061\u0061\u006d\u0069\u0067\u006f\u0073\u0078\u0064\u0031\u0032"});
HackHax.push({GrandesLigas: "\u004b\u0072\u0061\u0075\u0073\u0073\u0065\u006e",GLH2015: "\u004b\u0072\u0061\u0075\u0073\u0073\u0065\u006e\u0039\u0039"});
HackHax.push({GrandesLigas: "\u0061\u006c\u0061\u006e",GLH2015: "\u006d\u0061\u0074\u0061\u0064\u006f\u0072\u0039\u0030"});
HackHax.push({GrandesLigas: "\u006a\u006f\u0061\u007a\u0069\u006e",GLH2015: "\u006a\u006f\u0061\u007a\u0069\u006e"});
HackHax.push({GrandesLigas: "\u0053\u0074\u006f\u0069\u0063\u0068\u006b\u006f\u0076",GLH2015: "\u0070\u0069\u0070\u0061\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0041\u0054\u0043\u003b \u004f\u0078\u0069\u002d\u0075\u0077\u0075\u002d",GLH2015: "\u004c\u0061\u0075\u0074\u0069\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0041\u006c\u0069\u006e\u0065 \u0061 \u004c\u0065\u006e\u0064\u0061\u0072\u0069\u0061",GLH2015: "\u0031\u0034\u0037\u0038\u0035\u0032\u0043"});
HackHax.push({GrandesLigas: "\u0077\u0061\u0073\u0073",GLH2015: "\u0067\u006f\u006e\u007a\u0061\u0067\u006f\u006e\u007a\u0061"});
HackHax.push({GrandesLigas: "\u096e\ufeea\u10dd\ufeea\u006c\u00e9\u00f2\u20a6",GLH2015: "\u0038\u0070\u0069\u006b\u0061\u0073\u0053\u0043"});
HackHax.push({GrandesLigas: "\u0061\u0063\u0054 \u0078\u0044",GLH2015: "\u0074\u0072\u0069\u0063\u006f\u006c\u006f\u0072\u0035\u0030"});
HackHax.push({GrandesLigas: "\u0043\u0068\u0069\u0063\u0068\u006f",GLH2015: "\u004d\u0061\u006d\u0075\u0073\u0068\u006b\u0061\u0031\u0033\u0037\u0039"});
HackHax.push({GrandesLigas: "\ud835\udc6a\u029c\u026a\u1d04\u029c\u1d0f",GLH2015: "\u0065\u006d\u0069\u006e\u0065\u006d\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0049\u028b\u03b1\u0273 \u0057\u0069\u0273\u0199\u0282 \u003b\ud83d\udda4\u2654",GLH2015: "\u0069\u0076\u0061\u006e\u0065\u006c\u0063\u0061\u0070\u006f\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0061\u006c\u006f\u006e\u0065\u007a\u0069\u0074\u006f",GLH2015: "\u0041\u006c\u006f\u006e\u0065\u0037\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0043\u0068\u0069\u0043\u0068\u0061\u0072\u0069\u0074\u006f",GLH2015: "\u004e\u0065\u0079\u006d\u0061\u0072\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0057\u0061\u006e\u0063\u0068\u0075\u0070\u0069",GLH2015: "\u0035\u0038\u0037\u0035\u0038\u0037\u0035\u0038\u0037\u0061"});
HackHax.push({GrandesLigas: "\u0063\u0065\u0072\u0076\u0031",GLH2015: "\u0073\u0061\u006c\u0076\u0061\u0064\u006f\u0072\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0052\u026a\u1d1c \u0050\u1d00\u1d1b\u0280\u026a\u1d04\u026a\u1d0f",GLH2015: "\u0035\u0034\u0033\u0032\u0031"});
HackHax.push({GrandesLigas: "\u0053\u0065\u0072\u0070\u0065",GLH2015: "\u0074\u006f\u0074\u006f\u0074\u006f\u0074\u006f"});
HackHax.push({GrandesLigas: "\u0068\u0069\u006b\u0061\u0072\u0075",GLH2015: "\u006e\u0061\u006b\u0061\u006d\u0075\u0072\u0061"});
HackHax.push({GrandesLigas: "\u0041\u006c\u0069\u006e\u0065",GLH2015: "\u0061\u006c\u0069\u006e\u0065\u0031\u0033"});
HackHax.push({GrandesLigas: "\ud83d\udc3a\u0398\u0166\u0394\u004b\u0055\ud83d\udc3a",GLH2015: "\u006c\u0069\u006e\u0064\u006f"});
HackHax.push({GrandesLigas: "\u0047\u0075\u0043\u0061\u0073\u0074\u0061\u006e\u0068\u0061",GLH2015: "\u0030\u0038\u0030\u0032\u0032\u0030\u0030\u0037"});
HackHax.push({GrandesLigas: "\u0280\u1d00\u1d22\u0280",GLH2015: "\u0065\u006d\u006d\u0061\u0032\u0030\u0032\u0030\u0032\u0030"});
HackHax.push({GrandesLigas: "\u004d\u1d0f\u1d1b\u1d0f\u029f\u026a\u0274",GLH2015: "\u004f\u0074\u0072\u0061\u0063\u006f\u006e\u0074\u0072\u0061\u0073\u0065\u006e\u0061"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0062\u006f",GLH2015: "\u0061\u006c\u0062\u006f\u0031\u0039\u0039\u0031"});
HackHax.push({GrandesLigas: "\u0045\u006c \u004d\u0061\u0067\u006f \u0052\u0061\u006d\u00ed\u0072\u0065\u007a",GLH2015: "\u006d\u0061\u0067\u006f\u0073\u0069\u0064\u0065\u0072\u0061\u0079\u0061\u006f\u0031\u0030"});
HackHax.push({GrandesLigas: "\ud835\ude73\ud835\ude84\ud835\ude7a\ud835\ude78",GLH2015: "\u0074\u006f\u0072\u006e\u0065\u006f\u0064\u0065\u0076\u0065\u0072\u0061\u006e\u006f\u0032\u0030\u0031\u0036"});
HackHax.push({GrandesLigas: "\u0052\u006f\u0062\u0065\u0072\u0074 \u004c\u0065\u0077\u0061\u006e\u0064\u006f\u0073\u006b\u0079",GLH2015: "\u0031\u0032\u0033\u0033"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0072\u0063\u0065\u006c",GLH2015: "\u006a\u0065\u0066\u0066\u0065\u0072\u0032\u0030\u0030\u0030"});
HackHax.push({GrandesLigas: "\u004c\u0063\u0069",GLH2015: "\u004c\u0075\u0070\u0069\u0074\u0061\u0031\u0033\u0032\u0033"});
HackHax.push({GrandesLigas: "\u005a\u0065\u006c\u0064\u0072\u0069\u0073",GLH2015: "\u006a\u0075\u006c\u0075\u0064\u0061\u0072\u0069"});
HackHax.push({GrandesLigas: "\u005a\u0065\u006c\u0064\u0072\u0069\u0073 \u003b",GLH2015: "\u006a\u0075\u006c\u0075\u0064\u0061\u0072\u0069\u0030\u0034"});
HackHax.push({GrandesLigas: "\u0070\u0069\u006d\u0070 \u0066\u006c\u0061\u0063\u006f",GLH2015: "\u006a\u0075\u006e\u0069\u006f\u0072"});
HackHax.push({GrandesLigas: "\u0046\u00dc\u0048\u0052\u0045\u0052",GLH2015: "\u006c\u0075\u0063\u0069\u0061\u006e\u006f"});
HackHax.push({GrandesLigas: "\u0048\u0069\u006c\u006f\u0053",GLH2015: "\u0048\u0069\u006c\u006f\u0053\u0031\u0039"});
HackHax.push({GrandesLigas: "\u005a\u0065\u006c\u0064\u0072\u0069\u0073 \u2022 \u0044\u004d",GLH2015: "\u006a\u0075\u006c\u0075\u0064\u0061\u0072\u0069\u0074\u0061"});
HackHax.push({GrandesLigas: "\u0043\u0075\u0063\u006f",GLH2015: "\u0053\u0065\u0074\u0061"});
HackHax.push({GrandesLigas: "\ud83d\udc21\ud835\udcaf\ud835\udc52\ud835\udcc2\ud835\udcc5\ud835\udc5c\u0027\ud83d\udc21",GLH2015: "\u0074\u0065\u006d\u0070\u006f\u0074\u0065\u006d\u0070\u006f\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0061\u0069\u0072\u006c\u0065\u0061\u0074\u0068\u0065\u0072\u0073",GLH2015: "\u0075\u0072\u0069\u0065\u006c\u0032\u0030\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0054\u0055\u0052\u0052\u004f \u004f\u004c\u0049\u0056\u0045\u0052\u0041",GLH2015: "\u0073\u0061\u0062\u0061\u006c\u0065\u0072\u006f\u0033\u0032"});
HackHax.push({GrandesLigas: "\u015c\ud835\udd43\u004f\uff37\u2c60\u1fe9",GLH2015: "\u006c\u0061\u0075\u0074\u0061\u0031\u0037"});
HackHax.push({GrandesLigas: "\u0021\u004e\u0045\u004b\u0048\u004f\u0023\u0041\u0046\u0052\u0049\u0043\u0041",GLH2015: "\u0041\u0046\u0052\u0049\u0043\u0041"});
HackHax.push({GrandesLigas: "\u0054\u0061\u0061\u0069\u006f",GLH2015: "\u0067\u0061\u0062\u0072\u0069\u0065\u006c\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0045\u002e\u0050\u0061\u006c\u0061\u0063\u0069\u006f\u0073",GLH2015: "\u0037\u0038\u0039\u0039\u0038\u0037"});
HackHax.push({GrandesLigas: "\u0064\u0061\u0076\u0069\u0068\u0075\u0062\u006e\u0065\u0072",GLH2015: "\u006d\u0061\u0063\u0061\u0063\u006f\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u004e\u0065\u0065\u0078\u0073",GLH2015: "\u0070\u006f\u0072\u006f\u0074\u006f\u0032\u0030"});
HackHax.push({GrandesLigas: "\u0053\u0069\u0068\u0069\u0072\u006c\u0065",GLH2015: "\u0065\u006c\u0073\u006d\u0069\u006c\u006f\u0073\u0074\u0065\u0072\u0026\u0026"});
HackHax.push({GrandesLigas: "\u004c\u0075\u0069\u0067\u0069\u0033\u0032",GLH2015: "\u0032\u0033\u006c\u0065\u0065\u0030\u0032\u0063\u0068\u006f\u0063\u0030\u0035"});
HackHax.push({GrandesLigas: "\u006b\u006f\u006b\u006f",GLH2015: "\u0031\u0032\u0033\u006c\u006f\u006c"});
HackHax.push({GrandesLigas: "\u0066\u0075\u0063\u006b",GLH2015: "\u006a\u0075\u0073\u0074\u0069\u006e\u0032\u0030\u0030\u0035"});
HackHax.push({GrandesLigas: "\u0046\u03b1\u0063\u03c5\u0057\u0442\u0e23\u0e23\u0e23",GLH2015: "\u0039\u0064\u0065\u0066\u0065\u0062\u0072\u0065\u0072\u006f"});
HackHax.push({GrandesLigas: "\ud835\udc05\u03b1\u0063\u03c5\ud835\udc16\u0442\u0e23\u0e23\u0e23",GLH2015: "\u0066\u0061\u0063\u0075\u006e\u0064\u006f\u0073\u0069\u006c\u0076\u0065\u0072\u0061"});
HackHax.push({GrandesLigas: "\u0042\u0043 \u0052\u0061\u0066\u0066",GLH2015: "\u0074\u0069\u0067\u0072\u0065\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\ud835\udc4d\ud835\udc52\ud835\udc59\ud835\udc51\ud835\udc5f\ud835\udc56\ud835\udc60 \u25cf \ud835\udc37\ud835\udc40",GLH2015: "\u006e\u0061\u0076\u0061\u0072\u0072\u006f"});
HackHax.push({GrandesLigas: "\u006a\u006f\u0075\u004c\u0045",GLH2015: "\u0072\u0079\u0071\u0075\u0065\u006c\u006d\u0065\u0072\u0071\u006d"});
HackHax.push({GrandesLigas: "\u006e\u006f\u0076\u0030\u0072",GLH2015: "\u006e\u0061\u0063\u0068\u006f\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0049\u006e\u0073\u0061",GLH2015: "\u0031\u0037\u0031\u0032\u0033\u0036\u0033\u0039"});
HackHax.push({GrandesLigas: "\u0045\u006c\u004c\u0075\u006b\u0075\u0074\u0065\u006b\u0075",GLH2015: "\u004c\u0075\u006b\u0075\u0074\u0065\u006b\u0075\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0043\u006c\u0065\u006f\u0070\u0061\u0074\u0072\u0061 \u0056\u0049\u0049",GLH2015: "\u006c\u0075\u0063\u0061\u0073\u0031\u0031\u0030\u0032\u0032\u0030\u0030\u0035"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0078\u0069 \u0076\u0065\u006c\u0061\u007a\u0071\u0075\u0065\u007a \u0027",GLH2015: "\u0061\u006c\u0064\u006f\u0073\u0069\u0076\u0069"});
HackHax.push({GrandesLigas: "\u00b0\u007c\u00f6\u005f\u00f6\u007c\u00b0",GLH2015: "\u0041\u004c\u0045\u0058\u0050\u0045\u0052\u0055"});
HackHax.push({GrandesLigas: "\u1d18\u1d00\u0274\u1d05\u1d00\ud83d\udc3c",GLH2015: "\u0050\u0061\u006e\u0064\u0061"});
HackHax.push({GrandesLigas: "\u0054\u0061\u006e\u006f",GLH2015: "\u0070\u0065\u0070\u0065\u006c\u0065\u0070\u0075"});
HackHax.push({GrandesLigas: "\u00df\u20ac\u00df\u20ac\u2502\u2719\u004a\u0055\u0056\u2719",GLH2015: "\u0063\u006c\u0065\u006f\u0070\u0061\u0074\u0072\u0061\u0031\u0034\u0030\u0032"});
HackHax.push({GrandesLigas: "\ud835\udc8c\ud835\udd91\ud835\udd86\ud835\udd93",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0038"});
HackHax.push({GrandesLigas: "\u005a\u0065\u006c\u0065\u0072\u0069\u006f\u0074",GLH2015: "\u0073\u0061\u006e\u0074\u0069\u0030\u0039\u0032\u0036\u0038\u0037\u0039\u0030\u0031"});
HackHax.push({GrandesLigas: "\u0047\u006f\u006e\u00e7\u0061\u006c\u006f",GLH2015: "\u0070\u0075\u0074\u006f\u0032\u0030\u0030\u0035"});
HackHax.push({GrandesLigas: "\u006c\u0065\u0076\u0069",GLH2015: "\u0061\u0063\u006b\u0065\u0072\u006d\u0061\u006e"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0072\u0074\u0069\u006e",GLH2015: "\u0062\u0075\u0073\u0063\u0068\u0065\u0072\u0021\u0021\u0031\u0036\u0032\u0037"});
HackHax.push({GrandesLigas: "\u006d\u0061\u0072\u0074\u0069\u006e\u0031\u0037\u0032\u0032",GLH2015: "\u006d\u0061\u0072\u0074\u0069\u006e\u0021\u0021\u0031\u0036\u0034\u0034"});
HackHax.push({GrandesLigas: "\ud835\udcd0\u0064\u006f\u006c\u0066\u006f\u200b \ud835\udcd6\u0061\u0069\u0063\u0068",GLH2015: "\u0041\u0064\u006f\u006c\u0066\u0069\u0074\u006f"});
HackHax.push({GrandesLigas: "\u0053\u0061\u006e\u0074\u006f\u0073",GLH2015: "\u006d\u0074\u0032\u0037\u0030\u0035\u0030\u0036"});
HackHax.push({GrandesLigas: "\u004c\u0061\u007a\u0061\u006e",GLH2015: "\u006c\u006f\u0073\u0061\u006e\u0064\u0065\u0073"});
HackHax.push({GrandesLigas: "\u0056\u0041\u0052\u0073\u0069\u006c",GLH2015: "\u0041\u0072\u0069\u0065\u006c\u0062\u006f\u0063\u0061\u0031"});
HackHax.push({GrandesLigas: "\u0041\u006e\u0074\u006f\u006e\u0079 \u004d\u0061\u0074\u0068\u0065\u0075\u0073 \u002d\u002d \u0033\u0039",GLH2015: "\u0067\u006f\u006e\u007a\u0061\u0030\u0034"});
HackHax.push({GrandesLigas: "\u0043\u0068\u006f\u006c\u0061\u0073\u0054\u0075\u004d\u0061\u0064\u0072\u0065",GLH2015: "\u0066\u0069\u0066\u0061\u0069\u0076\u0061\u006e"});
HackHax.push({GrandesLigas: "\u004d\u03b1\u03c9\u03b9\u2113\u0454",GLH2015: "\u0074\u006f\u0062\u0069\u0031\u0037\u0034\u0031\u0067\u006f"});
HackHax.push({GrandesLigas: "\u004d\u0069\u00f1\u006f",GLH2015: "\u006d\u0069\u00f1\u006f\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0038\u0039"});
HackHax.push({GrandesLigas: "\u0045\u0078\u0065\u005f\u004b\u0075\u0073\u0068\u0037",GLH2015: "\u0062\u0061\u0072\u0072\u006f\u007a\u0070\u0061\u0073\u006f\u0073\u0035\u0033\u0038\u0032"});
HackHax.push({GrandesLigas: "\u0043\u006c\u0065\u006f\u0070\u0061\u0074\u0072\u0061 \u2166",GLH2015: "\u0073\u0070\u0069\u006e\u006f\u007a\u0061\u0031\u0031\u0030\u0032\u0032\u0030\u0030\u0035"});
HackHax.push({GrandesLigas: "\u004f\u0053\u0046 \u0062\u006c\u0061\u006e\u0064\u0069",GLH2015: "\u0070\u0065\u0075\u0067\u0065\u006f\u0074\u0033\u0030\u0036\u0078\u0072"});
HackHax.push({GrandesLigas: "\u0059\u0075\u004e\u006f\u0033\u0030\u0033",GLH2015: "\u006a\u0061\u0076\u0069\u0065\u0072\u006f\u0061\u0072\u0032\u0030\u0030\u0033"});
HackHax.push({GrandesLigas: "\u0057\u0061\u006e\u0063\u0068\u006f\u0070\u0065 \u0041\u0062\u0069\u006c\u0061",GLH2015: "\u0068\u006f\u006c\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\ud835\udc42\ud835\udc5b\ud835\udc52\u2474\ud835\udc6a\ud835\udc89\ud835\udc90\ud835\udc91\ud835\udc86 \u2d4c\u146b",GLH2015: "\u0070\u0075\u006c\u0070\u0061\u006e\u006f\u0063\u0068\u0061"});
HackHax.push({GrandesLigas: "\ud835\udc0a\u1d0f\u1d0b\u1d0f",GLH2015: "\u0034\u0034\u0035\u0035\u0034\u0030\u0033\u0037\u006c\u0074\u006c\u006b\u006f\u006b\u006f"});
HackHax.push({GrandesLigas: "\u0191\u1d00\u028b\u026a\u1d0f",GLH2015: "\u0031\u0032\u0033\u0064\u006b\u006e\u006f"});
HackHax.push({GrandesLigas: "\u007c\u2020 \u0041\u006c\u0033\u0078\u0069\u0073 \u2020\u007c \u0037",GLH2015: "\u0076\u0069\u0063\u0065\u006e\u0074\u0065"});
HackHax.push({GrandesLigas: "\u0047\u006f\u006c\u0065\u0061\u0064\u006f\u0072 \u006e\u0061\u0074\u006f",GLH2015: "\u0032\u0030\u0031\u0039"});
HackHax.push({GrandesLigas: "\u004c\u0061 \u0054\u0069 \u0047\u006f",GLH2015: "\u0073\u0037\u0069\u006c\u0034\u0036\u0069\u0032"});
HackHax.push({GrandesLigas: "\u004c\u0061\u0074\u0069\u0067\u006f",GLH2015: "\u0043\u0068\u0065\u0073\u0073\u004a\u0075\u0061\u006e\u0058\u0058\u0049\u0049\u0049"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0072\u0073\u0068\u0061\u006c",GLH2015: "\u0034\u0039\u0031\u0031\u0030\u0032\u0032\u0035\u0032\u0039\u0067"});
HackHax.push({GrandesLigas: "\u0052\u0061\u006a\u0061\u0061\u006c",GLH2015: "\u006d\u0069\u006c\u006f\u006e\u0067\u0061\u0032\u0030\u0030"});
HackHax.push({GrandesLigas: "\ud835\udcdb\ud835\udc4e\u1d1b\u026a\u0261\u1d0f",GLH2015: "\u0043\u0068\u0065\u0073\u0073\u004a\u0055\u0041\u004e\u0058\u0049\u0049\u0049"});
HackHax.push({GrandesLigas: "\u004d\u0069\u0073\u0061\u006b\u0069",GLH2015: "\u006d\u0069\u0073\u0061\u006b\u0069"});
HackHax.push({GrandesLigas: "\u0046\u03b1\u0063\u03c5\ud835\udd4e\u0442\u0e23\u0e23\u0e23",GLH2015: "\u0046\u03b1\u0063\u03c5\u0057\u0442\u0e23\u0e23\u0e23"});
HackHax.push({GrandesLigas: "\u0191\u1d00\u1d03\u0280\u026a",GLH2015: "\u0046\u0061\u0062\u0072\u0069\u0031"});
HackHax.push({GrandesLigas: "\u0062\u006f\u006c\u006f\u0078",GLH2015: "\u006a\u0065\u0067\u0075\u0065\u005f"});
HackHax.push({GrandesLigas: "\u0046\u0061\u0062\u0072\u0069\u0057\u0069\u0073\u0074",GLH2015: "\u0057\u0069\u0073\u0074"});
HackHax.push({GrandesLigas: "\u0046\u1d00\u0299\u0280\u026a\u0057\u026a\u0073\u1d1b",GLH2015: "\u0077\u0069\u0073\u0074\u0031"});
HackHax.push({GrandesLigas: "\ud835\udce2\ud835\udcee\ud835\udce5\ud835\udcee",GLH2015: "\u006d\u0061\u0074\u0069\u0061\u0073\u0038\u0035\u0032"});
HackHax.push({GrandesLigas: "\u006a\u0075\u006c\u0069\u0063\u0061\u0069",GLH2015: "\u0031\u0039\u0039\u0038\u0069\u006e\u0064\u0065\u0070\u0065\u006e\u0064\u0069\u0065\u006e\u0074\u0065"});
HackHax.push({GrandesLigas: "\u0063\u0061\u0062\u0065\u006c\u006c\u0061",GLH2015: "\u0063\u0061\u0062\u0065\u0067\u006f\u006c"});
HackHax.push({GrandesLigas: "\u0041\u006e\u0073\u0075 \u0046\u0061\u0074\u0069",GLH2015: "\u0041\u006e\u0073\u0075\u0031\u0046\u0061\u0074\u0069"});
HackHax.push({GrandesLigas: "\ud83d\udc3c\ud835\udc0f\ud835\udc00\ud835\udc0d\ud835\udc03\ud835\udc00\ud83d\udc3c",GLH2015: "\u0034\u0036\u0039\u0032\u0034\u0039\u0036\u0031\u0061"});
HackHax.push({GrandesLigas: "\u0056\u0069\u0074\u0065\u006c \u0054\u006f\u006e\u00e9",GLH2015: "\u0076\u0069\u006c\u0061\u0072\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0038",GLH2015: "\u0076\u0031\u0033\u0031\u0076\u0031\u0033\u0031\u0076\u0031\u0033\u0031\u0076\u0031\u0033\u0031\u0076\u0031\u0033\u0031"});
HackHax.push({GrandesLigas: "\u0053\u0072\u002e\u004b\u0072\u006f\u006f\u0073",GLH2015: "\u0034\u0034\u0036\u0034\u0032\u0034\u0035\u0036"});
HackHax.push({GrandesLigas: "\u0044\u006f\u006e\u0043\u0061\u0073\u0074\u0065\u006c\u006c\u006f",GLH2015: "\u006d\u0064\u0064\u0063\u0079\u0074\u0031\u0038\u0061"});
HackHax.push({GrandesLigas: "\u0065\u006c \u0072\u0065\u006c\u006f\u006a\u0069\u0074\u006f \u0070\u0061\u0074\u006f",GLH2015: "\u0070\u0061\u0074\u006f\u0064\u0065\u006c\u0061\u0067\u0065\u006e\u0074\u0065\u0032\u0031"});
HackHax.push({GrandesLigas: "\u0070\u006e\u006c\u0064\u006f",GLH2015: "\u0039\u0039\u0036\u0033\u0037\u0033\u0031\u0035"});
HackHax.push({GrandesLigas: "\u0043\u006c\u0061\u006e\u0064\u0065\u0073\u0074\u0069\u006e\u006f",GLH2015: "\u0072\u0069\u0076\u0065\u0072\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\ud835\udce2\u2113\ud835\udc1d\ud835\udc94",GLH2015: "\u0074\u006f\u006d\u0079\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004b\u0061\u007a\u0061\u006a\u0069\u0073\u0074\u00e1\u006e",GLH2015: "\u004a\u0075\u006c\u0069\u0061\u006e\u0030\u0035"});
HackHax.push({GrandesLigas: "\u004e\u0061\u0063\u0068\u006f \u0046\u0065\u0072\u006e\u0061\u006e\u0064\u0065\u007a",GLH2015: "\u0068\u006f\u006c\u0061\u006b\u0068\u0061\u0063\u0065\u0031\u0031"});
HackHax.push({GrandesLigas: "\u004a\u0075\u0061\u006e\u0070\u0069\u0069",GLH2015: "\u0068\u0061\u0078\u0062\u0061\u006c\u006c\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004d\u0061\u006e\u0075",GLH2015: "\u0065\u006c\u006b\u0069\u0065\u006c\u006f\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0058\u0061\u0076\u0069",GLH2015: "\u0039\u0031\u0032\u0031\u0038\u0033\u0031"});
HackHax.push({GrandesLigas: "\u0065\u0442\u0069\u0065\u0274\u0274\u0065",GLH2015: "\u007a\u0061\u0068\u0069\u0063\u0061\u006c\u0076\u006f\u0030\u0033"});
HackHax.push({GrandesLigas: "\u0058\u0058\u0058\u0054\u0045\u004e\u0054\u0041\u0043\u0049\u004f\u004e",GLH2015: "\u006e\u0061\u0063\u0068\u0069\u0074\u006f\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0042\u006f\u0062\u0062\u0079 \u0067\u006f\u0061\u006c\u006b\u0065\u0065\u0070\u0065\u0072",GLH2015: "\u0070\u0075\u0063\u0063\u0061\u0062\u0069\u0061"});
HackHax.push({GrandesLigas: "\u007c\u2020 \u0047\u0034\u0072\u0079 \u004d\u0033\u0064\u0033\u006c \u2020\u007c \u0031\u0037",GLH2015: "\u0067\u0061\u0072\u0079\u006d\u0065\u0064\u0065\u006c"});
HackHax.push({GrandesLigas: "\u006c\u0061\u0072\u0072\u0079\u006c\u006f\u0076\u0065\u0073\u006c\u006f\u0076\u0065",GLH2015: "\u006d\u0069\u006d\u0069\u0063\u0039\u0038"});
HackHax.push({GrandesLigas: "\u0050\u006f\u0072\u007a\u0065\u0065",GLH2015: "\u0041\u006c\u0074\u0075\u0072\u0061\u0073\u0031\u0034"});
HackHax.push({GrandesLigas: "\u0046\u006c\u0061\u0074\u0075 \u004c\u006f\u0070\u0065\u007a",GLH2015: "\u0070\u0061\u0063\u0068\u0075\u0070\u0069\u006e\u0063\u0068\u0061\u0031"});
HackHax.push({GrandesLigas: "\u004b\u0061\u0067\u0061\u0073\u0061\u0077\u0061",GLH2015: "\u0030\u0031\u0030\u0035\u0032\u0030\u0030\u0035"});
HackHax.push({GrandesLigas: "\u0070\u0069\u0063\u0068\u0075\u006c\u0061\u0063\u006f\u006e\u0070\u0061\u006e",GLH2015: "\u0072\u0075\u0063\u0061\u006c\u0068\u0075\u0065\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0110\u01b3\u03b2\u039b\u0141\u0394\u301a\u0049\u0030\u301b\u002d\u005f\u227b\ud835\udd1f\ud835\udc87\ud835\udcec\u227a",GLH2015: "\u0034\u0034\u0034\u0032\u0031\u0032\u0037\u0038\u0065\u007a\u0065"});
HackHax.push({GrandesLigas: "\u09ea",GLH2015: "\u0064\u0061\u0064\u0061\u0064\u0061"});
HackHax.push({GrandesLigas: "\u0047\u00f6\u0074\u007a\u0065",GLH2015: "\u0067\u006f\u0074\u007a\u0065\u0031\u0039\u0032\u0030\u0031\u0034"});
HackHax.push({GrandesLigas: "\u0048\u0061\u0064\u0065\u0073",GLH2015: "\u0074\u0072\u0069\u0070\u006c\u0065\u0070\u0075\u0065\u0072\u006b\u006f"});
HackHax.push({GrandesLigas: "\u0067\u006b\u2757",GLH2015: "\u0072\u0069\u0063\u0065\u0062\u0061\u006c\u006c\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0065\u006c \u006d\u00e1\u0067\u0069\u0063\u006f \u0067\u006f\u006e\u007a\u00e1\u006c\u0065\u007a",GLH2015: "\u006c\u0065\u006f\u0063\u0061\u0070\u006f\u0031\u0032\u0033\u0034\u0035"});
HackHax.push({GrandesLigas: "\ud835\udcd0\u2113\u0065\u006a\u0061\u006e\u0221\u0072\u006f",GLH2015: "\u0063\u0061\u006c\u006c\u0065\u006a\u0065\u0072\u006f\u0073\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0075\u0078",GLH2015: "\u0066\u006f\u0075\u0063\u0061\u0075\u006c\u0074\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0065\u006c \u0070\u0069\u0063\u0068\u0069\u0063\u0068\u0069",GLH2015: "\u0033\u0032\u0031\u0034\u0035\u0036"});
HackHax.push({GrandesLigas: "\u004d\u0069\u006f\u006e\u0065\u006c \u004c\u0065\u0073\u0073\u0069",GLH2015: "\u0070\u0069\u006e\u0067\u006f\u006c\u0061\u0073\u0069\u006f\u0031"});
HackHax.push({GrandesLigas: "\u0045\u006c\u0065\u0076\u0065\u006e",GLH2015: "\u0065\u006c\u0065\u0076\u0065\u006e\u0031\u0031"});
HackHax.push({GrandesLigas: "\u1d0d\u0069\u006f\u006e\u0065\u006c \u029f\u0065\u0073\u0073\u0069",GLH2015: "\u0057\u0069\u006e\u0069\u006d\u0061\u006e\u0032"});
HackHax.push({GrandesLigas: "\u0048\u0069\u0072\u0061\u006b\u006f",GLH2015: "\u0045\u006c\u0062\u0069\u006f\u0050\u0061\u0070\u0061"});
HackHax.push({GrandesLigas: "\u0065\u006c\u0061\u0072\u0062\u006f\u006c\u0071\u006c",GLH2015: "\u0063\u0068\u006f\u0063\u006c\u006f\u0031\u0037"});
HackHax.push({GrandesLigas: "\u005a\u0065\u0072\u0069",GLH2015: "\u0050\u0045\u004c\u004f\u0054\u0055\u0044\u004f\u0064\u0065\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0072\u0061\u006e\u0064\u0079",GLH2015: "\u0062\u006f\u0063\u0061\u006a\u0075\u006e\u0069\u006f\u0072\u0073\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0077\u0065\u006e\u0063\u0065\u0073\u006c\u0061\u03c3",GLH2015: "\u0068\u0061\u0078\u0062\u0061\u006c\u006c\u0031\u0030"});
HackHax.push({GrandesLigas: "\u004c\u0065\u0076\u0059\u0061\u0073\u0068\u0069\u006e",GLH2015: "\u0034\u0035\u0036\u0033\u0036\u0039"});
HackHax.push({GrandesLigas: "\u0058\u0061\u0076\u0069\u0031\u0037",GLH2015: "\u0039\u0031\u0032\u0031\u0038\u0033\u0031\u0052\u0062"});
HackHax.push({GrandesLigas: "\u0058\u0061\u0076\u0069\u005f\u0031\u0037",GLH2015: "\u0039\u0031\u0032\u0031\u0038\u0033\u0031\u0030\u0032"});
HackHax.push({GrandesLigas: "\u006c\u0065\u0063\u006f\u0076",GLH2015: "\u0061\u0073\u0064\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0043\u006f\u0072\u006c\u0065\u006f\u006e\u0065\u002e\u002d \u2022 \ud835\udc02\ud835\udc1a\ud835\udc00",GLH2015: "\u006c\u0061\u0073\u0074\u006f\u006e\u0069\u006e\u0061\u0073\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0063\u0068\u0072\u0065\u0059",GLH2015: "\u0062\u0061\u006e\u0066\u0069\u0065\u006c\u0064\u0031\u0036"});
HackHax.push({GrandesLigas: "\u0053\u0061\u0067\u0061\u0069\u007a",GLH2015: "\u002a\u002a\u0073\u006f\u0075\u0073\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0053\u0061\u0067\u0061\u0069\u007a \u0023\u0021\u0033",GLH2015: "\u0052\u006f\u0063\u006b\u0068\u0075\u0064\u0073\u006f\u006e\u0031"});
HackHax.push({GrandesLigas: "\u0031\u0034\u005f\u0058\u0061\u0076\u0069",GLH2015: "\u0063\u0069\u0074\u0072\u006f\u0065\u006e\u0032\u0030\u0036\u0078\u0072"});
HackHax.push({GrandesLigas: "\u0045\u006c\u0047\u0061\u0062\u0069\u0067\u006f\u006c\u0050\u0061\u0072\u0061\u0067\u0075\u0061\u0079\u006f",GLH2015: "\u0045\u006c\u0047\u0061\u0062\u0069\u0067\u006f\u006c"});
HackHax.push({GrandesLigas: "\u004a\u0061\u0076\u0061\u0053\u0063\u0072\u0069\u0070\u0074",GLH2015: "\u0041\u006a\u0041\u0041\u0058\u0035\u0036\u0035"});
HackHax.push({GrandesLigas: "\u004e\u0061\u0072\u0061\u0074",GLH2015: "\u0069\u0076\u0061\u006e\u0073\u0075\u0061\u0072\u0065\u007a\u0039\u0039"});
HackHax.push({GrandesLigas: "\u007c\u03ef \ud835\udcd6\ud835\udc4e\u1d19\u028f \ud835\udcdc\u1d07\u1d05\u1d07\u029f \u03ef\u007c \u2498",GLH2015: "\u0070\u0069\u0074\u0062\u0075\u006c\u006c"});
HackHax.push({GrandesLigas: "\u0047\u0075\u0065\u0064\u0065\u0073 \u0023\u0032\u0033",GLH2015: "\u0062\u0072\u0061\u0076\u0069\u006e\u0031"});
HackHax.push({GrandesLigas: "\u004a\u0075\u0061\u006e \u0046\u0065\u0072\u006e\u0061\u006e\u0064\u006f \u0043\u0061\u0069\u0063\u0065\u0064\u006f",GLH2015: "\u0035\u0034\u0039\u0035\u006d\u0061\u0074\u0079"});
HackHax.push({GrandesLigas: "\u0061\u0067\u0075\u0073\u0074\u0069\u006e",GLH2015: "\u0070\u0065\u0064\u006f\u0073\u0075\u0073\u0062"});
HackHax.push({GrandesLigas: "\u004b\u0065\u0076\u006e\u0061\u006b",GLH2015: "\u004b\u006c\u0061\u006b\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u24b9\u24d0\u24e1\u24da",GLH2015: "\u006c\u0030\u0031\u0030\u0037\u0039\u0039\u0030\u0031"});
HackHax.push({GrandesLigas: "\u0053\u0065\u0072\u0067\u0069\u006f \u0052\u0061\u006d\u006f\u0073",GLH2015: "\u006a\u0075\u006a\u0075\u0079\u0032\u0038\u0035"});
HackHax.push({GrandesLigas: "\u004d\u0065\u0064\u0064\u0075",GLH2015: "\u0072\u0061\u006c\u0076\u0061\u0072\u0065\u007a\u0031"});
HackHax.push({GrandesLigas: "\u0044\u0069\u0065\u0067\u006f \u0043\u006f\u0073\u0074\u0061",GLH2015: "\u0043\u006f\u0070\u0065\u0072\u006e\u0069\u0063\u006f\u0039"});
HackHax.push({GrandesLigas: "\u0073\u0069\u006d\u0065\u0063 \u0073\u0072\u0073",GLH2015: "\u0062\u0072\u0069\u0061\u006e\u0039\u0039\u0030\u0038"});
HackHax.push({GrandesLigas: "\u0072\u0075\u006e\u0069",GLH2015: "\u0072\u006f\u006f\u006e\u0065\u0079\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0038\u002e",GLH2015: "\u0064\u0075\u0073\u006b\u0074\u0069\u006c\u006c\u0064\u0061\u0077\u006e"});
HackHax.push({GrandesLigas: "\u0064\u0061\u0072\u0074\u0068\u0065\u0073 \u0065\u006c \u0069\u006c\u0075\u006d\u0069\u006e\u0061\u0064\u006f",GLH2015: "\u0065\u006c\u006d\u0065\u006a\u006f\u0072\u0064\u0065\u0074\u006f\u0064\u006f\u0073"});
HackHax.push({GrandesLigas: "\u0042\u1d00\u0280\u1d0d\u1d07\u0274\u026a\u1d00",GLH2015: "\u0061\u006a\u0061\u0061\u0078"});
HackHax.push({GrandesLigas: "\u0077\u0061\u006c\u006c\u0073",GLH2015: "\u0076\u0069\u0063\u0065\u0063\u0068\u0065\u0074\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0050\u0061\u0063\u006f \u0041\u006d\u006f\u0072\u006f\u0073\u006f",GLH2015: "\u004d\u0069\u006e\u0065\u0063\u0072\u0061\u0066\u0074\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0043\u0041\u0056\u0049\u0047\u004f\u004c",GLH2015: "\u0040\u0052\u006f\u006a\u0069\u006e\u0065\u0067\u0072\u006f\u0063\u0061\u006d\u0070\u0065\u006f\u006e\u0030\u0034"});
HackHax.push({GrandesLigas: "\ud835\ude42\u1d00\u0280\u0280\u026a\u0274\u1d04\u029c\u1d00",GLH2015: "\u0041\u0063\u0075\u0061\u0072\u0069\u006f\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0066\u0072\u0065\u006e\u006b\u0069\u0065 \u0064\u0065 \u004a\u006f\u006e\u0067",GLH2015: "\u0031\u0031\u0036\u0038\u0035\u0034\u0034\u0039\u0033\u0032\u006a\u0061"});
HackHax.push({GrandesLigas: "\u0048\u03b1\u007a\u03b1\u0280\u1d05",GLH2015: "\u0069\u006d\u0069\u006e\u0074\u0068\u0065\u0062\u0061\u006e\u0064\u0031"});
HackHax.push({GrandesLigas: "\u271e\u004d\u0061\u0072\u0074\u0069\u006e \u0053\u0061\u0072\u0072\u0061\u0066\u0069\u006f\u0072\u0065 \u0038 \u00ae \ud83d\udc51",GLH2015: "\u0049\u006e\u0074\u0065\u0072\u006e\u0061\u0063\u0069\u006f\u006e\u0061\u006c"});
HackHax.push({GrandesLigas: "\u0047\u0054\u007c\u0044\u0041\u004e\u0030\u004e\u0049\u004e\u0048\u004f",GLH2015: "\u0068\u0061\u0072\u0074\u006d\u0061\u006e\u006e\u0030\u0035"});
HackHax.push({GrandesLigas: "\u0043\u0061\u007a\u0061\u0072\u0065\u0073\u0031\u0030",GLH2015: "\u0036\u0034\u0031\u0030\u0074\u0072\u0065\u007a\u0065"});
HackHax.push({GrandesLigas: "\u0042\u0065\u0074\u006f \u0042\u006f\u006c\u006f\u0067\u006e\u0061",GLH2015: "\u0064\u0065\u006e\u0061\u007a\u0069\u006a\u0075\u0061\u0073\u006a\u0075\u0061\u0073"});
HackHax.push({GrandesLigas: "\u0057\u0061\u006e\u002d\u0042\u0069\u0073\u0073\u0061\u006b\u0061",GLH2015: "\u0031\u0032\u0033\u0033\u0032\u0031\u0031\u0033\u0032"});
HackHax.push({GrandesLigas: "\u0047\u004f\u0052\u0044\u0049\u0054\u004f",GLH2015: "\u0074\u0061\u0074\u006f\u0030\u0037"});
HackHax.push({GrandesLigas: "\u1d33\u1d3c\u1d3f\u1d30\u1d35\u1d40\u1d3c",GLH2015: "\u0063\u006c\u0061\u0075\u0064\u0069\u006f\u0030\u0037"});
HackHax.push({GrandesLigas: "\u004e\u0065\u0067\u0072\u006f",GLH2015: "\u0065\u006c\u006e\u0065\u0072\u0067\u0072\u006f\u0078\u0044"});
HackHax.push({GrandesLigas: "\u0070\u0065\u006e\u0065 \u0065\u0072\u0065\u0063\u0074\u006f",GLH2015: "\u0043\u0068\u0065\u006c\u0073\u0065\u0061\u0032\u0034\u0068\u0061\u0078"});
HackHax.push({GrandesLigas: "\u0046\u0069\u006c\u0069\u004d\u0061\u006e",GLH2015: "\u0057\u0045\u0052\u0041\u0050\u004f\u0054"});
HackHax.push({GrandesLigas: "\u0044\u0065 \u0041\u0072\u0072\u0061\u0073\u0063\u0061\u0065\u0074\u0061",GLH2015: "\u0066\u006f\u0072\u006d\u0075\u006c\u0061\u0032"});
HackHax.push({GrandesLigas: "\u006e\u0065\u006f\u0078",GLH2015: "\u0065\u0072\u0069\u0063\u0032\u0030\u0030\u0036"});
HackHax.push({GrandesLigas: "\u004f\u0070\u0073\u0061",GLH2015: "\u006f\u0070\u0073\u0061\u0032\u0035\u0030\u0033\u0037\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004f\u1d18\ud835\udcfc\u1d00",GLH2015: "\u0072\u0061\u006d\u0069\u0072\u006f\u0032\u0035\u0030\u0033\u0037\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0043\u0065\u0063\u0069\u006c\u0069\u006f\u0044\u006f\u006d\u0069\u006e\u0067\u0075\u0065\u007a",GLH2015: "\u006d\u006d\u006d\u0033\u0033\u0033\u006f\u006c\u0065"});
HackHax.push({GrandesLigas: "\u0049\u0073\u0070\u0049",GLH2015: "\u0067\u0061\u0074\u006f\u0074\u0069\u0067\u0072\u0065"});
HackHax.push({GrandesLigas: "\u0046\u0072\u0061\u006e\u006b \u004c\u0061\u006d\u0070\u0061\u0072\u0064 \u00b7\u003f\u00bf\u00b7",GLH2015: "\u0031\u0030\u0033\u0030\u0035\u0030\u0037\u0030"});
HackHax.push({GrandesLigas: "\ud835\udcab\u1d00\u1d04\u1d0f \ud835\udc9c\u1d0d\u1d0f\u0280\u1d0f\u0073\u1d0f",GLH2015: "\u0077\u0065\u006c\u006d\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0074\u0061\u0078",GLH2015: "\u0031\u0035\u0036\u0031"});
HackHax.push({GrandesLigas: "\u2571\u0052\u0061\u0063\u006b\u0073\u006f\u2572",GLH2015: "\u006e\u0069\u0063\u006f\u0072\u006f\u006a\u0061\u0073\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0454\u006c\u005f\u0454\u0e20\u007a\u0e4f",GLH2015: "\u0071\u0077\u0065\u0072\u0074\u0079\u0031\u0032\u0033\u0061\u0062\u0063"});
HackHax.push({GrandesLigas: "\ud835\udc39\ud835\udc4e\ud835\udc60\ud835\udc61\ud835\udc52\ud835\udc5f \u002e \ud835\udc65",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0038\u0079\u0074"});
HackHax.push({GrandesLigas: "\u006b\u006f\u0074\u006f",GLH2015: "\u006e\u0031\u006e\u0035\u006e\u0038\u006e\u0039\u006e\u0038"});
HackHax.push({GrandesLigas: "\u007c \u004b\u006f\u0072\u0063\u0068\u006f \u007c",GLH2015: "\u0074\u006f\u0072\u0074\u0061\u0064\u0065\u0061\u0072\u0072\u006f\u007a\u0030\u0032"});
HackHax.push({GrandesLigas: "\ud835\udce2\u1d00\ud835\udc5b\u1d05\ud835\udcfc",GLH2015: "\u0073\u0061\u006e\u0064\u0073\u0039\u0038\u0037\u0036\u0035\u0034\u0033\u0032\u0031"});
HackHax.push({GrandesLigas: "\u0043\u0061\u0072\u006c\u0069\u0074\u006f\u0073",GLH2015: "\u006a\u0069\u0072\u006f\u0065\u006e\u0074\u0065\u0072\u006f"});
HackHax.push({GrandesLigas: "\u0048\u1d00\u1d22\u1d00\u0280\u1d05",GLH2015: "\u0049\u006d\u0069\u006e\u0074\u0068\u0065\u0062\u0061\u006e\u0064\u0031\u0031"});
HackHax.push({GrandesLigas: "\u005b \u0067\u006f\u0064 \u005d \u0068\u0065\u006e",GLH2015: "\u0039\u0039\u0035\u0031\u0038\u0035\u0034\u0032\u0032"});
HackHax.push({GrandesLigas: "\u0058\u0071\u0053\u0049",GLH2015: "\u0031\u0032\u0033\u0073\u006c"});
HackHax.push({GrandesLigas: "\u004e\u00e3\u006f \u0053\u0065\u0069 \u004a\u006f\u0067\u0061\u0072",GLH2015: "\u0040\u0047\u0061\u0062\u0072\u0069\u0065\u006c\u0031\u0033"});
HackHax.push({GrandesLigas: "\u004a\u006f\u0063\u006b\u0065\u0072\u0076\u0069",GLH2015: "\u0043\u0061\u0072\u0070\u0031\u0030"});
HackHax.push({GrandesLigas: "\u004c\u0049\u0043\u0048\u0049 \u0041\u0052\u004d\u0041\u004e\u0049",GLH2015: "\u0050\u0052\u004f\u0042\u0052\u004f"});
HackHax.push({GrandesLigas: "\u0052\u0061\u006d\u0069",GLH2015: "\u0072\u006f\u006b\u006f\u0063\u0068\u0069\u0076\u0061\u0079\u006c\u0069\u006e\u0064\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0048\u0069\u0070\u0065\u0072\u0066\u0072\u0061\u006e\u0063\u006f",GLH2015: "\u0066\u0072\u0061\u006e\u006b\u0065\u0074\u006f\u0073\u0075\u0070\u0065\u0072\u0030\u0032"});
HackHax.push({GrandesLigas: "\u0045\u004c \u0047\u004f\u0052\u0044\u0049\u0054\u004f \u0044\u0045\u004c \u0041\u0052\u0043\u004f",GLH2015: "\u0068\u006f\u006c\u0061\u006a\u0061\u006a\u0061"});
HackHax.push({GrandesLigas: "\u0056\u0069\u0063\u0074\u006f\u0072\u0079",GLH2015: "\u0068\u0061\u0078\u0062\u0061\u006c\u006c\u006c\u006f\u006c"});
HackHax.push({GrandesLigas: "\u271e\u2133\ud835\ude22\ud835\ude33\ud835\ude35\ud835\ude2a\ud835\ude2f \ud835\udc46\ud835\ude22\ud835\ude33\ud835\ude33\ud835\ude22\ud835\ude27\ud835\ude2a\ud835\ude30\ud835\ude33\ud835\ude26 \u0038 \u00ae \ud83d\udc51",GLH2015: "\u0042\u0061\u0072\u0063\u0065\u006c\u006f\u006e\u0061"});
HackHax.push({GrandesLigas: "\u0074\u0072\u0061\u0070\u0069\u0074\u006f \u0062\u0061\u0072\u006f\u0076\u0065\u0072\u006f",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0074\u0074"});
HackHax.push({GrandesLigas: "\u0067\u006f\u0074\u007a\u0065\u0027",GLH2015: "\u0063\u006f\u006c\u006f\u0063\u006f\u006c\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u210b\u1d07\u0280\u1d04\u1d1c\u029f\u1d07\u0073",GLH2015: "\u0067\u0061\u0072\u0063\u0069\u0061\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0042\u0065\u0072\u0067\u006b\u0061\u006d\u0070",GLH2015: "\u0062\u0069\u006f\u0068\u0061\u007a\u0061\u0072\u0064"});
HackHax.push({GrandesLigas: "\u0045\u004c \u004b\u0041\u0049\u0053\u0045\u0052",GLH2015: "\u0078\u0064\u0032\u0033\u0034\u0035\u0036"});
HackHax.push({GrandesLigas: "\ud835\udd3c\ud835\udd43 \ud835\udd42\ud835\udd38\ud835\udd40\ud835\udd4a\ud835\udd3c\u211d",GLH2015: "\u006e\u0061\u0063\u0068\u0075\u0075\u006c\u0061"});
HackHax.push({GrandesLigas: "\u0045\u006c \u0052\u0075\u0073\u006f \u0052\u006f\u0064\u0072\u0069\u0067\u0075\u0065\u007a",GLH2015: "\u0068\u006f\u006c\u0061\u006a\u0061\u006a\u0061\u006a\u0061"});
HackHax.push({GrandesLigas: "\u0065\u006c \u004b\u00e1\u0069\u0073\u0065\u0072",GLH2015: "\u006b\u0061\u006b\u0061\u0069\u0073\u0065\u0072"});
HackHax.push({GrandesLigas: "\u004b\u0065\u0076\u0069\u006e\u0044\u0065\u0042\u0072\u0075\u0079\u006e\u0065",GLH2015: "\u0061\u006c\u006f\u0070\u006f\u006c\u0069\u0063\u0069\u0061"});
HackHax.push({GrandesLigas: "\u0077\u006f\u0062\u0069",GLH2015: "\u006d\u0061\u0074\u0069\u006d\u0061\u0074\u0069\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004d\u0072\u002e\u0043\u006f\u006c\u006c\u0069\u0065 \u004c\u0054\u0048\u0043",GLH2015: "\u004d\u0072\u0043\u006f\u006c\u006c\u0069\u0065"});
HackHax.push({GrandesLigas: "\u004d\u0280\u0043\u1d0f\u029f\u029f\u026a\u1d07 \ud835\udc0b\ud835\udc13\ud835\udc07\ud835\udc02",GLH2015: "\u006d\u0072\u0064\u0072\u006f\u0067\u0061"});
HackHax.push({GrandesLigas: "\ud835\udcd5\u002e \ud835\udcd3\u1d07 \ud835\udcd9\u1d0f\u0274\u0262",GLH2015: "\u0035\u0034\u0031\u0031\u0033\u0036\u0033\u0037\u0037\u0038\u0030\u0039"});
HackHax.push({GrandesLigas: "\u0053\u0039\u0053",GLH2015: "\u0073\u0065\u0072\u0067\u0069\u006f\u0032\u0030\u0031\u0036"});
HackHax.push({GrandesLigas: "\u00dc\u007a\u0069\u006c",GLH2015: "\u004d\u0061\u0072\u0074\u0069\u006e\u0038\u0039"});
HackHax.push({GrandesLigas: "\u0066\u006c\u0065\u0078\u0078",GLH2015: "\u0042\u0061\u006e\u0066\u0069\u0065\u006c\u0064\u0039"});
HackHax.push({GrandesLigas: "\u0191\u026a\u1d05\u1d07\u1d0f",GLH2015: "\u0072\u0075\u0073\u0069\u006f\u0038\u0030\u006c\u006f\u0078"});
HackHax.push({GrandesLigas: "\u0043\u0068\u0061\u0072\u006c\u0065\u0073",GLH2015: "\u0063\u0068\u0061\u0072\u006c\u0065"});
HackHax.push({GrandesLigas: "\u0061\u006e\u0074\u0069",GLH2015: "\u004a\u006f\u0072\u0064\u0061\u006e\u0033\u0030\u0031\u0039\u0030\u0039"});
HackHax.push({GrandesLigas: "\u0052\u0069\u0063\u0061\u0072\u0064\u006f\u0041\u0072\u006a\u006f\u006e\u0061",GLH2015: "\u006e\u006f\u0073\u0065\u0063\u006f\u006d\u006f\u0065\u0073\u0031"});
HackHax.push({GrandesLigas: "\u0054\u0072\u0065\u006e\u0074 \u0041\u006c\u0065\u0078\u0061\u006e\u0064\u0065\u0072\u002d\u0041\u0072\u006e\u006f\u006c\u0064",GLH2015: "\u0043\u0061\u0073\u006c\u0061\u0031\u0039\u0030\u0038"});
HackHax.push({GrandesLigas: "\u0070\u0070 \u0073\u0061\u006e\u0064",GLH2015: "\u0034\u0034\u0035\u0031\u0034\u0033\u0031\u0031\u006a\u0065\u0074\u0061"});
HackHax.push({GrandesLigas: "\u004e\u006f\u006f\u0062\u20a2\u0066\u007c\u0053\u0072\u0047\u0061\u006c\u0069\u006e\u0068\u0061\u0056\u006f\u0061\u0064\u006f\u0072\u0061\ud83d\udc14",GLH2015: "\u0054\u0065\u006c\u0065\u0066\u006f\u006e\u0065\u0032\u0030\u0033"});
HackHax.push({GrandesLigas: "\u0043\u0048\u0061\u0077\u0069\u004e",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0061"});
HackHax.push({GrandesLigas: "\u0053\u0061\u0067\u0061\u0072\u006f",GLH2015: "\u0031\u0031\u0030\u0037\u0061\u006e\u0064\u0079"});
HackHax.push({GrandesLigas: "\u004a\u006f\u006b\u0065\u0072",GLH2015: "\u006e\u0061\u0063\u0069\u006f\u006e\u0061\u006c\u002e\u0030\u0039"});
HackHax.push({GrandesLigas: "\ud835\udcdc\u026a\u0274\u0303\u1d0f",GLH2015: "\u0034\u0039\u0032\u0032\u0037\u0033\u0030"});
HackHax.push({GrandesLigas: "\u0061\u0072\u006b",GLH2015: "\u0035\u0031\u0030\u0037\u0033\u006d\u006f\u006e\u0063\u0068\u0069"});
HackHax.push({GrandesLigas: "\u004d\u0061\u006e\u0075\u0078\u0058",GLH2015: "\u0032\u0032\u0031\u0038\u0030\u0032\u0031\u0031\u0070\u0070"});
HackHax.push({GrandesLigas: "\u0045\u006c \u004d\u0061\u00f1\u0061\u006e\u0065\u0072\u006f",GLH2015: "\u0032\u0033\u0030\u0035\u0030\u0031"});
HackHax.push({GrandesLigas: "\u0076\u0061\u006c\u0065\u006e\u0074\u0069\u006e\u0056\u0054",GLH2015: "\u0066\u0061\u0063\u0075\u0061\u006e\u0067\u0069\u0065\u0039"});
HackHax.push({GrandesLigas: "\u004f\u0062\u0069\u002d\u0057\u0061\u006e \u004a\u0065\u0073\u00fa\u0073",GLH2015: "\u0062\u006f\u0063\u0061\u006d\u006f\u0072\u0069\u0073\u0074\u0065\u0065\u006e\u006d\u0061\u0064\u0072\u0069\u0064"});
HackHax.push({GrandesLigas: "\u0052\u0065\u0074\u0068\u006c\u007a\u0065 \u004c\u005a",GLH2015: "\u006d\u0069\u006c\u0072\u0061\u0079\u0069\u0074\u0061\u0073"});
HackHax.push({GrandesLigas: "\u004f\u0052\u0055\u0047\u0041",GLH2015: "\u004f\u0052\u0055\u0047\u0041"});
HackHax.push({GrandesLigas: "\u0045\u0064\u0067\u0061\u0072 \u0044\u0061\u0076\u0069\u0064\u0073",GLH2015: "\u0061\u0073\u0072\u006f\u006d\u0061\u0033"});
HackHax.push({GrandesLigas: "\u0061",GLH2015: "\u0061\u006e\u0064\u0072\u0065\u0073\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0064\u006f\u0075\u0067\u006c\u0061\u0073",GLH2015: "\u0061\u006e\u0061\u006e\u0064\u0061\u0033\u0033"});
HackHax.push({GrandesLigas: "\u0073\u0065\u0065\u0062\u0061\u006a\u0061\u006a",GLH2015: "\u0031\u0031\u006a\u0075\u006c\u0039\u0039"});
HackHax.push({GrandesLigas: "\u004d\u0069\u0073\u0074\u0065\u0072\u0069\u006f\u0073\u006f",GLH2015: "\u006d\u0061\u006c\u0064\u0069\u006e\u0069"});
HackHax.push({GrandesLigas: "\u0043\u0072\u0065\u006d\u0061",GLH2015: "\u0064\u0065\u0073\u0074\u0069\u006e\u0079\u0033\u0032"});
HackHax.push({GrandesLigas: "\u0049\u0073\u029c\u026a\u1d0b\u1d00\u1d21\u1d00",GLH2015: "\u0069\u0067\u006e\u0069\u0061\u0072\u0069\u0073\u0074\u0069"});
HackHax.push({GrandesLigas: "\ud835\udcd5\u1d07\u029f\u026a \ud835\udcdd\u1d00\u1d04\u026a\u1d0f\u0274\u1d00\u029f\u200b",GLH2015: "\u006e\u0061\u0063\u0069\u006f\u006e\u0061\u006c\u0072\u006f\u006f\u006d"});
HackHax.push({GrandesLigas: "\u004e\u0069\u0063\u006f \u004c\u006f\u0064\u0065\u0069\u0072\u006f",GLH2015: "\u0061\u0064\u0069\u0064\u0061\u0073"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0072\u0061\u0064\u006f\u006e\u0061\u0045\u0052\u004b",GLH2015: "\u0070\u0061\u0074\u006f\u0063\u0061\u0070\u006f\u0031\u0032"});
HackHax.push({GrandesLigas: "\u004b\u0065\u0076\u0069\u006e\u0044\u0065\u0042\u0072\u0075\u0079\u006e\u0065 \u0053\u0055\u0054",GLH2015: "\u0063\u0039\u0030"});
HackHax.push({GrandesLigas: "\u0043\u0061\u0074\u0061 \u0044\u00ed\u0061\u007a",GLH2015: "\u004e\u006f\u0072\u006d\u0061\u006c\u0032"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0072\u0079\u004d\u0065\u0064\u0065\u006c\u0031\u0037",GLH2015: "\u0076\u0061\u006c\u0065\u006d\u0061\u0074\u0069\u0061\u0073\u0031"});
HackHax.push({GrandesLigas: "\u0070\u0061\u006e\u0063\u0068\u0075\u006c\u006f",GLH2015: "\u0072\u006f\u0063\u006b\u0031\u0039\u0039\u0039\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0299\u1d00\u1d1b\u026a\u0073\u1d1b\u1d1c\u1d1b\u1d00 \ud835\ude9f\ud835\ude8f",GLH2015: "\u0062\u0061\u0074\u0069\u0073\u0074\u0075\u0074\u0061\u0068\u0061\u0078"});
HackHax.push({GrandesLigas: "\ud835\udce1\u1d0f\u1d05\u0280\u026a \ud835\udcd3\u1d07 \ud835\udcdf\u1d00\u1d1c\u029f",GLH2015: "\u0032\u0037\u0030\u0033\u0062"});
HackHax.push({GrandesLigas: "\u211b\u006f\u1d05\u0280\u0069 \ud835\udc9f\u1d07 \ud835\udcab\u1d00\u0075\u029f\u200b",GLH2015: "\u0032\u0037\u0030\u0033\u0062\u0061\u006e\u0066\u0069\u0065\u006c\u0064"});
HackHax.push({GrandesLigas: "\ud835\udc39\ud835\udc4e\ud835\udc60\ud835\udc61\ud835\udc52\ud835\udc5f \u002e\ud835\udce7",GLH2015: "\u0072\u006f\u0073\u0073\u006f\u006e\u0065\u0072\u006f\u0073"});
HackHax.push({GrandesLigas: "\u004e\u0061\u0078\u006f\u0070\u0072\u0065\u006e\u006f",GLH2015: "\u006b\u0065\u0076\u0069\u006e\u0031\u0032\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0050\u0061\u0075\u006c\u0069\u006e\u0068\u006f",GLH2015: "\u0063\u0061\u006e\u0031\u0032\u0033\u0033\u0032\u0031"});
HackHax.push({GrandesLigas: "\u0062\u0075\u006f\u006e\u0061\u006e\u006f\u0074\u0074\u0065",GLH2015: "\u0072\u0069\u0076\u0065\u0072\u0063\u0061\u006d\u0070\u0065\u006f\u006e\u0033\u0033"});
HackHax.push({GrandesLigas: "\u0052\u006f\u006e\u0061\u006c\u0064\u0069\u006e\u0068\u006f",GLH2015: "\u0074\u0065\u006e\u0069\u0073\u006f\u006e\u006a\u006f\u0073\u0065"});
HackHax.push({GrandesLigas: "\u0052\u1d0f\u0274\u1d00\u029f\u1d05\u026a\u0274\u029c\u1d0f",GLH2015: "\u0052\u006f\u006e\u0061\u006c\u0064\u0069\u006e\u0068\u006f"});
HackHax.push({GrandesLigas: "\u0035",GLH2015: "\u0061\u006c\u0065\u006a\u0061\u006e\u0064\u0072\u006f\u0064\u0061\u006e\u0069\u0065\u006c\u0072\u006f\u006c\u0064\u0061\u006e"});
HackHax.push({GrandesLigas: "\ud835\udcd1\u1d07\u1d1b\u1d0f \ud835\udcd1\u1d0f\u029f\u1d0f\u0262\u0274\u1d00",GLH2015: "\u006a\u0075\u0061\u0073\u006a\u0075\u0061\u0073\u006c\u006f\u006c\u0078\u0064"});
HackHax.push({GrandesLigas: "\u004a\u006f\u0074\u0061\u0043\u0065\u0021",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0036\u0037"});
HackHax.push({GrandesLigas: "\u004a\u0061\u006e \u004f\u0062\u006c\u0061\u006b",GLH2015: "\u0068\u0061\u0078\u006c\u006f\u006d\u0065\u006a\u006f\u0072"});
HackHax.push({GrandesLigas: "\u0043\u006f\u0072\u004a\u006f\u006b",GLH2015: "\u0068\u0069\u006a\u006f\u0064\u0065\u006d\u0069\u006c\u0070\u0075\u0074\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0043\u1d0f\u0280\u004a\u1d0f\u1d0b",GLH2015: "\u0068\u0069\u006a\u006f\u0064\u0065\u006d\u0069\u006c\u0070\u0075\u0074\u0061\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0045\u0070\u0069\u0074\u0061",GLH2015: "\u006a\u006f\u0073\u0065\u006d\u0069\u0063\u006f\u0064\u0035"});
HackHax.push({GrandesLigas: "\ud835\udcdd\u1d07\u0262\u0280\u1d0f",GLH2015: "\u0065\u006c\u006e\u0065\u0067\u0072\u0069\u0074\u006f\u0078\u0044"});
HackHax.push({GrandesLigas: "\u0070\u0061\u006c\u0061",GLH2015: "\u0070\u0061\u006c\u0061\u0067\u0065\u006e\u0069\u006f\u0039\u0039\u0039"});
HackHax.push({GrandesLigas: "\u0061\u006c\u006b \u0076\u0069\u0072\u0061\u0076\u0069\u0072\u006f\u0075",GLH2015: "\u006d\u0061\u0072\u0063\u006f\u0034\u0063\u006c\u0061\u0072\u0065\u0074"});
HackHax.push({GrandesLigas: "\u004c\u0065\u007a\u0063\u0061\u002d\u005f\u002d\u005f\u002d",GLH2015: "\u0074\u006f\u006d\u0061\u0073\u0031\u0032\u0033\u0034\u0035"});
HackHax.push({GrandesLigas: "\u0073\u0037\u006f\u0072\u0064 \u0041\u004c\u004b\u0027",GLH2015: "\u0072\u0065\u0062\u006f\u0074\u0065\u006c\u006c\u0061"});
HackHax.push({GrandesLigas: "\u0048\u0061\u006c\u006c\u0065\u0077\u0042\u006f\u0079",GLH2015: "\u0068\u0061\u006c\u006c\u0065\u0077\u006c\u0065\u006e\u0064\u0061"});
HackHax.push({GrandesLigas: "\ud800\udf11\ud800\udf42\u002e \ud835\udcd1\ud835\udd2f\ud835\udd26\ud835\udd1e\ud835\udd2b \u30c4",GLH2015: "\u0068\u0061\u0078\u0062\u0061\u006c\u006c\u0064\u0069\u006f\u0073\u0031\u0030\u0031\u0032"});
HackHax.push({GrandesLigas: "\u004e\u0065\u0064\u0076\u011b\u0064",GLH2015: "\u0069\u006e\u006f\u006c\u0076\u0069\u0064\u0061\u0062\u006c\u0065\u0031\u0039\u0039\u0037"});
HackHax.push({GrandesLigas: "\u006c\u0061\u0075\u0064\u0072\u0075\u0070",GLH2015: "\u0061\u0062\u0063\u0031\u0032\u0033\u0034\u0035\u0036\u002a"});
HackHax.push({GrandesLigas: "\u004a\u0075\u0061\u0067\u0068\u0069",GLH2015: "\u0074\u0061\u006c\u0061\u006e\u0061\u006c\u0069\u0074\u0061"});
HackHax.push({GrandesLigas: "\u0048\u0065\u044f\u00f8 \u007c \ud835\udce3\ud835\udcd5\ud835\udcd2",GLH2015: "\u006d\u0061\u0074\u006d\u0069\u0074\u006f"});
HackHax.push({GrandesLigas: "\u004b\u006f\u006c\u0061\u0063\u0061\u006f",GLH2015: "\u006d\u0075\u006e\u0064\u006f\u0067\u0061\u0074\u0075\u0072\u0072\u006f\u0031\u0033\u0035"});
HackHax.push({GrandesLigas: "\u0056\u006c\u0061\u0064\u0069\u006d\u0069\u0072 \u0050\u0075\u0074\u0069\u006e",GLH2015: "\u0050\u0075\u0074\u0069\u006e\u0056\u006c\u0061\u0064\u0069\u006d\u0069\u0072\u0031\u0039"});
HackHax.push({GrandesLigas: "\u0048\u0065\u0072\u006f",GLH2015: "\u006d\u0061\u0074\u0067\u006f\u0073\u0074\u006f\u0073\u006f"});
HackHax.push({GrandesLigas: "\u004a\u0050\u0044\u0069\u0061\u007a",GLH2015: "\u006a\u0070\u0031\u0032\u0033\u0034\u0035\u0036"});
HackHax.push({GrandesLigas: "\u004c\u0069\u0063\u0068\u0061\u006e",GLH2015: "\u006c\u0069\u0063\u0068\u0061\u006e\u0034\u0035\u0031\u0036\u0034\u0032\u0034"});
HackHax.push({GrandesLigas: "\u26a1\u0106\u0394\u0197\u00d8\u26a1",GLH2015: "\u0052\u0034\u004d\u0034\u004c\u004c\u0030\u0034\u0052\u0047"});
HackHax.push({GrandesLigas: "\u004d\u0061\u006e\u0079\u0061\u0031\u0038\u0039\u0031",GLH2015: "\u004f\u0072\u006f\u0079\u0063\u0061\u0072\u0062\u006f\u006e\u0068\u0069\u006e\u0063\u0068\u0061\u0064\u0065\u006c\u006d\u0061\u006e\u0079\u0061\u0064\u0065\u0063\u006f\u0072\u0061\u007a\u006f\u006e"});
HackHax.push({GrandesLigas: "\u1d0d\u1d07\u0073\u026a\u1d1b\u1d00",GLH2015: "\u006d\u0065\u0073\u0061\u0075\u0079"});
HackHax.push({GrandesLigas: "\u0056\u0069\u0063\u0068\u006f\u006f",GLH2015: "\u0067\u0075\u0061\u0072\u0069\u0073\u0061\u0070\u006f\u0032\u0030\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0073\u0068\u0069\u0073\u0068\u0069",GLH2015: "\u0067\u0061\u006e\u0067\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0063\u0068\u0061\u006e\u0063\u0068\u0069",GLH2015: "\u0063\u006f\u006e\u0074\u0072\u0061\u0073\u0065\u00f1\u0061\u0032\u0030\u0032\u0030"});
HackHax.push({GrandesLigas: "\u004b\u0072\u0061\u0077\u006b",GLH2015: "\u0034\u0036\u0037\u0038\u0035\u0036\u0038\u0037"});
HackHax.push({GrandesLigas: "\ud835\udc02\ud835\udc1a\ud835\udc2f\ud835\udc1e\ud835\udc20\ud835\udc28\ud835\udc25 \ud835\udfd7 \ud835\udc00\ud835\udc0b\ud835\udc0a",GLH2015: "\u0074\u006f\u006d\u0079\u0033\u0032\u0032\u0038"});
HackHax.push({GrandesLigas: "\u0048\u00e5\u006c\u0061\u006e\u0064",GLH2015: "\u0033\u0073\u0074\u0065\u0062\u0061\u006e\u0038"});
HackHax.push({GrandesLigas: "\u0042\u0072\u006f\u0063\u0061\u0064\u006f\u0072",GLH2015: "\u0062\u0072\u006f\u0063\u0061\u0064\u006f\u0072\u0030\u0039\u0038"});
HackHax.push({GrandesLigas: "\u0065\u006c \u006e\u0069\u00f1\u006f",GLH2015: "\u0065\u006c\u006a\u0061\u006c\u006f\u006e\u0035"});
HackHax.push({GrandesLigas: "\u0044\u0061\u006e \u042f",GLH2015: "\u0064\u0061\u006e\u0069\u0065\u006c\u006c\u0065\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0046\u006c\u0061\u006d\u0061",GLH2015: "\u0030\u0031\u0034\u0031\u0036\u0030\u0038\u0030\u0031"});
HackHax.push({GrandesLigas: "\u0046\u029f\u1d00\u1d0d\u1d00",GLH2015: "\u0031\u0036\u0078\u0064\u0030\u0038\u0030\u0031"});
HackHax.push({GrandesLigas: "\u2131\u029f\ud835\uddba\ud835\udc5a\ud835\uddba",GLH2015: "\u0031\u0036\u0030\u0038\u0030\u0031"});
HackHax.push({GrandesLigas: "\ud83d\udd06\u0054\u0061\u0069\u0079\u006f\u0075\ud83d\udd06",GLH2015: "\u0053\u0075\u006e\u0053\u0075\u006e"});
HackHax.push({GrandesLigas: "\ud83d\udd06\ud835\udc13\u1d00\u0069\u0443\u1d0f\u1d1c\ud83d\udd06",GLH2015: "\u0053\u0075\u006e\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0042\u0061\u006c\u006f\u006d\u0069\u0074\u006f",GLH2015: "\u004f\u0072\u0073\u0069\u006e\u0069\u0031\u0030"});
HackHax.push({GrandesLigas: "\u004c\u0075\u0074\u007a\u0047\u0061\u006d\u0065\u0073",GLH2015: "\u0021\u004d\u0065\u0067\u0061\u004e\u006f\u0076\u006f"});
HackHax.push({GrandesLigas: "\u0064\u0033\u0073\u0074\u0072\u006f",GLH2015: "\u0074\u0061\u0074\u0075\u0064\u006f\u0075\u0074\u0065\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0076\u0069\u0074\u006f\u0072\u006d\u0061\u0072\u0063\u0068\u0069\u006e\u0069\u0040\u0068\u006f\u0074\u006d\u0061\u0069\u006c\u002e\u0063\u006f\u006d",GLH2015: "\u0032\u0030\u0032\u0030\u0035\u0035\u0056\u0049\u0054\u004f\u0052\u0052\u0045\u0047\u0049\u004f"});
HackHax.push({GrandesLigas: "\u0056\u0069\u0074\u00e3\u006f \u00ae \u2022 \u0041",GLH2015: "\u006a\u0061\u006a\u0061\u006a\u0061"});
HackHax.push({GrandesLigas: "\u0042\u0061\u006b\u0075\u0067\u006f",GLH2015: "\u0074\u0068\u0065\u0062\u0065\u0061\u0074\u006c\u0065\u0073\u0036\u0033"});
HackHax.push({GrandesLigas: "\u0057\u0061\u006c\u0074\u0065\u0072 \u005a\u0065\u006e\u0067\u0061 \u0031",GLH2015: "\u004d\u0069\u006c\u006f\u0063\u0061\u0070\u006f\u0039\u0030"});
HackHax.push({GrandesLigas: "\u0049\u0062\u0072\u0061\u0068\u0069\u006d\u006f\u0076\u0069\u0063",GLH2015: "\u0069\u0062\u0072\u0061\u0068\u0061\u0078"});
HackHax.push({GrandesLigas: "\ud835\udd3d\ud835\udd43\ud835\udd38\ud835\udd44\ud835\udd38",GLH2015: "\u0030\u0031\u0034\u0032\u0036\u0039\u0030\u0038\u0030\u0032\u0036\u0078\u0064"});
HackHax.push({GrandesLigas: "\ud835\ude75\u02ea\u1d00\u043c\u1d00",GLH2015: "\u0066\u006c\u0061\u006d\u0061\u0074\u0068\u0065\u0062\u0065\u0073\u0074"});
HackHax.push({GrandesLigas: "\u0047\u006f\u006c\u0064\u0069\u006e\u0067",GLH2015: "\u0031\u0034\u0030\u0035\u0037\u0038"});
HackHax.push({GrandesLigas: "\u0050\u0065\u0072\u006f\u006e \u004d\u0069 \u0050\u0072\u0065\u0073\u0069 \u003c\u0033 \u0048\u0044\u0042",GLH2015: "\u0034\u0037\u0034\u0035\u0033\u0037\u0037\u0032\u006a"});
HackHax.push({GrandesLigas: "\u0041\u006c\u0065\u006a\u006f \u0067\u0061\u006d\u0065\u0072 \u003a\u0076",GLH2015: "\u0070\u0061\u0073\u0073\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0054\u0069\u0061\u0047\u006f\u0064",GLH2015: "\u0074\u0061\u006c\u0061\u006e\u0061\u006c\u0069\u0074\u0061\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0063\u0061\u0074\u0063\u0075\u006c\u0069\u0061\u006f",GLH2015: "\u0076\u0065\u0067\u0065\u0074\u0074\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0061\u0072\u0072\u0069\u0061\u0062\u0061\u007a\u0061\u006c\u0067\u0061",GLH2015: "\u0067\u0061\u0073\u0074\u006f\u006e\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0041\u006c\u0070\u0068\u0061\u0050\u0061\u0074\u006f\u004c\u0075\u0071\u0075\u0069",GLH2015: "\u006c\u006f\u006c\u0078\u0064\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004e\u0061\u0076\u0065",GLH2015: "\u0053\u0069\u006d\u0062\u0072\u006f\u006e\u0032\u0037\u0036\u0030"});
HackHax.push({GrandesLigas: "\u004e\u1d00\u1d20\u1d07",GLH2015: "\u004e\u0061\u0076\u0065"});
HackHax.push({GrandesLigas: "\u004e\u0044\u0049\u0044\u0049",GLH2015: "\u0033\u0073\u0074\u0033\u0062\u0061\u006e\u0038"});
HackHax.push({GrandesLigas: "\u006d\u0069\u006e\u0061\u006d\u0069\u006e\u006f",GLH2015: "\u0062\u0061\u0069\u006c\u0065\u0079"});
HackHax.push({GrandesLigas: "\u004b\u0061\u0068\u006e",GLH2015: "\u0073\u0069\u006c\u006c\u0061\u0031\u0032\u0033\u0034\u0035\u0036"});
HackHax.push({GrandesLigas: "\u004e\u0065\u0077\u0045\u0078\u0070\u0072\u0065\u0073\u0073",GLH2015: "\u004e\u0065\u0077\u0045\u0078\u0070\u0072\u0065\u0073\u0073"});
HackHax.push({GrandesLigas: "\ud835\udc6e\ud835\udc68\ud835\udc69\ud835\udc70\ud835\udc6e\ud835\udc76\ud835\udc73 \u00ae",GLH2015: "\u0046\u004c\u0041\u004d\u0045\u004e\u0047\u004f"});
HackHax.push({GrandesLigas: "\u0073\u0077\u0061\u0067\u0067\u0069\u0065 \u0048\u0044\u0042",GLH2015: "\u006e\u0061\u0063\u0068\u006f\u0074\u0065\u0061\u006d\u006f\u0031"});
HackHax.push({GrandesLigas: "\u0055\u0062\u0061\u006c\u0064\u006f \u0046\u0069\u006c\u006c\u006f\u006c \u002d \u0031",GLH2015: "\u004d\u0069\u006c\u006f\u0063\u0061\u0070\u006f\u0039\u0030\u0030"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0073\u0069\u0074\u0061 \u0044\u0069\u0064\u0061",GLH2015: "\u004d\u0069\u006c\u0061\u006e\u0064\u006f\u0076\u0069\u0063\u0048\u0039\u0030"});
HackHax.push({GrandesLigas: "\u0047\u006f\u006c\u006f\u0076\u0069\u006e",GLH2015: "\u0072\u0075\u0073\u0073\u0069\u0061\u006e\u0030"});
HackHax.push({GrandesLigas: "\u0054\u006a\u0037\u0037",GLH2015: "\u0076\u0061\u0073\u0063\u006f\u0064\u0061\u0067\u0061\u006d\u0061\u0037"});
HackHax.push({GrandesLigas: "\u0065\u006d\u0070\u0061\u006e\u0061\u0064\u0069\u0074\u0061",GLH2015: "\u006d\u0065\u0064\u0061\u006c\u006c\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0043\u0061\u007a\u006f\u0072\u006c\u0061",GLH2015: "\u0035\u0031\u0034\u0039\u0039\u0031\u0035\u0034\u0063\u0068\u0069\u0063\u0068\u0065"});
HackHax.push({GrandesLigas: "\u0046\u0069\u0072\u006d\u0069\u006e\u006f \u0039",GLH2015: "\u0077\u0077\u0065\u0065\u0073\u006d\u0069\u0070\u0061\u0073\u0069\u006f\u006e"});
HackHax.push({GrandesLigas: "\u0046\u026a\u0280\u1d0d\u026a\u0274\u1d0f \u09ed",GLH2015: "\u0077\u0077\u0065\u006d\u0069\u0070\u0061\u0073\u0069\u006f\u006e"});
HackHax.push({GrandesLigas: "\u0061\u0072\u0067",GLH2015: "\u0031\u0032\u0036\u0033\u0036\u0039\u0033\u0036\u0039"});
HackHax.push({GrandesLigas: "\u004e\u0069\u0075\u0054\u0069",GLH2015: "\u006a\u0065\u0066\u0066\u0031\u0033\u0031\u0031\u0032\u0030\u0030\u0035"});
HackHax.push({GrandesLigas: "\u0072\u006f\u006e\u0061\u006c\u0064\u006f \u0066\u0065\u006e\u006f\u006d\u0065\u006e\u006f",GLH2015: "\u004c\u006f\u0073\u0062\u0061\u006c\u006c\u0061\u0073\u0031"});
HackHax.push({GrandesLigas: "\u0280\u1d0f\u0274\u1d00\u029f\u1d05\u1d0f \u0493\u1d07\u0274\u1d0f\u1d0d\u1d07\u0274\u1d0f",GLH2015: "\u006c\u006f\u0073\u0062\u0061\u006c\u006c\u0061\u0073\u0031"});
HackHax.push({GrandesLigas: "\u0043\u0061\u006c\u006c\u0065\u0072\u0069 \u004c\u004e\u0043",GLH2015: "\u0074\u0069\u0061\u0067\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0056\u0061\u006c\u0065\u006e\u0063\u0069\u0061",GLH2015: "\u0074\u0069\u006d\u0062\u0075\u0076\u0069\u0070"});
HackHax.push({GrandesLigas: "\u0054\u0068\u0065\u004c\u0069\u006f\u006c",GLH2015: "\u0074\u0072\u0069\u0070\u006c\u0065\u0070\u0075\u0065\u0072\u006b\u006f\u0031\u0033"});
HackHax.push({GrandesLigas: "\u004c\u0075\u0063\u0068\u006f\u0052\u006f\u0064\u0072\u0069\u0067\u0075\u0065\u007a",GLH2015: "\u0053\u0061\u006e\u0067\u0072\u0065\u0072\u006f\u006a\u0061\u0031\u0030\u0031"});
HackHax.push({GrandesLigas: "\u2717\u1d00\u1d20\u026a",GLH2015: "\u0034\u0031\u0039\u0030\u0036\u0035\u0038\u0039"});
HackHax.push({GrandesLigas: "\u006a\u0061\u0062",GLH2015: "\u0031\u0031\u0032\u0032\u0068\u0061\u0068\u0061"});
HackHax.push({GrandesLigas: "\u265f\ufe0f \u0059\u0075\u0072\u0069 \u0047\u0061\u007a\u0069\u006e\u0073\u006b\u0069 \u265f\ufe0f",GLH2015: "\u0069\u0076\u0061\u006e\u0065\u006c\u0063\u0061\u0070\u006f\u0031\u0033"});
HackHax.push({GrandesLigas: "\u265f\ufe0f \ud835\udcb4\u1d1c\u0280\u026a \ud835\udc3a\u1d00\u1d22\u026a\u0274\u0073\u1d0b\u026a \u265f\ufe0f",GLH2015: "\u0069\u0076\u0061\u006e\u0065\u006c\u0063\u0061\u0070\u006f\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0050\u006f\u0064\u006f\u006c\u0073\u006b\u0069 \u0053\u004b",GLH2015: "\u0031\u0034\u0064\u0065\u006a\u0075\u006e\u0069\u006f"});
HackHax.push({GrandesLigas: "\u0056\u0065\u0072\u0072\u0061\u0074\u0069",GLH2015: "\u0032\u0062\u0032\u0074\u0079\u0065"});
HackHax.push({GrandesLigas: "\u0045\u006e\u007a\u006f \u0050\u0065\u0072\u0065\u007a",GLH2015: "\u006b\u0068\u0065\u0061\u0062\u0072\u006f\u0033\u0035\u0036"});
HackHax.push({GrandesLigas: "\u2591\u0050\u0065\u0070\u0047\u0075\u0061\u0072\u0064\u0069\u006f\u006c\u0061\u2591",GLH2015: "\u004c\u0061\u0070\u0065\u0072\u0072\u0061\u0070\u0065\u006e\u006e\u0079\u0032\u0030\u0031\u0032"});
HackHax.push({GrandesLigas: "\u004e\u0061\u0063\u0068\u006f\u0043\u0061\u0073\u006c\u0061",GLH2015: "\u0061\u0065\u007a\u0061\u006b\u006d\u0069\u0031\u0031"});
HackHax.push({GrandesLigas: "\u006f\u0072",GLH2015: "\u006f\u0072"});
HackHax.push({GrandesLigas: "\ua9c1 \ud835\udd44\ud835\udd38\ud835\udd4a\u20b5\u2c67\ud835\udd3c\u211d\ud835\udd38\u2115\ud835\udd46\ua9c2",GLH2015: "\u006b\u0068\u0065\u0061\u0062\u0072\u006f"});
HackHax.push({GrandesLigas: "\u006a\u0075\u0061\u006e\u0073\u0069\u006f",GLH2015: "\u0061\u0072\u0072\u0069\u006f\u006c\u0061\u006a\u0075\u0061\u006e"});
HackHax.push({GrandesLigas: "\u0044\u002e\u004f\u002e\u0044",GLH2015: "\u006f\u0073\u006f\u0070\u0072\u0061\u0074\u0074\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0074\u0061\u0078 \u002d \u0043\u004c",GLH2015: "\u0038\u0037\u0033\u0030\u0031\u0035\u0036\u0031"});
HackHax.push({GrandesLigas: "\u0063\u0061\u0069\u006d\u0061\u006e \u0064\u0065\u0073\u0064\u0065 \u006c\u0061 \u0049\u0073\u006c\u0061",GLH2015: "\u0058\u0061\u0076\u0069\u0048\u0065\u0072\u006e\u0061\u006e\u0064\u0065\u007a\u0042\u0061\u006c\u006f\u006e\u0044\u0065\u004f\u0072\u006f\u004e\u0064\u0065\u0061\u0068"});
HackHax.push({GrandesLigas: "\u0042\u0065\u006e \u0053\u006f\u006c\u006f",GLH2015: "\u0066\u0072\u0061\u006e\u0063\u0069\u0073\u0063\u006f"});
HackHax.push({GrandesLigas: "\u0046 \u0031\u0032\u0033",GLH2015: "\u0031\u0032\u0036\u0033\u0036\u0039"});
HackHax.push({GrandesLigas: "\u0046\u0065\u007a\u0075\u0075",GLH2015: "\u0046\u0065\u007a\u0075\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0038\u0039\u0031\u0030\u0031\u0031\u0046\u005a"});
HackHax.push({GrandesLigas: "\u0043\u0072\u006f\u0073\u0073",GLH2015: "\u006b\u0065\u0076\u0069\u006e\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0053\u0068\u0061\u0077\u006e \u004d\u0065\u006e\u0064\u0065\u0073",GLH2015: "\u0073\u0068\u0061\u0077\u006e\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0442\u0061\u0445",GLH2015: "\u0038\u0037\u0033\u0030"});
HackHax.push({GrandesLigas: "\u2133\u026a\u029f\u1d0b\u028f \ud835\udcb2\u1d00\u028f",GLH2015: "\u0031\u0030\u0039\u0034\u0032\u0034\u0033\u0036\u0032\u0038\u0061"});
HackHax.push({GrandesLigas: "\u004d\u004f\u004e\u0053\u0054\u0045\u0052",GLH2015: "\u006b\u0065\u0076\u0069\u006e\u0031\u0033"});
HackHax.push({GrandesLigas: "\u0043\u0065\u006c\u0065\u0073\u0074\u0072\u006f\u006e",GLH2015: "\u0043\u006f\u006c\u006f\u0043\u006f\u006c\u006f"});
HackHax.push({GrandesLigas: "\u004d\u0056\u0041\u0050\u0050\u0045",GLH2015: "\u0074\u0068\u0073\u0032\u0036\u0038\u0033\u0030\u0030\u0034\u0032"});
HackHax.push({GrandesLigas: "\u006a\u0063\u0065",GLH2015: "\u0066\u0065\u0062\u0072\u0065\u0072\u006f"});
HackHax.push({GrandesLigas: "\ud800\udf11\ud800\udf42\u002e \ud835\udcd1\ud835\udd2f\ud835\udd26\ud835\udd1e\ud835\udd2b \u30c4 \ud835\udcd5\ud835\udcd1\ud835\udcd2",GLH2015: "\u0064\u0069\u006f\u0073\u0068\u0061\u0078\u0062\u0061\u006c\u006c\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0280\u0061\u1d22\u0280",GLH2015: "\u0072\u0061\u007a\u0072\u0032\u0031\u0068\u0061\u0078\u0062\u0061\u006c\u006c"});
HackHax.push({GrandesLigas: "\u0045\u006e\u0044\u0065\u0072\u0070",GLH2015: "\u0074\u0061\u006c\u0061\u006e\u0061\u006c\u0069\u0074\u0061\u0032\u0030\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0048\u0061\u0072\u0069\u0074",GLH2015: "\u0062\u0072\u0061\u0068\u0069\u006d\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0047\u0061\u006e\u007a\u006f\u006c\u006f \u0048\u0069\u0067\u0075\u0061\u0069\u006e",GLH2015: "\u0068\u006f\u006c\u0061\u0032\u0030\u0032\u0030"});
HackHax.push({GrandesLigas: "\u0070\u0061\u0073\u0074\u006f\u0072\u0065\u002b\u0031\u0030",GLH2015: "\u0070\u0061\u0073\u0074\u006f\u0072\u0065\u002b\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0045\u006c \u006c\u006f\u0063\u006f",GLH2015: "\u0074\u0075\u0076\u0069\u0065\u006a\u0061\u0065\u006e\u0074\u0061\u006e\u0067\u0061"});
HackHax.push({GrandesLigas: "\u0054\u0072\u0065\u0063\u0065",GLH2015: "\u006c\u006f\u006c\u0069\u0070\u006f\u0070"});
HackHax.push({GrandesLigas: "\u0054\u0069\u0061\u006e",GLH2015: "\u0031\u0033\u0031\u0033"});
HackHax.push({GrandesLigas: "\u0039\u007a \u004d\u0061\u006c\u0061\u0073\u006f",GLH2015: "\u0066\u0061\u0063\u0065\u0062\u006f\u006f\u006b\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0042\u0061\u006e\u0064\u0065\u0072\u0069\u006e\u0044\u0065\u006c\u0043\u006f\u0072\u006e\u0065\u0072",GLH2015: "\u0062\u0061\u006e\u0064\u0065"});
HackHax.push({GrandesLigas: "\u0054\u0061\u0072\u0065\u006b",GLH2015: "\u0052\u0061\u0063\u0069\u006e\u0067\u0043\u006c\u0075\u0062\u0032\u0030\u0030\u0034"});
HackHax.push({GrandesLigas: "\u0054\u006f\u006d\u0069\u0063\u0061\u0062\u0072\u0069\u0067\u006e\u0061\u0063",GLH2015: "\u0077\u0061\u0072\u006d\u0061\u0073\u0074\u0065\u0072\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004c\u0061\u0062\u0075\u0072\u006f",GLH2015: "\u0047\u0075\u0069\u006c\u006c\u0065\u0066\u0065\u0064\u0065\u0031\u0035\u0032\u0033\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0043\u0075\u0062\u0065\u0072\u006f \u0023\u0035",GLH2015: "\u0043\u0075\u0062\u0065\u0072\u0069\u0074\u006f\u0070\u0072\u006f"});
HackHax.push({GrandesLigas: "\ud835\udd6e\ud835\udd3c\u0052\ud835\udcb1\ud83c\udd78\u00b9\u00b9",GLH2015: "\u006d\u0069\u006c\u0061\u0067\u0072\u006f\u0032\u0032"});
HackHax.push({GrandesLigas: "\u0048\u006f\u006a\u0069\u0074\u0061",GLH2015: "\u006f\u006a\u0061\u006c\u0061\u006c\u0061\u0074\u0075\u0076\u0069\u0065\u0072\u0061\u0065\u006c\u006c\u0061"});
HackHax.push({GrandesLigas: "\u0045\u0064\u002e\u006c\u0075\u0073\u006b\u0061",GLH2015: "\u0032\u0033\u0032\u0036\u0031\u0031\u006a\u0065"});
HackHax.push({GrandesLigas: "\u0041\u0072\u0061\u006f\u0073",GLH2015: "\u006d\u0061\u006e\u007a\u0061\u006e\u0061\u0030\u0030"});
HackHax.push({GrandesLigas: "\u004e\u0061\u0073\u0061\u0077",GLH2015: "\u0073\u006f\u0079\u0070\u0075\u0074\u0061\u0073\u006f"});
HackHax.push({GrandesLigas: "\u0062\u0061\u0072\u0065\u0073\u0069",GLH2015: "\u0032\u0036\u0033\u0031\u0030\u0037\u0032\u0035\u0031\u0039"});
HackHax.push({GrandesLigas: "\u0068\u0061\u0072\u0064\u0065\u006e",GLH2015: "\u0076\u0074\u0072\u0033\u0031\u0030\u0038\u0030\u0031"});
HackHax.push({GrandesLigas: "\u004c\u002e \u004c\u0061\u0077\u006c\u0069\u0065\u0074",GLH2015: "\u0072\u0079\u0075\u007a\u0061\u006b\u0069"});
HackHax.push({GrandesLigas: "\u0045\u0073\u0074\u0065\u0062\u0061\u006e\u005f\u0045\u0061\u0064\u006f",GLH2015: "\u006c\u0065\u0070\u0072\u006f\u0073\u006f\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0043\u0061\u006c\u0061\u0063\u0061",GLH2015: "\u0066\u0061\u0073\u0069\u0074\u006f\u0032\u0035"});
HackHax.push({GrandesLigas: "\u006d\u0031\u006b\u0034\u0033\u006c\u0030\u0070",GLH2015: "\u006d\u0069\u006b\u0061\u0065\u006c\u006c\u0070\u0031\u0034"});
HackHax.push({GrandesLigas: "\u0053\u0068\u0061\u0044\u006f\u0030\u0077\u0027",GLH2015: "\u0076\u0061\u0073\u006d\u0032\u0030\u0031\u0033"});
HackHax.push({GrandesLigas: "\u004b\u0069\u006e\u0067 \u004a\u0052",GLH2015: "\u0068\u0061\u006e\u0067\u0065\u006e\u0033\u0034\u0035"});
HackHax.push({GrandesLigas: "\u004c\u00fa\u00f9\u0048",GLH2015: "\u0073\u0061\u0066\u0069\u0032\u0035\u0030\u0039"});
HackHax.push({GrandesLigas: "\u0056\u0069\u00f1\u0061\u0073",GLH2015: "\u0067\u0072\u0061\u0063\u0069\u0065\u006c\u0061\u0032\u0035"});
HackHax.push({GrandesLigas: "\ud83d\udca4\ud83d\udeab\u2605\u26a1\u0262\u1d00\u1d0d\u0432\u1d2e\u2660 \u0299\u026a\u01ac\u26a1\u262f\ud83d\udeab\ud83d\udca4",GLH2015: "\u0073\u006c\u0061"});
HackHax.push({GrandesLigas: "\u0049\u006e\u0064\u0065\u0070\u0065\u006e\u0064\u0069\u0065\u006e\u0074\u0065 \u0064\u0065\u006c \u0056\u0061\u006c\u006c\u0065",GLH2015: "\u0072\u0065\u006c\u0069\u0063\u0061\u006e\u0074\u0068\u0039\u0037"});
HackHax.push({GrandesLigas: "\u0067\u0061\u0062\u0072\u0069\u0065\u006c \u006a\u0065\u0073\u0075\u0073",GLH2015: "\u0031\u0031\u0032\u0037\u0036\u0030\u0037\u0037\u0034\u0034"});
HackHax.push({GrandesLigas: "\u004b\u0031\u0031\u0072\u0079\u0065",GLH2015: "\u006c\u0075\u0063\u0061\u0073\u0063\u0075\u006c\u006f\u0076\u0065\u0072\u0064\u0065\u0031\u0032\u0033\u0034\u0035"});
HackHax.push({GrandesLigas: "\u0053\u0065\u0076\u0065\u006e\u0074\u0079",GLH2015: "\u0074\u0061\u0064\u0065\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u006d\u0065\u0072\u0063\u0061\u0064\u006f",GLH2015: "\u006d\u0065\u0072\u0063\u0061\u0064\u006f"});
HackHax.push({GrandesLigas: "\u0054\u0069\u0074\u006f \u0053\u0061\u006e\u0074\u006f\u006e\u0069",GLH2015: "\u006b\u0061\u006c\u006f\u0075\u0075\u0031\u0032"});
HackHax.push({GrandesLigas: "\u004c\u0041 \u0046\u004c\u0045\u0043\u0048\u0041",GLH2015: "\u0072\u0069\u0076\u0065\u0072\u0070\u006c\u0061\u0074\u0065\u0032\u0035"});
HackHax.push({GrandesLigas: "\u004b\u0052\u0049\u004c\u0049\u004e",GLH2015: "\u0063\u006f\u006e\u0074\u0072\u0061\u006b\u0072\u0069\u006c\u0069\u006e"});
HackHax.push({GrandesLigas: "\ud835\ude42\u1d00\u0299\u0069\u0262\u006f\u029f",GLH2015: "\u0066\u0061\u0073\u0069\u0074\u006f\u0031"});
HackHax.push({GrandesLigas: "\u0066\u0061\u0062\u0069\u006e\u0068\u006f",GLH2015: "\u0073\u0061\u006e\u0074\u0069\u006e\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0046\u1d00\u0299\u026a\u0274\u029c\u1d0f",GLH2015: "\u0071\u0075\u0069\u006e\u0074\u0061\u006e\u0061\u0034\u0035\u0032\u0030"});
HackHax.push({GrandesLigas: "\u0042\u0061\u0072\u006e\u0065\u0073",GLH2015: "\u0066\u0061\u006e\u0074\u0061\u0073\u0069\u006f\u0073\u006f"});
HackHax.push({GrandesLigas: "\u0076\u0061\u006c\u0065\u006e\u0074\u0069\u006e\u006f",GLH2015: "\u0063\u0068\u0069\u006c\u0065\u0031\u0032\u0033\u0034\u0035"});
HackHax.push({GrandesLigas: "\u0042\u0075\u0073\u0063\u0061\u0070\u0069\u00e9\u0073",GLH2015: "\u0073\u0061\u006d\u006d\u0079\u0076\u006f\u006c\u0061\u0064\u006f\u0072\u0061"});
HackHax.push({GrandesLigas: "\u004d\u0069\u006e\u0061\u0074\u006f\u004e\u0061\u006d\u0069\u006b\u0061\u007a\u0065",GLH2015: "\u0061\u0062\u0072\u0061\u0068\u0061\u006d \u006d\u0061\u0074\u0065\u006f"});
HackHax.push({GrandesLigas: "\u004d\u0061\u006e\u0064\u0061\u0072\u0069\u006e\u006f",GLH2015: "\u0068\u0061\u0078\u0062\u0061\u006c\u006c"});
HackHax.push({GrandesLigas: "\u0076\u0061\u006c\u0065\u006e\u0074\u0069\u006e\u006f\u006f",GLH2015: "\u0067\u006f\u0079\u006f\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u004e\u0065\u0079\u006d\u0061\u0072 \u004a\u0052\u002e \u0023\u0031\u0030",GLH2015: "\u0032\u0036\u0032\u0033\u0031\u0031\u006a\u0065"});
HackHax.push({GrandesLigas: "\u004a\u0061\u006d\u0065\u0073\u0052\u006f\u0064\u0072\u00ed\u0067\u0075\u0065\u007a",GLH2015: "\u0074\u0069\u0074\u006f\u0030\u0037\u0033\u0031"});
HackHax.push({GrandesLigas: "\u0041\u006f\u006d\u0069\u006e\u0065",GLH2015: "\u0034\u0032\u0032\u0035\u0033\u0039"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0062\u0072\u0069\u0065\u006c \u004d\u0061\u0072\u0074\u0069\u006e\u0065\u006c\u006c\u0069",GLH2015: "\u0074\u0061\u0062\u006f"});
HackHax.push({GrandesLigas: "\ud835\udc6a\ud835\udc8a\ud835\udc8f\ud835\udc9b\ud835\udc8a\ud835\udc90 \ud835\udc74\ud835\udc96\ud835\udc9b\ud835\udc8a\ud835\udc90",GLH2015: "\u0069\u0076\u0061\u006e\u0065\u006c\u0063\u0061\u0070\u006f\u0032\u0030"});
HackHax.push({GrandesLigas: "\u0041\u0067\u0075\u0061",GLH2015: "\u006d\u0069\u006d\u0061\u006d\u0061\u006d\u0065\u006d\u0069\u006d\u0061"});
HackHax.push({GrandesLigas: "\u0050\u0041\u004e\u0043\u0048\u004f\u004e\u0045",GLH2015: "\u0050\u004f\u0052\u004f\u0050\u004f\u0050\u004f\u0050\u004f\u0052\u004f\u0050\u004f\u0050\u004f"});
HackHax.push({GrandesLigas: "\u1e3c\u0041 \u0492\u004c\u0045\u0108\u0048\u01cd",GLH2015: "\u0032\u0035\u0030\u0034\u0030\u0031"});
HackHax.push({GrandesLigas: "\ud835\udc13\ud835\udc1e\ud835\udc2b\ud835\udc2b\ud835\udc32",GLH2015: "\u0040\u0043\u0068\u0061\u006e\u0063\u0068\u006f\u0031\u0039\u0037\u0033"});
HackHax.push({GrandesLigas: "\u0042\u0041\u0054\u0045\u0052\u0049\u0041 \ud83d\udd0b",GLH2015: "\u0053\u0065\u006e\u006a\u0069\u0078\u0078\u0070\u0072\u006f"});
HackHax.push({GrandesLigas: "\u0046\u0065\u0072\u0074\u006f\u006c\u0069",GLH2015: "\u006d\u006f\u0072\u0061\u006d\u0065\u0073\u0073\u0069\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0070\u0069\u0062\u0065 \u0063\u0061\u006e\u0074\u0069\u006e\u0061",GLH2015: "\u0065\u0073\u0063\u006f\u006e\u0064\u0069\u0064\u006f\u0031"});
HackHax.push({GrandesLigas: "\u004d\u03b1\u044f\u0063\u03c3 \u0052\u0454\u03c5\u0455\u00aa",GLH2015: "\u0031\u0035\u0034\u0030\u0030\u0032\u0035\u0030\u0034"});
HackHax.push({GrandesLigas: "\u0041\u0072\u0074\u0075\u0072\u006f \u0042\u0069\u0064\u00f3\u006e",GLH2015: "\u0043\u006f\u0070\u0065\u0072\u006e\u0069\u0063\u006f\u0031"});
HackHax.push({GrandesLigas: "\u0070\u0069\u0063\u0068\u0069\u0072\u0069\u0063\u006f \u0065\u006d\u0065 \u006a\u006f\u0074\u006f",GLH2015: "\u0067\u0032\u0031\u0036\u0035\u0034\u0034\u0032\u0030"});
HackHax.push({GrandesLigas: "\u0058\u0065\u006e\u0065",GLH2015: "\u0068\u0061\u0078\u0062\u0061\u006c\u006c\u0031\u0038"});
HackHax.push({GrandesLigas: "\u0041\u006c\u0061\u006e\u0062\u006a\u0065\u007a",GLH2015: "\u0063\u0061\u0063\u0061\u006d\u0061\u006e\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0049\u0046\u0061\u0074\u0068\u0065\u0072\u0031",GLH2015: "\u0030\u0037\u0031\u0032\u0072\u0079\u0061\u006e"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0067\u0069\u0061",GLH2015: "\u0039\u0038\u0037\u0036\u0035\u0034\u0033\u0032\u0031"});
HackHax.push({GrandesLigas: "\u26a1\ud835\udd40\ud835\udd3e\u2115\ud835\udd38\u20b5\u2160\ud835\udd46 \ud835\udd4a\u24b8\ud835\udd46\u20b5\u20b5\ud835\udd46\u26a1",GLH2015: "\u0061\u0072\u0067\u0065\u006e\u0074\u0069\u006e\u0061\u0032\u0030\u0032\u0030"});
HackHax.push({GrandesLigas: "\u0053\u0069\u0064\u0053\u0069\u006c\u0065\u006e\u0063\u0065",GLH2015: "\u004c\u0075\u0063\u0068\u0069\u0068\u0061\u006b\u0075\u006e\u0039\u0035"});
HackHax.push({GrandesLigas: "\u0050\u0061\u0062\u006c\u0069\u0074\u006f \u0041\u006e\u0064\u0072\u006f\u0069\u0064",GLH2015: "\u0064\u0072\u0061\u0067\u006f\u006e\u0031\u0030\u0031\u0030\u0078\u0064"});
HackHax.push({GrandesLigas: "\u0050\u0065\u0070\u0073\u0069",GLH2015: "\u0062\u0065\u006c\u0067\u0072\u0061\u006e\u006f\u0064\u0065\u0063\u006f\u0072\u0064\u006f\u0062\u0061"});
HackHax.push({GrandesLigas: "\u0072\u0075\u0073\u0069\u0074\u006f \u0061\u0073\u0073\u0061\u0064",GLH2015: "\u006a\u006b\u0061\u0067\u0068\u0065\u0072\u0061\u0065"});
HackHax.push({GrandesLigas: "\u005c\u0394\u03fb\u2081\u2080\u2081\u2084\u002f",GLH2015: "\u0067\u0061\u0062\u0072\u0069\u0065\u006c\u0072\u006f\u006a\u0061\u0073\u0078\u0064"});
HackHax.push({GrandesLigas: "\u0067\u0061\u0062\u0072\u0069\u0065\u006c\u0072\u006f\u006a\u0061\u0073\u0034\u0033\u0033\u0034\u0033",GLH2015: "\u0067\u0061\u0062\u0072\u0069\u0065\u006c\u0072\u006f\u006a\u0061\u0073\u0078\u0064\u0064\u0064\u0064\u0064\u0064"});
HackHax.push({GrandesLigas: "\u007a\u0065\u0072\u006b\u006f\u0072",GLH2015: "\u0030\u0037\u0031\u0031\u0031\u0039\u0030\u0035\u0039\u0031"});
HackHax.push({GrandesLigas: "\u0063\u0061\u0069\u0072",GLH2015: "\u0063\u0033\u0031\u0039\u0035\u0038\u0032\u0034"});
HackHax.push({GrandesLigas: "\u0068\u0069\u006d\u0061\u006c\u0061\u0079\u0065\u0072\u006f",GLH2015: "\u006c\u0061\u0075\u0072\u0065\u0061\u006e\u006f"});
HackHax.push({GrandesLigas: "\u0049\u0062\u0072\u0061\u0068\u0069\u006d\u006f\u0076\u0069\u0063\u0032\u0039\u0030\u0035",GLH2015: "\u0069\u0062\u0072\u0061\u0068\u0061\u0078\u0078"});
HackHax.push({GrandesLigas: "\ud83d\udc00\u005b\u044f\u0332\u0305\u03b1\u0332\u0305\u0442\u0332\u0305\u03c3\u0332\u0305\u005d\ud83d\udc01",GLH2015: "\u0072\u0061\u0074\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0058\u0056\u0075\u0072\u0074\u005f",GLH2015: "\u0062\u0072\u0061\u0077\u006c\u0073\u0074\u0061\u0072\u0073"});
HackHax.push({GrandesLigas: "\u004c\u0079\u004b \u0023\u0032\u0030",GLH2015: "\u0070\u006f\u006b\u0065\u0072\u0063\u006f\u0064\u0032"});
HackHax.push({GrandesLigas: "\u006c\u0061\u0075\u0074\u0069\u0063\u0061\u0074",GLH2015: "\u0061\u006d\u0061\u0072\u0067\u0061\u0073\u0061\u0075\u0072\u0075\u0073"});
HackHax.push({GrandesLigas: "\u0048\u0061\u0061\u006c\u0061\u006e\u0064",GLH2015: "\u0072\u0069\u0076\u0065\u0072\u0070\u006c\u0061\u0074\u0065\u0031\u0037"});
HackHax.push({GrandesLigas: "\u0023\u0042\u0065\u006e\u006a\u0069",GLH2015: "\u006c\u006f\u0073\u0073\u0069\u006d\u0070\u0073\u006f\u006e"});
HackHax.push({GrandesLigas: "\u0042\u0065\u006e\u006a\u0069",GLH2015: "\u006c\u006f\u0073\u0073\u0069\u006d\u0070\u0073\u006f\u006e\u0032\u0030\u0030\u0035"});
HackHax.push({GrandesLigas: "\u0047\u0079\u006e\u0054\u0075\u0072\u0062\u006f",GLH2015: "\u0062\u0079\u0065\u006c\u0064\u0069\u0066\u0072\u0061\u006e"});
HackHax.push({GrandesLigas: "\ud835\udc6e\ud835\udc82\ud835\udc83\ud835\udc93\ud835\udc8a\ud835\udc86\ud835\udc8d\u30c4",GLH2015: "\u0064\u0069\u006e\u006f\u0073\u0073\u0061\u0075\u0072\u006f\u0073"});
HackHax.push({GrandesLigas: "\u0053\u03b1\u0438\u0442\u0131\u002e\u0193\u03c5\u0131\u043c\u03b1\ufe31\u0046\u00dc",GLH2015: "\u0074\u0031\u0034\u006b\u0039\u0061\u006c\u0073"});
HackHax.push({GrandesLigas: "\u006c\u0061\u0076\u0069\u0072\u0075\u0074\u0061\u0076\u0065\u0072\u0061",GLH2015: "\u0078\u0065\u006e\u0065\u0069\u0078\u0065\u0031\u0030"});
HackHax.push({GrandesLigas: "\u26a1\u0421\u0466\u0456\u047a\u26a1",GLH2015: "\u0043\u0030\u0052\u0052\u0031\u0033\u004e\u0054\u0033\u0053"});
HackHax.push({GrandesLigas: "\u0063\u0065\u0072\u0065\u007a\u0061",GLH2015: "\u0063\u0065\u006e\u0061\u0074\u0069\u006f\u006e\u0039\u0038"});
HackHax.push({GrandesLigas: "\u0043\u0061\u0072\u006c\u006f\u0073",GLH2015: "\u0062\u0075\u006e\u0064\u0065\u0073\u006c\u0069\u0067\u0061\u0031"});
HackHax.push({GrandesLigas: "\u0044\u0065 \u0041\u0072\u0072\u0061\u0073\u0063\u0061\u006e\u0065\u0074\u0061 \u2020",GLH2015: "\u0079\u0061\u006e\u007a\u0069\u0063\u0061\u0031\u0035\u0037\u0037"});
HackHax.push({GrandesLigas: "\u0042\u0045\u0053\u0054\u0049\u0041 \u0044\u0045\u004c \u0048\u0041\u0052\u0044\u0043\u004f\u0052\u0045",GLH2015: "\u0066\u0065\u006c\u0069\u0070\u0069\u006e\u006f\u0031"});
HackHax.push({GrandesLigas: "\u0053\u0075\u0072\u0072\u0065\u0079",GLH2015: "\u0033\u0037\u0048\u0033\u0072\u0065\u0075\u004d"});
HackHax.push({GrandesLigas: "\ud835\ude3d\ud835\ude5a\ud835\ude56\ud835\ude69\ud835\ude6f",GLH2015: "\u0063\u0068\u0061\u006d\u0070\u0069\u006f\u006e\u007a"});
HackHax.push({GrandesLigas: "\u0053\u0061\u006e\u0074\u0069\u006e\u006f",GLH2015: "\u0073\u0061\u006e\u0074\u0069\u006e\u006f\u0030\u0039\u0032\u0036\u0038\u0037\u0039\u0030\u0031"});
HackHax.push({GrandesLigas: "\u0262\u1d00\u0299\u0280\u026a\u1d07\u029f \u1d0d\u1d00\u0280\u1d1b\u026a\u0274\u1d07\u029f\u029f\u026a",GLH2015: "\u0072\u0061\u0069\u0032\u0030\u0030\u0037"});
HackHax.push({GrandesLigas: "\u004a\u006f\u0072\u0067\u0065 \u0053\u0065\u0048",GLH2015: "\u004a\u006f\u0072\u0067\u0065\u0039\u0038"});
HackHax.push({GrandesLigas: "\u0062\u0061\u0074\u0069\u0073\u0074\u0075\u0074\u0061 \u0076\u0066",GLH2015: "\u0062\u0061\u0074\u0069\u0073\u0074\u0075\u0074\u0061\u0068\u0061\u0078\u0031\u0038"});
HackHax.push({GrandesLigas: "\u0062\u0061\u0074\u0069\u0073\u0074\u0075\u0074\u0061",GLH2015: "\u0046\u0065\u0072\u0072\u006f\u0063\u0061\u0072\u0072\u0069\u006c\u0031\u0038"});
HackHax.push({GrandesLigas: "\u004b\u0061\u0073 \u004b\u0061\u006c\u0069",GLH2015: "\u004d\u0069\u006c\u006f\u0065\u006c\u006b\u0061\u0073\u0073\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0053\u0075\u0069\u007a\u006f",GLH2015: "\u0043\u0068\u0061\u006c\u006f\u0073\u006f\u0031\u0034"});
HackHax.push({GrandesLigas: "\u0041\u0064\u0065\u0062\u0061\u0079\u006f\u0072\u0072",GLH2015: "\u0078\u0064\u0065\u006c\u006f\u006c\u0030\u0033\u0030\u0036"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0062\u0072\u0069\u0065\u006c \u004d\u0065\u006e\u0069\u006e\u006f",GLH2015: "\u0050\u0061\u006c\u006d\u0065\u0069\u0072\u0061\u0073\u0032\u0030"});
HackHax.push({GrandesLigas: "\u006a\u0072",GLH2015: "\u0031\u0032\u0033\u0034\u0034\u0033\u0032\u0031"});
HackHax.push({GrandesLigas: "\u0048\u1d00\u030a\u029f\u1d00\u0274\u1d05",GLH2015: "\u0069\u006e\u0064\u0065\u0070\u0065\u0064\u0069\u0065\u006e\u0074\u0065"});
HackHax.push({GrandesLigas: "\u0073\u0074\u0069\u0076\u0065\u006e",GLH2015: "\u0073\u0065\u006c\u0065\u0063\u0063\u0069\u006f\u006e"});
HackHax.push({GrandesLigas: "\u00c9\u006c\u00e9\u0067\u0061\u006e\u0074",GLH2015: "\u0061\u0074\u0072\u0070\u0065\u0072\u0072\u006f"});
HackHax.push({GrandesLigas: "\u0046\u0065\u006c\u0069\u0070\u0065\u002a\u002d\u0031\u0033",GLH2015: "\u006d\u0061\u0078\u0069\u006d\u0069\u006c\u0069\u0061\u006e\u006f\u0037"});
HackHax.push({GrandesLigas: "\u0048\u1d00\u1d00\u029f\u1d00\u0274\u1d05",GLH2015: "\u0078\u0064\u0078\u0064\u0078\u0064\u0078\u0064"});
HackHax.push({GrandesLigas: "\u0050\u0061\u0073\u0074\u006f\u0072\u0065 \u002b\u0031\u0030",GLH2015: "\u0033\u0039\u0030\u0036\u0031\u0037\u0034\u0034"});
HackHax.push({GrandesLigas: "\u004d\u0049\u0053\u0054\u0045\u0052 \u0053\u0041\u0054\u0041\u004e",GLH2015: "\u006d\u0069\u0074\u0069\u006f\u006d\u0065\u0068\u0061\u0063\u0065\u0065\u006c\u006f\u0072\u0074\u006f"});
HackHax.push({GrandesLigas: "\u0045\u004c \u0050\u0045\u004f\u0052 \u0041\u0052\u0051\u0055\u0045\u0052\u004f \u0044\u0045 \u0048\u0041\u0058\u0042\u0041\u004c\u004c",GLH2015: "\u0031\u0031\u0032\u0032\u0033\u0033\u0034\u0034\u0035\u0035"});
HackHax.push({GrandesLigas: "\u0050\u0061\u0062\u006c\u006f",GLH2015: "\u0078\u0069\u0071\u0075\u0069\u0074\u0061\u0034"});
HackHax.push({GrandesLigas: "\u0044\u0061\u006e\u0069\u0065\u006c",GLH2015: "\u006c\u0061\u0075\u0072\u0065\u0061\u006e\u006f\u0031\u0031"});
HackHax.push({GrandesLigas: "\u004e\u0069\u0073\u0073\u0061\u0062\u0065",GLH2015: "\u006e\u0069\u0073\u0073\u0061\u006c\u0061\u0075\u0072\u0065\u0061\u006e\u006f\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0043\u0041\u005a\u004f \u0045\u004c \u004d\u0041\u004d\u0042\u004f",GLH2015: "\u0066\u0065\u006c\u0069\u0070\u0069\u006e\u006f\u0032"});
HackHax.push({GrandesLigas: "\u0053\u0068\u0065\u0076",GLH2015: "\u006c\u0061\u006d\u0061\u0071\u0075\u0069\u006e\u0061"});
HackHax.push({GrandesLigas: " \u0043\u006f\u006e\u0064\u006f\u0072 \u0052\u006f\u006a\u0061\u0073",GLH2015: "\u0050\u0069\u006e\u006f\u0063\u006f\u0064\u0061\u0072\u006b"});
HackHax.push({GrandesLigas: "\u0068\u0061\u007a\u0061\u0072\u0064",GLH2015: "\u006d\u0061\u0072\u0069\u0061\u006e\u0069\u0074\u006f\u0031"});
HackHax.push({GrandesLigas: "\u0073\u0068\u0075\u0079\u0061",GLH2015: "\u0073\u0068\u0075\u0079\u0069\u0074\u0061"});
HackHax.push({GrandesLigas: "\u0046\u0061\u006c\u0063\u00e3\u006f",GLH2015: "\u0073\u0061\u006e\u0074\u006f\u0073\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004c\u0075\u0073\u0063\u0061 \u004c\u0069\u006d\u0061",GLH2015: "\u006c\u0075\u006b\u0069\u006e\u0068\u0061\u0035\u0037"});
HackHax.push({GrandesLigas: "\u0042\u0065\u0065\u0074\u0068\u006f\u0076\u0065\u006e",GLH2015: "\u0033\u0038\u0034\u0036\u0031\u0032\u0030\u0034"});
HackHax.push({GrandesLigas: "\u0056\u0072\u0061\u0069\u006b\u0061\u006c",GLH2015: "\u0065\u006e\u007a\u006f\u0033\u0030\u0031\u0033\u0038\u0037\u0031\u0038"});
HackHax.push({GrandesLigas: "\u26a1\uff44\uff52\uff41\uff58\u3000\u6e29\u30de \u26a1",GLH2015: "\u0074\u0068\u0075\u006e\u0064\u0065\u0072\u0039\u0039\u0030"});
HackHax.push({GrandesLigas: "\u002e\u005f\u002e",GLH2015: "\u0057\u0034\u0047\u0051\u0055\u0055\u0043\u0030\u0045\u0038\u0047\u004e"});
HackHax.push({GrandesLigas: "\u0054\u0068\u006f\u006d\u0061\u0073 \u0053\u0068\u0065\u006c\u0062\u0079",GLH2015: "\u0062\u006f\u0063\u0061\u0063\u0061\u006d\u006f\u0072\u0069\u0073\u0074\u0065\u0065\u006e\u006d\u0061\u0064\u0072\u0069\u0064"});
HackHax.push({GrandesLigas: "\ud835\ude4b\ud835\ude5e\ud835\ude65\ud835\ude56\ud835\ude47\ud835\ude6a\ud835\ude58\ud835\ude58\ud835\ude56",GLH2015: "\u0073\u0063\u0068\u0032\u0030\u0030\u0031"});
HackHax.push({GrandesLigas: "\u0041\u006c\u0065\u0078\u0069\u0073 \u004d\u0061\u0063 \u0041\u006c\u006c\u0069\u0073\u0074\u0065\u0072",GLH2015: "\u0042\u0072\u0069\u0067\u0068\u0074\u006f\u006e"});
HackHax.push({GrandesLigas: "\u006b\u0075\u0073\u0061",GLH2015: "\u0066\u0061\u0063\u0075\u006e\u0064\u006f\u0031\u0036"});
HackHax.push({GrandesLigas: "\u0074\u006f\u0062\u0079 \u0064\u0072\u0061\u006d\u0061\u0073",GLH2015: "\u0074\u006f\u0062\u0079\u0031\u0064\u0072\u0061\u006d\u0061\u0073"});
HackHax.push({GrandesLigas: "\u006a\u006f\u0061\u006f\u007a\u0069\u0074\u006f \u002d \u0041\u0064\u0065\u0075\u0073 \u0076\u00f4 \u003c\u0033",GLH2015: "\u006a\u006f\u0061\u006f\u007a\u0069\u006e\u0068\u006f\u0032\u0030\u0030\u0035"});
HackHax.push({GrandesLigas: "\u0056\u0072\u0073\u0061\u006c\u006a\u006b\u006f",GLH2015: "\u0062\u006f\u0062\u006d\u0061\u0072\u0031\u0033\u0031\u0037"});
HackHax.push({GrandesLigas: "\u0056\u0065\u0072\u0068",GLH2015: "\u0073\u006b\u0079\u0070\u0065\u0037\u0036\u0038"});
HackHax.push({GrandesLigas: "\u0042\u0068\u0065\u0072\u0067\u0061\u0064\u006f\u0072",GLH2015: "\u0062\u0068\u0065\u0072\u0067\u0061"});
HackHax.push({GrandesLigas: "\u0046\u0061\u0063\u0075\u0047\u0061\u006d\u0065\u0072",GLH2015: "\u004e\u0053\u004d"});
HackHax.push({GrandesLigas: "\u0053\u0063\u0073\u007a\u0065\u0073\u006e\u0079 \u0031",GLH2015: "\u0066\u0061\u0072\u0063\u0072\u0079"});
HackHax.push({GrandesLigas: "\u0041\u006e\u0074\u006f\u006e\u0061\u0073\u006b\u0069",GLH2015: "\u0062\u006f\u006f\u006b\u0065\u0072\u0030\u0037"});
HackHax.push({GrandesLigas: "\u0050\u0061\u0076\u0065\u006c \u004e\u0065\u0064\u0076\u011b\u0064",GLH2015: "\u0050\u0061\u0076\u0065\u006c \u004e\u0065\u0064\u0076\u011b\u0064"});
HackHax.push({GrandesLigas: "\u3010\uff2e\uff2b\u3011\u2122",GLH2015: "\u0061\u0067\u0075\u0073\u0033\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u006b\u0061\u006f\u0073",GLH2015: "\u0031\u0032\u0074\u0072\u0065\u0073"});
HackHax.push({GrandesLigas: "\u0057\u006f\u0073",GLH2015: "\u0056\u0061\u006d\u006f\u0073\u006d\u0069\u006c\u006c\u006f"});
HackHax.push({GrandesLigas: "\ud835\udc12\ud835\udc22\ud835\udc33\ud835\udc2e\ud835\udc27\ud835\udc28 \u2022 \ud835\udc08\ud835\udc1d\ud835\udc0c",GLH2015: "\u0071\u0031\u0077\u0032\u0065\u0033\u0061\u0073\u0064\u0036\u0038"});
HackHax.push({GrandesLigas: "\u0041\u0274\u1d1b\u1d0f\u0274\u1d00\u0073\u1d0b\u026a",GLH2015: "\u006d\u0065\u0073\u0073\u0069\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0072\u006f\u0064\u0072\u0031\u006b",GLH2015: "\u0063\u0061\u0063\u0061\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0064\u0061\u0072\u0074\u0068 \u0076\u0065\u0072\u0067\u0061",GLH2015: "\u0064\u0061\u0072\u0074\u0068\u0076\u0065\u0072\u0067\u0061\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0063\u006c\u006f\u006e\u006e",GLH2015: "\u0055\u0043\u006c\u006f\u006e\u006e\u0035"});
HackHax.push({GrandesLigas: "\u004c\u0061\u0075\u0074\u0061\u0061",GLH2015: "\u006d\u0065\u0067\u0075\u0073\u0074\u0061\u0065\u006c\u0066\u0075\u0074\u0062\u006f\u006c\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0052\u0061\u0073\u0073\u0068\u006f\u005f",GLH2015: "\u0031\u0035\u0038\u0061\u006d\u0032\u0030\u0031\u0039"});
HackHax.push({GrandesLigas: "\ud835\udcb1\u1d00\u029f\u1d07\u0274\u1d1b\u026a\u0274\u1d0f",GLH2015: "\u0070\u0061\u006a\u0061\u0072\u006f\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0043\u0045\u0043\u0069\u0067\u006f\u006f\u0072",GLH2015: "\u0035\u0033\u0039\u0039\u0033\u0032\u0030"});
HackHax.push({GrandesLigas: "\u0054\u0068\u0065\u0055\u006e\u006b\u006e\u006f\u0077\u006e",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0038\u0073\u0061\u006d\u0069\u0072\u0076"});
HackHax.push({GrandesLigas: "\u0054\u006f\u006b\u0063\u007a\u0069\u006b\u006f",GLH2015: "\u0074\u0061\u0064\u0065\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0070\u0065\u0072\u006f\u0274\u0069\u0455\u0442\u03b1",GLH2015: "\u0052\u0069\u0076\u0065\u0072\u0050\u006c\u0061\u0074\u0065\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0043\u0068\u0069\u006c\u0065\u0042\u0061\u0074\u0074\u006c\u0065\u0052",GLH2015: "\u006d\u0061\u0074\u0069\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0076\u0061\u006c\u0065\u006e\u0074\u0069\u006e\u006f\u0073\u0073\u006a",GLH2015: "\u0063\u0068\u0069\u006c\u0065\u0063\u0068\u0069\u006c\u0065\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0077\u0069\u0064\u006e\u0065\u0079\u0062\u0072",GLH2015: "\u0077\u0069\u0064\u006e\u0065\u0079\u0030\u0037"});
HackHax.push({GrandesLigas: "\u006e\u00f3\u0065\u0073\u0069\u0073 \u0079 \u006e\u00f3\u0065\u006d\u0061",GLH2015: "\u0063\u006c\u0061\u0076\u0065\u006c\u0068\u0065\u0063\u0068\u0069\u007a\u0061\u0064\u006f"});
HackHax.push({GrandesLigas: "\u0048\u0073\u006f",GLH2015: "\u006a\u0069\u0074\u006f\u0039"});
HackHax.push({GrandesLigas: "\u0044\u0065\u006e\u00ed\u0073 \u0043\u0068\u00e9\u0072\u0079\u0073\u0068\u0065\u0076",GLH2015: "\u004e\u0075\u006d\u0065\u0072\u006f\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0076\u0069\u0063\u006d\u0070\u0033",GLH2015: "\u0056\u0031\u0063\u004d\u0070\u0033"});
HackHax.push({GrandesLigas: "\u004c\u0065\u0061\u006e\u0074",GLH2015: "\u0073\u0061\u006e\u0074\u0079\u0074\u0068\u006f\u006d\u0061\u0073\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u00a7\u0043\u00e1\u006e\u0063\u0065\u0072\u00a7",GLH2015: "\u0063\u0061\u006e\u0063\u0065\u0072\u006c\u0061\u006c\u0065\u0079\u0065\u006e\u0064\u0061"});
HackHax.push({GrandesLigas: "\u004c\u0045\u0043\u0048\u0055\u0047\u0049\u0054\u0041",GLH2015: "\u0065\u0064\u0075\u0061\u0072\u0064\u006f\u0065\u006e\u0064\u006f"});
HackHax.push({GrandesLigas: "\u0054\u006b\u0053",GLH2015: "\u0063\u0061\u0063\u0061\u0063\u0061\u0063\u0061\u0031"});
HackHax.push({GrandesLigas: "\u24bd\u24d0\u24df\u24df\u24d8\u24d4\u24e1",GLH2015: "\u0063\u006f\u0072\u0063\u006f\u0076\u0061\u0031"});
HackHax.push({GrandesLigas: "\u0056\u002e\u0050\u0065\u0072\u0073\u0069\u0065",GLH2015: "\u006c\u0061\u0075\u0074\u0061\u0072\u006f\u0031"});
HackHax.push({GrandesLigas: "\u006b\u0075\u0073\u0061",GLH2015: "\u0066\u0061\u0063\u0075\u006e\u0064\u006f\u0031\u0036"});
HackHax.push({GrandesLigas: "\u0062\u0061\u0075\u0064\u0065\u006c\u0061\u0069\u0072\u0065",GLH2015: "\u0062\u0061\u0075\u0064\u0065\u006c\u0061\u0069\u0072\u0065\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0046\u1d07\u1d05\u1d07 \u0056\u1d00\u029f\u1d20\u1d07\u0280\u1d05\u1d07",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0065\u006d\u0069"});
HackHax.push({GrandesLigas: "\u0045\u006d\u0069\u0069",GLH2015: "\u0045\u006d\u0069\u0069\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0044\u0069\u0061\u006c\u006d\u0075\u006e",GLH2015: "\u0044\u0069\u0061\u006c\u006d\u0075\u006e"});
HackHax.push({GrandesLigas: "\u0046\u0065\u0072\u0072\u0065\u0079",GLH2015: "\u006c\u0061\u0063\u0061\u0063\u0061\u0034\u0033"});
HackHax.push({GrandesLigas: "\u0042\u006f\u0075",GLH2015: "\u004e\u0061\u0063\u0068\u006f\u0032\u0030\u0030\u0031"});
HackHax.push({GrandesLigas: "\u0041\u0044\u0045\u004c\u0041\u004e\u0054\u0045 \u0053\u0049\u0045\u004d\u0050\u0052\u0045",GLH2015: "\u0039\u0031\u0036\u0037\u0036\u0031\u0037\u0031\u0061"});
HackHax.push({GrandesLigas: "\u0041\u0072\u0074\u0075\u0072 \u005a\u0061\u006e\u0061\u0074\u0074\u0061",GLH2015: "\u0070\u0075\u0063\u0063\u0061\u0062\u0069\u0061"});
HackHax.push({GrandesLigas: "\u0063\u0072\u0069\u0073\u0074\u0069\u0061\u006e\u006f \u006d\u0065\u0073\u0073\u0069\u006e\u0061\u006c\u0064\u006f \u006a\u0072",GLH2015: "\u006c\u0069\u006f\u006e\u0065\u006c \u006d\u0065\u0073\u0073\u0069"});
HackHax.push({GrandesLigas: "\u0050\u0061\u0072\u006b \u0043\u0068\u0075\u002d\u0059\u006f\u0075\u006e\u0067",GLH2015: "\u0062\u006f\u0063\u0061\u006d\u006f\u0072\u0069\u0073\u0074\u0065\u0065\u006e\u006d\u0061\u0064\u0072\u0069\u0064\u0039\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0064\u0061\u006e\u0074\u0065",GLH2015: "\u0064\u0061\u006e\u0074\u0065\u0030\u0030\u0030\u0031"});
HackHax.push({GrandesLigas: "\u0073\u1d00\u026a\u028f\u1d00\u1d0a\u026a\u0274",GLH2015: "\u0031\u0034\u0035\u006f\u0072\u0073\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0048\u0075\u0067\u006f \u0042\u006f\u0073\u0073 \u00ae",GLH2015: "\u0061\u0062\u0063\u0064\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0042\u0072\u0079\u0061\u006e\u0074\u004d\u0079\u0065\u0072\u0073\ud83d\ude0e",GLH2015: "\u0054\u0065\u0056\u0061\u0073\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0074\u0068\u0065\u0075\u0073 \u0043\u0075\u006e\u0068\u0061",GLH2015: "\u006f\u0074\u0061\u0076\u0069\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0050\u0061\u006a\u0061\u0072\u0069\u0074\u006f \u0076\u0061\u006c\u0076\u0065\u0072\u0064\u0065",GLH2015: "\u0070\u0061\u006a\u0061\u0072\u0069\u0074\u006f"});
HackHax.push({GrandesLigas: "\u0049\u0073\u0061\u0061\u0063 \u0041\u0073\u0069\u006d\u006f\u0076",GLH2015: "\u0065\u006e\u0074\u0072\u006f\u0070\u0069\u0061"});
HackHax.push({GrandesLigas: "\u0051\u0075\u0065\u0065\u006e\u0073\u0072\u00ff\u0063\u0068\u0065",GLH2015: "\u0063\u006f\u006d\u0070\u0075\u0032\u0030\u0032\u0031"});
HackHax.push({GrandesLigas: "\u0056\u0069\u0074\u00e3\u006f \u00ae \u2022 \u0041",GLH2015: "\u0072\u006f\u0076\u0069\u0074"});
HackHax.push({GrandesLigas: "\u0048\u0061\u0076\u0065\u0072\u0074\u007a",GLH2015: "\u0072\u0069\u0076\u0065\u0072\u0070\u006c\u0061\u0074\u0065\u0031\u0033"});
HackHax.push({GrandesLigas: "\u0070\u006c\u0061\u0079",GLH2015: "\u0070\u006c\u0061\u0079\u0065\u006c\u006d\u0065\u006a\u006f\u0072"});
HackHax.push({GrandesLigas: "\u0045\u006d\u0061\u005f\u0039\u0036",GLH2015: "\u0031\u0035\u0036\u0038\u0036\u0032\u0037\u0039\u0031\u0035"});
HackHax.push({GrandesLigas: "\u004f\u0072\u0075\u0061\u006d",GLH2015: "\u006d\u0061\u0075\u006c\u0065\u006f\u0064\u0075\u0061\u0072\u0074\u0065\u0031\u0032"});
HackHax.push({GrandesLigas: "\u003e\u003e\u003e\u0043\u0041\u0052\u004c\u004f\u0053\u003c\u003c\u003c",GLH2015: "\u0046\u0061\u006d\u0069\u006c\u0069\u0061\u004d\u0069\u0072\u0061\u006e\u0064\u0061"});
HackHax.push({GrandesLigas: "\u0042\u1d0f\u1d0f\u1d0d\u1d07\u0280\u004a",GLH2015: "\u006e\u0069\u0072\u0076\u0061\u006e\u0061\u0067\u0072\u0065\u0065\u006e\u0064\u0061\u0079\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0044 \u0059 \u0042 \u0041 \u004c \u0041",GLH2015: "\u004d\u0065\u0067\u0061\u004e\u006f\u0076\u006f"});
HackHax.push({GrandesLigas: "\u004b\u0069\u03c9\u0069",GLH2015: "\u0063\u0075\u0063\u0061\u0072\u0061\u0063\u0068\u0061"});
HackHax.push({GrandesLigas: "\u004e\u0061\u0068\u0075\u0065\u006c",GLH2015: "\u0047\u0052\u0041\u004e\u0044\u0045\u0053\u006c\u0069\u0067\u0061\u0073\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0043\u0061\u0072\u0072\u0061\u0073\u0063\u0061\u006c",GLH2015: "\u0070\u0069\u0073\u0061\u0072\u006c\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0043\u0069\u006c\u0074\u006f\u006e \u004d\u0061\u0073\u0063\u006f",GLH2015: "\u0072\u0069\u0076\u0065\u0072\u0070\u006c\u0061\u0074\u0065\u0032\u0030\u0031\u0034"});
HackHax.push({GrandesLigas: "\u0046\u0065\u006c\u0069 \u004e\u0061\u0063\u0069\u006f\u006e\u0061\u006c\u002e\u0075\u0079",GLH2015: "\u0072\u0061\u0074\u0061\u0074\u0061\u0074\u0061"});
HackHax.push({GrandesLigas: "\u0045\u006c \u0044\u0079\u006c\u0061\u006e\u221a",GLH2015: "\u0064\u0079\u006c\u0061\u006e\u0031\u0031\u0030\u0035\u0031\u0031\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0074\u006f\u0070\u0068\u0027\u0073 \u0062\u0066",GLH2015: "\u0032\u0039\u0030\u0039\u0039\u0032"});
HackHax.push({GrandesLigas: "\u0066\u0069\u0073\u0068",GLH2015: "\u0062\u006f\u006b\u0075\u006e\u006f\u0068\u0065\u0072\u006f"});
HackHax.push({GrandesLigas: "\u006d\u006f\u0064\u0072\u0069\u0063",GLH2015: "\u006d\u006f\u0064\u0072\u0069\u0063\u0072\u006f\u0063\u006b\u006f"});
HackHax.push({GrandesLigas: "\u0048\u0061\u0076\u0065\u0072\u0074\u007a \u0023\u0032\u0039",GLH2015: "\u0072\u0069\u0076\u0065\u0072\u0070\u006c\u0061\u0074\u0065\u0031\u0038"});
HackHax.push({GrandesLigas: "\u0074\u0075\u0070\u0061\u0063\u005f\u0067\u006f\u0064",GLH2015: "\u0074\u0075\u0070\u0061\u0063"});
HackHax.push({GrandesLigas: "\u0056\u006f\u0072\u0065\u006e",GLH2015: "\u0031\u0033\u0030\u0038"});
HackHax.push({GrandesLigas: "\ud835\udcd3\ud835\udd02\ud835\udceb\ud835\udcea\ud835\udcf5\ud835\udcea\u1d5b\u1d43\u1d56\u1d52",GLH2015: "\u0044\u0045\u004c\u0054\u0041"});
HackHax.push({GrandesLigas: "\u0054\u006f\u0072\u0074\u0069\u006c\u006c\u0061\u0044\u0065\u0054\u006f\u006d\u0061\u0074\u0065\u005f\u0078\u0064",GLH2015: "\u004c\u0065\u0067\u0075\u0069\u007a\u0061\u006d\u006f\u006e\u0030\u0037"});
HackHax.push({GrandesLigas: "\u004c \u0055 \u0043 \u0041 \u0053 \u0042 \u0031 \u0033",GLH2015: "\u006c\u0075\u0063\u0061\u0073\u006a\u006f\u0061\u006f"});
HackHax.push({GrandesLigas: "\u004d\u0069\u0072\u006b\u006f \u0053\u0061\u0072\u0069\u0063",GLH2015: "\u0034\u0033\u0035\u0033\u0031\u0031\u0032\u0036"});
HackHax.push({GrandesLigas: "\u0054\u0068\u006f\u0072\u0066\u0069\u006e\u006e",GLH2015: "\u004c\u0061\u004e\u0075\u006d\u0065\u0072\u006f\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0050\u0061\u006f\u006c\u006f \u0047\u0075\u0065\u0072\u0072\u0065\u0072\u006f",GLH2015: "\u0072\u0061\u0066\u0061\u0065\u006c\u0030\u0037"});
HackHax.push({GrandesLigas: "\u004b\u0079\u004e",GLH2015: "\u0070\u0069\u0074\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u006b\u0072\u0061\u0070\u0061",GLH2015: "\u006b\u0072\u0061\u0070\u0061\u0062\u006f\u006f\u0062\u006f\u0062\u006f\u006f\u0065"});
HackHax.push({GrandesLigas: "\u0063\u0061\u006e\u0061\u0072\u0069\u006f",GLH2015: "\u006c\u0075\u0063\u0069\u0031\u0039\u0039\u0036"});
HackHax.push({GrandesLigas: "\u03df\u0106\u0394\u0197\u00d8\u03df",GLH2015: "\u0070\u0065\u006c\u006f\u0074\u0061\u006e\u0061\u0072\u0061\u006e\u006a\u0061"});
HackHax.push({GrandesLigas: "\u0073\u029c\u1d1c\u028f\u1d00",GLH2015: "\u0061\u0073\u0064\u0071\u0077\u0065"});
HackHax.push({GrandesLigas: "\ud835\udc02\ud835\udc1a\ud835\udc26\ud835\udc29\ud835\udc2e \u2022 \ud835\udc08\ud835\udc1d\ud835\udc0c",GLH2015: "\u0063\u0061\u006d\u0070\u0075\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0040\u005f\u005f\u005f\u005f\u005f\u005f\u005f\u005f\u005f\u005f\u005f\u005f\u005f\u005f\u005f\u005f\u005f\u005f\u005f\u005f\u005f\u0066\u0069\u0073\u0068",GLH2015: "\u0073\u006f\u006c\u006f\u0075\u0063\u006f"});
HackHax.push({GrandesLigas: "\u0058\u002d\u004d\u0045\u004e",GLH2015: "\u0066\u0065\u006c\u0069\u0070\u0069\u006e\u006f\u0033"});
HackHax.push({GrandesLigas: "\u0021\u002d\u004c\u1d1c\u1d04\u029c\u1d0f\u002d\u0021",GLH2015: "\u006c\u0075\u0069\u0073\u0072\u0069\u006f\u0073\u0065\u0063\u006f\u0037"});
HackHax.push({GrandesLigas: "\u0043\u0065\u0062\u006f\u006c\u006c\u0069\u0074\u0061",GLH2015: "\u004d\u0061\u0072\u0034\u0032\u0036\u0034\u0033\u0034\u0031\u0033"});
HackHax.push({GrandesLigas: "\u0046 \u0027 \u004d\u0075\u0072\u0061",GLH2015: "\u0063\u002e\u0072\u006f\u006e\u0061\u006c\u0064\u006f"});
HackHax.push({GrandesLigas: "\u0054\u0069\u0074\u006f \u0046\u006f\u0072\u006d\u0069\u006c\u0069\u0061\u006e\u006f",GLH2015: "\u0073\u0061\u0070\u0065"});
HackHax.push({GrandesLigas: "\u0043\u0061\u006d\u0065\u0072\u0061\u006d\u0061\u006e",GLH2015: "\u006d\u0061\u0074\u0065\u006c\u0030\u0037\u0037"});
HackHax.push({GrandesLigas: "\u0053\u0069\u006c\u006b\u0079",GLH2015: "\u0065\u006e\u007a\u0069\u0032\u0030\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0041\u0044\u0042 \u002d \u0050\u002e \u0050\u006f\u0067\u0062\u0061",GLH2015: "\u0041\u0044\u0042"});
HackHax.push({GrandesLigas: "\ud835\udc00\ud835\udc03\ud835\udc01 \uff5e \ud835\udcab\u002e \ud835\udcab\ud835\ude30\ud835\ude28\ud835\ude23\ud835\ude22",GLH2015: "\u0033\u0038\u0032\u0037\u0039\u0031\u0039\u0032"});
HackHax.push({GrandesLigas: "\u0063\u0072\u0033",GLH2015: "\u006e\u006f\u0074\u0065\u006e\u0067\u006f\u006e\u0069\u006e\u0067\u0075\u006e\u0061"});
HackHax.push({GrandesLigas: "\u006b\u006c\u006f\u0073\u0065 \u0041\u0044\u0042",GLH2015: "\u006d\u0061\u0072\u0069\u0061\u006e\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004d\u0072\u0043\u006f\u006c\u006c\u0069\u0065 \u004c\u0054\u0048\u0043",GLH2015: "\u0066\u0065\u0064\u0065\u0072\u0069\u0063\u006f\u0031"});
HackHax.push({GrandesLigas: "\u0043\u0072\u0069\u0073\u0074\u0069\u0061\u006e\u006f\u004b\u0072\u0061\u0067\u004d\u0065\u006f\u006e",GLH2015: "\u0031\u0032\u0033\u0068\u0064\u0033\u0032\u0031"});
HackHax.push({GrandesLigas: "\u006e\u0069\u0063\u006f \u0074\u0061\u0067\u006c\u0069\u0061\u0066\u0069\u0063\u006f",GLH2015: "\u0061\u0073\u0064\u0032\u0030\u0030\u0032"});
HackHax.push({GrandesLigas: "\u004e\u0049\u0054\u0052\u0034\u004d\u005f\u0058",GLH2015: "\u006d\u0061\u0072\u0074\u0069\u006e\u0031\u0031\u0032\u0035"});
HackHax.push({GrandesLigas: "\u006c\u006f\u006e\u0078\u006c\u0079\u0062\u006f\u0079",GLH2015: "\u0063\u0061\u0073\u0061\u006e\u006f\u0076\u0061\u0032\u0030\u0030\u0035"});
HackHax.push({GrandesLigas: "\u0043\u0072\u0069\u006d\u0069\u006e\u0061\u006c\u004d\u0061\u006d\u0062\u0061",GLH2015: "\u0031\u0032\u0033\u0031\u0032\u0033\u0071\u0077\u0065\u0072"});
HackHax.push({GrandesLigas: "\u0053\u0065\u0062\u0061\u0061",GLH2015: "\u0065\u006c\u0068\u006f\u0062\u0062\u0069\u0074"});
HackHax.push({GrandesLigas: "\u0043\u006a\u006f\u0077",GLH2015: "\u006d\u0065\u0069\u006e\u0065\u006c\u0069\u0065\u0062\u0065\u0031\u0035\u0036"});
HackHax.push({GrandesLigas: "\u0065\u0072\u006c\u0069\u006e\u0067 \u0052\u0075\u0062\u0079 \u0052\u0045\u0044",GLH2015: "\u0032\u0033\u0035\u0036\u0031\u0039\u0036\u0035"});
HackHax.push({GrandesLigas: "\u0262\u1d0f\u1d05\u1d0f\u0192\u0280\u1d07\u1d05\u1d0f",GLH2015: "\u0076\u0072\u0075\u0066\u0072\u0065\u0064\u006f"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0076\u0069\u006e \u0048\u0061\u0072\u0072\u0069\u0073",GLH2015: "\u0070\u006f\u0072\u0074\u006f\u0073\u0065\u0063\u006f"});
HackHax.push({GrandesLigas: "\u004d\u018c\u13a1\u0d1f\u13bb\u018c\u1e36",GLH2015: "\u0032\u0039\u0031\u0031\u0030\u0032\u0032\u0035\u0032\u0039\u0067\u0067"});
HackHax.push({GrandesLigas: "\u0391\u0501\u006f\u006c\u0066\u006f \u13c0\ud835\uddba\ud835\uddc2\ud835\uddbc\ud835\uddc1",GLH2015: "\u0065\u006c\u0074\u0061\u006c\u0061\u0031\u0034\u0032\u0034"});
HackHax.push({GrandesLigas: "\u0048\u0069\u0067\u0075\u0061\u0069\u006e \u20ac\u004c \u0050\u20ac\u0050\u00d8 \u1d40\u1d50\u1d9c",GLH2015: "\u0068\u0069\u0067\u0075\u0061\u0069\u006e\u0065\u006c\u0070\u0065\u0070\u006f"});
HackHax.push({GrandesLigas: "\ud835\udd6f\ud835\udd86\ud835\udd93\ud835\udd99\ud835\udd8a\ud835\udd8d",GLH2015: "\u0074\u0065\u006c\u0065\u0076\u0069\u0073\u006f\u0072\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\ud835\uddfa\u0061\u0493\u0071",GLH2015: "\u0073\u0075\u0061\u0073\u0065\u006e\u0068\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0041\u0062\u0075\u0065\u006c\u006f",GLH2015: "\u0063\u006c\u0061\u0075\u0064\u0069\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u006c\u0075\u0063\u0061\u0073 \u006b\u0068\u0061\u0064\u006f\u0075\u0072",GLH2015: "\u006b\u006b\u006b\u006b\u006b\u006b\u006b\u006b"});
HackHax.push({GrandesLigas: "\u1d0d\u1d00\u0280\u1d0f",GLH2015: "\u006d\u0061\u0072\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0043\u006f\u006c\u006c",GLH2015: "\u0068\u0075\u0061\u0069\u0072\u0061\u0030\u0034"});
HackHax.push({GrandesLigas: "\u004c\u0065\u0065",GLH2015: "\u006d\u0061\u0074\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0047\u0072\u0065\u0063\u006f",GLH2015: "\u0050\u0061\u006e\u0074\u0061\u006e\u006f\u0073\u006f\u0030\u0021"});
HackHax.push({GrandesLigas: "\u0063\u0064\u006e \u0073\u0065\u0074\u0065\u006c\u0065\u0072\u0073",GLH2015: "\u004e\u0061\u0063\u0068\u0069\u0074\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0073\u0061\u006c\u006f\u006d\u006f\u006e\u0065",GLH2015: "\u0073\u0061\u006c\u006f\u006d\u006f\u006e\u0065\u0032\u0030\u0030\u0032"});
HackHax.push({GrandesLigas: "\u0050\u0065\u0064\u0072\u0069\u006e\u0068\u006f",GLH2015: "\u006e\u0065\u0067\u006f\u002e\u0069\u0074\u0061\u006c\u006f"});
HackHax.push({GrandesLigas: "\u004a\u006f\u0072\u006d\u0061\u006e \u0043\u0061\u006d\u0070\u0075\u007a\u0061\u006e\u006f",GLH2015: "\u0063\u0061\u006d\u0070\u0075\u007a\u0061\u006e\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004d\u006f\u0072\u0061\u0074\u0061",GLH2015: "\u0073\u0061\u006e\u0066\u0072\u0061\u006e\u0063\u0069\u0073\u0063\u006f"});
HackHax.push({GrandesLigas: "\u0053\u006c\u0061\u0076\u006f\u006a \u017d\u0069\u017e\u0065\u006b",GLH2015: "\u0036 \u0037 \u0038 \u004f\u006e\u0065"});
HackHax.push({GrandesLigas: "\u004c\u0069\u0061\u006d \u0047\u0061\u006c\u006c\u0061\u0067\u0068\u0065\u0072",GLH2015: "\u0074\u0068\u0065\u0062\u0065\u0061\u0074\u006c\u0065\u0073\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0048\u0061\u0061\u006c\u0061\u006e\u0501",GLH2015: "\u0045\u0072\u006c\u0069\u006e\u0067\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0074\u0072\u0061\u0076\u0069\u0073 \u0073\u0063\u006f\u0074\u0074",GLH2015: "\u006d\u0069\u006c\u0074\u006f\u006e"});
HackHax.push({GrandesLigas: "\u0041\u0067\u0075\u0065\u0072\u0072\u0065",GLH2015: "\u0065\u006d\u0069\u006c\u0069\u0061\u006e\u006f\u0032\u0031\u0030\u0037"});
HackHax.push({GrandesLigas: "\u004b\u0065\u006e\u0064\u0072\u0069\u0063\u006b",GLH2015: "\u0034\u0031\u0039\u0032\u0031\u0035\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0052\u0061\u0073\u0074\u0061",GLH2015: "\u0064\u006f\u006c\u0061\u0070\u0065\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u2022\u005a\u0075\u0072\u0064\u006f\u2022",GLH2015: "\u007a\u0075\u0072\u0064\u006f\u0032\u0030\u0030\u0036"});
HackHax.push({GrandesLigas: "\u006e\u0065\u0067\u0075\u0065\u0062\u0061",GLH2015: "\u006e\u0065\u002e\u0067\u0075\u0065\u002e\u0062\u0061\u002e\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0047\u006f\u006e\u007a\u0061\u004d\u0065\u0064\u0069\u006e\u0061",GLH2015: "\u0061\u0072\u0067\u0065\u006e\u0074\u0069\u006e\u0061\u0031\u0030"});
HackHax.push({GrandesLigas: "\u004b\u0041\u0052\u004d\u0041",GLH2015: "\u0066\u0069\u006c\u006d\u0061\u0068\u0061\u0078\u0031"});
HackHax.push({GrandesLigas: "\u006c\u0075\u0073\u0068\u006f",GLH2015: "\u0073\u0061\u006e\u0074\u0069\u0061\u0067\u006f\u0031\u0039\u0034\u0031\u0032\u0030\u0031\u0034"});
HackHax.push({GrandesLigas: "\u0050\u006f\u006c\u0069\u006c\u006c\u0061",GLH2015: "\u0070\u0075\u006d\u0061\u0031\u0030"});
HackHax.push({GrandesLigas: "\u0062\u0061\u0072\u0064\u006f\u0063\u006b",GLH2015: "\u0031\u0038\u0032\u0031\u0030\u0037"});
HackHax.push({GrandesLigas: "\u0056\u0041\u004d\u0054\u0049\u0052\u004f",GLH2015: "\u0067\u0072\u0061\u0063\u0069\u0065\u006c\u0061\u0031\u0032\u0033\u0035\u0034"});
HackHax.push({GrandesLigas: "\u0041\u006c\u0065\u0078 \u2022 \u0043\u0048\u0049",GLH2015: "\u0061\u006c\u006f\u006e\u0073\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0053\u0069\u006e\u0061\u006d\u0061\u002d\u0050\u006f\u006e\u0067\u006f\u006c\u006c\u0065",GLH2015: "\u0062\u006f\u0063\u0061\u006d\u0075\u0065\u0072\u0074\u006f\u0065\u006e\u006d\u0061\u0064\u0072\u0069\u0064"});
HackHax.push({GrandesLigas: "\u0432\u03c5\u0455\u0442\u006f\u0455",GLH2015: "\u0061\u0073\u0064\u0032\u0030\u0030\u0032\u0061\u0073\u0064"});
HackHax.push({GrandesLigas: "\u0053\u0068\u0061\u0077\u0065\u006e\u0052\u0065\u0066\u0065\u0073\u0061\u0076",GLH2015: "\u006d\u0061\u0078\u0073\u0074\u0065\u006c\u006c\u0035"});
HackHax.push({GrandesLigas: "\u0053\u0069\u006d\u006f\u006e \u004b\u006a\u0061\u0065\u0072",GLH2015: "\u0061\u006d\u0030\u0038\u0030\u0038"});
HackHax.push({GrandesLigas: "\u0054\u0065\u0079\u006b\u0065\u0072\u0047\u0048\u0054\u0053",GLH2015: "\u0042\u0069\u0063\u0061\u006d\u0070\u0065\u006f\u006e\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u041d\u00e5\u006c\u0061\u006e\u0064",GLH2015: "\u0073\u0065\u0062\u0061\u0076\u0061"});
HackHax.push({GrandesLigas: "\ud835\udfca\u006f\u0072\u0065\u0073\u0074\u0065\u0072",GLH2015: "\u0074\u006f\u006d\u0040\u0073\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0046\u006f\u0072 \u0061\u006c\u006c \u0077\u006f\u006d\u0065\u006e",GLH2015: "\u0063\u0065\u0063\u0039\u0037\u0030\u0033"});
HackHax.push({GrandesLigas: "\u0065\u0072\u006c\u0069\u006e\u0067 \u0052\u0075\u0062\u0079 \ud83d\udd34",GLH2015: "\u0032\u0033\u0035\u0036\u0031\u0039\u0036\u0035\u0078"});
HackHax.push({GrandesLigas: "\u0045\u006c \u006e\u0065\u0067\u0072\u006f \u0047\u0075\u006c\u006c\u0069\u0074",GLH2015: "\u0033\u0037\u0032\u0031\u0036\u0030\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0041\u0061\u0072\u006f\u006e \u0052\u006f\u0064\u0067\u0065\u0072\u0073",GLH2015: "\u0066\u006f\u0072\u006d\u0075\u006c\u0061\u0031\u0069\u006e\u0074\u0065\u0072\u006c\u0061\u0067\u006f\u0073"});
HackHax.push({GrandesLigas: "\u006b\u0065\u0069\u006f\u0075",GLH2015: "\u0063\u0068\u0061\u0076\u006f\u0073\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u13f0\u03b1\u0280\u1e09\u03b1",GLH2015: "\u0034\u0037\u0034\u0038\u0031\u0032\u0037\u0035"});
HackHax.push({GrandesLigas: "\u0043\u0068\u0072\u006f\u006e\u006f\u0073 \u0041\u0065\u006f\u006e",GLH2015: "\u0044\u0065\u0073\u0074\u0072\u0075\u0069\u0072\u0036\u0037\u0036"});
HackHax.push({GrandesLigas: "\u004c\u0075\u006b\u0061 \u0044\u006f\u006e\u010d\u0069\u0107",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0041"});
HackHax.push({GrandesLigas: "\u0053\u0069\u0063\u0061\u0072\u0069\u006f \u0072\u006f\u006a\u0061\u0073",GLH2015: "\u0067\u006f\u006e\u007a\u0061\u006c\u006f\u0032\u0030\u0032\u0030"});
HackHax.push({GrandesLigas: "\u0054\u0068\u0069\u0061\u0067\u006f\u005f\u0041\u006c\u006d\u0061\u0064\u0061",GLH2015: "\u0056\u0065\u006c\u0065\u007a\u0032\u0030\u0031\u0034"});
HackHax.push({GrandesLigas: "\u0064\u0072\u0073\u0074\u0072\u0061\u006e\u0067\u0065\u006c\u006f\u0076\u0065",GLH2015: "\u0064\u0061\u006d\u0069\u0032\u0030\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0046\u0061\u006c\u0063\u00e3\u006f \u004d\u0041\u0045\u0053\u0054\u0052\u004f",GLH2015: "\u0068\u0061\u0078"});
HackHax.push({GrandesLigas: "\u0050\u0041\u0052\u0055\u005a\u005a\u004f",GLH2015: "\u0074\u0069\u0067\u0072\u0065\u0032\u0030\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0045\u0075\u006c\u0065\u0072",GLH2015: "\u004c\u0065\u006f\u006e\u0065\u006c\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004f\u006b\u006e\u0065\u0073",GLH2015: "\u0064\u0065\u0072\u0075\u0074\u0061\u0064\u0065\u006e\u0061\u007a\u0069\u0064\u0065\u0072\u0075\u0074\u0061"});
HackHax.push({GrandesLigas: "\u0067\u0061\u0062\u0072\u0069\u0065\u006c\u0072\u006f\u006a\u0061\u0073\u0037\u0037\u0037\u0037",GLH2015: "\u0031\u0030\u0030\u0035\u0039\u0039\u0072\u0075"});
HackHax.push({GrandesLigas: "\u271e\ua9c1\u0f12\ud83c\uddf9 \ud83c\udded \ud83c\uddea  \ud83c\udde9 \ud83c\uddf4 \ud83c\uddec \u0f12\ua9c2\u271e",GLH2015: "\u0062\u0069\u0065\u006c\u0030\u0031\u0031\u0037"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0072\u0063\u0065\u006c\u006f \u004d\u006f\u0072\u0065\u006e\u006f",GLH2015: "\u0070\u006f\u0072\u0074\u006f\u0073\u0065\u0063\u006f\u0031\u0036"});
HackHax.push({GrandesLigas: "\u0053\u0072\u002e \u0044\u0061\u006d\u0061\u0073\u0063\u0065\u006e\u006f",GLH2015: "\u006b\u0061\u0079\u0071\u0075\u0065\u0064\u0061\u006d\u0061\u0073\u0063\u0065\u006e\u006f"});
HackHax.push({GrandesLigas: "\u0042\u0076\u0073\u0068\u0033",GLH2015: "\u006d\u0061\u0074\u0069\u0032\u0036\u0032\u0035"});
HackHax.push({GrandesLigas: "\u0047\u006f\u006e\u007a\u0069",GLH2015: "\u0065\u006c\u0073\u0065\u00f1\u006f\u0072\u0064\u0065\u006c\u006f\u0073\u0061\u006e\u0069\u006c\u006c\u006f\u0073"});
HackHax.push({GrandesLigas: "\ud835\udde1\ud835\uddee\ud835\uddf0\ud835\uddf5\ud835\uddfc \u2022 \ud835\udc08\ud835\udc1d\ud835\udc0c",GLH2015: "\u0068\u006f\u006c\u0061\u006b\u0068\u0061\u0063\u0065\u0031\u0033"});
HackHax.push({GrandesLigas: "\u0057\u002e\u004d\u006f\u006e\u0074\u0069\u006c\u006c\u006f",GLH2015: "\u0063\u0079\u006a\u0031\u0030\u0030\u0033\u0031\u0039"});
HackHax.push({GrandesLigas: "\u0049\u0073\u0061\u0061\u0063\u0045\u0053\u0050",GLH2015: "\u0075\u006e\u0069\u006f\u006e\u0032\u0030\u0031\u0033"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0074\u0069\u0061\u0073 \u0053\u0075\u00e1\u0072\u0065\u007a",GLH2015: "\u0072\u0069\u0076\u0065\u0072\u0070\u006c\u0061\u0074\u0065\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0045\u006c \u004d\u0061\u0072\u0063\u006f\u0073",GLH2015: "\u0031\u0037\u0031\u0031\u0030\u0038"});
HackHax.push({GrandesLigas: "\u0058\u0044\u004d\u0041\u0055\u0042\u0045\u0052\u0054\u0058\u0044",GLH2015: "\u0053\u0049\u004d\u004f\u004e\u0031\u0039\u0033\u0035\u002a"});
HackHax.push({GrandesLigas: "\u0041\u0062\u006f\u0075\u0074 \u004d\u0061\u006e\u0069",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0036\u0062\u0072"});
HackHax.push({GrandesLigas: "\u004e\u006f\u006f\u0062",GLH2015: "\u0031\u0032\u006d\u0061\u0078\u0069\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0054\u0061\u0062\u0075\u0063\u0068\u0069",GLH2015: "\u0063\u0075\u0065\u0072\u006e\u006f\u0031\u0037"});
HackHax.push({GrandesLigas: "\u13a2\u0061\u0062\u0075\u0063\u0068\u0069",GLH2015: "\u0074\u0061\u0062\u0075\u0063\u0068\u0069\u0031\u0037"});
HackHax.push({GrandesLigas: "\u0063\u006f\u0073\u006e\u006f\u006e\u0069\u0073",GLH2015: "\u0067\u0061\u0062\u0072\u0069\u0065\u006c\u0030\u0039"});
HackHax.push({GrandesLigas: "\u0062\u0065\u006e\u006a\u0061\u006d\u0069\u006e",GLH2015: "\u0070\u0065\u0070\u006f\u0070\u0065\u0070\u0069\u006e"});
HackHax.push({GrandesLigas: "\u0056\u0061\u006c\u0063\u0072\u006f\u0053\u0053",GLH2015: "\u004a\u0075\u0061\u006e\u0069\u0045\u0076\u0065\u0072\u0064\u0065\u0065\u006e"});
HackHax.push({GrandesLigas: "\u004c \u004c\u0061\u0077\u006c\u0069\u0065\u0074",GLH2015: "\u006e\u0065\u0061\u0072\u006d\u0065\u006c\u006c\u006f"});
HackHax.push({GrandesLigas: "\ud835\udd6d\ud835\udd70\ud835\udd79\ud835\udd75\ud835\udd6c \ud83c\udfc8\ud83c\udfc8",GLH2015: "\u0062\u0065\u006e\u006a\u0061\u0063\u0030\u0032"});
HackHax.push({GrandesLigas: "\u0052\u004f",GLH2015: "\u0032\u0030\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0440\u0069\u0063\u0068\u0069\u0072\u0069\u0063\u006f \u0065\u006d\u0065 \u006a\u006f\u0074\u006f",GLH2015: "\u0067\u0033\u0036\u0033\u0032\u0039\u0035\u0036\u0037"});
HackHax.push({GrandesLigas: "\u004c\u006f\u0072\u0065\u006e\u007a\u006f\u0031\u0035",GLH2015: "\u0048\u0061\u0078\u0062\u0061\u006c\u006c\u0032\u0030\u0032\u0030"});
HackHax.push({GrandesLigas: "\u0052\u006f\u006e\u0061\u006c\u0064",GLH2015: "\u0030\u0037\u0031\u0037"});
HackHax.push({GrandesLigas: "\u0047\u0078\u0078",GLH2015: "\u0070\u0065\u0073\u0061\u0064\u0069\u006c\u006c\u0061\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0071\u0077\u0065\u0072\u0074\u0079",GLH2015: "\u0070\u0061\u0070\u0061\u0067\u0061\u0069\u006f"});
HackHax.push({GrandesLigas: "\u0062\u0072\u0065\u0065\u0065\u0062\u0072",GLH2015: "\u0062\u0072\u0062\u0072\u0062\u0072"});
HackHax.push({GrandesLigas: "\u0070\u0065\u0072\u006b\u0069\u006e\u0067",GLH2015: "\u0070\u0065\u0072\u006b\u0069\u006e\u0067\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004e\u0048\u0046\u0043\u007c\u005b\u0332\u0305\u004c\u0332\u0305\u0454\u0332\u0305\u0438\u0332\u0305\u0064\u0332\u0305\u03b1 \u270c\u0028\u30c4",GLH2015: "\u0054\u0065\u006c\u0065\u0066\u006f\u006e\u0065\u0032\u0030\u0030\u0037"});
HackHax.push({GrandesLigas: "\u004e\u0039 \u2022 \u004d\u0055",GLH2015: "\u0034\u0036\u0038\u0039\u0035\u0036\u0036\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0054\u002e \u0057\u0065\u0072\u006e\u0065\u0072",GLH2015: "\u0070\u0061\u006c\u0069\u0074\u006f\u0031\u0031\u0039\u0037"});
HackHax.push({GrandesLigas: "\u0041\u0064\u0065\u0073\u0061\u006e\u0079\u0061",GLH2015: "\u0061\u0068\u0070\u0065\u006c\u006f\u0063\u0031\u0039\u0039\u0038"});
HackHax.push({GrandesLigas: "\u0051\u0077\u0061\u0072\u006f",GLH2015: "\u0034\u0038\u0032\u0031\u0039\u0031"});
HackHax.push({GrandesLigas: "\u0073",GLH2015: "\u0032\u0035\u0032\u0035"});
HackHax.push({GrandesLigas: "\u0073\u0069\u006e\u0064\u006f\u0072",GLH2015: "\u0036\u0036\u0034\u0034\u0031\u0031\u0032\u0032"});
HackHax.push({GrandesLigas: "\u0397\u0069\u0072\u0061\u006b\u006f",GLH2015: "\u0039\u0035\u0031\u0037\u0035\u0033\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0061\u006e\u0064\u0072\u0061\u0064\u0061",GLH2015: "\u006c\u0075\u0063\u0068\u006f\u006d\u0061\u0072\u0063\u0075\u0063\u0063\u0069\u0031\u0030"});
HackHax.push({GrandesLigas: "\u004a\u0061\u0064\u006f\u006e \u0053\u0061\u006e\u0063\u0068\u006f",GLH2015: "\u006c\u006f\u006c\u0078\u0064\u006c\u006f\u006c\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u03f9\u0061\u0072\u0065\u0074\u0061\u0073",GLH2015: "\u0076\u0065\u0072\u0064\u0065\u0076\u0065\u0072\u0064\u0065\u0031"});
HackHax.push({GrandesLigas: "\u0043\u0061\u0072\u006c \u0043\u0041\u0042",GLH2015: "\u006d\u0061\u0072\u0074\u0069\u006e\u0076\u0061\u0072\u0065\u006c\u0061\u0039\u0038\u0032\u0030"});
HackHax.push({GrandesLigas: "\u004b\u0065\u0076\u004d\u0069\u0074\u006f",GLH2015: "\u0030\u0031\u0030\u0032\u0030\u0033"});
HackHax.push({GrandesLigas: "\u004d\u0061\u0074\u0069\u0061\u0073 \u0046\u0065\u0072\u006e\u0061\u006e\u0064\u0065\u007a",GLH2015: "\u0072\u006f\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004c\u006f\u006c\u006f \u004d\u0069\u0072\u0061\u006e\u0064\u0061",GLH2015: "\u006c\u006f\u006c\u006f\u0063\u0072\u0061\u0063\u006b"});
HackHax.push({GrandesLigas: "\u16d5\u0065\u006e\u0064\u0072\u0069\u0063\u006b",GLH2015: "\u0031\u0032\u0033\u006e\u006f\u0069\u0061\u0021"});
HackHax.push({GrandesLigas: "\u004e\u0076\u0068\u0075",GLH2015: "\u006e\u006a\u0061\u0077\u0037\u0035\u0033\u0033"});
HackHax.push({GrandesLigas: "\u0047\u0068\u0069\u0072\u006c\u0061\u006e\u0064\u006f\u0077\u0073\u006b\u0079",GLH2015: "\u006f\u0072\u006f\u0032\u0035\u0031\u0031"});
HackHax.push({GrandesLigas: "\u2622 \u0047\u0069\u006f\u0076\u0061\u006e\u006e\u0069 \u0052\u0065\u0079\u006e\u0061 \u2622",GLH2015: "\u0061\u0031\u0062\u0032\u0063\u0033\u0064\u0034"});
HackHax.push({GrandesLigas: "\u0054\u006f\u006d\u00e1\u0073 \u0057\u0065\u0072\u006e\u0065\u0072",GLH2015: "\u0074\u0061\u0070\u0069\u0074\u0061\u0031\u0031\u0039\u0037"});
HackHax.push({GrandesLigas: "\u0076\u00f8\u006c\u0074\u007a",GLH2015: "\u0069\u006e\u0074\u0065\u0072\u006e\u0065\u0074\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u004b\u0061\u006e\u0074\u0065",GLH2015: "\u0030\u0031\u0031\u0030\u0072\u0065\u006e\u0061\u0074\u006f"});
HackHax.push({GrandesLigas: "\u050c\u006f\u006e\u007a\u0069",GLH2015: "\u0032\u0034\u0039\u0033\u0036\u0034\u0036\u0036"});
HackHax.push({GrandesLigas: "\u0053\u0063\u0068\u0077\u0065\u0069\u006e\u0073\u0074\u0065\u0069\u0067\u0065\u0072",GLH2015: "\u0053\u0063\u0068\u0077\u0065\u0069\u006e\u0073\u0074\u0065\u0069\u0067\u0065\u0072\u0031\u0032\u0037"});
HackHax.push({GrandesLigas: "\u007a\u0061\u007a\u0061",GLH2015: "\u007a\u0061\u007a\u0061"});
HackHax.push({GrandesLigas: "\u0046\u0061\u0062\u0072\u006f",GLH2015: "\u0066\u0061\u0062\u0072\u006f\u0068\u0061\u0078\u0062\u0061\u006c\u006c\u0030\u0035\u0030\u0035"});
HackHax.push({GrandesLigas: "\u0068\u0065\u006c\u0061\u0064\u0065\u0072\u006f",GLH2015: "\u0063\u0061\u006d\u0069\u006c\u006f"});
HackHax.push({GrandesLigas: "\u0053\u0041\u0052\u004d\u0049\u0045\u004e\u0054\u004f \u0044\u0045 \u004a\u0055\u004e\u0049\u004e",GLH2015: "\u0053\u0041\u0052\u004d\u0049\u0045\u004e\u0054\u004f\u0044\u0045\u004a\u0055\u004e\u0049\u004e"});
HackHax.push({GrandesLigas: "\u0064\u0075\u0064\u0061\u006d\u0065\u006c",GLH2015: "\u0075\u0072\u0075\u0067\u0075\u0061\u0079\u0032\u0030\u0031\u0038"});
HackHax.push({GrandesLigas: "\u0044\u0061\u006e\u0069\u0065\u006c \u0053\u0063\u0069\u006f\u006c\u0069",GLH2015: "\u0062\u0072\u0061\u007a\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0052\u006f\u006c\u006c\u0065",GLH2015: "\u0076\u0065\u006c\u006f\u0063\u0069\u0072\u0061\u0070\u0074\u006f\u0072\u0032\u0032"});
HackHax.push({GrandesLigas: "\u0043\u0061\u0072\u006c\u006f\u0073 \u0056\u0065\u006c\u0061",GLH2015: "\u006e\u006f\u0074\u0065\u006e\u0067\u006f"});
HackHax.push({GrandesLigas: "\u0050\u0061\u0073\u0074\u0061\u0066\u0072\u006f\u006c\u0061",GLH2015: "\u0046\u0072\u0061\u006e\u0063\u006f\u0031\u0039\u0039\u0037"});
HackHax.push({GrandesLigas: "\u0041\u0072\u006b\u0061\u0064\u0069\u0075\u0073\u007a \u004d\u0069\u006c\u0069\u006b",GLH2015: "\u0076\u0065\u0072\u0064\u0065\u0039\u0030\u0031\u0035"});
HackHax.push({GrandesLigas: "\u004a\u006f\u0074\u0061\u0072\u006f \u004b\u0075\u006a\u006f",GLH2015: "\u004a\u0075\u0061\u006e\u0063\u0069\u0074\u006f\u0032\u0030\u0030\u0039\u0038\u0038\u0030"});
HackHax.push({GrandesLigas: "\u004d\u0065\u006e\u0061",GLH2015: "\u006e\u0069\u0063\u006f\u006c\u0061\u0073\u0068\u0061\u0078\u0062\u0061\u006c\u006c"});
HackHax.push({GrandesLigas: "\u0053\u006f\u0070\u0069\u0074\u0061 \u004b\u0075\u0079\u0074",GLH2015: "\u0063\u0061\u0073\u006c\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0050\u0069\u0062\u0065 \u0064\u0065\u006c \u0056\u0069\u0061\u0064\u0075\u0063\u0074\u006f",GLH2015: "\u0041\u0072\u0073\u0065\u006e\u0061\u006c\u0053\u0061\u0072\u0061\u006e\u0064\u00ed\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0038"});
HackHax.push({GrandesLigas: "\u0065\u006c \u006e\u0065\u0067\u0072\u006f \u0069\u0062\u0061\u0072\u0072\u0061",GLH2015: "\u0042\u004f\u0043\u0041\u0050\u0041\u0053\u0049\u004f\u004e\u006e\u0031\u0039\u0039\u0037"});
HackHax.push({GrandesLigas: "\u0073\u0068\u0061\u0066\u0074\u002e",GLH2015: "\u0050\u0075\u0074\u0069\u0074\u006f\u0031\u0033\u002d"});
HackHax.push({GrandesLigas: "\u0044\u0069\u00f1\u006f",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0036\u0061"});
HackHax.push({GrandesLigas: "\u300a\u0052\u0065\u0064 \u0057\u006f\u006c\u0066\u0073\u300b \u0041\u006c\u0069\u0073\u0073\u006f\u006e \u0048\u0079\u0061\u0067\u006f",GLH2015: "\u0065\u0075\u0067\u006f\u0073\u0074\u006f\u0064\u0065\u0074\u006f\u006d\u0061\u0072\u0063\u0061\u0066\u0065\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0067\u0075\u0069\u0064\u006f \u0063\u0061\u0073\u0070\u0061",GLH2015: "\u006d\u0061\u006e\u0063\u0068\u0061\u0078\u0064\u0031\u0032"});
HackHax.push({GrandesLigas: "\u0052\u0065\u0075\u0073 \u0023\u0031\u0031",GLH2015: "\u0052\u0065\u0075\u0073\u0031\u0031"});
HackHax.push({GrandesLigas: "\u0045\u0073\u0074\u0065\u0062\u0061\u006e \u0041\u006e\u0064\u0072\u0061\u0064\u0061",GLH2015: "\u0042\u004f\u0043\u0041\u004d\u0050\u0052\u004f\u0036\u0037"});
HackHax.push({GrandesLigas: "\u0047\u00f6\u006c\u0065\u0061\u0064\u006f\u0072\u007c\u007c",GLH2015: "\u0070\u0065\u0072\u0072\u0079\u0031\u0033\u0035\u0031"});
HackHax.push({GrandesLigas: "\u127d\u1202\u1293",GLH2015: "\u0075\u006e\u0063\u0068\u0069\u006e\u0069\u0074\u006f"});
HackHax.push({GrandesLigas: "\u0042\u0061\u006c\u0065",GLH2015: "\u006e\u0061\u0063\u0068\u006f\u0078\u0032"});
HackHax.push({GrandesLigas: "\u0053\u006f\u006d\u00e1\u006c\u0069\u0061 \u0039 \u00ae \u0073\u0054",GLH2015: "\u0032\u0032\u0034\u0034\u0039\u0039"});
HackHax.push({GrandesLigas: "\u0047\u0061\u0067\u006f",GLH2015: "\u0066\u0072\u0061\u006e\u0063\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004f\u0062\u006c\u0061\u006b \u0028\u0045\u006c \u006f\u0072\u0069\u0067\u0069\u006e\u0061\u006c\u0029",GLH2015: "\u0039\u0031\u0036\u0037\u0036\u0031\u0037\u0031"});
HackHax.push({GrandesLigas: "\u004f\u0062\u006c\u0061\u006b \u0028\u0045\u006c \u006f\u0072\u0069\u0067\u0069\u006e\u0061\u006c \u0031\u0030\u0030\u0025\u0029",GLH2015: "\u0038\u0039\u0035\u0031\u0030\u0039\u0038\u0031"});
HackHax.push({GrandesLigas: "\u0412\u0061\u006c\u0065",GLH2015: "\u006e\u0075\u0065\u0076\u0065\u0064\u0065\u006c\u0064\u006f\u0063\u0065"});
HackHax.push({GrandesLigas: "\u0053\u0041\u004e \u004d\u0041\u0052\u0049\u004e\u004f",GLH2015: "\u006c\u0061\u006f\u0074\u0072\u0061\u0070\u0061\u0073\u0069\u006f\u006e"});
HackHax.push({GrandesLigas: "\u0041\u0072\u006b\u0061\u0064\u0069\u0075\u0073\u007a\u004d\u0069\u006c\u0069\u006b\u0039\u0039",GLH2015: "\u0072\u006f\u006a\u006f\u0039\u0030\u0031\u0035"});
HackHax.push({GrandesLigas: "\u0142\u0142\u00f8\u004c\u0111",GLH2015: "\u0035\u0037\u0036\u0038\u0039\u0039\u0031\u0038"});
HackHax.push({GrandesLigas: "\u0056\u0069\u0074\u006f \u0053\u0063\u0061\u006c\u0065\u0074\u0074\u0061",GLH2015: "\u0063\u0061\u0063\u0061\u006a\u0072"});
HackHax.push({GrandesLigas: "\u0052\u0079\u0075\u006b\u006f \u004d\u0061\u0074\u006f\u0069",GLH2015: "\u0073\u0033\u006e\u006b\u0065\u0074\u0073\u0075"});
HackHax.push({GrandesLigas: "\u0045\u004c \u0054\u004f\u0052\u004f",GLH2015: "\u0074\u006f\u0072\u006f\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u15e9\u018a\u144c\u5c3a\u5de5\u017b\ud83c\udfb5",GLH2015: "\u0074\u006f\u0074\u006f\u0035\u0038\u0037\u0034"});
HackHax.push({GrandesLigas: "\u13c0\u00f6\u006c\u0065\u0061\u0064\u006f\u0072\u007c\u007c",GLH2015: "\u0074\u0072\u006f\u006c\u006c\u0066\u0061\u0063\u0045"});
HackHax.push({GrandesLigas: "\ud83c\udd71\ud83c\udd74\ud83c\udd70\ud83c\udd83\ud83c\udd88 \u2022 \ud835\udc38\ud835\udc9e",GLH2015: "\u0066\u0072\u0061\u006e\u0032\u0030\u0030\u0034"});
HackHax.push({GrandesLigas: "\u0042\u0065\u0061\u0074\u0079 \u318d \ud835\udc38\ud801\udca8",GLH2015: "\u0066\u0072\u0061\u006e\u0032\u0030\u0032\u0030"});
HackHax.push({GrandesLigas: "\u0052\u0049\u0051\u0055\u0045\u004c\u004d\u0045",GLH2015: "\u0068\u0075\u0072\u0061\u0063\u0061\u006e\u0039"});
HackHax.push({GrandesLigas: "\u007a\u0061\u006e\u0065\u0074\u0074\u0069",GLH2015: "\u006d\u0061\u0063\u0072\u0069\u0067\u0061\u0074\u006f"});
HackHax.push({GrandesLigas: "\u0047\u0046 \u0048\u0065\u0067\u0065\u006c",GLH2015: "\u0031\u0032\u0033\u0034\u0035\u0036\u0037\u0038\u0039\u0030"});
HackHax.push({GrandesLigas: "\u004b\u0069\u006e\u0067 \u0043\u0072\u0069\u006d\u0073\u006f\u006e",GLH2015: "\u0068\u006f\u0072\u0069\u007a\u006f\u006e\u0074\u0065\u0032"});
HackHax.push({GrandesLigas: "\u0054\u0052\u0056\u0050\u0050\u0045\u0052",GLH2015: "\u0073\u0069\u006e\u0064\u0072\u006f\u006d\u0065\u0064\u0065\u0065\u0067\u006f\u0033\u0032\u0031"});
HackHax.push({GrandesLigas: "\u004d\u002e \u0047\u0065\u006c\u006f \u0035",GLH2015: "\u0061\u006e\u0062\u006f\u0038\u0069"});
HackHax.push({GrandesLigas: "\u13c3\u0061\u006e\u0065\u0074\u0074\u0069",GLH2015: "\u0061\u006d\u0061\u0072\u0069\u006c\u006c\u006f\u0039\u0030\u0032\u0030"});
HackHax.push({GrandesLigas: "\u004f\u004d\u0047 \u0069\u0074\u0073 \u004d\u0047\u0035",GLH2015: "\u0063\u0075\u006c\u006f\u0063\u0075\u006c\u006f"});
HackHax.push({GrandesLigas: "\u004d\u0069\u006c\u0061\u006e\u0065\u0073\u0061\u0023\u0034\u0035\u0032\u0030",GLH2015: "\u006a\u006f\u0073\u0065\u006c\u0075\u0069\u0073\u0033\u0037"});
HackHax.push({GrandesLigas: "\u0041\u0044\u0042 \u002d \u004f\u007a\u007a\u0021",GLH2015: "\u0061\u0078\u0065\u006c\u0032\u0039\u0033\u0035"});
HackHax.push({GrandesLigas: "\u0064\u006f\u0073\u0062\u006f\u0074\u0065\u006c\u006c\u0061\u0073",GLH2015: "\u0047\u006f\u006e\u007a\u0061\u006c\u006f\u0031\u0034\u0030\u0031"});
HackHax.push({GrandesLigas: "\u0054\u006f\u006e\u0069 \u004b\u0072\u006f\u006f\u0073 \u007c\u0038\u007c",GLH2015: "\u0054\u006f\u0078\u0069\u0063\u006f\u0073\u0062\u0061\u006e"});
HackHax.push({GrandesLigas: "\u0044\u0065\u0076\u0065\u006e",GLH2015: "\u0064\u0076\u006e\u0064\u0076\u006e"});
HackHax.push({GrandesLigas: "\u0051\u003f",GLH2015: "\u0039\u0035\u0031\u0039\u0035\u0031\u0072\u006f\u0064"});
HackHax.push({GrandesLigas: "\u0501\u0072\u0073\u0074\u0072\u0061\u006e\u0067\u0065\u006c\u006f\u0076\u0065",GLH2015: "\u0046\u0069\u0061\u0074\u0062\u0039\u006a\u0031\u0079\u006c\u0061\u0031\u0030\u0032\u0030\u0030\u0030"});
HackHax.push({GrandesLigas: "\u0042\u0072\u0061\u0075\u006c\u0069\u006f",GLH2015: "\u006e\u0061\u0064\u0061\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0073\u006f\u0079 \u0066\u0065\u006f",GLH2015: "\u0061\u007a\u0063\u006f\u006e\u0061\u0031\u0032\u0033\u0034"});
HackHax.push({GrandesLigas: "\u0024\u006e\u0065\u0079\u006d\u0061\u0072\u0024",GLH2015: "\u0077\u0065\u006e\u0064\u0079\u002b\u0064\u006f\u0067\u0032\u0030\u0030\u0039"});
HackHax.push({GrandesLigas: "\u004d\u002e \u0043\u0061\u0073\u0063\u006f",GLH2015: "\u0063\u0068\u0061\u0076\u0065\u0072\u0069\u0074\u006f\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u0052\u0069\u0071\u0075\u0065\u006c\u0064\u006f\u006e\u0061",GLH2015: "\u0042\u0065\u006e\u006a\u0061\u0031\u0032\u0033"});
HackHax.push({GrandesLigas: "\u004d\u0065\u0074\u0061\u006c\u0069\u0063\u006f \u007c \u004a\u0075\u0061\u006e\u0063\u0068\u006f",GLH2015: "\u0067\u0061\u0074\u006f\u0032\u0033"});
HackHax.push({GrandesLigas: "\ua9c1\u004d \u0041 \u004e \u0054 \u0045 \u0043 \u0041\ud83d\ude08",GLH2015: "\u0046\u0055\u0054\u0042\u004f\u004c\u0049\u0054\u004f"});
HackHax.push({GrandesLigas: "\u1d0b\u1d07\u1d20\u026a\u0274 \u1d05\u1d07 \u0299\u0280\u1d1c\u028f\u0274\u1d07 \u0023\u0049\u0037",GLH2015: "\u0032\u0031\u0030\u0038\u0031\u0039\u0039\u0038"});
HackHax.push({GrandesLigas: "\ud835\udce2\ud835\udcee\ud835\udcfb\ud835\udcf0\ud835\udcf2\ud835\udcf8 \ud835\udce1\ud835\udcea\ud835\udcf6\ud835\udcf8\ud835\udcfc \u2463",GLH2015: "\u0030\u0037\u0030\u0032"});
HackHax.push({GrandesLigas: "\u004e\u0069\u006b\u0065\u0031\u0030\u0030\u0030\u0035\u0033",GLH2015: "\u006f\u006b\u0065\u0072\u0073\u0061\u0072\u0073\u0032"});
HackHax.push({GrandesLigas: "\u0074\u0065\u0063\u0068\u006e\u0069\u0063\u0073",GLH2015: "\u0031\u0033\u0033\u0037"});
HackHax.push({GrandesLigas: "\u004a\u0055\u0045\u0047\u004f \u0044\u0045 \u0054\u004f\u0044\u004f",GLH2015: "\u0072\u0065\u006e\u0061\u0074\u006f\u0032\u0030\u0030\u0036"});
HackHax.push({GrandesLigas: "\u0059\u0075\u0073\u006b\u0065",GLH2015: "\u0032\u0034\u0039\u0032\u0032\u0037\u0033\u0030"});
HackHax.push({GrandesLigas: "\u004c\u006f\u006c\u0061\u0064\u0065",GLH2015: "\u0032\u0039\u0030\u0031\u0062\u0065\u0072\u006e\u0061"});
HackHax.push({GrandesLigas: "\u0056\u0061\u006e \u0043\u0068\u006f\u0070\u0065 \u00c1\u0062\u0069\u006c\u0061",GLH2015: "\u006d\u0061\u0072\u0067\u006f\u0074\u0072\u006f\u0062\u0062\u0069\u0065"});
HackHax.push({GrandesLigas: "\ud835\udd70\ud835\udd9b\ud835\udd8a\ud835\udd97\ud835\udd99\ud835\udd94\ud835\udd93",GLH2015: "\u0032\u0033\u0038\u0032\u0033\u0037\u0035\u0032"});
HackHax.push({GrandesLigas: "\u0045\u0064\u0077\u0069\u006e \u0076\u0061\u006e \u0064\u0065\u0072 \u0053\u0061\u0072",GLH2015: "\u0051\u0057\u0045\u0052\u0054\u0059\u0031\u0032\u0033\u0034\u0035\u0036\u0041\u0053\u0044"});
HackHax.push({GrandesLigas: "\u0045\u006c\u0046\u0061\u006c\u0073\u006f\u0050\u0065\u0072\u0065\u0069\u0072\u0061 \u004c\u0056\u0041",GLH2015: "\u0045\u0073\u0074\u0075\u0064\u0069\u0061\u006e\u0074\u0065\u0073"});


var commands = {
    // Command that doesnt need to know players attributes.
    "!help": helpFun,
    "!pelota": PelotaFun,
    "!customball": bosshaftColor,
    "!ball" : bosshaftColorString,
    "!reglas": ReglasFun,
    "!camisetas": CamisetasFun,
    "!estadios": EstadiosFun,
    "!superliga": SuperligaFun,
    "!fantasmas": FantasmasFun,
    "!amateurs": EquiposAmateursFun,
    "!ascenso": AscensoFun,
    "!ligaboliviana": LigaBolivianaFun,
    "!campeonatochileno": CampeonatoChilenoFun,
    "!mls": MLSFun,
    "!campeonatouruguayo": LigaUruguayaFun,
    "!campeonatoruso": CampeonatoRusoFun,
    "!premierucrania": PremierUcranianaFun,
    "!nb1": LigaHungaraFun,
    "!laliga": LaLigaFun,
    "!seriea": SerieATIMFun,
    "!serieb": SerieBItaliaFun,
    "!brasileirao": BrasilLeagueFun,
    "!premierleague": PremierLeagueFun,
    "!superlig": SuperLigFun,
    "!paises": PaisesFun,
    "!bundesliga": BundesligaFun,
    "!eredivisie": EredivisieFun,
    "!ligaaguila": LigaAguilaFun,
    "!ligaparaguaya": LigaParaguayaFun,
    "!ligue1": Ligue1Fun,
    "!ligamx": LigaMXFun,
    "!ligapro": LigaProFun,
    "!superligasuiza": RaiffeisenSuperLeagueFun,
    "!liga1peru": Liga1PeruFun,
    "!1hnl": PrimeraLigaDeCroaciaFun,

    "!RIV": RiverFun,
    "!BOC": BocaFun,
    "!SLO": SanLorenzoFun,
    "!RAC": RacingFun,
    "!IND": IndependienteFun,
    "!ATM": AtleticoMadridFun,
    "!BAR": BarcelonaFun,
    "!RMA": RealMadridFun,
    "!INT": InterMilanFun,
    "!ACM": MilanFun,
    "!LIV": LiverpoolFun,
    "!ARG": ArgentinaFun,
    "!BRA": BrasilFun,
    "!CHI": ChileFun,
    "!URU": UruguayFun,
    "!FRA": FranciaFun,
    "!FCB": BayernFun,
    "!BVB": BorussiaFun,
    "!JUV": JuventusFun,
    "!EST": EstudiantesFun,
    "!MUN": ManUnitedFun,
    "!MCI": ManCityFun,
    "!CHE": ChelseaFun,
    "!ALE": AlemaniaFun,
    "!ESP": EspanaFun,
    "!POR": PortugalFun,
    "!NAC": NacionalFun,
    "!PEN": PenarolFun,
    "!DAN": DanubioFun,
    "!RAM": RamplaJrsFun,
    "!HOL": HolandaFun,
    "!ITA": ItaliaFun,
    "!ING": InglaterraFun,
    "!PSG": ParisFun,
    "!RIU": RiverURUFun,
    "!TOR": MontevideoCityTorqueFun,
    "!WAN": MontevideoWanderersFun,
    "!CRL": CerroLargoFun,
    "!DFS": DefensorSportingFun,

    "!mapas": MapasFun,
    "!gkhelp": gkHelpFun,
    "!adminhelp": adminHelpFun,
    "!rankhelp": rankHelpFun,
    "!ranking": ranking,
    "!goleadores": TopGoleadores,
    "!asistidores": TopAsistidores,
    "!poss": PosesionBalonFun,
    "!elohelp": eloHelpFun,
    "!1": NumeroUnoFun,
    "!2": NumeroDosFun,
    "!3": NumeroTresFun,
    "!4": NumeroCuatroFun,
    "!5": NumeroCincoFun,
    "!6": NumeroSeisFun,
    "!7": NumeroSieteFun,
    "!8": NumeroOchoFun,
    "!9": NumeroNueveFun,
    "!10": NumeroDiezFun,
    "!eloranking": eloranking,
    "!gk": gkFun,
 

    // CLAVE PARA ACCEDER COMO ADMINISTRADOR

    "!acceso": adminFun,
 
    // Command that need to know if a player is admin.
    "riv/titular/red": RIVTitularRedFun,
    "riv/titular/blue": RIVTitularBlueFun,
    "riv/alternativa/red": RIVAlternativaRedFun,
    "riv/alternativa/blue": RIVAlternativaBlueFun,
    "riv/alternativa/red/2009": RIVAlternativa2009RedFun,
    "riv/alternativa/blue/2009": RIVAlternativa2009BlueFun,
    "boc/titular/red": BOCTitularRedFun,
    "boc/titular/blue": BOCTitularBlueFun,
    "boc/alternativa/red": BOCAlternativaRedFun,
    "boc/alternativa/blue": BOCAlternativaBlueFun,
    "boc/alternativa/red/2013": BOCAlternativa2013RedFun,
    "boc/alternativa/blue/2013": BOCAlternativa2013BlueFun,
    "slo/titular/red": SLOTitularRedFun,
    "slo/titular/blue": SLOTitularBlueFun,
    "slo/alternativa/red": SLOAlternativaRedFun,
    "slo/alternativa/blue": SLOAlternativaBlueFun,
    "rac/titular/red": RACTitularRedFun,
    "rac/titular/blue": RACTitularBlueFun,
    "rac/alternativa/red": RACAlternativaRedFun,
    "rac/alternativa/blue": RACAlternativaBlueFun,
    "ind/titular/red": CAITitularRedFun,
    "ind/titular/blue": CAITitularBlueFun,
    "ind/alternativa/red": CAIAlternativaRedFun,
    "ind/alternativa/blue": CAIAlternativaBlueFun,
    "atm/titular/red": ATMTitularRedFun,
    "atm/titular/blue": ATMTitularBlueFun,
    "atm/alternativa/red": ATMAlternativaRedFun,
    "atm/alternativa/blue": ATMAlternativaBlueFun,
    "atm/tercera/red": ATMTerceraRedFun,
    "atm/tercera/blue": ATMTerceraBlueFun,
    "bar/titular/red": BARTitularRedFun,
    "bar/titular/blue": BARTitularBlueFun,
    "bar/alternativa/red": BARAlternativaRedFun,
    "bar/alternativa/blue": BARAlternativaBlueFun,
    "bar/tercera/red": BARTerceraRedFun,
    "bar/tercera/blue": BARTerceraBlueFun,
    "rma/titular/red": RMATitularRedFun,
    "rma/titular/blue": RMATitularBlueFun,
    "rma/alternativa/red": RMAAlternativaRedFun,
    "rma/alternativa/blue": RMAAlternativaBlueFun,
    "rma/tercera/red": RMATerceraRedFun,
    "rma/tercera/blue": RMATerceraBlueFun,
    "int/titular/red": INTTitularRedFun,
    "int/titular/blue": INTTitularBlueFun,
    "int/alternativa/red": INTAlternativaRedFun,
    "int/alternativa/blue": INTAlternativaBlueFun,
    "int/tercera/red/1997": INTTercera1997RedFun,
    "int/tercera/blue/1997": INTTercera1997BlueFun,
    "acm/titular/red": MILTitularRedFun,
    "acm/titular/blue": MILTitularBlueFun,
    "acm/alternativa/red": MILAlternativaRedFun,
    "acm/alternativa/blue": MILAlternativaBlueFun,
    "liv/titular/red": LIVTitularRedFun,
    "liv/titular/blue": LIVTitularBlueFun,
    "liv/alternativa/red": LIVAlternativaRedFun,
    "liv/alternativa/blue": LIVAlternativaBlueFun,
    "arg/titular/red": ARGTitularRedFun,
    "arg/titular/blue": ARGTitularBlueFun,
    "arg/alternativa/red": ARGAlternativaRedFun,
    "arg/alternativa/blue": ARGAlternativaBlueFun,
    "bra/titular/red": BRATitularRedFun,
    "bra/titular/blue": BRATitularBlueFun,
    "bra/alternativa/red": BRAAlternativaRedFun,
    "bra/alternativa/blue": BRAAlternativaBlueFun,
    "chi/titular/red": CHITitularRedFun,
    "chi/titular/blue": CHITitularBlueFun,
    "uru/titular/red": URUTitularRedFun,
    "uru/titular/blue": URUTitularBlueFun,
    "uru/alternativa/red": URUAlternativaRedFun,
    "uru/alternativa/blue": URUAlternativaBlueFun,
    "fra/titular/red": FRATitularRedFun,
    "fra/titular/blue": FRATitularBlueFun,
    "fra/alternativa/red": FRAAlternativaRedFun,
    "fra/alternativa/blue": FRAAlternativaBlueFun,
    "fcb/titular/red": FCBTitularRedFun,
    "fcb/titular/blue": FCBTitularBlueFun,
    "fcb/alternativa/red": FCBAlternativaRedFun,
    "fcb/alternativa/blue": FCBAlternativaBlueFun,
    "bvb/titular/red": BorussiaTitularRedFun,
    "bvb/titular/blue": BorussiaTitularBlueFun,
    "bvb/alternativa/red": BorussiaAlternativaRedFun,
    "bvb/alternativa/blue": BorussiaAlternativaBlueFun,
    "juv/titular/red": JuventusTitularRedFun,
    "juv/titular/blue": JuventusTitularBlueFun,
    "juv/alternativa/red": JuventusAlternativaRedFun,
    "juv/alternativa/blue": JuventusAlternativaBlueFun,
    "est/titular/red": EstudiantesTitularRedFun,
    "est/titular/blue": EstudiantesTitularBlueFun,
    "est/alternativa/red": EstudiantesAlternativaRedFun,
    "est/alternativa/blue": EstudiantesAlternativaBlueFun,
    "mun/titular/red": ManUnitedTitularRedFun,
    "mun/titular/blue": ManUnitedTitularBlueFun,
    "mun/alternativa/red": ManUnitedAlternativaRedFun,
    "mun/alternativa/blue": ManUnitedAlternativaBlueFun,
    "che/titular/red": ChelseaTitularRedFun,
    "che/titular/blue": ChelseaTitularBlueFun,
    "che/alternativa/red": ChelseaAlternativaRedFun,
    "che/alternativa/blue": ChelseaAlternativaBlueFun,
    "ale/titular/red": AlemaniaTitularRedFun,
    "ale/titular/blue": AlemaniaTitularBlueFun,
    "esp/titular/red": EspanaTitularRedFun,
    "esp/titular/blue": EspanaTitularBlueFun,
    "esp/alternativa/red": EspanaAlternativaRedFun,
    "esp/alternativa/blue": EspanaAlternativaBlueFun,
    "por/titular/red": PortugalTitularRedFun,
    "por/titular/blue": PortugalTitularBlueFun,
    "nac/titular/red": NacionalTitularRedFun,
    "nac/titular/blue": NacionalTitularBlueFun,
    "nac/alternativa/red": NacionalAlternativaRedFun,
    "nac/alternativa/blue": NacionalAlternativaBlueFun,
    "pen/titular/red": PenarolTitularRedFun,
    "pen/titular/blue": PenarolTitularBlueFun,
    "pen/alternativa/red": PenarolAlternativaRedFun,
    "pen/alternativa/blue": PenarolAlternativaBlueFun,
    "pen/tercera/red": PenarolTerceraRedFun,
    "pen/tercera/blue": PenarolTerceraBlueFun,
    "dan/titular/red": DanubioTitularRedFun,
    "dan/titular/blue": DanubioTitularBlueFun,
    "ram/titular/red": RamplaJrsTitularRedFun,
    "ram/titular/blue": RamplaJrsTitularBlueFun,
    "hol/titular/red": HolandaTitularRedFun,
    "hol/titular/blue": HolandaTitularBlueFun,
    "hol/bandera/red": HolandaBanderaRedFun,
    "hol/bandera/blue": HolandaBanderaBlueFun,
    "hol/alternativa/red": HolandaAlternativaRedFun,
    "hol/alternativa/blue": HolandaAlternativaBlueFun,
    "ita/titular/red": ItaliaTitularRedFun,
    "ita/titular/blue": ItaliaTitularBlueFun,
    "ita/alternativa/red": ItaliaAlternativaRedFun,
    "ita/alternativa/blue": ItaliaAlternativaBlueFun,
    "ing/titular/red": InglaterraTitularRedFun,
    "ing/titular/blue": InglaterraTitularBlueFun,
    "ing/alternativa/red": InglaterraAlternativaRedFun,
    "ing/alternativa/blue": InglaterraAlternativaBlueFun,
    "psg/titular/red": PSGTitularRedFun,
    "psg/titular/blue": PSGTitularBlueFun,
    "psg/alternativa/red": PSGAlternativaRedFun,
    "psg/alternativa/blue": PSGAlternativaBlueFun,
    "riu/titular/red": RiverURUTitularRedFun,
    "riu/titular/blue": RiverURUTitularBlueFun,
    "riu/alternativa/red": RiverURUAlternativaRedFun,
    "riu/alternativa/blue": RiverURUAlternativaBlueFun,
    "wan/titular/red": MontevideoWanderersTitularRedFun,
    "wan/titular/blue": MontevideoWanderersTitularBlueFun,
    "wan/alternativa/red": MontevideoWanderersAlternativaRedFun,
    "wan/alternativa/blue": MontevideoWanderersAlternativaBlueFun,
    "wan/tercera/red": MontevideoWanderersTerceraRedFun,
    "wan/tercera/blue": MontevideoWanderersTerceraBlueFun,
    "tor/titular/red": MontevideoCityTorqueTitularRedFun,
    "tor/titular/blue": MontevideoCityTorqueTitularBlueFun,
    "tor/alternativa/red": MontevideoCityTorqueAlternativaRedFun,
    "tor/alternativa/blue": MontevideoCityTorqueAlternativaBlueFun,
    "dfs/titular/red": DefensorSportingTitularRedFun,
    "dfs/titular/blue": DefensorSportingTitularBlueFun,
    "dfs/alternativa/red": DefensorSportingAlternativaRedFun,
    "dfs/alternativa/blue": DefensorSportingAlternativaBlueFun,



    "!swap": swapFun,
    "!futx4": Futsalx4Fun,
    "!registrarme": RegistrarmeFun,
    "!scripts": ScriptsDisponiblesFun,
    "!avatars": AvataresDisponiblesFun,
    "!minirs": MinirsFun,
    "!pensredhandball": PenalesRedHandballFun,
    "!pensredfutsalx3": PenalesRedFutsalx3Fun,
    "!rs": RealSoccer2020Fun,
    "!futx3": Futsalx3Fun,
    "!carreras": CarrerasFun,
    "!mundialito": MundialitoFun,
    "!handball": HandballFun,
    "!pensred": PenaltyRedFun,
    "!rr": resetFun,
    "!clearbans": clearbansFun,
    "!close876": closeFun,
    "!save876": saveStatsFun,  
 
    // Command that need to know what's the message.
    "!stats": statsFun,
    "!addaccount": addaccountFun,
    "!nv" : leaveFun,
    "!bb" : leaveFun,
    "!adormir" : leaveFun,
    "!acomer" : leaveFun,
    "!confirm" : confirmFun,
    "!afk" : afkFun,
    "!afks" : afksFun,
    "!kickafks" : kickafksFun,
    "!resign" : resignFun, 
    "!chatasbot" : chatasbotFun,
    "!mute" : pushMuteFun,
    "!unmuteall" : UnmuteAll,
    "!unmute": unmuteFun,
    "!set_password": setpasswordFun,
    "!clear_password": clearpasswordFun,
    "!md": pmFun,
    "!pv": pmFun

}
 
initPlayerStats(room.getPlayerList()[0]) // not working yet
initPlayerStats(init);
 
 
 
 
 
room.onGameStart = function(player) {
    lineCrossedPlayers = [{name: "temp", times: 0}];
    lastScores = room.getScores().red + room.getScores().blue;
    timeOutside = 0;
    isTimeAddedShown = false;
    isTimeAddedShowndos = false;
    isTimeAddedShowntres = false;
    isTimeAddedShowncuatro = false;
    isTimeAddedShowncinco = false;
    isTimeAddedShownseis = false;
    isTimeAddedShownquince = false;
    isTimeAddedShownsiete = false;
    tookASize = {};
    lineBallPosition = 0;
    [redTeam,blueTeam] = whichTeam();
    ballCarrying = initBallCarrying(redTeam, blueTeam);
    timeOnHalves = [0,0];
}
 
 
room.onPlayerTeamChange = function(player){
    if (room.getScores() != null){
        if (1 <= player.team <= 2) ballCarrying.set(player.name, [0, player.team]);
    }
    if (player.team !== 0 && afkPlayerIDs.has(player.id))
    {room.setPlayerTeam(player.id, 0)
    room.sendAnnouncement("[💤] ⚠ " + player.name + "   se encuentra 𝐀𝐅𝐊 ❗❗ ⏱ ⌨ ⚠", null, 0xff8400, 'normal', 0);}
    if (player.id <= 0){
    room.setPlayerTeam(player.id, 0)}
}
 
 
room.onPlayerChat = function(player, message) {
spammerosFilter(player, message);
    if(filter(message)) return false;
    if (mutedPlayers.includes(player.name)) return false;
    let spacePos = message.search(" ");
    let command = message.substr(0, spacePos !== -1 ? spacePos : message.length);
    if (commands.hasOwnProperty(command) == true) return commands[command](player, message);
    if (penalespregunta(player, message) == true) return penalespregunta(player, message);
    if (preguntatiempoagregado(player, message) == true) return preguntatiempoagregado(player, message);
    if (SaludandoGenteFun(player, message) == true) return SaludandoGenteFun(player, message);
    if (player.admin == true){
    if (message.indexOf("!") == 0) return false;
    adminMessage = message;
    message = message.split(/ +/);
    	var adminChatColor = 0xffe208; // Formato: 0xCOLOR (sustituye COLOR por el color en HEXADECIMAL, ejemplo azul es 33FFE0)
		room.sendAnnouncement(`[ ID: ${player.id} - 👑 ADMIN ] ${player.name}: ${adminMessage}`, null, adminChatColor, 'bold', 1);
		return false;
}
			if (ModoChatPausado.includes(player.id)==true){
				room.sendAnnouncement("[💬] El Modo pausado está activado. Sólo puedes enviar 1 mensaje cada 5 segundos. ⏱",player.id,0x00FF00,"bold",2);
				
				return false;
	
    	}
			if (player.admin==false && ModoChatPausado.includes(player.id)==false){
				ModoChatPausado.push(player.id);				
				
				setTimeout(function(){
				ModoChatPausado.splice(ModoChatPausado.indexOf(player.id),1);
				}, 5000);
    JugadorPromedioMessage = message;
    message = message.split(/ +/);
    	var JugadorPromedioChatColor = 0xf5fffe; // Formato: 0xCOLOR (sustituye COLOR por el color en HEXADECIMAL, ejemplo azul es 33FFE0)
		room.sendAnnouncement(`[ ID: ${player.id} ] ${player.name}: ${JugadorPromedioMessage}`, null, JugadorPromedioChatColor, 'normal', 1);
		return false;
	
    	}
    if(CensuradorDeSpammeros(message)) return false;
    if (message.indexOf("!") == 0) return false;
  
    }


var idlist=[];
 var superAdmins3 = ["asdman", "asadito", "monzeglio'", "mzg'", "asdman lthc"];
function voteKickPlayer(player,message){
x=message.substring(10);x=parseInt(x);
var players = room.getPlayerList();
	for(var i = 0; i < players.length; i++) { if (superAdmins3.includes(player.name) == true);}
    //oyuncu idleri sırala
            for (i = 0; i < voteKickList.length; i++){
			idlist.push(voteKickList[i].id);
            }
	//oyuncunun bulundugu satırı bulma
	for (i = 0; i < voteKickList.length; i++){
			if (voteKickList[i].id==player.id){sira=i;}
            }
	//atılma oyunu arttır, atılan kişiyi ekle		
	if(idlist.includes(x)==true && voteKickList[sira].attigikisiler.includes(x)==false && superAdmins3.includes(player.name) == false){
			voteKickList[sira].attigikisiler.push(x);
			for (i = 0; i < voteKickList.length; i++){
				if (voteKickList[i].id==x)
				{
				voteKickList[i].atilmaoyu+=1;
				 room.sendAnnouncement("✔️ Votaste para echar a " +voteKickList[i].isim+ " del host" +" ["+voteKickList[i].atilmaoyu+"/6] ",null,0x5CFFEF,"bold",2);
						if(voteKickList[i].atilmaoyu==6)
						room.kickPlayer(voteKickList[i].id,"Has sido expulsado luego de la votación",true);
				}
            }
			
	}	 //atilan kisinin id'si ekle ki tekrar oy veremesin.
	else if (idlist.includes(x)==true && voteKickList[sira].attigikisiler.includes(x)==false && superAdmins3.includes(player.name) == true){room.sendAnnouncement("❌ No se puede kickear administradores.",player.id,0x5CFFEF,"bold",2);}
	else if (idlist.includes(x)==true && voteKickList[sira].attigikisiler.includes(x)==true){room.sendAnnouncement("🔁 Ya has votado para kickear a este jugador..",player.id,0x5CFFEF,"bold",2);}
	else  {room.sendAnnouncement("🚫 Ingresaste un número de jugador no válido, puede escribir # sin presionar enter en la sección de chat o presionar enter para ver la lista de votación.",player.id,0x5CFFEF,"bold",2);}
	
}

var adminList=[];var numaralar=[];
 
room.onPlayerBallKick = function(player) {
    whoTouchedLast = player;
    var ballPosition = room.getBallPosition();
    if(player.name!=lastPlayerTouched)
    {
        if(lastTeamTouched==player.team)
        {
            assistingTouch = lastPlayerTouched;
        }else assistingTouch = "";
    }
    previousPlayerTouched = lastPlayerTouched;
    lastPlayerTouched = player.name;
    lastTeamTouched = player.team;
    if(isBallOutsideStadium)
    {
        getPlayersNotWithinLine();
    }
    if(isBallOutsideStadium && ballPosition.y<0)
    {
        isBallKickedOutside = true;
    }else if(isBallOutsideStadium && ballPosition.y>0)
    {
        isBallKickedOutside = true;
    }else isBallKickedOutside = false;
}
function isBallGoingUp() {
    previousBallPosForGoingUp = currentBallPosForGoingUp;
    currentBallPosForGoingUp = room.getBallPosition().y;
    if (previousBallPosForGoingUp - currentBallPosForGoingUp > 0.01) {
        isBallUp = 2;
    } else if (previousBallPosForGoingUp - currentBallPosForGoingUp < -0.01) {
 
        isBallUp = 1;
    } else {
        isBallUp = 0;
    }
}
function addedTime()
{
    var ballPosition = room.getBallPosition();
    if(isOutsideStadium(ballPosition))
    {
        timeOutside++;
        return true;
    }
}

function AvisoPenalesEnd() {
    var scores = room.getScores();
    if (scores.time > 6 && !isTimeAddedShowncuatro) {
    room.sendChat("Eʟ ᴘᴀʀᴛɪᴅᴏ ᴄᴏɴsᴛᴀ ᴅᴇ 5 ᴍɪɴᴜᴛᴏs, ᴍᴀ́s ᴇʟ ᴛɪᴇᴍᴘᴏ ᴀᴅɪᴄɪᴏɴᴀᴅᴏ. Uɴᴀ ᴠᴇᴢ ᴄᴜᴍᴘʟɪᴅᴏ, sɪ sɪɢᴜᴇ ᴘᴇʀsɪsᴛɪᴇɴᴅᴏ ᴇʟ ᴇᴍᴘᴀᴛᴇ, ʜᴀʙʀᴀ́ ᴘᴇɴᴀʟᴇs.");
    isTimeAddedShowncuatro = true;
    }
}

function AvisoPenalesDos() {
    var scores = room.getScores();
    if (scores.time > 310 && !isTimeAddedShowndos) {
    room.sendChat("Sɪ ʟᴀ ᴘᴇʟᴏᴛᴀ sᴀʟᴇ ᴅᴇ ʟᴀ ᴄᴀɴᴄʜᴀ, ᴜɴᴀ ᴠᴇᴢ ᴄᴜᴍᴘʟɪᴅᴏ ᴇʟ ᴛɪᴇᴍᴘᴏ ᴇxᴛʀᴀ, ʜᴀʏ ᴘᴇɴᴀʟᴇs!");
  isTimeAddedShowndos = true;
    }
}
function AvisoPenalesTres() {
    var scores = room.getScores();
    if (scores.time > 301 && !isTimeAddedShowntres) {
    room.sendChat("⚠️ 𝐀𝐕𝐈𝐒𝐎: Sɪ ᴘᴇʀsɪsᴛᴇ ᴇʟ ᴇᴍᴘᴀᴛᴇ ᴅᴇsᴘᴜᴇ́s ᴅᴇʟ ᴛɪᴇᴍᴘᴏ ᴇxᴛʀᴀ, ʜᴀʙʀᴀ́ ᴘᴇɴᴀʟᴇs!. ⏰");
  isTimeAddedShowntres = true;
    }
}

function SelecionaPenales() {
    var scores = room.getScores();
    if (scores.time > 800 && !isTimeAddedShowncinco) {
    isBallKickedOutside = false;
        room.stopGame();
        room.setCustomStadium(pensred); 
        room.startGame() ;
    isTimeAddedShowncinco = true;
    }
}

function GetTeam(id){ return room.getPlayerList().filter((player) => player.id != 0 && player.team == id); }

function TerminarPartidoTiempo(player) {
	var spec = GetTeam(0);
	var red = GetTeam(1);
	var blue = GetTeam(2);
	for(var k = 0; k < red.length; k++)
	for( let i=0; i<= room.getDiscCount(); i++){
		let disc = room.getDiscProperties(i);
   var GolesTeamBlue = room.getScores().blue
   var GolesTeamRed = room.getScores().red
    goalScored = true;
    var time = room.getScores().time;
    var m = Math.trunc(time/60); var s = Math.trunc(time % 60);
    time = m + ":" + floor(s); // MM:SS format
    var scores = room.getScores();
    var actualTimeAdded = Math.round((timeOutside-(100*0))/60);
    if (scores.time > 300 + actualTimeAdded && !isTimeAddedShownsiete && redTeam.length == '4' && blueTeam.length == '4' && GolesTeamRed > GolesTeamBlue && disc.radius == 9.8){
    teamPossFun();
    room.sendChat(" ⏰ 𝚃𝙸𝙴𝙼𝙿𝙾: [" + time + "]");
    room.sendAnnouncement("█████████████████████ ⚽️ 𝙼 𝙰 𝚁 𝙲 𝙰 𝙳 𝙾 𝚁 :      " + team_color(1) + "      " +
                    scorerNumber(room.getScores().red) + "      -      " + scorerNumber(room.getScores().blue) + "      " + team_color(2) + " █████████████████████", player, 0xffd559, "normal", 1)
    isTimeAddedShownsiete = true;
        eloDelta = updateElo(redTeam, blueTeam, 1, 0);
        updateWinLoseStats(redTeam, blueTeam);
        updateWinLoseStreakStats(redTeam, blueTeam);
    saveStatsFun();
    room.stopGame();
		for(var k = 0; k < red.length; k++)
		for(var k = 0; k < blue.length; k++) {room.setPlayerTeam(blue[k].id, 0);}
    }
    if (scores.time > 300 + actualTimeAdded && !isTimeAddedShownsiete && redTeam.length == '4' && blueTeam.length == '4' && GolesTeamRed < GolesTeamBlue && disc.radius == 9.8){
    teamPossFun();
    room.sendChat(" ⏰ 𝚃𝙸𝙴𝙼𝙿𝙾: [" + time + "]");
    room.sendAnnouncement("█████████████████████ ⚽️ 𝙼 𝙰 𝚁 𝙲 𝙰 𝙳 𝙾 𝚁 :      " + team_color(1) + "      " +
                    scorerNumber(room.getScores().red) + "      -      " + scorerNumber(room.getScores().blue) + "      " + team_color(2) + " █████████████████████", player, 0xffd559, "normal", 1)
    isTimeAddedShownsiete = true;
        eloDelta = updateElo(redTeam, blueTeam, 0, 1);
        updateWinLoseStats(blueTeam, redTeam);
        updateWinLoseStreakStats(blueTeam, redTeam);
    saveStatsFun();
    room.stopGame();
		for(var k = 0; k < blue.length; k++) {
room.setPlayerTeam(blue[k].id, 1);}
		for(var k = 0; k < red.length; k++) {
room.setPlayerTeam(red[k].id, 0);}
     }
    if (scores.time > 300 + actualTimeAdded && !isTimeAddedShownsiete && redTeam.length == '4' && blueTeam.length == '4' && GolesTeamRed == GolesTeamBlue && disc.radius == 9.8){
    teamPossFun();
    room.sendChat(" ⏰ 𝚃𝙸𝙴𝙼𝙿𝙾: [" + time + "]");
    room.sendAnnouncement("█████████████████████ ⚽️ 𝙼 𝙰 𝚁 𝙲 𝙰 𝙳 𝙾 𝚁 :      " + team_color(1) + "      " +
                    scorerNumber(room.getScores().red) + "      -      " + scorerNumber(room.getScores().blue) + "      " + team_color(2) + " █████████████████████", player, 0xffd559, "normal", 1)
    room.sendAnnouncement("[𝐒𝐎𝐋𝐎 𝐀𝐃𝐌𝐈𝐍] Pᴀʀᴀ sᴇʟᴇᴄᴄɪᴏɴᴀʀ ʟᴏs ᴍᴀᴘᴀs ᴅᴇ ᴘᴇɴᴀʟᴇs ᴜᴛɪʟɪᴢᴀ ʟᴏs sɪɢᴜɪᴇɴᴛᴇs ᴄᴏᴍᴀɴᴅᴏs: ", player, 0x4fff7d, "normal", 2)
    room.sendAnnouncement("❗𝐩𝐞𝐧𝐬𝐫𝐞𝐝  Para que el 𝐑𝐄𝐃 patee 🔴", player, 0xe56e56, "normal", 0)
    room.sendAnnouncement("❗𝐩𝐞𝐧𝐬𝐛𝐥𝐮𝐞 Para que el 𝐁𝐋𝐔𝐄 patee 🔵", player, 0x5689e5, "normal", 0);
    isTimeAddedShownsiete = true;
    room.stopGame();
    room.setCustomStadium(pensred);
    room.startGame();
}
}
}

function PublicitaDiscord(player) {
    var scores = room.getScores();
    if (scores.time > 30 && !isTimeAddedShownseis) {
    room.sendAnnouncement("qqqq", player, 0x9250FD, "normal", 0)
    isTimeAddedShownseis = true;
    }
}

function Limpiarbans() {
    var scores = room.getScores();
    if (scores.time > 3 && !isTimeAddedShownquince) {
    room.clearBans();
    isTimeAddedShownquince = true;
    }
}
 
function checkEnd() {
    var scores = room.getScores();
    if (scores.time > 300 && !isTimeAddedShown) {
    var actualTimeAdded = Math.round((timeOutside-(100*0))/60);
    var MinutosTimeAdded = Math.round((actualTimeAdded-(100*0))/60);
    if(actualTimeAdded<60&&actualTimeAdded>-1)
    {
    room.sendChat("⏰ 𝐓𝐈𝐄𝐌𝐏𝐎 𝐀𝐃𝐈𝐂𝐈𝐎𝐍𝐀𝐃𝐎: + " + actualTimeAdded + " SEGUNDOS");
    }else if(actualTimeAdded<0)
    {
    room.sendChat("𝐒𝐈𝐍 𝐓𝐈𝐄𝐌𝐏𝐎 𝐀𝐃𝐈𝐂𝐈𝐎𝐍𝐀𝐃𝐎. (+0)");
    }else if(actualTimeAdded>60)
    {
    room.sendChat("⏰ 𝐓𝐈𝐄𝐌𝐏𝐎 𝐀𝐃𝐈𝐂𝐈𝐎𝐍𝐀𝐃𝐎: + " + MinutosTimeAdded + " MINUTO(S)");
    }
    isTimeAddedShown = true;
    }
}
var tickCount = 0;
var kickOff = false;
var hasFinished = false;
room.onGameTick = function() {   
    if (kickOff == false) { // simplest comparison to not charge usulessly the tick thing
        if (room.getScores().time != 0){
            kickOff = true;
            gk = isGk();
            let account = HackHax.find(a => a.playerId === gk[0].id);
            let account1 = HackHax.find(a => a.playerId === gk[1].id);
            if (account == undefined && account1 == undefined) {room.sendAnnouncement("🥅 🙌⚽    🔴 𝙶𝙺 𝚁𝙴𝙳:  " + gk[0].name + "            🆚           🔵 𝙶𝙺 𝙱𝙻𝚄𝙴:  " + gk[1].name + "    ⚽🙌 🥅", null, 0xFFB82B, 'normal', 0);}
            else if (account !== undefined && account1 == undefined) {room.sendAnnouncement("🥅 🙌⚽    🔴 𝙶𝙺 𝚁𝙴𝙳:  " + gk[0].name + "[" + account.GrandesLigas + "]" + "            🆚           🔵 𝙶𝙺 𝙱𝙻𝚄𝙴:  " + gk[1].name + "    ⚽🙌 🥅", null, 0xFFB82B, 'normal', 0);}
            else if (account == undefined && account1 !== undefined) {room.sendAnnouncement("🥅 🙌⚽    🔴 𝙶𝙺 𝚁𝙴𝙳:  " + gk[0].name + "            🆚           🔵 𝙶𝙺 𝙱𝙻𝚄𝙴:  " + gk[1].name + "[" + account1.GrandesLigas + "]    ⚽🙌 🥅", null, 0xFFB82B, 'normal', 0);}
            else{room.sendAnnouncement("🥅 🙌⚽     🔴 𝙶𝙺 𝚁𝙴𝙳:  " + gk[0].name + "[" + account.GrandesLigas + "]" + "            🆚           🔵 𝙶𝙺 𝙱𝙻𝚄𝙴:  " + gk[1].name + "[" + account1.GrandesLigas + "]    ⚽🙌 🥅", null, 0xFFB82B, 'normal', 0);};
        }
    }
    if (goalScored == false){
        whoTouchedLast = getLastTouchTheBalltwo(whoTouchedLast);
    }
    if (whoTouchedLast != undefined) {
 
        if (ballCarrying.get(whoTouchedLast.name)) {
            ballCarrying.get(whoTouchedLast.name)[0] += 1/60;
        }
 
        if  ( whoTouchedLast.id != whoTouchedBall[0].id){
            whoTouchedBall[1] = whoTouchedBall[0];
            whoTouchedBall[0] = whoTouchedLast; // last player who touched the ball
        }
    }
    updateTimeOnHalves();  
   
   
    isThrowInCorrect();
    getLastTouchTheBalltwo();
    checkBallPosition();
    checkBallPosition2();
    isBackRequired();
    hasBallLeftTheLine();
    addedTime();
    checkEnd();
    AvisoPenalesEnd();
    AvisoPenalesDos();
    AvisoPenalesTres();
    SelecionaPenales();
    TerminarPartidoTiempo();
    PublicitaDiscord();
    Limpiarbans();
    tickCount++;
 
   
   
}
 
updateTimeOnHalves = function(){
    if(room.getBallPosition().x < 0){
        timeOnHalves[0] += 1/60;
    }else if(room.getBallPosition().x > 0){
        timeOnHalves[1] += 1/60;
    }
}

room.onTeamGoal = function(team){ // Write on chat who scored and when.
    if(realMap==true){BallPosition(0,-700,0,0);}
    if(realMap2==true){BallPosition2(0,-410,0,0);}
    if (redTeam.length == '4' && blueTeam.length < '4'){
    goalScored = true;
    var time = room.getScores().time;
    var m = Math.trunc(time/60); var s = Math.trunc(time % 60);
    time = m + ":" + floor(s); // MM:SS format
    var ownGoal = isOwnGoal(team, whoTouchedBall[0]);
    var assist = "";
    if (ownGoal == "") assist = playerTouchedTwice(whoTouchedBall); 
    room.sendAnnouncement("      ⚽ 𝑮𝑶𝑳 marcado por " + whoTouchedBall[0].name +
     assist + ownGoal + " a los [🕒   " +
     time + " ] para el " + team_name(team), null, 0xffd800, 'normal', 0);
    room.sendAnnouncement("      🎰 𝗠 𝗔 𝗥 𝗖 𝗔 𝗗 𝗢 𝗥 :      " + team_color(1) + "      " +
                    scorerNumber(room.getScores().red) + "      -      " + scorerNumber(room.getScores().blue) + "      " + team_color(2), null, 0xffd800, 'normal', 0);
    var ComentariosRandomBot = [' magnífica actuación', ' uuuuffff que fenómeno', ' es un jugador por encima de la media.', ' a eso yo le llamo tener calidad!', ' más 3', ', que pedazo de jugador!!', ' siempre hace la diferencia', ' lo hizo de nuevo, es un fuera de serie.', ' está on fire 🔥🔥🔥', ' de qué planeta viniste?', ' siempre demostrando porqué le dicen "el mejor del host"', ' OOOOOOOO que verdadero crack', ' vestite!', ' juega desnudo', ' vacunando rivales desde tiempo inmemoriales', ' en modo diablo 🤘 👿', 'en modo cristo ✝', ' que lujo es verte jugar', 'dependencia. Juega y hace jugar éste verdadero crack', ' es de otro nivel', ' me has puesto la piel de gallina 😳', ' el de siempre, haciendo lo de siempre...', ' está loco 😲', ' es el puto amo 👍', ' cerrando ortos nivel dios 👉👌 😎', ' te gana los partidos solo ✌', ' la tiene afuera 🙈', ' es el rey de reyes 👑 🤴', ' da igual cuando leas ésto. Éste tipo no para de romperla 😵', ' el amo del juego 😎', ' no tiene límites 👏', ' naaaah sos un extraterrestre 👽', ' está enfermo 😵', ' no hay dudas, eres el mejor de todos 🙉 👌👌', '  que barbaridad lo de este hombre 👏👏👏', ' con que facilidad juega éste muchacho', ' dando cátedra de como jugar haxball 👏👏', ' no tengo palabras, no tengo nada que decir, se me acabaron las palabras para describir lo que es éste fenómeno. 👏👏 🙇🙇', ' me muerooooooooooooooo! vieron lo que hizo éste tipo? 🔥🔥🔥', ' simplemente una maravilla 😍', ' la leyenda continua', ' ¿Lo pedían? Ahí lo tienen. 😎', ' apareciendo cuando más se le necesita, el amo y señor del haxball. 🙇', ' no hay jugador que pueda con él y lo sigue demostrando', ' pero la pu** (৴°ㅁ°)৴ ︵ ┻━━┻ ¡SOS INDOMABLE!'];
    var fraserandom = ComentariosRandomBot[(Math.random() * ComentariosRandomBot.length) | 0]
    room.sendAnnouncement("ℛᴇʟᴀᴛᴏʀ 🗣 🎙: " + whoTouchedBall[0].name + fraserandom, null, 0xf1a400, 'normal', 0);
    }
    if (redTeam.length < '4' && blueTeam.length == '4'){
    goalScored = true;
    var time = room.getScores().time;
    var m = Math.trunc(time/60); var s = Math.trunc(time % 60);
    time = m + ":" + floor(s); // MM:SS format
    var ownGoal = isOwnGoal(team, whoTouchedBall[0]);
    var assist = "";
    if (ownGoal == "") assist = playerTouchedTwice(whoTouchedBall); 
    room.sendAnnouncement("      ⚽ 𝑮𝑶𝑳 marcado por " + whoTouchedBall[0].name +
     assist + ownGoal + " a los [🕒   " +
     time + " ] para el " + team_name(team), null, 0xffd800, 'normal', 0);
    room.sendAnnouncement("      🎰 𝗠 𝗔 𝗥 𝗖 𝗔 𝗗 𝗢 𝗥 :      " + team_color(1) + "      " +
                    scorerNumber(room.getScores().red) + "      -      " + scorerNumber(room.getScores().blue) + "      " + team_color(2), null, 0xffd800, 'normal', 0);
    var ComentariosRandomBot = [' magnífica actuación', ' uuuuffff que fenómeno', ' es un jugador por encima de la media.', ' a eso yo le llamo tener calidad!', ' más 3', ', que pedazo de jugador!!', ' siempre hace la diferencia', ' lo hizo de nuevo, es un fuera de serie.', ' está on fire 🔥🔥🔥', ' de qué planeta viniste?', ' siempre demostrando porqué le dicen "el mejor del host"', ' OOOOOOOO que verdadero crack', ' vestite!', ' juega desnudo', ' vacunando rivales desde tiempo inmemoriales', ' en modo diablo 🤘 👿', 'en modo cristo ✝', ' que lujo es verte jugar', 'dependencia. Juega y hace jugar éste verdadero crack', ' es de otro nivel', ' me has puesto la piel de gallina 😳', ' el de siempre, haciendo lo de siempre...', ' está loco 😲', ' es el puto amo 👍', ' cerrando ortos nivel dios 👉👌 😎', ' te gana los partidos solo ✌', ' la tiene afuera 🙈', ' es el rey de reyes 👑 🤴', ' da igual cuando leas ésto. Éste tipo no para de romperla 😵', ' el amo del juego 😎', ' no tiene límites 👏', ' naaaah sos un extraterrestre 👽', ' está enfermo 😵', ' no hay dudas, eres el mejor de todos 🙉 👌👌', '  que barbaridad lo de este hombre 👏👏👏', ' con que facilidad juega éste muchacho', ' dando cátedra de como jugar haxball 👏👏', ' no tengo palabras, no tengo nada que decir, se me acabaron las palabras para describir lo que es éste fenómeno. 👏👏 🙇🙇', ' me muerooooooooooooooo! vieron lo que hizo éste tipo? 🔥🔥🔥', ' simplemente una maravilla 😍', ' la leyenda continua', ' ¿Lo pedían? Ahí lo tienen. 😎', ' apareciendo cuando más se le necesita, el amo y señor del haxball. 🙇', ' no hay jugador que pueda con él y lo sigue demostrando'];
    var fraserandom = ComentariosRandomBot[(Math.random() * ComentariosRandomBot.length) | 0]
    room.sendAnnouncement("ℛᴇʟᴀᴛᴏʀ 🗣 🎙: " + whoTouchedBall[0].name + fraserandom, null, 0xf1a400, 'normal', 0);
    }
    if (redTeam.length > '4' && blueTeam.length < '4'){
    goalScored = true;
    var time = room.getScores().time;
    var m = Math.trunc(time/60); var s = Math.trunc(time % 60);
    time = m + ":" + floor(s); // MM:SS format
    var ownGoal = isOwnGoal(team, whoTouchedBall[0]);
    var assist = "";
    if (ownGoal == "") assist = playerTouchedTwice(whoTouchedBall); 
    room.sendAnnouncement("      ⚽ 𝑮𝑶𝑳 marcado por " + whoTouchedBall[0].name +
     assist + ownGoal + " a los [🕒   " +
     time + " ] para el " + team_name(team), null, 0xffd800, 'normal', 0);
    room.sendAnnouncement("      🎰 𝗠 𝗔 𝗥 𝗖 𝗔 𝗗 𝗢 𝗥 :      " + team_color(1) + "      " +
                    scorerNumber(room.getScores().red) + "      -      " + scorerNumber(room.getScores().blue) + "      " + team_color(2), null, 0xffd800, 'normal', 0);
    var ComentariosRandomBot = [' magnífica actuación', ' uuuuffff que fenómeno', ' es un jugador por encima de la media.', ' a eso yo le llamo tener calidad!', ' más 3', ', que pedazo de jugador!!', ' siempre hace la diferencia', ' lo hizo de nuevo, es un fuera de serie.', ' está on fire 🔥🔥🔥', ' de qué planeta viniste?', ' siempre demostrando porqué le dicen "el mejor del host"', ' OOOOOOOO que verdadero crack', ' vestite!', ' juega desnudo', ' vacunando rivales desde tiempo inmemoriales', ' en modo diablo 🤘 👿', 'en modo cristo ✝', ' que lujo es verte jugar', 'dependencia. Juega y hace jugar éste verdadero crack', ' es de otro nivel', ' me has puesto la piel de gallina 😳', ' el de siempre, haciendo lo de siempre...', ' está loco 😲', ' es el puto amo 👍', ' cerrando ortos nivel dios 👉👌 😎', ' te gana los partidos solo ✌', ' la tiene afuera 🙈', ' es el rey de reyes 👑 🤴', ' da igual cuando leas ésto. Éste tipo no para de romperla 😵', ' el amo del juego 😎', ' no tiene límites 👏', ' naaaah sos un extraterrestre 👽', ' está enfermo 😵', ' no hay dudas, eres el mejor de todos 🙉 👌👌', '  que barbaridad lo de este hombre 👏👏👏', ' con que facilidad juega éste muchacho', ' dando cátedra de como jugar haxball 👏👏', ' no tengo palabras, no tengo nada que decir, se me acabaron las palabras para describir lo que es éste fenómeno. 👏👏 🙇🙇', ' me muerooooooooooooooo! vieron lo que hizo éste tipo? 🔥🔥🔥', ' simplemente una maravilla 😍', ' la leyenda continua', ' ¿Lo pedían? Ahí lo tienen. 😎', ' apareciendo cuando más se le necesita, el amo y señor del haxball. 🙇', ' no hay jugador que pueda con él y lo sigue demostrando'];
    var fraserandom = ComentariosRandomBot[(Math.random() * ComentariosRandomBot.length) | 0]
    room.sendAnnouncement("ℛᴇʟᴀᴛᴏʀ 🗣 🎙: " + whoTouchedBall[0].name + fraserandom, null, 0xf1a400, 'normal', 0);
    }
    if (redTeam.length < '4' && blueTeam.length > '4'){
    goalScored = true;
    var time = room.getScores().time;
    var m = Math.trunc(time/60); var s = Math.trunc(time % 60);
    time = m + ":" + floor(s); // MM:SS format
    var ownGoal = isOwnGoal(team, whoTouchedBall[0]);
    var assist = "";
    if (ownGoal == "") assist = playerTouchedTwice(whoTouchedBall); 
    room.sendAnnouncement("      ⚽ 𝑮𝑶𝑳 marcado por " + whoTouchedBall[0].name +
     assist + ownGoal + " a los [🕒   " +
     time + " ] para el " + team_name(team), null, 0xffd800, 'normal', 0);
    room.sendAnnouncement("      🎰 𝗠 𝗔 𝗥 𝗖 𝗔 𝗗 𝗢 𝗥 :      " + team_color(1) + "      " +
                    scorerNumber(room.getScores().red) + "      -      " + scorerNumber(room.getScores().blue) + "      " + team_color(2), null, 0xffd800, 'normal', 0);
    var ComentariosRandomBot = [' magnífica actuación', ' uuuuffff que fenómeno', ' es un jugador por encima de la media.', ' a eso yo le llamo tener calidad!', ' más 3', ', que pedazo de jugador!!', ' siempre hace la diferencia', ' lo hizo de nuevo, es un fuera de serie.', ' está on fire 🔥🔥🔥', ' de qué planeta viniste?', ' siempre demostrando porqué le dicen "el mejor del host"', ' OOOOOOOO que verdadero crack', ' vestite!', ' juega desnudo', ' vacunando rivales desde tiempo inmemoriales', ' en modo diablo 🤘 👿', 'en modo cristo ✝', ' que lujo es verte jugar', 'dependencia. Juega y hace jugar éste verdadero crack', ' es de otro nivel', ' me has puesto la piel de gallina 😳', ' el de siempre, haciendo lo de siempre...', ' está loco 😲', ' es el puto amo 👍', ' cerrando ortos nivel dios 👉👌 😎', ' te gana los partidos solo ✌', ' la tiene afuera 🙈', ' es el rey de reyes 👑 🤴', ' da igual cuando leas ésto. Éste tipo no para de romperla 😵', ' el amo del juego 😎', ' no tiene límites 👏', ' naaaah sos un extraterrestre 👽', ' está enfermo 😵', ' no hay dudas, eres el mejor de todos 🙉 👌👌', '  que barbaridad lo de este hombre 👏👏👏', ' con que facilidad juega éste muchacho', ' dando cátedra de como jugar haxball 👏👏', ' no tengo palabras, no tengo nada que decir, se me acabaron las palabras para describir lo que es éste fenómeno. 👏👏 🙇🙇', ' me muerooooooooooooooo! vieron lo que hizo éste tipo? 🔥🔥🔥', ' simplemente una maravilla 😍', ' la leyenda continua', ' ¿Lo pedían? Ahí lo tienen. 😎', ' apareciendo cuando más se le necesita, el amo y señor del haxball. 🙇', ' no hay jugador que pueda con él y lo sigue demostrando'];
    var fraserandom = ComentariosRandomBot[(Math.random() * ComentariosRandomBot.length) | 0]
    room.sendAnnouncement("ℛᴇʟᴀᴛᴏʀ 🗣 🎙: " + whoTouchedBall[0].name + fraserandom, null, 0xf1a400, 'normal', 0);
    }
    if (redTeam.length > '4' && blueTeam.length > '4'){
    goalScored = true;
    var time = room.getScores().time;
    var m = Math.trunc(time/60); var s = Math.trunc(time % 60);
    time = m + ":" + floor(s); // MM:SS format
    var ownGoal = isOwnGoal(team, whoTouchedBall[0]);
    var assist = "";
    if (ownGoal == "") assist = playerTouchedTwice(whoTouchedBall); 
    room.sendAnnouncement("      ⚽ 𝑮𝑶𝑳 marcado por " + whoTouchedBall[0].name +
     assist + ownGoal + " a los [🕒   " +
     time + " ] para el " + team_name(team), null, 0xffd800, 'normal', 0);
    room.sendAnnouncement("      🎰 𝗠 𝗔 𝗥 𝗖 𝗔 𝗗 𝗢 𝗥 :      " + team_color(1) + "      " +
                    scorerNumber(room.getScores().red) + "      -      " + scorerNumber(room.getScores().blue) + "      " + team_color(2), null, 0xffd800, 'normal', 0);
    var ComentariosRandomBot = [' magnífica actuación', ' uuuuffff que fenómeno', ' es un jugador por encima de la media.', ' a eso yo le llamo tener calidad!', ' más 3', ', que pedazo de jugador!!', ' siempre hace la diferencia', ' lo hizo de nuevo, es un fuera de serie.', ' está on fire 🔥🔥🔥', ' de qué planeta viniste?', ' siempre demostrando porqué le dicen "el mejor del host"', ' OOOOOOOO que verdadero crack', ' vestite!', ' juega desnudo', ' vacunando rivales desde tiempo inmemoriales', ' en modo diablo 🤘 👿', 'en modo cristo ✝', ' que lujo es verte jugar', 'dependencia. Juega y hace jugar éste verdadero crack', ' es de otro nivel', ' me has puesto la piel de gallina 😳', ' el de siempre, haciendo lo de siempre...', ' está loco 😲', ' es el puto amo 👍', ' cerrando ortos nivel dios 👉👌 😎', ' te gana los partidos solo ✌', ' la tiene afuera 🙈', ' es el rey de reyes 👑 🤴', ' da igual cuando leas ésto. Éste tipo no para de romperla 😵', ' el amo del juego 😎', ' no tiene límites 👏', ' naaaah sos un extraterrestre 👽', ' está enfermo 😵', ' no hay dudas, eres el mejor de todos 🙉 👌👌', '  que barbaridad lo de este hombre 👏👏👏', ' con que facilidad juega éste muchacho', ' dando cátedra de como jugar haxball 👏👏', ' no tengo palabras, no tengo nada que decir, se me acabaron las palabras para describir lo que es éste fenómeno. 👏👏 🙇🙇', ' me muerooooooooooooooo! vieron lo que hizo éste tipo? 🔥🔥🔥', ' simplemente una maravilla 😍', ' la leyenda continua', ' ¿Lo pedían? Ahí lo tienen. 😎', ' apareciendo cuando más se le necesita, el amo y señor del haxball. 🙇', ' no hay jugador que pueda con él y lo sigue demostrando'];
    var fraserandom = ComentariosRandomBot[(Math.random() * ComentariosRandomBot.length) | 0]
    room.sendAnnouncement("ℛᴇʟᴀᴛᴏʀ 🗣 🎙: " + whoTouchedBall[0].name + fraserandom, null, 0xf1a400, 'normal', 0);
    }
    if (redTeam.length < '4' && blueTeam.length < '4'){
    goalScored = true;
    var time = room.getScores().time;
    var m = Math.trunc(time/60); var s = Math.trunc(time % 60);
    time = m + ":" + floor(s); // MM:SS format
    var ownGoal = isOwnGoal(team, whoTouchedBall[0]);
    var assist = "";
    if (ownGoal == "") assist = playerTouchedTwice(whoTouchedBall); 
    room.sendAnnouncement("      ⚽ 𝑮𝑶𝑳 marcado por " + whoTouchedBall[0].name +
     assist + ownGoal + " a los [🕒   " +
     time + " ] para el " + team_name(team), null, 0xffd800, 'normal', 0);
    room.sendAnnouncement("      🎰 𝗠 𝗔 𝗥 𝗖 𝗔 𝗗 𝗢 𝗥 :      " + team_color(1) + "      " +
                    scorerNumber(room.getScores().red) + "      -      " + scorerNumber(room.getScores().blue) + "      " + team_color(2), null, 0xffd800, 'normal', 0);
    var ComentariosRandomBot = [' magnífica actuación', ' uuuuffff que fenómeno', ' es un jugador por encima de la media.', ' a eso yo le llamo tener calidad!', ' más 3', ', que pedazo de jugador!!', ' siempre hace la diferencia', ' lo hizo de nuevo, es un fuera de serie.', ' está on fire 🔥🔥🔥', ' de qué planeta viniste?', ' siempre demostrando porqué le dicen "el mejor del host"', ' OOOOOOOO que verdadero crack', ' vestite!', ' juega desnudo', ' vacunando rivales desde tiempo inmemoriales', ' en modo diablo 🤘 👿', 'en modo cristo ✝', ' que lujo es verte jugar', 'dependencia. Juega y hace jugar éste verdadero crack', ' es de otro nivel', ' me has puesto la piel de gallina 😳', ' el de siempre, haciendo lo de siempre...', ' está loco 😲', ' es el puto amo 👍', ' cerrando ortos nivel dios 👉👌 😎', ' te gana los partidos solo ✌', ' la tiene afuera 🙈', ' es el rey de reyes 👑 🤴', ' da igual cuando leas ésto. Éste tipo no para de romperla 😵', ' el amo del juego 😎', ' no tiene límites 👏', ' naaaah sos un extraterrestre 👽', ' está enfermo 😵', ' no hay dudas, eres el mejor de todos 🙉 👌👌', '  que barbaridad lo de este hombre 👏👏👏', ' con que facilidad juega éste muchacho', ' dando cátedra de como jugar haxball 👏👏', ' no tengo palabras, no tengo nada que decir, se me acabaron las palabras para describir lo que es éste fenómeno. 👏👏 🙇🙇', ' me muerooooooooooooooo! vieron lo que hizo éste tipo? 🔥🔥🔥', ' simplemente una maravilla 😍', ' la leyenda continua', ' ¿Lo pedían? Ahí lo tienen. 😎', ' apareciendo cuando más se le necesita, el amo y señor del haxball. 🙇', ' no hay jugador que pueda con él y lo sigue demostrando'];
    var fraserandom = ComentariosRandomBot[(Math.random() * ComentariosRandomBot.length) | 0]
    room.sendAnnouncement("ℛᴇʟᴀᴛᴏʀ 🗣 🎙: " + whoTouchedBall[0].name + fraserandom, null, 0xf1a400, 'normal', 0);
    }
    if (redTeam.length == blueTeam.length && redTeam.length == '4' && blueTeam.length == '4'){
    goalScored = true;
    var time = room.getScores().time;
    var m = Math.trunc(time/60); var s = Math.trunc(time % 60);
    time = m + ":" + floor(s); // MM:SS format
    var ownGoal = isOwnGoal(team, whoTouchedBall[0]);
    var assist = "";
    if (ownGoal == "") assist = playerTouchedTwice(whoTouchedBall);
 
    let account = HackHax.find(a => a.playerId === whoTouchedBall[0].id);
    if (account !== undefined) {
 
    room.sendAnnouncement("      ⎮ ⚽ 𝑮𝑶𝑳 marcado por " + whoTouchedBall[0].name + "⎮ [" + account.GrandesLigas + "]" +
     assist + ownGoal + " ⎮ A los [🕒   " +
     time + " ] para el " + team_name(team), null, 0xffd800, 'normal', 0);
    room.sendAnnouncement("      🎰 𝗠 𝗔 𝗥 𝗖 𝗔 𝗗 𝗢 𝗥 :      " + team_color(1) + "      " +
                    scorerNumber(room.getScores().red) + "      -      " + scorerNumber(room.getScores().blue) + "      " + team_color(2), null, 0xffd800, 'normal', 0);
    var ComentariosRandomBot = [' magnífica actuación', ' uuuuffff que fenómeno', ' es un jugador por encima de la media.', ' a eso yo le llamo tener calidad!', ' más 3', ', que pedazo de jugador!!', ' siempre hace la diferencia', ' lo hizo de nuevo, es un fuera de serie.', ' está on fire 🔥🔥🔥', ' de qué planeta viniste?', ' siempre demostrando porqué le dicen "el mejor del host"', ' OOOOOOOO que verdadero crack', ' vestite!', ' juega desnudo', ' vacunando rivales desde tiempo inmemoriales', ' en modo diablo 🤘 👿', 'en modo cristo ✝', ' que lujo es verte jugar', 'dependencia. Juega y hace jugar éste verdadero crack', ' es de otro nivel', ' me has puesto la piel de gallina 😳', ' el de siempre, haciendo lo de siempre...', ' está loco 😲', ' es el puto amo 👍', ' cerrando ortos nivel dios 👉👌 😎', ' te gana los partidos solo ✌', ' la tiene afuera 🙈', ' es el rey de reyes 👑 🤴', ' da igual cuando leas ésto. Éste tipo no para de romperla 😵', ' el amo del juego 😎', ' no tiene límites 👏', ' naaaah sos un extraterrestre 👽', ' está enfermo 😵', ' no hay dudas, eres el mejor de todos 🙉 👌👌', '  que barbaridad lo de este hombre 👏👏👏', ' con que facilidad juega éste muchacho', ' dando cátedra de como jugar haxball 👏👏', ' no tengo palabras, no tengo nada que decir, se me acabaron las palabras para describir lo que es éste fenómeno. 👏👏 🙇🙇', ' me muerooooooooooooooo! vieron lo que hizo éste tipo? 🔥🔥🔥', ' simplemente una maravilla 😍', ' la leyenda continua', ' ¿Lo pedían? Ahí lo tienen. 😎', ' apareciendo cuando más se le necesita, el amo y señor del haxball. 🙇', ' no hay jugador que pueda con él y lo sigue demostrando'];
    var fraserandom = ComentariosRandomBot[(Math.random() * ComentariosRandomBot.length) | 0]
    room.sendAnnouncement("ℛᴇʟᴀᴛᴏʀ 🗣 🎙: " + whoTouchedBall[0].name + fraserandom, null, 0xf1a400, 'normal', 0);
 
     if (ownGoal != "") {
     } else {
         stats[account.GrandesLigas][0] += 1;
     }
    }
    else {
    room.sendAnnouncement("      ⚽ 𝑮𝑶𝑳 marcado por " + whoTouchedBall[0].name +
     assist + ownGoal + " a los [🕒   " +
     time + " ] para el " + team_name(team), null, 0xffd800, 'normal', 0);
    room.sendAnnouncement("      🎰 𝗠 𝗔 𝗥 𝗖 𝗔 𝗗 𝗢 𝗥 :      " + team_color(1) + "      " +
                    scorerNumber(room.getScores().red) + "      -      " + scorerNumber(room.getScores().blue) + "      " + team_color(2), null, 0xffd800, 'normal', 0);
    var ComentariosRandomBot = [' magnífica actuación', ' uuuuffff que fenómeno', ' es un jugador por encima de la media.', ' a eso yo le llamo tener calidad!', ' más 3', ', que pedazo de jugador!!', ' siempre hace la diferencia', ' lo hizo de nuevo, es un fuera de serie.', ' está on fire 🔥🔥🔥', ' de qué planeta viniste?', ' siempre demostrando porqué le dicen "el mejor del host"', ' OOOOOOOO que verdadero crack', ' vestite!', ' juega desnudo', ' vacunando rivales desde tiempo inmemoriales', ' en modo diablo 🤘 👿', 'en modo cristo ✝', ' que lujo es verte jugar', 'dependencia. Juega y hace jugar éste verdadero crack', ' es de otro nivel', ' me has puesto la piel de gallina 😳', ' el de siempre, haciendo lo de siempre...', ' está loco 😲', ' es el puto amo 👍', ' cerrando ortos nivel dios 👉👌 😎', ' te gana los partidos solo ✌', ' la tiene afuera 🙈', ' es el rey de reyes 👑 🤴', ' da igual cuando leas ésto. Éste tipo no para de romperla 😵', ' el amo del juego 😎', ' no tiene límites 👏', ' naaaah sos un extraterrestre 👽', ' está enfermo 😵', ' no hay dudas, eres el mejor de todos 🙉 👌👌', '  que barbaridad lo de este hombre 👏👏👏', ' con que facilidad juega éste muchacho', ' dando cátedra de como jugar haxball 👏👏', ' no tengo palabras, no tengo nada que decir, se me acabaron las palabras para describir lo que es éste fenómeno. 👏👏 🙇🙇', ' me muerooooooooooooooo! vieron lo que hizo éste tipo? 🔥🔥🔥', ' simplemente una maravilla 😍', ' la leyenda continua', ' ¿Lo pedían? Ahí lo tienen. 😎', ' apareciendo cuando más se le necesita, el amo y señor del haxball. 🙇', ' no hay jugador que pueda con él y lo sigue demostrando'];
    var fraserandom = ComentariosRandomBot[(Math.random() * ComentariosRandomBot.length) | 0]
    room.sendAnnouncement("ℛᴇʟᴀᴛᴏʀ 🗣 🎙: " + whoTouchedBall[0].name + fraserandom, null, 0xf1a400, 'normal', 0);
    }
    let account1 = HackHax.find(a => a.playerId === whoTouchedBall[1].id);
    if (account1 !== undefined) {
    if (whoTouchedBall[1] != init && assist != "") stats[account1.GrandesLigas][1] += 1;
    }
    else{
    if (whoTouchedBall[1] != init && assist != "");
    }
 
 
    if (scorers == undefined) scorers = new Map(); // Initializing dict of scorers
    whoTouchedBall = [init, init];
    whoTouchedLast = undefined;
    saveStatsFun();
}}
room.onPositionsReset = function(){
    let id = Object.keys(tookASize);
    let size;
    for (var i = 0; i < id.length; i++) {
        if (tookASize.hasOwnProperty(id[i])){
            size = tookASize[id[i]];
            room.setPlayerDiscProperties(id[i], {radius: size, invMass: size / 30});
        }
    }
}
    goalScored = false;
 
 
room.onTeamVictory = function(scores){ // Sum up all scorers since the beginning of the match.
    goalScored = true;
    var time = room.getScores().time;
    var m = Math.trunc(time/60); var s = Math.trunc(time % 60);
    time = m + ":" + floor(s); // MM:SS format
    var scores = room.getScores();
    var actualTimeAdded = Math.round((timeOutside-(100*0))/60);
    if (redTeam.length < '4' && redTeam.length == blueTeam.length){
    teamPossFun();
    room.sendChat(" ⏰ 𝚃𝙸𝙴𝙼𝙿𝙾: [" + time + "]");
    room.sendAnnouncement("█████████████████████ ⚽️ 𝙼 𝙰 𝚁 𝙲 𝙰 𝙳 𝙾 𝚁 :      " + team_color(1) + "      " +
                    scorerNumber(room.getScores().red) + "      -      " + scorerNumber(room.getScores().blue) + "      " + team_color(2) + " █████████████████████", null, 0xffd559, "normal", 1)
    isTimeAddedShownsiete = true;
}
    if (redTeam.length > '4' && redTeam.length == blueTeam.length){
    teamPossFun();
    room.sendChat(" ⏰ 𝚃𝙸𝙴𝙼𝙿𝙾: [" + time + "]");
    room.sendAnnouncement("█████████████████████ ⚽️ 𝙼 𝙰 𝚁 𝙲 𝙰 𝙳 𝙾 𝚁 :      " + team_color(1) + "      " +
                    scorerNumber(room.getScores().red) + "      -      " + scorerNumber(room.getScores().blue) + "      " + team_color(2) + " █████████████████████", null, 0xffd559, "normal", 1)
    isTimeAddedShownsiete = true;
}
    if (redTeam.length == '4' && redTeam.length == blueTeam.length){
    teamPossFun();
    room.sendChat(" ⏰ 𝚃𝙸𝙴𝙼𝙿𝙾: [" + time + "]");
    room.sendAnnouncement("█████████████████████ ⚽️ 𝙼 𝙰 𝚁 𝙲 𝙰 𝙳 𝙾 𝚁 :      " + team_color(1) + "      " +
                    scorerNumber(room.getScores().red) + "      -      " + scorerNumber(room.getScores().blue) + "      " + team_color(2) + " █████████████████████", null, 0xffd559, "normal", 1)
    isTimeAddedShownsiete = true;
}
}
 
room.onGameStop = function(){
    scorers = undefined;
    whoTouchedBall = [init, init];
    whoTouchedLast = undefined;
    gk = [init, init];
    kickOff = false;
    hasFinished = false;
}
 
function getNewRating(myRating, opponentRating, myGameResult) {
  return myRating + getRatingDelta(myRating, opponentRating, myGameResult);
}
 
var _savestatsInterval = 15769500 * 15769500;
SaveStats = setInterval(function() {saveStatsFun();},_savestatsInterval);
 
function download(data, filename, type) {
    var file = new Blob([data], {type: type});
    var a = document.createElement("a"),
            url = URL.createObjectURL(file);
    a.href = url;
    a.download = filename;
    document.body.appendChild(a);
    a.click();
    setTimeout(function() {
        document.body.removeChild(a);
        window.URL.revokeObjectURL(url);  
    }, 0);
}


    // IPS BANEADAS
const IpsBaneada1 = ["38382E3234362E32342E3533"];
const IpsBaneada2 = ["3133382E3131372E32312E3335"];
const IpsBaneada3 = ["38382E3234362E32342E3533"];
const IpsBaneada4 = ["3139302E3130352E38302E3336"]; // OneChope
const IpsBaneada5 = ["3137392E35372E3135392E35"]; // Cucumuelo
const IpsBaneada6 = ["3138312E37332E3232392E313131"]; // Gordito
const IpsBaneada7 = ["3138312E3136362E38302E313830"]; // 𝓐𝓮𝓰𝓸𝓷 [𝔸𝓵𝕄𝕥]
const IpsBaneada8 = ["3135322E3137312E3132352E313131"]; // Uno que le hizo du a cerv1
const IpsBaneada9 = ["3139302E31382E33382E3632"]; // Uno usa nicks insultando a BARBA RETIRADA
const IpsBaneada10 = ["3138362E32332E3134332E3738"]; // Uno usa nicks insultando a BARBA RETIRADA y a Joyita
const IpsBaneada11 = ["3137392E35372E3135342E313433"]; // Cucumuelo
const IpsBaneada12 = ["3138312E34352E3131342E323233"]; // Van Dijk (Que dice que no es)
const IpsBaneada13 = ["3136372E36322E3138342E3236"]; // Spammea en Mayúsculas y pide admin (Nick: GOD)
const IpsBaneada14 = ["3138312E3136362E38302E313830"]; // Uno que le hace du a cerv1
const IpsBaneada15 = ["3138312E3232392E37302E323330"]; // Taggear "DOWNB3TO ROÑOSO"
const IpsBaneada16 = ["3138312E34352E32302E313837"]; // Taggear "BEBELO SOBA PENE"
const IpsBaneada17 = ["3138362E3133362E3230382E313630"]; // Gordo Ronaldo (Pele)
const IpsBaneada18 = ["3138362E35392E3135362E313636"]; // Darthes por insultar con sangre sucia, asco
const IpsBaneada19 = ["3138312E3233392E3232352E3533"]; // !Chano
const IpsBaneada20 = ["3138362E35392E3138302E3331"]; // Darthes ip n°2
const IpsBaneada22 = ["3139312E3130392E31322E3733"]; // 𝓐𝓁𝒾𝓈𝑜𝓃 𝓑𝒆𝓬𝓴𝒆𝓻
const IpsBaneada23 = ["34352E352E36382E3436"]; // ƙ⍨ʀᵻ𝓉ᴀ_➢[ȵāȼ
const IpsBaneada24 = ["3230312E3235322E39342E3934"]; // Guaraní
const IpsBaneada25 = ["3138362E35392E3133362E313536"]; // El Niño (Por insultar y realizar denuncias falsas)
const IpsBaneada26 = ["3139302E3232392E31342E313931"]; // serete
const IpsBaneada27 = ["3138312E3232362E37362E3336"]; // cucumuelo ip 2
const IpsBaneada28 = ["3230312E3231352E3234322E3936"]; // Miño Blandi
const IpsBaneada29 = ["3139302E35352E34362E323038"]; // Wanchope
const IpsBaneada30 = ["3138362E31392E3130352E313932"]; // Uno insultando a Bakunin
const IpsBaneada31 = ["3138312E34332E37382E3238"]; // Nunos
const IpsBaneada32 = ["3138392E37332E3134392E3333"]; // EL PEPE
const IpsBaneada33 = ["3230302E3230332E32302E313033"]; // EL PEPE 2da IP
const IpsBaneada34 = ["3139302E3232352E39352E3638"]; // Shawn Mendes (Guarani segunda ip)
const IpsBaneada35 = ["3138362E35392E3134362E3334"]; // El niño (Munir)
const IpsBaneada36 = ["3230302E3132372E38302E313039"]; // Uno que insultó a AgusFer
const IpsBaneada37 = ["3139302E3232382E3234342E323533"]; // Shawn
const IpsBaneada38 = ["3138362E32302E3231362E323135"]; // Empanadita
const IpsBaneada39 = ["3138312E3136362E36342E313735"]; // ROJOMAN
const IpsBaneada40 = ["33372E3133302E3232342E3231"]; // Shawn ip3
const IpsBaneada41 = ["3138362E35392E3232372E3236"]; // El Niño IP 2
const IpsBaneada42 = ["3135392E3235332E3134352E313833"]; // AnonymoX 1
const IpsBaneada43 = ["33372E3133302E3232342E3232"]; // AnonymoX 2 
const IpsBaneada44 = ["33372E3133302E3232392E313439"]; // AnonymoX 3 
const IpsBaneada45 = ["3134362E3138352E33312E323134"]; // AnonymoX 4 
const IpsBaneada46 = ["32332E3233352E3232372E313036"]; // AnonymoX 5 
const IpsBaneada47 = ["32332E3233352E3232372E313038"]; // AnonymoX 6 
const IpsBaneada48 = ["33372E3133302E3232342E323032"]; // AnonymoX 7 
const IpsBaneada49 = ["3134362E3138352E33312E323231"]; // AnonymoX 8 
const IpsBaneada50 = ["3134362E3138352E33312E323133"]; // AnonymoX 9 - uk5g - La que utilizará hazard
const IpsBaneada51 = ["3139382E32342E3136322E313739"]; // AnonymoX 10
const IpsBaneada52 = ["32332E3233352E3232372E313039"]; // AnonymoX 11
const IpsBaneada53 = ["3139302E3232352E3233312E313638"]; //  MamaLéguas (shawn)
const IpsBaneada54 = ["3139302E3136312E3134372E3531"]; // FUTEBOLTOTAL
const IpsBaneada55 = ["3138352E3234382E3130332E313634"]; // FUTEBOLTOTAL 2
const IpsBaneada56 = ["3139302E3137332E36382E3135"]; // Fran
const IpsBaneada57 = ["3139302E3137332E3131382E323235"]; // Fran - ip 2
const IpsBaneada58 = ["3138312E3136372E382E323036"]; // Du a Arii (Kas Kali Discord: #4024)
const IpsBaneada59 = ["3138312E3136362E36332E313834"]; // ROJOMAN 2
const IpsBaneada60 = ["3139312E3131392E32382E313236"]; // SHECKA CHUPAME LA CORNETA - Ver mensaje Shecka privado
const IpsBaneada61 = ["3139302E3232392E31342E3737"]; // Clonn - Trollea - Goles En contra
const IpsBaneada62 = ["3138312E39382E34382E3433"]; // Clonn Ip 2 | scealeo#1785
const IpsBaneada63 = ["3138362E32322E32322E3235352E313839"]; // TIRADOR DE HOST
const IpsBaneada64 = ["3139302E31372E3134312E323135"]; // Socrates
const IpsBaneada65 = ["32342E3233322E31322E3433"]; // Haland
const IpsBaneada66 = ["3138312E39352E3133332E3736"]; // fran 2da ip
const IpsBaneada67 = ["3138312E34332E3132392E39"]; // Haland segunda ip
const IpsBaneada69 = ["3137392E392E3230382E3232"]; // W. Montillo (verdadero)
const IpsBaneada70 = ["3139302E3137332E3131322E3136"]; // fran 3ra ip
const IpsBaneada71 = ["3139312E3132362E3133352E3730"]; // PEKE_77
const IpsBaneada72 = ["3138312E34332E3132382E3632"]; // Haland tercera ip
const IpsBaneada73 = ["3137392E3137362E37352E3437"]; // Haland cuarta ip
const IpsBaneada74 = ["3139302E3137332E3131322E323134"]; // fran 4ta
const IpsBaneada75 = ["3139302E3137332E3130332E313435"]; // fran 5ta
const IpsBaneada76 = ["3230302E3132302E3138302E3230"]; // replik por trollear
const IpsBaneada77 = ["3139302E3132332E3130312E3238"]; // replik 2da IP
const IpsBaneada78 = ["3133382E3235352E3137312E3731"]; // maldini - Provocar a Barbilla Roja
const IpsBaneada79 = ["3137372E31382E35342E313330"]; // 890 - jugador troll
const IpsBaneada80 = ["3137372E3135372E3135352E323535"]; // Du a BARBA RETIRADA 
const IpsBaneada81 = ["3230302E3131342E3139372E313434"]; // Maria Becerra
const IpsBaneada82 = ["3135322E3136382E34302E313235"]; // bonjog_gordx_putx_y_cagx
const IpsBaneada83 = ["3138312E34372E3230382E323136"]; // ß€ß€ NOALPERONISMO para que diga quien le pasó la clave de superadmin

    // IPS SUPERADMINS
const IpSuperAdmin = ["3135322E3137312E3137332E313235"]; // maxi velazquez
const IpSuperAdmin2 = ["3137302E3234362E3138332E31"]; // Marcos #10
const IpSuperAdmin3 = ["3139302E35352E3131332E3238"]; // Era Istefi
const IpSuperAdmin4 = ["3138362E36302E3233322E3139"]; // AppleJack
const IpSuperAdmin5 = ["3139302E3139302E38352E3636"]; // Welmaa
const IpSuperAdmin7 = ["3230302E36332E33352E3932"]; // almada cc ✿#7479
const IpSuperAdmin8 = ["3139302E3137322E3134372E323133"]; // Lucas Martinez & Gian Mancini
const IpSuperAdmin9 = ["3230302E3131342E3139372E313434"]; // Arii♪
const IpSuperAdmin11 = ["3138312E34372E39372E313830"]; // bonjog
const IpSuperAdmin12 = ["3230312E3231332E3231312E323438"]; // Loquito HD
const IpSuperAdmin13 = ["3230302E37342E34382E3832"]; // Neos
const IpSuperAdmin14 = ["3138362E32322E32362E3533"]; // 𝐀rriabazalga
const IpSuperAdmin15 = ["3138312E39372E39312E36"]; // Cleopatra VII

    // IPS JUGADORES
const IpJugador = ["3139302E3133332E37362E313130"]; // Paco Sanz
const IpJugador3 = ["3139312E3131342E3134302E3334"]; // Higuain €L P€PØ ᵀᵐᶜ (discord: #0205)
const IpJugador4 = ["3138312E3137312E3134362E3531"]; // SantiGuima#2771
const IpJugador5 = ["3230302E3132372E3231322E313436"]; // Islas Vírgenes
const IpJugador6 = ["3136372E35382E39322E313838"]; // Berubi
const IpJugador7 = ["3138312E34342E31362E3330"]; // Gringo Heinze #8857
const IpJugador8 = ["3139302E3232362E37332E313931"]; // Toby Dramas
const IpJugador9 = ["3138362E3133342E3139362E313735"]; // Gonzalo Maroni #7053
const IpJugador10 = ["3138312E32382E3131392E3834"]; // Simon Kjaer #4655
const IpJugador11 = ["3137372E31312E3136332E3338"]; // About Mani #5460
const IpJugador12 = ["3230302E38362E3230342E3337"]; // Diego Costa #9706
const IpJugador13 = ["3136382E3139342E3136342E313530"]; // ¥ŇØØβƤŁΔ¥€Ř #1893 Nick Ⓗⓐⓟⓟⓘⓔⓡ

room.onPlayerJoin = function(player) {
	CreateOyuncu(player);
	  if(player.name == "GLH" && player.auth != auth){room.kickPlayer(player.id,"❌ " + player.name + "  𝐄𝐑𝐄𝐒 𝐔𝐍 𝐈𝐌𝐏𝐎𝐒𝐓𝐎𝐑 (𝐃𝐔)!",false);}
	  if(player.name == "Grandes Ligas HaxBall" && player.auth != auth){room.kickPlayer(player.id,"❌ " + player.name + "  𝐄𝐑𝐄𝐒 𝐔𝐍 𝐈𝐌𝐏𝐎𝐒𝐓𝐎𝐑 (𝐃𝐔)!",false);}


   let conn = connections.find(a => a[1] === player.conn);
            if (conn) {
             room.kickPlayer(player.id,"𝚂𝙾́𝙻𝙾 𝚄𝙽 𝙹𝚄𝙶𝙰𝙳𝙾𝚁 𝙿𝙾𝚁 𝙸𝙿 ❌",true);
            }
            else {
            connections.push([player.id, player.conn]);
            }



    if (db.log.filter((p) => p.id == player.id).length == 0) { db.log.push({ id: player.id, lm: [] }); }
    checkBanedAdmins(player);
    BaneandoGenteProhibidaFun(player);
    clonekick(player);
    playerName = player.name.replace(/ /g,"_");
    var SaludosRandomBot = [' bienvenido al host!', ' ojalá la pases bien!', ', acabas de unirte al host.', ' te damos las bienvenida.', ', nos alegra mucho que nos elijas!', ' hola!  llegó el más crack.', ' nos hacias falta en éste host.', ' hola!!!', ' gracias por unirte a nuestra comunidad.', ' te damos la bienvenida', ' ha llegado. Se acabó la fiesta.', ' te estábamos esperando', ' está aquí, tal y como predijo la profecía.', ' acaba de unirse. ¡Hagan como que están jugando!', ' acaba de aterrizar', ' se ha unido.', ' ha venido a carrear conos y a marcar muchos goles.', ' está aquí.', ' se ha unido al host! ¡Es superefectivo!', ' se ha unido. Ahora deberán jugar más que el 100%.', ' acaba de unirse... ¿O no?', ' MIRÁ QUIÉN LLEGÓ ¡Es un pájaro! ¡Es un avión! Ah no, no he dicho nada. Flashé', ' hola! quédate un rato y disfruta.', ' llegó el más grande.', ' ha ingresado. Eh muchachos, miren quién llegó.', ' Te estábamos esperando ( ͡° ͜ʖ ͡°)', ' se ha unido al host.', ' acaba de llegar.', ' apareció! cuidado que es salvaje.', ' Hola!! Alguien lo andaba buscando?', ' te estabamos esperando!'];
    var GeneradorRandom = SaludosRandomBot[(Math.random() * SaludosRandomBot.length) | 0]
    room.sendAnnouncement("[📶] IP del jugador: " + player.conn + " | Nickname: @" + playerName , null, 0x06ff00, 'bold', 0);

setTimeout(function(){
room.sendAnnouncement(" @" + playerName + GeneradorRandom , player.id, 0x00FFB3, "normal", 0);
room.sendAnnouncement("@" + playerName + " --> Registrate ahora en http://bit.ly/2JJ78O1 para poder ver tus estadísticas.", player.id, 0x00FFB3, "normal", 0);
				}, 4000);
setTimeout(function(){
room.sendAnnouncement("🔶                                             ",player.id,0x73fac6,"bold",0)
room.sendAnnouncement("🔷                                                                          ",player.id,0x73fac6,"bold",0);
				}, 7000);
setTimeout(function(){
room.sendAnnouncement("qqqq",player.id,0x00ff92,"bold",0)
room.sendAnnouncement("qq",player.id,0xffffff,"bold",0);
				}, 10000);
setTimeout(function(){
room.sendAnnouncement("q",player.id,0x0f97ff,"bold",0)
room.sendAnnouncement("q",player.id,0xff770f,"bold",0);
room.sendAnnouncement("q",player.id,0x73fac6,"bold",0);
				}, 13000);
setTimeout(function(){
room.sendAnnouncement("                                [%] Con el comando !poss puedes ver la posesión del balón",player.id,0xff0f90,"bold",0);
				}, 16000);
setTimeout(function(){
room.sendAnnouncement("▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔",player.id,0x33fb9b,"bold",0);
				}, 16600);

setTimeout(function(){
room.sendAnnouncement("q",player.id,0xf2ff1a,"small-bold",0);
				}, 19000);
setTimeout(function(){
room.sendAnnouncement("q",player.id,0xf2ff1a,"small-bold",0);
				}, 20000);
setTimeout(function(){
room.sendAnnouncement("qqqqqqqq",player.id,0xf2ff1a,"small-bold",0);
				}, 21000);
setTimeout(function(){
room.sendAnnouncement("Solo se decir q",player.id,0x9efb33,"italic",0);
				}, 22000);
setTimeout(function(){
room.sendAnnouncement("que crack que es asdman",player.id,0x73fac6,"bold",0);
room.sendAnnouncement("digo.. q",player.id,0xffffff,"bold",0);
				}, 25000);
setTimeout(function(){
room.sendAnnouncement("@" + playerName + " Escribe !help, !adminhelp, !rankhelp para ver los comandos.", player.id, 0x00FFB3, "normal", 0);
				}, 28000);
    var players = room.getPlayerList();
    var adminNumber = 0;
    for (var i = 0; i < players.length; i++) {
        if (players[i].admin) {
            adminNumber++;
        }
    }
    if (adminNumber < 2) {
        room.setPlayerAdmin(players[1].id, true);
    }
}
function DeleteOyuncu(id) { for(var i = 0; i < voteKickList.length; i++) {if(voteKickList[i].id == id) {voteKickList.splice(i, 1);}}}
function CreateOyuncu(player) { voteKickList[voteKickList.length] = {isim:player.name,id:player.id,atilmaoyu:0,attigikisiler:[0]};}
room.onPlayerLeave = function(player) {
DeleteOyuncu(player.id);
connections = connections.filter(a => a[0] !== player.id);
    var players = room.getPlayerList();
    var adminNumber = 0;
    for (var i = 0; i < players.length; i++) {
        if (players[i].admin) {
            adminNumber++;
        }
    }
}
 
function isOutsideStadium(ballPosition) {if(ballPosition.y<-127 || ballPosition.y>127){return ballPosition.x > stadiumWidth || ballPosition.x < -stadiumWidth || ballPosition.y > stadiumHeight || ballPosition.y < -stadiumHeight;}}
 
var isBallOutsideStadium = false;
 
function checkBallPosition() {
    var ballPosition = room.getBallPosition();
   if(realMap==true){
    if(isOutsideStadium(ballPosition)) {
	  ballOut=true;
        if(!isBallOutsideStadium) {
            isBallOutsideStadium = true;
            exitingPos = ballPosition.x;
            exitingPos2 = ballPosition.y;
            var totalScores = room.getScores().red + room.getScores().blue;
            if(lastScores != totalScores) {
                lastScores = totalScores;
                return false;
            }
            if(ballPosition.x > stadiumWidth && lastTeamTouched == Team.RED || ballPosition.x < -stadiumWidth && lastTeamTouched == Team.BLUE) {
			
                lastCall = lastTeamTouched == Team.RED ? "2" : "1";				
				
				if(ballPosition.x<0 && ballPosition.y<0){BallPosition( -1200,-210,0,0)}
				if(ballPosition.x<0 && ballPosition.y>0){BallPosition( -1200,210,0,0)}
				if(ballPosition.x>0 && ballPosition.y>0){BallPosition(  1200,210,0,0)}
				if(ballPosition.x>0 && ballPosition.y<0){BallPosition(  1200,-210,0,0)}
				setBallColor(lastCall == 1 ? 0xFF0000:0x0000FF);
                room.sendAnnouncement("━━━━━━━━━━━━━━━━━━━━━━ 【⚽】sᴀǫᴜᴇ ᴅᴇ ᴀʀᴄᴏ ━━━━━━━━━━━━━", null, 0x00FF6E, "normal", 1);

				
				
            }
            else if(ballPosition.x > stadiumWidth && lastTeamTouched == Team.BLUE || ballPosition.x < -stadiumWidth && lastTeamTouched == Team.RED) {
               
                lastCall = lastTeamTouched == Team.RED ? "2" : "1";				
				
				if(ballPosition.x<0 && ballPosition.y<0){BallPosition(-1197,-615,0,0)}
				if(ballPosition.x<0 && ballPosition.y>0){BallPosition(-1197,615,0,0)}
				if(ballPosition.x>0 && ballPosition.y>0){BallPosition( 1197,615,0,0)}
				if(ballPosition.x>0 && ballPosition.y<0){BallPosition( 1197,-615,0,0)}
				setBallColor(lastCall == 1 ? 0xFF0000:0x0000FF);
                room.sendAnnouncement("━━━━━━━━━━━━━━━━━━━━━━ 【🚩】 ᴄᴏʀɴᴇʀ ━━━━━━━━━━━━━━━━", null, 0x00FF6E, "normal", 1);

            }
            else {
			
                isBallKickedOutside = false;
          room.sendAnnouncement(lastTeamTouched == Team.RED ? "          🔵 🔵 🔵           【𝐋𝐀𝐓】 ʟᴀᴛᴇʀᴀʟ ᴘᴀʀᴀ ᴇʟ 𝐁𝐋𝐔𝐄           🔵 🔵 🔵" : "          🔴 🔴 🔴           【𝐋𝐀𝐓】 ʟᴀᴛᴇʀᴀʟ ᴘᴀʀᴀ ᴇʟ 𝐑𝐄𝐃            🔴 🔴 🔴", null, 0xbbff45, 'normal', 2);
                lastCall = lastTeamTouched == Team.RED ? "2" : "1";
				setBallColor(lastCall == 1 ? 0xFF0000:0x0000FF);
			if(exitingPos2>0){BallPosition(exitingPos,exitingPos2+17.5,0,0);}	
			if(exitingPos2<0){BallPosition(exitingPos,exitingPos2-17.5,0,0);}

				
            }

        }
    }
    else {
	    if(ballOut==true){ setBallColor(0xFFFFFF);}
        isBallOutsideStadium = false;
        backMSG = true;
		ballOut=false;
		
    }
      return true;
	}
		
}

function BallPosition(a,b,c,d){
	for( let i=0; i<= room.getDiscCount(); i++){
		let disc = room.getDiscProperties(i);
		
		if(disc && disc.radius == 9.8){
			room.setDiscProperties(i, {x: a,y:b});
			room.setDiscProperties(i, {xspeed :c,yspeed:d});
		}
	}
}


function setBallColor(c){
	for( let i=0; i<= room.getDiscCount(); i++){
		let disc = room.getDiscProperties(i);
		
		if(disc && disc.radius == 9.8){
			room.setDiscProperties(i, {color: c});
			
		}
	}
}
realMap=false;
ballOut=true;
kirmiziTakim=[];
maviTakim=[];
redTeam  =[0,0,0,0,0,0];
blueTeam =[0,0,0,0,0,0];
redT=[];
blueT=[];


function isOutsideStadium2(ballPosition2) {if(ballPosition2.y<-83.5 || ballPosition2.y>83.5){return ballPosition2.x > 700 || ballPosition2.x < -700 || ballPosition2.y > 320 || ballPosition2.y < -320;}}
 
var isBallOutsideStadium2 = false;
 
function checkBallPosition2() {
	for( let i=0; i<= room.getDiscCount(); i++){
		let disc = room.getDiscProperties(i);
    var ballPosition2 = room.getBallPosition();
   if(realMap2==true){
    if(isOutsideStadium2(ballPosition2)) {
	  ballOut2=true;
        if(!isBallOutsideStadium2) {
            isBallOutsideStadium2 = true;
            exitingPos3 = ballPosition2.x;
            exitingPos4 = ballPosition2.y;
            var totalScores = room.getScores().red + room.getScores().blue;
            if(lastScores != totalScores) {
                lastScores = totalScores;
                return false;
            }
            if(ballPosition2.x > 700 && lastTeamTouched == Team.RED && disc.radius == 9.9 || ballPosition2.x < -700 && lastTeamTouched == Team.BLUE && disc.radius == 9.9) {
			
                lastCall2 = lastTeamTouched == Team.RED ? "2" : "1";				
				
				if(ballPosition2.x<0 && ballPosition2.y<0){BallPosition2( -750,-195,0,0)}
				if(ballPosition2.x<0 && ballPosition2.y>0){BallPosition2( -750,195,0,0)}
				if(ballPosition2.x>0 && ballPosition2.y>0){BallPosition2(  750,195,0,0)}
				if(ballPosition2.x>0 && ballPosition2.y<0){BallPosition2(  750,-195,0,0)}
				setBallColor2(lastCall2 == 1 ? 0xFF0000:0x0000FF);
                room.sendAnnouncement("[⚽] Sᴀǫᴜᴇ ᴅᴇ ᴀʀᴄᴏ", null, 0x00FF6E, "normal", 1);

				
				
            }
            else if(ballPosition2.x > 700 && lastTeamTouched == Team.BLUE && disc.radius == 9.9 || ballPosition2.x < -700 && lastTeamTouched == Team.RED && disc.radius == 9.9) {
               
                lastCall2 = lastTeamTouched == Team.RED ? "2" : "1";				
				
				if(ballPosition2.x<0 && ballPosition2.y<0){BallPosition2(-745,-330,0,0)}
				if(ballPosition2.x<0 && ballPosition2.y>0){BallPosition2(-745,330,0,0)}
				if(ballPosition2.x>0 && ballPosition2.y>0){BallPosition2( 745,330,0,0)}
				if(ballPosition2.x>0 && ballPosition2.y<0){BallPosition2( 745,-330,0,0)}
				setBallColor2(lastCall2 == 1 ? 0xFF0000:0x0000FF);
                room.sendAnnouncement("[🚩] ᴄᴏʀɴᴇʀ", null, 0x00FF6E, "normal", 1);

            }
        }
    }
    else {
	    if(ballOut2==true){ setBallColor2(0xFFDD00);}
        isBallOutsideStadium2 = false;
        backMSG = true;
		ballOut2=false;
		
    }
}
      return true;
	}
		
}

function BallPosition2(e,f,g,h){
	for( let i=0; i<= room.getDiscCount(); i++){
		let disc = room.getDiscProperties(i);
		
		if(disc && disc.radius == 9.9){
			room.setDiscProperties(i, {x: e,y:f});
			room.setDiscProperties(i, {xspeed :g,yspeed:h});
		}
	}
}


function setBallColor2(c){
	for( let i=0; i<= room.getDiscCount(); i++){
		let disc = room.getDiscProperties(i);
		
		if(disc && disc.radius == 9.9){
			room.setDiscProperties(i, {color: c});
			
		}
	}
}
realMap2=false;
ballOut2=true;
kirmiziTakim=[];
maviTakim=[];
redTeam  =[0,0,0,0,0,0];
blueTeam =[0,0,0,0,0,0];
redT=[];
blueT=[];
 
function getLastTouchTheBalltwo() {
    var ballPosition = room.getBallPosition();
    var players = room.getPlayerList();
    for(var i = 0; i < players.length; i++) {
        if(players[i].position != null) {
            var distanceToBall = pointDistance(players[i].position, ballPosition);
            if(distanceToBall < triggerDistance) {
                if(lastPlayerTouched!=players[i].name)
                {
                    if(lastTeamTouched==players[i].team)
                    {
                        assistingTouch = lastPlayerTouched;
                    }else assistingTouch = "";
                }
                lastTeamTouched = players[i].team;
                previousPlayerTouched == lastPlayerTouched;
                lastPlayerTouched = players[i].name;
            }
        }
    }
    return lastPlayerTouched;
}
function SuperAdminsTruchos(message)
{
    message = message.toLowerCase();
    message = message.replace(/\s/g, '');
    message = message.replace(/\./g,' ')
    if(message.includes("dameadmin") ||message.includes("medasadm") ||message.includes("denmeadmin") ||message.includes("medanadmin") ||message.includes("medasadm") ||message.includes("medanadm") ||message.includes("pasameadm") ||message.includes("pasenmeadm") ||message.includes("dameadm") ||message.includes("hacemeadmin") ||message.includes("haganmeadmin") ||message.includes("haganmeadm") ||message.includes("mepodriasdar") ||message.includes("mepodesdar"))
    {
        return true;
    }else return false;
}
function filter(message)
{
    message = message.toLowerCase();
    message = message.replace(/\s/g, '');
    message = message.replace(/\./g,' ')
    if(message.includes("ఌ") ||message.includes("甈") ||message.includes("㐷") ||message.includes("怅") ||message.includes("瘪") ||message.includes("⑸") ||message.includes("㬆") ||message.includes("権") ||message.includes("怜") ||message.includes("∯") ||message.includes("㤒") ||message.includes("䉊") ||message.includes("匊") ||message.includes("ᙻ") ||message.includes("ൽ") ||message.includes("ᴧ") ||message.includes("爂") ||message.includes("爇") ||message.includes("त") ||message.includes("権") ||message.includes("怜") ||message.includes("∯") ||message.includes("㤒") ||message.includes("vengan") ||message.includes("soccer") ||message.includes("PIPIPI") ||message.includes("creas") ||message.includes("creen") ||message.includes("TITITI") ||message.includes("h0st") ||message.includes("hosteo") ||message.includes("cre0") ||message.includes("眮") ||message.includes("㤮") ||message.includes("㵧") ||message.includes("creo") ||message.includes("host") ||message.includes("間") ||message.includes("謝") ||message.includes("奶") ||message.includes("如") ||message.includes("失") ||message.includes("好") ||message.includes("莖") ||message.includes("治") ||message.includes("帶") ||message.includes("陰") ||message.includes("play?c=") ||message.includes("cr30") ||message.includes("RScon") ||message.includes("creers") ||message.includes("creenrs") ||message.includes("ʟᴀᴛᴇʀᴀʟ") ||message.includes("ᴄᴏʀɴᴇʀ") ||message.includes("ᴀʀᴄᴏ") ||message.includes("creé") ||message.includes("r5") ||message.includes("r3") ||message.includes("reals") ||message.includes("s0") ||message.includes("rscon") ||message.includes("ccercon") ||message.includes("cc3rc0n") ||message.includes("rsc0n") ||message.includes("rrr") ||message.includes("sss") ||message.includes("apocalip") ||message.includes("cortoluz") ||message.includes("soycaca") ||message.includes("down") ||message.includes("mogolico") ||message.includes("sidoso") ||message.includes("sidosa") ||message.includes("mogolica") ||message.includes("mogolic") ||message.includes("cancerigen") ||message.includes("d0wn") ||message.includes("m0g0lic0") ||message.includes("m0golic") ||message.includes("mog0lic") ||message.includes("mogol1c") ||message.includes("﷽") ||message.includes("m0g0l1c") ||message.includes("﷽") ||message.includes("﷽") ||message.includes("﷽") ||message.includes("﷽") ||message.includes("﷽") ||message.includes("﷽") ||message.includes("﷽") ||message.includes("﷽") ||message.includes("﷽") ||message.includes("﷽") ||message.includes("autista") ||message.includes("mongolic") ||message.includes("cancer") ||message.includes("retrasad") ||message.includes("enfermomental") ||message.includes("enfermito") ||message.includes("aborto") ||message.includes("peruanosucio") ||message.includes("muertodehambre") ||message.includes("esclavo") ||message.includes("comepalomas") ||message.includes("veteatupais") ||message.includes("negroaborigen") ||message.includes("peruanosucio") ||message.includes("abandonenestassalas") ||message.includes("abandonenlasala") ||message.includes("glhcorrupcion") ||message.includes("http") ||message.includes("\u0061\u0064\u0066\u006f\u0063\u002e\u0075\u0073") ||message.includes("arsa") ||message.includes("ars4") ||message.includes("4rs4") ||message.includes("4rsa") ||message.includes("newton") ||message.includes("\u0074\u00ed\u0061") ||message.includes("\u0063\u0072\u0065\u00e9") ||message.includes("dovvn") ||message.includes("daun") ||message.includes("doun"))
    {
        return true;
    }else return false;
}
function penalespregunta(player, message)
{
    message = message.toLowerCase();
    message = message.replace(/\s/g, '');
    message = message.replace(/\./g,' ')
    if(message.includes("cuandohaypenales") ||message.includes("haypen") ||message.includes("haypenales?") ||message.includes("cuando") ||message.includes("cuando termina") ||message.includes("acuanto") ||message.includes("nohaypenales") ||message.includes("nohaypen") ||message.includes("acuant") ||message.includes("acuantos") ||message.includes("minutos") ||message.includes("minuto") ||message.includes("mins") ||message.includes("tiempo") ||message.includes("time") ||message.includes("limit") ||message.includes("nohay") ||message.includes("cuantos"))
    {
        room.sendAnnouncement('⏰ Eʟ ᴀʀʙɪᴛʀᴏ ᴀᴅɪᴄɪᴏɴᴀ ᴛɪᴇᴍᴘᴏ ᴇɴ ᴇʟ ᴍɪɴᴜᴛᴏ 5. ​', player.id, 0xFF3838, "normal", 1);
        room.sendAnnouncement('Uɴᴀ ᴠᴇᴢ ᴄᴜᴍᴘʟɪᴅᴏ, sɪ sɪɢᴜᴇ ᴘᴇʀsɪsᴛɪᴇɴᴅᴏ ᴇʟ ᴇᴍᴘᴀᴛᴇ, ʜᴀʙʀᴀ́ ᴘᴇɴᴀʟᴇs.', player.id, 0xFF3838, "normal", 0);
    var actualTimeAdded = Math.round((timeOutside-(100*0))/60);
    var MinutosTimeAdded = Math.round((actualTimeAdded-(100*0))/60);
    var TiempoTotal = Math.round(MinutosTimeAdded+5);
    if(actualTimeAdded<60&&actualTimeAdded>-1)
    {
    room.sendAnnouncement("⏰ 𝐓𝐄𝐑𝐌𝐈𝐍𝐀 𝐀 𝐋𝐎𝐒: 5 MINUTOS y  " + actualTimeAdded + " SEGUNDOS (𝐏𝐎𝐑 𝐀𝐇𝐎𝐑𝐀)", player.id, 0x00FF88, "normal", 1);
    }else if(actualTimeAdded<0)
    {
    room.sendAnnouncement("𝐓𝐄𝐑𝐌𝐈𝐍𝐀 𝐀 𝐋𝐎𝐒 𝟓 𝐌𝐈𝐍𝐔𝐓𝐎𝐒 (𝐏𝐎𝐑 𝐀𝐇𝐎𝐑𝐀)", player.id, 0x00FF88, "normal", 1);
    }else if(actualTimeAdded>60)
    {
    room.sendAnnouncement("⏰ 𝐓𝐄𝐑𝐌𝐈𝐍𝐀 𝐀 𝐋𝐎𝐒: " + TiempoTotal + " MINUTOS (𝐏𝐎𝐑 𝐀𝐇𝐎𝐑𝐀)", player.id, 0x00FF88, "normal", 1);
    }
}
}

function preguntatiempoagregado(player, message)
{
    message = message.toLowerCase();
    message = message.replace(/\s/g, '');
    message = message.replace(/\./g,' ')
    if(message.includes("cuantoagreg") ||message.includes("cuantoadicion") ||message.includes("cuantosminutosagreg") ||message.includes("cuantosminsagreg") ||message.includes("cuantosminsañadi") ||message.includes("cuantosañadi") ||message.includes("cuantoañadi") ||message.includes("cuantosminutosagreg"))
    {
    var actualTimeAdded = Math.round((timeOutside-(100*0))/60);
    var MinutosTimeAdded = Math.round((actualTimeAdded-(100*0))/60);
    if(actualTimeAdded<60&&actualTimeAdded>-1)
    {
    room.sendAnnouncement("⏰ 𝐓𝐈𝐄𝐌𝐏𝐎 𝐀𝐃𝐈𝐂𝐈𝐎𝐍𝐀𝐃𝐎: + " + actualTimeAdded + " SEGUNDOS (𝐏𝐎𝐑 𝐀𝐇𝐎𝐑𝐀)", player.id, 0xFF4400, "normal", 1);
    }else if(actualTimeAdded<0)
    {
    room.sendAnnouncement("𝐒𝐈𝐍 𝐓𝐈𝐄𝐌𝐏𝐎 𝐀𝐃𝐈𝐂𝐈𝐎𝐍𝐀𝐃𝐎. (+0) (𝐏𝐎𝐑 𝐀𝐇𝐎𝐑𝐀)", player.id, 0xFF4400, "normal", 1);
    }else if(actualTimeAdded>60)
    {
    room.sendAnnouncement("⏰ 𝐓𝐈𝐄𝐌𝐏𝐎 𝐀𝐃𝐈𝐂𝐈𝐎𝐍𝐀𝐃𝐎: + " + MinutosTimeAdded + " MINUTOS (𝐏𝐎𝐑 𝐀𝐇𝐎𝐑𝐀)", player.id, 0xFF4400, "normal", 1);
    }
}
}

function BaneandoGenteProhibidaFun(player)
{
    nicknameban = player.name
    nicknameban = nicknameban.toLowerCase();
    nicknameban = nicknameban.replace(/\s/g, '');
    nicknameban = nicknameban.replace(/\./g,' ')
    if(nicknameban.includes("realsoccercon") ||nicknameban.includes("detectorde") ||nicknameban.includes("admindown") ||nicknameban.includes("realsoccer") ||nicknameban.includes("r3al") ||nicknameban.includes("Áʀʙɪᴛʀᴏ ʙᴏᴛ") ||nicknameban.includes("rscon") ||nicknameban.includes("rbitro") ||nicknameban.includes("ʀʙɪᴛʀᴏʙᴏᴛ") ||nicknameban.includes("pipipi") ||nicknameban.includes("tititi") ||nicknameban.includes("ccc") ||nicknameban.includes("cacajr") ||nicknameban.includes("cacaj") ||nicknameban.includes("caca") ||nicknameban.includes("caquita") ||nicknameban.includes("caquita") ||nicknameban.includes("caqui") ||nicknameban.includes("cakit") ||nicknameban.includes("kakit") ||nicknameban.includes("kaquit") ||nicknameban.includes("kakajr") ||nicknameban.includes("kacajr") ||nicknameban.includes("kacajr") ||nicknameban.includes("kakitaj") ||nicknameban.includes("kakita") ||nicknameban.includes("kk") ||nicknameban.includes("desbann") ||nicknameban.includes("gordodesb") ||nicknameban.includes("desbanner") ||nicknameban.includes("nnerhack") ||nicknameban.includes("hack") ||nicknameban.includes("laexde") ||nicknameban.includes("jajaja") ||nicknameban.includes("mecojoatu") ||nicknameban.includes("banearme") ||nicknameban.includes("jaja") ||nicknameban.includes("puto") ||nicknameban.includes("lahermanade") ||nicknameban.includes("lamamade") ||nicknameban.includes("elpapade") ||nicknameban.includes("\u0063\u00e1\u0063\u0061\u006a\u0072") ||nicknameban.includes("\u006b\u00e1\u006b\u0061\u006a\u0072") ||nicknameban.includes("\u0063\u0061\u0063\u00e1\u006a\u0072") ||nicknameban.includes("\u006b\u0061\u006b\u00e1\u006a\u0072") ||nicknameban.includes("elhijode") ||nicknameban.includes("demierda") ||nicknameban.includes("mogolic") ||nicknameban.includes("baneame") ||nicknameban.includes("papade") ||nicknameban.includes("mamade") ||nicknameban.includes("hermanade") ||nicknameban.includes("\u0063\u00e1\u0063\u00e1") ||nicknameban.includes("criptonk") ||nicknameban.includes("jesusteama") ||nicknameban.includes("\u006a\u0065\u0073\u00fa\u0073\u0074\u0065\u0061\u006d\u0061") ||nicknameban.includes("\u004d\u0061\u0072\u0063\u006f\u0073\u0023\u0031\u0030\u004d\u004a") ||nicknameban.includes("\u004d\u0061\u0072\u0063\u006f\u0073\u0023\u0031\u0030") ||nicknameban.includes("puta") ||nicknameban.includes("pelotud") ||nicknameban.includes("down") ||nicknameban.includes("dawn") ||nicknameban.includes("quetepario") ||nicknameban.includes("laconchadetu") ||nicknameban.includes("\u006d\u006f\u0067\u00f3\u006c\u0069\u0063") ||nicknameban.includes("thescience") ||nicknameban.includes("anarchy") ||nicknameban.includes("scienceanarchy") ||nicknameban.includes("cienciaanarquia") ||nicknameban.includes("yhcranaeht") ||nicknameban.includes("aiuqrana") ||nicknameban.includes("\u0061\u006e\u0061\u0072\u0071\u0075\u00ed\u0061") ||nicknameban.includes("aicneic") ||nicknameban.includes("\u0061\u00ed\u0075\u0071\u0072\u0061\u006e\u0061") ||nicknameban.includes("shawnn") ||nicknameban.includes("shawn") ||nicknameban.includes("▇") ||nicknameban.includes("▆") ||nicknameban.includes(" ") ||nicknameban.includes("\ud83c\udfc1") ||nicknameban.includes("host") ||nicknameban.includes("arsa") ||nicknameban.includes("vengan") ||nicknameban.includes("newton") ||nicknameban.includes("4rsa") ||nicknameban.includes("ars4") ||nicknameban.includes("4rs4"))
    {
        room.kickPlayer(player.id,"𝙰𝙲𝙲𝙴𝚂𝙾 𝙳𝙴𝙽𝙴𝙶𝙰𝙳𝙾 🚫", true);
    }
}
function SaludandoGenteFun(player, message)
{
    message = message.toLowerCase();
    message = message.replace(/\s/g, '');
    message = message.replace(/\./g,' ')
    if(message.includes("HolaArbitro") ||message.includes("holabot") ||message.includes("holaarb") ||message.includes("hola🏁 Áʀʙɪᴛʀᴏ ʙᴏᴛ 🤖") ||message.includes("hola Áʀʙɪᴛʀᴏ") ||message.includes("hola bot") ||message.includes("holaárbitro"))
    {
    var myArray = ['Hola', 'Que tal!!', 'Buen dia!', 'Todo bien? Todo correcto? Y yo que me alegro', 'Saludas a un bot? Ndeah', 'Hello!', 'Hi!', 'Hola bro', 'Holis!!!'];
    var rand = myArray[(Math.random() * myArray.length) | 0]
    var myArray2 = ['😀','😁','😂','😃','😄','😅','😆','😉','😊','😋','😎','😍','😘','😏','😣','😥','😮','😯','😪','😫','😴','😌','😛','😜','😝'];
    var randimage = myArray2[(Math.random() * myArray2.length) | 0]
    var playerName = player.name.replace(/ /g,"_");
    room.sendChat((randimage + " " + rand + " @" + playerName ));
}
}
function pointDistance(p1, p2) {
    var d1 = p1.x - p2.x;
    var d2 = p1.y - p2.y;
    return Math.sqrt(d1 * d1 + d2 * d2);
}
var playersNotInLine = new Array;
function getPlayersNotWithinLine() {
    console.log("test");
    playersNotInLine = new Array;
    var players = room.getPlayerList();
        for (var i = 0; i < players.length; i++) {
            if (players[i].position != null) {
                if (players[i].team != lastTeamTouched && players[i].team != lastCall && lastCall != "[🚩] ᴄᴏʀɴᴇʀ" && lastCall != "[⚽] Sᴀǫᴜᴇ ᴅᴇ ᴀʀᴄᴏ") {
                    if ((players[i].position.y > greenLine || players[i].position.y < -greenLine) && pointDistance(room.getBallPosition(), players[i].position) < 500) {
                        playersNotInLine.push(players[i].name);
                    }
                }
 
            }
        }
}
function checkPlayersLine(player) {
 
    console.log("2");
    for(var i = 0; i < playersNotInLine.length; i++)
    {
    var found = false;
    for (var j = 0; j < lineCrossedPlayers.length; j++) {
                            if (lineCrossedPlayers[j].name == playersNotInLine[i]) {
                                lineCrossedPlayers[j].times = lineCrossedPlayers[j].times + 1;
                                room.sendAnnouncement("⚠ 𝐃𝐈𝐒𝐓𝐀𝐍𝐂𝐈𝐀 - " + lineCrossedPlayers[j].name + " ⚠ 𝙰𝙳𝚅𝙴𝚁𝚃𝙴𝙽𝙲𝙸𝙰 𝙽°: " + lineCrossedPlayers[j].times + " ⛔ ", player, 0xfcc21b, "normal", 1);
                                found = true;
                            }
 
                        }
                        if (!found) {
                            lineCrossedPlayers.push({
                                name: playersNotInLine[i],
                                times: 1,
                                punished: false
                            });
                            room.sendAnnouncement("⚠ 𝐃𝐈𝐒𝐓𝐀𝐍𝐂𝐈𝐀 - " + playersNotInLine[i] + " ⚠ 𝙰𝙳𝚅𝙴𝚁𝚃𝙴𝙽𝙲𝙸𝙰 𝙽°: 1  ⛔ ", player, 0xfcc21b, "normal", 1);
                        }
    }
 
}
var trigger = false;
var wrongThrowPosition = false;
function isBackRequired(player)
{
    var ballPosition = room.getBallPosition();
    if(!isBallKickedOutside)
    {
    if(lastCall=="1")
    {
        if((ballPosition.x - exitingPos > throwInLeeway) && backMSG==true && isOutsideStadium(ballPosition) && ((ballPosition.y - outLineY > 20) || (ballPosition.y - outLineY < -20)))
        {
            backMSG = false;
            room.sendAnnouncement("👈 ⚠ 𝚂𝙰𝚀𝚄𝙴 𝙼𝙰𝚂 𝙰𝚃𝚁𝙰𝚂 ⚠ ⬅⬅⬅", player, 0x66ffa0, "normal", 1);
            trigger = true;
            wrongThrowPosition = true;
        }
        if((ballPosition.x - exitingPos < -throwInLeeway) && backMSG==true && isOutsideStadium(ballPosition) && ((ballPosition.y - outLineY > 20) || (ballPosition.y - outLineY < -20)))
        {
            backMSG = false;
            room.sendAnnouncement("👉 ⚠ 𝚂𝙰𝚀𝚄𝙴 𝙼𝙰𝚂 𝙰𝙳𝙴𝙻𝙰𝙽𝚃𝙴 ⚠ ➡➡➡", player, 0x66ffa0, "normal", 1);
            trigger = true;
            wrongThrowPosition = true;
        }
    }
    if(lastCall=="2")
    {
        if((ballPosition.x - exitingPos > throwInLeeway) && backMSG==true && isOutsideStadium(ballPosition) && ((ballPosition.y - outLineY > 20) || (ballPosition.y - outLineY < -20)))
        {
            backMSG = false;
            room.sendAnnouncement("👈 ⚠ 𝚂𝙰𝚀𝚄𝙴 𝙼𝙰𝚂 𝙰𝙳𝙴𝙻𝙰𝙽𝚃𝙴 ⚠ ⬅⬅⬅", player, 0x66ffa0, "normal", 1);
            trigger = true;
            wrongThrowPosition = true;
        }
        if((ballPosition.x - exitingPos < -throwInLeeway) && backMSG==true && isOutsideStadium(ballPosition) && ((ballPosition.y - outLineY > 20) || (ballPosition.y - outLineY < -20)))
        {
            backMSG = false;
            room.sendAnnouncement("👉 ⚠ 𝚂𝙰𝚀𝚄𝙴 𝙼𝙰𝚂 𝙰𝚃𝚁𝙰𝚂 ⚠ ➡➡➡", player, 0x66ffa0, "normal", 1);
            trigger = true;
            wrongThrowPosition = true;
        }
    }
    }
    if(lastCall=="2" && trigger && isOutsideStadium && Math.abs(exitingPos - ballPosition.x)< throwInLeeway-20)
    {
        room.sendAnnouncement("AHÍ ESTÁ BIEN 👍", null, 0x1bff71, 'bold', 0);
        trigger = false;
        wrongThrowPosition = false;
        backMSG = true;
    }
    if(lastCall=="1" && trigger && isOutsideStadium && Math.abs(exitingPos - ballPosition.x)< throwInLeeway-20)
    {
        room.sendAnnouncement("AHÍ ESTÁ BIEN 👍", null, 0x1bff71, 'bold', 0);
        trigger = false;
        wrongThrowPosition = false;
        backMSG = true;
    }
 
 
 
}
function isThrowInCorrect(player)
{
    var ballPosition = room.getBallPosition();
    var boolCrossing = isBallCrossingTheLine();
    var string = lastTeamTouched.toString();
 
    if(boolCrossing && !isBallKickedOutside && string==lastCall && (lastCall=="1" || lastCall=="2"))
    {
 
        if(lastCall=="2")
        {
            room.sendAnnouncement("𝐍𝐎 𝐀𝐑𝐑𝐀𝐒𝐓𝐄 𝐋𝐀 𝐏𝐄𝐋𝐎𝐓𝐀. 𝐒𝐀𝐐𝐔𝐄 𝐁𝐈𝐄𝐍", player, 0x66ffa0, "normal", 1);
        }
        if(lastCall=="1")
        {
            room.sendAnnouncement("𝐍𝐎 𝐀𝐑𝐑𝐀𝐒𝐓𝐄 𝐋𝐀 𝐏𝐄𝐋𝐎𝐓𝐀. 𝐒𝐀𝐐𝐔𝐄 𝐁𝐈𝐄𝐍", player, 0x66ffa0, "normal", 1);
        }
 
        isBallKickedOutside == false;
    }else if(boolCrossing && string!=lastCall && (lastCall=="1" || lastCall=="2"))
    {
        //room.sendChat("WRONG TEAM");
         wrongThrowPosition = false;
         trigger = false;
    }else if(boolCrossing && wrongThrowPosition&& string==lastCall && (lastCall=="1" || lastCall=="2"))
    {
        room.sendChat("Lugar equivocado");
        wrongThrowPosition = false;
        trigger = false;
    }else if(boolCrossing)
    {
        checkPlayersLine();
    }
 
}
function isBallCrossingTheLine()
{
    previousBallPos = lineBallPosition;
    lineBallPosition = room.getBallPosition().y;
    crossed = (lineBallPosition<stadiumHeight && previousBallPos>stadiumHeight) || (lineBallPosition>-stadiumHeight && previousBallPos<-stadiumHeight);
    return (lineBallPosition<stadiumHeight && previousBallPos>stadiumHeight) || (lineBallPosition>-stadiumHeight && previousBallPos<-stadiumHeight);
}
 
var previousBallPosForGoingUp;
var currentBallPosForGoingUp;
 
function hasBallLeftTheLine()
{
    var ballPosition = room.getBallPosition();
    if(ballPosition.y<outLineY && isBallKickedOutside)
    {
    }else if (ballPosition.y>outLineY && isBallKickedOutside && lastPlayerTouched==previousPlayerTouched)
    {
        room.sendChat("MAL SACADO");
    }
 
}
var db = { p: { N: 13, kt: 2 }, log: [] }; function f(a, b, c) { for (var i = 0; i < a.length; i += 1) { if (a[i][b] === c) { return i; } } return -1; } function spammerosFilter(player, message) { if (player.id == 0) { return; } var ind = f(db.log, 'id', player.id); db.log[ind].lm.push({ ts: Date.now() }); if (db.log[ind].lm.length >= db.p.N) { db.log[ind].lm.splice(0, db.log[ind].lm.length - db.p.N); if (db.log[ind].lm.length / ((db.log[ind].lm[db.log[ind].lm.length - 1].ts - db.log[ind].lm[0].ts) / 4000) > db.p.kt) {
    if (player.admin == false){

 room.kickPlayer(player.id, "[👎] ❌ 🚫 𝐏𝐑𝐎𝐇𝐈𝐁𝐈𝐃𝐎 𝐒𝐏𝐀𝐌𝐌𝐄𝐑𝐎𝐒 🚫 ❌ ", true); } } } }

function onlyBotChangeStadium(byPlayer)
{
	if(byPlayer.name != "🏁 Áʀʙɪᴛʀᴏ ʙᴏᴛ 🤖" && byPlayer.id != 0)
	{
	realMap=true;
    room.setScoreLimit(0);
    room.setTimeLimit(0);
    room.setCustomStadium(RawRGLHMap);
            room.sendAnnouncement("[⛔] Sólo puedes elegir mapas con el comando: !mapas", null, 0xFFB82B, 'bold', 2);
	}
}

room.onStadiumChange = function(stadiumName, byPlayer) {
	onlyBotChangeStadium(byPlayer);
}
