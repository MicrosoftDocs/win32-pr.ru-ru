---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: пажеблендколорспацеиккпрофилеури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f3a6143bd934ebcb75c3e5455a30c7365f1a89
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104081749"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="89035-104">пажеблендколорспацеиккпрофилеури</span><span class="sxs-lookup"><span data-stu-id="89035-104">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="89035-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="89035-105">This topic is not current.</span></span> <span data-ttu-id="89035-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="89035-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="89035-107">Задает относительную ссылку URI для профиля ICC, определяющего цветовое пространство, которое должно использоваться для смешения.</span><span class="sxs-lookup"><span data-stu-id="89035-107">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="89035-108"><Uri>— Это абсолютное \_ имя компонента относительно корня пакета.</span><span class="sxs-lookup"><span data-stu-id="89035-108">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="89035-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="89035-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="89035-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="89035-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="89035-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="89035-111">Element Information</span></span>



| <span data-ttu-id="89035-112">Имя</span><span class="sxs-lookup"><span data-stu-id="89035-112">Name</span></span>                       |                                                                                                                                        |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89035-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="89035-113">Element Type</span></span> <br/>   | <span data-ttu-id="89035-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="89035-114">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="89035-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="89035-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="89035-116">Страница</span><span class="sxs-lookup"><span data-stu-id="89035-116">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="89035-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="89035-117">Notes</span></span> <br/>          | <span data-ttu-id="89035-118">Это относится только к документам XPS и не должен использоваться в произвольных PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="89035-118">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="89035-119">Связан с элементом Пажеблендколорспаце.</span><span class="sxs-lookup"><span data-stu-id="89035-119">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="89035-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="89035-120">Structure Content</span></span>

<span data-ttu-id="89035-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="89035-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlendColorSpaceICCProfileURI">
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

## <a name="structure-properties"></a><span data-ttu-id="89035-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="89035-122">Structure Properties</span></span>

<span data-ttu-id="89035-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="89035-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="89035-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="89035-124">Property</span></span>                | <span data-ttu-id="89035-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="89035-125">xsi:type</span></span>           | <span data-ttu-id="89035-126">Значение</span><span class="sxs-lookup"><span data-stu-id="89035-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="89035-127">DataType</span><span class="sxs-lookup"><span data-stu-id="89035-127">DataType</span></span><br/>     | <span data-ttu-id="89035-128">строка</span><span class="sxs-lookup"><span data-stu-id="89035-128">string</span></span><br/>  | <span data-ttu-id="89035-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="89035-129">xs:string</span></span><br/>       |
| <span data-ttu-id="89035-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="89035-130">DefaultValue</span></span><br/> | <span data-ttu-id="89035-131">строка</span><span class="sxs-lookup"><span data-stu-id="89035-131">string</span></span><br/>  | <span data-ttu-id="89035-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="89035-132">undefined</span></span><br/>       |
| <span data-ttu-id="89035-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="89035-133">MaxLength</span></span><br/>    | <span data-ttu-id="89035-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="89035-134">integer</span></span><br/> | <span data-ttu-id="89035-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="89035-135">undefined</span></span><br/>       |
| <span data-ttu-id="89035-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="89035-136">MinLength</span></span><br/>    | <span data-ttu-id="89035-137">целое число</span><span class="sxs-lookup"><span data-stu-id="89035-137">integer</span></span><br/> | <span data-ttu-id="89035-138">1</span><span class="sxs-lookup"><span data-stu-id="89035-138">1</span></span><br/>               |
| <span data-ttu-id="89035-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="89035-139">Mandatory</span></span><br/>    | <span data-ttu-id="89035-140">строка</span><span class="sxs-lookup"><span data-stu-id="89035-140">string</span></span><br/>  | <span data-ttu-id="89035-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="89035-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="89035-142">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="89035-142">UnitType</span></span><br/>     | <span data-ttu-id="89035-143">строка</span><span class="sxs-lookup"><span data-stu-id="89035-143">string</span></span><br/>  | <span data-ttu-id="89035-144">characters</span><span class="sxs-lookup"><span data-stu-id="89035-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="89035-145">См. также</span><span class="sxs-lookup"><span data-stu-id="89035-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89035-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="89035-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




