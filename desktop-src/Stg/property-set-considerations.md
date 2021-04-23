---
title: Рекомендации по установке свойств
description: Настоятельно рекомендуется, чтобы наборы свойств были небольшими, так как поток набора свойств считывается в память до того, как одно свойство может быть считано или записано.
ms.assetid: 520db05e-81cd-40ef-af89-471d7194c634
keywords:
- Рекомендации по установке свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfd89140092b13d113122ffe1c1a2b576e654c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780096"
---
# <a name="property-set-considerations"></a><span data-ttu-id="50058-104">Рекомендации по установке свойств</span><span class="sxs-lookup"><span data-stu-id="50058-104">Property Set Considerations</span></span>

<span data-ttu-id="50058-105">Настоятельно рекомендуется, чтобы наборы свойств были небольшими, так как поток набора свойств считывается в память до того, как одно свойство может быть считано или записано.</span><span class="sxs-lookup"><span data-stu-id="50058-105">It is strongly recommended that property sets be kept small because the property set stream is read into memory before a single property can be read or written.</span></span> <span data-ttu-id="50058-106">"Малый" означает объем данных менее 32 КБ.</span><span class="sxs-lookup"><span data-stu-id="50058-106">"small" means less than 32 kilobytes of data.</span></span> <span data-ttu-id="50058-107">Это редко представляет проблему, поскольку обычно «встроенные» свойства представляют собой небольшие элементы, такие как описательные строки, ключевые слова, метки времени, счетчики, имена авторов, глобальные уникальные идентификаторы (GUID), идентификаторы классов (CLSID) и т. д.</span><span class="sxs-lookup"><span data-stu-id="50058-107">This rarely presents a problem because typically, "in-line" properties will be small items such as descriptive strings, keywords, time stamps, counts, author names, globally unique identifiers (GUIDs), class identifiers (CLSIDs), and so forth.</span></span>

<span data-ttu-id="50058-108">Для хранения больших фрагментов данных или в случаях, когда общий размер набора связанных свойств превышает рекомендуемый объем, настоятельно рекомендуется использовать непростые типы, такие как **VT \_ Stream** и **VT \_** .</span><span class="sxs-lookup"><span data-stu-id="50058-108">To store larger chunks of data, or in cases where the total size of a set of related properties far exceeds the recommended amount, the use of nonsimple types such as **VT\_STREAM** and **VT\_STORAGE** are strongly recommended.</span></span> <span data-ttu-id="50058-109">Они не хранятся в потоке набора свойств, поэтому они не влияют на изначальные издержки при первом доступе и записи свойства.</span><span class="sxs-lookup"><span data-stu-id="50058-109">These are not stored within the property set stream, so they do not significantly affect the initial overhead of the first accessing and writing of a property.</span></span> <span data-ttu-id="50058-110">Существует небольшая нагрузка, так как поток набора свойств содержит имя одноуровневого потока или свойства, возвращающего хранилище, и это занимает дополнительное небольшое время для обработки.</span><span class="sxs-lookup"><span data-stu-id="50058-110">There is a minimal overhead as the property set stream contains the name of the sibling stream- or storage-valued property and this takes an additional small amount of time to process.</span></span>

<span data-ttu-id="50058-111">Дополнительные сведения можно найти в разделе</span><span class="sxs-lookup"><span data-stu-id="50058-111">For more information, see:</span></span>

-   [<span data-ttu-id="50058-112">Рекомендации по реализации IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="50058-112">IPropertySetStorage Implementation Considerations</span></span>](ipropertysetstorage-implementation-considerations.md)
-   [<span data-ttu-id="50058-113">Хранение наборов свойств</span><span class="sxs-lookup"><span data-stu-id="50058-113">Storing Property Sets</span></span>](storing-property-sets.md)
-   [<span data-ttu-id="50058-114">Характеристики производительности</span><span class="sxs-lookup"><span data-stu-id="50058-114">Performance Characteristics</span></span>](performance-characteristics.md)
-   [<span data-ttu-id="50058-115">Реализация набора свойств сводных данных</span><span class="sxs-lookup"><span data-stu-id="50058-115">Implementing the Summary Information Property Set</span></span>](implementing-the-summary-information-property-set.md)

 

 




