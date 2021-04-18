---
title: Справочник по API узла устройства
description: Следующие интерфейсы являются частью API узла устройства с технологией UPnP. Узел устройства с технологией UPnP поддерживает Microsoft Visual Basic и C++.
ms.assetid: 48e20a09-7e78-4b8d-aa16-78751b6fb586
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62f42b43efcc1d51eb5e5581770260238640469
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411198"
---
# <a name="device-host-api-reference"></a><span data-ttu-id="e9bf1-104">Справочник по API узла устройства</span><span class="sxs-lookup"><span data-stu-id="e9bf1-104">Device Host API Reference</span></span>

<span data-ttu-id="e9bf1-105">Следующие интерфейсы являются частью API узла устройства с технологией UPnP.</span><span class="sxs-lookup"><span data-stu-id="e9bf1-105">The following interfaces are part of the Device Host API with UPnP technology.</span></span> <span data-ttu-id="e9bf1-106">Узел устройства с технологией UPnP поддерживает Microsoft Visual Basic и C++.</span><span class="sxs-lookup"><span data-stu-id="e9bf1-106">The Device Host with UPnP technology supports Microsoft Visual Basic and C++.</span></span>

<span data-ttu-id="e9bf1-107">Этот API не обеспечивает поддержку Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="e9bf1-107">This API does not provide support for Microsoft Visual Basic Scripting Edition (VBScript).</span></span>



| <span data-ttu-id="e9bf1-108">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="e9bf1-108">Interface</span></span>                                                  | <span data-ttu-id="e9bf1-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e9bf1-109">Description</span></span>                                                                                         |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9bf1-110">**иупнпдевицеконтрол**</span><span class="sxs-lookup"><span data-stu-id="e9bf1-110">**IUPnPDeviceControl**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol)           | <span data-ttu-id="e9bf1-111">Используется узлом устройства для управления устройствами и связанными службами.</span><span class="sxs-lookup"><span data-stu-id="e9bf1-111">Used by the device host to manage devices and related services.</span></span>                                     |
| [<span data-ttu-id="e9bf1-112">**иупнпдевицепровидер**</span><span class="sxs-lookup"><span data-stu-id="e9bf1-112">**IUPnPDeviceProvider**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider)         | <span data-ttu-id="e9bf1-113">Используется узлом устройства для запуска и завершения поставщиков устройств.</span><span class="sxs-lookup"><span data-stu-id="e9bf1-113">Used by the device host to start and stop device providers.</span></span>                                         |
| [<span data-ttu-id="e9bf1-114">**иупнпевентсинк**</span><span class="sxs-lookup"><span data-stu-id="e9bf1-114">**IUPnPEventSink**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink)                   | <span data-ttu-id="e9bf1-115">Используется устройствами для отправки уведомлений о событиях на узел устройства.</span><span class="sxs-lookup"><span data-stu-id="e9bf1-115">Used by devices to send event notifications to the device host.</span></span>                                     |
| [<span data-ttu-id="e9bf1-116">**иупнпевентсаурце**</span><span class="sxs-lookup"><span data-stu-id="e9bf1-116">**IUPnPEventSource**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource)               | <span data-ttu-id="e9bf1-117">Используется узлом устройства для подписки на события, предоставляемых размещенной службой, и отмены подписки на них.</span><span class="sxs-lookup"><span data-stu-id="e9bf1-117">Used by the device host to subscribe or unsubscribe to events provided by the hosted service.</span></span>       |
| [<span data-ttu-id="e9bf1-118">**иупнпрегистрар**</span><span class="sxs-lookup"><span data-stu-id="e9bf1-118">**IUPnPRegistrar**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar)                   | <span data-ttu-id="e9bf1-119">Используется устройствами для регистрации на узле устройства.</span><span class="sxs-lookup"><span data-stu-id="e9bf1-119">Used by devices to register with the device host.</span></span>                                                   |
| [<span data-ttu-id="e9bf1-120">**иупнпремотиндпоинтинфо**</span><span class="sxs-lookup"><span data-stu-id="e9bf1-120">**IUPnPRemoteEndpointInfo**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) | <span data-ttu-id="e9bf1-121">Используется устройствами для получения сведений об инициаторе запроса (то есть контрольной точке) и запросе.</span><span class="sxs-lookup"><span data-stu-id="e9bf1-121">Used by devices to obtain information about a requester (that is, a control point) and the request.</span></span> |
| [<span data-ttu-id="e9bf1-122">**иупнпререгистрар**</span><span class="sxs-lookup"><span data-stu-id="e9bf1-122">**IUPnPReregistrar**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)               | <span data-ttu-id="e9bf1-123">Используется устройствами для повторной регистрации на узле устройства.</span><span class="sxs-lookup"><span data-stu-id="e9bf1-123">Used by devices to re-register with the device host.</span></span>                                                |



 

 

 




