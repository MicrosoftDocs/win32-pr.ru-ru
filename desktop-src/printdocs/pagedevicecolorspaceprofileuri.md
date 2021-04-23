---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: пажедевицеколорспацепрофилеури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4536251150851ad02abf41ca26ffaa36699281db
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703522"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="82e36-104">пажедевицеколорспацепрофилеури</span><span class="sxs-lookup"><span data-stu-id="82e36-104">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="82e36-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="82e36-105">This topic is not current.</span></span> <span data-ttu-id="82e36-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="82e36-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="82e36-107">Указывает относительный URI для корня пакета в профиль ICC, содержащийся в документе XPS.</span><span class="sxs-lookup"><span data-stu-id="82e36-107">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="82e36-108">Обработка этого параметра зависит от значения функции Пажедевицеколорспацеусаже.</span><span class="sxs-lookup"><span data-stu-id="82e36-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="82e36-109">Предполагается, что все элементы, использующие этот профиль, уже находятся в соответствующем цветовом пространстве устройства и не будут управлять цветом в драйвере или устройстве.</span><span class="sxs-lookup"><span data-stu-id="82e36-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="82e36-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="82e36-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="82e36-111">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="82e36-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="82e36-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="82e36-112">Element Information</span></span>



| <span data-ttu-id="82e36-113">Имя</span><span class="sxs-lookup"><span data-stu-id="82e36-113">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82e36-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="82e36-114">Element Type</span></span> <br/>   | <span data-ttu-id="82e36-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="82e36-115">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="82e36-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="82e36-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="82e36-117">Страница</span><span class="sxs-lookup"><span data-stu-id="82e36-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="82e36-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="82e36-118">Notes</span></span> <br/>          | <span data-ttu-id="82e36-119">Это относится только к документам XPS и не должен использоваться в произвольных PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="82e36-119">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="82e36-120">Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="82e36-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="82e36-121">Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части.</span><span class="sxs-lookup"><span data-stu-id="82e36-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="82e36-122">Эти параметры относятся к формату XPS.</span><span class="sxs-lookup"><span data-stu-id="82e36-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="82e36-123">URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="82e36-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="82e36-124">Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="82e36-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="82e36-125">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="82e36-125">Structure Content</span></span>

<span data-ttu-id="82e36-126">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="82e36-126">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDeviceColorSpaceProfileURI">
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

## <a name="structure-properties"></a><span data-ttu-id="82e36-127">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="82e36-127">Structure Properties</span></span>

<span data-ttu-id="82e36-128">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="82e36-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="82e36-129">Свойство</span><span class="sxs-lookup"><span data-stu-id="82e36-129">Property</span></span>                | <span data-ttu-id="82e36-130">xsi:type</span><span class="sxs-lookup"><span data-stu-id="82e36-130">xsi:type</span></span>           | <span data-ttu-id="82e36-131">Значение</span><span class="sxs-lookup"><span data-stu-id="82e36-131">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="82e36-132">DataType</span><span class="sxs-lookup"><span data-stu-id="82e36-132">DataType</span></span><br/>     | <span data-ttu-id="82e36-133">строка</span><span class="sxs-lookup"><span data-stu-id="82e36-133">string</span></span><br/>  | <span data-ttu-id="82e36-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="82e36-134">xs:string</span></span><br/>       |
| <span data-ttu-id="82e36-135">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="82e36-135">DefaultValue</span></span><br/> | <span data-ttu-id="82e36-136">строка</span><span class="sxs-lookup"><span data-stu-id="82e36-136">string</span></span><br/>  | <span data-ttu-id="82e36-137">неопределенный</span><span class="sxs-lookup"><span data-stu-id="82e36-137">undefined</span></span><br/>       |
| <span data-ttu-id="82e36-138">MaxLength</span><span class="sxs-lookup"><span data-stu-id="82e36-138">MaxLength</span></span><br/>    | <span data-ttu-id="82e36-139">Целое число</span><span class="sxs-lookup"><span data-stu-id="82e36-139">integer</span></span><br/> | <span data-ttu-id="82e36-140">неопределенный</span><span class="sxs-lookup"><span data-stu-id="82e36-140">undefined</span></span><br/>       |
| <span data-ttu-id="82e36-141">MinLength</span><span class="sxs-lookup"><span data-stu-id="82e36-141">MinLength</span></span><br/>    | <span data-ttu-id="82e36-142">целое число</span><span class="sxs-lookup"><span data-stu-id="82e36-142">integer</span></span><br/> | <span data-ttu-id="82e36-143">1</span><span class="sxs-lookup"><span data-stu-id="82e36-143">1</span></span><br/>               |
| <span data-ttu-id="82e36-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="82e36-144">Mandatory</span></span><br/>    | <span data-ttu-id="82e36-145">строка</span><span class="sxs-lookup"><span data-stu-id="82e36-145">string</span></span><br/>  | <span data-ttu-id="82e36-146">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="82e36-146">psk:Conditional</span></span><br/> |
| <span data-ttu-id="82e36-147">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="82e36-147">UnitType</span></span><br/>     | <span data-ttu-id="82e36-148">строка</span><span class="sxs-lookup"><span data-stu-id="82e36-148">string</span></span><br/>  | <span data-ttu-id="82e36-149">characters</span><span class="sxs-lookup"><span data-stu-id="82e36-149">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="82e36-150">См. также</span><span class="sxs-lookup"><span data-stu-id="82e36-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82e36-151">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="82e36-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




