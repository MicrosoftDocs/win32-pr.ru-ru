---
title: Куча
description: Куча отслеживает группу выделений, освобожденных как единое целое.
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- Веб-службы кучи для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e1651f90b8ad1afca8f85f9dd2e6f10fc7f5c3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104414220"
---
# <a name="heap"></a><span data-ttu-id="68c21-106">Куча</span><span class="sxs-lookup"><span data-stu-id="68c21-106">Heap</span></span>

<span data-ttu-id="68c21-107">Куча отслеживает группу выделений, освобожденных как единое целое.</span><span class="sxs-lookup"><span data-stu-id="68c21-107">A heap tracks a group of allocations that are freed as a unit.</span></span>

<span data-ttu-id="68c21-108">Это позволяет избежать сложных шаблонов выделения и освобождения памяти при использовании ВВСАПИ.</span><span class="sxs-lookup"><span data-stu-id="68c21-108">This allows you to avoid complex patterns of allocating and deallocating memory when you use the WWSAPI.</span></span>


<span data-ttu-id="68c21-109">Существует куча, связанная с каждым сообщением.</span><span class="sxs-lookup"><span data-stu-id="68c21-109">There is a heap associated with every message.</span></span> <span data-ttu-id="68c21-110">При отправке сообщения или при получении сообщения используется куча сообщения для всех выделений, связанных с конкретным сообщением.</span><span class="sxs-lookup"><span data-stu-id="68c21-110">As a message is being sent, or as a message is being received, the heap of the message is used for any allocations relating to that particular message.</span></span> <span data-ttu-id="68c21-111">После отправки или получения сообщения куча сбрасывается (что очищает все выделения, связанные с конкретным сообщением).</span><span class="sxs-lookup"><span data-stu-id="68c21-111">After a message is sent or received, the heap is reset (which cleans up any allocations related to the particular message).</span></span>

<span data-ttu-id="68c21-112">Кучи также можно использовать для хранения данных сообщений отдельно от времени существования сообщения.</span><span class="sxs-lookup"><span data-stu-id="68c21-112">Heaps can also be used to store message data separately from the lifetime of a message.</span></span> <span data-ttu-id="68c21-113">Многие из спецификаций API, позволяющие использовать кучу для считывания данных, предоставляют явный контроль над временем существования любых считываемых данных.</span><span class="sxs-lookup"><span data-stu-id="68c21-113">Many of the API's allow specification of the heap to use when reading data give explicit control over the lifetime of any data read.</span></span>

<span data-ttu-id="68c21-114">При выделении из кучи гарантированно выводятся по крайней мере 8-байтная граница.</span><span class="sxs-lookup"><span data-stu-id="68c21-114">Allocations from a heap are guaranteed to be aligned on at least an 8 byte boundary.</span></span>

<span data-ttu-id="68c21-115">Выделение нулевого байта вернет непустой указатель.</span><span class="sxs-lookup"><span data-stu-id="68c21-115">Zero byte allocations will return a non-NULL pointer.</span></span>

<span data-ttu-id="68c21-116">В Windows 7, если Пажехеап включен, для управления памятью используется куча, возвращенная из Хеапкреате.</span><span class="sxs-lookup"><span data-stu-id="68c21-116">In Windows 7, if PageHeap is enabled, a heap returned from HeapCreate is used to manage the memory.</span></span> <span data-ttu-id="68c21-117">В этом случае [**всаллок**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) сопоставляется напрямую с хеапаллок, а [**Всресесеап**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) — с хеапдестрой.</span><span class="sxs-lookup"><span data-stu-id="68c21-117">In this case, [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) maps directly to HeapAlloc and [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) maps to HeapDestroy.</span></span>

<span data-ttu-id="68c21-118">В куче используется следующее перечисление:</span><span class="sxs-lookup"><span data-stu-id="68c21-118">The following enumeration is used with the heap:</span></span>

-   [<span data-ttu-id="68c21-119">**\_ \_ идентификатор свойства WS \_ heap**</span><span class="sxs-lookup"><span data-stu-id="68c21-119">**WS\_HEAP\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

<span data-ttu-id="68c21-120">В куче используются следующие функции:</span><span class="sxs-lookup"><span data-stu-id="68c21-120">The following functions are used with the heap:</span></span>

-   [<span data-ttu-id="68c21-121">**всаллок**</span><span class="sxs-lookup"><span data-stu-id="68c21-121">**WsAlloc**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [<span data-ttu-id="68c21-122">**вскреатехеап**</span><span class="sxs-lookup"><span data-stu-id="68c21-122">**WsCreateHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [<span data-ttu-id="68c21-123">**всфрихеап**</span><span class="sxs-lookup"><span data-stu-id="68c21-123">**WsFreeHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [<span data-ttu-id="68c21-124">**всжесеаппроперти**</span><span class="sxs-lookup"><span data-stu-id="68c21-124">**WsGetHeapProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [<span data-ttu-id="68c21-125">**всресесеап**</span><span class="sxs-lookup"><span data-stu-id="68c21-125">**WsResetHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

<span data-ttu-id="68c21-126">В куче используется следующий маркер:</span><span class="sxs-lookup"><span data-stu-id="68c21-126">The following handle is used with the heap:</span></span>

-   [<span data-ttu-id="68c21-127">\_куча WS</span><span class="sxs-lookup"><span data-stu-id="68c21-127">WS\_HEAP</span></span>](ws-heap.md)

<span data-ttu-id="68c21-128">В куче используются следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="68c21-128">The following structures are used with the heap:</span></span>

-   [<span data-ttu-id="68c21-129">**\_Свойства КУЧИ \_ WS**</span><span class="sxs-lookup"><span data-stu-id="68c21-129">**WS\_HEAP\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [<span data-ttu-id="68c21-130">**\_свойство WS heap \_**</span><span class="sxs-lookup"><span data-stu-id="68c21-130">**WS\_HEAP\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




