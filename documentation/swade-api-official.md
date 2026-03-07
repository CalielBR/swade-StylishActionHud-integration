# Running Savage Worlds in Foundry VTT

If this is your first time using the Foundry Virtual Tabletop, please check out the official [Knowledge Base](https://foundryvtt.com/kb/) for the software; the Savage Worlds system builds on top of the base Foundry functionality, and this guide is focused on the system-specific details.

---

## 1. Playing the Game

### Rewarding Bennies
GMs can quickly reward Bennies from the Players List in the bottom left of the screen.
* To the right of each player listing is the number of Bennies they currently have. Clicking on this number increments the number of Bennies by one.
* Right-clicking on any player name displays a context menu with additional options:
    * **Give a Benny:** Gives the player a single benny as above.
    * **Refresh Bennies:** Resets the selected player’s characters’ Bennies to their Bennies Reset value as indicated in their character sheet.
    * **Refresh All Bennies:** Resets all player’s Bennies as above.

### Using Area Templates
The *Savage Worlds Adventure Edition* system for Foundry adds custom Cone, Blast and Stream Templates to the Measurement Controls toolbar.
* Icons include: Cone Template, Stream Template, Small, Medium, and Large Blast Templates.

### Vision
The system expands upon the base Foundry token vision handling with two additional detection modes:
* **See Heat:** Blocked by walls.
* **Sense Heat:** Not blocked by walls.
* These modes allow a token to see any token in range that does **not** have the **cold-bodied** status. This detection ignores both ordinary illumination and the native invisible condition. Tokens visible only through heat vision have a unique color filter overlaid.

---

## 2. Combat

### Damage
In order to resolve damage with a token, select the token you want to handle damage for and then click **Resolve Damage** on the chat card. 
This triggers the **Damage Applicator**, allowing adjustments before taking damage or attempting to soak. Note: It does not currently account for Ballistic Protection or specific vulnerabilities automatically; please adjust the final damage number accordingly.

### The Combat Tracker
The SWADE system modifies the Combat Tracker to align with Savage Worlds’ Action Card initiative:
* **Incapacitated:** Actors can be incapacitated without being removed from initiative (useful for bleeding out risks).
* **Hold:** Combatants can go on hold to delay their turn. Options include *Act Now* (to interrupt) or *Act After Current Combatant*.
* **Jokers:** If a Joker was drawn in the previous round, the deck is shuffled automatically. The +2 bonus to trait and damage rolls is applied automatically to the token.

### Grouping Combatants
You can group combatants by dragging them onto a "leader" in the combat tracker. This is ideal for extras. Only the leader is dealt an action card, and only the leader's initiative modifiers matter.

---

## 3. Items

Items are the components used to equip actors. They can be created in the Items Directory or directly on actor sheets.
* **Hindrances:** Includes a checkbox to indicate if it is a Major Hindrance.
* **Edges:** Fields for Requirements and a checkbox for Arcane Backgrounds.
* **Skills:** Configures the die type, modifiers, and linked attributes.
* **Weapons:** Damage should be written as dice expressions (e.g., `d6 + 1`). Use `@str + d4` to automatically include the character's Strength.
* **Powers:** Fields for Power Points, Range, Duration, and the specific Arcane Skill used for activation.

---

## 4. Pace

Pace is shown on the main tab under 'Derived Stats'. The system supports four movement types:
* **Ground** (defaults to 6), **Fly**, **Swim**, and **Burrow**.
* **Running Die:** Defaults to d6 and is shared across all Pace types. Click the die symbol next to the Pace box to roll for running.
* **Wounds:** By default, the system reduces Pace automatically when an actor receives wounds (configurable in settings).

---

## 5. Rolling Inline Roll Attributes

You can roll dice directly from the chat using `/r` or `/roll` with the following shortcuts:
* **Attributes:** `@str`, `@agi`, `@sma`, `@spi`, `@vig`.
* **Status:** `@wounds`, `@fatigue`.
* **Skills:** `@skill-slug` (Example: "Weird Science" becomes `@weird-science`).

---

## 6. Active Effects (AE)

Active Effects allow you to modify an Actor or Item on a temporary or permanent basis.
* **Change Modes:**
    1. *Add:* The most common mode (use negative numbers to subtract).
    2. *Multiply:* Used to multiply or divide.
    3. *Override:* Completely replaces a value.
    4. *Upgrade/Downgrade:* Sets floors or ceilings for values.
* **Affecting Items:** You can target specific items using the syntax:
  `@ItemType{Item Name or ID}[attribute key]`
  Example: `@Weapon{M-16}[system.ap]` to modify the armor piercing of a specific rifle.


# PT-BR

# Running Savage Worlds in Foundry VTT

Se esta é a sua primeira vez utilizando o Foundry Virtual Tabletop, consulte a [Base de Conhecimento oficial](https://foundryvtt.com/kb/) do software. O sistema Savage Worlds é construído sobre a funcionalidade base do Foundry, e este guia foca nos detalhes específicos do sistema.

---

## 1. Jogando (Playing the Game)

### Recompensando com Bennies
Mestres (GMs) podem recompensar Bennies rapidamente através da Lista de Jogadores no canto inferior esquerdo da tela.
* Ao lado de cada jogador, o número indica os Bennies atuais. Clique no número para aumentar o valor em um.
* Clique com o botão direito no nome de qualquer jogador para acessar:
    * **Give a Benny:** Dá um único Benny.
    * **Refresh Bennies:** Reseta os Bennies do personagem para o valor de reset definido na ficha.
    * **Refresh All Bennies:** Reseta os Bennies de todos os jogadores simultaneamente.

### Modelos de Área (Area Templates)
O sistema SWADE adiciona modelos customizados de Cone, Explosão (Blast) e Jato (Stream) na barra de ferramentas de Medição.
* Ícones disponíveis: Cone, Jato, Explosão Pequena, Média e Larga.

### Visão (Vision)
O sistema expande a visão nativa do Foundry com dois modos de detecção adicionais:
* **See Heat (Ver Calor):** Bloqueado por paredes.
* **Sense Heat (Sentir Calor):** Não é bloqueado por paredes.
* Ambos os modos ignoram iluminação comum e a condição de invisibilidade nativa. Tokens visíveis apenas por visão térmica recebem um filtro de cor exclusivo.

---

## 2. Combate

### Dano (Damage)
Para resolver o dano, selecione o token alvo e clique em **Resolve Damage** no card de chat. Isso abrirá o **Damage Applicator**, que permite ajustes (como absorção ou modificadores manuais) antes da aplicação final. 
*Nota: Atualmente, o sistema não calcula automaticamente Proteção Balística ou vulnerabilidades específicas; ajuste o número final conforme necessário.*

### O Combat Tracker
O SWADE modifica o rastreador de combate para alinhar com as regras de iniciativa de cartas:
* **Exibição:** O valor numérico de iniciativa é substituído pelo naipe e valor da Carta de Ação.
* **Incapacitado:** Atores podem ser marcados como incapacitados sem serem removidos da iniciativa (útil para regras de sangramento).
* **Esperar (Hold):** Permite que combatentes atrasem seu turno ou interrompam outros.
* **Coringas (Jokers):** Se um Coringa for sacado, o deck é embaralhado na rodada seguinte e o bônus de +2 em rolagens de característica e dano é aplicado automaticamente.

### Agrupando Combatentes
Você pode agrupar combatentes arrastando-os sobre um "líder" no rastreador. Apenas o líder recebe uma carta de ação, facilitando a gestão de Extras e aliados.

---

## 3. Itens

Itens são componentes para criar e equipar atores. Podem ser criados no diretório de itens ou diretamente na ficha.
* **Hindrances (Complicações):** Define se é Maior ou Menor.
* **Edges (Vantagens):** Requisitos de Rank, Atributos ou outras Vantagens.
* **Skills (Perícias):** Configura o tipo de dado, modificadores permanentes e atributo vinculado.
* **Gear (Equipamento):** Peso, custo e quantidade.
* **Weapons (Armas):** Suporta expressões como `d6 + 1` ou `@str + d4` para incluir a força do personagem.

---

## 4. Movimentação (Pace)

O sistema permite configurar quatro tipos de movimentação: **Ground** (Chão), **Fly** (Voo), **Swim** (Natação) e **Burrow** (Escavação).
* **Running Die (Dado de Corrida):** Padrão d6, compartilhado entre todos os tipos de Pace.
* **Wounds (Ferimentos):** Por padrão, ferimentos reduzem o Pace automaticamente (configurável nas opções do sistema).

---

## 5. Rolagens Diretas (Inline Roll Attributes)

Você pode rolar dados diretamente do chat usando `/r` ou `/roll` com os seguintes atalhos:
* **Atributos:** `@str`, `@agi`, `@sma`, `@spi`, `@vig`.
* **Status:** `@wounds`, `@fatigue`.
* **Perícias:** `@skill-slug` (Exemplo: "Atirar" vira `@shooting`).

---

## 6. Efeitos Ativos (Active Effects)

Active Effects (AE) permitem modificar um Ator de forma temporária ou permanente.
* **Modos de Mudança:**
    * *Add:* Soma valores (ou subtrai se negativo).
    * *Multiply:* Multiplica ou divide.
    * *Override:* Substitui o valor original.
    * *Upgrade/Downgrade:* Define valores mínimos ou máximos.
* **Efeitos em Itens:** Você pode afetar outros itens usando a sintaxe `@ItemType{Nome do Item}[chave]`. 
    * Exemplo: `@Weapon{M-16}[system.ap]` para aumentar a perfuração de armadura de uma arma específica.