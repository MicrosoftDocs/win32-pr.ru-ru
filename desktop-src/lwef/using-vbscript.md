---
title: Использование VBScript
description: Использование VBScript
ms.assetid: a078eb60-aa12-42ea-850c-7b845fc8037c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691ed6bf520c83e4b679bb174274abb984eaa2f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258543"
---
# <a name="using-vbscript"></a>Использование VBScript

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

VBScript — это язык программирования, входящий в состав Microsoft Internet Explorer. Для других браузеров обратитесь к поставщику за поддержкой. Для использования с агентом рекомендуется использовать VBScript 2,0 (или более поздней версии). Хотя более ранние версии VBScript могут работать с агентом, у них отсутствуют некоторые функции, которые можно использовать. Можно загрузить VBScript 2,0 и получить дополнительные сведения о VBScript на сайте загрузки Майкрософт и на сайте Microsoft VBScript.

Чтобы программировать Microsoft Agent из VBScript, используйте HTML <SCRIPT> tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

Для событий включите имя элемента управления, за которым следует имя события и любые параметры:

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

Можно также указать обработчик событий с помощью метода <SCRIPT> tag's **For...Event** syntax:

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

Хотя Microsoft Internet Explorer поддерживает этот синтаксис, не все браузеры. Для обеспечения совместимости используйте только бывший синтаксис для событий.

При использовании VBScript (2,0 или более поздней версии) можно проверить, установлен ли агент Microsoft Agent, попытаться создать объект и проверить его существование. В следующем примере показано, как проверить наличие элемента управления агента без запуска автоматической загрузки элемента управления (как это произойдет, если <OBJECT> на странице был включен тег для элемента управления):

``` syntax
<!-- WARNING - This code requires VBScript 2.0.
It will always fail to detect the Agent control
in VbScript 1.x, because CreateObject doesn't work.
-->

<SCRIPT LANGUAGE=VBSCRIPT>
If HaveAgent() Then
      'Microsoft Agent control was found.
document.write "<H2 align=center>Found</H2>"
Else
      'Microsoft Agent control was not found.
document.write "<H2 align=center>Not Found</H2>"
End If

Function HaveAgent()
' This procedure attempts to create an Agent Control object.
' If it succeeds, it returns True.
'    This means the control is available on the client.
' If it fails, it returns False.
'    This means the control hasn't been installed on the client.

   Dim agent
   HaveAgent = False
   On Error Resume Next
   Set agent = CreateObject("Agent.Control.1")
   HaveAgent = IsObject(agent)

End Function

</SCRIPT>
```

 

 




