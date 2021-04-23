---
description: Поставщик услуг телефонии (TSP) — это библиотека динамической компоновки (DLL), которая поддерживает управление устройствами связи с помощью набора экспортированных функций службы.
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: Поставщики услуг телефонии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3c8887723cc74a1bf0d77bcdcfd06c8468a4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912763"
---
# <a name="telephony-service-providers"></a><span data-ttu-id="1357f-103">Поставщики услуг телефонии</span><span class="sxs-lookup"><span data-stu-id="1357f-103">Telephony Service Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="1357f-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="1357f-104">Purpose</span></span>

<span data-ttu-id="1357f-105">Поставщик услуг телефонии (TSP) — это библиотека динамической компоновки (DLL), которая поддерживает управление устройствами связи с помощью набора экспортированных функций службы.</span><span class="sxs-lookup"><span data-stu-id="1357f-105">A telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="1357f-106">Приложение TAPI использует стандартизованные команды, TAPI передает сведения поставщику услуг телефонии, а метод TSP обрабатывает конкретные команды, которые должны обмениваться данными с устройством.</span><span class="sxs-lookup"><span data-stu-id="1357f-106">A TAPI application uses standardized commands, TAPI passes information to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span>

<span data-ttu-id="1357f-107">TSP должен соответствовать интерфейсу поставщика услуг телефонии (ТСПИ) для функционирования в качестве поставщика услуг в среде телефонии Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="1357f-107">A TSP must conform to the Telephony Service Provider Interface (TSPI) to function as a service provider within the Microsoft Telephony environment.</span></span> <span data-ttu-id="1357f-108">ТСПИ определяет внешние функции, предоставляемые поставщиком услуг телефонии, предоставляемым оборудованием связи.</span><span class="sxs-lookup"><span data-stu-id="1357f-108">TSPI defines the external functions exposed by a telephony service provider supplied with communications equipment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1357f-109">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="1357f-109">Developer audience</span></span>

<span data-ttu-id="1357f-110">Приложения с поддержкой TAPI можно писать на многих языках, включая Java, Visual Basic и C/C++.</span><span class="sxs-lookup"><span data-stu-id="1357f-110">You can write TAPI-enabled applications in many languages, including Java, Visual Basic, and C/C++.</span></span> <span data-ttu-id="1357f-111">Предыдущий опыт разработки с телекоммуникациями или другими приложениями телефонии является полезным, но не необходимым.</span><span class="sxs-lookup"><span data-stu-id="1357f-111">Previous development experience with telecommunications or other telephony applications is helpful but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1357f-112">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="1357f-112">Run-time requirements</span></span>

<span data-ttu-id="1357f-113">ТСПИ включает разработку специалистами для всех версий Windows.</span><span class="sxs-lookup"><span data-stu-id="1357f-113">TSPI enables development of TSPs for all versions of Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1357f-114">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="1357f-114">In this section</span></span>



| <span data-ttu-id="1357f-115">Раздел</span><span class="sxs-lookup"><span data-stu-id="1357f-115">Topic</span></span>                                                                | <span data-ttu-id="1357f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="1357f-116">Description</span></span>                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="1357f-117">Обзор</span><span class="sxs-lookup"><span data-stu-id="1357f-117">Overview</span></span>](about-the-telephony-service-provider-tsp-.md)<br/> | <span data-ttu-id="1357f-118">Общие сведения об архитектуре и компонентах ТСПИ.</span><span class="sxs-lookup"><span data-stu-id="1357f-118">General information about TSPI's architecture and components.</span></span><br/> |
| [<span data-ttu-id="1357f-119">Ссылки</span><span class="sxs-lookup"><span data-stu-id="1357f-119">Reference</span></span>](tspi-reference.md)<br/>                           | <span data-ttu-id="1357f-120">Документация по интерфейсам ТСПИ.</span><span class="sxs-lookup"><span data-stu-id="1357f-120">Documentation for the TSPI interfaces.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="1357f-121">См. также</span><span class="sxs-lookup"><span data-stu-id="1357f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1357f-122">Обзор телефонии Майкрософт</span><span class="sxs-lookup"><span data-stu-id="1357f-122">Microsoft Telephony Overview</span></span>](./microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="1357f-123">Поставщики служб мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1357f-123">Media Service Providers</span></span>](./media-service-providers-start-page.md)
</dt> <dt>

[<span data-ttu-id="1357f-124">TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="1357f-124">TAPI 2.2</span></span>](./tapi-2-2-start-page.md)
</dt> <dt>

[<span data-ttu-id="1357f-125">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="1357f-125">TAPI 3.1</span></span>](./tapi-3-1-start-page.md)
</dt> </dl>

 

