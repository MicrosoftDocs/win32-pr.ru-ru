---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: c529c731-fcf0-463e-a251-6a05215e4d23
title: пажедевицеколорспацеусаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be77f143457ea24d5c23aba443209ba35ce02454
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "103914279"
---
# <a name="pagedevicecolorspaceusage"></a><span data-ttu-id="0ea07-104">пажедевицеколорспацеусаже</span><span class="sxs-lookup"><span data-stu-id="0ea07-104">PageDeviceColorSpaceUsage</span></span>

<span data-ttu-id="0ea07-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="0ea07-105">This topic is not current.</span></span> <span data-ttu-id="0ea07-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0ea07-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0ea07-107">В сочетании с параметром Пажедевицеколорспацепрофилеури этот параметр определяет поведение отрисовки для элементов, представленных в цветовом пространстве устройства.</span><span class="sxs-lookup"><span data-stu-id="0ea07-107">In conjunction with the PageDeviceColorSpaceProfileURI parameter, this parameter defines the rendering behavior for elements presented in a device color space.</span></span>

-   [<span data-ttu-id="0ea07-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0ea07-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0ea07-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="0ea07-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0ea07-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="0ea07-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0ea07-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0ea07-111">Element Information</span></span>



| <span data-ttu-id="0ea07-112">Имя</span><span class="sxs-lookup"><span data-stu-id="0ea07-112">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea07-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="0ea07-113">Element Type</span></span> <br/>   | <span data-ttu-id="0ea07-114">Функция</span><span class="sxs-lookup"><span data-stu-id="0ea07-114">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="0ea07-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="0ea07-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0ea07-116">Страница</span><span class="sxs-lookup"><span data-stu-id="0ea07-116">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="0ea07-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="0ea07-117">Notes</span></span> <br/>          | <span data-ttu-id="0ea07-118">Это относится только к документам XPS и не должен использоваться в произвольных PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="0ea07-118">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="0ea07-119">Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="0ea07-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="0ea07-120">Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части.</span><span class="sxs-lookup"><span data-stu-id="0ea07-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="0ea07-121">Эти параметры относятся к формату XPS.</span><span class="sxs-lookup"><span data-stu-id="0ea07-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="0ea07-122">URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="0ea07-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="0ea07-123">Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0ea07-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="0ea07-124">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="0ea07-124">Structural Content</span></span>

<span data-ttu-id="0ea07-125">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="0ea07-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceColorSpaceUsage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="0ea07-126">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="0ea07-126">Structure Variables</span></span>

<span data-ttu-id="0ea07-127">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="0ea07-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0ea07-128">Имя</span><span class="sxs-lookup"><span data-stu-id="0ea07-128">Name</span></span>                               | <span data-ttu-id="0ea07-129">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0ea07-129">Data type</span></span>         | <span data-ttu-id="0ea07-130">Unit</span><span class="sxs-lookup"><span data-stu-id="0ea07-130">Unit</span></span>                  | <span data-ttu-id="0ea07-131">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="0ea07-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0ea07-132">Сводка</span><span class="sxs-lookup"><span data-stu-id="0ea07-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0ea07-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0ea07-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0ea07-134">строка</span><span class="sxs-lookup"><span data-stu-id="0ea07-134">string</span></span><br/> | <span data-ttu-id="0ea07-135">characters</span><span class="sxs-lookup"><span data-stu-id="0ea07-135">characters</span></span><br/> | <span data-ttu-id="0ea07-136">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="0ea07-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0ea07-137">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0ea07-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0ea07-138">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="0ea07-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="0ea07-139">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="0ea07-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0ea07-140">строка</span><span class="sxs-lookup"><span data-stu-id="0ea07-140">string</span></span><br/> | <span data-ttu-id="0ea07-141">Недоступно</span><span class="sxs-lookup"><span data-stu-id="0ea07-141">n/a</span></span><br/>        | <span data-ttu-id="0ea07-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="0ea07-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0ea07-143">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="0ea07-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0ea07-144">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="0ea07-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0ea07-145">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="0ea07-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0ea07-146">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="0ea07-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceColorSpaceUsage">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- If the device determines that the profile specified by the PageDeviceColorSpaceProfileURI parameter can be used as a device color space profile, all elements using the same profile are treated as already being specified in device color space. All other elements MUST use the profile specified for that element.
If the profile cannot be used as a device color space profile, elements using the profile MUST be color managed like any other element using the color profile. -->
  <psf:Option name="psk:MatchToDefault" />
  <!-- If the profile specified by the PageDeviceColorSpaceProfileURI parameter has a number of channels matching the number of primaries of the device, it SHOULD be used instead of the devices internal color management for all elements. Elements using this profile are assumed to be in device color space and will not be color managed further. -->
  <psf:Option name="psk:OverrideDeviceDefault" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="0ea07-147">См. также</span><span class="sxs-lookup"><span data-stu-id="0ea07-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ea07-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="0ea07-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




