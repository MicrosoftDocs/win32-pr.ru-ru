---
title: Справочник по журналам событий Windows
description: Ниже приведены элементы программирования, которые используются для создания манифеста инструментирования, создания ресурсов из манифеста, используемого поставщиком, получения метаданных инструментирования во время выполнения и запроса событий из каналов и файлов журналов.
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fef1af82cdab1ab92b4ea4768479541053fe65d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072381"
---
# <a name="windows-event-log-reference"></a><span data-ttu-id="d31b3-103">Справочник по журналам событий Windows</span><span class="sxs-lookup"><span data-stu-id="d31b3-103">Windows Event Log Reference</span></span>

<span data-ttu-id="d31b3-104">Ниже приведены элементы программирования, используемые для создания манифеста инструментирования, создания ресурсов из манифеста, используемого поставщиком, получения метаданных инструментирования во время выполнения и запроса событий из каналов и файлов журналов.</span><span class="sxs-lookup"><span data-stu-id="d31b3-104">The following are the programming elements that you use to create an instrumentation manifest, create resources from the manifest that your provider uses, get instrumentation metadata at run time, and query events from channels and log files:</span></span>

-   [<span data-ttu-id="d31b3-105">Схема Евентманифест</span><span class="sxs-lookup"><span data-stu-id="d31b3-105">EventManifest Schema</span></span>](eventmanifestschema-schema.md)
-   [<span data-ttu-id="d31b3-106">Схема событий</span><span class="sxs-lookup"><span data-stu-id="d31b3-106">Event Schema</span></span>](eventschema-schema.md)
-   [<span data-ttu-id="d31b3-107">Схема запроса</span><span class="sxs-lookup"><span data-stu-id="d31b3-107">Query Schema</span></span>](queryschema-schema.md)
-   [<span data-ttu-id="d31b3-108">Константы журнала событий Windows</span><span class="sxs-lookup"><span data-stu-id="d31b3-108">Windows Event Log Constants</span></span>](windows-event-log-constants.md)
-   [<span data-ttu-id="d31b3-109">Типы данных журнала событий Windows</span><span class="sxs-lookup"><span data-stu-id="d31b3-109">Windows Event Log Data Types</span></span>](windows-event-log-data-types.md)
-   [<span data-ttu-id="d31b3-110">Перечисления журнала событий Windows</span><span class="sxs-lookup"><span data-stu-id="d31b3-110">Windows Event Log Enumerations</span></span>](windows-event-log-enumerations.md)
-   [<span data-ttu-id="d31b3-111">Функции журнала событий Windows</span><span class="sxs-lookup"><span data-stu-id="d31b3-111">Windows Event Log Functions</span></span>](windows-event-log-functions.md)
-   [<span data-ttu-id="d31b3-112">Структуры журнала событий Windows</span><span class="sxs-lookup"><span data-stu-id="d31b3-112">Windows Event Log Structures</span></span>](windows-event-log-structures.md)
-   [<span data-ttu-id="d31b3-113">Средства журнала событий Windows</span><span class="sxs-lookup"><span data-stu-id="d31b3-113">Windows Event Log Tools</span></span>](windows-event-log-tools.md)

<span data-ttu-id="d31b3-114">Для приложений, написанных с использованием языка .NET, например C# или Visual Basic, см. следующие пространства имен:</span><span class="sxs-lookup"><span data-stu-id="d31b3-114">For applications written using a .NET language, such as C# or Visual Basic, see the following namespaces:</span></span>

-   <span data-ttu-id="d31b3-115">Для записи событий используйте классы и методы, определенные в пространстве имен [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) .</span><span class="sxs-lookup"><span data-stu-id="d31b3-115">To write events, use the classes and methods defined in the [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) namespace.</span></span>
-   <span data-ttu-id="d31b3-116">Чтобы использовать события из канала или журнала событий Windows, используйте классы и методы, определенные в пространстве имен [System. Diagnostics. Eventing. Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="d31b3-116">To consume events from a Windows Event Log channel or log, use the classes and methods defined in the [System.Diagnostics.Eventing.Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.</span></span>

<span data-ttu-id="d31b3-117">В качестве альтернативы использованию пространства имен [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) для записи событий можно использовать аргумент **-CS** или **-CSS** , чтобы компилятор сообщений создавал код для записи событий.</span><span class="sxs-lookup"><span data-stu-id="d31b3-117">As an alternative to using the [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) namespace to write events, you can use the **-cs** or **-css** argument to have the message compiler generate the code to write the events.</span></span> <span data-ttu-id="d31b3-118">Дополнительные сведения см. в разделе [**компилятор сообщений**](message-compiler--mc-exe-.md).</span><span class="sxs-lookup"><span data-stu-id="d31b3-118">For details, see [**Message Compiler**](message-compiler--mc-exe-.md).</span></span>
