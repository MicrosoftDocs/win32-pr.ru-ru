---
description: Интерфейсы программирования приложений телефонии (Майкрософт) поддерживают разработку коммуникационных приложений для Microsoft Windows. В следующей таблице перечислены интерфейсы телефонии.
ms.assetid: e7348296-ee2d-4e0a-b274-3563dccea841
title: Интерфейсы программирования приложений телефонии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19fd6a520c8a53440967eeef753b7ed8c90ba5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912764"
---
# <a name="telephony-application-programming-interfaces"></a><span data-ttu-id="c03af-104">Интерфейсы программирования приложений телефонии</span><span class="sxs-lookup"><span data-stu-id="c03af-104">Telephony Application Programming Interfaces</span></span>

<span data-ttu-id="c03af-105">Интерфейсы программирования приложений телефонии (Майкрософт) поддерживают разработку коммуникационных приложений для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c03af-105">The Microsoft telephony application programming interfaces support the development of communications applications for Microsoft Windows.</span></span> <span data-ttu-id="c03af-106">В следующей таблице перечислены интерфейсы телефонии.</span><span class="sxs-lookup"><span data-stu-id="c03af-106">The telephony interfaces are listed in the following table.</span></span>



| <span data-ttu-id="c03af-107">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="c03af-107">Interface</span></span>                                                  | <span data-ttu-id="c03af-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c03af-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c03af-109">Интерфейс TAPI 2. x</span><span class="sxs-lookup"><span data-stu-id="c03af-109">TAPI 2.x</span></span>](./tapi-2-2-start-page.md)               | <span data-ttu-id="c03af-110">API на основе языка C, который позволяет реализовать коммуникационные приложения от основного элемента управления модемом до центров вызовов с несколькими агентами и коммутаторами.</span><span class="sxs-lookup"><span data-stu-id="c03af-110">A C-programming language based API that enables you to implement communications applications ranging from basic modem control to call centers with multiple agents and switches.</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="c03af-111">Интерфейс TAPI 3. x</span><span class="sxs-lookup"><span data-stu-id="c03af-111">TAPI 3.x</span></span>](tapi-3-1-start-page.md)                        | <span data-ttu-id="c03af-112">API на основе COM, который выполняет слияние классической и IP-телефонии.</span><span class="sxs-lookup"><span data-stu-id="c03af-112">A COM-based API that merges classic and IP telephony.</span></span>                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="c03af-113">тспи</span><span class="sxs-lookup"><span data-stu-id="c03af-113">TSPI</span></span>](./telephony-service-providers-start-page.md) | <span data-ttu-id="c03af-114">Поставщик услуг телефонии (TSP) — это библиотека динамической компоновки (DLL), которая поддерживает управление устройствами связи с помощью набора экспортированных функций службы.</span><span class="sxs-lookup"><span data-stu-id="c03af-114">A telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="c03af-115">Приложение TAPI использует стандартизованные команды, TAPI передает сведения поставщику услуг телефонии, а метод TSP обрабатывает конкретные команды, которые должны обмениваться данными с устройством.</span><span class="sxs-lookup"><span data-stu-id="c03af-115">A TAPI application uses standardized commands, TAPI passes information to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span> |
| [<span data-ttu-id="c03af-116">мспи</span><span class="sxs-lookup"><span data-stu-id="c03af-116">MSPI</span></span>](media-service-providers-start-page.md)             | <span data-ttu-id="c03af-117">Поставщик службы мультимедиа (MSP) позволяет приложению значительно управлять носителем для конкретного транспортного механизма.</span><span class="sxs-lookup"><span data-stu-id="c03af-117">A media service provider (MSP) allows an application considerable control over the media for a particular transport mechanism.</span></span> <span data-ttu-id="c03af-118">MSP всегда сопряжен с поставщиком услуг телефонии (TSP).</span><span class="sxs-lookup"><span data-stu-id="c03af-118">An MSP is always paired with a telephony service provider (TSP).</span></span>                                                                                                                                                         |



 

 

 
