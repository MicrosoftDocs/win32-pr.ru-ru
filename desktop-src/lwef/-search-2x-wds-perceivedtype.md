---
title: Распознанные типы (устаревшие функции среды Windows)
description: PerceivedType — это свойство, которое классифицирует элемент в индексе.
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afaf7d8b827495a94b441e5504762dd53dbe733c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105691746"
---
# <a name="perceived-types-legacy-windows-environment-features"></a><span data-ttu-id="5273a-103">Распознанные типы (устаревшие функции среды Windows)</span><span class="sxs-lookup"><span data-stu-id="5273a-103">Perceived Types (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="5273a-104">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5273a-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="5273a-105">В более поздних выпусках используйте вместо этого [Поиск Windows](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="5273a-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="5273a-106">`PerceivedType` свойство, которое классифицирует элемент в индексе.</span><span class="sxs-lookup"><span data-stu-id="5273a-106">`PerceivedType` is a property that classifies an item in the index.</span></span> <span data-ttu-id="5273a-107">Эта классификация отличается от классификации "тип", используемой [расширенным синтаксисом запросов](-search-2x-wds-aqsreference.md) , но также позволяет пользователям уточнять результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="5273a-107">This classification is different from the "kind" classification used by the [Advanced Query Syntax](-search-2x-wds-aqsreference.md) but similarly lets users refine their search results.</span></span> <span data-ttu-id="5273a-108">Тип АКС позволяет пользователям ограничить поисковый запрос, тогда как свойство PerceivedType позволяет пользователям фильтровать свои результирующие наборы.</span><span class="sxs-lookup"><span data-stu-id="5273a-108">The AQS kind lets users limit their search query while the PerceivedType property lets users filter their result set.</span></span>

## <a name="types"></a><span data-ttu-id="5273a-109">Типы</span><span class="sxs-lookup"><span data-stu-id="5273a-109">Types</span></span>

<span data-ttu-id="5273a-110">Используйте свойство PerceivedType для классификации типа файлов, чтобы пользователи могли фильтровать результаты поиска по типу.</span><span class="sxs-lookup"><span data-stu-id="5273a-110">Use the PerceivedType property to classify your file type so that users can filter their search results by type.</span></span> <span data-ttu-id="5273a-111">Выходные данные должны быть одной из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="5273a-111">The output must be one of the following strings:</span></span>

-   <span data-ttu-id="5273a-112">contact</span><span class="sxs-lookup"><span data-stu-id="5273a-112">contact</span></span>
-   <span data-ttu-id="5273a-113">IP-адресу (DIP)</span><span class="sxs-lookup"><span data-stu-id="5273a-113">communications</span></span>
-   <span data-ttu-id="5273a-114">связь и электронная почта</span><span class="sxs-lookup"><span data-stu-id="5273a-114">communications/email</span></span>
-   <span data-ttu-id="5273a-115">связь и календарь</span><span class="sxs-lookup"><span data-stu-id="5273a-115">communications/calendar</span></span>
-   <span data-ttu-id="5273a-116">связь/задача</span><span class="sxs-lookup"><span data-stu-id="5273a-116">communications/task</span></span>
-   <span data-ttu-id="5273a-117">Обмен данными и обмен мгновенными сообщениями</span><span class="sxs-lookup"><span data-stu-id="5273a-117">communications/im</span></span>
-   <span data-ttu-id="5273a-118">документ</span><span class="sxs-lookup"><span data-stu-id="5273a-118">document</span></span>
-   <span data-ttu-id="5273a-119">документ/Примечание</span><span class="sxs-lookup"><span data-stu-id="5273a-119">document/note</span></span>
-   <span data-ttu-id="5273a-120">документ/текст</span><span class="sxs-lookup"><span data-stu-id="5273a-120">document/text</span></span>
-   <span data-ttu-id="5273a-121">документ/электронная таблица</span><span class="sxs-lookup"><span data-stu-id="5273a-121">document/spreadsheet</span></span>
-   <span data-ttu-id="5273a-122">документ/презентация</span><span class="sxs-lookup"><span data-stu-id="5273a-122">document/presentation</span></span>
-   <span data-ttu-id="5273a-123">music</span><span class="sxs-lookup"><span data-stu-id="5273a-123">music</span></span>
-   <span data-ttu-id="5273a-124">images</span><span class="sxs-lookup"><span data-stu-id="5273a-124">images</span></span>
-   <span data-ttu-id="5273a-125">изображения и рисунки</span><span class="sxs-lookup"><span data-stu-id="5273a-125">images/picture</span></span>
-   <span data-ttu-id="5273a-126">изображения и видео</span><span class="sxs-lookup"><span data-stu-id="5273a-126">images/video</span></span>
-   <span data-ttu-id="5273a-127">folder</span><span class="sxs-lookup"><span data-stu-id="5273a-127">folder</span></span>
-   <span data-ttu-id="5273a-128">программа</span><span class="sxs-lookup"><span data-stu-id="5273a-128">program</span></span>

<span data-ttu-id="5273a-129">Например, если требуется создать надстройку фильтра для нового типа файла изображений, в интерфейсе [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)необходимо реализовать следующее:</span><span class="sxs-lookup"><span data-stu-id="5273a-129">For example, when you want to create a filter add-in for a new picture file type, you need to implement the following in your [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface:</span></span>

-   <span data-ttu-id="5273a-130">Для возврата **блока** фуллпропспек, включающего: D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType</span><span class="sxs-lookup"><span data-stu-id="5273a-130">**GetChunk** to return a FULLPROPSPEC that includes: D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType</span></span>
-   <span data-ttu-id="5273a-131">**GetValue** возвращает пропвариант, включающий: VT \_ LPWSTR = "Images/Picture"</span><span class="sxs-lookup"><span data-stu-id="5273a-131">**GetValue** to return a PROPVARIANT that includes: VT\_LPWSTR = "images/picture"</span></span>

## <a name="related-topics"></a><span data-ttu-id="5273a-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5273a-132">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5273a-133">**Reference**</span><span class="sxs-lookup"><span data-stu-id="5273a-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5273a-134">Разработка надстроек IFilter</span><span class="sxs-lookup"><span data-stu-id="5273a-134">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="5273a-135">Разработка обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="5273a-135">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="5273a-136">Синтаксис расширенных запросов</span><span class="sxs-lookup"><span data-stu-id="5273a-136">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="5273a-137">счематабле</span><span class="sxs-lookup"><span data-stu-id="5273a-137">SchemaTable</span></span>](-search-2x-wds-schematable.md)
</dt> </dl>

 

 
