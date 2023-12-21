# Snake-Water-Gun-game_JS
The game should ask you to enter S, W or G. The computer should be able to randomly generate S, W or G and declare win or loss using alert, prompt and confirm where ever required!
let user = prompt('Enter S, W, or G: ');
let comp1 = Math.floor(Math.random() * 3);
let comp = ["S", "W", "G"][comp1];

const match = (comp, user) => {
  if (comp === user) {
    return "Tie";
  } else if (comp === "S" && user === "W") {
    return "comp";
  } else if (comp === "W" && user === "S") {
    return "user";
  } else if (comp === "G" && user === "W") {
    return "comp";
  } else if (comp === "W" && user === "G") {
    return "user";
  } else if (comp === "S" && user === "G") {
    return "comp";
  } else if (comp === "G" && user === "S") {
    return "user";
  }
};

let result = match(comp, user);
document.write(`Comp: ${comp} <br> User: ${user} <br> The winner is ${result}`);

