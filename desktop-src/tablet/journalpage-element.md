---
description: Содержит сведения об отдельной странице в заметке журнала.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Жаурналпаже, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7223818de8200f2ff7748edd7eb472f49e92e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911392"
---
# <a name="journalpage-element"></a><span data-ttu-id="6e852-103">Жаурналпаже, элемент</span><span class="sxs-lookup"><span data-stu-id="6e852-103">JournalPage Element</span></span>

<span data-ttu-id="6e852-104">Содержит сведения об отдельной странице в заметке журнала.</span><span class="sxs-lookup"><span data-stu-id="6e852-104">Contains the details about an individual page in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="6e852-105">Определение</span><span class="sxs-lookup"><span data-stu-id="6e852-105">Definition</span></span>

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="6e852-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6e852-106">Parent Elements</span></span>

[<span data-ttu-id="6e852-107">**жаурналдокумент**</span><span class="sxs-lookup"><span data-stu-id="6e852-107">**JournalDocument**</span></span>](journaldocument-element.md)

## <a name="child-elements"></a><span data-ttu-id="6e852-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6e852-108">Child Elements</span></span>

[<span data-ttu-id="6e852-109">**Стационарный**</span><span class="sxs-lookup"><span data-stu-id="6e852-109">**Stationary**</span></span>](stationery-element.md)

[<span data-ttu-id="6e852-110">**доЦимаже**</span><span class="sxs-lookup"><span data-stu-id="6e852-110">**DocImage**</span></span>](docimage-element.md)

[<span data-ttu-id="6e852-111">**титлеинфо**</span><span class="sxs-lookup"><span data-stu-id="6e852-111">**TitleInfo**</span></span>](titleinfo-element.md)

[<span data-ttu-id="6e852-112">**Содержани**</span><span class="sxs-lookup"><span data-stu-id="6e852-112">**Content**</span></span>](content-element--journal-reader.md)

## <a name="attributes"></a><span data-ttu-id="6e852-113">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6e852-113">Attributes</span></span>



| <span data-ttu-id="6e852-114">attribute</span><span class="sxs-lookup"><span data-stu-id="6e852-114">Attribute</span></span>      | <span data-ttu-id="6e852-115">Тип</span><span class="sxs-lookup"><span data-stu-id="6e852-115">Type</span></span>                      | <span data-ttu-id="6e852-116">Обязательно</span><span class="sxs-lookup"><span data-stu-id="6e852-116">Required</span></span> | <span data-ttu-id="6e852-117">Описание</span><span class="sxs-lookup"><span data-stu-id="6e852-117">Description</span></span>                                                                        | <span data-ttu-id="6e852-118">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="6e852-118">Possible Values</span></span>                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="6e852-119">**Число**</span><span class="sxs-lookup"><span data-stu-id="6e852-119">**Number**</span></span>     | <span data-ttu-id="6e852-120">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="6e852-120">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="6e852-121">Обязательно</span><span class="sxs-lookup"><span data-stu-id="6e852-121">Required</span></span> | <span data-ttu-id="6e852-122">Порядковый номер страницы в документе журнала, начиная с единицы (1).</span><span class="sxs-lookup"><span data-stu-id="6e852-122">The ordinal number of the page within the Journal document, starting with one (1).</span></span> | <span data-ttu-id="6e852-123">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="6e852-123">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="6e852-124">**Width**</span><span class="sxs-lookup"><span data-stu-id="6e852-124">**Width**</span></span>      | <span data-ttu-id="6e852-125">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="6e852-125">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="6e852-126">Обязательно</span><span class="sxs-lookup"><span data-stu-id="6e852-126">Required</span></span> | <span data-ttu-id="6e852-127">Ширина страницы.</span><span class="sxs-lookup"><span data-stu-id="6e852-127">The width of the page.</span></span>                                                             | <span data-ttu-id="6e852-128">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="6e852-128">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="6e852-129">**Height**</span><span class="sxs-lookup"><span data-stu-id="6e852-129">**Height**</span></span>     | <span data-ttu-id="6e852-130">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="6e852-130">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="6e852-131">Обязательно</span><span class="sxs-lookup"><span data-stu-id="6e852-131">Required</span></span> | <span data-ttu-id="6e852-132">Высота страницы.</span><span class="sxs-lookup"><span data-stu-id="6e852-132">The height of the page.</span></span>                                                            | <span data-ttu-id="6e852-133">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="6e852-133">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="6e852-134">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="6e852-134">**LineHeight**</span></span> | <span data-ttu-id="6e852-135">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="6e852-135">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="6e852-136">Необязательно</span><span class="sxs-lookup"><span data-stu-id="6e852-136">Optional</span></span> | <span data-ttu-id="6e852-137">Высота линии, используемой на странице.</span><span class="sxs-lookup"><span data-stu-id="6e852-137">The height of the line used on the page.</span></span>                                           | <span data-ttu-id="6e852-138">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="6e852-138">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="6e852-139">**LanguageId**</span><span class="sxs-lookup"><span data-stu-id="6e852-139">**LanguageId**</span></span> | <span data-ttu-id="6e852-140">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="6e852-140">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="6e852-141">Необязательно</span><span class="sxs-lookup"><span data-stu-id="6e852-141">Optional</span></span> | <span data-ttu-id="6e852-142">Идентификатор языка, используемый для страницы.</span><span class="sxs-lookup"><span data-stu-id="6e852-142">The language id used for the page.</span></span>                                                 | <span data-ttu-id="6e852-143">Неотрицательное целое число, представляющее допустимый идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="6e852-143">A non-negative integer representing a valid language id.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="6e852-144">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6e852-144">Element Information</span></span>



|              |                                                                     |
|--------------|---------------------------------------------------------------------|
| <span data-ttu-id="6e852-145">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="6e852-145">Element type</span></span> | <span data-ttu-id="6e852-146">[**Жаурналпажетипе**](journalpagetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="6e852-146">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="6e852-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6e852-147">Namespace</span></span>    | <span data-ttu-id="6e852-148">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="6e852-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                          |
| <span data-ttu-id="6e852-149">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="6e852-149">Schema name</span></span>  | <span data-ttu-id="6e852-150">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="6e852-150">Journal Reader</span></span>                                                      |



 

 

 



