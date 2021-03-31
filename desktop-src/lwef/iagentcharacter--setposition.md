---
title: Иажентчарактер SetPosition
description: Иажентчарактер SetPosition
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aee48ea26c714c570f7ae11b9b2dbc0fe92ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067754"
---
# <a name="iagentcharactersetposition"></a><span data-ttu-id="0d421-103">Иажентчарактер:: SetPosition</span><span class="sxs-lookup"><span data-stu-id="0d421-103">IAgentCharacter::SetPosition</span></span>

<span data-ttu-id="0d421-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0d421-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

<span data-ttu-id="0d421-105">Задает расположение кадра анимации символа.</span><span class="sxs-lookup"><span data-stu-id="0d421-105">Sets the position of the character's animation frame.</span></span>

-   <span data-ttu-id="0d421-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="0d421-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0d421-107"><span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*ллефт*</span><span class="sxs-lookup"><span data-stu-id="0d421-107"><span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*</span></span>
</dt> <dd>

<span data-ttu-id="0d421-108">Координата экрана левого края кадра анимации символов в пикселях относительно начала координат экрана (вверху слева).</span><span class="sxs-lookup"><span data-stu-id="0d421-108">Screen coordinate of the character animation frame's left edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="0d421-109"><span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*лтоп*</span><span class="sxs-lookup"><span data-stu-id="0d421-109"><span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*</span></span>
</dt> <dd>

<span data-ttu-id="0d421-110">Координата экрана верхнего края кадра анимации символов в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="0d421-110">Screen coordinate of the character animation frame's top edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="0d421-111">Параметр этого свойства применяется ко всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="0d421-111">This property's setting applies to all clients of the character.</span></span> <span data-ttu-id="0d421-112">Несмотря на то, что символ отображается в окне области неправильной формы, расположение символа основано на его прямоугольной рамке анимации.</span><span class="sxs-lookup"><span data-stu-id="0d421-112">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

> [!Note]  
> <span data-ttu-id="0d421-113">В отличие от метода [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) , эта функция не находится в очереди.</span><span class="sxs-lookup"><span data-stu-id="0d421-113">Unlike the [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) method, this function is not queued.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="0d421-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="0d421-114">See Also</span></span>

[<span data-ttu-id="0d421-115">**Иажентчарактер:: Disposition**</span><span class="sxs-lookup"><span data-stu-id="0d421-115">**IAgentCharacter::GetPosition**</span></span>](iagentcharacter--getposition.md)


 

 




