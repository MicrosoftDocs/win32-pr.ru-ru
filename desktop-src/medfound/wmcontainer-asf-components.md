---
description: Объекты Вмконтаинер обеспечивают низкоуровневый контроль над синтаксическим анализом и записью файла в формате ASF.
ms.assetid: 258ea139-581f-4b94-9655-43ecf1e77f10
title: Компоненты ASF Вмконтаинер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7d1c1b76683cfe01dc0970ab1c077580215d2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998645"
---
# <a name="wmcontainer-asf-components"></a><span data-ttu-id="c0850-103">Компоненты ASF Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="c0850-103">WMContainer ASF Components</span></span>

<span data-ttu-id="c0850-104">Объекты Вмконтаинер обеспечивают низкоуровневый контроль над синтаксическим анализом и записью файла в формате ASF.</span><span class="sxs-lookup"><span data-stu-id="c0850-104">The WMContainer objects provide low-level control over parsing and writing an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="c0850-105">[Компоненты ASF уровня конвейера](pipeline-layer-asf-components.md) используют объекты вмконтаинер внутренне.</span><span class="sxs-lookup"><span data-stu-id="c0850-105">The [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) use the WMContainer objects internally.</span></span> <span data-ttu-id="c0850-106">Большинство приложений должны использовать компоненты конвейера вместо использования объектов Вмконтаинер.</span><span class="sxs-lookup"><span data-stu-id="c0850-106">Most applications should use the pipeline components, rather than using WMContainer objects.</span></span> <span data-ttu-id="c0850-107">Используйте Вмконтаинер, только если требуется низкоуровневый контроль над синтаксическим анализом и записью файла ASF.</span><span class="sxs-lookup"><span data-stu-id="c0850-107">Use WMContainer only if you require low-level control over parsing and writing an ASF file.</span></span>

<span data-ttu-id="c0850-108">Слой Вмконтаинер содержит следующие объекты:</span><span class="sxs-lookup"><span data-stu-id="c0850-108">The WMContainer layer includes the following objects:</span></span>

-   [<span data-ttu-id="c0850-109">Профиль ASF</span><span class="sxs-lookup"><span data-stu-id="c0850-109">ASF Profile</span></span>](asf-profile.md)
-   [<span data-ttu-id="c0850-110">Объект Контентинфо ASF</span><span class="sxs-lookup"><span data-stu-id="c0850-110">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
-   [<span data-ttu-id="c0850-111">Разделитель ASF</span><span class="sxs-lookup"><span data-stu-id="c0850-111">ASF Splitter</span></span>](asf-splitter.md)
-   [<span data-ttu-id="c0850-112">Мультиплексор ASF</span><span class="sxs-lookup"><span data-stu-id="c0850-112">ASF Multiplexer</span></span>](asf-multiplexer.md)
-   [<span data-ttu-id="c0850-113">Индексатор ASF</span><span class="sxs-lookup"><span data-stu-id="c0850-113">ASF Indexer</span></span>](asf-index-object.md)

<span data-ttu-id="c0850-114">В следующих разделах содержатся пошаговые инструкции по использованию Вмконтаинер для чтения или записи файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="c0850-114">The following topics contain step-by-step instructions about using WMContainer to read or write ASF files.</span></span>

-   [<span data-ttu-id="c0850-115">Руководство. чтение файла ASF с помощью объектов Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="c0850-115">Tutorial: Reading an ASF File by Using WMContainer Objects</span></span>](tutorial--reading-an-asf-file.md)
-   [<span data-ttu-id="c0850-116">Руководство. копирование потоков ASF с помощью объектов Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="c0850-116">Tutorial: Copying ASF Streams by Using WMContainer Objects</span></span>](tutorial--copying-asf-streams-from-one-file-to-another.md)
-   [<span data-ttu-id="c0850-117">Учебник. запись файла WMA с помощью объектов Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="c0850-117">Tutorial: Writing a WMA File by Using WMContainer Objects</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

## <a name="about-wm-container"></a><span data-ttu-id="c0850-118">О контейнере WM</span><span class="sxs-lookup"><span data-stu-id="c0850-118">About WM Container</span></span>

<span data-ttu-id="c0850-119">Объекты Вмконтаинер взаимодействуют напрямую с объектами файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="c0850-119">The WMContainer objects interact directly with ASF file objects.</span></span> <span data-ttu-id="c0850-120">На следующей схеме показана структура файла ASF и соответствующие объекты Вмконтаинер.</span><span class="sxs-lookup"><span data-stu-id="c0850-120">The following diagram shows the ASF file structure and the corresponding WMContainer objects.</span></span>

![Схема, показывающая структуру файлов ASF и соответствующие объекты Media Foundation](images/asf-components01.png)

<span data-ttu-id="c0850-122">За исключением разделителя и мультиплексора, каждый из этих объектов поддерживает синтаксический анализ (чтение) и запись файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="c0850-122">Except for the splitter and multiplexer, each of these objects supports both parsing (reading) and writing ASF files.</span></span> <span data-ttu-id="c0850-123">Разделитель используется только для чтения файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="c0850-123">The splitter is used only for reading ASF files.</span></span> <span data-ttu-id="c0850-124">Мультиплексор используется только для создания новых файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="c0850-124">The multiplexer is used only for authoring new ASF files.</span></span>

<span data-ttu-id="c0850-125">Все операции, выполняемые объектами Вмконтаинер, являются синхронными, то есть они блокируют вызывающий поток.</span><span class="sxs-lookup"><span data-stu-id="c0850-125">All operations performed by WMContainer objects are synchronous, meaning they block the calling thread.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0850-126">См. также</span><span class="sxs-lookup"><span data-stu-id="c0850-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0850-127">Поддержка ASF в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c0850-127">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



