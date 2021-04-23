---
description: В следующих разделах описывается использование API ETW для трассировки событий.
ms.assetid: 7362874a-8206-4973-bb79-a9eaff55feb4
title: Использование трассировки событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5141c19838796c0ec29f9eb20add689d56b97757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263344"
---
# <a name="using-event-tracing"></a><span data-ttu-id="f1ae9-103">Использование трассировки событий</span><span class="sxs-lookup"><span data-stu-id="f1ae9-103">Using Event Tracing</span></span>

<span data-ttu-id="f1ae9-104">В следующих разделах описывается использование API ETW для трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="f1ae9-104">The following topics describe how to use the ETW API for event tracing.</span></span>



| <span data-ttu-id="f1ae9-105">Раздел</span><span class="sxs-lookup"><span data-stu-id="f1ae9-105">Topic</span></span>                                                                          | <span data-ttu-id="f1ae9-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f1ae9-106">Description</span></span>                                                                                                             |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1ae9-107">Управление сеансами трассировки событий</span><span class="sxs-lookup"><span data-stu-id="f1ae9-107">Controlling Event Tracing Sessions</span></span>](controlling-event-tracing-sessions.md)   | <span data-ttu-id="f1ae9-108">Описывает управление сеансами трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="f1ae9-108">Describes how to manage event tracing sessions.</span></span>                                                                         |
| [<span data-ttu-id="f1ae9-109">Предоставление событий</span><span class="sxs-lookup"><span data-stu-id="f1ae9-109">Providing Events</span></span>](providing-events.md)                                       | <span data-ttu-id="f1ae9-110">Описание процесса регистрации и инструментирования поставщика трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="f1ae9-110">Describes how to register and instrument an event trace provider.</span></span>                                                       |
| [<span data-ttu-id="f1ae9-111">Использование событий</span><span class="sxs-lookup"><span data-stu-id="f1ae9-111">Consuming Events</span></span>](consuming-events.md)                                       | <span data-ttu-id="f1ae9-112">Описывает, как реализовать функции обратного вызова, используемые для использования и обработки событий из файла журнала трассировки или в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="f1ae9-112">Describes how to implement callback functions used to consume and process events from a trace log file or in real time.</span></span> |
| [<span data-ttu-id="f1ae9-113">Препроцессор трассировки программного обеспечения Windows</span><span class="sxs-lookup"><span data-stu-id="f1ae9-113">Windows Software Trace Preprocessor</span></span>](windows-software-trace-preprocessor.md) | <span data-ttu-id="f1ae9-114">Предоставляет эффективный механизм для ведения журнала и использования событий, происходящих во время выполнения приложения или драйвера.</span><span class="sxs-lookup"><span data-stu-id="f1ae9-114">Provides an efficient mechanism to log and consume events that occur during the execution of an application or driver.</span></span>  |



 

<span data-ttu-id="f1ae9-115">Включите файл заголовка Вмистр. h перед включением файла заголовка Евнтраце. h.</span><span class="sxs-lookup"><span data-stu-id="f1ae9-115">Include the Wmistr.h header file before including the Evntrace.h header file.</span></span>

 

 



