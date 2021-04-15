---
description: 'Перечисление Стреамкуалитипроперти, используемое методами Итстреамкуалитиконтрол::, Итстреамкуалитиконтрол:: Get и Итстреамкуалитиконтрол:: Set для указания свойства качества потока, для которого выполняется обращение.'
ms.assetid: 28c9257f-6fbb-440f-9b84-c15a74229b5b
title: Перечисление Стреамкуалитипроперти (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f552641cd0847bb3ff8eec9d528a03171a78c2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689526"
---
# <a name="streamqualityproperty-enumeration"></a><span data-ttu-id="bc984-103">Перечисление Стреамкуалитипроперти</span><span class="sxs-lookup"><span data-stu-id="bc984-103">StreamQualityProperty enumeration</span></span>

<span data-ttu-id="bc984-104">\[ Это перечисление недоступно для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="bc984-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bc984-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="bc984-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bc984-106">Перечисление **стреамкуалитипроперти** , используемое методами [**итстреамкуалитиконтрол::**](itstreamqualitycontrol-getrange.md), [**Итстреамкуалитиконтрол:: Get**](itstreamqualitycontrol-get.md)и [**итстреамкуалитиконтрол:: Set**](itstreamqualitycontrol-set.md) для указания свойства качества потока, для которого выполняется обращение.</span><span class="sxs-lookup"><span data-stu-id="bc984-106">The **StreamQualityProperty** enum used by the [**ITStreamQualityControl::GetRange**](itstreamqualitycontrol-getrange.md), [**ITStreamQualityControl::Get**](itstreamqualitycontrol-get.md), and [**ITStreamQualityControl::Set**](itstreamqualitycontrol-set.md) methods to indicate the stream quality property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc984-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc984-107">Syntax</span></span>


```C++
} StreamQualityProperty;
```



## <a name="constants"></a><span data-ttu-id="bc984-108">Константы</span><span class="sxs-lookup"><span data-stu-id="bc984-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bc984-109"><span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**Стреамкуалити \_ максбитрате**</span><span class="sxs-lookup"><span data-stu-id="bc984-109"><span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**StreamQuality\_MaxBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="bc984-110">Максимальная скорость.</span><span class="sxs-lookup"><span data-stu-id="bc984-110">Maximum bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="bc984-111"><span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**Стреамкуалити \_ куррбитрате**</span><span class="sxs-lookup"><span data-stu-id="bc984-111"><span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**StreamQuality\_CurrBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="bc984-112">Минимальная скорость.</span><span class="sxs-lookup"><span data-stu-id="bc984-112">Minimum bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="bc984-113"><span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**Стреамкуалити \_ минфрамеинтервал**</span><span class="sxs-lookup"><span data-stu-id="bc984-113"><span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**StreamQuality\_MinFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="bc984-114">Максимальный интервал кадров.</span><span class="sxs-lookup"><span data-stu-id="bc984-114">Maximum frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="bc984-115"><span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**Стреамкуалити \_ авгфрамеинтервал**</span><span class="sxs-lookup"><span data-stu-id="bc984-115"><span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**StreamQuality\_AvgFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="bc984-116">Минимальный интервал кадров.</span><span class="sxs-lookup"><span data-stu-id="bc984-116">Minimum frame interval.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc984-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bc984-117">Requirements</span></span>



| <span data-ttu-id="bc984-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bc984-118">Requirement</span></span> | <span data-ttu-id="bc984-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bc984-119">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bc984-120">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="bc984-120">TAPI version</span></span><br/> | <span data-ttu-id="bc984-121">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="bc984-121">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="bc984-122">Header</span><span class="sxs-lookup"><span data-stu-id="bc984-122">Header</span></span><br/>       | <dl> <span data-ttu-id="bc984-123"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc984-123"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc984-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc984-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc984-125">**Итстреамкуалитиконтрол:: Range**</span><span class="sxs-lookup"><span data-stu-id="bc984-125">**ITStreamQualityControl::GetRange**</span></span>](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="bc984-126">**Итстреамкуалитиконтрол:: Get**</span><span class="sxs-lookup"><span data-stu-id="bc984-126">**ITStreamQualityControl::Get**</span></span>](itstreamqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="bc984-127">**Итстреамкуалитиконтрол:: Set**</span><span class="sxs-lookup"><span data-stu-id="bc984-127">**ITStreamQualityControl::Set**</span></span>](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




