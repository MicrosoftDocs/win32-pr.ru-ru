---
description: TAPI версии 3,1 — это API на основе COM, который выполняет слияние классической и IP-телефонии. Возможные приложения находятся в диапазоне от простых голосовых вызовов по коммутируемой телефонной сети (PSTN) для многоадресной передачи мультимедийных пакетов мультимедиа с качеством обслуживания (QOS).
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: Обзор TAPI 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30b70ccdc1c4a0985107d2bd2fc36bfbe4e3fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683395"
---
# <a name="tapi-31-overview"></a><span data-ttu-id="6e46a-104">Обзор TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="6e46a-104">TAPI 3.1 Overview</span></span>

<span data-ttu-id="6e46a-105">TAPI версии 3,1 — это API на основе COM, который выполняет слияние классической и IP-телефонии.</span><span class="sxs-lookup"><span data-stu-id="6e46a-105">TAPI version 3.1 is a COM-based API that merges classic and IP telephony.</span></span> <span data-ttu-id="6e46a-106">Возможные приложения находятся в диапазоне от простых голосовых вызовов по коммутируемой телефонной сети (PSTN) для многоадресной передачи мультимедийных пакетов мультимедиа с качеством обслуживания (QOS).</span><span class="sxs-lookup"><span data-stu-id="6e46a-106">Possible applications range from simple voice calls over the Public Switched Telephone Network (PSTN) to multicast multimedia IP conferencing with quality of service (QOS).</span></span>

<span data-ttu-id="6e46a-107">Дополнительные сведения о возможностях IP-телефонии в TAPI 3,1 см. в техническом документе "IP-телефония с интерфейсом TAPI 3", который находится на веб-сайте корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="6e46a-107">For additional information on TAPI 3.1 IP Telephony capabilities, please consult the "IP Telephony with TAPI 3" white paper, which can be found on the Microsoft web site.</span></span>

<span data-ttu-id="6e46a-108">Существует четыре основных компонента для TAPI 3,1:</span><span class="sxs-lookup"><span data-stu-id="6e46a-108">There are four major components to TAPI 3.1:</span></span>

-   <span data-ttu-id="6e46a-109">API COM</span><span class="sxs-lookup"><span data-stu-id="6e46a-109">COM API</span></span>
-   <span data-ttu-id="6e46a-110">Сервер TAPI</span><span class="sxs-lookup"><span data-stu-id="6e46a-110">TAPI Server</span></span>
-   <span data-ttu-id="6e46a-111">Поставщики услуг телефонии (специалистами)</span><span class="sxs-lookup"><span data-stu-id="6e46a-111">Telephony Service Providers (TSPs)</span></span>
-   <span data-ttu-id="6e46a-112">Поставщики потоков мультимедиа (MSP)</span><span class="sxs-lookup"><span data-stu-id="6e46a-112">Media Stream Providers (MSPs)</span></span>

<span data-ttu-id="6e46a-113">На следующей схеме показана архитектура TAPI 3,1.</span><span class="sxs-lookup"><span data-stu-id="6e46a-113">The following diagram illustrates the TAPI 3.1 architecture:</span></span>

![Архитектура TAPI 3](images/callarc-gif-1.png)

<span data-ttu-id="6e46a-115">API реализован в виде набора объектов модели COM.</span><span class="sxs-lookup"><span data-stu-id="6e46a-115">The API is implemented as a suite of Component Object Model (COM) objects.</span></span> <span data-ttu-id="6e46a-116">Перемещение TAPI в объектно-ориентированную модель COM позволяет разработчикам писать приложения с поддержкой TAPI на многих языках, таких как Java, Visual Basic или C/C++.</span><span class="sxs-lookup"><span data-stu-id="6e46a-116">Moving TAPI to the object-oriented COM model allows developers to write TAPI-enabled applications in many languages, such as Java, Visual Basic, or C/C++.</span></span> <span data-ttu-id="6e46a-117">Использование COM обеспечивает обновление компонентов функций TAPI.</span><span class="sxs-lookup"><span data-stu-id="6e46a-117">Use of COM enables component upgrades of TAPI features.</span></span>

<span data-ttu-id="6e46a-118">Серверный процесс TAPI (ТАПИСРВ) абстрагирует интерфейс поставщика услуг TAPI (ТСПИ) от TAPI 3. x и TAPI 2. x, позволяя использовать поставщики услуг телефонии TAPI 2. x с интерфейсом TAPI 3. x, сохраняя внутреннее состояние TAPI.</span><span class="sxs-lookup"><span data-stu-id="6e46a-118">The TAPI Server process (TAPISRV) abstracts the TAPI Service Provider Interface (TSPI) from TAPI 3.x and TAPI 2.x, allowing TAPI 2.x Telephony Service Providers to be used with TAPI 3.x, maintaining the internal state of TAPI.</span></span> <span data-ttu-id="6e46a-119">ТАПИСРВ реализуется как процесс службы в SVCHOST.</span><span class="sxs-lookup"><span data-stu-id="6e46a-119">TAPISRV is implemented as a service process within SVCHOST.</span></span>

<span data-ttu-id="6e46a-120">[Поставщики услуг](./tapi-service-providers.md) являются абстрактными механизмами транспортировки носителей, специфичными для поставщика.</span><span class="sxs-lookup"><span data-stu-id="6e46a-120">[Service Providers](./tapi-service-providers.md) abstract provider-specific media transport mechanisms.</span></span> <span data-ttu-id="6e46a-121">Обычно они существуют в парах — поставщик услуг телефонии (TSP) для управления вызовами и поставщик службы мультимедиа (MSP) для управления мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6e46a-121">They typically exist in pairs – a Telephony Service Provider (TSP) for call control and a Media Service Provider (MSP) for media control.</span></span>

<span data-ttu-id="6e46a-122">[Поставщики услуг телефонии](./telephony-service-providers-start-page.md) (специалистами) отвечают за разрешение модели независимых вызовов TAPI в механизмы управления вызовами, зависящие от протокола.</span><span class="sxs-lookup"><span data-stu-id="6e46a-122">[Telephony Service Providers](./telephony-service-providers-start-page.md) (TSPs) are responsible for resolving the protocol-independent call model of TAPI into protocol-specific call control mechanisms.</span></span> <span data-ttu-id="6e46a-123">TAPI 3,1 обеспечивает обратную совместимость с TAPI 2,1 специалистами.</span><span class="sxs-lookup"><span data-stu-id="6e46a-123">TAPI 3.1 provides backward compatibility with TAPI 2.1 TSPs.</span></span> <span data-ttu-id="6e46a-124">Два поставщика услуг IP-телефонии (и связанные с ними MSP) поставляются по умолчанию с помощью TAPI 3,1: TSP H. 323 и TSP многоадресной рассылки IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="6e46a-124">Two IP Telephony service providers (and their associated MSPs) ship by default with TAPI 3.1: the H.323 TSP and the IP Multicast Conferencing TSP.</span></span>

<span data-ttu-id="6e46a-125">[Поставщики служб мультимедиа](media-service-providers-start-page.md) (MSP) предоставляют единообразный способ доступа к потокам мультимедиа в вызове, поддерживающем API DirectShow<sup>TM</sup> в качестве основного обработчика потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6e46a-125">[Media Service Providers](media-service-providers-start-page.md) (MSPs) provide a uniform way to access the media streams in a call, supporting the DirectShow<sup>TM</sup> API as the primary media stream handler.</span></span> <span data-ttu-id="6e46a-126">TAPI MSP реализует интерфейсы DirectShow для определенного TSP и требуется для любой службы телефонии, использующей потоковую передачу DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6e46a-126">TAPI MSPs implement DirectShow interfaces for a particular TSP and are required for any telephony service that makes use of DirectShow streaming.</span></span> <span data-ttu-id="6e46a-127">Универсальные потоки обрабатываются приложением.</span><span class="sxs-lookup"><span data-stu-id="6e46a-127">Generic streams are handled by the application.</span></span>

 

 
