---
title: Новые возможности API-интерфейсов UPnP
description: API-интерфейсы™ UPnP имеют новые возможности и обновленную документацию по Windows XP SP2. В следующей таблице приведены сведения о новой документации.
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27747c6185b5aecea86e240d388ab10410aa29f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779886"
---
# <a name="whats-new-in-the-upnp-apis"></a><span data-ttu-id="e06ec-104">Новые возможности API-интерфейсов UPnP</span><span class="sxs-lookup"><span data-stu-id="e06ec-104">What's New in the UPnP APIs</span></span>

<span data-ttu-id="e06ec-105">API-интерфейсы™ UPnP имеют новые возможности и обновленную документацию по Windows XP SP2.</span><span class="sxs-lookup"><span data-stu-id="e06ec-105">The UPnP™ APIs have new features and updated documentation for Windows XP SP2.</span></span> <span data-ttu-id="e06ec-106">В следующей таблице приведены сведения о новой документации.</span><span class="sxs-lookup"><span data-stu-id="e06ec-106">The following table identifies the new documentation.</span></span>



| <span data-ttu-id="e06ec-107">Функция</span><span class="sxs-lookup"><span data-stu-id="e06ec-107">Feature</span></span>                                                          | <span data-ttu-id="e06ec-108">Описание</span><span class="sxs-lookup"><span data-stu-id="e06ec-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e06ec-109">**иупнпремотиндпоинтинфо**</span><span class="sxs-lookup"><span data-stu-id="e06ec-109">**IUPnPRemoteEndpointInfo**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | <span data-ttu-id="e06ec-110">Этот новый интерфейс позволяет размещенному устройству получать сведения об инициаторе запроса (то есть контрольной точке) и запросе.</span><span class="sxs-lookup"><span data-stu-id="e06ec-110">This new interface allows a hosted device to obtain information about a requester (that is, a control point) and the request.</span></span> <span data-ttu-id="e06ec-111">Он включает три метода, каждый из которых предоставляет разный тип информации.</span><span class="sxs-lookup"><span data-stu-id="e06ec-111">It includes three methods, each of which provides a different type of information.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="e06ec-112">Реализация поведения устройства</span><span class="sxs-lookup"><span data-stu-id="e06ec-112">Implementing Device Behavior</span></span>](implementing-device-behavior.md) | <span data-ttu-id="e06ec-113">Этот раздел содержит новый раздел, в котором объясняется, как получить сведения о конечной точке с помощью нового интерфейса [**иупнпремотиндпоинтинфо**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) .</span><span class="sxs-lookup"><span data-stu-id="e06ec-113">This topic includes a new section that explains how to obtain endpoint information by using the new [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) interface.</span></span>                                                                                                                                                                                                     |
| [<span data-ttu-id="e06ec-114">Параметры конфигурации</span><span class="sxs-lookup"><span data-stu-id="e06ec-114">Configuration Settings</span></span>](configuration-settings.md)             | <span data-ttu-id="e06ec-115">Этот новый раздел содержит сведения о параметрах реестра, влияющих на поведение API-интерфейсов UPnP.</span><span class="sxs-lookup"><span data-stu-id="e06ec-115">This new topic provides information about the registry settings that affect the behavior of the UPnP APIs.</span></span>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="e06ec-116">Коды ошибок устройства</span><span class="sxs-lookup"><span data-stu-id="e06ec-116">Device Error Codes</span></span>](device-error-codes.md)                     | <span data-ttu-id="e06ec-117">В этом новом разделе объясняется, как код ошибки из устройства преобразуется в значение HRESULT и наоборот.</span><span class="sxs-lookup"><span data-stu-id="e06ec-117">This new topic explains how an error code from a device is converted to an HRESULT value and vice versa.</span></span> <span data-ttu-id="e06ec-118">Понимание этого процесса необходимо для того, чтобы оценить значение HRESULT, возвращаемое методами [**иупнпсервице:: инвокеактион**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) и [**Иупнпсервице:: куеристатевариабле**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) .</span><span class="sxs-lookup"><span data-stu-id="e06ec-118">An understanding of this process is necessary in order to evaluate an HRESULT value that is returned by the [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) and [**IUPnPService::QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) methods.</span></span> |



 

 

 




