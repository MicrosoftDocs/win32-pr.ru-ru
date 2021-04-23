---
title: Иаженткоммандвиндов
description: Иаженткоммандвиндов
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8c036d02c210ecb26da5dfde207bfe56afe8a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986562"
---
# <a name="iagentcommandwindowgetposition"></a><span data-ttu-id="225e8-103">Иаженткоммандвиндов:: Disposition</span><span class="sxs-lookup"><span data-stu-id="225e8-103">IAgentCommandWindow::GetPosition</span></span>

<span data-ttu-id="225e8-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="225e8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of Voice Commands Window
   long * plTop    // address of variable for top edge of Voice Commands Window
);
```

<span data-ttu-id="225e8-105">Возвращает расположение окна "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="225e8-105">Retrieves the Voice Commands Window's position.</span></span>

-   <span data-ttu-id="225e8-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="225e8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="225e8-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*пллефт*</span><span class="sxs-lookup"><span data-stu-id="225e8-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="225e8-108">Адрес переменной, которая получает координату экрана левого края окна "Voice Commands" в пикселях относительно начала координат экрана (вверху слева).</span><span class="sxs-lookup"><span data-stu-id="225e8-108">Address of a variable that receives the screen coordinate of the left edge of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="225e8-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*плтоп*</span><span class="sxs-lookup"><span data-stu-id="225e8-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="225e8-110">Адрес переменной, которая получает координату экрана верхнего края окна "Voice Commands" в пикселях относительно начала координат экрана (вверху слева).</span><span class="sxs-lookup"><span data-stu-id="225e8-110">Address of a variable that receives the screen coordinate of the top edge of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="225e8-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="225e8-111">See Also</span></span>

[<span data-ttu-id="225e8-112">**Иаженткоммандвиндов:: DataSize**</span><span class="sxs-lookup"><span data-stu-id="225e8-112">**IAgentCommandWindow::GetSize**</span></span>](iagentcommandwindow--getsize.md)


 

 




