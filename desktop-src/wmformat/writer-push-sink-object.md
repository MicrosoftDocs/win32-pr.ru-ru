---
title: Объект приемника push-уведомлений
description: Объект приемника push-уведомлений
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- Windows Media Format SDK, объекты приемника push-уведомлений
- Расширенный системный формат (ASF), объекты приемника push-уведомлений
- ASF (Расширенный системный формат), объекты приемника push-уведомлений
- объекты, объекты приемника push-уведомлений
- объекты приемника push-уведомлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19ea9855219dcb4572ef187ad93e03696b88492
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987187"
---
# <a name="writer-push-sink-object"></a><span data-ttu-id="069bd-108">Объект приемника push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="069bd-108">Writer Push Sink Object</span></span>

<span data-ttu-id="069bd-109">Объект приемника push-уведомлений распространяет цифровые носители в точки публикации.</span><span class="sxs-lookup"><span data-stu-id="069bd-109">The writer push sink object distributes digital media to publishing points.</span></span> <span data-ttu-id="069bd-110">Например, динамический концерт может быть закодирован на одном сервере, а затем доставлен или *отправлен* на несколько других серверов, которые фактически будут передавать содержимое пользователям.</span><span class="sxs-lookup"><span data-stu-id="069bd-110">For example, a live concert can be encoded by a single server and then delivered, or *pushed*, to several other servers that will actually stream the content to users.</span></span>

<span data-ttu-id="069bd-111">Объект приемника push-уведомлений создается функцией [**вмкреатевритерпушсинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink), которая устанавливает указатель на интерфейс **ивмвритерпушсинк** .</span><span class="sxs-lookup"><span data-stu-id="069bd-111">A writer push sink object is created by the function [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink), which sets a pointer to an **IWMWriterPushSink** interface.</span></span> <span data-ttu-id="069bd-112">Другие интерфейсы, поддерживаемые объектом, перечисленные в следующей таблице, можно получить, вызвав метод **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="069bd-112">The other interfaces supported by the object, listed in the following table, can be obtained by calling the **QueryInterface** method.</span></span>



| <span data-ttu-id="069bd-113">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="069bd-113">Interface</span></span>                                          | <span data-ttu-id="069bd-114">Описание</span><span class="sxs-lookup"><span data-stu-id="069bd-114">Description</span></span>                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="069bd-115">**ивмрегистеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="069bd-115">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | <span data-ttu-id="069bd-116">Позволяет приложению получать сообщения о состоянии от объекта.</span><span class="sxs-lookup"><span data-stu-id="069bd-116">Enables the application to get status messages from the object.</span></span>                                                  |
| [<span data-ttu-id="069bd-117">**ивмвритерпушсинк**</span><span class="sxs-lookup"><span data-stu-id="069bd-117">**IWMWriterPushSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | <span data-ttu-id="069bd-118">Управляет сеансом распространения push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="069bd-118">Manages a push distribution session.</span></span>                                                                             |
| [<span data-ttu-id="069bd-119">**ивмвритерсинк**</span><span class="sxs-lookup"><span data-stu-id="069bd-119">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | <span data-ttu-id="069bd-120">Выделяет память, определяет, работает ли приемник в режиме реального времени, и предоставляет несколько функций обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="069bd-120">Allocates memory, determines whether the sink is operating in real time, and exposes several callback functions.</span></span> |



 

<span data-ttu-id="069bd-121">В приложении можно реализовать следующий интерфейс обратного вызова для отслеживания хода выполнения объекта приемника push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="069bd-121">The following callback interface can be implemented by the application to track the progress of a writer push sink object.</span></span>



| <span data-ttu-id="069bd-122">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="069bd-122">Interface</span></span>                                      | <span data-ttu-id="069bd-123">Описание</span><span class="sxs-lookup"><span data-stu-id="069bd-123">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="069bd-124">**ивмстатускаллбакк**</span><span class="sxs-lookup"><span data-stu-id="069bd-124">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="069bd-125">Требуется, если информация о состоянии должна быть передана ведущему приложению.</span><span class="sxs-lookup"><span data-stu-id="069bd-125">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="069bd-126">См. также</span><span class="sxs-lookup"><span data-stu-id="069bd-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="069bd-127">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="069bd-127">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="069bd-128">**Отправка данных ASF в точку публикации**</span><span class="sxs-lookup"><span data-stu-id="069bd-128">**Sending ASF Data to a Publishing Point**</span></span>](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[<span data-ttu-id="069bd-129">**Работа с приемниками модуля записи**</span><span class="sxs-lookup"><span data-stu-id="069bd-129">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




