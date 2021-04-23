---
description: Базовый интерфейс TAPI 2,2 можно использовать для управления центрами обработки вызовов и другими элементами сетевой инфраструктуры телефонии (например, серверами IVR и голосовой почты) через Управление вызовами сторонних производителей.
ms.assetid: e920dc4a-adb4-4a36-ac04-f265538531eb
title: Управление центром обработки вызовов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4200ff434249856507109915f41f7f1479eddfd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911547"
---
# <a name="call-center-control"></a><span data-ttu-id="189b6-103">Управление центром обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="189b6-103">Call Center Control</span></span>

<span data-ttu-id="189b6-104">Базовый интерфейс TAPI 2,2 можно использовать для управления центрами обработки вызовов и другими элементами сетевой инфраструктуры телефонии (например, серверами IVR и голосовой почты) через Управление вызовами сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="189b6-104">Basic TAPI 2.2 can be used to manage call centers and other elements of Telephony network infrastructure (such as IVR and voice mail servers) through third-party call control.</span></span> <span data-ttu-id="189b6-105">Для создания ACD-прокси, которые будут выполняться на серверах, в TAPI 2,2 были добавлены функции для предоставления дополнительной помощи разработчикам приложений.</span><span class="sxs-lookup"><span data-stu-id="189b6-105">To help create ACD proxies that will run on servers, functions have been added to TAPI 2.2 to provide additional assistance to application developers.</span></span>

<span data-ttu-id="189b6-106">В следующих разделах описываются функции TAPI 2,2, которые можно использовать для реализации элементов управления центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="189b6-106">The following topics describe the TAPI 2.2 features that you can use to implement call center controls:</span></span>

-   [<span data-ttu-id="189b6-107">Моделирование центра обработки звонков</span><span class="sxs-lookup"><span data-stu-id="189b6-107">Modeling of a Call Center</span></span>](modeling-of-a-call-center.md)
-   [<span data-ttu-id="189b6-108">Станций</span><span class="sxs-lookup"><span data-stu-id="189b6-108">Stations</span></span>](stations.md)
-   [<span data-ttu-id="189b6-109">Прогнозирующий набор</span><span class="sxs-lookup"><span data-stu-id="189b6-109">Predictive Dialing</span></span>](predictive-dialing.md)
-   [<span data-ttu-id="189b6-110">Очереди вызовов и точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="189b6-110">Call Queues and Route Points</span></span>](call-queues-and-route-points.md)
-   [<span data-ttu-id="189b6-111">Мониторинг и контроль агента ACD</span><span class="sxs-lookup"><span data-stu-id="189b6-111">ACD Agent Monitoring and Control</span></span>](acd-agent-monitoring-and-control.md)
-   [<span data-ttu-id="189b6-112">Управление состоянием станции</span><span class="sxs-lookup"><span data-stu-id="189b6-112">Station Status Control</span></span>](station-status-control.md)
-   [<span data-ttu-id="189b6-113">Управление состоянием станции</span><span class="sxs-lookup"><span data-stu-id="189b6-113">Station Status Control</span></span>](station-status-control.md)
-   [<span data-ttu-id="189b6-114">Таймер состояния вызова</span><span class="sxs-lookup"><span data-stu-id="189b6-114">Call State Timer</span></span>](call-state-timer.md)
-   [<span data-ttu-id="189b6-115">Таймеры событий мультимедиа</span><span class="sxs-lookup"><span data-stu-id="189b6-115">Media Event Timers</span></span>](media-event-timers.md)

<span data-ttu-id="189b6-116">Интерфейс TAPI 3. x — предпочтительный API для написания приложений ACD Agent.</span><span class="sxs-lookup"><span data-stu-id="189b6-116">TAPI 3.x is the preferred API of writing ACD Agent applications.</span></span> <span data-ttu-id="189b6-117">Сведения об использовании этих интерфейсов и методов см. в разделе [элементы управления центра обработки вызовов](./about-call-center-controls.md) .</span><span class="sxs-lookup"><span data-stu-id="189b6-117">Please see the [Call Center Controls](./about-call-center-controls.md) section for information on using these interfaces and methods.</span></span> <span data-ttu-id="189b6-118">Однако при необходимости TAPI 2,2 остается пригодным для полноценных наборов приложений.</span><span class="sxs-lookup"><span data-stu-id="189b6-118">However, TAPI 2.2 remains usable for full ACD application suites if desired.</span></span>

 

 
