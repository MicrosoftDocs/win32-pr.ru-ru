---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: пажедестинатионколорпрофилеури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fff2ca269eaed9331f6c2077e6b396cca5a01c4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703533"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="848e6-104">пажедестинатионколорпрофилеури</span><span class="sxs-lookup"><span data-stu-id="848e6-104">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="848e6-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="848e6-105">This topic is not current.</span></span> <span data-ttu-id="848e6-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="848e6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="848e6-107">Задает относительную ссылку URI для профиля ICC, содержащегося в документе XPS.</span><span class="sxs-lookup"><span data-stu-id="848e6-107">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="848e6-108">Обработка этого параметра зависит от значения функции Пажедевицеколорспацеусаже.</span><span class="sxs-lookup"><span data-stu-id="848e6-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="848e6-109">Предполагается, что все элементы, использующие этот профиль, уже находятся в соответствующем цветовом пространстве устройства и не будут управлять цветом в драйвере или устройстве.</span><span class="sxs-lookup"><span data-stu-id="848e6-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="848e6-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="848e6-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="848e6-111">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="848e6-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="848e6-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="848e6-112">Element Information</span></span>



| <span data-ttu-id="848e6-113">Имя</span><span class="sxs-lookup"><span data-stu-id="848e6-113">Name</span></span>                       |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="848e6-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="848e6-114">Element Type</span></span> <br/>   | <span data-ttu-id="848e6-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="848e6-115">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="848e6-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="848e6-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="848e6-117">Страница</span><span class="sxs-lookup"><span data-stu-id="848e6-117">Page</span></span><br/>                                          |
| <span data-ttu-id="848e6-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="848e6-118">Notes</span></span> <br/>          | <span data-ttu-id="848e6-119">Связано с элементом Пажедестинатионколорпрофиле</span><span class="sxs-lookup"><span data-stu-id="848e6-119">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="848e6-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="848e6-120">Structure Content</span></span>

<span data-ttu-id="848e6-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="848e6-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileURI">
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

## <a name="structure-properties"></a><span data-ttu-id="848e6-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="848e6-122">Structure Properties</span></span>

<span data-ttu-id="848e6-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="848e6-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="848e6-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="848e6-124">Property</span></span>                | <span data-ttu-id="848e6-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="848e6-125">xsi:type</span></span>           | <span data-ttu-id="848e6-126">Значение</span><span class="sxs-lookup"><span data-stu-id="848e6-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="848e6-127">DataType</span><span class="sxs-lookup"><span data-stu-id="848e6-127">DataType</span></span><br/>     | <span data-ttu-id="848e6-128">строка</span><span class="sxs-lookup"><span data-stu-id="848e6-128">string</span></span><br/>  | <span data-ttu-id="848e6-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="848e6-129">xs:string</span></span><br/>       |
| <span data-ttu-id="848e6-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="848e6-130">DefaultValue</span></span><br/> | <span data-ttu-id="848e6-131">строка</span><span class="sxs-lookup"><span data-stu-id="848e6-131">string</span></span><br/>  | <span data-ttu-id="848e6-132">неопределенный</span><span class="sxs-lookup"><span data-stu-id="848e6-132">undefined</span></span><br/>       |
| <span data-ttu-id="848e6-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="848e6-133">MaxLength</span></span><br/>    | <span data-ttu-id="848e6-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="848e6-134">integer</span></span><br/> | <span data-ttu-id="848e6-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="848e6-135">undefined</span></span><br/>       |
| <span data-ttu-id="848e6-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="848e6-136">MinLength</span></span><br/>    | <span data-ttu-id="848e6-137">целое число</span><span class="sxs-lookup"><span data-stu-id="848e6-137">integer</span></span><br/> | <span data-ttu-id="848e6-138">1</span><span class="sxs-lookup"><span data-stu-id="848e6-138">1</span></span><br/>               |
| <span data-ttu-id="848e6-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="848e6-139">Mandatory</span></span><br/>    | <span data-ttu-id="848e6-140">строка</span><span class="sxs-lookup"><span data-stu-id="848e6-140">string</span></span><br/>  | <span data-ttu-id="848e6-141">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="848e6-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="848e6-142">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="848e6-142">UnitType</span></span><br/>     | <span data-ttu-id="848e6-143">строка</span><span class="sxs-lookup"><span data-stu-id="848e6-143">string</span></span><br/>  | <span data-ttu-id="848e6-144">characters</span><span class="sxs-lookup"><span data-stu-id="848e6-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="848e6-145">См. также</span><span class="sxs-lookup"><span data-stu-id="848e6-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="848e6-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="848e6-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




