---
description: Ознакомьтесь с параметром Пажедестинатионколорпрофилеури. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: пажедестинатионколорпрофилеури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3cf719a97f8f8086e88425c1667199815efbbb
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396679"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="704ec-105">пажедестинатионколорпрофилеури</span><span class="sxs-lookup"><span data-stu-id="704ec-105">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="704ec-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="704ec-106">This topic is not current.</span></span> <span data-ttu-id="704ec-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="704ec-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="704ec-108">Задает относительную ссылку URI для профиля ICC, содержащегося в документе XPS.</span><span class="sxs-lookup"><span data-stu-id="704ec-108">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="704ec-109">Обработка этого параметра зависит от значения функции Пажедевицеколорспацеусаже.</span><span class="sxs-lookup"><span data-stu-id="704ec-109">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="704ec-110">Предполагается, что все элементы, использующие этот профиль, уже находятся в соответствующем цветовом пространстве устройства и не будут управлять цветом в драйвере или устройстве.</span><span class="sxs-lookup"><span data-stu-id="704ec-110">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="704ec-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="704ec-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="704ec-112">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="704ec-112">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="704ec-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="704ec-113">Element Information</span></span>



| <span data-ttu-id="704ec-114">Имя</span><span class="sxs-lookup"><span data-stu-id="704ec-114">Name</span></span> | <span data-ttu-id="704ec-115">Значение</span><span class="sxs-lookup"><span data-stu-id="704ec-115">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="704ec-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="704ec-116">Element Type</span></span> <br/>   | <span data-ttu-id="704ec-117">параметердеф</span><span class="sxs-lookup"><span data-stu-id="704ec-117">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="704ec-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="704ec-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="704ec-119">Страница</span><span class="sxs-lookup"><span data-stu-id="704ec-119">Page</span></span><br/>                                          |
| <span data-ttu-id="704ec-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="704ec-120">Notes</span></span> <br/>          | <span data-ttu-id="704ec-121">Связано с элементом Пажедестинатионколорпрофиле</span><span class="sxs-lookup"><span data-stu-id="704ec-121">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="704ec-122">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="704ec-122">Structure Content</span></span>

<span data-ttu-id="704ec-123">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="704ec-123">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="704ec-124">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="704ec-124">Structure Properties</span></span>

<span data-ttu-id="704ec-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="704ec-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="704ec-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="704ec-126">Property</span></span>                | <span data-ttu-id="704ec-127">xsi:type</span><span class="sxs-lookup"><span data-stu-id="704ec-127">xsi:type</span></span>           | <span data-ttu-id="704ec-128">Значение</span><span class="sxs-lookup"><span data-stu-id="704ec-128">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="704ec-129">DataType</span><span class="sxs-lookup"><span data-stu-id="704ec-129">DataType</span></span><br/>     | <span data-ttu-id="704ec-130">строка</span><span class="sxs-lookup"><span data-stu-id="704ec-130">string</span></span><br/>  | <span data-ttu-id="704ec-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="704ec-131">xs:string</span></span><br/>       |
| <span data-ttu-id="704ec-132">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="704ec-132">DefaultValue</span></span><br/> | <span data-ttu-id="704ec-133">строка</span><span class="sxs-lookup"><span data-stu-id="704ec-133">string</span></span><br/>  | <span data-ttu-id="704ec-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="704ec-134">undefined</span></span><br/>       |
| <span data-ttu-id="704ec-135">MaxLength</span><span class="sxs-lookup"><span data-stu-id="704ec-135">MaxLength</span></span><br/>    | <span data-ttu-id="704ec-136">Целое число</span><span class="sxs-lookup"><span data-stu-id="704ec-136">integer</span></span><br/> | <span data-ttu-id="704ec-137">неопределенный</span><span class="sxs-lookup"><span data-stu-id="704ec-137">undefined</span></span><br/>       |
| <span data-ttu-id="704ec-138">MinLength</span><span class="sxs-lookup"><span data-stu-id="704ec-138">MinLength</span></span><br/>    | <span data-ttu-id="704ec-139">целое число</span><span class="sxs-lookup"><span data-stu-id="704ec-139">integer</span></span><br/> | <span data-ttu-id="704ec-140">1</span><span class="sxs-lookup"><span data-stu-id="704ec-140">1</span></span><br/>               |
| <span data-ttu-id="704ec-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="704ec-141">Mandatory</span></span><br/>    | <span data-ttu-id="704ec-142">строка</span><span class="sxs-lookup"><span data-stu-id="704ec-142">string</span></span><br/>  | <span data-ttu-id="704ec-143">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="704ec-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="704ec-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="704ec-144">UnitType</span></span><br/>     | <span data-ttu-id="704ec-145">строка</span><span class="sxs-lookup"><span data-stu-id="704ec-145">string</span></span><br/>  | <span data-ttu-id="704ec-146">characters</span><span class="sxs-lookup"><span data-stu-id="704ec-146">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="704ec-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="704ec-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="704ec-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="704ec-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




