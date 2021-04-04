---
title: Методы символьных объектов
description: Методы символьных объектов
ms.assetid: 0f926b7b-c1cf-4bd6-ba8c-1b2877eb1d24
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bb0dbb256c99660cbce1613c9fdd27d85a92dc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987375"
---
# <a name="character-object-methods"></a>Методы символьных объектов

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

Сервер также предоставляет методы для каждого символа в коллекции [**символов**](/windows/desktop/lwef/the-characters-object) . Поддерживаются следующие методы:

-   [**Вызова**](activate-method.md)
-   [**жестуреат**](gestureat-method.md)
-   [**Получить**](get-method.md)
-   [**Скрыть**](hide-method.md)
-   [**Прервать**](interrupt-method.md)
-   [**Прослушивание**](listen-method.md)
-   [**MoveTo**](moveto-method.md)
-   [**Воспроизведение**](play-method.md)
-   [**Казывающи**](show-method.md)
-   [**шовпопупмену**](showpopupmenu-method.md)
-   [**Speak**](speak-method.md)
-   [**Stop**](stop-method.md)
-   [**стопалл**](stopall-method.md)
-   [**Ситуацию**](think-method.md)
-   [**Ожидание**](wait-method.md)

Чтобы использовать метод, сослаться на символ в коллекции. В VBScript и Visual Basic это можно сделать, указав идентификатор символа:


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



Чтобы упростить синтаксис кода, можно определить переменную объекта и задать для нее ссылку на символьный объект в коллекции [**символов**](/windows/desktop/lwef/the-characters-object) . Затем можно использовать переменную для ссылки на методы или свойства символа. В следующем примере показано, как это можно сделать с помощью инструкции Visual Basic Set:


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



В Visual Basic 5,0 можно также создать ссылку, объявляя переменную как [**символьный**](/windows/desktop/lwef/the-characters-object)объект:


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



 

 