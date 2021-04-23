---
description: '\_Список КОНСТАНТ линекаллтреатмент содержит использование для вызовов, которые не отвечают, или в удержании. За исключением обычной проверки параметров, метод обработки вызовов — это прямой транзит по интерфейсу TAPI поставщику услуг.'
ms.assetid: c28c9200-dd51-48b2-905c-fbe37c83b00f
title: Константы LINECALLTREATMENT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25a19b5db4525550047c468b496cce2363f6ee2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689344"
---
# <a name="linecalltreatment_-constants"></a><span data-ttu-id="d989d-104">\_Константы линекаллтреатмент</span><span class="sxs-lookup"><span data-stu-id="d989d-104">LINECALLTREATMENT\_ Constants</span></span>

<span data-ttu-id="d989d-105">Список **констант \_ линекаллтреатмент** содержит использование для вызовов, которые не отвечают, или в удержании.</span><span class="sxs-lookup"><span data-stu-id="d989d-105">The **LINECALLTREATMENT\_** constants list treatments for calls that are unanswered or on hold.</span></span> <span data-ttu-id="d989d-106">За исключением обычной проверки параметров, метод обработки вызовов — это прямой транзит по интерфейсу TAPI поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="d989d-106">Except for basic parameter validation, call treatment is a straight pass-through by TAPI to the service provider.</span></span>

<dl> <dt>

<span data-ttu-id="d989d-107"><span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**ЛИНЕКАЛЛТРЕАТМЕНТ \_ занят**</span><span class="sxs-lookup"><span data-stu-id="d989d-107"><span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d989d-108">Если вызов не подключен к устройству (предложению или onhold), то сторона слышит сигнал занятости.</span><span class="sxs-lookup"><span data-stu-id="d989d-108">When the call is not actively connected to a device (offering or onhold), the party hears busy signal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d989d-109"><span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**ЛИНЕКАЛЛТРЕАТМЕНТ \_ музыка**</span><span class="sxs-lookup"><span data-stu-id="d989d-109"><span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**LINECALLTREATMENT\_MUSIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d989d-110">Если вызов не подключен к устройству (предложению или onhold), то он слышит музыку.</span><span class="sxs-lookup"><span data-stu-id="d989d-110">When the call is not actively connected to a device (offering or onhold), the party hears music.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d989d-111"><span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**ЛИНЕКАЛЛТРЕАТМЕНТ \_ звонка**</span><span class="sxs-lookup"><span data-stu-id="d989d-111"><span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**LINECALLTREATMENT\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d989d-112">Если вызов не подключен к устройству (предложению или "onhold), сторона слышит тон звонка.</span><span class="sxs-lookup"><span data-stu-id="d989d-112">When the call is not actively connected to a device (offering or onhold), the party hears ringback tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d989d-113"><span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**ЛИНЕКАЛЛТРЕАТМЕНТ \_ тишины**</span><span class="sxs-lookup"><span data-stu-id="d989d-113"><span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**LINECALLTREATMENT\_SILENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d989d-114">Если вызов не подключен к устройству (предложению или onhold), то сторона слышит тишину.</span><span class="sxs-lookup"><span data-stu-id="d989d-114">When the call is not actively connected to a device (offering or onhold), the party hears silence.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d989d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d989d-115">Remarks</span></span>

<span data-ttu-id="d989d-116">Значение 0x00000000 зарезервировано, чтобы указать, что поставщик услуг не поддерживает вызов использование.</span><span class="sxs-lookup"><span data-stu-id="d989d-116">The value 0x00000000 is reserved to indicate that the service provider does not support call treatments.</span></span> <span data-ttu-id="d989d-117">Значения в диапазоне от 0x00000005 до 0x000000FF зарезервированы для определения в будущем.</span><span class="sxs-lookup"><span data-stu-id="d989d-117">Values in the range 0x00000005 through 0x000000FF are reserved for future definition.</span></span> <span data-ttu-id="d989d-118">Значения в диапазоне от 0x00000100 до 0xFFFFFFFF зарезервированы для назначения поставщиками услуг и могут включать в себя идентификацию определенных музыкальных выборов или записанных объявлений.</span><span class="sxs-lookup"><span data-stu-id="d989d-118">Values in the range 0x00000100 through 0xFFFFFFFF are reserved for assignment by service providers, and may include identification of specific musical selections or recorded announcements.</span></span>

## <a name="requirements"></a><span data-ttu-id="d989d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d989d-119">Requirements</span></span>



| <span data-ttu-id="d989d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d989d-120">Requirement</span></span> | <span data-ttu-id="d989d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d989d-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d989d-122">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="d989d-122">TAPI version</span></span><br/> | <span data-ttu-id="d989d-123">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d989d-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d989d-124">Header</span><span class="sxs-lookup"><span data-stu-id="d989d-124">Header</span></span><br/>       | <dl> <span data-ttu-id="d989d-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d989d-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




