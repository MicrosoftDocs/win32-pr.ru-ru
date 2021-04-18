---
title: Proxy (Прокси)
description: Прокси-сервер находится в адресном пространстве вызывающего процесса и выступает в качестве суррогата для удаленного объекта.
ms.assetid: 6c82f655-ac46-4ed9-992b-0387b324a8f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11257dd060f51bef118a4afc0cc35acf995c111
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "105713221"
---
# <a name="proxy"></a><span data-ttu-id="bea22-103">Proxy (Прокси)</span><span class="sxs-lookup"><span data-stu-id="bea22-103">Proxy</span></span>

<span data-ttu-id="bea22-104">Прокси-сервер находится в адресном пространстве вызывающего процесса и выступает в качестве суррогата для удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="bea22-104">A proxy resides in the address space of the calling process and acts as a surrogate for the remote object.</span></span> <span data-ttu-id="bea22-105">С точки зрения вызывающего объекта прокси-объект является объектом.</span><span class="sxs-lookup"><span data-stu-id="bea22-105">From the perspective of the calling object, the proxy is the object.</span></span> <span data-ttu-id="bea22-106">Как правило, роль прокси-сервера заключается в упаковке параметров интерфейса для вызовов методов в своих интерфейсах объектов.</span><span class="sxs-lookup"><span data-stu-id="bea22-106">Typically, the proxy's role is to package the interface parameters for calls to methods in its object interfaces.</span></span> <span data-ttu-id="bea22-107">Прокси-сервер упаковывает параметры в буфер сообщений и передает буфер в канал, который обрабатывает транспорт между процессами.</span><span class="sxs-lookup"><span data-stu-id="bea22-107">The proxy packages the parameters into a message buffer and passes the buffer onto the channel, which handles the transport between processes.</span></span> <span data-ttu-id="bea22-108">Прокси-сервер реализуется как агрегатный или составной объект.</span><span class="sxs-lookup"><span data-stu-id="bea22-108">The proxy is implemented as an aggregate, or composite, object.</span></span> <span data-ttu-id="bea22-109">Она содержит предоставленный системой Диспетчер прокси-сервера и один или несколько компонентов интерфейса, называемых прокси-интерфейсами интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bea22-109">It contains a system-provided, manager piece called the proxy manager and one or more interface-specific components called interface proxies.</span></span> <span data-ttu-id="bea22-110">Число прокси-серверов интерфейса равно числу интерфейсов объектов, которые были предоставлены этому конкретному клиенту.</span><span class="sxs-lookup"><span data-stu-id="bea22-110">The number of interface proxies equals the number of object interfaces that have been exposed to that particular client.</span></span> <span data-ttu-id="bea22-111">Для клиентов, которые приводят к работе с объектной моделью компонента, прокси-сервер является реальным объектом.</span><span class="sxs-lookup"><span data-stu-id="bea22-111">To the client complying with the component object model, the proxy appears to be the real object.</span></span>

> [!Note]  
> <span data-ttu-id="bea22-112">При пользовательском маршалировании прокси-сервер можно реализовать аналогичным образом или напрямую с объектом без использования заглушки.</span><span class="sxs-lookup"><span data-stu-id="bea22-112">With custom marshaling, the proxy can be implemented similarly or it can communicate directly with the object without using a stub.</span></span>

 

<span data-ttu-id="bea22-113">Каждый прокси-интерфейс представляет собой объект компонента, реализующий код маршалирования для одного из интерфейсов объекта.</span><span class="sxs-lookup"><span data-stu-id="bea22-113">Each interface proxy is a component object that implements the marshaling code for one of the object's interfaces.</span></span> <span data-ttu-id="bea22-114">Прокси-сервер представляет объект, для которого он обеспечивает упаковку кода.</span><span class="sxs-lookup"><span data-stu-id="bea22-114">The proxy represents the object for which it provides marshaling code.</span></span> <span data-ttu-id="bea22-115">Каждый прокси-сервер также реализует интерфейс [**ирпкпроксибуффер**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) .</span><span class="sxs-lookup"><span data-stu-id="bea22-115">Each proxy also implements the [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) interface.</span></span> <span data-ttu-id="bea22-116">Хотя объектный интерфейс, представленный прокси-сервером, является открытым, реализация **ирпкпроксибуффер** является закрытой и используется внутри прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="bea22-116">Although the object interface represented by the proxy is public, the **IRpcProxyBuffer** implementation is private and is used internally within the proxy.</span></span> <span data-ttu-id="bea22-117">Диспетчер прокси-сервера отслеживает прокси интерфейсов, а также содержит открытую реализацию интерфейса управления [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) для статистического выражения.</span><span class="sxs-lookup"><span data-stu-id="bea22-117">The proxy manager keeps track of the interface proxies and also contains the public implementation of the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface for the aggregate.</span></span> <span data-ttu-id="bea22-118">Каждый прокси-сервер интерфейса может существовать в отдельной библиотеке DLL, которая загружается, когда поддерживаемый им интерфейс является материализованным для клиента.</span><span class="sxs-lookup"><span data-stu-id="bea22-118">Each interface proxy can exist in a separate DLL that is loaded when the interface it supports is materialized to the client.</span></span>

## <a name="structure-of-the-proxy"></a><span data-ttu-id="bea22-119">Структура прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="bea22-119">Structure of the Proxy</span></span>

<span data-ttu-id="bea22-120">На следующей схеме показана структура прокси-сервера, который поддерживает стандартный маршалирование параметров, принадлежащих двум интерфейсам: IA1 и IA2.</span><span class="sxs-lookup"><span data-stu-id="bea22-120">The following diagram shows the structure of a proxy that supports the standard marshaling of parameters belonging to two interfaces: IA1 and IA2.</span></span> <span data-ttu-id="bea22-121">Каждый прокси-интерфейс реализует [**ирпкпроксибуффер**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) для внутреннего взаимодействия между агрегатными частями.</span><span class="sxs-lookup"><span data-stu-id="bea22-121">Each interface proxy implements [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) for internal communication between the aggregate pieces.</span></span> <span data-ttu-id="bea22-122">Когда прокси-сервер готов к передаче упакованных параметров через границу процесса, он вызывает методы в интерфейсе [**ирпкчаннелбуффер**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) , который реализуется каналом.</span><span class="sxs-lookup"><span data-stu-id="bea22-122">When the proxy is ready to pass its marshaled parameters across the process boundary, it calls methods in the [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) interface, which is implemented by the channel.</span></span> <span data-ttu-id="bea22-123">Канал в свою очередь перенаправляет вызов в библиотеку времени выполнения RPC, чтобы он мог достичь места назначения в объекте.</span><span class="sxs-lookup"><span data-stu-id="bea22-123">The channel in turn forwards the call to the RPC run-time library so that it can reach its destination in the object.</span></span>

![Схема, на которой показана структура прокси-сервера.](images/4432d8d3-dfab-4635-90f8-408aecf70134.png)

## <a name="related-topics"></a><span data-ttu-id="bea22-125">См. также</span><span class="sxs-lookup"><span data-stu-id="bea22-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bea22-126">Канал</span><span class="sxs-lookup"><span data-stu-id="bea22-126">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="bea22-127">Обмен данными между объектами</span><span class="sxs-lookup"><span data-stu-id="bea22-127">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="bea22-128">Сведения о маршалировании</span><span class="sxs-lookup"><span data-stu-id="bea22-128">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="bea22-129">Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="bea22-129">Microsoft RPC</span></span>](microsoft-rpc.md)
</dt> <dt>

[<span data-ttu-id="bea22-130">Заглушка</span><span class="sxs-lookup"><span data-stu-id="bea22-130">Stub</span></span>](stub.md)
</dt> </dl>

 

 