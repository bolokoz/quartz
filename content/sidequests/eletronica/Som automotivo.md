
# Objetivo e componentes

Qualidade e facilidade de remoção (e budget)
- Subwoofer de 12" porque eu tinha um de 8" e não trazia _aquele_ sentimento (R$800)
- Componente de qualidade  (R$600)
- 6x9 nas portas trazeiras (R$300)
- 1 amp 800w 4ch pra frente (R$400) 
- 1 amp pro sub (R$400)
- Caixa de sub (R$300)
- 1 equalizador (dsp) pra testar se vale a pena (R$300)
- Fiação, fuseis, blocos e mão de obra (R$500)

Estourei, achei que com R$2000 dava

# Esquema

```mermaid
flowchart TB

  

        classDef positivo stroke:#f00

        classDef negativo fill:#f96

        classDef Falante fill:#f96

        classDef pos stroke:red

  

        linkStyle default stroke:red

        %% Alternador --> B:::positivo

        B(fa:fa-car-battery Bateria)

        B --> Bloco

        Bloco -----------> |800w = 60a - 5 metros - 4guage - 70 ampere| Ab{Amplificador Sub}

        Bloco --> |800w = 60a| Af

        Bloco --> C

        C-.->Af

  

        %% Af ==> -

        %% Ab ==> -

        %% B ==> -

        %% Alternador --> -{Chassis}

  
  
  
  
  

  
  

        C -.-> Ab

        Ab -.-> S[(Subwoofer)]:::Falante

  
  

        M{Multimidia} -.-> C{CrossOver}

  

        Af{Amplificador frente}

        Af -.......-> TE[(Porta traseira esquerda)]:::Falante

        CFD

        Af -..-> CFD

        Af -.-> CFE

        %% FD -.->

        CFD{Crossover D}

        CFD -.-> TweeterD[(Tweeter Direita)]:::Falante

        CFD -.-> PortaD[(Porta Direita)]:::Falante

        %% FD -.->

        CFE{Crossover E}

        CFE -.-> TweeterE[(Tweeter Esquerda)]:::Falante

        CFE -.-> PortaE[(Porta Esquerda)]:::Falante

  

        Af -......-> TD[(Porta traseira direita)]:::Falante
```

