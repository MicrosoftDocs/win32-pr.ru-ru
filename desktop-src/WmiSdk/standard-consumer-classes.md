---
description: В следующей таблице перечислены классы для предустановленных постоянных потребителей WMI.
ms.assetid: 1239ea25-2835-4546-b66d-20a83704653e
ms.tgt_platform: multiple
title: Классы стандартных потребителей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a5033077f3dabf90d3e935b2dfec9fad892f630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272751"
---
# <a name="standard-consumer-classes"></a><span data-ttu-id="e1eec-103">Классы стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="e1eec-103">Standard Consumer Classes</span></span>

<span data-ttu-id="e1eec-104">В следующей таблице перечислены классы для предустановленных постоянных потребителей WMI.</span><span class="sxs-lookup"><span data-stu-id="e1eec-104">The following table lists the classes for WMI preinstalled permanent consumers.</span></span> <span data-ttu-id="e1eec-105">Можно создать экземпляры этих классов, чтобы предоставить постоянный класс потребителя для предоставления логического потребителя, реагирующего на события, заданные в фильтре.</span><span class="sxs-lookup"><span data-stu-id="e1eec-105">You can create instances of these classes to provide the permanent consumer class to supply the logical consumer that responds when triggered by the events specified in the filter.</span></span> <span data-ttu-id="e1eec-106">Например, используйте класс [**активескриптевентконсумер**](activescripteventconsumer.md) для определения скрипта, который выполняется при наступлении указанного события.</span><span class="sxs-lookup"><span data-stu-id="e1eec-106">For example, use the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class to define the script that executes when a specified event occurs.</span></span>

<span data-ttu-id="e1eec-107">Дополнительные сведения см. [в разделе Мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md) и [событий мониторинга](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="e1eec-107">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md) and [Monitoring Events](monitoring-events.md).</span></span>



| <span data-ttu-id="e1eec-108">Класс</span><span class="sxs-lookup"><span data-stu-id="e1eec-108">Class</span></span>                                                                        | <span data-ttu-id="e1eec-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e1eec-109">Description</span></span>                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1eec-110">**активескриптевентконсумер**</span><span class="sxs-lookup"><span data-stu-id="e1eec-110">**ActiveScriptEventConsumer**</span></span>](activescripteventconsumer.md)               | <span data-ttu-id="e1eec-111">Выполняет предопределенный скрипт на произвольном языке скриптов при доставке события в него.</span><span class="sxs-lookup"><span data-stu-id="e1eec-111">Executes a predefined script in an arbitrary scripting language when an event is delivered to it.</span></span><br/> <span data-ttu-id="e1eec-112">Пример. [выполнение скрипта на основе события](running-a-script-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="e1eec-112">Example: [Running a Script Based on an Event](running-a-script-based-on-an-event.md)</span></span><br/>                                         |
| [<span data-ttu-id="e1eec-113">**коммандлинивентконсумер**</span><span class="sxs-lookup"><span data-stu-id="e1eec-113">**CommandLineEventConsumer**</span></span>](commandlineeventconsumer.md)                 | <span data-ttu-id="e1eec-114">Запускает произвольный процесс в контексте локальной системы при доставке события в него.</span><span class="sxs-lookup"><span data-stu-id="e1eec-114">Launches an arbitrary process in the local system context when an event is delivered to it.</span></span><br/> <span data-ttu-id="e1eec-115">Пример. [Запуск программы из командной строки на основе события](running-a-program-from-the-command-line-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="e1eec-115">Example: [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md)</span></span><br/> |
| [<span data-ttu-id="e1eec-116">**логфиливентконсумер**</span><span class="sxs-lookup"><span data-stu-id="e1eec-116">**LogFileEventConsumer**</span></span>](logfileeventconsumer.md)                         | <span data-ttu-id="e1eec-117">Записывает настраиваемые строки в текстовый файл журнала при доставке событий в него.</span><span class="sxs-lookup"><span data-stu-id="e1eec-117">Writes customized strings to a text log file when events are delivered to it.</span></span><br/> <span data-ttu-id="e1eec-118">Пример. [запись в файл журнала на основе события](writing-to-a-log-file-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="e1eec-118">Example: [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md)</span></span><br/>                                                   |
| [<span data-ttu-id="e1eec-119">**нтевентложевентконсумер**</span><span class="sxs-lookup"><span data-stu-id="e1eec-119">**NTEventLogEventConsumer**</span></span>](nteventlogeventconsumer.md)                   | <span data-ttu-id="e1eec-120">Записывает в журнал событий Windows конкретное сообщение при доставке события в него.</span><span class="sxs-lookup"><span data-stu-id="e1eec-120">Logs a specific message to the Windows event log when an event is delivered to it.</span></span><br/> <span data-ttu-id="e1eec-121">Пример. [ведение журнала событий NT на основе события](logging-to-nt-event-log-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="e1eec-121">Example: [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md)</span></span><br/>                                          |
| [<span data-ttu-id="e1eec-122">**скриптингстандардконсумерсеттинг**</span><span class="sxs-lookup"><span data-stu-id="e1eec-122">**ScriptingStandardConsumerSetting**</span></span>](scriptingstandardconsumersetting.md) | <span data-ttu-id="e1eec-123">Предоставляет данные регистрации, общие для всех экземпляров класса [**активескриптевентконсумер**](activescripteventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="e1eec-123">Provides registration data common to all instances of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="e1eec-124">**смтпевентконсумер**</span><span class="sxs-lookup"><span data-stu-id="e1eec-124">**SMTPEventConsumer**</span></span>](smtpeventconsumer.md)                               | <span data-ttu-id="e1eec-125">Отправляет сообщение электронной почты по протоколу SMTP каждый раз, когда в него будет доставлено событие.</span><span class="sxs-lookup"><span data-stu-id="e1eec-125">Sends an email message using SMTP each time an event is delivered to it.</span></span><br/> <span data-ttu-id="e1eec-126">Пример: [Отправка сообщения электронной почты на основе события](sending-e-mail-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="e1eec-126">Example: [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md)</span></span><br/>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="e1eec-127">См. также</span><span class="sxs-lookup"><span data-stu-id="e1eec-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1eec-128">Мониторинг событий</span><span class="sxs-lookup"><span data-stu-id="e1eec-128">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="e1eec-129">Получение событий в любое время</span><span class="sxs-lookup"><span data-stu-id="e1eec-129">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="e1eec-130">Выполнение скрипта на основе события</span><span class="sxs-lookup"><span data-stu-id="e1eec-130">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="e1eec-131">Отправка сообщения электронной почты на основе события</span><span class="sxs-lookup"><span data-stu-id="e1eec-131">Sending Email Based on an Event</span></span>](sending-e-mail-based-on-an-event.md)
</dt> </dl>

 

 




