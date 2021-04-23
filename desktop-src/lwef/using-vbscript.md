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
# <a name="using-vbscript"></a><span data-ttu-id="bc1e4-103">Использование VBScript</span><span class="sxs-lookup"><span data-stu-id="bc1e4-103">Using VBScript</span></span>

<span data-ttu-id="bc1e4-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bc1e4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="bc1e4-105">VBScript — это язык программирования, входящий в состав Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="bc1e4-105">VBScript is a programming language included with Microsoft Internet Explorer.</span></span> <span data-ttu-id="bc1e4-106">Для других браузеров обратитесь к поставщику за поддержкой.</span><span class="sxs-lookup"><span data-stu-id="bc1e4-106">For other browsers, contact your vendor about support.</span></span> <span data-ttu-id="bc1e4-107">Для использования с агентом рекомендуется использовать VBScript 2,0 (или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="bc1e4-107">VBScript 2.0 (or later) is recommended for use with Agent.</span></span> <span data-ttu-id="bc1e4-108">Хотя более ранние версии VBScript могут работать с агентом, у них отсутствуют некоторые функции, которые можно использовать.</span><span class="sxs-lookup"><span data-stu-id="bc1e4-108">Although earlier versions of VBScript may work with Agent, they lack certain functions that you may want to use.</span></span> <span data-ttu-id="bc1e4-109">Можно загрузить VBScript 2,0 и получить дополнительные сведения о VBScript на сайте загрузки Майкрософт и на сайте Microsoft VBScript.</span><span class="sxs-lookup"><span data-stu-id="bc1e4-109">You can download VBScript 2.0 and obtain further information on VBScript at the Microsoft Downloads site and the Microsoft VBScript site.</span></span>

<span data-ttu-id="bc1e4-110">Чтобы программировать Microsoft Agent из VBScript, используйте HTML</span><span class="sxs-lookup"><span data-stu-id="bc1e4-110">To program Microsoft Agent from VBScript, use the HTML</span></span> <SCRIPT> <span data-ttu-id="bc1e4-111">tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:</span><span class="sxs-lookup"><span data-stu-id="bc1e4-111">tags. To access the programming interface, use the name of control you assign in the <OBJECT> tag, followed by the subobject (if any), the name of the method or property, and any parameters or values supported by the method or property:</span></span>

``` syntax
agent[.object].Method parameter, [parameter]
agent[.object].Property = value
```

<span data-ttu-id="bc1e4-112">Для событий включите имя элемента управления, за которым следует имя события и любые параметры:</span><span class="sxs-lookup"><span data-stu-id="bc1e4-112">For events, include the name of the control followed by the name of the event and any parameters:</span></span>

``` syntax
Sub agent_event (ByVal parameter[,ByVal parameter])
statements
End Sub
```

<span data-ttu-id="bc1e4-113">Можно также указать обработчик событий с помощью метода</span><span class="sxs-lookup"><span data-stu-id="bc1e4-113">You can also specify an event handler using the</span></span> <SCRIPT> <span data-ttu-id="bc1e4-114">tag's **For...Event** syntax:</span><span class="sxs-lookup"><span data-stu-id="bc1e4-114">tag's **For...Event** syntax:</span></span>

``` syntax
<SCRIPT LANGUAGE=VBScript For=agent Event=event[(parameter[,parameter])]>
statements
</SCRIPT>
```

<span data-ttu-id="bc1e4-115">Хотя Microsoft Internet Explorer поддерживает этот синтаксис, не все браузеры.</span><span class="sxs-lookup"><span data-stu-id="bc1e4-115">Although Microsoft Internet Explorer supports this latter syntax, not all browsers do.</span></span> <span data-ttu-id="bc1e4-116">Для обеспечения совместимости используйте только бывший синтаксис для событий.</span><span class="sxs-lookup"><span data-stu-id="bc1e4-116">For compatibility, use only the former syntax for events.</span></span>

<span data-ttu-id="bc1e4-117">При использовании VBScript (2,0 или более поздней версии) можно проверить, установлен ли агент Microsoft Agent, попытаться создать объект и проверить его существование.</span><span class="sxs-lookup"><span data-stu-id="bc1e4-117">With VBScript (2.0 or later), you can verify whether Microsoft Agent is installed by trying to create the object and checking to see if it exists.</span></span> <span data-ttu-id="bc1e4-118">В следующем примере показано, как проверить наличие элемента управления агента без запуска автоматической загрузки элемента управления (как это произойдет, если <OBJECT> на странице был включен тег для элемента управления):</span><span class="sxs-lookup"><span data-stu-id="bc1e4-118">The following sample demonstrates how to check for the Agent control without triggering an auto-download of the control (as would happen if you included an <OBJECT> tag for the control on the page):</span></span>

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

 

 




