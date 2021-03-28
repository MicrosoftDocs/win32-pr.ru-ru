---
description: Содержит список средств, используемых в трассировке событий.
ms.assetid: 7a1c9d8c-5bf4-4f0c-b815-5b70e53c5e2d
title: Средства трассировки событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1cb68e3d04be53f5a99c9e319540fd49f02000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265955"
---
# <a name="event-tracing-tools"></a><span data-ttu-id="202d0-103">Средства трассировки событий</span><span class="sxs-lookup"><span data-stu-id="202d0-103">Event Tracing Tools</span></span>

<span data-ttu-id="202d0-104">Для использования доступны следующие средства трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="202d0-104">The following event tracing tools are available for your use.</span></span>



| <span data-ttu-id="202d0-105">Средство</span><span class="sxs-lookup"><span data-stu-id="202d0-105">Tool</span></span>     | <span data-ttu-id="202d0-106">Описание</span><span class="sxs-lookup"><span data-stu-id="202d0-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="202d0-107">Logman</span><span class="sxs-lookup"><span data-stu-id="202d0-107">Logman</span></span>   | <span data-ttu-id="202d0-108">Управляет и планирует сбор счетчиков производительности и журналов трассировки событий в локальных и удаленных системах.</span><span class="sxs-lookup"><span data-stu-id="202d0-108">Manages and schedules performance counter and event trace log collections on local and remote systems.</span></span> <span data-ttu-id="202d0-109">Это средство можно использовать для перечисления поставщиков, которые [опубликовали макет данных о событиях](publishing-your-event-schema.md) в корневом \\ пространстве имен WMI.</span><span class="sxs-lookup"><span data-stu-id="202d0-109">You can use this tool to list the providers that have [published the layout of their event data](publishing-your-event-schema.md) in the root\\wmi namespace.</span></span> <span data-ttu-id="202d0-110">Дополнительные сведения об использовании этого средства см. в **центре справки и поддержки**.</span><span class="sxs-lookup"><span data-stu-id="202d0-110">For details on using this tool, see the **Help and Support Center**.</span></span> |
| <span data-ttu-id="202d0-111">трацефмт</span><span class="sxs-lookup"><span data-stu-id="202d0-111">Tracefmt</span></span> | <span data-ttu-id="202d0-112">Форматирует сведения в файле журнала трассировки в удобочитаемой форме.</span><span class="sxs-lookup"><span data-stu-id="202d0-112">Formats information in a trace log file in human-readable form.</span></span> <span data-ttu-id="202d0-113">Дополнительные сведения см. в разделе средства для трассировки программного обеспечения в пакете средств разработки драйверов Microsoft Windows (DDK).</span><span class="sxs-lookup"><span data-stu-id="202d0-113">For details, see Tools for Software Tracing in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="202d0-114">Используется только трассировкой программного обеспечения WPP.</span><span class="sxs-lookup"><span data-stu-id="202d0-114">Used by WPP Software Tracing only.</span></span>                                                                                                                                      |
| <span data-ttu-id="202d0-115">Tracelog</span><span class="sxs-lookup"><span data-stu-id="202d0-115">Tracelog</span></span> | <span data-ttu-id="202d0-116">Управляет сеансом трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="202d0-116">Controls an event trace session.</span></span> <span data-ttu-id="202d0-117">Дополнительные сведения см. в разделе средства для трассировки программного обеспечения в DDK.</span><span class="sxs-lookup"><span data-stu-id="202d0-117">For details, see Tools for Software Tracing in the DDK.</span></span>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="202d0-118">трацепдб</span><span class="sxs-lookup"><span data-stu-id="202d0-118">Tracepdb</span></span> | <span data-ttu-id="202d0-119">Создает файл формата сообщений трассировки, который средство Трацефмт использует для преобразования журнальных сообщений в форму, доступную для восприятия.</span><span class="sxs-lookup"><span data-stu-id="202d0-119">Creates a trace message format file that the Tracefmt tool uses to convert logged messages to a human-readable form.</span></span> <span data-ttu-id="202d0-120">Дополнительные сведения см. в разделе средства для трассировки программного обеспечения в DDK.</span><span class="sxs-lookup"><span data-stu-id="202d0-120">For details, see Tools for Software Tracing in the DDK.</span></span> <span data-ttu-id="202d0-121">Используется только трассировкой программного обеспечения WPP.</span><span class="sxs-lookup"><span data-stu-id="202d0-121">Used by WPP Software Tracing only.</span></span>                                                                                                                            |
| <span data-ttu-id="202d0-122">Tracerpt</span><span class="sxs-lookup"><span data-stu-id="202d0-122">Tracerpt</span></span> | <span data-ttu-id="202d0-123">Обрабатывает журналы трассировки событий или события в режиме реального времени от инструментированных поставщиков трассировки событий и позволяет создавать отчеты анализа трассировки и файлы CSV (с разделителями-запятыми) для создаваемых событий.</span><span class="sxs-lookup"><span data-stu-id="202d0-123">Processes event trace logs or real-time events from instrumented event trace providers and allows you to generate trace analysis reports and CSV (comma-delimited) files for the events generated.</span></span> <span data-ttu-id="202d0-124">Дополнительные сведения см. в **центре справки и поддержки**.</span><span class="sxs-lookup"><span data-stu-id="202d0-124">For details, see the **Help and Support Center**.</span></span>                                                                                       |



 

 

 



