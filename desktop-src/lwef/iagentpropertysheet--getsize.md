---
title: Иажентпропертишит
description: Иажентпропертишит
ms.assetid: 09bac150-ad68-40b2-9c2c-760f6bc919e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd5e185a6e8d55d87e561f727c8dc9df8a8cfd63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700574"
---
# <a name="iagentpropertysheetgetsize"></a><span data-ttu-id="2bc18-103">Иажентпропертишит:: DataSize</span><span class="sxs-lookup"><span data-stu-id="2bc18-103">IAgentPropertySheet::GetSize</span></span>

<span data-ttu-id="2bc18-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2bc18-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for property sheet width
   long * plHeight  // address of variable for property sheet height
);
```

<span data-ttu-id="2bc18-105">Возвращает размер окна страницы свойств агента Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="2bc18-105">Retrieves the size of the Microsoft Agent property sheet window.</span></span>

-   <span data-ttu-id="2bc18-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2bc18-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2bc18-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*плвидс*</span><span class="sxs-lookup"><span data-stu-id="2bc18-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="2bc18-108">Адрес переменной, получающей ширину страницы свойств в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="2bc18-108">Address of a variable that receives the width of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="2bc18-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*плхеигхт*</span><span class="sxs-lookup"><span data-stu-id="2bc18-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="2bc18-110">Адрес переменной, которая получает высоту страницы свойств в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="2bc18-110">Address of a variable that receives the height of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="2bc18-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="2bc18-111">See Also</span></span>

[<span data-ttu-id="2bc18-112">**Иажентпропертишит:: Disposition**</span><span class="sxs-lookup"><span data-stu-id="2bc18-112">**IAgentPropertySheet::GetPosition**</span></span>](iagentpropertysheet--getposition.md)


 

 




