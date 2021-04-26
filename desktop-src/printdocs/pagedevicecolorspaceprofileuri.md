---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: пажедевицеколорспацепрофилеури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a1b4cf607ddf880311659e562647ba583a2951
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995681"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="31015-104">пажедевицеколорспацепрофилеури</span><span class="sxs-lookup"><span data-stu-id="31015-104">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="31015-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="31015-105">This topic is not current.</span></span> <span data-ttu-id="31015-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="31015-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="31015-107">Указывает относительный URI для корня пакета в профиль ICC, содержащийся в документе XPS.</span><span class="sxs-lookup"><span data-stu-id="31015-107">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="31015-108">Обработка этого параметра зависит от значения функции Пажедевицеколорспацеусаже.</span><span class="sxs-lookup"><span data-stu-id="31015-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="31015-109">Предполагается, что все элементы, использующие этот профиль, уже находятся в соответствующем цветовом пространстве устройства и не будут управлять цветом в драйвере или устройстве.</span><span class="sxs-lookup"><span data-stu-id="31015-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="31015-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="31015-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="31015-111">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="31015-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="31015-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="31015-112">Element Information</span></span>



| <span data-ttu-id="31015-113">Имя</span><span class="sxs-lookup"><span data-stu-id="31015-113">Name</span></span> | <span data-ttu-id="31015-114">Значение</span><span class="sxs-lookup"><span data-stu-id="31015-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31015-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="31015-115">Element Type</span></span> <br/>   | <span data-ttu-id="31015-116">параметердеф</span><span class="sxs-lookup"><span data-stu-id="31015-116">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="31015-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="31015-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="31015-118">Страница</span><span class="sxs-lookup"><span data-stu-id="31015-118">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="31015-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="31015-119">Notes</span></span> <br/>          | <span data-ttu-id="31015-120">Это относится только к документам XPS и не должен использоваться в произвольных PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="31015-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="31015-121">Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="31015-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="31015-122">Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части.</span><span class="sxs-lookup"><span data-stu-id="31015-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="31015-123">Эти параметры относятся к формату XPS.</span><span class="sxs-lookup"><span data-stu-id="31015-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="31015-124">URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="31015-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="31015-125">Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="31015-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="31015-126">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="31015-126">Structure Content</span></span>

<span data-ttu-id="31015-127">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="31015-127">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="31015-128">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="31015-128">Structure Properties</span></span>

<span data-ttu-id="31015-129">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="31015-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="31015-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="31015-130">Property</span></span>                | <span data-ttu-id="31015-131">xsi:type</span><span class="sxs-lookup"><span data-stu-id="31015-131">xsi:type</span></span>           | <span data-ttu-id="31015-132">Значение</span><span class="sxs-lookup"><span data-stu-id="31015-132">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="31015-133">DataType</span><span class="sxs-lookup"><span data-stu-id="31015-133">DataType</span></span><br/>     | <span data-ttu-id="31015-134">строка</span><span class="sxs-lookup"><span data-stu-id="31015-134">string</span></span><br/>  | <span data-ttu-id="31015-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="31015-135">xs:string</span></span><br/>       |
| <span data-ttu-id="31015-136">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="31015-136">DefaultValue</span></span><br/> | <span data-ttu-id="31015-137">строка</span><span class="sxs-lookup"><span data-stu-id="31015-137">string</span></span><br/>  | <span data-ttu-id="31015-138">неопределенный</span><span class="sxs-lookup"><span data-stu-id="31015-138">undefined</span></span><br/>       |
| <span data-ttu-id="31015-139">MaxLength</span><span class="sxs-lookup"><span data-stu-id="31015-139">MaxLength</span></span><br/>    | <span data-ttu-id="31015-140">Целое число</span><span class="sxs-lookup"><span data-stu-id="31015-140">integer</span></span><br/> | <span data-ttu-id="31015-141">неопределенный</span><span class="sxs-lookup"><span data-stu-id="31015-141">undefined</span></span><br/>       |
| <span data-ttu-id="31015-142">MinLength</span><span class="sxs-lookup"><span data-stu-id="31015-142">MinLength</span></span><br/>    | <span data-ttu-id="31015-143">целое число</span><span class="sxs-lookup"><span data-stu-id="31015-143">integer</span></span><br/> | <span data-ttu-id="31015-144">1</span><span class="sxs-lookup"><span data-stu-id="31015-144">1</span></span><br/>               |
| <span data-ttu-id="31015-145">Обязательный</span><span class="sxs-lookup"><span data-stu-id="31015-145">Mandatory</span></span><br/>    | <span data-ttu-id="31015-146">строка</span><span class="sxs-lookup"><span data-stu-id="31015-146">string</span></span><br/>  | <span data-ttu-id="31015-147">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="31015-147">psk:Conditional</span></span><br/> |
| <span data-ttu-id="31015-148">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="31015-148">UnitType</span></span><br/>     | <span data-ttu-id="31015-149">строка</span><span class="sxs-lookup"><span data-stu-id="31015-149">string</span></span><br/>  | <span data-ttu-id="31015-150">characters</span><span class="sxs-lookup"><span data-stu-id="31015-150">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="31015-151">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="31015-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31015-152">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="31015-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




