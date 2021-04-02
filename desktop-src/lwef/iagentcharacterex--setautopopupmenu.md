---
title: Иажентчарактерекс Сетаутопопупмену
description: Иажентчарактерекс Сетаутопопупмену
ms.assetid: f2402b1f-a39b-4fd5-a046-c0a3245d2af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcfd1bd7ea0b02f226ed6f0365b466577807a193
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986534"
---
# <a name="iagentcharacterexsetautopopupmenu"></a><span data-ttu-id="045e5-103">Иажентчарактерекс:: Сетаутопопупмену</span><span class="sxs-lookup"><span data-stu-id="045e5-103">IAgentCharacterEx::SetAutoPopupMenu</span></span>

<span data-ttu-id="045e5-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="045e5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetAutoPopupMenu(
   long bAutoPopupMenu,  // auto pop-up menu display setting
);
```

<span data-ttu-id="045e5-105">Указывает, будет ли сервер автоматически отображать всплывающее меню символа.</span><span class="sxs-lookup"><span data-stu-id="045e5-105">Sets whether the server automatically displays the character's pop-up menu.</span></span>

-   <span data-ttu-id="045e5-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="045e5-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="045e5-107"><span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*баутопопупмену*</span><span class="sxs-lookup"><span data-stu-id="045e5-107"><span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*</span></span>
</dt> <dd>

<span data-ttu-id="045e5-108">Автоматически отображаемый флаг отображения всплывающего меню.</span><span class="sxs-lookup"><span data-stu-id="045e5-108">The automatic pop-up menu display flag.</span></span> <span data-ttu-id="045e5-109">Если этот параметр имеет **значение true**, Microsoft Agent автоматически отображает всплывающее меню символа, когда пользователь щелкает правой кнопкой мыши значок символа или символа на панели задач.</span><span class="sxs-lookup"><span data-stu-id="045e5-109">If this parameter is **True**, Microsoft Agent automatically displays the character's pop-up menu when the user right-clicks the character or character's taskbar icon.</span></span>

</dd> </dl>

<span data-ttu-id="045e5-110">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="045e5-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="045e5-111">Если задать для этого свойства **значение false**, можно создать собственное поведение при обработке меню.</span><span class="sxs-lookup"><span data-stu-id="045e5-111">By setting this property to **False**, you can create your own menu-handling behavior.</span></span> <span data-ttu-id="045e5-112">Чтобы отобразить меню после присвоения этому свойству значения **false**, используйте метод [**Иажентчарактерекс:: шовпопупмену**](iagentcharacterex--showpopupmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="045e5-112">To display the menu after setting this property to **False**, use the [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="045e5-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="045e5-113">See Also</span></span>

<span data-ttu-id="045e5-114">[**Иажентчарактерекс:: жетаутопопупмену**](iagentcharacterex--getautopopupmenu.md), [ **иажентчарактерекс:: шовпопупмену**](iagentcharacterex--showpopupmenu.md)</span><span class="sxs-lookup"><span data-stu-id="045e5-114">[**IAgentCharacterEx::GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span></span>


 

 




