---
description: Проверьте элемент Пажедевицеколорспацеусаже, настраиваемый пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: c529c731-fcf0-463e-a251-6a05215e4d23
title: пажедевицеколорспацеусаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30b81a37d103d3ce5f1cbb1fb8c032a18d495c2c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396669"
---
# <a name="pagedevicecolorspaceusage"></a><span data-ttu-id="b087a-105">пажедевицеколорспацеусаже</span><span class="sxs-lookup"><span data-stu-id="b087a-105">PageDeviceColorSpaceUsage</span></span>

<span data-ttu-id="b087a-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="b087a-106">This topic is not current.</span></span> <span data-ttu-id="b087a-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b087a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b087a-108">В сочетании с параметром Пажедевицеколорспацепрофилеури этот параметр определяет поведение отрисовки для элементов, представленных в цветовом пространстве устройства.</span><span class="sxs-lookup"><span data-stu-id="b087a-108">In conjunction with the PageDeviceColorSpaceProfileURI parameter, this parameter defines the rendering behavior for elements presented in a device color space.</span></span>

-   [<span data-ttu-id="b087a-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b087a-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b087a-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="b087a-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b087a-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b087a-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b087a-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b087a-112">Element Information</span></span>



| <span data-ttu-id="b087a-113">Имя</span><span class="sxs-lookup"><span data-stu-id="b087a-113">Name</span></span> | <span data-ttu-id="b087a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b087a-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b087a-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="b087a-115">Element Type</span></span> <br/>   | <span data-ttu-id="b087a-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="b087a-116">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="b087a-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="b087a-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b087a-118">Страница</span><span class="sxs-lookup"><span data-stu-id="b087a-118">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b087a-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="b087a-119">Notes</span></span> <br/>          | <span data-ttu-id="b087a-120">Это относится только к документам XPS и не должен использоваться в произвольных PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="b087a-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="b087a-121">Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="b087a-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="b087a-122">Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части.</span><span class="sxs-lookup"><span data-stu-id="b087a-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="b087a-123">Эти параметры относятся к формату XPS.</span><span class="sxs-lookup"><span data-stu-id="b087a-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="b087a-124">URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="b087a-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="b087a-125">Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="b087a-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="b087a-126">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="b087a-126">Structural Content</span></span>

<span data-ttu-id="b087a-127">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="b087a-127">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="b087a-128">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="b087a-128">Structure Variables</span></span>

<span data-ttu-id="b087a-129">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="b087a-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b087a-130">Имя</span><span class="sxs-lookup"><span data-stu-id="b087a-130">Name</span></span>                               | <span data-ttu-id="b087a-131">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b087a-131">Data type</span></span>         | <span data-ttu-id="b087a-132">Unit</span><span class="sxs-lookup"><span data-stu-id="b087a-132">Unit</span></span>                  | <span data-ttu-id="b087a-133">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="b087a-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b087a-134">Итоги</span><span class="sxs-lookup"><span data-stu-id="b087a-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b087a-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="b087a-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b087a-136">строка</span><span class="sxs-lookup"><span data-stu-id="b087a-136">string</span></span><br/> | <span data-ttu-id="b087a-137">characters</span><span class="sxs-lookup"><span data-stu-id="b087a-137">characters</span></span><br/> | <span data-ttu-id="b087a-138">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="b087a-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b087a-139">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b087a-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b087a-140">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="b087a-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="b087a-141">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="b087a-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b087a-142">строка</span><span class="sxs-lookup"><span data-stu-id="b087a-142">string</span></span><br/> | <span data-ttu-id="b087a-143">Недоступно</span><span class="sxs-lookup"><span data-stu-id="b087a-143">n/a</span></span><br/>        | <span data-ttu-id="b087a-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="b087a-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b087a-145">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="b087a-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b087a-146">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b087a-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b087a-147">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="b087a-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b087a-148">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="b087a-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="b087a-149">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b087a-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b087a-150">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="b087a-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




