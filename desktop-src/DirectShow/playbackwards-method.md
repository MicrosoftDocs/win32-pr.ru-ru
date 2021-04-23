---
description: Метод Плайбакквардс запускает обратное воспроизведение из текущего расположения с указанной скоростью.
ms.assetid: 7f8421e7-f835-4a10-a9c9-0e43de159e4f
title: Метод Плайбакквардс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b396c3829569d3f3ad25f0c0e8718dfd23f268
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494199"
---
# <a name="playbackwards-method"></a><span data-ttu-id="f7de5-103">Метод Плайбакквардс</span><span class="sxs-lookup"><span data-stu-id="f7de5-103">PlayBackwards Method</span></span>

> [!Note]  
> <span data-ttu-id="f7de5-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f7de5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f7de5-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="f7de5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f7de5-106">`PlayBackwards`Метод запускает обратное воспроизведение из текущего расположения с указанной скоростью.</span><span class="sxs-lookup"><span data-stu-id="f7de5-106">The `PlayBackwards` method starts backward playback from the current location at the specified speed.</span></span>

``` syntax
MSWebDVD.PlayBackwards(nSpeed)
```

## <a name="parameters"></a><span data-ttu-id="f7de5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7de5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7de5-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*нспид*</span><span class="sxs-lookup"><span data-stu-id="f7de5-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="f7de5-109">Указывает скорость воспроизведения в виде числа.</span><span class="sxs-lookup"><span data-stu-id="f7de5-109">Specifies the speed at which to play as a number.</span></span> <span data-ttu-id="f7de5-110">Это число является множителем — 1,0 — это обычная скорость воспроизведения; 2,0 — это двойная скорость, 0,5 — половина скорости и т. д.</span><span class="sxs-lookup"><span data-stu-id="f7de5-110">This number is a multiplier—1.0 is normal playback speed; 2.0 is double speed, 0.5 is half speed, and so on.</span></span> <span data-ttu-id="f7de5-111">Если **нспид** не равно 1,0, звук будет выключен и подизображение будет отключено.</span><span class="sxs-lookup"><span data-stu-id="f7de5-111">When **nSpeed** does not equal 1.0, audio is muted and the subpicture is turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7de5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7de5-112">Return Value</span></span>

<span data-ttu-id="f7de5-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="f7de5-113">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7de5-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7de5-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7de5-115">**плайфорвардс**</span><span class="sxs-lookup"><span data-stu-id="f7de5-115">**PlayForwards**</span></span>](playforwards-method.md)
</dt> </dl>

 

 



