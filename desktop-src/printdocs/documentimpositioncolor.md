---
description: Сведения о параметре Документимпоситионколор. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: e1cb7e46-3078-46bf-a8c8-e10f6b9dd222
title: документимпоситионколор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b747487c19160d29778f306a91b62cf43d245f65
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120009"
---
# <a name="documentimpositioncolor"></a><span data-ttu-id="63290-105">документимпоситионколор</span><span class="sxs-lookup"><span data-stu-id="63290-105">DocumentImpositionColor</span></span>

<span data-ttu-id="63290-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="63290-106">This topic is not current.</span></span> <span data-ttu-id="63290-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="63290-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="63290-108">Содержимое приложения с меткой указанного именованного цвета должно отображаться во всех цветоделении.</span><span class="sxs-lookup"><span data-stu-id="63290-108">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="63290-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="63290-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="63290-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="63290-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="63290-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="63290-111">Element Information</span></span>



| <span data-ttu-id="63290-112">Имя</span><span class="sxs-lookup"><span data-stu-id="63290-112">Name</span></span> | <span data-ttu-id="63290-113">Значение</span><span class="sxs-lookup"><span data-stu-id="63290-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="63290-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="63290-114">Element Type</span></span> <br/>   | <span data-ttu-id="63290-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="63290-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="63290-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="63290-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="63290-117">Документ</span><span class="sxs-lookup"><span data-stu-id="63290-117">Document</span></span><br/>     |
| <span data-ttu-id="63290-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="63290-118">Notes</span></span> <br/>          | <span data-ttu-id="63290-119">Нет</span><span class="sxs-lookup"><span data-stu-id="63290-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="63290-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="63290-120">Structure Content</span></span>

<span data-ttu-id="63290-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="63290-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentImpositionColor">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="63290-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="63290-122">Structure Properties</span></span>

<span data-ttu-id="63290-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="63290-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="63290-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="63290-124">Property</span></span>                | <span data-ttu-id="63290-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="63290-125">xsi:type</span></span>           | <span data-ttu-id="63290-126">Значение</span><span class="sxs-lookup"><span data-stu-id="63290-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="63290-127">DataType</span><span class="sxs-lookup"><span data-stu-id="63290-127">DataType</span></span><br/>     | <span data-ttu-id="63290-128">строка</span><span class="sxs-lookup"><span data-stu-id="63290-128">string</span></span><br/>  | <span data-ttu-id="63290-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="63290-129">xs:string</span></span><br/>       |
| <span data-ttu-id="63290-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="63290-130">DefaultValue</span></span><br/> | <span data-ttu-id="63290-131">строка</span><span class="sxs-lookup"><span data-stu-id="63290-131">string</span></span><br/>  | <span data-ttu-id="63290-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="63290-132">undefined</span></span><br/>       |
| <span data-ttu-id="63290-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="63290-133">MaxLength</span></span><br/>    | <span data-ttu-id="63290-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="63290-134">integer</span></span><br/> | <span data-ttu-id="63290-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="63290-135">undefined</span></span><br/>       |
| <span data-ttu-id="63290-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="63290-136">MinLength</span></span><br/>    | <span data-ttu-id="63290-137">целое число</span><span class="sxs-lookup"><span data-stu-id="63290-137">integer</span></span><br/> | <span data-ttu-id="63290-138">1</span><span class="sxs-lookup"><span data-stu-id="63290-138">1</span></span><br/>               |
| <span data-ttu-id="63290-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="63290-139">Mandatory</span></span><br/>    | <span data-ttu-id="63290-140">строка</span><span class="sxs-lookup"><span data-stu-id="63290-140">string</span></span><br/>  | <span data-ttu-id="63290-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="63290-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="63290-142">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="63290-142">UnitType</span></span><br/>     | <span data-ttu-id="63290-143">строка</span><span class="sxs-lookup"><span data-stu-id="63290-143">string</span></span><br/>  | <span data-ttu-id="63290-144">characters</span><span class="sxs-lookup"><span data-stu-id="63290-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="63290-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="63290-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63290-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="63290-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




