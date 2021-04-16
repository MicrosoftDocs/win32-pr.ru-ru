---
title: Схема Евентманифест
ms.assetid: 89acbc43-739b-4e89-a96a-cc3438ec8ecc
description: 'Дополнительные сведения о: схема Евентманифест'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 67e1c2e9b769cd26e81a71853037655220a27d1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693067"
---
# <a name="eventmanifest-schema"></a><span data-ttu-id="3e446-103">Схема Евентманифест</span><span class="sxs-lookup"><span data-stu-id="3e446-103">EventManifest Schema</span></span>

<span data-ttu-id="3e446-104">Схема Евентманифест определяет следующие элементы и типы, которые используются для записи манифеста инструментирования:</span><span class="sxs-lookup"><span data-stu-id="3e446-104">The EventManifest schema defines the following elements and types that you use to write an instrumentation manifest:</span></span>

-   [<span data-ttu-id="3e446-105">Элементы Евентманифестсчема</span><span class="sxs-lookup"><span data-stu-id="3e446-105">EventManifestSchema Elements</span></span>](eventmanifestschema-elements.md)
-   [<span data-ttu-id="3e446-106">Простые типы Евентманифестсчема</span><span class="sxs-lookup"><span data-stu-id="3e446-106">EventManifestSchema Simple Types</span></span>](eventmanifestschema-simple-types.md)
-   [<span data-ttu-id="3e446-107">Сложные типы Евентманифестсчема</span><span class="sxs-lookup"><span data-stu-id="3e446-107">EventManifestSchema Complex Types</span></span>](eventmanifestschema-complex-types.md)

<span data-ttu-id="3e446-108">Раздел Elements содержит имена элементов, используемых в манифесте. Однако, чтобы получить подробные сведения для каждого элемента, см. сложный тип, содержащий элемент.</span><span class="sxs-lookup"><span data-stu-id="3e446-108">The elements section contains the names of the elements that you use in your manifest; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="3e446-109">Манифест инструментирования — это XML-файл, определяющий поставщика событий, каналы, на которые записываются события, сами события, условия фильтрации событий, такие как уровни, задачи и коды операций, а также локализованные строки, используемые при отрисовке событий.</span><span class="sxs-lookup"><span data-stu-id="3e446-109">An instrumentation manifest is an XML file that defines an event provider, the channels to which the events are written, the events themselves, the event filtering criteria such as levels, tasks, and opcodes, and the localized strings used when rendering the events.</span></span> <span data-ttu-id="3e446-110">Соглашение заключается в использовании. Man в качестве расширения для файлов манифеста.</span><span class="sxs-lookup"><span data-stu-id="3e446-110">The convention is to use .man as the extension for manifest files.</span></span> <span data-ttu-id="3e446-111">Дополнительные сведения о создании манифеста см. в разделе [написание манифеста инструментирования](writing-an-instrumentation-manifest.md).</span><span class="sxs-lookup"><span data-stu-id="3e446-111">For details on writing a manifest, see [Writing an Instrumentation Manifest](writing-an-instrumentation-manifest.md).</span></span>

<span data-ttu-id="3e446-112">Windows SDK включает схему в \\ \\ файл include. xsd.</span><span class="sxs-lookup"><span data-stu-id="3e446-112">The Windows SDK includes the schema in the \\Include\\Eventman.xsd file.</span></span> <span data-ttu-id="3e446-113">Для проверки манифеста можно использовать XSD.</span><span class="sxs-lookup"><span data-stu-id="3e446-113">You can use the XSD to validate your manifest.</span></span>

<span data-ttu-id="3e446-114">В дополнение к схеме Евентманифест журнал событий Windows также определяет следующие схемы:</span><span class="sxs-lookup"><span data-stu-id="3e446-114">In addition to the EventManifest schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="3e446-115">[Схема событий](eventschema-schema.md)— определяет элементы и типы, используемые для отрисовки события.</span><span class="sxs-lookup"><span data-stu-id="3e446-115">[Event Schema](eventschema-schema.md)—defines the elements and types used to render an event.</span></span>
-   <span data-ttu-id="3e446-116">[Схема запроса](queryschema-schema.md)— определяет элементы и типы, используемые для записи запроса на получение событий из одного или нескольких каналов.</span><span class="sxs-lookup"><span data-stu-id="3e446-116">[Query Schema](queryschema-schema.md)—defines the elements and types used to write a query to retrieve events from one or more channels.</span></span>

 

 




