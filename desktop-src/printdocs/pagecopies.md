---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: пажекопиес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b1fc822d27d104364c2414ca89cf1fdf30c7d3
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997671"
---
# <a name="pagecopies"></a><span data-ttu-id="1573f-104">пажекопиес</span><span class="sxs-lookup"><span data-stu-id="1573f-104">PageCopies</span></span>

<span data-ttu-id="1573f-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="1573f-105">This topic is not current.</span></span> <span data-ttu-id="1573f-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1573f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1573f-107">Указывает количество копий страницы.</span><span class="sxs-lookup"><span data-stu-id="1573f-107">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="1573f-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1573f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1573f-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="1573f-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1573f-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1573f-110">Element Information</span></span>



| <span data-ttu-id="1573f-111">Имя</span><span class="sxs-lookup"><span data-stu-id="1573f-111">Name</span></span> | <span data-ttu-id="1573f-112">Значение</span><span class="sxs-lookup"><span data-stu-id="1573f-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="1573f-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="1573f-113">Element Type</span></span> <br/>   | <span data-ttu-id="1573f-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="1573f-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="1573f-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="1573f-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1573f-116">Страница</span><span class="sxs-lookup"><span data-stu-id="1573f-116">Page</span></span><br/>         |
| <span data-ttu-id="1573f-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="1573f-117">Notes</span></span> <br/>          | <span data-ttu-id="1573f-118">Нет</span><span class="sxs-lookup"><span data-stu-id="1573f-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="1573f-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="1573f-119">Structure Content</span></span>

<span data-ttu-id="1573f-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="1573f-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageCopies">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="1573f-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="1573f-121">Structure Properties</span></span>

<span data-ttu-id="1573f-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="1573f-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1573f-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="1573f-123">Property</span></span>                | <span data-ttu-id="1573f-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1573f-124">xsi:type</span></span>           | <span data-ttu-id="1573f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1573f-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="1573f-126">DataType</span><span class="sxs-lookup"><span data-stu-id="1573f-126">DataType</span></span><br/>     | <span data-ttu-id="1573f-127">строка</span><span class="sxs-lookup"><span data-stu-id="1573f-127">string</span></span><br/>  | <span data-ttu-id="1573f-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1573f-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="1573f-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1573f-129">DefaultValue</span></span><br/> | <span data-ttu-id="1573f-130">целое число</span><span class="sxs-lookup"><span data-stu-id="1573f-130">integer</span></span><br/> | <span data-ttu-id="1573f-131">1</span><span class="sxs-lookup"><span data-stu-id="1573f-131">1</span></span><br/>                 |
| <span data-ttu-id="1573f-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1573f-132">MaxValue</span></span><br/>     | <span data-ttu-id="1573f-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="1573f-133">integer</span></span><br/> | <span data-ttu-id="1573f-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="1573f-134">undefined</span></span><br/>         |
| <span data-ttu-id="1573f-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="1573f-135">MinValue</span></span><br/>     | <span data-ttu-id="1573f-136">целое число</span><span class="sxs-lookup"><span data-stu-id="1573f-136">integer</span></span><br/> | <span data-ttu-id="1573f-137">1</span><span class="sxs-lookup"><span data-stu-id="1573f-137">1</span></span><br/>                 |
| <span data-ttu-id="1573f-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1573f-138">Mandatory</span></span><br/>    | <span data-ttu-id="1573f-139">строка</span><span class="sxs-lookup"><span data-stu-id="1573f-139">string</span></span><br/>  | <span data-ttu-id="1573f-140">PSK: безусловное</span><span class="sxs-lookup"><span data-stu-id="1573f-140">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="1573f-141">Несколько</span><span class="sxs-lookup"><span data-stu-id="1573f-141">Multiple</span></span><br/>     | <span data-ttu-id="1573f-142">целое число</span><span class="sxs-lookup"><span data-stu-id="1573f-142">integer</span></span><br/> | <span data-ttu-id="1573f-143">1</span><span class="sxs-lookup"><span data-stu-id="1573f-143">1</span></span><br/>                 |
| <span data-ttu-id="1573f-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="1573f-144">UnitType</span></span><br/>     | <span data-ttu-id="1573f-145">строка</span><span class="sxs-lookup"><span data-stu-id="1573f-145">string</span></span><br/>  | <span data-ttu-id="1573f-146">Копи</span><span class="sxs-lookup"><span data-stu-id="1573f-146">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="1573f-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1573f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1573f-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="1573f-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




