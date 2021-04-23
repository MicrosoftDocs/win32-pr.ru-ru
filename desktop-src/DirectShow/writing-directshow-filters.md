---
description: Написание фильтров DirectShow
ms.assetid: ffbc92b2-4f45-439b-b140-49a66fc4d914
title: Написание фильтров DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b266f3bbb9781dddcd2d0fb065b63d895a732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683060"
---
# <a name="writing-directshow-filters"></a><span data-ttu-id="92ebe-103">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="92ebe-103">Writing DirectShow Filters</span></span>

<span data-ttu-id="92ebe-104">Если вы разрабатываете фильтр для использования в графе фильтра Microsoft DirectShow, прочтите статьи в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="92ebe-104">If you are developing a filter for use in a Microsoft DirectShow filter graph, read the articles in this section.</span></span> <span data-ttu-id="92ebe-105">В общем случае нет необходимости читать этот раздел при написании приложения DirectShow.</span><span class="sxs-lookup"><span data-stu-id="92ebe-105">In general, you do not have to read this section if you are writing a DirectShow application.</span></span> <span data-ttu-id="92ebe-106">Большинство приложений не имеют доступа к фильтрам или графу фильтра на уровне, описанном в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="92ebe-106">Most applications do not access filters or the filter graph at the level discussed in this section.</span></span>

-   [<span data-ttu-id="92ebe-107">Введение в разработку фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="92ebe-107">Introduction to DirectShow Filter Development</span></span>](introduction-to-directshow-filter-development.md)
-   [<span data-ttu-id="92ebe-108">Создание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="92ebe-108">Building DirectShow Filters</span></span>](building-directshow-filters.md)
-   [<span data-ttu-id="92ebe-109">Как подключаются фильтры</span><span class="sxs-lookup"><span data-stu-id="92ebe-109">How Filters Connect</span></span>](how-filters-connect.md)
-   [<span data-ttu-id="92ebe-110">Поток данных для разработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="92ebe-110">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="92ebe-111">Потоки и критические разделы</span><span class="sxs-lookup"><span data-stu-id="92ebe-111">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
-   [<span data-ttu-id="92ebe-112">Управление качеством</span><span class="sxs-lookup"><span data-stu-id="92ebe-112">Quality-Control Management</span></span>](quality-control-management.md)
-   [<span data-ttu-id="92ebe-113">DirectShow и COM</span><span class="sxs-lookup"><span data-stu-id="92ebe-113">DirectShow and COM</span></span>](directshow-and-com.md)
-   [<span data-ttu-id="92ebe-114">Запись фильтров источника</span><span class="sxs-lookup"><span data-stu-id="92ebe-114">Writing Source Filters</span></span>](writing-source-filters.md)
-   [<span data-ttu-id="92ebe-115">Написание фильтров преобразования</span><span class="sxs-lookup"><span data-stu-id="92ebe-115">Writing Transform Filters</span></span>](writing-transform-filters.md)
-   [<span data-ttu-id="92ebe-116">Написание модулей подготовки видео</span><span class="sxs-lookup"><span data-stu-id="92ebe-116">Writing Video Renderers</span></span>](writing-video-renderers.md)
-   [<span data-ttu-id="92ebe-117">Запись фильтров записи</span><span class="sxs-lookup"><span data-stu-id="92ebe-117">Writing Capture Filters</span></span>](writing-capture-filters.md)
-   [<span data-ttu-id="92ebe-118">Предоставление форматов записи и сжатия</span><span class="sxs-lookup"><span data-stu-id="92ebe-118">Exposing Capture and Compression Formats</span></span>](exposing-capture-and-compression-formats.md)
-   [<span data-ttu-id="92ebe-119">Регистрация пользовательского типа файла</span><span class="sxs-lookup"><span data-stu-id="92ebe-119">Registering a Custom File Type</span></span>](registering-a-custom-file-type.md)
-   [<span data-ttu-id="92ebe-120">Создание страницы свойств фильтра</span><span class="sxs-lookup"><span data-stu-id="92ebe-120">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)

 

 



