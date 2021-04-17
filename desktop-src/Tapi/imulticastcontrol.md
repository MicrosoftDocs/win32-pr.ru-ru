---
description: Интерфейс Имултикастконтрол реализуется Ипконф MSP и доступен только для объектов многоадресного вызова.
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: Интерфейс Имултикастконтрол (Конфприв. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98ad006ea41034d6d4da32359d1ecbcdd250ab6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689207"
---
# <a name="imulticastcontrol-interface"></a><span data-ttu-id="da5f3-103">Интерфейс Имултикастконтрол</span><span class="sxs-lookup"><span data-stu-id="da5f3-103">IMulticastControl interface</span></span>

<span data-ttu-id="da5f3-104">\[**Имултикастконтрол** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="da5f3-104">\[**IMulticastControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="da5f3-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="da5f3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="da5f3-106">Интерфейс **имултикастконтрол** реализуется ипконф MSP и доступен только для объектов многоадресного вызова.</span><span class="sxs-lookup"><span data-stu-id="da5f3-106">The **IMulticastControl** interface is implemented by the IPConf MSP and available only on multicast call objects.</span></span> <span data-ttu-id="da5f3-107">Этот интерфейс предоставляет методы, обеспечивающие создание и обработку терминалов, которые могут взаимодействовать между клиентами H323 и SDP.</span><span class="sxs-lookup"><span data-stu-id="da5f3-107">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span> <span data-ttu-id="da5f3-108">Интерфейс **имултикастконтрол** управляет режимом многоадресного замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="da5f3-108">The **IMulticastControl** interface controls the multicast loopback mode.</span></span>

<span data-ttu-id="da5f3-109">В режиме MM \_ без \_ замыкания на себя многоадресная рассылка отключена, что означает, что два приложения на одном компьютере, которые присоединяются к одной группе многоадресной рассылки, получат пакеты друг друга.</span><span class="sxs-lookup"><span data-stu-id="da5f3-109">In the MM\_NO\_LOOPBACK mode, multicast loopback is disabled, which means two applications on the same machine who join the same multicast group will get each other's packets.</span></span> <span data-ttu-id="da5f3-110">Этот режим имеет лучшую производительность, если на компьютере всегда только одно приложение, соединяющее группу многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="da5f3-110">This mode has the best performance if there is always only one application joining the multicast group on the machine.</span></span> <span data-ttu-id="da5f3-111">\_ \_ В качестве режима по умолчанию используется mm без замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="da5f3-111">MM\_NO\_LOOPBACK mode is the default mode.</span></span>

<span data-ttu-id="da5f3-112">\_Режим полного замыкания на mm подходит \_ только для тестирования.</span><span class="sxs-lookup"><span data-stu-id="da5f3-112">The MM\_FULL\_LOOPBACK mode is good only for testing.</span></span> <span data-ttu-id="da5f3-113">Все отправленные пакеты также будут циклически возвращаться.</span><span class="sxs-lookup"><span data-stu-id="da5f3-113">All the packets sent out are looped back as well.</span></span> <span data-ttu-id="da5f3-114">Это можно использовать для проверки работоспособности устройств.</span><span class="sxs-lookup"><span data-stu-id="da5f3-114">This can be used to test if the devices are working.</span></span>

<span data-ttu-id="da5f3-115">\_Режим селективного \_ замыкания на себя mm используется для включения нескольких приложений на одном компьютере для приподключения к одной группе многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="da5f3-115">The MM\_SELECTIVE\_LOOPBACK mode is used to enable multiple applications on one machine to join the same multicast group.</span></span> <span data-ttu-id="da5f3-116">Пакеты передаются обратно из стека, и каждый сеанс RTP отвечает за фильтрацию ненужных пакетов.</span><span class="sxs-lookup"><span data-stu-id="da5f3-116">The packets are looped back from the stack, and each RTP session is responsible for filtering out unwanted packets.</span></span>

## <a name="members"></a><span data-ttu-id="da5f3-117">Элементы</span><span class="sxs-lookup"><span data-stu-id="da5f3-117">Members</span></span>

<span data-ttu-id="da5f3-118">Интерфейс **имултикастконтрол** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="da5f3-118">The **IMulticastControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="da5f3-119">**Имултикастконтрол** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="da5f3-119">**IMulticastControl** also has these types of members:</span></span>

-   [<span data-ttu-id="da5f3-120">Методы</span><span class="sxs-lookup"><span data-stu-id="da5f3-120">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="da5f3-121">Методы</span><span class="sxs-lookup"><span data-stu-id="da5f3-121">Methods</span></span>

<span data-ttu-id="da5f3-122">Интерфейс **имултикастконтрол** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="da5f3-122">The **IMulticastControl** interface has these methods.</span></span>



| <span data-ttu-id="da5f3-123">Метод</span><span class="sxs-lookup"><span data-stu-id="da5f3-123">Method</span></span>                                                          | <span data-ttu-id="da5f3-124">Описание</span><span class="sxs-lookup"><span data-stu-id="da5f3-124">Description</span></span>                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [<span data-ttu-id="da5f3-125">**получить \_ лупбаккмоде**</span><span class="sxs-lookup"><span data-stu-id="da5f3-125">**get\_LoopbackMode**</span></span>](imulticastcontrol-get-loopbackmode.md) | <span data-ttu-id="da5f3-126">Возвращает режим многоадресного замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="da5f3-126">Gets the multicast loopback mode.</span></span><br/> |
| [<span data-ttu-id="da5f3-127">**разместить \_ лупбаккмоде**</span><span class="sxs-lookup"><span data-stu-id="da5f3-127">**put\_LoopbackMode**</span></span>](imulticastcontrol-put-loopbackmode.md) | <span data-ttu-id="da5f3-128">Задает режим многоадресного замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="da5f3-128">Sets the multicast loopback mode.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="da5f3-129">Требования</span><span class="sxs-lookup"><span data-stu-id="da5f3-129">Requirements</span></span>



| <span data-ttu-id="da5f3-130">Требование</span><span class="sxs-lookup"><span data-stu-id="da5f3-130">Requirement</span></span> | <span data-ttu-id="da5f3-131">Значение</span><span class="sxs-lookup"><span data-stu-id="da5f3-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da5f3-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="da5f3-132">TAPI version</span></span><br/> | <span data-ttu-id="da5f3-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="da5f3-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="da5f3-134">Header</span><span class="sxs-lookup"><span data-stu-id="da5f3-134">Header</span></span><br/>       | <dl> <span data-ttu-id="da5f3-135"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="da5f3-135"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="da5f3-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="da5f3-136">Library</span></span><br/>      | <dl> <span data-ttu-id="da5f3-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da5f3-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="da5f3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="da5f3-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="da5f3-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da5f3-139"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="da5f3-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da5f3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da5f3-141">Ипконф MSP</span><span class="sxs-lookup"><span data-stu-id="da5f3-141">IPConf MSP</span></span>](ipconf-msp.md)
</dt> </dl>

 

