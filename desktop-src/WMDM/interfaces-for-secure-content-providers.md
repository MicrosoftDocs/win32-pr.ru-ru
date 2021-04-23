---
title: Интерфейсы для поставщиков защищенного содержимого
description: Интерфейсы для поставщиков защищенного содержимого
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Диспетчер устройств Windows Media, содержимое, защищенное с использованием DRM
- Диспетчер устройств, содержимое, защищенное с использованием DRM
- Справочник по программированию, содержимое, защищенное с использованием DRM
- Справочник по диспетчер устройств Windows Media, содержимому, защищенному с использованием DRM
- Содержимое, защищенное DRM
- Диспетчер устройств Windows Media, поставщик защищенного содержимого (SCP)
- Диспетчер устройств, поставщик защищенного содержимого (SCP)
- Справочник по программированию, поставщик защищенного содержимого (SCP)
- Справочник по диспетчер устройств Windows Media, поставщику защищенного содержимого (SCP)
- Поставщик защищенного содержимого (SCP)
- SCP (поставщик защищенного содержимого)
- Диспетчер устройств Windows Media, интерфейсы SCP
- Диспетчер устройств, интерфейсы SCP
- Справочник по программированию, интерфейсы SCP
- Справочник по диспетчер устройств Windows Media, интерфейсам SCP
- Интерфейсы SCP, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e4483a5bfb62e165b1bc17e588dfe3bd5b73f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691244"
---
# <a name="interfaces-for-secure-content-providers"></a><span data-ttu-id="23b4a-119">Интерфейсы для поставщиков защищенного содержимого</span><span class="sxs-lookup"><span data-stu-id="23b4a-119">Interfaces for Secure Content Providers</span></span>

<span data-ttu-id="23b4a-120">Защищенный поставщик содержимого (SCP) — это подключаемый компонент, который позволяет диспетчер устройств Windows Media передавать и запрашивать сведения о правах из содержимого, защищенного с помощью DRM.</span><span class="sxs-lookup"><span data-stu-id="23b4a-120">A secure content provider (SCP) is a plug-in component that enables Windows Media Device Manager to transfer and request rights information from DRM-protected content.</span></span> <span data-ttu-id="23b4a-121">Корпорация Майкрософт предоставляет компонент SCP, который может работать с файлами WMA и WMV, защищенными с помощью DRM.</span><span class="sxs-lookup"><span data-stu-id="23b4a-121">Microsoft provides an SCP component that can handle DRM-protected WMA and WMV files.</span></span> <span data-ttu-id="23b4a-122">Если устройство или приложение будет использовать содержимое других форматов, защищенное с помощью DRM, необходимо создать компонент SCP, реализовав все эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="23b4a-122">If your device or application will use DRM-protected content of other formats, it should create an SCP component by implementing all of these interfaces.</span></span> <span data-ttu-id="23b4a-123">В противном случае использовать эти интерфейсы будет необязательно.</span><span class="sxs-lookup"><span data-stu-id="23b4a-123">Otherwise, you will not need to use these interfaces.</span></span>



| <span data-ttu-id="23b4a-124">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="23b4a-124">Interface</span></span>                                                  | <span data-ttu-id="23b4a-125">Описание</span><span class="sxs-lookup"><span data-stu-id="23b4a-125">Description</span></span>                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23b4a-126">**искпсекуреаусентикате**</span><span class="sxs-lookup"><span data-stu-id="23b4a-126">**ISCPSecureAuthenticate**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | <span data-ttu-id="23b4a-127">Основной интерфейс поставщика безопасного содержимого.</span><span class="sxs-lookup"><span data-stu-id="23b4a-127">The primary interface of the secure content provider.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="23b4a-128">**ISCPSecureAuthenticate2**</span><span class="sxs-lookup"><span data-stu-id="23b4a-128">**ISCPSecureAuthenticate2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | <span data-ttu-id="23b4a-129">Расширяет **искпсекуреаусентикате** , предоставляя способ получения объекта сеанса.</span><span class="sxs-lookup"><span data-stu-id="23b4a-129">Extends **ISCPSecureAuthenticate** by providing a way to get a session object.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="23b4a-130">**искпсекуриксчанже**</span><span class="sxs-lookup"><span data-stu-id="23b4a-130">**ISCPSecureExchange**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | <span data-ttu-id="23b4a-131">Используется для обмена защищенным содержимым и правами, связанными с содержимым.</span><span class="sxs-lookup"><span data-stu-id="23b4a-131">Used to exchange secured content and rights associated with content.</span></span>                                                                                                                                                                                 |
| [<span data-ttu-id="23b4a-132">**ISCPSecureExchange2**</span><span class="sxs-lookup"><span data-stu-id="23b4a-132">**ISCPSecureExchange2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | <span data-ttu-id="23b4a-133">Расширяет **искпсекуриксчанже** , предоставляя новую версию метода **трансферконтаинердата** .</span><span class="sxs-lookup"><span data-stu-id="23b4a-133">Extends **ISCPSecureExchange** by providing a new version of the **TransferContainerData** method.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="23b4a-134">**ISCPSecureExchange3**</span><span class="sxs-lookup"><span data-stu-id="23b4a-134">**ISCPSecureExchange3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | <span data-ttu-id="23b4a-135">Расширяет **ISCPSecureExchange2** , предоставляя улучшенную производительность обмена данными и метод обратного вызова для завершения перемещения.</span><span class="sxs-lookup"><span data-stu-id="23b4a-135">Extends **ISCPSecureExchange2** by providing improved data exchange performance, and a transfer complete callback method.</span></span>                                                                                                                            |
| [<span data-ttu-id="23b4a-136">**искпсекурекуери**</span><span class="sxs-lookup"><span data-stu-id="23b4a-136">**ISCPSecureQuery**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | <span data-ttu-id="23b4a-137">Запрашивается диспетчер устройств Windows Media для определения принадлежности защищенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="23b4a-137">Queried by Windows Media Device Manager to determine ownership of secured content.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="23b4a-138">**ISCPSecureQuery2**</span><span class="sxs-lookup"><span data-stu-id="23b4a-138">**ISCPSecureQuery2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | <span data-ttu-id="23b4a-139">Расширяет **искпсекурекуери** с помощью функций, определяющих, отвечает ли поставщик защищенного содержимого содержимому, и, если это так, предоставление URL-адреса для обновления отозванных компонентов и определение того, какие компоненты были отозваны.</span><span class="sxs-lookup"><span data-stu-id="23b4a-139">Extends **ISCPSecureQuery** through functionality that determines whether the secure content provider is responsible for the content, and if so, providing a URL for updating revoked components and determining which components have been revoked.</span></span> |
| [<span data-ttu-id="23b4a-140">**ISCPSecureQuery3**</span><span class="sxs-lookup"><span data-stu-id="23b4a-140">**ISCPSecureQuery3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | <span data-ttu-id="23b4a-141">Расширяет **ISCPSecureQuery2** , предоставляя набор новых методов для получения прав и принятия решения по четкому каналу.</span><span class="sxs-lookup"><span data-stu-id="23b4a-141">Extends **ISCPSecureQuery2** by providing a set of new methods for retrieving the rights and making decision on a clear channel.</span></span>                                                                                                                     |
| [<span data-ttu-id="23b4a-142">**искпсессион**</span><span class="sxs-lookup"><span data-stu-id="23b4a-142">**ISCPSession**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | <span data-ttu-id="23b4a-143">Обеспечивает эффективное управление состоянием для нескольких операций.</span><span class="sxs-lookup"><span data-stu-id="23b4a-143">Provides efficient common state management for multiple operations.</span></span>                                                                                                                                                                                  |



 

 

 




