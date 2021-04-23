---
description: Следующие перечисления поддерживают API таблиц распределенной маршрутизации (DRT).
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: Перечисление таблиц распределенной маршрутизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c432b156a9299a9f70026a394a6fd97f06528a25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663352"
---
# <a name="distributed-routing-table-enumerations"></a><span data-ttu-id="41fbd-103">Перечисление таблиц распределенной маршрутизации</span><span class="sxs-lookup"><span data-stu-id="41fbd-103">Distributed Routing Table Enumerations</span></span>

<span data-ttu-id="41fbd-104">Следующие перечисления поддерживают API таблиц распределенной маршрутизации (DRT).</span><span class="sxs-lookup"><span data-stu-id="41fbd-104">The following enumerations support the Distributed Routing Table (DRT) API.</span></span>



| <span data-ttu-id="41fbd-105">Перечисление</span><span class="sxs-lookup"><span data-stu-id="41fbd-105">Enumeration</span></span>                                                            | <span data-ttu-id="41fbd-106">Описание</span><span class="sxs-lookup"><span data-stu-id="41fbd-106">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41fbd-107">**\_область DRT**</span><span class="sxs-lookup"><span data-stu-id="41fbd-107">**DRT\_SCOPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | <span data-ttu-id="41fbd-108">Определяет набор областей IPv6, в которых будет выполняться сервер DRT при использовании транспортного протокола IPv6 UDP, созданного [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport).</span><span class="sxs-lookup"><span data-stu-id="41fbd-108">Defines the set of IPv6 scopes in which DRT will operate when using the IPv6 UDP transport created by [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport).</span></span> |
| [<span data-ttu-id="41fbd-109">**\_ \_ Флаги адреса DRT**</span><span class="sxs-lookup"><span data-stu-id="41fbd-109">**DRT\_ADDRESS\_FLAGS**</span></span>](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | <span data-ttu-id="41fbd-110">Определяет набор ответов, которые могут возвращаться промежуточным узлом при выполнении поиска ключа.</span><span class="sxs-lookup"><span data-stu-id="41fbd-110">Defines the set of responses that may be returned by an intermediate node when performing a search for a key.</span></span>                                                         |
| [<span data-ttu-id="41fbd-111">**\_состояние DRT**</span><span class="sxs-lookup"><span data-stu-id="41fbd-111">**DRT\_STATUS**</span></span>](/windows/desktop/api/drt/ne-drt-drt_status)                                      | <span data-ttu-id="41fbd-112">Определяет возможные состояния подключения и ошибки локального узла.</span><span class="sxs-lookup"><span data-stu-id="41fbd-112">Defines the possible connectivity and error states of a local node.</span></span>                                                                                                   |
| [<span data-ttu-id="41fbd-113">**\_тип соответствия \_ DRT**</span><span class="sxs-lookup"><span data-stu-id="41fbd-113">**DRT\_MATCH\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | <span data-ttu-id="41fbd-114">Определяет точное совпадение результатов, возвращаемых при выполнении поиска.</span><span class="sxs-lookup"><span data-stu-id="41fbd-114">Defines the exactness of results returned when a search is performed.</span></span>                                                                                                 |
| [<span data-ttu-id="41fbd-115">**\_ \_ \_ тип изменения ключа конечного элемента \_ DRT**</span><span class="sxs-lookup"><span data-stu-id="41fbd-115">**DRT\_LEAFSET\_KEY\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | <span data-ttu-id="41fbd-116">Определяет набор типов изменений, которые могут быть выполнены с локальным узлом конечного набора в локальном кэше DRT.</span><span class="sxs-lookup"><span data-stu-id="41fbd-116">Defines the set of change types that can be performed on a local leaf set node in the local DRT cache.</span></span>                                                                |
| [<span data-ttu-id="41fbd-117">**\_Тип события \_ DRT**</span><span class="sxs-lookup"><span data-stu-id="41fbd-117">**DRT\_EVENT\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | <span data-ttu-id="41fbd-118">Определяет набор событий, которые могут быть вызваны DRT.</span><span class="sxs-lookup"><span data-stu-id="41fbd-118">Defines the set of events that can be raised by the DRT.</span></span>                                                                                                              |
| [<span data-ttu-id="41fbd-119">**\_режим безопасности \_ DRT**</span><span class="sxs-lookup"><span data-stu-id="41fbd-119">**DRT\_SECURITY\_MODE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | <span data-ttu-id="41fbd-120">Определяет возможные режимы безопасности DRT.</span><span class="sxs-lookup"><span data-stu-id="41fbd-120">Defines the possible security modes of the DRT.</span></span> <span data-ttu-id="41fbd-121">Это перечисление является полем структуры [**\_ параметров DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .</span><span class="sxs-lookup"><span data-stu-id="41fbd-121">This enumeration is a field of the [**DRT\_SETTINGS**](/windows/desktop/api/drt/ns-drt-drt_settings) structure.</span></span>                                   |
| [<span data-ttu-id="41fbd-122">**\_состояние регистрации \_ DRT**</span><span class="sxs-lookup"><span data-stu-id="41fbd-122">**DRT\_REGISTRATION\_STATE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | <span data-ttu-id="41fbd-123">Определяет состояние зарегистрированного ключа.</span><span class="sxs-lookup"><span data-stu-id="41fbd-123">Defines the state of a registered key.</span></span>                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="41fbd-124">См. также</span><span class="sxs-lookup"><span data-stu-id="41fbd-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41fbd-125">Структуры таблиц распределенной маршрутизации</span><span class="sxs-lookup"><span data-stu-id="41fbd-125">Distributed Routing Table Structures</span></span>](distributed-routing-table-structures.md)
</dt> <dt>

[<span data-ttu-id="41fbd-126">Функции таблиц распределенной маршрутизации</span><span class="sxs-lookup"><span data-stu-id="41fbd-126">Distributed Routing Table Functions</span></span>](distributed-routing-table-functions.md)
</dt> <dt>

[<span data-ttu-id="41fbd-127">Справочник по распределенной маршрутизации API таблиц</span><span class="sxs-lookup"><span data-stu-id="41fbd-127">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



