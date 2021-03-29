---
title: Иажентчарактерекс Жеселпмодеон
description: Иажентчарактерекс Жеселпмодеон
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072f657ba5ac93d057474f062f73101f2559aed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258925"
---
# <a name="iagentcharacterexgethelpmodeon"></a><span data-ttu-id="64805-103">Иажентчарактерекс:: Жеселпмодеон</span><span class="sxs-lookup"><span data-stu-id="64805-103">IAgentCharacterEx::GetHelpModeOn</span></span>

<span data-ttu-id="64805-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="64805-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

<span data-ttu-id="64805-105">Возвращает значение, указывающее, включен ли контекстно-зависимый режим справки для символа.</span><span class="sxs-lookup"><span data-stu-id="64805-105">Retrieves whether context-sensitive Help mode is on for the character.</span></span>

-   <span data-ttu-id="64805-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="64805-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="64805-107"><span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*пбхелпмодеон*</span><span class="sxs-lookup"><span data-stu-id="64805-107"><span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*</span></span>
</dt> <dd>

<span data-ttu-id="64805-108">Адрес переменной, принимающей **значение true** , если режим справки включен для символа, и **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="64805-108">Address of a variable that receives **True** if Help mode is on for the character and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="64805-109">Если для этого свойства задано значение **true**, указатель мыши превращается в контекстно-зависимый рисунок справки при перемещении по символу или во всплывающем меню для символа.</span><span class="sxs-lookup"><span data-stu-id="64805-109">When this property is set to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="64805-110">Когда пользователь щелкает или перетаскивает символ или щелкает элемент во всплывающем меню символа, сервер запускает событие [**иажентнотифисинкекс:: хелпкомплете**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) и выходит из режима справки.</span><span class="sxs-lookup"><span data-stu-id="64805-110">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**IAgentNotifySinkEx::HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) event and exits Help mode.</span></span>

<span data-ttu-id="64805-111">В режиме справки сервер не отправляет события [**иажентнотифисинк:: Click**](iagentnotifysink--click.md), [**Иажентнотифисинк::D рагстарт**](iagentnotifysink--dragstart.md), [**Иажентнотифисинк::D Рагкомплете**](iagentnotifysink--dragcomplete.md)и [**иажентнотифисинк:: Command**](iagentnotifysink--command.md) , если только свойство [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) не возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="64805-111">In Help mode, the server does not send the [**IAgentNotifySink::Click**](iagentnotifysink--click.md), [**IAgentNotifySink::DragStart**](iagentnotifysink--dragstart.md), [**IAgentNotifySink::DragComplete**](iagentnotifysink--dragcomplete.md), and [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events, unless [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) property returns **True**.</span></span> <span data-ttu-id="64805-112">В этом случае сервер отправит событие **иажентнотифисинк:: Click** (не выходит из режима справки), но только для нажатия правой кнопки мыши, чтобы отобразить всплывающее меню.</span><span class="sxs-lookup"><span data-stu-id="64805-112">In that case, the server will send the **IAgentNotifySink::Click** event (does not exit Help mode), but only for the right mouse button to enable you to display the pop-up menu.</span></span>

<span data-ttu-id="64805-113">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="64805-113">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="64805-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="64805-114">See Also</span></span>

[<span data-ttu-id="64805-115">**Иажентчарактерекс:: Сеселпмодеон**</span><span class="sxs-lookup"><span data-stu-id="64805-115">**IAgentCharacterEx::SetHelpModeOn**</span></span>](iagentcharacterex--sethelpmodeon.md)


 

 




