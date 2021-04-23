---
title: Иажентчарактер
description: Иажентчарактер
ms.assetid: 8324ab84-2b59-4459-b375-700d72b621bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39d5b33afa7ff59516b793f194a0ba186c2e002
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778722"
---
# <a name="iagentcharactersetsize"></a><span data-ttu-id="977dc-103">Иажентчарактер:: SetSize</span><span class="sxs-lookup"><span data-stu-id="977dc-103">IAgentCharacter::SetSize</span></span>

<span data-ttu-id="977dc-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="977dc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSize(
   long * lWidth,  // width of the character frame
   long * lHeight  // height of the character frame
);
```

<span data-ttu-id="977dc-105">Задает размер кадра анимации символа.</span><span class="sxs-lookup"><span data-stu-id="977dc-105">Sets the size of the character's animation frame.</span></span>

-   <span data-ttu-id="977dc-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="977dc-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="977dc-107"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*лвидс*</span><span class="sxs-lookup"><span data-stu-id="977dc-107"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span></span>
</dt> <dd>

<span data-ttu-id="977dc-108">Ширина кадра анимации символа в пикселях.</span><span class="sxs-lookup"><span data-stu-id="977dc-108">The width of the character's animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="977dc-109"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*лхеигхт*</span><span class="sxs-lookup"><span data-stu-id="977dc-109"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span></span>
</dt> <dd>

<span data-ttu-id="977dc-110">Высота кадра анимации символа (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="977dc-110">The height of the character's animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="977dc-111">Изменение размера кадра символа масштабирует символ до размера, заданного этим методом.</span><span class="sxs-lookup"><span data-stu-id="977dc-111">Changing the character's frame size scales the character to the size set with this method.</span></span> <span data-ttu-id="977dc-112">Параметр этого свойства применяется ко всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="977dc-112">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="977dc-113">Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на его прямоугольной рамке анимации.</span><span class="sxs-lookup"><span data-stu-id="977dc-113">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="977dc-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="977dc-114">See Also</span></span>

[<span data-ttu-id="977dc-115">**Иажентчарактер:: DataSize**</span><span class="sxs-lookup"><span data-stu-id="977dc-115">**IAgentCharacter::GetSize**</span></span>](iagentcharacter--getsize.md)


 

 




