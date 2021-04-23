---
title: Обзор сетевых интерфейсов
description: Обзор сетевых интерфейсов
ms.assetid: 7aa7ff1b-9c81-4fee-afa9-2a9eed457360
keywords:
- Windows Media Format SDK, сетевые интерфейсы
- Windows Media Format SDK, интерфейсы
- Расширенный системный формат (ASF), сетевые интерфейсы
- ASF (Расширенный системный формат), сетевые интерфейсы
- Расширенный системный формат (ASF), список интерфейсов для сетевых функций
- ASF (Расширенный системный формат), список интерфейсов для сетевых функций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd1c235e7e8b36964993bb24ce30977446d9af8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789246"
---
# <a name="overview-of-networking-interfaces"></a><span data-ttu-id="de63a-109">Обзор сетевых интерфейсов</span><span class="sxs-lookup"><span data-stu-id="de63a-109">Overview of Networking Interfaces</span></span>

<span data-ttu-id="de63a-110">Сетевые возможности этого пакета SDK поддерживаются с помощью методов следующих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="de63a-110">The networking features of this SDK are supported through methods of the following interfaces.</span></span>



| <span data-ttu-id="de63a-111">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="de63a-111">Interface</span></span>                                                  | <span data-ttu-id="de63a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="de63a-112">Description</span></span>                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de63a-113">**ивмклиентконнектионс**</span><span class="sxs-lookup"><span data-stu-id="de63a-113">**IWMClientConnections**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)       | <span data-ttu-id="de63a-114">Возвращает сведения о клиентах, подключенных к сетевому приемнику.</span><span class="sxs-lookup"><span data-stu-id="de63a-114">Gets information about the clients connected to a network sink.</span></span>                                                                                       |
| [<span data-ttu-id="de63a-115">**IWMClientConnections2**</span><span class="sxs-lookup"><span data-stu-id="de63a-115">**IWMClientConnections2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2)     | <span data-ttu-id="de63a-116">Предоставляет метод для получения сведений о клиенте, подключенном к приемнику сети записи.</span><span class="sxs-lookup"><span data-stu-id="de63a-116">Provides a method to get information about a client attached to a writer network sink.</span></span> <span data-ttu-id="de63a-117">Этот интерфейс расширяет интерфейс **ивмклиентконнектионс** .</span><span class="sxs-lookup"><span data-stu-id="de63a-117">This interface extends the **IWMClientConnections** interface.</span></span> |
| [<span data-ttu-id="de63a-118">**ивмкредентиалкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="de63a-118">**IWMCredentialCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)     | <span data-ttu-id="de63a-119">Предоставляет метод обратного вызова для получения учетных данных пользователя при доступе к удаленному сайту.</span><span class="sxs-lookup"><span data-stu-id="de63a-119">Provides a callback method to acquire user credentials when accessing a remote site.</span></span>                                                                  |
| [<span data-ttu-id="de63a-120">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="de63a-120">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)           | <span data-ttu-id="de63a-121">Предоставляет дополнительные методы для объекта Reader.</span><span class="sxs-lookup"><span data-stu-id="de63a-121">Provides advanced methods on the reader object.</span></span>                                                                                                       |
| [<span data-ttu-id="de63a-122">**IWMReaderAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="de63a-122">**IWMReaderAdvanced3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)           | <span data-ttu-id="de63a-123">Расширяет интерфейс **IWMReaderAdvanced2** .</span><span class="sxs-lookup"><span data-stu-id="de63a-123">Extends the **IWMReaderAdvanced2** interface.</span></span>                                                                                                         |
| [<span data-ttu-id="de63a-124">**IWMReaderAdvanced4**</span><span class="sxs-lookup"><span data-stu-id="de63a-124">**IWMReaderAdvanced4**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)           | <span data-ttu-id="de63a-125">Расширяет интерфейс **IWMReaderAdvanced3** .</span><span class="sxs-lookup"><span data-stu-id="de63a-125">Extends the **IWMReaderAdvanced3** interface.</span></span>                                                                                                         |
| [<span data-ttu-id="de63a-126">**ивмреадернетворкконфиг**</span><span class="sxs-lookup"><span data-stu-id="de63a-126">**IWMReaderNetworkConfig**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)   | <span data-ttu-id="de63a-127">Настраивает параметры сети для объекта модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="de63a-127">Configures the network settings on the reader object.</span></span>                                                                                                 |
| [<span data-ttu-id="de63a-128">**IWMReaderNetworkConfig2**</span><span class="sxs-lookup"><span data-stu-id="de63a-128">**IWMReaderNetworkConfig2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) | <span data-ttu-id="de63a-129">Настраивает дополнительные параметры сети для объекта Reader.</span><span class="sxs-lookup"><span data-stu-id="de63a-129">Configures additional network settings on the reader object.</span></span> <span data-ttu-id="de63a-130">Этот интерфейс расширяет интерфейс **ивмреадернетворкконфиг** .</span><span class="sxs-lookup"><span data-stu-id="de63a-130">This interface extends the **IWMReaderNetworkConfig** interface.</span></span>                         |
| [<span data-ttu-id="de63a-131">**ивмвритернетворксинк**</span><span class="sxs-lookup"><span data-stu-id="de63a-131">**IWMWriterNetworkSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)       | <span data-ttu-id="de63a-132">Настраивает объект сетевого приемника, который используется для записи цифрового мультимедиа в сеть.</span><span class="sxs-lookup"><span data-stu-id="de63a-132">Configures the network sink object, which is used to write digital media to a network.</span></span>                                                                |
| [<span data-ttu-id="de63a-133">**ивмвритерпушсинк**</span><span class="sxs-lookup"><span data-stu-id="de63a-133">**IWMWriterPushSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)             | <span data-ttu-id="de63a-134">Настраивает объект приемника push-уведомлений, который используется для распространения цифровых носителей в точки публикации.</span><span class="sxs-lookup"><span data-stu-id="de63a-134">Configures the push sink object, which is used to distribute digital media to publishing points.</span></span>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="de63a-135">См. также</span><span class="sxs-lookup"><span data-stu-id="de63a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de63a-136">**Реализация функций сети**</span><span class="sxs-lookup"><span data-stu-id="de63a-136">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> </dl>

 

 




