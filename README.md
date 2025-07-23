var room = HBInit({
  roomName: "Sala de prueba", // Nombre de la sala
  maxPlayers: 8,              // Máximo de jugadores
  public: true,               // Pública o privada
  noPlayer: true              // Permite que corra sin jugador anfitrión
});

room.setDefaultStadium("Big"); // Estadio por defecto
room.setScoreLimit(5);
room.setTimeLimit(3);

room.onPlayerJoin = function(player) {
  room.sendChat("¡Bienvenido " + player.name + "!");
};

room.onPlayerLeave = function(player) {
  room.sendChat(player.name + " ha salido de la sala.");
};
