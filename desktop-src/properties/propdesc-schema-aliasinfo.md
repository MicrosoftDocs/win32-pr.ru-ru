---
description: Задает псевдоним сортировки или список псевдонимов сортировки, указывая элемент, который содержит свойство Sort или список свойств сортировки.
ms.assetid: 4c514197-0df0-49c6-b39e-8a2a7cefa93d
title: aliasInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052409864617bdaba7acbf9ae561752c83d18395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711675"
---
# <a name="aliasinfo"></a><span data-ttu-id="7d151-103">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="7d151-103">aliasInfo</span></span>

<span data-ttu-id="7d151-104">Задает псевдоним сортировки или список псевдонимов сортировки, указывая элемент, который содержит свойство Sort или список свойств сортировки.</span><span class="sxs-lookup"><span data-stu-id="7d151-104">Specifies a sort alias or list of sort aliases by specifying an element that contains a sort property or list of sort properties.</span></span> <span data-ttu-id="7d151-105">Для каждого элемента [пропертидескриптион](./propdesc-schema-propertydescription.md) должен быть только один элемент [aliasInfo]() .</span><span class="sxs-lookup"><span data-stu-id="7d151-105">There should be only one [aliasInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span> <span data-ttu-id="7d151-106">Для свойств, устанавливающих Канграупби = true, если не указано дополнительное свойство сортировки ( aliasInfo/@additionalSortByAliases = prop: example), пользователь может столкнуться с непредвиденным поведением при изменении порядка сортировки в представлении, сгруппированном по свойству.</span><span class="sxs-lookup"><span data-stu-id="7d151-106">For properties that set canGroupBy=true, unless a secondary sort property is specified (aliasInfo/@additionalSortByAliases=prop:example), the user may experience unexpected behavior when changing the sort order in a view that is grouped by the property.</span></span> <span data-ttu-id="7d151-107">В частности, порядок групп изменится, но порядок элементов в группах не будет.</span><span class="sxs-lookup"><span data-stu-id="7d151-107">Specifically, the order of the groups will change, but the order of items within the groups will not.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d151-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d151-108">Syntax</span></span>


```
<!-- aliasInfo -->
<xs:element name="aliasInfo">
    <xs:complexType>
        <xs:attribute name="sortByAlias" type="canonical-name"/>
        <xs:attribute name="additionalSortByAliases" type="proplist"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="7d151-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7d151-109">Element Information</span></span>



| <span data-ttu-id="7d151-110">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="7d151-110">Parent Element</span></span>                                                   | <span data-ttu-id="7d151-111">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7d151-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="7d151-112">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="7d151-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="7d151-113">Нет</span><span class="sxs-lookup"><span data-stu-id="7d151-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="7d151-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7d151-114">Attributes</span></span>



| <span data-ttu-id="7d151-115">Атрибут</span><span class="sxs-lookup"><span data-stu-id="7d151-115">Attribute</span></span>               | <span data-ttu-id="7d151-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7d151-116">Description</span></span>                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d151-117">сортбялиас</span><span class="sxs-lookup"><span data-stu-id="7d151-117">sortByAlias</span></span>             | <span data-ttu-id="7d151-118">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="7d151-118">Public.</span></span> <span data-ttu-id="7d151-119">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="7d151-119">Optional.</span></span> <span data-ttu-id="7d151-120">Каноническое имя свойства, которое должно использоваться для сортировки.</span><span class="sxs-lookup"><span data-stu-id="7d151-120">The canonical name of the property that should be used to sort by.</span></span> <span data-ttu-id="7d151-121">Эта строка имеет тип канонического типа.</span><span class="sxs-lookup"><span data-stu-id="7d151-121">This string is of type canonical-type.</span></span>                                            |
| <span data-ttu-id="7d151-122">аддитионалсортбялиасес</span><span class="sxs-lookup"><span data-stu-id="7d151-122">additionalSortByAliases</span></span> | <span data-ttu-id="7d151-123">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="7d151-123">Public.</span></span> <span data-ttu-id="7d151-124">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="7d151-124">Optional.</span></span> <span data-ttu-id="7d151-125">Разделенный точками с запятой список дополнительных свойств, которые будут использоваться при сортировке.</span><span class="sxs-lookup"><span data-stu-id="7d151-125">A semi-colon delimited list of additional properties to be used when sorting.</span></span> <span data-ttu-id="7d151-126">Свойства применяются к сортировке в той последовательности, в которой они указаны.</span><span class="sxs-lookup"><span data-stu-id="7d151-126">The properties are applied to the sort in the sequence they are given.</span></span> |



 

 

 
