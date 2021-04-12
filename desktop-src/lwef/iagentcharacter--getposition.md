---
title: Иажентчарактер
description: Иажентчарактер
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cdff0d6876fc7257e05014f3d9ba695db5d168
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332760"
---
# <a name="iagentcharactergetposition"></a><span data-ttu-id="23b47-103">Иажентчарактер:: Disposition</span><span class="sxs-lookup"><span data-stu-id="23b47-103">IAgentCharacter::GetPosition</span></span>

<span data-ttu-id="23b47-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="23b47-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

<span data-ttu-id="23b47-105">Возвращает расположение кадра анимации символа.</span><span class="sxs-lookup"><span data-stu-id="23b47-105">Retrieves the character's animation frame position.</span></span>

-   <span data-ttu-id="23b47-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="23b47-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="23b47-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*пллефт*</span><span class="sxs-lookup"><span data-stu-id="23b47-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="23b47-108">Адрес переменной, получающей экранную координату левого края кадра анимации символов в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="23b47-108">Address of a variable that receives the screen coordinate of the character animation frame's left edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="23b47-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*плтоп*</span><span class="sxs-lookup"><span data-stu-id="23b47-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="23b47-110">Адрес переменной, получающей экранную координату верхнего края кадра анимации символов в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="23b47-110">Address of a variable that receives the screen coordinate of the character animation frame's top edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="23b47-111">Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на его прямоугольной рамке анимации.</span><span class="sxs-lookup"><span data-stu-id="23b47-111">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="23b47-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="23b47-112">See Also</span></span>

<span data-ttu-id="23b47-113">[**Иажентчарактер:: SetPosition**](iagentcharacter--setposition.md), [ **иажентчарактер:: DataSize**](iagentcharacter--getsize.md)</span><span class="sxs-lookup"><span data-stu-id="23b47-113">[**IAgentCharacter::SetPosition**](iagentcharacter--setposition.md), [**IAgentCharacter::GetSize**](iagentcharacter--getsize.md)</span></span>


 

 




