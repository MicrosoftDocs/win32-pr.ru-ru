---
title: Иажентчарактер MoveTo
description: Иажентчарактер MoveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d1ba423dc637895216ff03e2adec2862bbf27d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069879"
---
# <a name="iagentcharactermoveto"></a><span data-ttu-id="c9d4d-103">Иажентчарактер:: MoveTo</span><span class="sxs-lookup"><span data-stu-id="c9d4d-103">IAgentCharacter::MoveTo</span></span>

<span data-ttu-id="c9d4d-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c9d4d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="c9d4d-105">Воспроизводит связанную анимацию с **перемещаемым** состоянием и перемещает рамку символов в указанное место.</span><span class="sxs-lookup"><span data-stu-id="c9d4d-105">Plays the associated **Moving** state animation and moves the character frame to the specified location.</span></span>

-   <span data-ttu-id="c9d4d-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c9d4d-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="c9d4d-107">При возврате функции эта переменная содержит идентификатор запроса.</span><span class="sxs-lookup"><span data-stu-id="c9d4d-107">When the function returns, this variable contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="c9d4d-108"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="c9d4d-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="c9d4d-109">Координата по оси x нового положения в пикселях относительно начала координат экрана (в левом верхнем углу).</span><span class="sxs-lookup"><span data-stu-id="c9d4d-109">The x-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="c9d4d-110">Расположение символа основано на левом верхнем углу фрейма анимации.</span><span class="sxs-lookup"><span data-stu-id="c9d4d-110">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="c9d4d-111"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="c9d4d-111"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="c9d4d-112">Координата по оси y нового положения в пикселях относительно начала координат экрана (сверху слева).</span><span class="sxs-lookup"><span data-stu-id="c9d4d-112">The y-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="c9d4d-113">Расположение символа основано на левом верхнем углу фрейма анимации.</span><span class="sxs-lookup"><span data-stu-id="c9d4d-113">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="c9d4d-114"><span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*лспид*</span><span class="sxs-lookup"><span data-stu-id="c9d4d-114"><span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="c9d4d-115">Параметр, задающий в миллисекундах скорость перемещения кадра символа.</span><span class="sxs-lookup"><span data-stu-id="c9d4d-115">A parameter specifying in milliseconds how quickly the character's frame moves.</span></span> <span data-ttu-id="c9d4d-116">Рекомендуемое значение — 1000.</span><span class="sxs-lookup"><span data-stu-id="c9d4d-116">The recommended value is 1000.</span></span> <span data-ttu-id="c9d4d-117">При указании нуля (0) кадр перемещается без воспроизведения анимации.</span><span class="sxs-lookup"><span data-stu-id="c9d4d-117">Specifying zero (0) moves the frame without playing an animation.</span></span>

</dd> <dt>

<span data-ttu-id="c9d4d-118"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*</span><span class="sxs-lookup"><span data-stu-id="c9d4d-118"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="c9d4d-119">Адрес переменной, которая получает идентификатор запроса [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) .</span><span class="sxs-lookup"><span data-stu-id="c9d4d-119">Address of a variable that receives the [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="c9d4d-120">При использовании протокола HTTP для доступа к данным символов и анимации используйте метод [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) , чтобы обеспечить доступность анимации **перемещаемого** состояния перед вызовом этого метода.</span><span class="sxs-lookup"><span data-stu-id="c9d4d-120">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Moving** state animations before calling this method.</span></span> <span data-ttu-id="c9d4d-121">Даже если анимация не загружена, сервер по-прежнему перемещает кадр.</span><span class="sxs-lookup"><span data-stu-id="c9d4d-121">Even if the animation is not loaded, the server still moves the frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9d4d-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="c9d4d-122">See Also</span></span>

[<span data-ttu-id="c9d4d-123">**Иажентчарактер:: SetPosition**</span><span class="sxs-lookup"><span data-stu-id="c9d4d-123">**IAgentCharacter::SetPosition**</span></span>](iagentcharacter--setposition.md)


 

 