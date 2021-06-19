---
description: Получение сведений о параметре Пажемедиасиземедиасизехеигхт. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 209b3024-60cf-47e0-8738-cd7795e38c2a
title: пажемедиасиземедиасизехеигхт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 547077e7a63d91d6db43e8ebf6225a771bf237d8
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395799"
---
# <a name="pagemediasizemediasizeheight"></a><span data-ttu-id="474ec-105">пажемедиасиземедиасизехеигхт</span><span class="sxs-lookup"><span data-stu-id="474ec-105">PageMediaSizeMediaSizeHeight</span></span>

<span data-ttu-id="474ec-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="474ec-106">This topic is not current.</span></span> <span data-ttu-id="474ec-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="474ec-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="474ec-108">Задает направление Медиасизехеигхт измерения для настраиваемого параметра Медиасизе.</span><span class="sxs-lookup"><span data-stu-id="474ec-108">Specifies the dimension MediaSizeHeight direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="474ec-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="474ec-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="474ec-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="474ec-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="474ec-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="474ec-111">Element Information</span></span>



| <span data-ttu-id="474ec-112">Имя</span><span class="sxs-lookup"><span data-stu-id="474ec-112">Name</span></span> | <span data-ttu-id="474ec-113">Значение</span><span class="sxs-lookup"><span data-stu-id="474ec-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="474ec-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="474ec-114">Element Type</span></span> <br/>   | <span data-ttu-id="474ec-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="474ec-115">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="474ec-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="474ec-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="474ec-117">Страница</span><span class="sxs-lookup"><span data-stu-id="474ec-117">Page</span></span><br/>                                           |
| <span data-ttu-id="474ec-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="474ec-118">Notes</span></span> <br/>          | <span data-ttu-id="474ec-119">Ссылка на элемент Пажемедиасизе, Пользовательский параметр</span><span class="sxs-lookup"><span data-stu-id="474ec-119">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="474ec-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="474ec-120">Structure Content</span></span>

<span data-ttu-id="474ec-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="474ec-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="474ec-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="474ec-122">Structure Properties</span></span>

<span data-ttu-id="474ec-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="474ec-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="474ec-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="474ec-124">Property</span></span>                | <span data-ttu-id="474ec-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="474ec-125">xsi:type</span></span>           | <span data-ttu-id="474ec-126">Значение</span><span class="sxs-lookup"><span data-stu-id="474ec-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="474ec-127">DataType</span><span class="sxs-lookup"><span data-stu-id="474ec-127">DataType</span></span><br/>     | <span data-ttu-id="474ec-128">строка</span><span class="sxs-lookup"><span data-stu-id="474ec-128">string</span></span><br/>  | <span data-ttu-id="474ec-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="474ec-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="474ec-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="474ec-130">DefaultValue</span></span><br/> | <span data-ttu-id="474ec-131">Целое число</span><span class="sxs-lookup"><span data-stu-id="474ec-131">integer</span></span><br/> | <span data-ttu-id="474ec-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="474ec-132">undefined</span></span><br/>       |
| <span data-ttu-id="474ec-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="474ec-133">MaxValue</span></span><br/>     | <span data-ttu-id="474ec-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="474ec-134">integer</span></span><br/> | <span data-ttu-id="474ec-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="474ec-135">undefined</span></span><br/>       |
| <span data-ttu-id="474ec-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="474ec-136">MinValue</span></span><br/>     | <span data-ttu-id="474ec-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="474ec-137">integer</span></span><br/> | <span data-ttu-id="474ec-138">неопределенный</span><span class="sxs-lookup"><span data-stu-id="474ec-138">undefined</span></span><br/>       |
| <span data-ttu-id="474ec-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="474ec-139">Mandatory</span></span><br/>    | <span data-ttu-id="474ec-140">строка</span><span class="sxs-lookup"><span data-stu-id="474ec-140">string</span></span><br/>  | <span data-ttu-id="474ec-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="474ec-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="474ec-142">Несколько</span><span class="sxs-lookup"><span data-stu-id="474ec-142">Multiple</span></span><br/>     | <span data-ttu-id="474ec-143">целое число</span><span class="sxs-lookup"><span data-stu-id="474ec-143">integer</span></span><br/> | <span data-ttu-id="474ec-144">1</span><span class="sxs-lookup"><span data-stu-id="474ec-144">1</span></span><br/>               |
| <span data-ttu-id="474ec-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="474ec-145">UnitType</span></span><br/>     | <span data-ttu-id="474ec-146">строка</span><span class="sxs-lookup"><span data-stu-id="474ec-146">string</span></span><br/>  | <span data-ttu-id="474ec-147">мкм</span><span class="sxs-lookup"><span data-stu-id="474ec-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="474ec-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="474ec-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="474ec-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="474ec-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




