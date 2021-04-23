---
title: Обработка ошибок (пакет SDK для проигрывателя Windows Media)
description: Обработка ошибок
ms.assetid: f0567c77-a855-4b93-9fb7-a36cde63859f
keywords:
- Проигрыватель Windows Media, обработка ошибок
- Объектная модель проигрывателя Windows Media, обработка ошибок
- Объектная модель, обработка ошибок
- Элемент управления ActiveX проигрывателя Windows Media, обработка ошибок
- Элемент управления ActiveX, обработка ошибок
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, обработка ошибок
- Проигрыватель Windows Media Mobile, обработка ошибок
- руководством по миграции, обработке ошибок
- Обработка ошибок в объектной модели
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3b96e04d24009ee4b7e5819fdb26dfd6effd63
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134859"
---
# <a name="error-handling-windows-media-player-sdk"></a><span data-ttu-id="81501-112">Обработка ошибок (пакет SDK для проигрывателя Windows Media)</span><span class="sxs-lookup"><span data-stu-id="81501-112">Error Handling (Windows Media Player SDK)</span></span>

<span data-ttu-id="81501-113">Элемент управления ActiveX проигрывателя Windows Media 6,4 обеспечивает обработку ошибок по умолчанию, отображая сообщения об ошибках в диалоговых окнах и в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="81501-113">The Windows Media Player 6.4 ActiveX control provides default error handling by displaying error messages in dialog boxes and on the status bar.</span></span> <span data-ttu-id="81501-114">Можно также предоставить настраиваемую обработку ошибок, обрабатывая ошибки в скрипте.</span><span class="sxs-lookup"><span data-stu-id="81501-114">You can also provide custom error handling by processing errors in your script.</span></span> <span data-ttu-id="81501-115">Обработка ошибок связана с событиями, что означает получение уведомления для каждой ошибки, и необходимо решить, как обрабатывать каждое событие ошибки при возникновении.</span><span class="sxs-lookup"><span data-stu-id="81501-115">Error handling is event driven, which means you receive a notification for each error, and must decide how to deal with each error event when it occurs.</span></span> <span data-ttu-id="81501-116">Дополнительные сведения об обработке ошибок с помощью объектной модели версии 6,4 см. в разделе Обработка ошибок статьи объектная модель проигрывателя версии 6,4, которая является частью пакета SDK для проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="81501-116">For more information about handling errors using the version 6.4 object model, see the Error Handling section of the Version 6.4 Player Object Model Guide, which is part of the Windows Media Player SDK.</span></span>

<span data-ttu-id="81501-117">Объектная модель проигрывателя Windows Media 7 или более поздней версии предоставляет объект **Error** и объект **ерроритем** для обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="81501-117">The Windows Media Player 7 or later object model provides the **Error** object and the **ErrorItem** object to handle errors.</span></span> <span data-ttu-id="81501-118">Эти два объекта работают вместе, чтобы обеспечить механизм обработки ошибок, обеспечивающий полное и гибкое управление процессом обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="81501-118">These two objects work together to provide you with an error handling mechanism that gives you complete and flexible control of the error handling process.</span></span> <span data-ttu-id="81501-119">Объект **Error** предоставляет доступ к коллекции объектов **ерроритем** ; Каждый объект **ерроритем** предоставляет сведения об отдельном сообщении об ошибке.</span><span class="sxs-lookup"><span data-stu-id="81501-119">The **Error** object provides access to a collection of **ErrorItem** objects; each **ErrorItem** object provides details about an individual error message.</span></span>

<span data-ttu-id="81501-120">При возникновении ошибки сведения об ошибке помещаются в очередь ошибок.</span><span class="sxs-lookup"><span data-stu-id="81501-120">When an error occurs, the error information is posted to an error queue.</span></span> <span data-ttu-id="81501-121">Очередь представляет собой коллекцию объектов **ерроритем** .</span><span class="sxs-lookup"><span data-stu-id="81501-121">The queue is a collection of **ErrorItem** objects.</span></span> <span data-ttu-id="81501-122">При добавлении каждой ошибки в очередь она связывается с номером индекса (начиная с нуля), который можно использовать для обнаружения конкретного объекта **ерроритем** .</span><span class="sxs-lookup"><span data-stu-id="81501-122">As each error is added to the queue, it is associated with an index number (beginning with zero) that can be used to identify the particular **ErrorItem** object.</span></span> <span data-ttu-id="81501-123">*Ошибка*. Свойство **ерроркаунт** извлекает количество ошибок в очереди ошибок.</span><span class="sxs-lookup"><span data-stu-id="81501-123">The *Error*.**errorCount** property retrieves the number of errors in the error queue.</span></span> <span data-ttu-id="81501-124">Поскольку нумерация индексов отсчитывается от нуля, последняя ошибка, отправленная в очередь, всегда будет иметь значение индекса, равное *Error*. **ерроркаунт** минус один.</span><span class="sxs-lookup"><span data-stu-id="81501-124">Since the index numbers are zero-based, the most recent error posted to the queue will always have an index value equal to *Error*.**errorCount** minus one.</span></span>

<span data-ttu-id="81501-125">Можно создать обработчик событий ошибок для проигрывателя Windows Media с помощью скрипта.</span><span class="sxs-lookup"><span data-stu-id="81501-125">You can create an error event handler for Windows Media Player using script.</span></span> <span data-ttu-id="81501-126">В следующем примере JScript показано, как получить последний ошибочный элемент из очереди ошибок и отобразить код ошибки и описание ошибки с помощью объектной модели проигрывателя Windows Media 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="81501-126">The following JScript example shows how to retrieve the most recent error item from the error queue and display the error code and error description using the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="81501-127">Объект **Player** создан с идентификатором "WMP9".</span><span class="sxs-lookup"><span data-stu-id="81501-127">The **Player** object was created with ID = "WMP9".</span></span>


```C++
<!-- Create an error event handler for Windows Media Player 7 or later errors. -->
<SCRIPT  LANGUAGE = "JScript"  FOR = WMP9  EVENT = error()>

// Store the number of errors in the error queue.
var max = WMP9.error.errorCount;

// Retrieve most recent ErrorItem object.
var err = WMP9.error.item(max-1)

// Store the error code number.
var errNum = err.errorCode;

// Store the error description string.
var errDesc = err.errorDescription;

// Build a message string to notify the user.
var msg = "Error number: " + errNum + "\n";
msg += "Error description: " + errDesc;

// Display the message box.
alert(msg);

</SCRIPT>

```



<span data-ttu-id="81501-128">Объект **Error** имеет два дополнительных метода, которые можно использовать.</span><span class="sxs-lookup"><span data-stu-id="81501-128">The **Error** object has two additional methods that you can use.</span></span> <span data-ttu-id="81501-129">*Ошибка*. метод **клеарерроркуеуе** позволяет удалить все ошибки из очереди ошибок и сбросить номер индекса до нуля.</span><span class="sxs-lookup"><span data-stu-id="81501-129">The *Error*.**clearErrorQueue** method allows you to remove all the errors from the error queue and reset the index number to zero.</span></span> <span data-ttu-id="81501-130">Вы полностью контролируете этот процесс; можно хранить ошибки в очереди до тех пор, пока они должны быть доступны, а затем очищать очередь по завершении обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="81501-130">You have complete control over this process; you can keep errors in the queue for as long as you need them to be available, and then empty the queue when you're finished handling the errors.</span></span>

<span data-ttu-id="81501-131">*Ошибка*. метод веб- **справки** позволяет отображать наиболее актуальные сведения об ошибках для пользователя через Интернет.</span><span class="sxs-lookup"><span data-stu-id="81501-131">The *Error*.**webHelp** method provides a way to display the most current error information to the user by using the Internet.</span></span> <span data-ttu-id="81501-132">При вызове этот метод передает все релевантные сведения о первой ошибке в очереди (с нулевым индексом) в веб-справку проигрывателя Windows Media, которая отображает дополнительные сведения об ошибке в текущем окне браузера.</span><span class="sxs-lookup"><span data-stu-id="81501-132">When called, this method transfers all relevant information about the first error in the queue (the one with index zero) to Microsoft Windows Media Player Web Help, which displays further information about the error in the current browser window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81501-133">См. также</span><span class="sxs-lookup"><span data-stu-id="81501-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81501-134">**Объект Error**</span><span class="sxs-lookup"><span data-stu-id="81501-134">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="81501-135">**Объект Ерроритем**</span><span class="sxs-lookup"><span data-stu-id="81501-135">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="81501-136">**Руководством по миграции объектной модели**</span><span class="sxs-lookup"><span data-stu-id="81501-136">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




