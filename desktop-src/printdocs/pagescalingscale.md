---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 49a60a94-fb65-4439-bebf-3f77ea0861fe
title: пажескалингскале
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974242cf43bae50a8e81b17bcdd13d653032c6a9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999201"
---
# <a name="pagescalingscale"></a><span data-ttu-id="4ce0b-104">пажескалингскале</span><span class="sxs-lookup"><span data-stu-id="4ce0b-104">PageScalingScale</span></span>

<span data-ttu-id="4ce0b-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="4ce0b-105">This topic is not current.</span></span> <span data-ttu-id="4ce0b-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4ce0b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4ce0b-107">Задает коэффициент масштабирования для пользовательского квадратичного масштабирования.</span><span class="sxs-lookup"><span data-stu-id="4ce0b-107">Specifies the scaling factor for custom square scaling.</span></span>

-   [<span data-ttu-id="4ce0b-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4ce0b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4ce0b-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="4ce0b-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4ce0b-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4ce0b-110">Element Information</span></span>



| <span data-ttu-id="4ce0b-111">Имя</span><span class="sxs-lookup"><span data-stu-id="4ce0b-111">Name</span></span> | <span data-ttu-id="4ce0b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4ce0b-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="4ce0b-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="4ce0b-113">Element Type</span></span> <br/>   | <span data-ttu-id="4ce0b-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="4ce0b-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="4ce0b-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="4ce0b-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4ce0b-116">Страница</span><span class="sxs-lookup"><span data-stu-id="4ce0b-116">Page</span></span><br/>                                         |
| <span data-ttu-id="4ce0b-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="4ce0b-117">Notes</span></span> <br/>          | <span data-ttu-id="4ce0b-118">Ссылка на элемент Пажескалинг, Пользовательский параметр</span><span class="sxs-lookup"><span data-stu-id="4ce0b-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4ce0b-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="4ce0b-119">Structure Content</span></span>

<span data-ttu-id="4ce0b-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="4ce0b-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="4ce0b-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="4ce0b-121">Structure Properties</span></span>

<span data-ttu-id="4ce0b-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="4ce0b-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4ce0b-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="4ce0b-123">Property</span></span>                | <span data-ttu-id="4ce0b-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4ce0b-124">xsi:type</span></span>           | <span data-ttu-id="4ce0b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4ce0b-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4ce0b-126">DataType</span><span class="sxs-lookup"><span data-stu-id="4ce0b-126">DataType</span></span><br/>     | <span data-ttu-id="4ce0b-127">строка</span><span class="sxs-lookup"><span data-stu-id="4ce0b-127">string</span></span><br/>  | <span data-ttu-id="4ce0b-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4ce0b-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="4ce0b-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4ce0b-129">DefaultValue</span></span><br/> | <span data-ttu-id="4ce0b-130">Целое число</span><span class="sxs-lookup"><span data-stu-id="4ce0b-130">integer</span></span><br/> | <span data-ttu-id="4ce0b-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="4ce0b-131">undefined</span></span><br/>       |
| <span data-ttu-id="4ce0b-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="4ce0b-132">MaxValue</span></span><br/>     | <span data-ttu-id="4ce0b-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="4ce0b-133">integer</span></span><br/> | <span data-ttu-id="4ce0b-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="4ce0b-134">undefined</span></span><br/>       |
| <span data-ttu-id="4ce0b-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="4ce0b-135">MinValue</span></span><br/>     | <span data-ttu-id="4ce0b-136">целое число</span><span class="sxs-lookup"><span data-stu-id="4ce0b-136">integer</span></span><br/> | <span data-ttu-id="4ce0b-137">1</span><span class="sxs-lookup"><span data-stu-id="4ce0b-137">1</span></span><br/>               |
| <span data-ttu-id="4ce0b-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4ce0b-138">Mandatory</span></span><br/>    | <span data-ttu-id="4ce0b-139">строка</span><span class="sxs-lookup"><span data-stu-id="4ce0b-139">string</span></span><br/>  | <span data-ttu-id="4ce0b-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="4ce0b-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4ce0b-141">Несколько</span><span class="sxs-lookup"><span data-stu-id="4ce0b-141">Multiple</span></span><br/>     | <span data-ttu-id="4ce0b-142">целое число</span><span class="sxs-lookup"><span data-stu-id="4ce0b-142">integer</span></span><br/> | <span data-ttu-id="4ce0b-143">1</span><span class="sxs-lookup"><span data-stu-id="4ce0b-143">1</span></span><br/>               |
| <span data-ttu-id="4ce0b-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="4ce0b-144">UnitType</span></span><br/>     | <span data-ttu-id="4ce0b-145">строка</span><span class="sxs-lookup"><span data-stu-id="4ce0b-145">string</span></span><br/>  | <span data-ttu-id="4ce0b-146">percent</span><span class="sxs-lookup"><span data-stu-id="4ce0b-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="4ce0b-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="4ce0b-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ce0b-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="4ce0b-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




