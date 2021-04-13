---
title: Справочник по ВМДМ
description: Справочник по программированию
ms.assetid: 1d2260a8-bc9f-41b3-a3b0-0176b45fff1f
keywords:
- Диспетчер устройств Windows Media, Справочник по программированию
- Диспетчер устройств, Справочник по программированию
- Windows Media диспетчер устройств, классические приложения
- Диспетчер устройств, классические приложения
- Диспетчер устройств Windows Media, поставщики услуг
- Диспетчер устройств, поставщики услуг
- Классические приложения, Справочник по программированию
- поставщики услуг, Справочник по программированию
- Справочник по программированию, классические приложения
- Справочник по программированию, поставщики услуг
- Справочник по программированию, Windows Media диспетчер устройств
- Справочник по диспетчер устройств Windows Media, о
- Справочник по диспетчер устройств Windows Media, классических приложениях
- Справочник по диспетчер устройств Windows Media, поставщикам услуг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1498d42e65de99abc1d32895f3628d93502c70f
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104412267"
---
# <a name="wmdm-reference"></a><span data-ttu-id="e0e90-117">Справочник по ВМДМ</span><span class="sxs-lookup"><span data-stu-id="e0e90-117">WMDM reference</span></span>

<span data-ttu-id="e0e90-118">Пакет Windows Media диспетчер устройств SDK состоит из коллекции интерфейсов, структур, перечислений и констант.</span><span class="sxs-lookup"><span data-stu-id="e0e90-118">The Windows Media Device Manager SDK consists of a collection of interfaces, structures, enumerations, and constants.</span></span> <span data-ttu-id="e0e90-119">В разделе Reference интерфейсы разбиваются на группы в соответствии с типом объекта, который их использует.</span><span class="sxs-lookup"><span data-stu-id="e0e90-119">The reference section divides the interfaces into groups according to the type of object that uses them.</span></span>



| <span data-ttu-id="e0e90-120">Section</span><span class="sxs-lookup"><span data-stu-id="e0e90-120">Section</span></span>                                                                                                    | <span data-ttu-id="e0e90-121">Описание</span><span class="sxs-lookup"><span data-stu-id="e0e90-121">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0e90-122">Интерфейсы для приложений</span><span class="sxs-lookup"><span data-stu-id="e0e90-122">Interfaces for Applications</span></span>](interfaces-for-applications.md)                                             | <span data-ttu-id="e0e90-123">Описывает интерфейсы, которые используются или реализуются только приложениями для настольных систем, подключаемых модулей проигрывателя Windows Media или COM-объектами, которым требуется высокоуровневый доступ к портативному устройству.</span><span class="sxs-lookup"><span data-stu-id="e0e90-123">Describes interfaces that are used or implemented only by desktop applications, Windows Media Player plug-ins, or COM objects that need high-level access to a portable device.</span></span>                     |
| [<span data-ttu-id="e0e90-124">Интерфейсы для поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="e0e90-124">Interfaces for Service Providers</span></span>](interfaces-for-service-providers.md)                                   | <span data-ttu-id="e0e90-125">Описание интерфейсов, которые используются или реализуются только поставщиками служб, которые обрабатывают фактическое взаимодействие низкого уровня с портативным устройством.</span><span class="sxs-lookup"><span data-stu-id="e0e90-125">Describes interfaces that are used or implemented only by service providers, which handle the actual low-level communication with a portable device.</span></span>                                                |
| [<span data-ttu-id="e0e90-126">Интерфейсы DRM-Implemented Windows Media</span><span class="sxs-lookup"><span data-stu-id="e0e90-126">Windows Media DRM-Implemented Interfaces</span></span>](windows-media-drm-implemented-interfaces.md)                   | <span data-ttu-id="e0e90-127">Описывает интерфейсы, которые не предназначены для реализации сторонними поставщиками услуг, но реализуются и вызываются внутри Windows Media DRM и Windows Media диспетчер устройств.</span><span class="sxs-lookup"><span data-stu-id="e0e90-127">Describes interfaces that are not intended to be implemented by third-party service providers, but are implemented and called internally by the Windows Media DRM and Windows Media Device Manager.</span></span> |
| [<span data-ttu-id="e0e90-128">Интерфейсы для поставщиков служб и приложений</span><span class="sxs-lookup"><span data-stu-id="e0e90-128">Interfaces for Service Providers and Applications</span></span>](interfaces-for-service-providers-and-applications.md) | <span data-ttu-id="e0e90-129">Описывает интерфейсы, которые могут использоваться приложениями или поставщиками служб.</span><span class="sxs-lookup"><span data-stu-id="e0e90-129">Describes interfaces that can be used either by applications or by service providers.</span></span>                                                                                                               |
| [<span data-ttu-id="e0e90-130">Интерфейсы для поставщиков защищенного содержимого</span><span class="sxs-lookup"><span data-stu-id="e0e90-130">Interfaces for Secure Content Providers</span></span>](interfaces-for-secure-content-providers.md)                     | <span data-ttu-id="e0e90-131">Описывает интерфейсы, которые должны быть реализованы устройством или приложением, которое будет использовать содержимое, защищенное с помощью DRM.</span><span class="sxs-lookup"><span data-stu-id="e0e90-131">Describes interfaces that must be implemented by a device or application that will use DRM-protected content.</span></span>                                                                                       |
| [<span data-ttu-id="e0e90-132">Структуры</span><span class="sxs-lookup"><span data-stu-id="e0e90-132">Structures</span></span>](structures.md)                                                                               | <span data-ttu-id="e0e90-133">Описывает структуры, используемые для методов диспетчер устройств Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e0e90-133">Describes structures used for Windows Media Device Manager methods.</span></span>                                                                                                                                 |
| [<span data-ttu-id="e0e90-134">Типы перечислений</span><span class="sxs-lookup"><span data-stu-id="e0e90-134">Enumeration Types</span></span>](enumeration-types.md)                                                                 | <span data-ttu-id="e0e90-135">Описывает перечисления, используемые для методов диспетчер устройств Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e0e90-135">Describes enumerations used for Windows Media Device Manager methods.</span></span>                                                                                                                               |
| [<span data-ttu-id="e0e90-136">Константы метаданных</span><span class="sxs-lookup"><span data-stu-id="e0e90-136">Metadata Constants</span></span>](metadata-constants.md)                                                               | <span data-ttu-id="e0e90-137">Описывает константы, определенные с помощью пакета SDK Windows Media диспетчер устройств для настройки или получения различных свойств метаданных для устройства или объекта на устройстве.</span><span class="sxs-lookup"><span data-stu-id="e0e90-137">Describes the constants defined by the Windows Media Device Manager SDK for setting or retrieving various metadata properties for a device or object on the device.</span></span>                                 |
| [<span data-ttu-id="e0e90-138">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="e0e90-138">Error Codes</span></span>](error-codes.md)                                                                             | <span data-ttu-id="e0e90-139">Описание кодов ошибок, которые могут возвращаться методами Windows Media диспетчер устройств SDK.</span><span class="sxs-lookup"><span data-stu-id="e0e90-139">Describes the error codes that can be returned by Windows Media Device Manager SDK methods.</span></span>                                                                                                         |



 

 

 




