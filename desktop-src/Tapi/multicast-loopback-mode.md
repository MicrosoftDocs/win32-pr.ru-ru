---
description: Перечисление режима многоадресного \_ замыкания \_ описывает режим многоадресного замыкания на себя.
ms.assetid: bf9c3665-71cc-4cde-9ad4-1a8b62eddf9f
title: Перечисление MULTICAST_LOOPBACK_MODE (Конфприв. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a15505efcd1a9e399866b104da0582ccf846689
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689536"
---
# <a name="multicast_loopback_mode-enumeration"></a><span data-ttu-id="43597-103">Перечисление в режиме многоадресного \_ замыкания \_</span><span class="sxs-lookup"><span data-stu-id="43597-103">MULTICAST\_LOOPBACK\_MODE enumeration</span></span>

<span data-ttu-id="43597-104">\[**Многоадресная рассылка \_ \_Режим замыкания на себя** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="43597-104">\[**MULTICAST\_LOOPBACK\_MODE** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="43597-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="43597-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="43597-106">Перечисление **режима многоадресного \_ замыкания \_** описывает режим многоадресного замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="43597-106">The **MULTICAST\_LOOPBACK\_MODE** enum describes the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="43597-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43597-107">Syntax</span></span>


```C++
} MULTICAST_LOOPBACK_MODE;
```



## <a name="constants"></a><span data-ttu-id="43597-108">Константы</span><span class="sxs-lookup"><span data-stu-id="43597-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="43597-109"><span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM \_ без \_ замыкания на себя**</span><span class="sxs-lookup"><span data-stu-id="43597-109"><span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM\_NO\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="43597-110">Многоадресное замыкание на себя отключено.</span><span class="sxs-lookup"><span data-stu-id="43597-110">Multicast loopback is disabled.</span></span> <span data-ttu-id="43597-111">Это означает, что два приложения на одном компьютере, присоединяющиеся к одной группе многоадресной рассылки, могут получить пакеты друг друга.</span><span class="sxs-lookup"><span data-stu-id="43597-111">That means two applications on the same machine joining the same multicast group can get each other's packets.</span></span>

</dd> <dt>

<span data-ttu-id="43597-112"><span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**\_полный \_ замыкание на себя mm**</span><span class="sxs-lookup"><span data-stu-id="43597-112"><span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**MM\_FULL\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="43597-113">Все отправленные пакеты также будут циклически возвращаться.</span><span class="sxs-lookup"><span data-stu-id="43597-113">All the packets sent out are looped back as well.</span></span> <span data-ttu-id="43597-114">Этот режим удобен только для тестирования.</span><span class="sxs-lookup"><span data-stu-id="43597-114">This mode is useful only for testing.</span></span>

</dd> <dt>

<span data-ttu-id="43597-115"><span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**\_повременное \_ замыкание на mm**</span><span class="sxs-lookup"><span data-stu-id="43597-115"><span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**MM\_SELECTIVE\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="43597-116">Режим выборочного замыкания на себя включен.</span><span class="sxs-lookup"><span data-stu-id="43597-116">Selective loopback is enabled.</span></span> <span data-ttu-id="43597-117">Это означает, что включение нескольких приложений на одном компьютере может быть присоединяться к одной группе многоадресной рассылки без путаницы.</span><span class="sxs-lookup"><span data-stu-id="43597-117">That means enabled multiple applications on one machine can join the same multicast group without confusion.</span></span> <span data-ttu-id="43597-118">Пакеты передаются обратно из стека, и каждый сеанс RTP отвечает за фильтрацию ненужных пакетов.</span><span class="sxs-lookup"><span data-stu-id="43597-118">The packets are looped back from the stack and each RTP session is responsible for filtering out unwanted packets.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43597-119">Требования</span><span class="sxs-lookup"><span data-stu-id="43597-119">Requirements</span></span>



| <span data-ttu-id="43597-120">Требование</span><span class="sxs-lookup"><span data-stu-id="43597-120">Requirement</span></span> | <span data-ttu-id="43597-121">Значение</span><span class="sxs-lookup"><span data-stu-id="43597-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43597-122">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="43597-122">TAPI version</span></span><br/> | <span data-ttu-id="43597-123">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="43597-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="43597-124">Header</span><span class="sxs-lookup"><span data-stu-id="43597-124">Header</span></span><br/>       | <dl> <span data-ttu-id="43597-125"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="43597-125"><dt>Confpriv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43597-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43597-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43597-127">**Имултикастконтрол:: Get \_ лупбаккмоде**</span><span class="sxs-lookup"><span data-stu-id="43597-127">**IMulticastControl::get\_LoopbackMode**</span></span>](imulticastcontrol-get-loopbackmode.md)
</dt> <dt>

[<span data-ttu-id="43597-128">**Имултикастконтрол::p UT \_ лупбаккмоде**</span><span class="sxs-lookup"><span data-stu-id="43597-128">**IMulticastControl::put\_LoopbackMode**</span></span>](imulticastcontrol-put-loopbackmode.md)
</dt> </dl>

 

 




