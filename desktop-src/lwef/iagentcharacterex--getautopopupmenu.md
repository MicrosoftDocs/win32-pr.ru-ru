---
title: Иажентчарактерекс Жетаутопопупмену
description: Иажентчарактерекс Жетаутопопупмену
ms.assetid: c29bfd6e-c7eb-426e-be38-2fa0bdb13211
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c7a3b8d1075c596f27af17df34c7cb94d8a1ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986678"
---
# <a name="iagentcharacterexgetautopopupmenu"></a><span data-ttu-id="383ee-103">Иажентчарактерекс:: Жетаутопопупмену</span><span class="sxs-lookup"><span data-stu-id="383ee-103">IAgentCharacterEx::GetAutoPopupMenu</span></span>

<span data-ttu-id="383ee-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="383ee-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAutoPopupMenu(
   long * pbAutoPopupMenu  // address of auto pop-up menu display setting
);
```

<span data-ttu-id="383ee-105">Определяет, будет ли сервер автоматически отображать всплывающее меню символа.</span><span class="sxs-lookup"><span data-stu-id="383ee-105">Retrieves whether the server automatically displays the character's pop-up menu.</span></span>

-   <span data-ttu-id="383ee-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="383ee-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="383ee-107"><span id="pbAutoPopupMenu"></span><span id="pbautopopupmenu"></span><span id="PBAUTOPOPUPMENU"></span>*пбаутопопупмену*</span><span class="sxs-lookup"><span data-stu-id="383ee-107"><span id="pbAutoPopupMenu"></span><span id="pbautopopupmenu"></span><span id="PBAUTOPOPUPMENU"></span>*pbAutoPopupMenu*</span></span>
</dt> <dd>

<span data-ttu-id="383ee-108">Адрес переменной, принимающей **значение true** , если сервер Microsoft Agent автоматически обрабатывает отображение всплывающего меню символа и **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="383ee-108">Address of a variable that receives **True** if the Microsoft Agent server automatically handles displaying the character's pop-up menu and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="383ee-109">Если для этого свойства задано значение **false**, приложение должно отобразить всплывающее меню с помощью метода [**Иажентчарактерекс:: шовпопупмену**](iagentcharacterex--showpopupmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="383ee-109">When this property is set to **False**, your application must display the pop-up menu using [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) method.</span></span>

<span data-ttu-id="383ee-110">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="383ee-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="383ee-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="383ee-111">See Also</span></span>

<span data-ttu-id="383ee-112">[**Иажентчарактерекс:: сетаутопопупмену**](iagentcharacterex--setautopopupmenu.md), [ **иажентчарактерекс:: шовпопупмену**](iagentcharacterex--showpopupmenu.md)</span><span class="sxs-lookup"><span data-stu-id="383ee-112">[**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md), [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span></span>


 

 




