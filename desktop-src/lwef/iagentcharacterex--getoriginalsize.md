---
title: Иажентчарактерекс Жеторигиналсизе
description: Иажентчарактерекс Жеторигиналсизе
ms.assetid: a27ae88f-3655-4375-b563-0cc320d012cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e1712587e70d9756e3d37ca9e0f3cbfdb82c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067790"
---
# <a name="iagentcharacterexgetoriginalsize"></a><span data-ttu-id="14d71-103">Иажентчарактерекс:: Жеторигиналсизе</span><span class="sxs-lookup"><span data-stu-id="14d71-103">IAgentCharacterEx::GetOriginalSize</span></span>

<span data-ttu-id="14d71-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="14d71-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetOriginalSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

<span data-ttu-id="14d71-105">Получает исходный размер кадра анимации символа.</span><span class="sxs-lookup"><span data-stu-id="14d71-105">Retrieves the original size of the character's animation frame.</span></span>

-   <span data-ttu-id="14d71-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="14d71-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="14d71-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*плвидс*</span><span class="sxs-lookup"><span data-stu-id="14d71-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="14d71-108">Адрес переменной, получающей исходную ширину кадра анимации символов в пикселях.</span><span class="sxs-lookup"><span data-stu-id="14d71-108">Address of a variable that receives the original width of the character animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="14d71-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*плхеигхт*</span><span class="sxs-lookup"><span data-stu-id="14d71-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="14d71-110">Адрес переменной, получающей исходную высоту кадра анимации символов в пикселях.</span><span class="sxs-lookup"><span data-stu-id="14d71-110">Address of a variable that receives the original height of the character animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="14d71-111">Этот вызов возвращает исходный размер рамки символов, созданной в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="14d71-111">This call returns the original size of the character frame as built in the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="14d71-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="14d71-112">See Also</span></span>

[<span data-ttu-id="14d71-113">**Иажентчарактер:: DataSize**</span><span class="sxs-lookup"><span data-stu-id="14d71-113">**IAgentCharacter::GetSize**</span></span>](iagentcharacter--getsize.md)


 

 




