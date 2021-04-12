---
title: Иажентчарактер
description: Иажентчарактер
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e40c219cd0a1dc1d11738149ca7cfd9869fe682e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332755"
---
# <a name="iagentcharactergetsize"></a><span data-ttu-id="98b8e-103">Иажентчарактер:: DataSize</span><span class="sxs-lookup"><span data-stu-id="98b8e-103">IAgentCharacter::GetSize</span></span>

<span data-ttu-id="98b8e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="98b8e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

<span data-ttu-id="98b8e-105">Возвращает размер кадра анимации символа.</span><span class="sxs-lookup"><span data-stu-id="98b8e-105">Retrieves the size of the character's animation frame.</span></span>

-   <span data-ttu-id="98b8e-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="98b8e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="98b8e-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*плвидс*</span><span class="sxs-lookup"><span data-stu-id="98b8e-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="98b8e-108">Адрес переменной, получающей ширину кадра анимации символов в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="98b8e-108">Address of a variable that receives the width of the character animation frame in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="98b8e-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*плхеигхт*</span><span class="sxs-lookup"><span data-stu-id="98b8e-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="98b8e-110">Адрес переменной, получающей высоту кадра анимации символов в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="98b8e-110">Address of a variable that receives the height of the character animation frame in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="98b8e-111">Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на его прямоугольной рамке анимации.</span><span class="sxs-lookup"><span data-stu-id="98b8e-111">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="98b8e-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="98b8e-112">See Also</span></span>

[<span data-ttu-id="98b8e-113">**Иажентчарактер:: SetSize**</span><span class="sxs-lookup"><span data-stu-id="98b8e-113">**IAgentCharacter::SetSize**</span></span>](iagentcharacter--setsize.md)


 

 




