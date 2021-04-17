---
description: '\_Перечисление возможностей H245 описывает поддержку формата аудио и видео.'
ms.assetid: 76aeb3a1-3233-4425-b9db-efacbedc309e
title: Перечисление H245_CAPABILITY (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7a6f81f87480f221f87680d9cf086120deb2de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689376"
---
# <a name="h245_capability-enumeration"></a><span data-ttu-id="2a75b-103">\_Перечисление возможностей H245</span><span class="sxs-lookup"><span data-stu-id="2a75b-103">H245\_CAPABILITY enumeration</span></span>

<span data-ttu-id="2a75b-104">\[**H245 \_ ВОЗМОЖНОСТЬ** недоступна для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2a75b-104">\[**H245\_CAPABILITY** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2a75b-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="2a75b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2a75b-106">Перечисление **\_ возможностей H245** описывает поддержку формата аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="2a75b-106">The **H245\_CAPABILITY** enum describes audio and video format support.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a75b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a75b-107">Syntax</span></span>


```C++
} H245_CAPABILITY;
```



## <a name="constants"></a><span data-ttu-id="2a75b-108">Константы</span><span class="sxs-lookup"><span data-stu-id="2a75b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2a75b-109"><span id="HC_G711"></span><span id="hc_g711"></span>**HC \_ G711**</span><span class="sxs-lookup"><span data-stu-id="2a75b-109"><span id="HC_G711"></span><span id="hc_g711"></span>**HC\_G711**</span></span>
</dt> <dd>

<span data-ttu-id="2a75b-110">Поддерживается звуковой протокол G. 711.</span><span class="sxs-lookup"><span data-stu-id="2a75b-110">The G.711 audio protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="2a75b-111"><span id="HC_G723"></span><span id="hc_g723"></span>**HC \_ G723**</span><span class="sxs-lookup"><span data-stu-id="2a75b-111"><span id="HC_G723"></span><span id="hc_g723"></span>**HC\_G723**</span></span>
</dt> <dd>

<span data-ttu-id="2a75b-112">Поддерживается звуковой протокол G. 723.</span><span class="sxs-lookup"><span data-stu-id="2a75b-112">The G.723 audio protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="2a75b-113"><span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC \_ H263QCIF**</span><span class="sxs-lookup"><span data-stu-id="2a75b-113"><span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC\_H263QCIF**</span></span>
</dt> <dd>

<span data-ttu-id="2a75b-114">Поддерживается протокол видео H. 263.</span><span class="sxs-lookup"><span data-stu-id="2a75b-114">The H.263 video protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="2a75b-115"><span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC \_ H261QCIF**</span><span class="sxs-lookup"><span data-stu-id="2a75b-115"><span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC\_H261QCIF**</span></span>
</dt> <dd>

<span data-ttu-id="2a75b-116">Поддерживается протокол видео H. 263.</span><span class="sxs-lookup"><span data-stu-id="2a75b-116">The H.263 video protocol is supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a75b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2a75b-117">Requirements</span></span>



| <span data-ttu-id="2a75b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2a75b-118">Requirement</span></span> | <span data-ttu-id="2a75b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2a75b-119">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a75b-120">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="2a75b-120">TAPI version</span></span><br/> | <span data-ttu-id="2a75b-121">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2a75b-121">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2a75b-122">Header</span><span class="sxs-lookup"><span data-stu-id="2a75b-122">Header</span></span><br/>       | <dl> <span data-ttu-id="2a75b-123"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a75b-123"><dt>H323priv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a75b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a75b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a75b-125">**IH323LineEx:: Сетдефаулткапабилитипреферренце**</span><span class="sxs-lookup"><span data-stu-id="2a75b-125">**IH323LineEx::SetDefaultCapabilityPreferrence**</span></span>](ih323lineex-setdefaultcapabilitypreferrence.md)
</dt> </dl>

 

 




