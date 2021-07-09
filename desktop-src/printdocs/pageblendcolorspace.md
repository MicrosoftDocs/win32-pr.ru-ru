---
description: Сведения об элементе Пажеблендколорспаце, настраиваемом пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: пажеблендколорспаце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b36ce3a1def74058014fc396d9ef53aed6a32302
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549342"
---
# <a name="pageblendcolorspace"></a><span data-ttu-id="8f225-105">пажеблендколорспаце</span><span class="sxs-lookup"><span data-stu-id="8f225-105">PageBlendColorSpace</span></span>

<span data-ttu-id="8f225-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="8f225-106">This topic is not current.</span></span> <span data-ttu-id="8f225-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8f225-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8f225-108">Описывает цветовое пространство, которое должно использоваться для операций смешения.</span><span class="sxs-lookup"><span data-stu-id="8f225-108">Describes the color space that should be used for blending operations.</span></span>

-   [<span data-ttu-id="8f225-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8f225-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8f225-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="8f225-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="8f225-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="8f225-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8f225-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8f225-112">Element Information</span></span>



| <span data-ttu-id="8f225-113">Имя</span><span class="sxs-lookup"><span data-stu-id="8f225-113">Name</span></span> | <span data-ttu-id="8f225-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8f225-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f225-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="8f225-115">Element Type</span></span> <br/>   | <span data-ttu-id="8f225-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="8f225-116">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8f225-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="8f225-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8f225-118">Задание</span><span class="sxs-lookup"><span data-stu-id="8f225-118">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="8f225-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="8f225-119">Notes</span></span> <br/>          | <span data-ttu-id="8f225-120">Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="8f225-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="8f225-121">Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части.</span><span class="sxs-lookup"><span data-stu-id="8f225-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="8f225-122">Эти параметры относятся к формату XPS.</span><span class="sxs-lookup"><span data-stu-id="8f225-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="8f225-123">URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="8f225-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="8f225-124">Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8f225-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="8f225-125">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="8f225-125">Structural Content</span></span>

<span data-ttu-id="8f225-126">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="8f225-126">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
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

## <a name="structure-variables"></a><span data-ttu-id="8f225-127">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="8f225-127">Structure Variables</span></span>

<span data-ttu-id="8f225-128">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="8f225-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8f225-129">Имя</span><span class="sxs-lookup"><span data-stu-id="8f225-129">Name</span></span>                               | <span data-ttu-id="8f225-130">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8f225-130">Data type</span></span>         | <span data-ttu-id="8f225-131">Unit</span><span class="sxs-lookup"><span data-stu-id="8f225-131">Unit</span></span>                  | <span data-ttu-id="8f225-132">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="8f225-132">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="8f225-133">Итоги</span><span class="sxs-lookup"><span data-stu-id="8f225-133">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8f225-134">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="8f225-134">\_OptionName\_</span></span><br/>          | <span data-ttu-id="8f225-135">строка</span><span class="sxs-lookup"><span data-stu-id="8f225-135">string</span></span><br/> | <span data-ttu-id="8f225-136">characters</span><span class="sxs-lookup"><span data-stu-id="8f225-136">characters</span></span><br/> | <span data-ttu-id="8f225-137">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="8f225-137">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="8f225-138">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8f225-138">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8f225-139">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="8f225-139">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="8f225-140">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="8f225-140">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="8f225-141">строка</span><span class="sxs-lookup"><span data-stu-id="8f225-141">string</span></span><br/> | <span data-ttu-id="8f225-142">Н/Д</span><span class="sxs-lookup"><span data-stu-id="8f225-142">n/a</span></span><br/>        | <span data-ttu-id="8f225-143">True, False.</span><span class="sxs-lookup"><span data-stu-id="8f225-143">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="8f225-144">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="8f225-144">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8f225-145">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="8f225-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8f225-146">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="8f225-146">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8f225-147">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="8f225-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- sRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:sRGB" />
  <!-- scRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:scRGB" />
  <!-- Specifies an ICC profile defining the color space that SHOULD be used for blending.  Note: This applies to XPS Documents only and should not be used in arbitrary PrintTickets. -->
  <psf:Option name="psk:ICCProfile">
    <!-- XPS specific part name for the blend mode ICC Profile -->
    <psf:ScoredProperty name="psk:URI">
      <psf:ParameterRef name="psk:PageBlendColorSpaceICCProfileURI" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="8f225-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8f225-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f225-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="8f225-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




