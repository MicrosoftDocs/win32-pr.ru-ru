---
title: Иажентпропертишит
description: Иажентпропертишит
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff4dcac994901824d7dc37868d7fcfc3f39cefd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700575"
---
# <a name="iagentpropertysheetgetposition"></a><span data-ttu-id="c7641-103">Иажентпропертишит:: Disposition</span><span class="sxs-lookup"><span data-stu-id="c7641-103">IAgentPropertySheet::GetPosition</span></span>

<span data-ttu-id="c7641-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c7641-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of property sheet
   long * plTop    // address of variable for top edge of property sheet
);
```

<span data-ttu-id="c7641-105">Получает расположение окна страницы свойств агента Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c7641-105">Retrieves the Microsoft Agent's property sheet window position.</span></span>

-   <span data-ttu-id="c7641-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c7641-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c7641-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*пллефт*</span><span class="sxs-lookup"><span data-stu-id="c7641-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="c7641-108">Адрес переменной, которая получает координату экрана левого края страницы свойств в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="c7641-108">Address of a variable that receives the screen coordinate of the left edge of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="c7641-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*плтоп*</span><span class="sxs-lookup"><span data-stu-id="c7641-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="c7641-110">Адрес переменной, которая получает координату экрана верхнего края страницы свойств в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="c7641-110">Address of a variable that receives the screen coordinate of the top edge of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="c7641-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="c7641-111">See Also</span></span>

[<span data-ttu-id="c7641-112">**Иажентпропертишит:: DataSize**</span><span class="sxs-lookup"><span data-stu-id="c7641-112">**IAgentPropertySheet::GetSize**</span></span>](iagentpropertysheet--getsize.md)


 

 




