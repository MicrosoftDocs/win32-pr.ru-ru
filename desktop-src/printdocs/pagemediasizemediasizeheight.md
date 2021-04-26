---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 209b3024-60cf-47e0-8738-cd7795e38c2a
title: пажемедиасиземедиасизехеигхт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 305f67179343fa4acb2fa784113d63d5d2333b0b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993711"
---
# <a name="pagemediasizemediasizeheight"></a><span data-ttu-id="4f6c2-104">пажемедиасиземедиасизехеигхт</span><span class="sxs-lookup"><span data-stu-id="4f6c2-104">PageMediaSizeMediaSizeHeight</span></span>

<span data-ttu-id="4f6c2-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="4f6c2-105">This topic is not current.</span></span> <span data-ttu-id="4f6c2-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4f6c2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4f6c2-107">Задает направление Медиасизехеигхт измерения для настраиваемого параметра Медиасизе.</span><span class="sxs-lookup"><span data-stu-id="4f6c2-107">Specifies the dimension MediaSizeHeight direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="4f6c2-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4f6c2-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4f6c2-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="4f6c2-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4f6c2-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4f6c2-110">Element Information</span></span>



| <span data-ttu-id="4f6c2-111">Имя</span><span class="sxs-lookup"><span data-stu-id="4f6c2-111">Name</span></span> | <span data-ttu-id="4f6c2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4f6c2-112">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="4f6c2-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="4f6c2-113">Element Type</span></span> <br/>   | <span data-ttu-id="4f6c2-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="4f6c2-114">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="4f6c2-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="4f6c2-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4f6c2-116">Страница</span><span class="sxs-lookup"><span data-stu-id="4f6c2-116">Page</span></span><br/>                                           |
| <span data-ttu-id="4f6c2-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="4f6c2-117">Notes</span></span> <br/>          | <span data-ttu-id="4f6c2-118">Ссылка на элемент Пажемедиасизе, Пользовательский параметр</span><span class="sxs-lookup"><span data-stu-id="4f6c2-118">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4f6c2-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="4f6c2-119">Structure Content</span></span>

<span data-ttu-id="4f6c2-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="4f6c2-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="4f6c2-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="4f6c2-121">Structure Properties</span></span>

<span data-ttu-id="4f6c2-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="4f6c2-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4f6c2-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="4f6c2-123">Property</span></span>                | <span data-ttu-id="4f6c2-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4f6c2-124">xsi:type</span></span>           | <span data-ttu-id="4f6c2-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4f6c2-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4f6c2-126">DataType</span><span class="sxs-lookup"><span data-stu-id="4f6c2-126">DataType</span></span><br/>     | <span data-ttu-id="4f6c2-127">строка</span><span class="sxs-lookup"><span data-stu-id="4f6c2-127">string</span></span><br/>  | <span data-ttu-id="4f6c2-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4f6c2-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="4f6c2-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4f6c2-129">DefaultValue</span></span><br/> | <span data-ttu-id="4f6c2-130">Целое число</span><span class="sxs-lookup"><span data-stu-id="4f6c2-130">integer</span></span><br/> | <span data-ttu-id="4f6c2-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="4f6c2-131">undefined</span></span><br/>       |
| <span data-ttu-id="4f6c2-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="4f6c2-132">MaxValue</span></span><br/>     | <span data-ttu-id="4f6c2-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="4f6c2-133">integer</span></span><br/> | <span data-ttu-id="4f6c2-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="4f6c2-134">undefined</span></span><br/>       |
| <span data-ttu-id="4f6c2-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="4f6c2-135">MinValue</span></span><br/>     | <span data-ttu-id="4f6c2-136">Целое число</span><span class="sxs-lookup"><span data-stu-id="4f6c2-136">integer</span></span><br/> | <span data-ttu-id="4f6c2-137">неопределенный</span><span class="sxs-lookup"><span data-stu-id="4f6c2-137">undefined</span></span><br/>       |
| <span data-ttu-id="4f6c2-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4f6c2-138">Mandatory</span></span><br/>    | <span data-ttu-id="4f6c2-139">строка</span><span class="sxs-lookup"><span data-stu-id="4f6c2-139">string</span></span><br/>  | <span data-ttu-id="4f6c2-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="4f6c2-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4f6c2-141">Несколько</span><span class="sxs-lookup"><span data-stu-id="4f6c2-141">Multiple</span></span><br/>     | <span data-ttu-id="4f6c2-142">целое число</span><span class="sxs-lookup"><span data-stu-id="4f6c2-142">integer</span></span><br/> | <span data-ttu-id="4f6c2-143">1</span><span class="sxs-lookup"><span data-stu-id="4f6c2-143">1</span></span><br/>               |
| <span data-ttu-id="4f6c2-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="4f6c2-144">UnitType</span></span><br/>     | <span data-ttu-id="4f6c2-145">строка</span><span class="sxs-lookup"><span data-stu-id="4f6c2-145">string</span></span><br/>  | <span data-ttu-id="4f6c2-146">мкм</span><span class="sxs-lookup"><span data-stu-id="4f6c2-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="4f6c2-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="4f6c2-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f6c2-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="4f6c2-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




