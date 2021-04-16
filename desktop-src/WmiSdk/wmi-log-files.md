---
description: WMI использует трассировку событий (ETW) и события можно получить с помощью пользовательского интерфейса Просмотр событий или программы командной строки wevtutil. Дополнительные сведения см. в разделе Трассировка действия WMI.
ms.assetid: 315b8355-03b9-40f9-a6c1-29a49f5a2cd8
ms.tgt_platform: multiple
title: Файлы журналов WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51dfe4efbec32e60812980511676f723fd5aee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692687"
---
# <a name="wmi-log-files"></a><span data-ttu-id="4798b-104">Файлы журналов WMI</span><span class="sxs-lookup"><span data-stu-id="4798b-104">WMI Log Files</span></span>

<span data-ttu-id="4798b-105">WMI использует [трассировку событий](/windows/desktop/ETW/event-tracing-portal) (ETW) и события можно получить с помощью пользовательского интерфейса **Просмотр событий** или программы командной строки wevtutil.</span><span class="sxs-lookup"><span data-stu-id="4798b-105">WMI uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events can be obtained through the **Event Viewer** user interface or the Wevtutil command line tool.</span></span> <span data-ttu-id="4798b-106">Дополнительные сведения см. в разделе [Трассировка действия WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="4798b-106">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

-   [<span data-ttu-id="4798b-107">Трассировка событий вместо текстовых журналов</span><span class="sxs-lookup"><span data-stu-id="4798b-107">Event Tracing Instead of Text Logs</span></span>](#event-tracing-instead-of-text-logs)
-   [<span data-ttu-id="4798b-108">Файлы журналов WMI</span><span class="sxs-lookup"><span data-stu-id="4798b-108">WMI Log Files</span></span>](#wmi-log-files)
-   [<span data-ttu-id="4798b-109">См. также</span><span class="sxs-lookup"><span data-stu-id="4798b-109">Related topics</span></span>](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a><span data-ttu-id="4798b-110">Трассировка событий вместо текстовых журналов</span><span class="sxs-lookup"><span data-stu-id="4798b-110">Event Tracing Instead of Text Logs</span></span>

<span data-ttu-id="4798b-111">Действия службы WMI записываются в файл ВмитраЦинг. log.</span><span class="sxs-lookup"><span data-stu-id="4798b-111">WMI service activity is recorded in the WMITracing.log file.</span></span> <span data-ttu-id="4798b-112">Дополнительные сведения о включении трассировки событий WMI и обращении к файлу ВмитраЦинг. log см. в разделе [Трассировка действий WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="4798b-112">For more information about enabling WMI event tracing and accessing the WMITracing.log file, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span> <span data-ttu-id="4798b-113">Поставщики WDM (WDM) продолжают вести журнал в файле Вбемпров. log.</span><span class="sxs-lookup"><span data-stu-id="4798b-113">Windows Driver Model (WDM) providers continue to log in the Wbemprov.log file.</span></span>

## <a name="wmi-log-files"></a><span data-ttu-id="4798b-114">Файлы журналов WMI</span><span class="sxs-lookup"><span data-stu-id="4798b-114">WMI Log Files</span></span>

<span data-ttu-id="4798b-115">Служба WMI и некоторые поставщики записывают текстовые файлы журнала для записи событий.</span><span class="sxs-lookup"><span data-stu-id="4798b-115">The WMI service and some providers write text log files to record events.</span></span>

<dl> <dt>

<span data-ttu-id="4798b-116"><span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[Файлы журналов поставщика WMI](wmi-provider-log-files.md)</span><span class="sxs-lookup"><span data-stu-id="4798b-116"><span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[WMI Provider Log Files](wmi-provider-log-files.md)</span></span>
</dt> <dd>

<span data-ttu-id="4798b-117">Поставщики WMI также могут поддерживать журналы.</span><span class="sxs-lookup"><span data-stu-id="4798b-117">WMI providers also may maintain logs.</span></span> <span data-ttu-id="4798b-118">Файлы журналов, отображаемые в системе, зависят от того, какие поставщики установлены.</span><span class="sxs-lookup"><span data-stu-id="4798b-118">Which log files appear on a system depends on which providers are installed.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="4798b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="4798b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4798b-120">Справочник по инструментарию WMI</span><span class="sxs-lookup"><span data-stu-id="4798b-120">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="4798b-121">Трассировка действий WMI</span><span class="sxs-lookup"><span data-stu-id="4798b-121">Tracing WMI Activity</span></span>](tracing-wmi-activity.md)
</dt> <dt>

[<span data-ttu-id="4798b-122">Ведение журнала действий WMI</span><span class="sxs-lookup"><span data-stu-id="4798b-122">Logging WMI Activity</span></span>](logging-wmi-activity.md)
</dt> </dl>

 

 
