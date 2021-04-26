---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 22e4a6e9-4d18-4fff-873c-27ba59a79222
title: пажемедиасиземедиасизевидс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50df088fd25a69ee566e1406d3f1b833aa6131f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997571"
---
# <a name="pagemediasizemediasizewidth"></a><span data-ttu-id="325c7-104">пажемедиасиземедиасизевидс</span><span class="sxs-lookup"><span data-stu-id="325c7-104">PageMediaSizeMediaSizeWidth</span></span>

<span data-ttu-id="325c7-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="325c7-105">This topic is not current.</span></span> <span data-ttu-id="325c7-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="325c7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="325c7-107">Задает направление Медиасизевидс измерения для настраиваемого параметра Медиасизе.</span><span class="sxs-lookup"><span data-stu-id="325c7-107">Specifies the dimension MediaSizeWidth direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="325c7-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="325c7-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="325c7-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="325c7-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="325c7-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="325c7-110">Element Information</span></span>



| <span data-ttu-id="325c7-111">Имя</span><span class="sxs-lookup"><span data-stu-id="325c7-111">Name</span></span> | <span data-ttu-id="325c7-112">Значение</span><span class="sxs-lookup"><span data-stu-id="325c7-112">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="325c7-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="325c7-113">Element Type</span></span> <br/>   | <span data-ttu-id="325c7-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="325c7-114">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="325c7-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="325c7-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="325c7-116">Страница</span><span class="sxs-lookup"><span data-stu-id="325c7-116">Page</span></span><br/>                                           |
| <span data-ttu-id="325c7-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="325c7-117">Notes</span></span> <br/>          | <span data-ttu-id="325c7-118">Ссылка на элемент Пажемедиасизе, Пользовательский параметр</span><span class="sxs-lookup"><span data-stu-id="325c7-118">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="325c7-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="325c7-119">Structure Content</span></span>

<span data-ttu-id="325c7-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="325c7-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="325c7-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="325c7-121">Structure Properties</span></span>

<span data-ttu-id="325c7-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="325c7-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="325c7-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="325c7-123">Property</span></span>                | <span data-ttu-id="325c7-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="325c7-124">xsi:type</span></span>           | <span data-ttu-id="325c7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="325c7-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="325c7-126">DataType</span><span class="sxs-lookup"><span data-stu-id="325c7-126">DataType</span></span><br/>     | <span data-ttu-id="325c7-127">строка</span><span class="sxs-lookup"><span data-stu-id="325c7-127">string</span></span><br/>  | <span data-ttu-id="325c7-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="325c7-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="325c7-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="325c7-129">DefaultValue</span></span><br/> | <span data-ttu-id="325c7-130">Целое число</span><span class="sxs-lookup"><span data-stu-id="325c7-130">integer</span></span><br/> | <span data-ttu-id="325c7-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="325c7-131">undefined</span></span><br/>       |
| <span data-ttu-id="325c7-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="325c7-132">MaxValue</span></span><br/>     | <span data-ttu-id="325c7-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="325c7-133">integer</span></span><br/> | <span data-ttu-id="325c7-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="325c7-134">undefined</span></span><br/>       |
| <span data-ttu-id="325c7-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="325c7-135">MinValue</span></span><br/>     | <span data-ttu-id="325c7-136">Целое число</span><span class="sxs-lookup"><span data-stu-id="325c7-136">integer</span></span><br/> | <span data-ttu-id="325c7-137">неопределенный</span><span class="sxs-lookup"><span data-stu-id="325c7-137">undefined</span></span><br/>       |
| <span data-ttu-id="325c7-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="325c7-138">Mandatory</span></span><br/>    | <span data-ttu-id="325c7-139">строка</span><span class="sxs-lookup"><span data-stu-id="325c7-139">string</span></span><br/>  | <span data-ttu-id="325c7-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="325c7-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="325c7-141">Несколько</span><span class="sxs-lookup"><span data-stu-id="325c7-141">Multiple</span></span><br/>     | <span data-ttu-id="325c7-142">целое число</span><span class="sxs-lookup"><span data-stu-id="325c7-142">integer</span></span><br/> | <span data-ttu-id="325c7-143">1</span><span class="sxs-lookup"><span data-stu-id="325c7-143">1</span></span><br/>               |
| <span data-ttu-id="325c7-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="325c7-144">UnitType</span></span><br/>     | <span data-ttu-id="325c7-145">строка</span><span class="sxs-lookup"><span data-stu-id="325c7-145">string</span></span><br/>  | <span data-ttu-id="325c7-146">мкм</span><span class="sxs-lookup"><span data-stu-id="325c7-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="325c7-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="325c7-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="325c7-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="325c7-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




