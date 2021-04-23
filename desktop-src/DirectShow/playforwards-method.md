---
description: Метод Плайфорвардс начинает пересылать воспроизведение из текущего расположения с указанной скоростью.
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: Метод Плайфорвардс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d49d8d6d80613c4dd5b2b8a374002b37d9baa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806245"
---
# <a name="playforwards-method"></a><span data-ttu-id="eed0f-103">Метод Плайфорвардс</span><span class="sxs-lookup"><span data-stu-id="eed0f-103">PlayForwards Method</span></span>

> [!Note]  
> <span data-ttu-id="eed0f-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="eed0f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="eed0f-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="eed0f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="eed0f-106">`PlayForwards`Метод начинает пересылать воспроизведение из текущего расположения с указанной скоростью.</span><span class="sxs-lookup"><span data-stu-id="eed0f-106">The `PlayForwards` method starts forward playback from the current location at the specified speed.</span></span>

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a><span data-ttu-id="eed0f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="eed0f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eed0f-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*нспид*</span><span class="sxs-lookup"><span data-stu-id="eed0f-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="eed0f-109">Задает скорость воспроизведения в виде целочисленного значения.</span><span class="sxs-lookup"><span data-stu-id="eed0f-109">Specifies the speed at which to play as an Integer value.</span></span> <span data-ttu-id="eed0f-110">Это значение равно множителю — 1,0 — нормальная скорость воспроизведения; 2,0 — это двойная скорость, 0,5 — половина скорости и т. д.</span><span class="sxs-lookup"><span data-stu-id="eed0f-110">This value is a multiplier—1.0 is normal playback speed; 2.0 is double speed, 0.5 is half speed, and so on.</span></span> <span data-ttu-id="eed0f-111">Если **нспид** не равно 1,0, звук будет выключен и подизображение будет отключено.</span><span class="sxs-lookup"><span data-stu-id="eed0f-111">When **nSpeed** does not equal 1.0, audio is muted and the subpicture is turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eed0f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eed0f-112">Return Value</span></span>

<span data-ttu-id="eed0f-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="eed0f-113">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="eed0f-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eed0f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed0f-115">**плайбакквардс**</span><span class="sxs-lookup"><span data-stu-id="eed0f-115">**PlayBackwards**</span></span>](playbackwards-method.md)
</dt> </dl>

 

 



