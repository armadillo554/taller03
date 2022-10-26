Nombre: Diego Navarro Cuevas

Estructura de las relaciones: (Clase1, clase2)= tipo de relacion(Clase1: multiplicidad / Clase2: multiplicidad)

Caso 1:
    Clases: Jugadores, partidos, goles 
    Relaciones: (Jugadores-partidos)= Asociacion bidireccional(Jugadores: * / partidos: *)
                (partidos♦-goles)= Agregacion (Partidos: *)
                (Jugadores♦-goles)= Agregacion (Jugador: *)
Caso 2:
    Clases:  empresaNaviera, buques, buquesDeBaja, partesBuquesDeBaja, astillero, comprarBuques, darDeBaja
    Relaciones: (empresaNaviera♦-buques)= Agregacion (empresaNaviera: 10..*)
                (empresaNaviera->comprarBuques)= Dependencia (empresaNaviera: 1..*)
                (empresaNaviera->darDeBaja)= Dependencia (empresaNaviera: 1..*)
                (buquesDeBaja♦-partesBuquesDeBaja)= Agregacion (buquesDeBaja: 1..*)

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