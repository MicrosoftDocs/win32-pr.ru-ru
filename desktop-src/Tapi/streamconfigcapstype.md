---
description: Тип перечисления Стреамконфигкапстипе используется в \_ структуре "заглушка" конфигурации потока TAPI в \_ \_ качестве параметра для указания того, используется ли потоковая передача аудио или видео.
ms.assetid: c3eec6b2-ce3b-49b1-a0ba-f450d60a1477
title: Перечисление Стреамконфигкапстипе (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14649edb7e451cdc7d955f2028a77c247148182b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680093"
---
# <a name="streamconfigcapstype-enumeration"></a><span data-ttu-id="40392-103">Перечисление Стреамконфигкапстипе</span><span class="sxs-lookup"><span data-stu-id="40392-103">StreamConfigCapsType enumeration</span></span>

<span data-ttu-id="40392-104">\[ Это перечисление недоступно для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="40392-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="40392-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="40392-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="40392-106">Тип перечисления **стреамконфигкапстипе** используется в структуре " [**\_ \_ \_ заглушка" конфигурации потока TAPI**](tapi-stream-config-caps.md) в качестве параметра для указания того, используется ли потоковая передача аудио или видео.</span><span class="sxs-lookup"><span data-stu-id="40392-106">The **StreamConfigCapsType** enumeration type is used by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure as a switch to indicate whether audio or video streaming is involved.</span></span>

## <a name="syntax"></a><span data-ttu-id="40392-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40392-107">Syntax</span></span>


```C++
} StreamConfigCapsType;
```



## <a name="constants"></a><span data-ttu-id="40392-108">Константы</span><span class="sxs-lookup"><span data-stu-id="40392-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="40392-109"><span id="AudioStreamConfigCaps"></span><span id="audiostreamconfigcaps"></span><span id="AUDIOSTREAMCONFIGCAPS"></span>**аудиостреамконфигкапс**</span><span class="sxs-lookup"><span data-stu-id="40392-109"><span id="AudioStreamConfigCaps"></span><span id="audiostreamconfigcaps"></span><span id="AUDIOSTREAMCONFIGCAPS"></span>**AudioStreamConfigCaps**</span></span>
</dt> <dd>

<span data-ttu-id="40392-110">Настройка потоковой передачи аудио.</span><span class="sxs-lookup"><span data-stu-id="40392-110">Audio streaming configuration.</span></span>

</dd> <dt>

<span data-ttu-id="40392-111"><span id="VideoStreamConfigCaps"></span><span id="videostreamconfigcaps"></span><span id="VIDEOSTREAMCONFIGCAPS"></span>**видеостреамконфигкапс**</span><span class="sxs-lookup"><span data-stu-id="40392-111"><span id="VideoStreamConfigCaps"></span><span id="videostreamconfigcaps"></span><span id="VIDEOSTREAMCONFIGCAPS"></span>**VideoStreamConfigCaps**</span></span>
</dt> <dd>

<span data-ttu-id="40392-112">Настройка потоковой передачи видео.</span><span class="sxs-lookup"><span data-stu-id="40392-112">Video streaming configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40392-113">Требования</span><span class="sxs-lookup"><span data-stu-id="40392-113">Requirements</span></span>



| <span data-ttu-id="40392-114">Требование</span><span class="sxs-lookup"><span data-stu-id="40392-114">Requirement</span></span> | <span data-ttu-id="40392-115">Значение</span><span class="sxs-lookup"><span data-stu-id="40392-115">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40392-116">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="40392-116">TAPI version</span></span><br/> | <span data-ttu-id="40392-117">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="40392-117">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="40392-118">Header</span><span class="sxs-lookup"><span data-stu-id="40392-118">Header</span></span><br/>       | <dl> <span data-ttu-id="40392-119"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="40392-119"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40392-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40392-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40392-121">**\_ \_ ограничения конфигурации потока \_ TAPI**</span><span class="sxs-lookup"><span data-stu-id="40392-121">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




