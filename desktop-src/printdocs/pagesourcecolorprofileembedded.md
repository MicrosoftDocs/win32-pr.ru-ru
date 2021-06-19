---
description: Сведения о параметре Пажесаурцеколорпрофилимбеддед. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 38411802-2b2e-441c-b3a6-334d87b11b5d
title: пажесаурцеколорпрофилимбеддед
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0633fa061601c1d575f174ab5572582efdf9a89e
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395639"
---
# <a name="pagesourcecolorprofileembedded"></a><span data-ttu-id="47fe0-105">пажесаурцеколорпрофилимбеддед</span><span class="sxs-lookup"><span data-stu-id="47fe0-105">PageSourceColorProfileEmbedded</span></span>

<span data-ttu-id="47fe0-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="47fe0-106">This topic is not current.</span></span> <span data-ttu-id="47fe0-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="47fe0-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="47fe0-108">Задает цветовой профиль внедренного источника.</span><span class="sxs-lookup"><span data-stu-id="47fe0-108">Specifies the embedded source color profile.</span></span>

-   [<span data-ttu-id="47fe0-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="47fe0-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="47fe0-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="47fe0-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="47fe0-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="47fe0-111">Element Information</span></span>



| <span data-ttu-id="47fe0-112">Имя</span><span class="sxs-lookup"><span data-stu-id="47fe0-112">Name</span></span> | <span data-ttu-id="47fe0-113">Значение</span><span class="sxs-lookup"><span data-stu-id="47fe0-113">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="47fe0-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="47fe0-114">Element Type</span></span> <br/>   | <span data-ttu-id="47fe0-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="47fe0-115">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="47fe0-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="47fe0-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="47fe0-117">Страница</span><span class="sxs-lookup"><span data-stu-id="47fe0-117">Page</span></span><br/>                                     |
| <span data-ttu-id="47fe0-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="47fe0-118">Notes</span></span> <br/>          | <span data-ttu-id="47fe0-119">Связано с элементом Пажесаурцеколорпрофиле</span><span class="sxs-lookup"><span data-stu-id="47fe0-119">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="47fe0-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="47fe0-120">Structure Content</span></span>

<span data-ttu-id="47fe0-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="47fe0-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageSourceColorProfileEmbedded">
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

## <a name="structure-properties"></a><span data-ttu-id="47fe0-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="47fe0-122">Structure Properties</span></span>

<span data-ttu-id="47fe0-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="47fe0-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="47fe0-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="47fe0-124">Property</span></span>                | <span data-ttu-id="47fe0-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="47fe0-125">xsi:type</span></span>           | <span data-ttu-id="47fe0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="47fe0-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="47fe0-127">DataType</span><span class="sxs-lookup"><span data-stu-id="47fe0-127">DataType</span></span><br/>     | <span data-ttu-id="47fe0-128">строка</span><span class="sxs-lookup"><span data-stu-id="47fe0-128">string</span></span><br/>  | <span data-ttu-id="47fe0-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="47fe0-129">xs:string</span></span><br/>       |
| <span data-ttu-id="47fe0-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="47fe0-130">DefaultValue</span></span><br/> | <span data-ttu-id="47fe0-131">строка</span><span class="sxs-lookup"><span data-stu-id="47fe0-131">string</span></span><br/>  | <span data-ttu-id="47fe0-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="47fe0-132">undefined</span></span><br/>       |
| <span data-ttu-id="47fe0-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="47fe0-133">MaxLength</span></span><br/>    | <span data-ttu-id="47fe0-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="47fe0-134">integer</span></span><br/> | <span data-ttu-id="47fe0-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="47fe0-135">undefined</span></span><br/>       |
| <span data-ttu-id="47fe0-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="47fe0-136">MinLength</span></span><br/>    | <span data-ttu-id="47fe0-137">целое число</span><span class="sxs-lookup"><span data-stu-id="47fe0-137">integer</span></span><br/> | <span data-ttu-id="47fe0-138">1</span><span class="sxs-lookup"><span data-stu-id="47fe0-138">1</span></span><br/>               |
| <span data-ttu-id="47fe0-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="47fe0-139">Mandatory</span></span><br/>    | <span data-ttu-id="47fe0-140">строка</span><span class="sxs-lookup"><span data-stu-id="47fe0-140">string</span></span><br/>  | <span data-ttu-id="47fe0-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="47fe0-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="47fe0-142">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="47fe0-142">UnitType</span></span><br/>     | <span data-ttu-id="47fe0-143">строка</span><span class="sxs-lookup"><span data-stu-id="47fe0-143">string</span></span><br/>  | <span data-ttu-id="47fe0-144">characters</span><span class="sxs-lookup"><span data-stu-id="47fe0-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="47fe0-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="47fe0-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47fe0-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="47fe0-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




