---
title: Схема событий
ms.assetid: 36037697-b777-4e5c-99af-77964200a3e4
description: 'Дополнительные сведения: схема событий'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bfb26f6c71d544e0c0a6a4d833b40a5d15ae5485
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909596"
---
# <a name="event-schema"></a><span data-ttu-id="b79a3-103">Схема событий</span><span class="sxs-lookup"><span data-stu-id="b79a3-103">Event Schema</span></span>

<span data-ttu-id="b79a3-104">Схема событий определяет следующие элементы и типы, которые определяют элементы и атрибуты регистрируемого события:</span><span class="sxs-lookup"><span data-stu-id="b79a3-104">The Event schema defines the following elements and types that identify the elements and attributes of a logged event:</span></span>

-   [<span data-ttu-id="b79a3-105">Элементы Евентсчема</span><span class="sxs-lookup"><span data-stu-id="b79a3-105">EventSchema Elements</span></span>](eventschema-elements.md)
-   [<span data-ttu-id="b79a3-106">Простые типы Евентсчема</span><span class="sxs-lookup"><span data-stu-id="b79a3-106">EventSchema Simple Types</span></span>](eventschema-simple-types.md)
-   [<span data-ttu-id="b79a3-107">Сложные типы Евентсчема</span><span class="sxs-lookup"><span data-stu-id="b79a3-107">EventSchema Complex Types</span></span>](eventschema-complex-types.md)

<span data-ttu-id="b79a3-108">Раздел Elements содержит имена элементов, которые можно найти в зарегистрированных событиях. Однако, чтобы получить подробные сведения для каждого элемента, см. сложный тип, содержащий элемент.</span><span class="sxs-lookup"><span data-stu-id="b79a3-108">The elements section contains the names of the elements that you would find in a logged events; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="b79a3-109">Windows SDK включает схему в \\ \\ файл include события. xsd.</span><span class="sxs-lookup"><span data-stu-id="b79a3-109">The Windows SDK includes the schema in the \\Include\\Event.xsd file.</span></span>

<span data-ttu-id="b79a3-110">Эту схему можно использовать для обнаружения элементов и атрибутов при вызове функции [**евтрендер**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) для отображения конкретных разделов или свойств события.</span><span class="sxs-lookup"><span data-stu-id="b79a3-110">You can use this schema to identify the elements and attributes when calling the [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function to render specific sections or properties of the event.</span></span> <span data-ttu-id="b79a3-111">Пример, демонстрирующий использование этой схемы при подготовке событий к просмотру, см. в разделе [Rendering Events](rendering-events.md).</span><span class="sxs-lookup"><span data-stu-id="b79a3-111">For an example that shows how to use this schema when rendering events, see [Rendering Events](rendering-events.md).</span></span>

<span data-ttu-id="b79a3-112">В дополнение к схеме событий журнал событий Windows также определяет следующие схемы:</span><span class="sxs-lookup"><span data-stu-id="b79a3-112">In addition to the Event schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="b79a3-113">[Евентманифест Schema](eventmanifestschema-schema.md)— определяет элементы и типы, используемые для записи манифеста инструментирования.</span><span class="sxs-lookup"><span data-stu-id="b79a3-113">[EventManifest Schema](eventmanifestschema-schema.md)—defines the elements and types used to write an instrumentation manifest.</span></span>
-   <span data-ttu-id="b79a3-114">[Схема запроса](queryschema-schema.md)— определяет элементы и типы, используемые для записи запроса на получение событий из одного или нескольких каналов.</span><span class="sxs-lookup"><span data-stu-id="b79a3-114">[Query Schema](queryschema-schema.md)—defines the elements and types used to write a query to retrieve events from one or more channels.</span></span>

 

 




