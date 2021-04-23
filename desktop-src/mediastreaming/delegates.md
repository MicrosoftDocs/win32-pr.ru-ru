---
title: Делегаты
description: API потоковой передачи мультимедиа предоставляет следующие функции обработчика событий.
ms.assetid: CDE7B829-D0D1-479D-9B35-4445E711AF58
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23fbf0f44a0822fd0c8914833b0696fcb9aacad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533128"
---
# <a name="delegates"></a><span data-ttu-id="b1288-103">Делегаты</span><span class="sxs-lookup"><span data-stu-id="b1288-103">Delegates</span></span>

<span data-ttu-id="b1288-104">[API потоковой передачи мультимедиа](media-streaming-api-portal.md) предоставляет следующие функции обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="b1288-104">The [Media Streaming API](media-streaming-api-portal.md) provides the following event handler functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b1288-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="b1288-105">In this section</span></span>



| <span data-ttu-id="b1288-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="b1288-106">Topic</span></span>                                                                                   | <span data-ttu-id="b1288-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b1288-107">Description</span></span>                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1288-108">[**коннектионстатушандлер**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b1288-108">[**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))</span></span><br/>                   | <span data-ttu-id="b1288-109">Представляет функцию, которая будет выполнять обработку события [**коннектионстатусчанжед**](connectionstatuschanged.md) , которое уведомляет клиента об изменениях в состоянии сетевого подключения устройства s.</span><span class="sxs-lookup"><span data-stu-id="b1288-109">Represents the function that will handle the [**ConnectionStatusChanged**](connectionstatuschanged.md) event which notifies the client of changes in the device s network connection status.</span></span><br/>               |
| <span data-ttu-id="b1288-110">[**девицеконтроллерфиндерхандлер**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b1288-110">[**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))</span></span><br/>       | <span data-ttu-id="b1288-111">Представляет функцию, которая будет выполнять обработку событий [**девицеарривал**](devicearrival.md) и [**девицедепартуре**](devicedeparture.md) , которые уведомляют клиента об изменениях в списке кэшированных устройств.</span><span class="sxs-lookup"><span data-stu-id="b1288-111">Represents the function that will handle the [**DeviceArrival**](devicearrival.md) and [**DeviceDeparture**](devicedeparture.md) events which notify the client of changes in the list of cached devices.</span></span><br/> |
| <span data-ttu-id="b1288-112">[**рендерингпараметерсупдатехандлер**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b1288-112">[**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))</span></span><br/> | <span data-ttu-id="b1288-113">Представляет функцию, которая будет выполнять обработку события [**рендерингпараметерсупдате**](renderingparametersupdate.md) , которое уведомляет клиента об обновлении с любыми параметрами элемента управления отрисовки ДМР.</span><span class="sxs-lookup"><span data-stu-id="b1288-113">Represents the function that will handle the [**RenderingParametersUpdate**](renderingparametersupdate.md) event which notifies the client of an update to any of the DMR s rendering control parameters.</span></span><br/>  |
| <span data-ttu-id="b1288-114">[**транспортпараметерсупдатехандлер**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b1288-114">[**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))</span></span><br/> | <span data-ttu-id="b1288-115">Представляет функцию, которая будет выполнять обработку события [**транспортпараметерсупдате**](transportparametersupdate.md) , которое уведомляет клиента об обновлении с любыми транспортными параметрами ДМР s.</span><span class="sxs-lookup"><span data-stu-id="b1288-115">Represents the function that will handle the [**TransportParametersUpdate**](transportparametersupdate.md) event which notifies the client of an update to any of the DMR s transport parameters.</span></span><br/>          |



 

 

