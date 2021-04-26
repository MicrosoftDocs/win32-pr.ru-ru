---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: пажеблендколорспацеиккпрофилеури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbf1233e172a81053baee0abe1e21d79064045a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997701"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="50236-104">пажеблендколорспацеиккпрофилеури</span><span class="sxs-lookup"><span data-stu-id="50236-104">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="50236-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="50236-105">This topic is not current.</span></span> <span data-ttu-id="50236-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="50236-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="50236-107">Задает относительную ссылку URI для профиля ICC, определяющего цветовое пространство, которое должно использоваться для смешения.</span><span class="sxs-lookup"><span data-stu-id="50236-107">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="50236-108"><Uri>— Это абсолютное \_ имя компонента относительно корня пакета.</span><span class="sxs-lookup"><span data-stu-id="50236-108">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="50236-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="50236-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="50236-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="50236-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="50236-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="50236-111">Element Information</span></span>



| <span data-ttu-id="50236-112">Имя</span><span class="sxs-lookup"><span data-stu-id="50236-112">Name</span></span> | <span data-ttu-id="50236-113">Значение</span><span class="sxs-lookup"><span data-stu-id="50236-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50236-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="50236-114">Element Type</span></span> <br/>   | <span data-ttu-id="50236-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="50236-115">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="50236-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="50236-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="50236-117">Страница</span><span class="sxs-lookup"><span data-stu-id="50236-117">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="50236-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="50236-118">Notes</span></span> <br/>          | <span data-ttu-id="50236-119">Это относится только к документам XPS и не должен использоваться в произвольных PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="50236-119">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="50236-120">Связан с элементом Пажеблендколорспаце.</span><span class="sxs-lookup"><span data-stu-id="50236-120">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="50236-121">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="50236-121">Structure Content</span></span>

<span data-ttu-id="50236-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="50236-122">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="50236-123">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="50236-123">Structure Properties</span></span>

<span data-ttu-id="50236-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="50236-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="50236-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="50236-125">Property</span></span>                | <span data-ttu-id="50236-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="50236-126">xsi:type</span></span>           | <span data-ttu-id="50236-127">Значение</span><span class="sxs-lookup"><span data-stu-id="50236-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="50236-128">DataType</span><span class="sxs-lookup"><span data-stu-id="50236-128">DataType</span></span><br/>     | <span data-ttu-id="50236-129">строка</span><span class="sxs-lookup"><span data-stu-id="50236-129">string</span></span><br/>  | <span data-ttu-id="50236-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="50236-130">xs:string</span></span><br/>       |
| <span data-ttu-id="50236-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="50236-131">DefaultValue</span></span><br/> | <span data-ttu-id="50236-132">строка</span><span class="sxs-lookup"><span data-stu-id="50236-132">string</span></span><br/>  | <span data-ttu-id="50236-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="50236-133">undefined</span></span><br/>       |
| <span data-ttu-id="50236-134">MaxLength</span><span class="sxs-lookup"><span data-stu-id="50236-134">MaxLength</span></span><br/>    | <span data-ttu-id="50236-135">Целое число</span><span class="sxs-lookup"><span data-stu-id="50236-135">integer</span></span><br/> | <span data-ttu-id="50236-136">неопределенный</span><span class="sxs-lookup"><span data-stu-id="50236-136">undefined</span></span><br/>       |
| <span data-ttu-id="50236-137">MinLength</span><span class="sxs-lookup"><span data-stu-id="50236-137">MinLength</span></span><br/>    | <span data-ttu-id="50236-138">целое число</span><span class="sxs-lookup"><span data-stu-id="50236-138">integer</span></span><br/> | <span data-ttu-id="50236-139">1</span><span class="sxs-lookup"><span data-stu-id="50236-139">1</span></span><br/>               |
| <span data-ttu-id="50236-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="50236-140">Mandatory</span></span><br/>    | <span data-ttu-id="50236-141">строка</span><span class="sxs-lookup"><span data-stu-id="50236-141">string</span></span><br/>  | <span data-ttu-id="50236-142">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="50236-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="50236-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="50236-143">UnitType</span></span><br/>     | <span data-ttu-id="50236-144">строка</span><span class="sxs-lookup"><span data-stu-id="50236-144">string</span></span><br/>  | <span data-ttu-id="50236-145">characters</span><span class="sxs-lookup"><span data-stu-id="50236-145">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="50236-146">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="50236-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50236-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="50236-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




