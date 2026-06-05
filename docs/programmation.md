---
layout: default
nav_order: 3
title: Programation
---

# Programmation

## Contexte du programme

Pour la partie arduino, notre objectif était de faire aller le robot le plus vite possible pour marquer un maximum de points sur les courses. Nous avons trouvé une esquisse de programme sur GitHub puis nous l'avons ensuite modifié pour l'intégrer à notre robot. L'avancée de notre robot est basée sur la rotation synchronisée des jambes et des pieds. Cela donne donc une impression de glissement sur le sol, nous avons eu beaucoup de difficultés au niveau des déplacements. Notre robot dévie quand il avance, même si nous rajoutons des offsets, il ne veut pas marchait tout droit. Si c'est le cas pour votre robot aussi, n'hésitez pas à changer les servomoteurs ! ou à développer des fonctions de rotation efficaces ! 

## Programme

Nous allons vous montrer ici les parties du programme qui nous ont permis de rendre notre robot opérationnel

### Fonction marche avant

void marcheAvant() {

  static int angle = 0;

  int amplitude = 20;

  float rad = angle * PI / 180.0;

  int jd = 90 + offsetJD - amplitude * sin(rad) - correction;
  int jg = 90 + offsetJG + amplitude * sin(rad);

  int pd = 90 + offsetPD + 6 * sin(rad + PI/2);
  int pg = 90 + offsetPG - 12* sin(rad + PI/2);

  jambeDroite.write(jd);
  jambeGauche.write(jg);

  piedDroit.write(pd);
  piedGauche.write(pg);

  angle += 10;

  if (angle >= 360) {
    angle = 0;
  }

  delay(15);
}



