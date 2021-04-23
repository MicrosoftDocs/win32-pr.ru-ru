---
description: 'Перечисление Каллкуалитипроперти используется методами Иткаллкуалитиконтрол::, Иткаллкуалитиконтрол:: Get и Иткаллкуалитиконтрол:: Set для указания свойства качества вызова, для которого выполняется обращение.'
ms.assetid: d9a04cc4-9b7d-4b01-918f-e4938c172b8e
title: Перечисление Каллкуалитипроперти (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ca3af31e0b85a443bb34ac1992b3d3b5c89bfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675716"
---
# <a name="callqualityproperty-enumeration"></a><span data-ttu-id="6afdc-103">Перечисление Каллкуалитипроперти</span><span class="sxs-lookup"><span data-stu-id="6afdc-103">CallQualityProperty enumeration</span></span>

<span data-ttu-id="6afdc-104">\[ Это перечисление недоступно для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="6afdc-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6afdc-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="6afdc-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6afdc-106">Перечисление **каллкуалитипроперти** используется методами [**иткаллкуалитиконтрол::**](itcallqualitycontrol-getrange.md), [**Иткаллкуалитиконтрол:: Get**](itcallqualitycontrol-get.md)и [**иткаллкуалитиконтрол:: Set**](itcallqualitycontrol-set.md) для указания свойства качества вызова, для которого выполняется обращение.</span><span class="sxs-lookup"><span data-stu-id="6afdc-106">The **CallQualityProperty** enum is used by the [**ITCallQualityControl::GetRange**](itcallqualitycontrol-getrange.md), [**ITCallQualityControl::Get**](itcallqualitycontrol-get.md), and [**ITCallQualityControl::Set**](itcallqualitycontrol-set.md) methods to indicate the call quality property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6afdc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6afdc-107">Syntax</span></span>


```C++
} CallQualityProperty;
```



## <a name="constants"></a><span data-ttu-id="6afdc-108">Константы</span><span class="sxs-lookup"><span data-stu-id="6afdc-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6afdc-109"><span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**Каллкуалити \_ контролинтервал**</span><span class="sxs-lookup"><span data-stu-id="6afdc-109"><span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**CallQuality\_ControlInterval**</span></span>
</dt> <dd>

<span data-ttu-id="6afdc-110">Интервал управления.</span><span class="sxs-lookup"><span data-stu-id="6afdc-110">Control interval.</span></span>

</dd> <dt>

<span data-ttu-id="6afdc-111"><span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**Каллкуалити \_ конфбитрате**</span><span class="sxs-lookup"><span data-stu-id="6afdc-111"><span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**CallQuality\_ConfBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="6afdc-112">Скорость для Конференции.</span><span class="sxs-lookup"><span data-stu-id="6afdc-112">Bit rate for conference.</span></span>

</dd> <dt>

<span data-ttu-id="6afdc-113"><span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**Каллкуалити \_ максинпутбитрате**</span><span class="sxs-lookup"><span data-stu-id="6afdc-113"><span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**CallQuality\_MaxInputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="6afdc-114">Максимальная скорость входных бит.</span><span class="sxs-lookup"><span data-stu-id="6afdc-114">Maximum input bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="6afdc-115"><span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**Каллкуалити \_ курринпутбитрате**</span><span class="sxs-lookup"><span data-stu-id="6afdc-115"><span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**CallQuality\_CurrInputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="6afdc-116">Текущая скорость входных битов.</span><span class="sxs-lookup"><span data-stu-id="6afdc-116">Current input bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="6afdc-117"><span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**Каллкуалити \_ максаутпутбитрате**</span><span class="sxs-lookup"><span data-stu-id="6afdc-117"><span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**CallQuality\_MaxOutputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="6afdc-118">Максимальная скорость выходного бита.</span><span class="sxs-lookup"><span data-stu-id="6afdc-118">Maximum output bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="6afdc-119"><span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**Каллкуалити \_ курраутпутбитрате**</span><span class="sxs-lookup"><span data-stu-id="6afdc-119"><span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**CallQuality\_CurrOutputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="6afdc-120">Текущая скорость потока вывода.</span><span class="sxs-lookup"><span data-stu-id="6afdc-120">Current output bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="6afdc-121"><span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**Каллкуалити \_ MaxCPULoad**</span><span class="sxs-lookup"><span data-stu-id="6afdc-121"><span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**CallQuality\_MaxCPULoad**</span></span>
</dt> <dd>

<span data-ttu-id="6afdc-122">Максимальная загрузка ЦП.</span><span class="sxs-lookup"><span data-stu-id="6afdc-122">Maximum CPU load.</span></span>

</dd> <dt>

<span data-ttu-id="6afdc-123"><span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**Каллкуалити \_ курркпулоад**</span><span class="sxs-lookup"><span data-stu-id="6afdc-123"><span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**CallQuality\_CurrCPULoad**</span></span>
</dt> <dd>

<span data-ttu-id="6afdc-124">Текущая загрузка ЦП.</span><span class="sxs-lookup"><span data-stu-id="6afdc-124">Current CPU load.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6afdc-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6afdc-125">Requirements</span></span>



| <span data-ttu-id="6afdc-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6afdc-126">Requirement</span></span> | <span data-ttu-id="6afdc-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6afdc-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6afdc-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="6afdc-128">TAPI version</span></span><br/> | <span data-ttu-id="6afdc-129">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="6afdc-129">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="6afdc-130">Header</span><span class="sxs-lookup"><span data-stu-id="6afdc-130">Header</span></span><br/>       | <dl> <span data-ttu-id="6afdc-131"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="6afdc-131"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6afdc-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6afdc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6afdc-133">**Иткаллкуалитиконтрол:: Range**</span><span class="sxs-lookup"><span data-stu-id="6afdc-133">**ITCallQualityControl::GetRange**</span></span>](itcallqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="6afdc-134">**Иткаллкуалитиконтрол:: Get**</span><span class="sxs-lookup"><span data-stu-id="6afdc-134">**ITCallQualityControl::Get**</span></span>](itcallqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="6afdc-135">**Иткаллкуалитиконтрол:: Set**</span><span class="sxs-lookup"><span data-stu-id="6afdc-135">**ITCallQualityControl::Set**</span></span>](itcallqualitycontrol-set.md)
</dt> </dl>

 

 




