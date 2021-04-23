---
title: Объект приемника сети модуля записи
description: Объект приемника сети модуля записи
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- Windows Media Format SDK, объекты приемника сети записи
- Расширенный системный формат (ASF), объекты приемника сети модуля записи
- ASF (Расширенный системный формат), объекты приемника сети модуля записи
- объекты, объекты приемника сети модуля записи
- объекты приемника сети записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85af356c1d326ddaaf3703ca87c3b7bdd1628b9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104133586"
---
# <a name="writer-network-sink-object"></a><span data-ttu-id="62348-108">Объект приемника сети модуля записи</span><span class="sxs-lookup"><span data-stu-id="62348-108">Writer Network Sink Object</span></span>

<span data-ttu-id="62348-109">Объект приемника сети записи используется для записи цифрового мультимедиа в сеть.</span><span class="sxs-lookup"><span data-stu-id="62348-109">The writer network sink object is used to write digital media to a network.</span></span>

<span data-ttu-id="62348-110">Объект приемника сети записи создается функцией [**вмкреатевритернетворксинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink), которая устанавливает указатель на интерфейс **ивмвритернетворксинк** .</span><span class="sxs-lookup"><span data-stu-id="62348-110">The writer network sink object is created by the function [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink), which sets a pointer to an **IWMWriterNetworkSink** interface.</span></span> <span data-ttu-id="62348-111">Другие интерфейсы объекта приемника сети модуля записи можно получить, вызвав метод **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="62348-111">The other interfaces of the writer network sink object can be obtained by calling the **QueryInterface** method.</span></span>



| <span data-ttu-id="62348-112">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="62348-112">Interface</span></span>                                              | <span data-ttu-id="62348-113">Описание</span><span class="sxs-lookup"><span data-stu-id="62348-113">Description</span></span>                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62348-114">**ивмклиентконнектионс**</span><span class="sxs-lookup"><span data-stu-id="62348-114">**IWMClientConnections**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | <span data-ttu-id="62348-115">Собирает сведения о подключенных клиентах.</span><span class="sxs-lookup"><span data-stu-id="62348-115">Collects information on connected clients.</span></span>                                                                                                                                                                      |
| [<span data-ttu-id="62348-116">**IWMClientConnections2**</span><span class="sxs-lookup"><span data-stu-id="62348-116">**IWMClientConnections2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | <span data-ttu-id="62348-117">Получает дополнительные сведения о клиенте.</span><span class="sxs-lookup"><span data-stu-id="62348-117">Retrieves advanced client information.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="62348-118">**ивмрегистеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="62348-118">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | <span data-ttu-id="62348-119">Позволяет приложению получать сообщения о состоянии от объекта.</span><span class="sxs-lookup"><span data-stu-id="62348-119">Enables the application to get status messages from the object.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="62348-120">**ивмвритернетворксинк**</span><span class="sxs-lookup"><span data-stu-id="62348-120">**IWMWriterNetworkSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | <span data-ttu-id="62348-121">Открывает и закрывает порты, устанавливает и получает максимальное количество клиентов, которые могут подключаться к объекту приемника, задает сетевой протокол, используемый объектом модуля записи, и выполняет другие расширенные функции.</span><span class="sxs-lookup"><span data-stu-id="62348-121">Opens and closes ports, sets and retrieves the maximum number of clients that can connect to the sink object, sets the network protocol to be used by the writer object, and performs other advanced functions.</span></span> |
| [<span data-ttu-id="62348-122">**ивмвритерсинк**</span><span class="sxs-lookup"><span data-stu-id="62348-122">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | <span data-ttu-id="62348-123">Выделяет память, определяет, работает ли приемник в режиме реального времени, и обрабатывает несколько функций обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="62348-123">Allocates memory, determines whether the sink is operating in real time, and handles several callback functions.</span></span>                                                                                                |



 

<span data-ttu-id="62348-124">Следующий интерфейс обратного вызова может быть реализован приложением для отслеживания хода выполнения объекта приемника сети записи.</span><span class="sxs-lookup"><span data-stu-id="62348-124">The following callback interface can be implemented by the application to track the progress of a writer network sink object.</span></span>



| <span data-ttu-id="62348-125">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="62348-125">Interface</span></span>                                      | <span data-ttu-id="62348-126">Описание</span><span class="sxs-lookup"><span data-stu-id="62348-126">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="62348-127">**ивмстатускаллбакк**</span><span class="sxs-lookup"><span data-stu-id="62348-127">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="62348-128">Требуется, если информация о состоянии должна быть передана ведущему приложению.</span><span class="sxs-lookup"><span data-stu-id="62348-128">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="62348-129">См. также</span><span class="sxs-lookup"><span data-stu-id="62348-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62348-130">**Трансляция данных ASF**</span><span class="sxs-lookup"><span data-stu-id="62348-130">**Broadcasting ASF Data**</span></span>](broadcasting-asf-data.md)
</dt> <dt>

[<span data-ttu-id="62348-131">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="62348-131">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="62348-132">**Работа с приемниками модуля записи**</span><span class="sxs-lookup"><span data-stu-id="62348-132">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




