---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: документбаннершит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ef61001e45178989d6f89e17d8cc38b82c1354
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996311"
---
# <a name="documentbannersheet"></a><span data-ttu-id="01183-104">документбаннершит</span><span class="sxs-lookup"><span data-stu-id="01183-104">DocumentBannerSheet</span></span>

<span data-ttu-id="01183-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="01183-105">This topic is not current.</span></span> <span data-ttu-id="01183-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="01183-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="01183-107">Описывает лист заголовка для вывода в определенном документе.</span><span class="sxs-lookup"><span data-stu-id="01183-107">Describes the banner sheet to be output for a particular document.</span></span> <span data-ttu-id="01183-108">Лист заголовков должен быть выведен на экран по умолчанию Пажемедиасизе с использованием Пажемедиатипе по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="01183-108">The banner sheet should be output on the default PageMediaSize ,using the default PageMediaType.</span></span> <span data-ttu-id="01183-109">Лист заголовков также должен быть изолирован от оставшейся части документа.</span><span class="sxs-lookup"><span data-stu-id="01183-109">The banner sheet should also be isolated from the remainder of the document.</span></span> <span data-ttu-id="01183-110">Это означает, что любые параметры завершения или обработки документа (например, Документдуплекс, Документстапле или Документбиндинг) не должны включать лист заголовков.</span><span class="sxs-lookup"><span data-stu-id="01183-110">This means that any document finishing or processing options (such as DocumentDuplex, DocumentStaple, or DocumentBinding) should not include the banner sheet.</span></span> <span data-ttu-id="01183-111">Лист заголовка может быть не изолирован от оставшейся части задания.</span><span class="sxs-lookup"><span data-stu-id="01183-111">The banner sheet may or may not be isolated from the remainder of the job.</span></span> <span data-ttu-id="01183-112">Это означает, что любые параметры завершения или обработки задания могут содержать титульный лист документа.</span><span class="sxs-lookup"><span data-stu-id="01183-112">This means that any job finishing or processing options, may include the document banner sheet.</span></span> <span data-ttu-id="01183-113">Лист заголовков должен быть первым листом документа.</span><span class="sxs-lookup"><span data-stu-id="01183-113">The banner sheet should occur as the first sheet of the document.</span></span>

-   [<span data-ttu-id="01183-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="01183-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="01183-115">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="01183-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="01183-116">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="01183-116">Element Information</span></span>



| <span data-ttu-id="01183-117">Имя</span><span class="sxs-lookup"><span data-stu-id="01183-117">Name</span></span> | <span data-ttu-id="01183-118">Значение</span><span class="sxs-lookup"><span data-stu-id="01183-118">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01183-119">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="01183-119">Element Type</span></span> <br/>   | <span data-ttu-id="01183-120">Компонент</span><span class="sxs-lookup"><span data-stu-id="01183-120">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="01183-121">Префикс области</span><span class="sxs-lookup"><span data-stu-id="01183-121">Scoping Prefix</span></span> <br/> | <span data-ttu-id="01183-122">Документ</span><span class="sxs-lookup"><span data-stu-id="01183-122">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="01183-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="01183-123">Notes</span></span> <br/>          | <span data-ttu-id="01183-124">Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="01183-124">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="01183-125">Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части.</span><span class="sxs-lookup"><span data-stu-id="01183-125">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="01183-126">Эти параметры относятся к формату XPS.</span><span class="sxs-lookup"><span data-stu-id="01183-126">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="01183-127">URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="01183-127">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="01183-128">Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="01183-128">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="01183-129">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="01183-129">Structural Content</span></span>

<span data-ttu-id="01183-130">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="01183-130">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="01183-131">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="01183-131">Structure Variables</span></span>

<span data-ttu-id="01183-132">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="01183-132">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="01183-133">Имя</span><span class="sxs-lookup"><span data-stu-id="01183-133">Name</span></span>                               | <span data-ttu-id="01183-134">Тип данных</span><span class="sxs-lookup"><span data-stu-id="01183-134">Data type</span></span>         | <span data-ttu-id="01183-135">Unit</span><span class="sxs-lookup"><span data-stu-id="01183-135">Unit</span></span>                   | <span data-ttu-id="01183-136">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="01183-136">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="01183-137">Сводка</span><span class="sxs-lookup"><span data-stu-id="01183-137">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="01183-138">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="01183-138">\_OptionName\_</span></span><br/>          | <span data-ttu-id="01183-139">строка</span><span class="sxs-lookup"><span data-stu-id="01183-139">string</span></span><br/> | <span data-ttu-id="01183-140">characters</span><span class="sxs-lookup"><span data-stu-id="01183-140">characters</span></span> <br/> | <span data-ttu-id="01183-141">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="01183-141">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="01183-142">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="01183-142">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="01183-143">Имя параметра</span><span class="sxs-lookup"><span data-stu-id="01183-143">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="01183-144">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="01183-144">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="01183-145">строка</span><span class="sxs-lookup"><span data-stu-id="01183-145">string</span></span><br/> | <span data-ttu-id="01183-146">Недоступно</span><span class="sxs-lookup"><span data-stu-id="01183-146">n/a</span></span><br/>         | <span data-ttu-id="01183-147">True, False</span><span class="sxs-lookup"><span data-stu-id="01183-147">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="01183-148">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="01183-148">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="01183-149">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="01183-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="01183-150">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="01183-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="01183-151">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="01183-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a DocumentBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="01183-152">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="01183-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01183-153">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="01183-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




