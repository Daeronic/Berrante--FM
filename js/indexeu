var lista = ["Guilherme e Santiago Jogado Na Rua.mp3", "Naiara Azevedo Part Maiara e Maraisa 50 Reais.mp3", "Alo_porteiro.mp3", "Henrique e Juliano Flor E O Beija Flor part Marilia Mendoca.mp3", "Maiara e Maraisa Medo Bobo.mp3", "Marilia Mendonca Infiel.mp3", "Simone e Simaria Meu Violao E O Nosso Cachorro.mp3", "Maiara e Maraisa 10 Por Cento.mp3", "Jorge e Mateus Louca de Saudade .mp3", "Henrique E Juliano Na Hora Da Raiva .mp3", "Luan Santana Eu Nao Merecia Isso.mp3"];
var i = 0;
var chamar = function () {
    $.getJSON("https://alotofnothing.000webhostapp.com/pl/musica/leitura.php", function (data) {
        var j = 0;
        $.each(data, function (val, name) {
            if (j > lista.length) {
                lista.push(name);
            }
            j++;
        });

    });
}
console.log(lista[1]);
$(".audio").attr("src", "https://alotofnothing.000webhostapp.com/pl/musica/Sertanojo/" + lista[i]);
$(".audio").load();
$(".nome").text(lista[i]);
function avancar() {


    i++;

    if (i >= lista.length) {
        i = 0;
        console.log("recomeçou")
    }
    $(".audio").attr("src", "https://alotofnothing.000webhostapp.com/pl/musica/Sertanojo/" + lista[i]);
    $(".audio")[0].load();
    $(".nome").text(lista[i]);
}
setInterval(() => {

    if ($(".audio")[0].currentTime >= $(".audio")[0].duration) {
        avancar();
    }
}
    , 500);
function pausar() {
    $(".audio")[0].pause();
}
function playmusic() {
    $(".audio")[0].play();
}
