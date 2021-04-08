---
title: Объект приемника файлов модуля записи
description: Объект приемника файлов модуля записи
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- Пакет SDK для формата Windows Media, объекты приемника файлов модуля записи
- Расширенные системные форматы (ASF), объекты приемника файлов модуля записи
- ASF (Расширенный системный формат), объекты приемника файлов модуля записи
- объекты, объекты приемников файлов модуля записи
- объекты приемника файлов модуля записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82009e5be74cfc23e687001a2a81cd4546812af9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104069702"
---
# <a name="writer-file-sink-object"></a><span data-ttu-id="b0883-108">Объект приемника файлов модуля записи</span><span class="sxs-lookup"><span data-stu-id="b0883-108">Writer File Sink Object</span></span>

<span data-ttu-id="b0883-109">Объект приемника файла модуля записи используется при записи выходных данных Windows Media в файл.</span><span class="sxs-lookup"><span data-stu-id="b0883-109">The writer file sink object is used when writing Windows Media output to a file.</span></span>

<span data-ttu-id="b0883-110">Объект приемника файла модуля записи создается функцией [**вмкреатевритерфилесинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink), которая устанавливает указатель на интерфейс **ивмвритерфилесинк** .</span><span class="sxs-lookup"><span data-stu-id="b0883-110">The writer file sink object is created by the function [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink), which sets a pointer to an **IWMWriterFileSink** interface.</span></span> <span data-ttu-id="b0883-111">Другие интерфейсы объекта приемника файла модуля записи можно получить, вызвав метод **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="b0883-111">The other interfaces of the writer file sink object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="b0883-112">Объект приемника файла модуля записи поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="b0883-112">The following interfaces are supported by the writer file sink object.</span></span>



| <span data-ttu-id="b0883-113">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="b0883-113">Interface</span></span>                                          | <span data-ttu-id="b0883-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b0883-114">Description</span></span>                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0883-115">**ивмрегистеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b0883-115">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | <span data-ttu-id="b0883-116">Позволяет приложению получать сообщения о состоянии от объекта.</span><span class="sxs-lookup"><span data-stu-id="b0883-116">Enables the application to get status messages from the object.</span></span>                                                                 |
| [<span data-ttu-id="b0883-117">**ивмвритерфилесинк**</span><span class="sxs-lookup"><span data-stu-id="b0883-117">**IWMWriterFileSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | <span data-ttu-id="b0883-118">Открывает файл, в который объект модуля записи может записывать данные.</span><span class="sxs-lookup"><span data-stu-id="b0883-118">Opens a file to which the writer object can write data.</span></span>                                                                         |
| [<span data-ttu-id="b0883-119">**IWMWriterFileSink2**</span><span class="sxs-lookup"><span data-stu-id="b0883-119">**IWMWriterFileSink2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | <span data-ttu-id="b0883-120">Обеспечивает расширенное управление объектом приемника файла.</span><span class="sxs-lookup"><span data-stu-id="b0883-120">Provides extended management of a file sink object.</span></span> <span data-ttu-id="b0883-121">Наследует все методы **ивмвритерфилесинк**.</span><span class="sxs-lookup"><span data-stu-id="b0883-121">Inherits all of the methods of **IWMWriterFileSink**.</span></span>                       |
| [<span data-ttu-id="b0883-122">**IWMWriterFileSink3**</span><span class="sxs-lookup"><span data-stu-id="b0883-122">**IWMWriterFileSink3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | <span data-ttu-id="b0883-123">Предоставляет дополнительные возможности для записи файлов.</span><span class="sxs-lookup"><span data-stu-id="b0883-123">Provides additional options for writing files.</span></span> <span data-ttu-id="b0883-124">Наследует все методы **ивмвритерфилесинк** и **IWMWriterFileSink2**.</span><span class="sxs-lookup"><span data-stu-id="b0883-124">Inherits all of the methods of **IWMWriterFileSink** and **IWMWriterFileSink2**.</span></span> |
| [<span data-ttu-id="b0883-125">**ивмвритерсинк**</span><span class="sxs-lookup"><span data-stu-id="b0883-125">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | <span data-ttu-id="b0883-126">Выделяет память, определяет, работает ли приемник в режиме реального времени, и обрабатывает несколько функций обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b0883-126">Allocates memory, determines whether the sink is operating in real time, and handles several callback functions.</span></span>                |



 

<span data-ttu-id="b0883-127">Для отслеживания хода выполнения объекта приемника файла модуля записи в приложении должен быть реализован следующий интерфейс обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b0883-127">The following callback interface should be implemented by the application to track the progress of a writer file sink object.</span></span>



| <span data-ttu-id="b0883-128">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="b0883-128">Interface</span></span>                                      | <span data-ttu-id="b0883-129">Описание</span><span class="sxs-lookup"><span data-stu-id="b0883-129">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="b0883-130">**ивмстатускаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b0883-130">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="b0883-131">Требуется, если информация о состоянии должна быть передана ведущему приложению.</span><span class="sxs-lookup"><span data-stu-id="b0883-131">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b0883-132">См. также</span><span class="sxs-lookup"><span data-stu-id="b0883-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0883-133">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="b0883-133">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="b0883-134">**Работа с приемниками модуля записи**</span><span class="sxs-lookup"><span data-stu-id="b0883-134">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




