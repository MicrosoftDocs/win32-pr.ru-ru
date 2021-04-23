---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 96b48917-1fbc-467f-b2b4-1a9673f1ee99
title: пажеблаккженератионпроцессингблаккинклимит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f565b6190f9bda11727efde6e799b6fb979cecc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105656739"
---
# <a name="pageblackgenerationprocessingblackinklimit"></a><span data-ttu-id="7cb24-104">пажеблаккженератионпроцессингблаккинклимит</span><span class="sxs-lookup"><span data-stu-id="7cb24-104">PageBlackGenerationProcessingBlackInkLimit</span></span>

<span data-ttu-id="7cb24-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="7cb24-105">This topic is not current.</span></span> <span data-ttu-id="7cb24-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7cb24-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7cb24-107">Содержимое приложения с меткой указанного именованного цвета должно отображаться во всех цветоделении.</span><span class="sxs-lookup"><span data-stu-id="7cb24-107">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="7cb24-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7cb24-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7cb24-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="7cb24-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7cb24-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7cb24-110">Element Information</span></span>



| <span data-ttu-id="7cb24-111">Имя</span><span class="sxs-lookup"><span data-stu-id="7cb24-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="7cb24-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="7cb24-112">Element Type</span></span> <br/>   | <span data-ttu-id="7cb24-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="7cb24-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="7cb24-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="7cb24-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7cb24-115">Страница</span><span class="sxs-lookup"><span data-stu-id="7cb24-115">Page</span></span><br/>                                            |
| <span data-ttu-id="7cb24-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="7cb24-116">Notes</span></span> <br/>          | <span data-ttu-id="7cb24-117">Связано с элементом Пажеблаккженератионпроцессинг</span><span class="sxs-lookup"><span data-stu-id="7cb24-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7cb24-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="7cb24-118">Structure Content</span></span>

<span data-ttu-id="7cb24-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="7cb24-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingBlackInkLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="7cb24-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="7cb24-120">Structure Properties</span></span>

<span data-ttu-id="7cb24-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="7cb24-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7cb24-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="7cb24-122">Property</span></span>                | <span data-ttu-id="7cb24-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7cb24-123">xsi:type</span></span>           | <span data-ttu-id="7cb24-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7cb24-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7cb24-125">DataType</span><span class="sxs-lookup"><span data-stu-id="7cb24-125">DataType</span></span><br/>     | <span data-ttu-id="7cb24-126">строка</span><span class="sxs-lookup"><span data-stu-id="7cb24-126">string</span></span><br/>  | <span data-ttu-id="7cb24-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7cb24-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="7cb24-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7cb24-128">DefaultValue</span></span><br/> | <span data-ttu-id="7cb24-129">строка</span><span class="sxs-lookup"><span data-stu-id="7cb24-129">string</span></span><br/>  | <span data-ttu-id="7cb24-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="7cb24-130">undefined</span></span><br/>       |
| <span data-ttu-id="7cb24-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7cb24-131">MaxValue</span></span><br/>     | <span data-ttu-id="7cb24-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="7cb24-132">integer</span></span><br/> | <span data-ttu-id="7cb24-133">100</span><span class="sxs-lookup"><span data-stu-id="7cb24-133">100</span></span><br/>             |
| <span data-ttu-id="7cb24-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="7cb24-134">MinValue</span></span><br/>     | <span data-ttu-id="7cb24-135">целое число</span><span class="sxs-lookup"><span data-stu-id="7cb24-135">integer</span></span><br/> | <span data-ttu-id="7cb24-136">0</span><span class="sxs-lookup"><span data-stu-id="7cb24-136">0</span></span><br/>               |
| <span data-ttu-id="7cb24-137">Несколько</span><span class="sxs-lookup"><span data-stu-id="7cb24-137">Multiple</span></span><br/>     | <span data-ttu-id="7cb24-138">целое число</span><span class="sxs-lookup"><span data-stu-id="7cb24-138">integer</span></span><br/> | <span data-ttu-id="7cb24-139">1</span><span class="sxs-lookup"><span data-stu-id="7cb24-139">1</span></span><br/>               |
| <span data-ttu-id="7cb24-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7cb24-140">Mandatory</span></span><br/>    | <span data-ttu-id="7cb24-141">строка</span><span class="sxs-lookup"><span data-stu-id="7cb24-141">string</span></span><br/>  | <span data-ttu-id="7cb24-142">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="7cb24-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7cb24-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="7cb24-143">UnitType</span></span><br/>     | <span data-ttu-id="7cb24-144">строка</span><span class="sxs-lookup"><span data-stu-id="7cb24-144">string</span></span><br/>  | <span data-ttu-id="7cb24-145">percent</span><span class="sxs-lookup"><span data-stu-id="7cb24-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="7cb24-146">См. также</span><span class="sxs-lookup"><span data-stu-id="7cb24-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cb24-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="7cb24-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




