---
description: Получение сведений о параметре Пажемедиасиземедиасизевидс. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 22e4a6e9-4d18-4fff-873c-27ba59a79222
title: пажемедиасиземедиасизевидс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3f84e36f689d4b3c5ca060020327d78b12f7d6
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395839"
---
# <a name="pagemediasizemediasizewidth"></a><span data-ttu-id="7a702-105">пажемедиасиземедиасизевидс</span><span class="sxs-lookup"><span data-stu-id="7a702-105">PageMediaSizeMediaSizeWidth</span></span>

<span data-ttu-id="7a702-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="7a702-106">This topic is not current.</span></span> <span data-ttu-id="7a702-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7a702-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7a702-108">Задает направление Медиасизевидс измерения для настраиваемого параметра Медиасизе.</span><span class="sxs-lookup"><span data-stu-id="7a702-108">Specifies the dimension MediaSizeWidth direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="7a702-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7a702-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7a702-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="7a702-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7a702-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7a702-111">Element Information</span></span>



| <span data-ttu-id="7a702-112">Имя</span><span class="sxs-lookup"><span data-stu-id="7a702-112">Name</span></span> | <span data-ttu-id="7a702-113">Значение</span><span class="sxs-lookup"><span data-stu-id="7a702-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="7a702-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="7a702-114">Element Type</span></span> <br/>   | <span data-ttu-id="7a702-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="7a702-115">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="7a702-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="7a702-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7a702-117">Страница</span><span class="sxs-lookup"><span data-stu-id="7a702-117">Page</span></span><br/>                                           |
| <span data-ttu-id="7a702-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="7a702-118">Notes</span></span> <br/>          | <span data-ttu-id="7a702-119">Ссылка на элемент Пажемедиасизе, Пользовательский параметр</span><span class="sxs-lookup"><span data-stu-id="7a702-119">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7a702-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="7a702-120">Structure Content</span></span>

<span data-ttu-id="7a702-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="7a702-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="7a702-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="7a702-122">Structure Properties</span></span>

<span data-ttu-id="7a702-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="7a702-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7a702-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="7a702-124">Property</span></span>                | <span data-ttu-id="7a702-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7a702-125">xsi:type</span></span>           | <span data-ttu-id="7a702-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7a702-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7a702-127">DataType</span><span class="sxs-lookup"><span data-stu-id="7a702-127">DataType</span></span><br/>     | <span data-ttu-id="7a702-128">строка</span><span class="sxs-lookup"><span data-stu-id="7a702-128">string</span></span><br/>  | <span data-ttu-id="7a702-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7a702-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="7a702-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7a702-130">DefaultValue</span></span><br/> | <span data-ttu-id="7a702-131">Целое число</span><span class="sxs-lookup"><span data-stu-id="7a702-131">integer</span></span><br/> | <span data-ttu-id="7a702-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="7a702-132">undefined</span></span><br/>       |
| <span data-ttu-id="7a702-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7a702-133">MaxValue</span></span><br/>     | <span data-ttu-id="7a702-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="7a702-134">integer</span></span><br/> | <span data-ttu-id="7a702-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="7a702-135">undefined</span></span><br/>       |
| <span data-ttu-id="7a702-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="7a702-136">MinValue</span></span><br/>     | <span data-ttu-id="7a702-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="7a702-137">integer</span></span><br/> | <span data-ttu-id="7a702-138">неопределенный</span><span class="sxs-lookup"><span data-stu-id="7a702-138">undefined</span></span><br/>       |
| <span data-ttu-id="7a702-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7a702-139">Mandatory</span></span><br/>    | <span data-ttu-id="7a702-140">строка</span><span class="sxs-lookup"><span data-stu-id="7a702-140">string</span></span><br/>  | <span data-ttu-id="7a702-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="7a702-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7a702-142">Несколько</span><span class="sxs-lookup"><span data-stu-id="7a702-142">Multiple</span></span><br/>     | <span data-ttu-id="7a702-143">целое число</span><span class="sxs-lookup"><span data-stu-id="7a702-143">integer</span></span><br/> | <span data-ttu-id="7a702-144">1</span><span class="sxs-lookup"><span data-stu-id="7a702-144">1</span></span><br/>               |
| <span data-ttu-id="7a702-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="7a702-145">UnitType</span></span><br/>     | <span data-ttu-id="7a702-146">строка</span><span class="sxs-lookup"><span data-stu-id="7a702-146">string</span></span><br/>  | <span data-ttu-id="7a702-147">мкм</span><span class="sxs-lookup"><span data-stu-id="7a702-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="7a702-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="7a702-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a702-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="7a702-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




