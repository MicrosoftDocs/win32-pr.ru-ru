---
title: Ловушек
description: Заглушка, как и прокси-сервер, состоит из одной или нескольких элементов интерфейса и руководителя.
ms.assetid: ed7d5546-2d19-4055-b078-62b39d0317b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109936ae16827dce7779b080902dbca74a8dfc51
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "105693804"
---
# <a name="stub"></a><span data-ttu-id="48962-103">Ловушек</span><span class="sxs-lookup"><span data-stu-id="48962-103">Stub</span></span>

<span data-ttu-id="48962-104">Заглушка, как и прокси-сервер, состоит из одной или нескольких элементов интерфейса и руководителя.</span><span class="sxs-lookup"><span data-stu-id="48962-104">The stub, like the proxy, is made up of one or more interface pieces and a manager.</span></span> <span data-ttu-id="48962-105">Каждая заглушка интерфейса предоставляет код для распаковки параметров и кода, который вызывает один из поддерживаемых интерфейсов объекта.</span><span class="sxs-lookup"><span data-stu-id="48962-105">Each interface stub provides code to unmarshal the parameters and code that calls one of the object's supported interfaces.</span></span> <span data-ttu-id="48962-106">Каждая заглушка также предоставляет интерфейс для внутренней связи.</span><span class="sxs-lookup"><span data-stu-id="48962-106">Each stub also provides an interface for internal communication.</span></span> <span data-ttu-id="48962-107">Диспетчер заглушек отслеживает доступные заглушки интерфейса.</span><span class="sxs-lookup"><span data-stu-id="48962-107">The stub manager keeps track of the available interface stubs.</span></span>

<span data-ttu-id="48962-108">Однако существуют следующие различия между заглушкой и прокси-сервером:</span><span class="sxs-lookup"><span data-stu-id="48962-108">There are, however, the following differences between the stub and the proxy:</span></span>

-   <span data-ttu-id="48962-109">Самое важное отличие заключается в том, что заглушка представляет клиента в адресном пространстве объекта.</span><span class="sxs-lookup"><span data-stu-id="48962-109">The most important difference is that the stub represents the client in the object's address space.</span></span>
-   <span data-ttu-id="48962-110">Заглушка не реализуется как агрегатный объект, так как нет необходимости просматривать клиент как единое целое. Каждый элемент в заглушке является отдельным компонентом.</span><span class="sxs-lookup"><span data-stu-id="48962-110">The stub is not implemented as an aggregate object because there is no requirement that the client be viewed as a single unit; each piece in the stub is a separate component.</span></span>
-   <span data-ttu-id="48962-111">Заглушки интерфейса являются частными, а не общедоступными.</span><span class="sxs-lookup"><span data-stu-id="48962-111">The interface stubs are private rather than public.</span></span>
-   <span data-ttu-id="48962-112">Заглушки интерфейса реализуют [**ирпкстуббуффер**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), а не [**ирпкпроксибуффер**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).</span><span class="sxs-lookup"><span data-stu-id="48962-112">The interface stubs implement [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), not [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).</span></span>
-   <span data-ttu-id="48962-113">Вместо упаковки упакованных параметров заглушка разменяет их после маршалирования, а затем упаковывает ответ.</span><span class="sxs-lookup"><span data-stu-id="48962-113">Instead of packaging parameters to be marshaled, the stub unpackages them after they have been marshaled and then packages the reply.</span></span>

## <a name="structure-of-the-stub"></a><span data-ttu-id="48962-114">Структура заглушки</span><span class="sxs-lookup"><span data-stu-id="48962-114">Structure of the Stub</span></span>

<span data-ttu-id="48962-115">На следующей диаграмме показана структура заглушки.</span><span class="sxs-lookup"><span data-stu-id="48962-115">The following diagram shows the structure of the stub.</span></span> <span data-ttu-id="48962-116">Каждая заглушка интерфейса подключена к интерфейсу объекта.</span><span class="sxs-lookup"><span data-stu-id="48962-116">Each interface stub is connected to an interface on the object.</span></span> <span data-ttu-id="48962-117">Канал отправляет входящие сообщения в соответствующую заглушку интерфейса.</span><span class="sxs-lookup"><span data-stu-id="48962-117">The channel dispatches incoming messages to the appropriate interface stub.</span></span> <span data-ttu-id="48962-118">Все компоненты говорят по каналу через [**ирпкчаннелбуффер**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer), интерфейс, предоставляющий доступ к библиотеке времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="48962-118">All the components talk to the channel through [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer), the interface that provides access to the RPC run-time library.</span></span>

![Снимок экрана, на котором показана структура заглушки.](images/98714a22-733e-432f-bb90-408bbeecc23f.png)

## <a name="related-topics"></a><span data-ttu-id="48962-120">См. также</span><span class="sxs-lookup"><span data-stu-id="48962-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48962-121">Канал</span><span class="sxs-lookup"><span data-stu-id="48962-121">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="48962-122">Обмен данными между объектами</span><span class="sxs-lookup"><span data-stu-id="48962-122">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="48962-123">Сведения о маршалировании</span><span class="sxs-lookup"><span data-stu-id="48962-123">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="48962-124">Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="48962-124">Microsoft RPC</span></span>](microsoft-rpc.md)
</dt> <dt>

[<span data-ttu-id="48962-125">Прокси</span><span class="sxs-lookup"><span data-stu-id="48962-125">Proxy</span></span>](proxy.md)
</dt> </dl>

 

 