---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: e1cb7e46-3078-46bf-a8c8-e10f6b9dd222
title: документимпоситионколор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228d1efded114c9471a55c4f88ca6e51ed6337ca
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997871"
---
# <a name="documentimpositioncolor"></a><span data-ttu-id="b5e00-104">документимпоситионколор</span><span class="sxs-lookup"><span data-stu-id="b5e00-104">DocumentImpositionColor</span></span>

<span data-ttu-id="b5e00-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="b5e00-105">This topic is not current.</span></span> <span data-ttu-id="b5e00-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b5e00-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b5e00-107">Содержимое приложения с меткой указанного именованного цвета должно отображаться во всех цветоделении.</span><span class="sxs-lookup"><span data-stu-id="b5e00-107">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="b5e00-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b5e00-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b5e00-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="b5e00-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b5e00-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b5e00-110">Element Information</span></span>



| <span data-ttu-id="b5e00-111">Имя</span><span class="sxs-lookup"><span data-stu-id="b5e00-111">Name</span></span> | <span data-ttu-id="b5e00-112">Значение</span><span class="sxs-lookup"><span data-stu-id="b5e00-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="b5e00-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="b5e00-113">Element Type</span></span> <br/>   | <span data-ttu-id="b5e00-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="b5e00-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="b5e00-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="b5e00-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b5e00-116">Документ</span><span class="sxs-lookup"><span data-stu-id="b5e00-116">Document</span></span><br/>     |
| <span data-ttu-id="b5e00-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="b5e00-117">Notes</span></span> <br/>          | <span data-ttu-id="b5e00-118">Нет</span><span class="sxs-lookup"><span data-stu-id="b5e00-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="b5e00-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="b5e00-119">Structure Content</span></span>

<span data-ttu-id="b5e00-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="b5e00-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="b5e00-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="b5e00-121">Structure Properties</span></span>

<span data-ttu-id="b5e00-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="b5e00-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b5e00-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="b5e00-123">Property</span></span>                | <span data-ttu-id="b5e00-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b5e00-124">xsi:type</span></span>           | <span data-ttu-id="b5e00-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b5e00-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b5e00-126">DataType</span><span class="sxs-lookup"><span data-stu-id="b5e00-126">DataType</span></span><br/>     | <span data-ttu-id="b5e00-127">строка</span><span class="sxs-lookup"><span data-stu-id="b5e00-127">string</span></span><br/>  | <span data-ttu-id="b5e00-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="b5e00-128">xs:string</span></span><br/>       |
| <span data-ttu-id="b5e00-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b5e00-129">DefaultValue</span></span><br/> | <span data-ttu-id="b5e00-130">строка</span><span class="sxs-lookup"><span data-stu-id="b5e00-130">string</span></span><br/>  | <span data-ttu-id="b5e00-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="b5e00-131">undefined</span></span><br/>       |
| <span data-ttu-id="b5e00-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="b5e00-132">MaxLength</span></span><br/>    | <span data-ttu-id="b5e00-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="b5e00-133">integer</span></span><br/> | <span data-ttu-id="b5e00-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="b5e00-134">undefined</span></span><br/>       |
| <span data-ttu-id="b5e00-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="b5e00-135">MinLength</span></span><br/>    | <span data-ttu-id="b5e00-136">целое число</span><span class="sxs-lookup"><span data-stu-id="b5e00-136">integer</span></span><br/> | <span data-ttu-id="b5e00-137">1</span><span class="sxs-lookup"><span data-stu-id="b5e00-137">1</span></span><br/>               |
| <span data-ttu-id="b5e00-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b5e00-138">Mandatory</span></span><br/>    | <span data-ttu-id="b5e00-139">строка</span><span class="sxs-lookup"><span data-stu-id="b5e00-139">string</span></span><br/>  | <span data-ttu-id="b5e00-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="b5e00-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b5e00-141">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="b5e00-141">UnitType</span></span><br/>     | <span data-ttu-id="b5e00-142">строка</span><span class="sxs-lookup"><span data-stu-id="b5e00-142">string</span></span><br/>  | <span data-ttu-id="b5e00-143">characters</span><span class="sxs-lookup"><span data-stu-id="b5e00-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="b5e00-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b5e00-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5e00-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="b5e00-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




