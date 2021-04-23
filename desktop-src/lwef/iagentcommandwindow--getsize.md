---
title: Иаженткоммандвиндов
description: Иаженткоммандвиндов
ms.assetid: 24ad3b48-6557-4790-b9c4-2cf7df92fa7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cf42d98f811905590209b6fed70b28a5728903
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710099"
---
# <a name="iagentcommandwindowgetsize"></a><span data-ttu-id="306c3-103">Иаженткоммандвиндов:: DataSize</span><span class="sxs-lookup"><span data-stu-id="306c3-103">IAgentCommandWindow::GetSize</span></span>

<span data-ttu-id="306c3-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="306c3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for Voice Commands Window width
   long * plHeight  // address of variable for Voice Commands Window height
);
```

<span data-ttu-id="306c3-105">Получает текущий размер окна "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="306c3-105">Retrieves the current size of the Voice Commands Window.</span></span>

-   <span data-ttu-id="306c3-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="306c3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="306c3-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*плвидс*</span><span class="sxs-lookup"><span data-stu-id="306c3-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="306c3-108">Адрес переменной, получающей ширину окна "Voice Commands" (в пикселях) относительно начала экрана (сверху слева).</span><span class="sxs-lookup"><span data-stu-id="306c3-108">Address of a variable that receives the width of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="306c3-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*плхеигхт*</span><span class="sxs-lookup"><span data-stu-id="306c3-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="306c3-110">Адрес переменной, получающей высоту окна "Voice Commands" (в пикселях) относительно начала экрана (сверху слева).</span><span class="sxs-lookup"><span data-stu-id="306c3-110">Address of a variable that receives the height of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="306c3-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="306c3-111">See Also</span></span>

[<span data-ttu-id="306c3-112">**Иаженткоммандвиндов:: Disposition**</span><span class="sxs-lookup"><span data-stu-id="306c3-112">**IAgentCommandWindow::GetPosition**</span></span>](iagentcommandwindow--getposition.md)


 

 




