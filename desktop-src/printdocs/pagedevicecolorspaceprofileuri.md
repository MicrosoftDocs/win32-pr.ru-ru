---
description: Ознакомьтесь с параметром Пажедевицеколорспацепрофилеури. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: пажедевицеколорспацепрофилеури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21420dec2e3057de903b1e04c55a7c6d234343b0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396649"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="8e2e2-105">пажедевицеколорспацепрофилеури</span><span class="sxs-lookup"><span data-stu-id="8e2e2-105">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="8e2e2-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="8e2e2-106">This topic is not current.</span></span> <span data-ttu-id="8e2e2-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8e2e2-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8e2e2-108">Указывает относительный URI для корня пакета в профиль ICC, содержащийся в документе XPS.</span><span class="sxs-lookup"><span data-stu-id="8e2e2-108">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="8e2e2-109">Обработка этого параметра зависит от значения функции Пажедевицеколорспацеусаже.</span><span class="sxs-lookup"><span data-stu-id="8e2e2-109">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="8e2e2-110">Предполагается, что все элементы, использующие этот профиль, уже находятся в соответствующем цветовом пространстве устройства и не будут управлять цветом в драйвере или устройстве.</span><span class="sxs-lookup"><span data-stu-id="8e2e2-110">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="8e2e2-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8e2e2-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8e2e2-112">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="8e2e2-112">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8e2e2-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8e2e2-113">Element Information</span></span>



| <span data-ttu-id="8e2e2-114">Имя</span><span class="sxs-lookup"><span data-stu-id="8e2e2-114">Name</span></span> | <span data-ttu-id="8e2e2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8e2e2-115">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e2e2-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="8e2e2-116">Element Type</span></span> <br/>   | <span data-ttu-id="8e2e2-117">параметердеф</span><span class="sxs-lookup"><span data-stu-id="8e2e2-117">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="8e2e2-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="8e2e2-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8e2e2-119">Страница</span><span class="sxs-lookup"><span data-stu-id="8e2e2-119">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="8e2e2-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="8e2e2-120">Notes</span></span> <br/>          | <span data-ttu-id="8e2e2-121">Это относится только к документам XPS и не должен использоваться в произвольных PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="8e2e2-121">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="8e2e2-122">Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="8e2e2-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="8e2e2-123">Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части.</span><span class="sxs-lookup"><span data-stu-id="8e2e2-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="8e2e2-124">Эти параметры относятся к формату XPS.</span><span class="sxs-lookup"><span data-stu-id="8e2e2-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="8e2e2-125">URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="8e2e2-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="8e2e2-126">Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8e2e2-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="8e2e2-127">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="8e2e2-127">Structure Content</span></span>

<span data-ttu-id="8e2e2-128">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="8e2e2-128">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="8e2e2-129">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="8e2e2-129">Structure Properties</span></span>

<span data-ttu-id="8e2e2-130">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="8e2e2-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8e2e2-131">Свойство</span><span class="sxs-lookup"><span data-stu-id="8e2e2-131">Property</span></span>                | <span data-ttu-id="8e2e2-132">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8e2e2-132">xsi:type</span></span>           | <span data-ttu-id="8e2e2-133">Значение</span><span class="sxs-lookup"><span data-stu-id="8e2e2-133">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="8e2e2-134">DataType</span><span class="sxs-lookup"><span data-stu-id="8e2e2-134">DataType</span></span><br/>     | <span data-ttu-id="8e2e2-135">строка</span><span class="sxs-lookup"><span data-stu-id="8e2e2-135">string</span></span><br/>  | <span data-ttu-id="8e2e2-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="8e2e2-136">xs:string</span></span><br/>       |
| <span data-ttu-id="8e2e2-137">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8e2e2-137">DefaultValue</span></span><br/> | <span data-ttu-id="8e2e2-138">строка</span><span class="sxs-lookup"><span data-stu-id="8e2e2-138">string</span></span><br/>  | <span data-ttu-id="8e2e2-139">неопределенный</span><span class="sxs-lookup"><span data-stu-id="8e2e2-139">undefined</span></span><br/>       |
| <span data-ttu-id="8e2e2-140">MaxLength</span><span class="sxs-lookup"><span data-stu-id="8e2e2-140">MaxLength</span></span><br/>    | <span data-ttu-id="8e2e2-141">Целое число</span><span class="sxs-lookup"><span data-stu-id="8e2e2-141">integer</span></span><br/> | <span data-ttu-id="8e2e2-142">неопределенный</span><span class="sxs-lookup"><span data-stu-id="8e2e2-142">undefined</span></span><br/>       |
| <span data-ttu-id="8e2e2-143">MinLength</span><span class="sxs-lookup"><span data-stu-id="8e2e2-143">MinLength</span></span><br/>    | <span data-ttu-id="8e2e2-144">целое число</span><span class="sxs-lookup"><span data-stu-id="8e2e2-144">integer</span></span><br/> | <span data-ttu-id="8e2e2-145">1</span><span class="sxs-lookup"><span data-stu-id="8e2e2-145">1</span></span><br/>               |
| <span data-ttu-id="8e2e2-146">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8e2e2-146">Mandatory</span></span><br/>    | <span data-ttu-id="8e2e2-147">строка</span><span class="sxs-lookup"><span data-stu-id="8e2e2-147">string</span></span><br/>  | <span data-ttu-id="8e2e2-148">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="8e2e2-148">psk:Conditional</span></span><br/> |
| <span data-ttu-id="8e2e2-149">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="8e2e2-149">UnitType</span></span><br/>     | <span data-ttu-id="8e2e2-150">строка</span><span class="sxs-lookup"><span data-stu-id="8e2e2-150">string</span></span><br/>  | <span data-ttu-id="8e2e2-151">characters</span><span class="sxs-lookup"><span data-stu-id="8e2e2-151">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="8e2e2-152">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8e2e2-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e2e2-153">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="8e2e2-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




