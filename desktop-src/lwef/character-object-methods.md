---
title: Методы символьных объектов
description: Методы символьных объектов
ms.assetid: 0f926b7b-c1cf-4bd6-ba8c-1b2877eb1d24
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141c0fbcfe26e198984fd4a4d8c6c67858085e41178786d2cb78d2938231fdf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480318"
---
# <a name="character-object-methods"></a>Методы символьных объектов

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

Сервер также предоставляет методы для каждого символа в коллекции [**символов**](/windows/desktop/lwef/the-characters-object) . Поддерживаются следующие методы:

-   [**Активировать**](activate-method.md)
-   [**жестуреат**](gestureat-method.md)
-   [**Получить**](get-method.md)
-   [**Скрыть**](hide-method.md)
-   [**Прервать**](interrupt-method.md)
-   [**Прослушивание**](listen-method.md)
-   [**MoveTo**](moveto-method.md)
-   [**Воспроизведение**](play-method.md)
-   [**Показать**](show-method.md)
-   [**шовпопупмену**](showpopupmenu-method.md)
-   [**Speak**](speak-method.md)
-   [**Позиции**](stop-method.md)
-   [**стопалл**](stopall-method.md)
-   [**Ситуацию**](think-method.md)
-   [**Ожидание**](wait-method.md)

Чтобы использовать метод, сослаться на символ в коллекции. в VBScript и Visual Basic это можно сделать, указав идентификатор символа:


```
   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Display the character
   Agent1.Characters("Genie").Show
   Agent1.Characters("Genie").Play "Greet"
   Agent1.Characters("Genie").Speak "Hello. "

   End Sub
```



Чтобы упростить синтаксис кода, можно определить переменную объекта и задать для нее ссылку на символьный объект в коллекции [**символов**](/windows/desktop/lwef/the-characters-object) . Затем можно использовать переменную для ссылки на методы или свойства символа. в следующем примере показано, как это можно сделать с помощью инструкции Visual Basic Set:


```
   'Define a global object variable
   Dim Genie as Object

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", " Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   'Get the Restpose animation
   Genie.Get "animation", "RestPose"

   'Make the character say Hello
   Genie.Speak "Hello."

   End Sub
```



в Visual Basic 5,0 можно также создать ссылку, объявляя переменную как [**символьный**](/windows/desktop/lwef/the-characters-object)объект:


```
   Dim Genie as IAgentCtlCharacterEx

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   End Sub
```



Объявление объекта типа Иажентктлчарактерекс делает возможным раннее связывание объекта, что приводит к лучшей производительности.

В VBScript нельзя объявлять ссылку как конкретный тип. Однако можно просто объявить ссылку на переменную:


```
<SCRIPT LANGUAGE = "VBSCRIPT">
<!—--

   Dim Genie
   
   Sub window_OnLoad
   
   'Load the character
   AgentCtl.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   'Create an object reference to the character in the collection
   set Genie= AgentCtl.Characters ("Genie")

   'Get the Showing state animation
   Genie.Get "state", "Showing"

   'Display the character
   Genie.Show

   End Sub

-->
   </SCRIPT>
```



Некоторые языки программирования не поддерживают коллекции. Однако доступ к методам [**символьного**](/windows/desktop/lwef/the-characters-object) объекта можно получить с помощью [**символьного**](character-method.md) метода:


```
   agent.Characters.Character("CharacterID").method
```



Кроме того, можно создать ссылку на объект [**character**](/windows/desktop/lwef/the-characters-object) , чтобы упростить выполнение кода скрипта:


```
<SCRIPT LANGUAGE="JScript" FOR="window" EVENT="onLoad()">
<!--
   
   //Load the character's data
   AgentCtl.Characters.Load ("Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf");   

   //Create a reference to this object
   Genie = AgentCtl.Characters.Character("Genie");
   
   //Get the Showing state animation
   Genie.Get("state", "Showing");

   //Display the character
   Genie.Show();

-->
</SCRIPT>
```



 

 