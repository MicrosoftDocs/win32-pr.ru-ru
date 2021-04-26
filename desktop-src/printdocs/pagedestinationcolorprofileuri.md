---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: пажедестинатионколорпрофилеури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b321cba1608b1098dcc91f3800ef11f4968fb3f2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996101"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="cee22-104">пажедестинатионколорпрофилеури</span><span class="sxs-lookup"><span data-stu-id="cee22-104">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="cee22-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="cee22-105">This topic is not current.</span></span> <span data-ttu-id="cee22-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cee22-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cee22-107">Задает относительную ссылку URI для профиля ICC, содержащегося в документе XPS.</span><span class="sxs-lookup"><span data-stu-id="cee22-107">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="cee22-108">Обработка этого параметра зависит от значения функции Пажедевицеколорспацеусаже.</span><span class="sxs-lookup"><span data-stu-id="cee22-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="cee22-109">Предполагается, что все элементы, использующие этот профиль, уже находятся в соответствующем цветовом пространстве устройства и не будут управлять цветом в драйвере или устройстве.</span><span class="sxs-lookup"><span data-stu-id="cee22-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="cee22-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="cee22-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cee22-111">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="cee22-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="cee22-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="cee22-112">Element Information</span></span>



| <span data-ttu-id="cee22-113">Имя</span><span class="sxs-lookup"><span data-stu-id="cee22-113">Name</span></span> | <span data-ttu-id="cee22-114">Значение</span><span class="sxs-lookup"><span data-stu-id="cee22-114">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="cee22-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="cee22-115">Element Type</span></span> <br/>   | <span data-ttu-id="cee22-116">параметердеф</span><span class="sxs-lookup"><span data-stu-id="cee22-116">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="cee22-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="cee22-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cee22-118">Страница</span><span class="sxs-lookup"><span data-stu-id="cee22-118">Page</span></span><br/>                                          |
| <span data-ttu-id="cee22-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="cee22-119">Notes</span></span> <br/>          | <span data-ttu-id="cee22-120">Связано с элементом Пажедестинатионколорпрофиле</span><span class="sxs-lookup"><span data-stu-id="cee22-120">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="cee22-121">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="cee22-121">Structure Content</span></span>

<span data-ttu-id="cee22-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="cee22-122">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="cee22-123">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="cee22-123">Structure Properties</span></span>

<span data-ttu-id="cee22-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="cee22-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cee22-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="cee22-125">Property</span></span>                | <span data-ttu-id="cee22-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="cee22-126">xsi:type</span></span>           | <span data-ttu-id="cee22-127">Значение</span><span class="sxs-lookup"><span data-stu-id="cee22-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="cee22-128">DataType</span><span class="sxs-lookup"><span data-stu-id="cee22-128">DataType</span></span><br/>     | <span data-ttu-id="cee22-129">строка</span><span class="sxs-lookup"><span data-stu-id="cee22-129">string</span></span><br/>  | <span data-ttu-id="cee22-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="cee22-130">xs:string</span></span><br/>       |
| <span data-ttu-id="cee22-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="cee22-131">DefaultValue</span></span><br/> | <span data-ttu-id="cee22-132">строка</span><span class="sxs-lookup"><span data-stu-id="cee22-132">string</span></span><br/>  | <span data-ttu-id="cee22-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="cee22-133">undefined</span></span><br/>       |
| <span data-ttu-id="cee22-134">MaxLength</span><span class="sxs-lookup"><span data-stu-id="cee22-134">MaxLength</span></span><br/>    | <span data-ttu-id="cee22-135">Целое число</span><span class="sxs-lookup"><span data-stu-id="cee22-135">integer</span></span><br/> | <span data-ttu-id="cee22-136">неопределенный</span><span class="sxs-lookup"><span data-stu-id="cee22-136">undefined</span></span><br/>       |
| <span data-ttu-id="cee22-137">MinLength</span><span class="sxs-lookup"><span data-stu-id="cee22-137">MinLength</span></span><br/>    | <span data-ttu-id="cee22-138">целое число</span><span class="sxs-lookup"><span data-stu-id="cee22-138">integer</span></span><br/> | <span data-ttu-id="cee22-139">1</span><span class="sxs-lookup"><span data-stu-id="cee22-139">1</span></span><br/>               |
| <span data-ttu-id="cee22-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cee22-140">Mandatory</span></span><br/>    | <span data-ttu-id="cee22-141">строка</span><span class="sxs-lookup"><span data-stu-id="cee22-141">string</span></span><br/>  | <span data-ttu-id="cee22-142">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="cee22-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="cee22-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="cee22-143">UnitType</span></span><br/>     | <span data-ttu-id="cee22-144">строка</span><span class="sxs-lookup"><span data-stu-id="cee22-144">string</span></span><br/>  | <span data-ttu-id="cee22-145">characters</span><span class="sxs-lookup"><span data-stu-id="cee22-145">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="cee22-146">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="cee22-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cee22-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="cee22-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




