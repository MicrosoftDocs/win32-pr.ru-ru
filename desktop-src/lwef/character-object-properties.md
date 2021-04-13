---
title: Свойства объекта character
description: Свойства объекта character
ms.assetid: 86748de2-f5c8-4057-bfa4-79d46cac1e62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6212d6f0539b7fcb29faa883e6d88101952c12f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412787"
---
# <a name="character-object-properties"></a>Свойства объекта character

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

Объект [**character**](/windows/desktop/lwef/the-characters-object) предоставляет следующие свойства:

-   [**Активна**](active-property.md)
-   [**аутопопупмену**](autopopupmenu-property.md)
-   [**Описание**](description-property.md)
-   [**екстрадата**](extradata-property.md)
-   [**УСТРОЙСТВА**](guid-property.md)
-   [**хасосерклиентс**](hasotherclients-property.md)
-   [**Высота**](height-property.md)
-   [**хелпконтекстид**](helpcontextid-property-ch.md)
-   [**HelpFile**](helpfile-property.md)
-   [**хелпмодеон**](helpmodeon-property.md)
-   [**идлеон**](idleon-property.md)
-   [**LanguageID**](languageid-property.md)
-   [**Слева**](left-property.md)
-   [**мовекаусе**](movecause-property.md)
-   [**Имя**](name-property.md)
-   [**оригиналхеигхт**](originalheight-property.md)
-   [**оригиналвидс**](originalwidth-property.md)
-   [**Высота тона**](pitch-property.md)
-   [**саундеффектсон**](soundeffectson-property.md)
-   [**Speed**](speed-property.md)
-   [**срмодеид**](srmodeid-property.md)
-   [**срстатус**](srstatus-property.md)
-   [**Вверх**](top-property.md)
-   [**ттсмодеид**](ttsmodeid-property.md)
-   [**Версия**](version-property.md)
-   [**висибилитикаусе**](visibilitycause-property.md)
-   [**Visible**](visible-property-cob.md)
-   [**Ширина**](width-property-co.md)

Обратите внимание, что свойства [**высоты**](height-property.md), [**левой**](left-property.md), [**верхней**](top-property.md)и [**ширины**](width-property-co.md) символов отличаются от тех, которые могут поддерживаться средой программирования для размещения элемента управления. Свойства [**символов**](/windows/desktop/lwef/the-characters-object) применяются к видимой презентации символа, а не к расположению элемента управления Microsoft Agent.

Как и в случае с [**символьными**](/windows/desktop/lwef/the-characters-object) методами, можно получить доступ к свойствам символа с помощью коллекции [**символов**](/windows/desktop/lwef/the-characters-object) или упростить синтаксис, объявив переменную объекта и установив для нее символ в коллекции. В следующем примере для test1 и Test2 будет задано одно и то же значение:


```
   Dim Genie 
   Dim MyRequest
   
   Sub window_Onload

   Agent.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent.Characters("Genie")

   Genie.MoveTo 15,15
   Set MyRequest = Genie.Show()

   End Sub

   Sub Agent_RequestComplete(ByVal Request)

   If Request = MyRequest Then 
      Test1 = Agent.Characters("Genie").Top
      Test2 = Genie.Top
      MsgBox "Test 1 is " + cstr(Test1) + "and Test 2 is " + cstr(Test2)
   End If

   End Sub
```



Так как сервер загружает символ асинхронно, перед запросом его свойств убедитесь, что этот символ был загружен, например с помощью события [**рекуесткомплете**](requestcomplete-event.md) . В противном случае свойства могут возвращать неверные значения.

 

 