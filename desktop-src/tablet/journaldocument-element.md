---
description: Элемент верхнего уровня в XML-файле заметки журнала.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Жаурналдокумент, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7820ef68dc87bf42d9580c800e2e165f2f2859a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432176"
---
# <a name="journaldocument-element"></a><span data-ttu-id="38699-103">Жаурналдокумент, элемент</span><span class="sxs-lookup"><span data-stu-id="38699-103">JournalDocument Element</span></span>

<span data-ttu-id="38699-104">Элемент верхнего уровня в XML-файле заметки журнала.</span><span class="sxs-lookup"><span data-stu-id="38699-104">The top-level element in a Journal note XML file.</span></span>

## <a name="definition"></a><span data-ttu-id="38699-105">Определение</span><span class="sxs-lookup"><span data-stu-id="38699-105">Definition</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="38699-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="38699-106">Parent Elements</span></span>

<span data-ttu-id="38699-107">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="38699-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="38699-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="38699-108">Child Elements</span></span>

[<span data-ttu-id="38699-109">**Stationery**</span><span class="sxs-lookup"><span data-stu-id="38699-109">**Stationery**</span></span>](stationery-element.md)

[<span data-ttu-id="38699-110">**жаурналпаже**</span><span class="sxs-lookup"><span data-stu-id="38699-110">**JournalPage**</span></span>](journalpage-element.md)

## <a name="attributes"></a><span data-ttu-id="38699-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="38699-111">Attributes</span></span>



| <span data-ttu-id="38699-112">attribute</span><span class="sxs-lookup"><span data-stu-id="38699-112">Attribute</span></span>             | <span data-ttu-id="38699-113">Тип</span><span class="sxs-lookup"><span data-stu-id="38699-113">Type</span></span>                      | <span data-ttu-id="38699-114">Обязательно</span><span class="sxs-lookup"><span data-stu-id="38699-114">Required</span></span> | <span data-ttu-id="38699-115">Описание</span><span class="sxs-lookup"><span data-stu-id="38699-115">Description</span></span>                                                      | <span data-ttu-id="38699-116">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="38699-116">Possible Values</span></span>           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="38699-117">**Версия**</span><span class="sxs-lookup"><span data-stu-id="38699-117">**Version**</span></span>           | <span data-ttu-id="38699-118">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="38699-118">**xs:string**</span></span>             | <span data-ttu-id="38699-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="38699-119">Required</span></span> | <span data-ttu-id="38699-120">Версия документа журнала, представленного в XML-файле.</span><span class="sxs-lookup"><span data-stu-id="38699-120">The version of the Journal document represented in the XML file.</span></span> | <span data-ttu-id="38699-121">1.0</span><span class="sxs-lookup"><span data-stu-id="38699-121">1.0</span></span>                       |
| <span data-ttu-id="38699-122">**дефаултпажевидс**</span><span class="sxs-lookup"><span data-stu-id="38699-122">**DefaultPageWidth**</span></span>  | <span data-ttu-id="38699-123">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="38699-123">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="38699-124">Обязательно</span><span class="sxs-lookup"><span data-stu-id="38699-124">Required</span></span> | <span data-ttu-id="38699-125">Ширина страницы по умолчанию для документа журнала.</span><span class="sxs-lookup"><span data-stu-id="38699-125">The default width of the page for the Journal document.</span></span>          | <span data-ttu-id="38699-126">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="38699-126">Any non-negative integer.</span></span> |
| <span data-ttu-id="38699-127">**дефаултпажехеигхт**</span><span class="sxs-lookup"><span data-stu-id="38699-127">**DefaultPageHeight**</span></span> | <span data-ttu-id="38699-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="38699-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="38699-129">Обязательно</span><span class="sxs-lookup"><span data-stu-id="38699-129">Required</span></span> | <span data-ttu-id="38699-130">Высота по умолчанию страницы для документа журнала.</span><span class="sxs-lookup"><span data-stu-id="38699-130">The default height of the page for the Journal document.</span></span>         | <span data-ttu-id="38699-131">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="38699-131">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="38699-132">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="38699-132">Element Information</span></span>



|  <span data-ttu-id="38699-133">Элемент</span><span class="sxs-lookup"><span data-stu-id="38699-133">Element</span></span>     | <span data-ttu-id="38699-134">Значение</span><span class="sxs-lookup"><span data-stu-id="38699-134">Value</span></span>                                                     |
|--------------|--------------------------------------------|
| <span data-ttu-id="38699-135">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="38699-135">Element type</span></span> | <span data-ttu-id="38699-136">**жаурналдокумент**</span><span class="sxs-lookup"><span data-stu-id="38699-136">**JournalDocument**</span></span>                        |
| <span data-ttu-id="38699-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="38699-137">Namespace</span></span>    | <span data-ttu-id="38699-138">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="38699-138">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="38699-139">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="38699-139">Schema name</span></span>  | <span data-ttu-id="38699-140">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="38699-140">Journal Reader</span></span>                             |



 

 

 



