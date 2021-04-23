---
description: Элемент верхнего уровня в XML-файле заметки журнала.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Жаурналдокумент, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408df14347c130e6b0a73ba869b634ca2493fb56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546919"
---
# <a name="journaldocument-element"></a><span data-ttu-id="dcb22-103">Жаурналдокумент, элемент</span><span class="sxs-lookup"><span data-stu-id="dcb22-103">JournalDocument Element</span></span>

<span data-ttu-id="dcb22-104">Элемент верхнего уровня в XML-файле заметки журнала.</span><span class="sxs-lookup"><span data-stu-id="dcb22-104">The top-level element in a Journal note XML file.</span></span>

## <a name="definition"></a><span data-ttu-id="dcb22-105">Определение</span><span class="sxs-lookup"><span data-stu-id="dcb22-105">Definition</span></span>

``` syntax
<xs:element name="JournalDocument">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="Stationery" type="StationeryType" minOccurs="0" maxOccurs="unbounded" />
    <xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
   </xs:sequence>
   <xs:attribute name="Version" type="xs:string" use="required" fixed="1.0" />
   <xs:attribute name="DefaultPageWidth" type="xs:nonNegativeInteger" use="required" />
   <xs:attribute name="DefaultPageHeight" type="xs:nonNegativeInteger" use="required" />
  </xs:complexType>
</xs:element>/>
```

## <a name="parent-elements"></a><span data-ttu-id="dcb22-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="dcb22-106">Parent Elements</span></span>

<span data-ttu-id="dcb22-107">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="dcb22-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="dcb22-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="dcb22-108">Child Elements</span></span>

[<span data-ttu-id="dcb22-109">**Stationery**</span><span class="sxs-lookup"><span data-stu-id="dcb22-109">**Stationery**</span></span>](stationery-element.md)

[<span data-ttu-id="dcb22-110">**жаурналпаже**</span><span class="sxs-lookup"><span data-stu-id="dcb22-110">**JournalPage**</span></span>](journalpage-element.md)

## <a name="attributes"></a><span data-ttu-id="dcb22-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="dcb22-111">Attributes</span></span>



| <span data-ttu-id="dcb22-112">attribute</span><span class="sxs-lookup"><span data-stu-id="dcb22-112">Attribute</span></span>             | <span data-ttu-id="dcb22-113">Тип</span><span class="sxs-lookup"><span data-stu-id="dcb22-113">Type</span></span>                      | <span data-ttu-id="dcb22-114">Обязательно</span><span class="sxs-lookup"><span data-stu-id="dcb22-114">Required</span></span> | <span data-ttu-id="dcb22-115">Описание</span><span class="sxs-lookup"><span data-stu-id="dcb22-115">Description</span></span>                                                      | <span data-ttu-id="dcb22-116">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="dcb22-116">Possible Values</span></span>           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="dcb22-117">**Version**</span><span class="sxs-lookup"><span data-stu-id="dcb22-117">**Version**</span></span>           | <span data-ttu-id="dcb22-118">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="dcb22-118">**xs:string**</span></span>             | <span data-ttu-id="dcb22-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="dcb22-119">Required</span></span> | <span data-ttu-id="dcb22-120">Версия документа журнала, представленного в XML-файле.</span><span class="sxs-lookup"><span data-stu-id="dcb22-120">The version of the Journal document represented in the XML file.</span></span> | <span data-ttu-id="dcb22-121">1.0</span><span class="sxs-lookup"><span data-stu-id="dcb22-121">1.0</span></span>                       |
| <span data-ttu-id="dcb22-122">**дефаултпажевидс**</span><span class="sxs-lookup"><span data-stu-id="dcb22-122">**DefaultPageWidth**</span></span>  | <span data-ttu-id="dcb22-123">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="dcb22-123">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="dcb22-124">Обязательно</span><span class="sxs-lookup"><span data-stu-id="dcb22-124">Required</span></span> | <span data-ttu-id="dcb22-125">Ширина страницы по умолчанию для документа журнала.</span><span class="sxs-lookup"><span data-stu-id="dcb22-125">The default width of the page for the Journal document.</span></span>          | <span data-ttu-id="dcb22-126">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="dcb22-126">Any non-negative integer.</span></span> |
| <span data-ttu-id="dcb22-127">**дефаултпажехеигхт**</span><span class="sxs-lookup"><span data-stu-id="dcb22-127">**DefaultPageHeight**</span></span> | <span data-ttu-id="dcb22-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="dcb22-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="dcb22-129">Обязательно</span><span class="sxs-lookup"><span data-stu-id="dcb22-129">Required</span></span> | <span data-ttu-id="dcb22-130">Высота по умолчанию страницы для документа журнала.</span><span class="sxs-lookup"><span data-stu-id="dcb22-130">The default height of the page for the Journal document.</span></span>         | <span data-ttu-id="dcb22-131">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="dcb22-131">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="dcb22-132">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="dcb22-132">Element Information</span></span>



|              |                                            |
|--------------|--------------------------------------------|
| <span data-ttu-id="dcb22-133">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="dcb22-133">Element type</span></span> | <span data-ttu-id="dcb22-134">**жаурналдокумент**</span><span class="sxs-lookup"><span data-stu-id="dcb22-134">**JournalDocument**</span></span>                        |
| <span data-ttu-id="dcb22-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dcb22-135">Namespace</span></span>    | <span data-ttu-id="dcb22-136">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="dcb22-136">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="dcb22-137">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="dcb22-137">Schema name</span></span>  | <span data-ttu-id="dcb22-138">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="dcb22-138">Journal Reader</span></span>                             |



 

 

 



