
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

        Alternador --> B:::positivo

        B(fa:fa-car-battery Bateria) --> fusebox --> M

        B --> |800w = 60a| Ab{Amplificador Sub}

        B --> |800w = 60a| Af

        B --> C

  
  

        %% Af ==> -

        %% Ab ==> -

        %% B ==> -

        %% Alternador --> -{Chassis}

  
  

        M{Multimidia} -.-> C{CrossOver}

  

        C-.->Af

        Af{Amplificador frente} -.-> FD{Frente esquerda}

  

        FD -.-> CFD{Crossover}

        CFD -.-> TweeterD[(Tweeter Direita)]:::Falante

        CFD -.-> PortaD[(Porta Direita)]:::Falante

        FD -.-> CFE{Crossover}

        CFE -.-> TweeterE[(Tweeter Esquerda)]:::Falante

        CFE -.-> PortaE[(Porta Esquerda)]:::Falante

        Af -.-> TE[(Porta traseira esquerda)]:::Falante

        Af -.-> TD[(Porta traseira direita)]:::Falante

  

        C -.-> Ab

        Ab -.-> S[(Subwoofer)]:::Falante
```

