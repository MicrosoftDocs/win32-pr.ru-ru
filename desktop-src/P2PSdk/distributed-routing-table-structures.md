---
description: Следующие структуры поддерживают функции API таблиц распределенной маршрутизации (DRT).
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: Структуры таблиц распределенной маршрутизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d454d2c28008422da897dc91ca9a3dc29db374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663349"
---
# <a name="distributed-routing-table-structures"></a><span data-ttu-id="38797-103">Структуры таблиц распределенной маршрутизации</span><span class="sxs-lookup"><span data-stu-id="38797-103">Distributed Routing Table Structures</span></span>

<span data-ttu-id="38797-104">Следующие структуры поддерживают функции API таблиц распределенной маршрутизации (DRT).</span><span class="sxs-lookup"><span data-stu-id="38797-104">The following structures support the Distributed Routing Table (DRT) API functions.</span></span>



| <span data-ttu-id="38797-105">Структура</span><span class="sxs-lookup"><span data-stu-id="38797-105">Structure</span></span>                                                  | <span data-ttu-id="38797-106">Описание</span><span class="sxs-lookup"><span data-stu-id="38797-106">Description</span></span>                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38797-107">**\_данные DRT**</span><span class="sxs-lookup"><span data-stu-id="38797-107">**DRT\_DATA**</span></span>](/windows/desktop/api/drt/ns-drt-drt_data)                              | <span data-ttu-id="38797-108">Содержит большой двоичный объект данных.</span><span class="sxs-lookup"><span data-stu-id="38797-108">Contains a data blob.</span></span> <span data-ttu-id="38797-109">Эта структура используется несколькими функциями DRT.</span><span class="sxs-lookup"><span data-stu-id="38797-109">This structure is used by several DRT functions.</span></span>                                                                                                                   |
| [<span data-ttu-id="38797-110">**\_Регистрация DRT**</span><span class="sxs-lookup"><span data-stu-id="38797-110">**DRT\_REGISTRATION**</span></span>](/windows/desktop/api/drt/ns-drt-drt_registration)              | <span data-ttu-id="38797-111">Содержит регистрацию ключа.</span><span class="sxs-lookup"><span data-stu-id="38797-111">Contains the key registration.</span></span> <span data-ttu-id="38797-112">Это член структуры [**\_ \_ результатов поиска DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) , который является аргументом, передаваемым в [**дртрегистеркэй**](/windows/desktop/api/drt/nf-drt-drtregisterkey).</span><span class="sxs-lookup"><span data-stu-id="38797-112">This is a member of the [**DRT\_SEARCH\_RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) structure and is an argument passed to [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey).</span></span> |
| [<span data-ttu-id="38797-113">**\_адрес DRT**</span><span class="sxs-lookup"><span data-stu-id="38797-113">**DRT\_ADDRESS**</span></span>](/windows/desktop/api/drt/ns-drt-drt_address)                        | <span data-ttu-id="38797-114">Содержит сведения о конечной точке для узла DRT, который принимал участие в поиске.</span><span class="sxs-lookup"><span data-stu-id="38797-114">Contains endpoint information about a DRT node that participated in a search.</span></span> <span data-ttu-id="38797-115">Эти сведения предназначены для использования при отладке проблем с подключением.</span><span class="sxs-lookup"><span data-stu-id="38797-115">This information is intended for use in debugging connectivity problems.</span></span>                                   |
| [<span data-ttu-id="38797-116">**\_список адресов \_ DRT**</span><span class="sxs-lookup"><span data-stu-id="38797-116">**DRT\_ADDRESS\_LIST**</span></span>](/windows/desktop/api/drt/ns-drt-drt_address_list)             | <span data-ttu-id="38797-117">Содержит набор структур [**\_ адресов DRT**](/windows/desktop/api/drt/ns-drt-drt_address) , представляющих узлы, к которым осуществляется обращение во время поиска ключа.</span><span class="sxs-lookup"><span data-stu-id="38797-117">Contains a set of [**DRT\_ADDRESS**](/windows/desktop/api/drt/ns-drt-drt_address) structures representing the nodes contacted during a search for a key.</span></span>                                                             |
| [<span data-ttu-id="38797-118">**\_поставщик безопасности \_ DRT**</span><span class="sxs-lookup"><span data-stu-id="38797-118">**DRT\_SECURITY\_PROVIDER**</span></span>](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | <span data-ttu-id="38797-119">Определяет интерфейс, который должен быть реализован поставщиком безопасности.</span><span class="sxs-lookup"><span data-stu-id="38797-119">Defines the interface that must be implemented by a security provider.</span></span>                                                                                                                   |
| [<span data-ttu-id="38797-120">**\_поставщик начальной загрузки DRT \_**</span><span class="sxs-lookup"><span data-stu-id="38797-120">**DRT\_BOOTSTRAP\_PROVIDER**</span></span>](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | <span data-ttu-id="38797-121">Определяет интерфейс, который должен быть реализован поставщиком начальной загрузки.</span><span class="sxs-lookup"><span data-stu-id="38797-121">Defines the interface that must be implemented by a bootstrap provider.</span></span>                                                                                                                  |
| [<span data-ttu-id="38797-122">**\_Параметры DRT**</span><span class="sxs-lookup"><span data-stu-id="38797-122">**DRT\_SETTINGS**</span></span>](/windows/desktop/api/drt/ns-drt-drt_settings)                      | <span data-ttu-id="38797-123">Определяет параметры DRT при инициализации.</span><span class="sxs-lookup"><span data-stu-id="38797-123">Defines DRT settings at initialization.</span></span> <span data-ttu-id="38797-124">Эта структура передается в качестве аргумента в [**дртопен**](/windows/desktop/api/drt/nf-drt-drtopen).</span><span class="sxs-lookup"><span data-stu-id="38797-124">This structure is passed as an argument to [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).</span></span>                                                                           |
| [<span data-ttu-id="38797-125">**\_сведения о поиске в DRT \_**</span><span class="sxs-lookup"><span data-stu-id="38797-125">**DRT\_SEARCH\_INFO**</span></span>](/windows/desktop/api/drt/ns-drt-drt_search_info)               | <span data-ttu-id="38797-126">Определяет поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="38797-126">Defines a search query.</span></span> <span data-ttu-id="38797-127">Эта структура передается в качестве аргумента в [**дртстартсеарч**](/windows/desktop/api/drt/nf-drt-drtstartsearch).</span><span class="sxs-lookup"><span data-stu-id="38797-127">This structure is passed as an argument to [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch).</span></span>                                                                             |
| [<span data-ttu-id="38797-128">**\_Результат поиска \_ DRT**</span><span class="sxs-lookup"><span data-stu-id="38797-128">**DRT\_SEARCH\_RESULT**</span></span>](/windows/desktop/api/drt/ns-drt-drt_search_result)           | <span data-ttu-id="38797-129">Содержит результат поиска.</span><span class="sxs-lookup"><span data-stu-id="38797-129">Contains a search result.</span></span> <span data-ttu-id="38797-130">Эта структура возвращается функцией [**дртжетсеарчресулт**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult).</span><span class="sxs-lookup"><span data-stu-id="38797-130">This structure is returned by [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult).</span></span>                                                                                |
| [<span data-ttu-id="38797-131">**\_данные событий \_ DRT**</span><span class="sxs-lookup"><span data-stu-id="38797-131">**DRT\_EVENT\_DATA**</span></span>](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | <span data-ttu-id="38797-132">Содержит данные события, возвращаемые вызовом [**дртжетевентдата**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) после того, как приложение получит сигнал события.</span><span class="sxs-lookup"><span data-stu-id="38797-132">Contains the event data returned by calling [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) after an application receives an event signal.</span></span>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="38797-133">См. также</span><span class="sxs-lookup"><span data-stu-id="38797-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38797-134">Перечисление таблиц распределенной маршрутизации</span><span class="sxs-lookup"><span data-stu-id="38797-134">Distributed Routing Table Enumerations</span></span>](distributed-routing-table-enumerations.md)
</dt> <dt>

[<span data-ttu-id="38797-135">Функции таблиц распределенной маршрутизации</span><span class="sxs-lookup"><span data-stu-id="38797-135">Distributed Routing Table Functions</span></span>](distributed-routing-table-functions.md)
</dt> <dt>

[<span data-ttu-id="38797-136">Справочник по распределенной маршрутизации API таблиц</span><span class="sxs-lookup"><span data-stu-id="38797-136">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



