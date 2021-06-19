---
description: Получение сведений о параметре Пажесаурцеколорпрофилеури. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 25c3c70f-20e3-4e44-9c59-bb66b4bd14d9
title: пажесаурцеколорпрофилеури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7b6acd064a6b0652720a6c0d783f10a7467fa16
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395629"
---
# <a name="pagesourcecolorprofileuri"></a><span data-ttu-id="93f25-105">пажесаурцеколорпрофилеури</span><span class="sxs-lookup"><span data-stu-id="93f25-105">PageSourceColorProfileURI</span></span>

<span data-ttu-id="93f25-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="93f25-106">This topic is not current.</span></span> <span data-ttu-id="93f25-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="93f25-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="93f25-108">Указывает источник для цветового профиля.</span><span class="sxs-lookup"><span data-stu-id="93f25-108">Specifies the source for color profile.</span></span>

-   [<span data-ttu-id="93f25-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="93f25-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="93f25-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="93f25-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="93f25-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="93f25-111">Element Information</span></span>



| <span data-ttu-id="93f25-112">Имя</span><span class="sxs-lookup"><span data-stu-id="93f25-112">Name</span></span> | <span data-ttu-id="93f25-113">Значение</span><span class="sxs-lookup"><span data-stu-id="93f25-113">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="93f25-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="93f25-114">Element Type</span></span> <br/>   | <span data-ttu-id="93f25-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="93f25-115">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="93f25-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="93f25-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="93f25-117">Страница</span><span class="sxs-lookup"><span data-stu-id="93f25-117">Page</span></span><br/>                                     |
| <span data-ttu-id="93f25-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="93f25-118">Notes</span></span> <br/>          | <span data-ttu-id="93f25-119">Связано с элементом Пажесаурцеколорпрофиле</span><span class="sxs-lookup"><span data-stu-id="93f25-119">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="93f25-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="93f25-120">Structure Content</span></span>

<span data-ttu-id="93f25-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="93f25-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageSourceColorProfileURI">
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

## <a name="structure-properties"></a><span data-ttu-id="93f25-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="93f25-122">Structure Properties</span></span>

<span data-ttu-id="93f25-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="93f25-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="93f25-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="93f25-124">Property</span></span>                | <span data-ttu-id="93f25-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="93f25-125">xsi:type</span></span>           | <span data-ttu-id="93f25-126">Значение</span><span class="sxs-lookup"><span data-stu-id="93f25-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="93f25-127">DataType</span><span class="sxs-lookup"><span data-stu-id="93f25-127">DataType</span></span><br/>     | <span data-ttu-id="93f25-128">строка</span><span class="sxs-lookup"><span data-stu-id="93f25-128">string</span></span><br/>  | <span data-ttu-id="93f25-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="93f25-129">xs:string</span></span><br/>       |
| <span data-ttu-id="93f25-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="93f25-130">DefaultValue</span></span><br/> | <span data-ttu-id="93f25-131">строка</span><span class="sxs-lookup"><span data-stu-id="93f25-131">string</span></span><br/>  | <span data-ttu-id="93f25-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="93f25-132">undefined</span></span><br/>       |
| <span data-ttu-id="93f25-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="93f25-133">MaxLength</span></span><br/>    | <span data-ttu-id="93f25-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="93f25-134">integer</span></span><br/> | <span data-ttu-id="93f25-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="93f25-135">undefined</span></span><br/>       |
| <span data-ttu-id="93f25-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="93f25-136">MinLength</span></span><br/>    | <span data-ttu-id="93f25-137">целое число</span><span class="sxs-lookup"><span data-stu-id="93f25-137">integer</span></span><br/> | <span data-ttu-id="93f25-138">1</span><span class="sxs-lookup"><span data-stu-id="93f25-138">1</span></span><br/>               |
| <span data-ttu-id="93f25-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="93f25-139">Mandatory</span></span><br/>    | <span data-ttu-id="93f25-140">строка</span><span class="sxs-lookup"><span data-stu-id="93f25-140">string</span></span><br/>  | <span data-ttu-id="93f25-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="93f25-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="93f25-142">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="93f25-142">UnitType</span></span><br/>     | <span data-ttu-id="93f25-143">строка</span><span class="sxs-lookup"><span data-stu-id="93f25-143">string</span></span><br/>  | <span data-ttu-id="93f25-144">characters</span><span class="sxs-lookup"><span data-stu-id="93f25-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="93f25-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="93f25-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93f25-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="93f25-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




