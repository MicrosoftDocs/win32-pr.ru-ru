---
description: Метод Плайпериодинтитлеаутостоп запускает воспроизведение в указанное время в заданном заголовке до указанного времени окончания.
ms.assetid: 0c4df76d-3991-4a6c-a8e5-5fd713eeffc2
title: Метод Плайпериодинтитлеаутостоп
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05899b66b7f1a11f8f5b177d311b9634a52595b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894497"
---
# <a name="playperiodintitleautostop-method"></a><span data-ttu-id="067df-103">Метод Плайпериодинтитлеаутостоп</span><span class="sxs-lookup"><span data-stu-id="067df-103">PlayPeriodInTitleAutoStop Method</span></span>

> [!Note]  
> <span data-ttu-id="067df-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="067df-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="067df-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="067df-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="067df-106">`PlayPeriodInTitleAutoStop`Метод запускает воспроизведение в указанное время в заданном заголовке до указанного времени окончания.</span><span class="sxs-lookup"><span data-stu-id="067df-106">The `PlayPeriodInTitleAutoStop` method starts playback at the specified time in the specified title until the specified stop time.</span></span>

``` syntax
MSWebDVD.PlayPeriodInTitleAutoStop(iTitle, sStartTime, sEndTime)
```

## <a name="parameters"></a><span data-ttu-id="067df-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="067df-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="067df-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*ититле*</span><span class="sxs-lookup"><span data-stu-id="067df-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="067df-109">Задает заголовок в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="067df-109">Specifies the title as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="067df-110"><span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*сстарттиме*</span><span class="sxs-lookup"><span data-stu-id="067df-110"><span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*</span></span>
</dt> <dd>

<span data-ttu-id="067df-111">Указывает время начала в виде строки в формате "чч: мм: СС: FF" (с указанием часов, минут, секунд, кадров).</span><span class="sxs-lookup"><span data-stu-id="067df-111">Specifies the start time as a string in "hh:mm:ss:ff" format (specifying hours, minutes, seconds, frames).</span></span>

</dd> <dt>

<span data-ttu-id="067df-112"><span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*сендтиме*</span><span class="sxs-lookup"><span data-stu-id="067df-112"><span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*</span></span>
</dt> <dd>

<span data-ttu-id="067df-113">Задает время окончания в виде строки в формате "чч: мм: СС: FF".</span><span class="sxs-lookup"><span data-stu-id="067df-113">Specifies the end time as a String in "hh:mm:ss:ff" format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="067df-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="067df-114">Return Value</span></span>

<span data-ttu-id="067df-115">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="067df-115">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="067df-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="067df-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="067df-117">**плайчаптерсаутостоп**</span><span class="sxs-lookup"><span data-stu-id="067df-117">**PlayChaptersAutoStop**</span></span>](playchaptersautostop-method.md)
</dt> </dl>

 

 



