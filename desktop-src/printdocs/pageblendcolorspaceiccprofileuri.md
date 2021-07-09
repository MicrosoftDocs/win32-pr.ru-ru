---
description: Ознакомьтесь с параметром Пажеблендколорспацеиккпрофилеури. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: пажеблендколорспацеиккпрофилеури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50db89757737ff5aa6a1358af418ee33809b960e
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549322"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="b1336-105">пажеблендколорспацеиккпрофилеури</span><span class="sxs-lookup"><span data-stu-id="b1336-105">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="b1336-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="b1336-106">This topic is not current.</span></span> <span data-ttu-id="b1336-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b1336-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b1336-108">Задает относительную ссылку URI для профиля ICC, определяющего цветовое пространство, которое должно использоваться для смешения.</span><span class="sxs-lookup"><span data-stu-id="b1336-108">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="b1336-109"><Uri>— Это абсолютное \_ имя компонента относительно корня пакета.</span><span class="sxs-lookup"><span data-stu-id="b1336-109">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="b1336-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b1336-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b1336-111">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="b1336-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="b1336-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b1336-112">Element Information</span></span>



| <span data-ttu-id="b1336-113">Имя</span><span class="sxs-lookup"><span data-stu-id="b1336-113">Name</span></span> | <span data-ttu-id="b1336-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b1336-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1336-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="b1336-115">Element Type</span></span> <br/>   | <span data-ttu-id="b1336-116">параметердеф</span><span class="sxs-lookup"><span data-stu-id="b1336-116">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="b1336-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="b1336-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b1336-118">Страница</span><span class="sxs-lookup"><span data-stu-id="b1336-118">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="b1336-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="b1336-119">Notes</span></span> <br/>          | <span data-ttu-id="b1336-120">Это относится только к документам XPS и не должен использоваться в произвольных PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="b1336-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="b1336-121">Связан с элементом Пажеблендколорспаце.</span><span class="sxs-lookup"><span data-stu-id="b1336-121">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="b1336-122">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="b1336-122">Structure Content</span></span>

<span data-ttu-id="b1336-123">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="b1336-123">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="b1336-124">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="b1336-124">Structure Properties</span></span>

<span data-ttu-id="b1336-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="b1336-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b1336-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="b1336-126">Property</span></span>                | <span data-ttu-id="b1336-127">xsi:type</span><span class="sxs-lookup"><span data-stu-id="b1336-127">xsi:type</span></span>           | <span data-ttu-id="b1336-128">Значение</span><span class="sxs-lookup"><span data-stu-id="b1336-128">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="b1336-129">DataType</span><span class="sxs-lookup"><span data-stu-id="b1336-129">DataType</span></span><br/>     | <span data-ttu-id="b1336-130">строка</span><span class="sxs-lookup"><span data-stu-id="b1336-130">string</span></span><br/>  | <span data-ttu-id="b1336-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="b1336-131">xs:string</span></span><br/>       |
| <span data-ttu-id="b1336-132">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="b1336-132">DefaultValue</span></span><br/> | <span data-ttu-id="b1336-133">строка</span><span class="sxs-lookup"><span data-stu-id="b1336-133">string</span></span><br/>  | <span data-ttu-id="b1336-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="b1336-134">undefined</span></span><br/>       |
| <span data-ttu-id="b1336-135">MaxLength</span><span class="sxs-lookup"><span data-stu-id="b1336-135">MaxLength</span></span><br/>    | <span data-ttu-id="b1336-136">Целое число</span><span class="sxs-lookup"><span data-stu-id="b1336-136">integer</span></span><br/> | <span data-ttu-id="b1336-137">неопределенный</span><span class="sxs-lookup"><span data-stu-id="b1336-137">undefined</span></span><br/>       |
| <span data-ttu-id="b1336-138">MinLength</span><span class="sxs-lookup"><span data-stu-id="b1336-138">MinLength</span></span><br/>    | <span data-ttu-id="b1336-139">целое число</span><span class="sxs-lookup"><span data-stu-id="b1336-139">integer</span></span><br/> | <span data-ttu-id="b1336-140">1</span><span class="sxs-lookup"><span data-stu-id="b1336-140">1</span></span><br/>               |
| <span data-ttu-id="b1336-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b1336-141">Mandatory</span></span><br/>    | <span data-ttu-id="b1336-142">строка</span><span class="sxs-lookup"><span data-stu-id="b1336-142">string</span></span><br/>  | <span data-ttu-id="b1336-143">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="b1336-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="b1336-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="b1336-144">UnitType</span></span><br/>     | <span data-ttu-id="b1336-145">строка</span><span class="sxs-lookup"><span data-stu-id="b1336-145">string</span></span><br/>  | <span data-ttu-id="b1336-146">characters</span><span class="sxs-lookup"><span data-stu-id="b1336-146">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="b1336-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b1336-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1336-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="b1336-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




