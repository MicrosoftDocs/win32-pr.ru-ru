---
description: TAPI 3 поддерживает интеграцию интерфейсов, зависящих от поставщика услуг, к стандартным объектам, что позволяет приложениям использовать преимущества функций конкретного поставщика.
ms.assetid: 8077c9a7-3235-41a7-97dc-ca5f3c291ee6
title: Интерфейсы Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f95499f005c8c3b3e854f33835b9c9b183416d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081316"
---
# <a name="provider-specific-interfaces"></a><span data-ttu-id="48132-103">Интерфейсы Provider-Specific</span><span class="sxs-lookup"><span data-stu-id="48132-103">Provider-Specific Interfaces</span></span>

<span data-ttu-id="48132-104">TAPI 3 поддерживает интеграцию интерфейсов, зависящих от поставщика услуг, к стандартным объектам, что позволяет приложениям использовать преимущества функций конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="48132-104">TAPI 3 supports integration of service provider-specific interfaces into the standard objects, allowing applications to take advantage of provider-specific functionality.</span></span> <span data-ttu-id="48132-105">Кроме того, TAPI 3 позволяет поставщикам услуг предоставлять приложениям зависящие от поставщика события в виде COM-объектов через тот же интерфейс, в котором приложение получает стандартные события.</span><span class="sxs-lookup"><span data-stu-id="48132-105">Additionally, TAPI 3 allows service providers to deliver vendor-specific events to applications as COM objects over the same interface on which the application receives standard events.</span></span>

<span data-ttu-id="48132-106">TAPI достигает этой интеграции, объединяя зависящие от поставщика объекты со стандартными объектами: TAPI, адрес, терминал, вызов и Каллхуб, а также диспетчеризации или делегируя неизвестные методы этим объектам конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="48132-106">TAPI achieves this integration by aggregating provider-specific objects with the standard objects – TAPI, Address, Terminal, Call, and CallHub – and dispatching or delegating unknown methods to these provider-specific objects.</span></span>

<span data-ttu-id="48132-107">Например, поставщик услуг может позволить приложениям получать сведения о вызове, помимо того, что предоставляется интерфейсом [**иткаллинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="48132-107">For example, a service provider may allow applications to obtain information about a call beyond what is exposed by the [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) interface.</span></span> <span data-ttu-id="48132-108">Поставщик должен определить интерфейс, позволяющий приложениям выполнять эти дополнительные запросы и реализовывать этот интерфейс для объекта.</span><span class="sxs-lookup"><span data-stu-id="48132-108">The vendor must define an interface that allows applications to make these extra queries and implement that interface on an object.</span></span> <span data-ttu-id="48132-109">Этот объект также реализует интерфейс запроса сведений о поставщике, чтобы приложение могло определить, какие виды функций, зависящих от поставщика, могут быть доступны.</span><span class="sxs-lookup"><span data-stu-id="48132-109">This object also implements a vendor information-querying interface so that an application can discover what sorts of provider-specific functions might be available.</span></span>

<span data-ttu-id="48132-110">Когда приложение получает ссылку на объект вызова, приложение может использовать новый интерфейс, зависящий от поставщика, и его методы, как если бы они были реализованы самим объектом Call.</span><span class="sxs-lookup"><span data-stu-id="48132-110">When the application obtains a reference to a call object, the application can use the new provider-specific interface and its methods as if they were implemented by the call object itself.</span></span>

<span data-ttu-id="48132-111">Список всех стандартных интерфейсов MSP см. в [справочнике по интерфейсу поставщика служб мультимедиа (мспи)](media-service-provider-interface-mspi-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="48132-111">See [Media Service Provider Interface (MSPI) Reference](media-service-provider-interface-mspi-reference.md) for a list of all standard MSP interfaces.</span></span>

<span data-ttu-id="48132-112">Список всех интерфейсов, относящихся к Ипконф MSP, см. в разделе [интерфейсы MSP ипконф](ipconf-msp-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="48132-112">See [IPConf MSP Interfaces](ipconf-msp-interfaces.md) for a list of all interfaces specific to the IPConf MSP.</span></span>

 

 



