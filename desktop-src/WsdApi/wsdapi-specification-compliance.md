---
description: API веб-служб на устройствах (WSDAPI) обеспечивает поддержку профиля устройств для веб-служб (DPWS) в Windows Vista, что позволяет осуществлять обмен данными между компьютерами на базе Windows и подключенными к сети устройствами с помощью веб-служб (WS).
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: Соответствие спецификации WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d915a8f963ff346ad8a8fee8a2188aa69cecb8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264633"
---
# <a name="wsdapi-specification-compliance"></a><span data-ttu-id="fb575-103">Соответствие спецификации WSDAPI</span><span class="sxs-lookup"><span data-stu-id="fb575-103">WSDAPI Specification Compliance</span></span>

<span data-ttu-id="fb575-104">API веб-служб на устройствах (WSDAPI) обеспечивает поддержку [профиля устройств для веб-служб](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) в Windows Vista, что позволяет осуществлять обмен данными между компьютерами на базе Windows и подключенными к сети устройствами с помощью веб-служб (WS).</span><span class="sxs-lookup"><span data-stu-id="fb575-104">Web Services on Devices API (WSDAPI) provides support for the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) on Windows Vista, which enables Web Services (WS) communication between Windows-based PCs and network connected devices.</span></span> <span data-ttu-id="fb575-105">DPWS собирает базовые спецификации WS, такие как [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)и [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), а также повышает или ограничивает их, предоставляющую базовый набор возможностей для устройств с ограниченными ресурсами.</span><span class="sxs-lookup"><span data-stu-id="fb575-105">DPWS assembles basic WS specifications, such as [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf), and [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), and enhances or constrains them to provide a baseline set of capabilities for resource-constrained devices.</span></span> <span data-ttu-id="fb575-106">Эта спецификация базовых показателей содержит необходимые функции, такие как возможность описания свойств устройства с помощью метаданных, а также дополнительные функциональные возможности, например возможность отклонять определенные сообщения по соображениям безопасности.</span><span class="sxs-lookup"><span data-stu-id="fb575-106">This baseline specification contains required functionality, such as the ability to describe properties of the device through metadata, and optional functionality, such as the ability to reject specific messages for security reasons.</span></span>

<span data-ttu-id="fb575-107">Реализация WSDAPI в Windows Vista является первым выпуском явной поддержки DPWS, а является неуправляемой реализацией DPWS, которая отличается от других реализаций веб-служб (таких как [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) или [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).</span><span class="sxs-lookup"><span data-stu-id="fb575-107">The WSDAPI implementation in Windows Vista is the first release of explicit support for the DPWS, and is an unmanaged implementation of DPWS that is separate and distinct from other Web Services implementations (such as the [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) or [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).</span></span>

<span data-ttu-id="fb575-108">Следующие разделы представляют интерес для изготовителей устройств и других разработчиков устройств, которые создают устройства, взаимодействующие с клиентами и узлами WSDAPI на основе Windows, без использования WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="fb575-108">The following topics are of interest to device manufacturers and other device implementers that create devices that interoperate with Windows-based WSDAPI clients and hosts without using WSDAPI.</span></span> <span data-ttu-id="fb575-109">В этих разделах описывается реализация WSDAPI относительно базовых спецификаций.</span><span class="sxs-lookup"><span data-stu-id="fb575-109">These topics describe the implementation of WSDAPI relative to the underlying specifications.</span></span> <span data-ttu-id="fb575-110">Они охватывают реализацию требуемых функций, дополнительные функциональные возможности и дополнительные функциональные возможности, не определенные в спецификации.</span><span class="sxs-lookup"><span data-stu-id="fb575-110">They cover the implementation of required functionality, optional functionality, and additional functionality not defined in the specification.</span></span>

-   [<span data-ttu-id="fb575-111">Соответствие спецификации DPWS</span><span class="sxs-lookup"><span data-stu-id="fb575-111">DPWS Specification Compliance</span></span>](dpws-specification-compliance.md)
-   [<span data-ttu-id="fb575-112">Соответствие спецификации WS-Discovery</span><span class="sxs-lookup"><span data-stu-id="fb575-112">WS-Discovery Specification Compliance</span></span>](ws-discovery-specification-compliance.md)
-   [<span data-ttu-id="fb575-113">Соответствие спецификации WS-MetadataExchange и WS-Transfer</span><span class="sxs-lookup"><span data-stu-id="fb575-113">WS-MetadataExchange and WS-Transfer Specification Compliance</span></span>](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [<span data-ttu-id="fb575-114">Дополнительные функции WS-Discovery</span><span class="sxs-lookup"><span data-stu-id="fb575-114">Additional WS-Discovery Functionality</span></span>](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a><span data-ttu-id="fb575-115">См. также</span><span class="sxs-lookup"><span data-stu-id="fb575-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb575-116">Разработка устройств WSD</span><span class="sxs-lookup"><span data-stu-id="fb575-116">WSD Device Development</span></span>](wsd-device-development.md)
</dt> <dt>

[<span data-ttu-id="fb575-117">Рекомендации по реализации устройств WSD</span><span class="sxs-lookup"><span data-stu-id="fb575-117">WSD Device Implementation Recommendations</span></span>](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
