---
description: Метод Плайаттимеинтитле запускает воспроизведение в указанное время в заданном заголовке.
ms.assetid: 82726885-8393-409b-b8a1-29a8e9e9ac65
title: Метод Плайаттимеинтитле
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c40373b4327b6df5fc341ca392c223d464a70a8b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494202"
---
# <a name="playattimeintitle-method"></a><span data-ttu-id="ade38-103">Метод Плайаттимеинтитле</span><span class="sxs-lookup"><span data-stu-id="ade38-103">PlayAtTimeInTitle Method</span></span>

> [!Note]  
> <span data-ttu-id="ade38-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ade38-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ade38-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="ade38-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ade38-106">`PlayAtTimeInTitle`Метод запускает воспроизведение в указанное время в заданном заголовке.</span><span class="sxs-lookup"><span data-stu-id="ade38-106">The `PlayAtTimeInTitle` method starts playback at the specified time within the specified title.</span></span>

``` syntax
MSWebDVD.PlayAtTimeInTitle(sTime, iTitle)
```

## <a name="parameters"></a><span data-ttu-id="ade38-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ade38-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ade38-108"><span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*стиме*</span><span class="sxs-lookup"><span data-stu-id="ade38-108"><span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*sTime*</span></span>
</dt> <dd>

<span data-ttu-id="ade38-109">Указывает время начала воспроизведения в виде строки.</span><span class="sxs-lookup"><span data-stu-id="ade38-109">Specifies the time at which to start playback as a string.</span></span> <span data-ttu-id="ade38-110">Строка должна иметь формат "чч: мм: СС: FF" (указание часов, минут, секунд, кадров).</span><span class="sxs-lookup"><span data-stu-id="ade38-110">The string must be in the format "hh:mm:ss:ff" (specifying hours, minutes, seconds, frames).</span></span>

</dd> <dt>

<span data-ttu-id="ade38-111"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*ититле*</span><span class="sxs-lookup"><span data-stu-id="ade38-111"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="ade38-112">Задает индекс заголовка в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="ade38-112">Specifies the index of the title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ade38-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ade38-113">Return Value</span></span>

<span data-ttu-id="ade38-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="ade38-114">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="ade38-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ade38-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ade38-116">**курренттитле**</span><span class="sxs-lookup"><span data-stu-id="ade38-116">**CurrentTitle**</span></span>](currenttitle-property.md)
</dt> <dt>

[<span data-ttu-id="ade38-117">**плайаттиме**</span><span class="sxs-lookup"><span data-stu-id="ade38-117">**PlayAtTime**</span></span>](playattime-method.md)
</dt> <dt>

[<span data-ttu-id="ade38-118">**титлесаваилабле**</span><span class="sxs-lookup"><span data-stu-id="ade38-118">**TitlesAvailable**</span></span>](titlesavailable-property.md)
</dt> </dl>

 

 



