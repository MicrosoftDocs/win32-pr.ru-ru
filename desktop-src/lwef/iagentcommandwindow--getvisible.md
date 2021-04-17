---
title: Иаженткоммандвиндов
description: Иаженткоммандвиндов
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66c6d7bf2ee59512f478fd8daa7cee882515690
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710055"
---
# <a name="iagentcommandwindowgetvisible"></a><span data-ttu-id="af06c-103">Иаженткоммандвиндов:: Visible</span><span class="sxs-lookup"><span data-stu-id="af06c-103">IAgentCommandWindow::GetVisible</span></span>

<span data-ttu-id="af06c-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="af06c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for Visible setting for 
);                   // Voice Commands Window
```

<span data-ttu-id="af06c-105">Определяет, является ли окно "Voice Commands" видимым или скрытым.</span><span class="sxs-lookup"><span data-stu-id="af06c-105">Determines whether the Voice Commands Window is visible or hidden.</span></span>

-   <span data-ttu-id="af06c-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="af06c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="af06c-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*пбвисибле*</span><span class="sxs-lookup"><span data-stu-id="af06c-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="af06c-108">Адрес переменной, которая получает **значение true** , если отображается окно "Voice Commands", или **значение false** , если оно скрыто.</span><span class="sxs-lookup"><span data-stu-id="af06c-108">Address of a variable that receives **True** if the Voice Commands Window is visible, or **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="af06c-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="af06c-109">See Also</span></span>

[<span data-ttu-id="af06c-110">**Иаженткоммандвиндов:: Сетвисибле**</span><span class="sxs-lookup"><span data-stu-id="af06c-110">**IAgentCommandWindow::SetVisible**</span></span>](iagentcommandwindow--setvisible.md)


 

 




