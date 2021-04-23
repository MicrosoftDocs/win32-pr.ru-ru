---
title: Реализация сообщений модуля чтения в обратном вызове OnStatus
description: Реализация сообщений модуля чтения в обратном вызове OnStatus
ms.assetid: f0535e02-a283-48bf-9242-ebcc17a6fb66
keywords:
- Расширенный системный формат (ASF), реализация сообщений для чтения
- ASF (Расширенный системный формат), реализация сообщений для чтения
- Расширенный формат систем (ASF), обратный вызов OnStatus
- ASF (Расширенный системный формат), обратный вызов OnStatus
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- асинхронные читатели, реализация сообщений чтения
- Метод обратного вызова OnStatus, реализация сообщений читателя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384cf8df8628efa9bd2cc17920dc6b1303655691
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069556"
---
# <a name="to-implement-reader-messages-in-the-onstatus-callback"></a><span data-ttu-id="11659-111">Реализация сообщений модуля чтения в обратном вызове OnStatus</span><span class="sxs-lookup"><span data-stu-id="11659-111">To Implement Reader Messages in the OnStatus Callback</span></span>

<span data-ttu-id="11659-112">Чтобы использовать асинхронное средство чтения для доставки содержимого из ASF-файла, необходимо реализовать как минимум два метода обратного вызова — [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) и [**ивмреадеркаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span><span class="sxs-lookup"><span data-stu-id="11659-112">To use the asynchronous reader to deliver content from an ASF file, you must implement a minimum of two callback methods, [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) and [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span></span> <span data-ttu-id="11659-113">В этом разделе описывается, как реализовать **ивмстатускаллбакк:: OnStatus** для получения сообщений о состоянии, отправленных модулем чтения, и реагирования на них.</span><span class="sxs-lookup"><span data-stu-id="11659-113">This section describes how to implement **IWMStatusCallback::OnStatus** to receive and respond to status messages sent by the reader.</span></span> <span data-ttu-id="11659-114">**OnStatus** используется другими объектами в пакете SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="11659-114">**OnStatus** is used by other objects in the Windows Media Format SDK.</span></span> <span data-ttu-id="11659-115">Общие сведения о **OnStatus** см. [в разделе Использование обратного вызова OnStatus](using-the-onstatus-callback.md).</span><span class="sxs-lookup"><span data-stu-id="11659-115">For general information about **OnStatus**, see [Using the OnStatus Callback](using-the-onstatus-callback.md).</span></span>

<span data-ttu-id="11659-116">При использовании асинхронного модуля чтения необходимо выполнить перехват следующих сообщений в **ивмстатускаллбакк:: OnStatus**.</span><span class="sxs-lookup"><span data-stu-id="11659-116">When using the asynchronous reader, you must trap the following messages in **IWMStatusCallback::OnStatus**.</span></span>



| <span data-ttu-id="11659-117">Сообщение о состоянии</span><span class="sxs-lookup"><span data-stu-id="11659-117">Status message</span></span> | <span data-ttu-id="11659-118">Описание</span><span class="sxs-lookup"><span data-stu-id="11659-118">Description</span></span>                                     |
|----------------|-------------------------------------------------|
| <span data-ttu-id="11659-119">ВМТ \_ открыт</span><span class="sxs-lookup"><span data-stu-id="11659-119">WMT\_OPENED</span></span>    | <span data-ttu-id="11659-120">Отправляется при завершении операций открытия файла.</span><span class="sxs-lookup"><span data-stu-id="11659-120">Sent when file opening operations are complete.</span></span> |
| <span data-ttu-id="11659-121">ВМТ \_ закрыт</span><span class="sxs-lookup"><span data-stu-id="11659-121">WMT\_CLOSED</span></span>    | <span data-ttu-id="11659-122">Посылается при завершении операций закрытия файла.</span><span class="sxs-lookup"><span data-stu-id="11659-122">Sent when file closing operations are complete.</span></span> |



 

<span data-ttu-id="11659-123">Для управления выполнением приложения чтения следует использовать перечисленные выше сообщения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="11659-123">You should use the status messages listed above to control execution of your reading application.</span></span> <span data-ttu-id="11659-124">Например, необходимо дождаться получения открытого сообщения **ВМТ \_** для запуска средства чтения или вызвать другие методы, требующие готовности файла для чтения.</span><span class="sxs-lookup"><span data-stu-id="11659-124">For example, you must wait until receiving the **WMT\_OPENED** message to start the reader or call other methods that require the reader to have a file ready.</span></span> <span data-ttu-id="11659-125">Часто приложения, созданные с помощью асинхронного модуля чтения, используют событие для сигнализации о завершении асинхронных вызовов и продолжают обработку.</span><span class="sxs-lookup"><span data-stu-id="11659-125">Frequently, applications built with the asynchronous reader use an event to signal the completion of asynchronous calls and proceed with processing.</span></span> <span data-ttu-id="11659-126">Дополнительные сведения об использовании событий для сигнализации о завершении операций см. [в разделе Использование событий с асинхронными вызовами](using-events-with-asynchronous-calls.md).</span><span class="sxs-lookup"><span data-stu-id="11659-126">For more information about using events for signaling completion of operations, see [Using Events with Asynchronous Calls](using-events-with-asynchronous-calls.md).</span></span>

<span data-ttu-id="11659-127">Многие другие сообщения отправляются в **OnStatus** объектом Reader, чтобы приложение отвечало на состояние операций чтения.</span><span class="sxs-lookup"><span data-stu-id="11659-127">Many other messages are sent to **OnStatus** by the reader object to enable the application to respond to the status of reading operations.</span></span> <span data-ttu-id="11659-128">Возможные значения сообщения о состоянии определены в типе перечисления [**\_ состояния ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .</span><span class="sxs-lookup"><span data-stu-id="11659-128">The possible status message values are defined in the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11659-129">См. также</span><span class="sxs-lookup"><span data-stu-id="11659-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11659-130">**Ивмстатускаллбакк:: OnStatus**</span><span class="sxs-lookup"><span data-stu-id="11659-130">**IWMStatusCallback::OnStatus**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)
</dt> <dt>

[<span data-ttu-id="11659-131">**Чтение файлов с помощью асинхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="11659-131">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="11659-132">**Использование обратного вызова OnStatus**</span><span class="sxs-lookup"><span data-stu-id="11659-132">**Using the OnStatus Callback**</span></span>](using-the-onstatus-callback.md)
</dt> </dl>

 

 




