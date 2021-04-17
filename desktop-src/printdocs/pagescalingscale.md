---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 49a60a94-fb65-4439-bebf-3f77ea0861fe
title: пажескалингскале
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246f77c5878b74e1b149c6d4020230030fb3c5b0
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703515"
---
# <a name="pagescalingscale"></a><span data-ttu-id="44c4c-104">пажескалингскале</span><span class="sxs-lookup"><span data-stu-id="44c4c-104">PageScalingScale</span></span>

<span data-ttu-id="44c4c-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="44c4c-105">This topic is not current.</span></span> <span data-ttu-id="44c4c-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="44c4c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="44c4c-107">Задает коэффициент масштабирования для пользовательского квадратичного масштабирования.</span><span class="sxs-lookup"><span data-stu-id="44c4c-107">Specifies the scaling factor for custom square scaling.</span></span>

-   [<span data-ttu-id="44c4c-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="44c4c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="44c4c-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="44c4c-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="44c4c-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="44c4c-110">Element Information</span></span>



| <span data-ttu-id="44c4c-111">Имя</span><span class="sxs-lookup"><span data-stu-id="44c4c-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="44c4c-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="44c4c-112">Element Type</span></span> <br/>   | <span data-ttu-id="44c4c-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="44c4c-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="44c4c-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="44c4c-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="44c4c-115">Страница</span><span class="sxs-lookup"><span data-stu-id="44c4c-115">Page</span></span><br/>                                         |
| <span data-ttu-id="44c4c-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="44c4c-116">Notes</span></span> <br/>          | <span data-ttu-id="44c4c-117">Ссылка на элемент Пажескалинг, Пользовательский параметр</span><span class="sxs-lookup"><span data-stu-id="44c4c-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="44c4c-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="44c4c-118">Structure Content</span></span>

<span data-ttu-id="44c4c-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="44c4c-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScale">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="44c4c-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="44c4c-120">Structure Properties</span></span>

<span data-ttu-id="44c4c-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="44c4c-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="44c4c-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="44c4c-122">Property</span></span>                | <span data-ttu-id="44c4c-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="44c4c-123">xsi:type</span></span>           | <span data-ttu-id="44c4c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="44c4c-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="44c4c-125">DataType</span><span class="sxs-lookup"><span data-stu-id="44c4c-125">DataType</span></span><br/>     | <span data-ttu-id="44c4c-126">строка</span><span class="sxs-lookup"><span data-stu-id="44c4c-126">string</span></span><br/>  | <span data-ttu-id="44c4c-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="44c4c-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="44c4c-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="44c4c-128">DefaultValue</span></span><br/> | <span data-ttu-id="44c4c-129">Целое число</span><span class="sxs-lookup"><span data-stu-id="44c4c-129">integer</span></span><br/> | <span data-ttu-id="44c4c-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="44c4c-130">undefined</span></span><br/>       |
| <span data-ttu-id="44c4c-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="44c4c-131">MaxValue</span></span><br/>     | <span data-ttu-id="44c4c-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="44c4c-132">integer</span></span><br/> | <span data-ttu-id="44c4c-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="44c4c-133">undefined</span></span><br/>       |
| <span data-ttu-id="44c4c-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="44c4c-134">MinValue</span></span><br/>     | <span data-ttu-id="44c4c-135">целое число</span><span class="sxs-lookup"><span data-stu-id="44c4c-135">integer</span></span><br/> | <span data-ttu-id="44c4c-136">1</span><span class="sxs-lookup"><span data-stu-id="44c4c-136">1</span></span><br/>               |
| <span data-ttu-id="44c4c-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="44c4c-137">Mandatory</span></span><br/>    | <span data-ttu-id="44c4c-138">строка</span><span class="sxs-lookup"><span data-stu-id="44c4c-138">string</span></span><br/>  | <span data-ttu-id="44c4c-139">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="44c4c-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="44c4c-140">Несколько</span><span class="sxs-lookup"><span data-stu-id="44c4c-140">Multiple</span></span><br/>     | <span data-ttu-id="44c4c-141">целое число</span><span class="sxs-lookup"><span data-stu-id="44c4c-141">integer</span></span><br/> | <span data-ttu-id="44c4c-142">1</span><span class="sxs-lookup"><span data-stu-id="44c4c-142">1</span></span><br/>               |
| <span data-ttu-id="44c4c-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="44c4c-143">UnitType</span></span><br/>     | <span data-ttu-id="44c4c-144">строка</span><span class="sxs-lookup"><span data-stu-id="44c4c-144">string</span></span><br/>  | <span data-ttu-id="44c4c-145">percent</span><span class="sxs-lookup"><span data-stu-id="44c4c-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="44c4c-146">См. также</span><span class="sxs-lookup"><span data-stu-id="44c4c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44c4c-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="44c4c-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




