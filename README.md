# Team-Stats
Codecademy project on extracting and adding information to sports teams.

const team = {
  _players: [
    {firstName: 'Master', lastName: 'Chief', age: 40},
    {firstName: 'Ezio', lastName: 'Auditore', age: 22},
    {firstName: 'Marcus', lastName: 'Fenix', age: 36}],

  _games: [
    {opponent: 'The Covenant', teamPoints: 62, opponentPoints: 38}, 
    {opponent: 'The Templar Order', teamPoints: 52, opponentPoints: 28}, 
    {opponent: 'Locust Horde', teamPoints: 48, opponentPoints: 40}],

  get players() {
    return this._players;
  },
  get games() {
    return this._games;
  },
  addPlayer(firstName, lastName, age) {
    const player = {
      firstName: firstName,
      lastName: lastName,
      age: age
    };
    return this.players.push(player);
  },
  addGame(opponent, teamPoints, opponentPoints) {
    const game = {
      opponent: opponent,
      teamPoints: teamPoints,
      opponentPoints: opponentPoints
    };
    return this.games.push(game);
  }
};

team.addPlayer('Steph', 'Curry', 28);
team.addPlayer('Lisa', 'Leslie', 44);
team.addPlayer('Bugs', 'Bunny', 76);
//console.log(team.players);
team.addGame('DumDums', 74, 18);
team.addGame('Chuck Norris', 38, 1000000);
team.addGame('Globo Gym', 54, 12);
console.log(team.games);
