---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: пажеблендколорспаце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12002b25265a66a0aa3a5168f29e1e8e542ce31
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998081"
---
# <a name="pageblendcolorspace"></a><span data-ttu-id="5401a-104">пажеблендколорспаце</span><span class="sxs-lookup"><span data-stu-id="5401a-104">PageBlendColorSpace</span></span>

<span data-ttu-id="5401a-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="5401a-105">This topic is not current.</span></span> <span data-ttu-id="5401a-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5401a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5401a-107">Описывает цветовое пространство, которое должно использоваться для операций смешения.</span><span class="sxs-lookup"><span data-stu-id="5401a-107">Describes the color space that should be used for blending operations.</span></span>

-   [<span data-ttu-id="5401a-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5401a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5401a-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="5401a-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5401a-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5401a-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5401a-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5401a-111">Element Information</span></span>



| <span data-ttu-id="5401a-112">Имя</span><span class="sxs-lookup"><span data-stu-id="5401a-112">Name</span></span> | <span data-ttu-id="5401a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="5401a-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5401a-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="5401a-114">Element Type</span></span> <br/>   | <span data-ttu-id="5401a-115">Компонент</span><span class="sxs-lookup"><span data-stu-id="5401a-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="5401a-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="5401a-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5401a-117">Задание</span><span class="sxs-lookup"><span data-stu-id="5401a-117">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5401a-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="5401a-118">Notes</span></span> <br/>          | <span data-ttu-id="5401a-119">Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="5401a-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="5401a-120">Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части.</span><span class="sxs-lookup"><span data-stu-id="5401a-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="5401a-121">Эти параметры относятся к формату XPS.</span><span class="sxs-lookup"><span data-stu-id="5401a-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="5401a-122">URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="5401a-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="5401a-123">Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5401a-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="5401a-124">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="5401a-124">Structural Content</span></span>

<span data-ttu-id="5401a-125">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="5401a-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="5401a-126">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="5401a-126">Structure Variables</span></span>

<span data-ttu-id="5401a-127">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="5401a-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5401a-128">Имя</span><span class="sxs-lookup"><span data-stu-id="5401a-128">Name</span></span>                               | <span data-ttu-id="5401a-129">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5401a-129">Data type</span></span>         | <span data-ttu-id="5401a-130">Unit</span><span class="sxs-lookup"><span data-stu-id="5401a-130">Unit</span></span>                  | <span data-ttu-id="5401a-131">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="5401a-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5401a-132">Сводка</span><span class="sxs-lookup"><span data-stu-id="5401a-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5401a-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5401a-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5401a-134">строка</span><span class="sxs-lookup"><span data-stu-id="5401a-134">string</span></span><br/> | <span data-ttu-id="5401a-135">characters</span><span class="sxs-lookup"><span data-stu-id="5401a-135">characters</span></span><br/> | <span data-ttu-id="5401a-136">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="5401a-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5401a-137">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5401a-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5401a-138">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="5401a-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5401a-139">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="5401a-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5401a-140">строка</span><span class="sxs-lookup"><span data-stu-id="5401a-140">string</span></span><br/> | <span data-ttu-id="5401a-141">Недоступно</span><span class="sxs-lookup"><span data-stu-id="5401a-141">n/a</span></span><br/>        | <span data-ttu-id="5401a-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="5401a-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5401a-143">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="5401a-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5401a-144">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5401a-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5401a-145">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="5401a-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5401a-146">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="5401a-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="5401a-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5401a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5401a-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="5401a-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




