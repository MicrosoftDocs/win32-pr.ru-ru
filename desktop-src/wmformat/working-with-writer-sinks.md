---
title: Работа с приемниками модуля записи
description: Работа с приемниками модуля записи
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- Расширенный формат систем (ASF), приемники записи
- ASF (Расширенный системный формат), приемники записи
- Расширенный формат систем (ASF), приемники
- ASF (Расширенный системный формат), приемники
- приемники, приемники записи
- Приемники модуля записи, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5b690d9e1ab25d15f7c1e8612bf20e32f87c81
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788665"
---
# <a name="working-with-writer-sinks"></a><span data-ttu-id="1a5a5-109">Работа с приемниками модуля записи</span><span class="sxs-lookup"><span data-stu-id="1a5a5-109">Working with Writer Sinks</span></span>

<span data-ttu-id="1a5a5-110">Объект модуля записи пакета SDK Windows Media Format обрабатывает входные данные мультимедиа в виде потока битов.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-110">The writer object of the Windows Media Format SDK processes input media data into a bit stream.</span></span> <span data-ttu-id="1a5a5-111">Однако объект модуля записи не доставляет поток битов в конечное место назначения (в файл или в сетевую папку).</span><span class="sxs-lookup"><span data-stu-id="1a5a5-111">However, the writer object does not deliver the bit stream to its final destination (either to a file or a network location).</span></span> <span data-ttu-id="1a5a5-112">Чтобы записать содержимое ASF в пригодном для использования формате, необходимо использовать приемники модуля записи.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-112">To write the ASF content to a usable format, you must use writer sinks.</span></span>

<span data-ttu-id="1a5a5-113">Объект модуля записи поддерживает три типа приемников: приемники файлов, сетевые приемники и приемники push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-113">The writer object supports three types of sinks: file sinks, network sinks, and push sinks.</span></span> <span data-ttu-id="1a5a5-114">Приемник файлов записывает содержимое ASF в файл ASF на диске.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-114">A file sink writes ASF content to an ASF file on disk.</span></span> <span data-ttu-id="1a5a5-115">Сетевой приемник рассылает содержимое ASF с сетевого адреса.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-115">A network sink broadcasts ASF content from a network address.</span></span> <span data-ttu-id="1a5a5-116">Приемник push-уведомлений доставляет данные на сервер, на котором работают службы Windows Media Services, чтобы сервер мог сделать содержимое доступным для предполагаемой аудитории.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-116">A push sink delivers data to a server running Windows Media Services so that the server can make the content available to its intended audience.</span></span> <span data-ttu-id="1a5a5-117">Вы также можете создавать собственные приемники для доставки данных ASF любым способом, необходимым для приложения.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-117">You can also create your own sinks to deliver ASF data in whatever way is required by your application.</span></span> <span data-ttu-id="1a5a5-118">Сведения о сетевых приемниках и приемниках push-уведомлений см. [в разделе Отправка данных ASF по сети](sending-asf-data-over-a-network.md).</span><span class="sxs-lookup"><span data-stu-id="1a5a5-118">For information about network sinks and push sinks, see [Sending ASF Data Over a Network](sending-asf-data-over-a-network.md).</span></span> <span data-ttu-id="1a5a5-119">В оставшейся части этого раздела обсуждаются приемники модуля записи.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-119">The remainder of this section discusses writer sinks.</span></span>

<span data-ttu-id="1a5a5-120">Можно настроить один или несколько приемников для каждого используемого экземпляра модуля записи.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-120">You can configure one or more sinks for each instance of the writer you use.</span></span> <span data-ttu-id="1a5a5-121">Каждый приемник обрабатывает только одно назначение.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-121">Each sink handles only a single destination.</span></span> <span data-ttu-id="1a5a5-122">Например, если требуется записать три файла одновременно, необходимо создать и настроить отдельный приемник файлов для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-122">For example, if you want to write three files at once, you must create and configure a separate file sink for each.</span></span>

<span data-ttu-id="1a5a5-123">В следующих разделах описывается использование приемников записи.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-123">The following sections describe the use of writer sinks.</span></span>



| <span data-ttu-id="1a5a5-124">Section</span><span class="sxs-lookup"><span data-stu-id="1a5a5-124">Section</span></span>                                                                      | <span data-ttu-id="1a5a5-125">Описание</span><span class="sxs-lookup"><span data-stu-id="1a5a5-125">Description</span></span>                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="1a5a5-126">Добавление приемников в модуль записи</span><span class="sxs-lookup"><span data-stu-id="1a5a5-126">Adding Sinks to the Writer</span></span>](adding-sinks-to-the-writer.md)                 | <span data-ttu-id="1a5a5-127">Описывает добавление приемников в модуль записи.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-127">Describes how to add sinks to the writer.</span></span>                                        |
| [<span data-ttu-id="1a5a5-128">Перечисление приемников</span><span class="sxs-lookup"><span data-stu-id="1a5a5-128">Enumerating Sinks</span></span>](enumerating-sinks.md)                                   | <span data-ttu-id="1a5a5-129">Описывает, как перечислить приемники, добавленные в модуль записи.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-129">Describes how to enumerate the sinks that have been added to the writer.</span></span>         |
| [<span data-ttu-id="1a5a5-130">Получение сообщений об ошибках из приемника</span><span class="sxs-lookup"><span data-stu-id="1a5a5-130">Getting Error Messages from a Sink</span></span>](getting-error-messages-from-a-sink.md) | <span data-ttu-id="1a5a5-131">Описание настройки приемников для доставки сообщений о состоянии в приложение.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-131">Describes how to configure sinks to deliver status messages to your application.</span></span> |
| [<span data-ttu-id="1a5a5-132">Использование файловых приемников</span><span class="sxs-lookup"><span data-stu-id="1a5a5-132">Using File Sinks</span></span>](using-file-sinks.md)                                     | <span data-ttu-id="1a5a5-133">Описание использования приемника файла модуля записи для создания файла ASF на диске.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-133">Describes how to use a writer file sink to create an ASF file on disk.</span></span>           |
| [<span data-ttu-id="1a5a5-134">Использование пользовательских приемников</span><span class="sxs-lookup"><span data-stu-id="1a5a5-134">Using Custom Sinks</span></span>](using-custom-sinks.md)                                 | <span data-ttu-id="1a5a5-135">Описывает создание и использование собственных настраиваемых приемников для доставки данных ASF.</span><span class="sxs-lookup"><span data-stu-id="1a5a5-135">Describes how to create and use your own custom sinks to deliver ASF data.</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="1a5a5-136">См. также</span><span class="sxs-lookup"><span data-stu-id="1a5a5-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a5a5-137">**Интерфейс Ивмвритерадванцед**</span><span class="sxs-lookup"><span data-stu-id="1a5a5-137">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="1a5a5-138">**Интерфейс Ивмвритерсинк**</span><span class="sxs-lookup"><span data-stu-id="1a5a5-138">**IWMWriterSink Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[<span data-ttu-id="1a5a5-139">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="1a5a5-139">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




