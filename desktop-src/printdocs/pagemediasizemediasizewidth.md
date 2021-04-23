---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 22e4a6e9-4d18-4fff-873c-27ba59a79222
title: пажемедиасиземедиасизевидс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1f72e667f3de3bce86beb1c65c5fde4ebc8669
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351785"
---
# <a name="pagemediasizemediasizewidth"></a><span data-ttu-id="056fe-104">пажемедиасиземедиасизевидс</span><span class="sxs-lookup"><span data-stu-id="056fe-104">PageMediaSizeMediaSizeWidth</span></span>

<span data-ttu-id="056fe-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="056fe-105">This topic is not current.</span></span> <span data-ttu-id="056fe-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="056fe-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="056fe-107">Задает направление Медиасизевидс измерения для настраиваемого параметра Медиасизе.</span><span class="sxs-lookup"><span data-stu-id="056fe-107">Specifies the dimension MediaSizeWidth direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="056fe-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="056fe-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="056fe-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="056fe-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="056fe-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="056fe-110">Element Information</span></span>



| <span data-ttu-id="056fe-111">Имя</span><span class="sxs-lookup"><span data-stu-id="056fe-111">Name</span></span>                       |                                                           |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="056fe-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="056fe-112">Element Type</span></span> <br/>   | <span data-ttu-id="056fe-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="056fe-113">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="056fe-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="056fe-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="056fe-115">Страница</span><span class="sxs-lookup"><span data-stu-id="056fe-115">Page</span></span><br/>                                           |
| <span data-ttu-id="056fe-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="056fe-116">Notes</span></span> <br/>          | <span data-ttu-id="056fe-117">Ссылка на элемент Пажемедиасизе, Пользовательский параметр</span><span class="sxs-lookup"><span data-stu-id="056fe-117">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="056fe-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="056fe-118">Structure Content</span></span>

<span data-ttu-id="056fe-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="056fe-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="056fe-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="056fe-120">Structure Properties</span></span>

<span data-ttu-id="056fe-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="056fe-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="056fe-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="056fe-122">Property</span></span>                | <span data-ttu-id="056fe-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="056fe-123">xsi:type</span></span>           | <span data-ttu-id="056fe-124">Значение</span><span class="sxs-lookup"><span data-stu-id="056fe-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="056fe-125">DataType</span><span class="sxs-lookup"><span data-stu-id="056fe-125">DataType</span></span><br/>     | <span data-ttu-id="056fe-126">строка</span><span class="sxs-lookup"><span data-stu-id="056fe-126">string</span></span><br/>  | <span data-ttu-id="056fe-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="056fe-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="056fe-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="056fe-128">DefaultValue</span></span><br/> | <span data-ttu-id="056fe-129">Целое число</span><span class="sxs-lookup"><span data-stu-id="056fe-129">integer</span></span><br/> | <span data-ttu-id="056fe-130">неопределенный</span><span class="sxs-lookup"><span data-stu-id="056fe-130">undefined</span></span><br/>       |
| <span data-ttu-id="056fe-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="056fe-131">MaxValue</span></span><br/>     | <span data-ttu-id="056fe-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="056fe-132">integer</span></span><br/> | <span data-ttu-id="056fe-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="056fe-133">undefined</span></span><br/>       |
| <span data-ttu-id="056fe-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="056fe-134">MinValue</span></span><br/>     | <span data-ttu-id="056fe-135">Целое число</span><span class="sxs-lookup"><span data-stu-id="056fe-135">integer</span></span><br/> | <span data-ttu-id="056fe-136">неопределенный</span><span class="sxs-lookup"><span data-stu-id="056fe-136">undefined</span></span><br/>       |
| <span data-ttu-id="056fe-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="056fe-137">Mandatory</span></span><br/>    | <span data-ttu-id="056fe-138">строка</span><span class="sxs-lookup"><span data-stu-id="056fe-138">string</span></span><br/>  | <span data-ttu-id="056fe-139">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="056fe-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="056fe-140">Несколько</span><span class="sxs-lookup"><span data-stu-id="056fe-140">Multiple</span></span><br/>     | <span data-ttu-id="056fe-141">целое число</span><span class="sxs-lookup"><span data-stu-id="056fe-141">integer</span></span><br/> | <span data-ttu-id="056fe-142">1</span><span class="sxs-lookup"><span data-stu-id="056fe-142">1</span></span><br/>               |
| <span data-ttu-id="056fe-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="056fe-143">UnitType</span></span><br/>     | <span data-ttu-id="056fe-144">строка</span><span class="sxs-lookup"><span data-stu-id="056fe-144">string</span></span><br/>  | <span data-ttu-id="056fe-145">мкм</span><span class="sxs-lookup"><span data-stu-id="056fe-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="056fe-146">См. также</span><span class="sxs-lookup"><span data-stu-id="056fe-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="056fe-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="056fe-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




