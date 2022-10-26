Nombre: Diego Navarro Cuevas

Estructura de las relaciones: (Clase1, clase2)= tipo de relacion(Clase1: multiplicidad / Clase2: multiplicidad)

NOTA IMPORTANTE: el merge a la rama Master lo hice a una hora que no corresponde ya que en el momento se me olvido, por lo que lo hice apenas me di cuenta
de mi error, disculpen las molestias

Caso 1:
    Clases: Jugador, partido, gol
    Relaciones: (Jugador-partido)= Asociacion bidireccional(Jugador: 0..* / partido: 0..*)
                (partido♦-gol)= Agregacion (Partido: 0..*)
                (Jugador♦-gol)= Agregacion (Jugador: 0..*)
Caso 2:
    Clases:  empresaNaviera, buques, buquesDeBaja, partesBuquesDeBaja, astillero, 
    Relaciones: (empresaNaviera♦-buques)= Composicion (empresaNaviera: 1..*)
                (buquesDeBaja♦-partesBuquesDeBaja)= Agregacion (buquesDeBaja: 0..*)
                (astillero♦-partesBuquesDeBaja)= Agregacion (astillero: 0..*) 

Caso 3:
    Clases: pedido, mesero
    Relaciones: (pedido-mesero)= Asociacion bidireccional (pedido: 1 / mesero: 0..*)

Caso 4:
    Clases: equipo, jugador, capitan
    Relaciones: (equipo♦-jugador)= Composicion (equipo: 1..* / jugador: 1)
                (equipo-capitan)= Asociacion bidireccional (equipo: 1 / capitan: 1)

Caso 5:
    Clases: evento
    Relaciones: (evento->evento)= Dependencia (evento: 0..*)  
