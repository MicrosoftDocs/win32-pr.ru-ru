---
description: Поставщик услуг мультимедиа (MSP) TAPI 3 позволяет приложению значительно управлять носителем для конкретного транспортного механизма.
ms.assetid: 2dd1268f-b31a-443b-a36b-05c1570e7a8a
title: Сведения о поставщике службы мультимедиа (MSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ef4d19a2f01c047d5fc2afd4a0323d7908fcac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104156999"
---
# <a name="about-the-media-service-provider-msp"></a><span data-ttu-id="a81ae-103">Сведения о поставщике службы мультимедиа (MSP)</span><span class="sxs-lookup"><span data-stu-id="a81ae-103">About the Media Service Provider (MSP)</span></span>

<span data-ttu-id="a81ae-104">Поставщик услуг мультимедиа (MSP) TAPI 3 позволяет приложению значительно управлять носителем для конкретного транспортного механизма.</span><span class="sxs-lookup"><span data-stu-id="a81ae-104">A TAPI 3 media service provider (MSP) allows an application considerable control over the media for a particular transport mechanism.</span></span> <span data-ttu-id="a81ae-105">MSP всегда существует в паре с поставщиком услуг телефонии (TSP).</span><span class="sxs-lookup"><span data-stu-id="a81ae-105">An MSP always exists paired with a Telephony Service Provider (TSP).</span></span> <span data-ttu-id="a81ae-106">Так же как TSP — это уровень абстракции для управления вызовами, носитель элементов управления MSP не нуждается в написании кода для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="a81ae-106">Just as a TSP is an abstraction layer for call control, the MSP controls media without need for device-specific coding.</span></span> <span data-ttu-id="a81ae-107">Пример обмена данными по протоколу MSP/TSP см. в разделе [Общие сведения о поставщике услуг TAPI](./tapi-service-provider-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a81ae-107">For an example of MSP/TSP communication, see [TAPI Service Provider Overview](./tapi-service-provider-overview.md).</span></span>

<span data-ttu-id="a81ae-108">MSP обеспечивает управление носителями с помощью специальных интерфейсов терминала, потоков и подпотоков, определенных TAPI.</span><span class="sxs-lookup"><span data-stu-id="a81ae-108">An MSP enables media control through the use of special terminal, stream, and substream interfaces defined by TAPI.</span></span> <span data-ttu-id="a81ae-109">На схеме в статье [о вызовах и элементах управления мультимедиа](about-call-and-media-controls.md) показано, как эти интерфейсы отображаются в приложении TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="a81ae-109">The diagram in [About Call and Media Controls](about-call-and-media-controls.md) illustrates how these interfaces appear to a TAPI 3 application.</span></span>

<span data-ttu-id="a81ae-110">Кроме того, MSP может реализовывать частные [интерфейсы, зависящие от поставщика](provider-specific-interfaces.md), которые TAPI будет объединять в стандартные объекты, предоставляемые приложению.</span><span class="sxs-lookup"><span data-stu-id="a81ae-110">In addition, an MSP may implement private [provider-specific interfaces](provider-specific-interfaces.md), which TAPI will aggregate onto the standard objects exposed to an application.</span></span> <span data-ttu-id="a81ae-111">Например, Microsoft Ипконф MSP, который устанавливается вместе с Microsoft Windows 2000, реализует интерфейс [**итпартиЦипант**](itparticipant.md) , который предоставляет элементы управления для отдельных участников Конференции.</span><span class="sxs-lookup"><span data-stu-id="a81ae-111">For example, the Microsoft IPConf MSP, which is installed with Microsoft Windows 2000, implements the [**ITParticipant**](itparticipant.md) interface, which provides controls for individual members of a conference.</span></span>

<span data-ttu-id="a81ae-112">В следующем разделе кратко описаны MSP, которые могут быть установлены с помощью операционной системы Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a81ae-112">The following topic briefly describes the MSPs that may be installed with a Microsoft operating system.</span></span> <span data-ttu-id="a81ae-113">Дополнительные сведения о конфигурации и использовании см. в наборе ресурсов для целевой платформы.</span><span class="sxs-lookup"><span data-stu-id="a81ae-113">For details on configuration and usage, see the resource kit for the target platform.</span></span>

<span data-ttu-id="a81ae-114">Дополнительные сторонние поставщики услуг мультимедиа могут быть написаны для конкретных протоколов или для физических устройств.</span><span class="sxs-lookup"><span data-stu-id="a81ae-114">Additional third-party media service providers can be written for particular protocols or for physical devices.</span></span> <span data-ttu-id="a81ae-115">[Интерфейс поставщика услуг мультимедиа (мспи)](media-service-provider-interface-mspi-.md) описывает интерфейсы, которые должны быть реализованы для того, чтобы MSP мог взаимодействовать с компонентами телефонии Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a81ae-115">The [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md) describes the interfaces that must be implemented to allow an MSP to interact with the components of Microsoft Telephony.</span></span>

 

 
