---
title: Иажентчарактерекс Сеселпмодеон
description: Иажентчарактерекс Сеселпмодеон
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674fc8dcca3bca2f44c0928474d8684e77fc6e9b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133731"
---
# <a name="iagentcharacterexsethelpmodeon"></a><span data-ttu-id="e3045-103">Иажентчарактерекс:: Сеселпмодеон</span><span class="sxs-lookup"><span data-stu-id="e3045-103">IAgentCharacterEx::SetHelpModeOn</span></span>

<span data-ttu-id="e3045-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e3045-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpModeOn(
   long bHelpModeOn  // help mode setting
);
```

<span data-ttu-id="e3045-105">Задает контекстно-зависимый режим справки для символа.</span><span class="sxs-lookup"><span data-stu-id="e3045-105">Sets context-sensitive Help mode on for the character.</span></span>

-   <span data-ttu-id="e3045-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e3045-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e3045-107"><span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*бхелпмодеон*</span><span class="sxs-lookup"><span data-stu-id="e3045-107"><span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*</span></span>
</dt> <dd>

<span data-ttu-id="e3045-108">Флаг режима справки.</span><span class="sxs-lookup"><span data-stu-id="e3045-108">Help mode flag.</span></span> <span data-ttu-id="e3045-109">Если этот параметр имеет **значение true**, Microsoft Agent включает режим справки для символа.</span><span class="sxs-lookup"><span data-stu-id="e3045-109">If this parameter is **True**, Microsoft Agent turns on Help mode for the character.</span></span>

</dd> </dl>

<span data-ttu-id="e3045-110">Если для этого свойства задано **значение true**, то при перемещении по символу или во всплывающем меню для символа указатель мыши превращается в контекстно-зависимый рисунок справки.</span><span class="sxs-lookup"><span data-stu-id="e3045-110">When you set this property to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="e3045-111">Когда пользователь щелкает или перетаскивает символ или щелкает элемент во всплывающем меню символа, сервер запускает событие [**иажентнотифисинкекс:: хелпкомплете**](iagentnotifysinkex--helpcomplete.md) и выходит из режима справки.</span><span class="sxs-lookup"><span data-stu-id="e3045-111">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md) event and exits Help mode.</span></span>

<span data-ttu-id="e3045-112">В режиме справки сервер не отправляет события [**Click**](click-event.md), [**драгстарт**](/windows/desktop/lwef/dragstart-event), [**драгкомплете**](https://www.bing.com/search?q=**DragComplete**)и [**Command**](command-event.md) , если свойство [**жетаутопопупмену**](iagentcharacterex--getautopopupmenu.md) не возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="e3045-112">In Help mode, the server does not send the [**Click**](click-event.md), [**DragStart**](/windows/desktop/lwef/dragstart-event), [**DragComplete**](https://www.bing.com/search?q=**DragComplete**), and [**Command**](command-event.md) events, unless the [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) property returns **True**.</span></span> <span data-ttu-id="e3045-113">В этом случае сервер будет отсылать событие **щелчка** (не выходя из режима справки), но только для правой кнопки мыши, чтобы можно было отобразить всплывающее меню.</span><span class="sxs-lookup"><span data-stu-id="e3045-113">In that case, the server will send the **Click** event (does not exit Help mode), but only for the right mouse button so you can display the pop-up menu.</span></span>

<span data-ttu-id="e3045-114">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="e3045-114">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3045-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="e3045-115">See Also</span></span>

<span data-ttu-id="e3045-116">[**Иажентчарактерекс:: жеселпмодеон**](iagentcharacterex--gethelpmodeon.md), [ **иажентнотифисинкекс:: хелпкомплете**](iagentnotifysinkex--helpcomplete.md)</span><span class="sxs-lookup"><span data-stu-id="e3045-116">[**IAgentCharacterEx::GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md)</span></span>


 

 