---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 209b3024-60cf-47e0-8738-cd7795e38c2a
title: пажемедиасиземедиасизехеигхт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db500f5a64254a0e0d152cb019d7f11f25471ce3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105693906"
---
# <a name="pagemediasizemediasizeheight"></a><span data-ttu-id="e0bf7-104">пажемедиасиземедиасизехеигхт</span><span class="sxs-lookup"><span data-stu-id="e0bf7-104">PageMediaSizeMediaSizeHeight</span></span>

<span data-ttu-id="e0bf7-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="e0bf7-105">This topic is not current.</span></span> <span data-ttu-id="e0bf7-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e0bf7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e0bf7-107">Задает направление Медиасизехеигхт измерения для настраиваемого параметра Медиасизе.</span><span class="sxs-lookup"><span data-stu-id="e0bf7-107">Specifies the dimension MediaSizeHeight direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="e0bf7-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e0bf7-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e0bf7-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="e0bf7-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e0bf7-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e0bf7-110">Element Information</span></span>



| <span data-ttu-id="e0bf7-111">Имя</span><span class="sxs-lookup"><span data-stu-id="e0bf7-111">Name</span></span>                       |                                                           |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e0bf7-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="e0bf7-112">Element Type</span></span> <br/>   | <span data-ttu-id="e0bf7-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="e0bf7-113">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="e0bf7-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="e0bf7-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e0bf7-115">Страница</span><span class="sxs-lookup"><span data-stu-id="e0bf7-115">Page</span></span><br/>                                           |
| <span data-ttu-id="e0bf7-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e0bf7-116">Notes</span></span> <br/>          | <span data-ttu-id="e0bf7-117">Ссылка на элемент Пажемедиасизе, Пользовательский параметр</span><span class="sxs-lookup"><span data-stu-id="e0bf7-117">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e0bf7-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="e0bf7-118">Structure Content</span></span>

<span data-ttu-id="e0bf7-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="e0bf7-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="e0bf7-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="e0bf7-120">Structure Properties</span></span>

<span data-ttu-id="e0bf7-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="e0bf7-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e0bf7-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="e0bf7-122">Property</span></span>                | <span data-ttu-id="e0bf7-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e0bf7-123">xsi:type</span></span>           | <span data-ttu-id="e0bf7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e0bf7-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e0bf7-125">DataType</span><span class="sxs-lookup"><span data-stu-id="e0bf7-125">DataType</span></span><br/>     | <span data-ttu-id="e0bf7-126">строка</span><span class="sxs-lookup"><span data-stu-id="e0bf7-126">string</span></span><br/>  | <span data-ttu-id="e0bf7-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e0bf7-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="e0bf7-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e0bf7-128">DefaultValue</span></span><br/> | <span data-ttu-id="e0bf7-129">Целое число</span><span class="sxs-lookup"><span data-stu-id="e0bf7-129">integer</span></span><br/> | <span data-ttu-id="e0bf7-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="e0bf7-130">undefined</span></span><br/>       |
| <span data-ttu-id="e0bf7-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e0bf7-131">MaxValue</span></span><br/>     | <span data-ttu-id="e0bf7-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="e0bf7-132">integer</span></span><br/> | <span data-ttu-id="e0bf7-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="e0bf7-133">undefined</span></span><br/>       |
| <span data-ttu-id="e0bf7-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="e0bf7-134">MinValue</span></span><br/>     | <span data-ttu-id="e0bf7-135">Целое число</span><span class="sxs-lookup"><span data-stu-id="e0bf7-135">integer</span></span><br/> | <span data-ttu-id="e0bf7-136">неопределенный</span><span class="sxs-lookup"><span data-stu-id="e0bf7-136">undefined</span></span><br/>       |
| <span data-ttu-id="e0bf7-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e0bf7-137">Mandatory</span></span><br/>    | <span data-ttu-id="e0bf7-138">строка</span><span class="sxs-lookup"><span data-stu-id="e0bf7-138">string</span></span><br/>  | <span data-ttu-id="e0bf7-139">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="e0bf7-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e0bf7-140">Несколько</span><span class="sxs-lookup"><span data-stu-id="e0bf7-140">Multiple</span></span><br/>     | <span data-ttu-id="e0bf7-141">целое число</span><span class="sxs-lookup"><span data-stu-id="e0bf7-141">integer</span></span><br/> | <span data-ttu-id="e0bf7-142">1</span><span class="sxs-lookup"><span data-stu-id="e0bf7-142">1</span></span><br/>               |
| <span data-ttu-id="e0bf7-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="e0bf7-143">UnitType</span></span><br/>     | <span data-ttu-id="e0bf7-144">строка</span><span class="sxs-lookup"><span data-stu-id="e0bf7-144">string</span></span><br/>  | <span data-ttu-id="e0bf7-145">мкм</span><span class="sxs-lookup"><span data-stu-id="e0bf7-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="e0bf7-146">См. также</span><span class="sxs-lookup"><span data-stu-id="e0bf7-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0bf7-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="e0bf7-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




