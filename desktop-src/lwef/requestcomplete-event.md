---
title: Событие Рекуесткомплете
description: Событие Рекуесткомплете
ms.assetid: 543b79d1-f09d-4061-a1a8-8c8ab496bceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 551aecdcfbeab76ab45e6211affef794ff37d876
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487716"
---
# <a name="requestcomplete-event"></a>Событие Рекуесткомплете

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Происходит, когда сервер завершает запрос в очереди.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Подагент * * * \_ рекуесткомплете* *  **(ByVal** *request * * *)**



| Отделение      | Описание                                            |
|-----------|--------------------------------------------------------|
| *Запрос* | Возвращает объект [**запроса**](/windows/desktop/lwef/the-request-object) . |



 

</dd> </dl>

### <a name="remarks"></a>Комментарии

Это событие возвращает объект [**запроса**](/windows/desktop/lwef/the-request-object) . Так как запросы обрабатываются асинхронно, можно использовать это событие, чтобы определить, когда сервер завершает обработку запроса (например, метод [**Get**](get-method.md), [**Play**](play-method.md)или [**говорите**](speak-method.md) ) для синхронизации этого события с другими действиями, создаваемыми приложением. Сервер отправляет событие только клиенту, который создал ссылку на объект **запроса** и только в том случае, если вы определили глобальную переменную для ссылки на запрос:


```
   Dim MyRequest 
   Dim Genie 

   Sub window_Onload
   
   Agent1.Characters.Load "Genie","https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent.Characters("Genie")

   ' This syntax will generate RequestStart and RequestComplete events.
   Set MyRequest = Genie.Get("state", "Showing")
   ' This syntax will not generate RequestStart and RequestComplete events.
   Genie.Get "state", "Hiding"
   
   End Sub

   Sub Agent1_RequestComplete(ByVal Request)

   If Request = MyRequest Then
      Status = "Showing animation is now loaded"

   End Sub
```



Поскольку объекты [**запроса**](/windows/desktop/lwef/the-request-object) анимации не назначаются до тех пор, пока сервер не обработает запрос, убедитесь, что объект **запроса** существует, прежде чем пытаться его оценить. Например, в Visual Basic, если вы используете условную проверку на предмет завершения определенного запроса, можно использовать ключевое слово **Nothing** :


```
   Sub Agent1_RequestComplete (ByVal Request)

   If Not (MyRequest Is Nothing) Then
      If Request = MyRequest Then
      '-- Do whatever
      End If
   End If

   End Sub
```



> [!Note]  
> В VBScript 1,0 это событие срабатывает, даже если не определены ссылки на объект [**запроса**](/windows/desktop/lwef/the-request-object) . Это было исправлено в VBScript 2,0, который можно скачать из <https://microsoft.com/msdownload/vbscript/scripting.asp> .

 

### <a name="see-also"></a>См. также:

[**Событие Рекуестстарт**](requeststart-event.md)


 

 