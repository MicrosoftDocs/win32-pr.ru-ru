---
description: Ознакомьтесь с элементом Документбаннершит, настраиваемым пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: документбаннершит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ce05ffae190835e4a8b4082c634b34e26103ab
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548772"
---
# <a name="documentbannersheet"></a><span data-ttu-id="7ef7d-105">документбаннершит</span><span class="sxs-lookup"><span data-stu-id="7ef7d-105">DocumentBannerSheet</span></span>

<span data-ttu-id="7ef7d-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-106">This topic is not current.</span></span> <span data-ttu-id="7ef7d-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7ef7d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7ef7d-108">Описывает лист заголовка для вывода в определенном документе.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-108">Describes the banner sheet to be output for a particular document.</span></span> <span data-ttu-id="7ef7d-109">Лист заголовков должен быть выведен на экран по умолчанию Пажемедиасизе с использованием Пажемедиатипе по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-109">The banner sheet should be output on the default PageMediaSize ,using the default PageMediaType.</span></span> <span data-ttu-id="7ef7d-110">Лист заголовков также должен быть изолирован от оставшейся части документа.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-110">The banner sheet should also be isolated from the remainder of the document.</span></span> <span data-ttu-id="7ef7d-111">Это означает, что любые параметры завершения или обработки документа (например, Документдуплекс, Документстапле или Документбиндинг) не должны включать лист заголовков.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-111">This means that any document finishing or processing options (such as DocumentDuplex, DocumentStaple, or DocumentBinding) should not include the banner sheet.</span></span> <span data-ttu-id="7ef7d-112">Лист заголовка может быть не изолирован от оставшейся части задания.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-112">The banner sheet may or may not be isolated from the remainder of the job.</span></span> <span data-ttu-id="7ef7d-113">Это означает, что любые параметры завершения или обработки задания могут содержать титульный лист документа.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-113">This means that any job finishing or processing options, may include the document banner sheet.</span></span> <span data-ttu-id="7ef7d-114">Лист заголовков должен быть первым листом документа.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-114">The banner sheet should occur as the first sheet of the document.</span></span>

-   [<span data-ttu-id="7ef7d-115">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7ef7d-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7ef7d-116">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="7ef7d-116">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="7ef7d-117">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7ef7d-117">Element Information</span></span>



| <span data-ttu-id="7ef7d-118">Имя</span><span class="sxs-lookup"><span data-stu-id="7ef7d-118">Name</span></span> | <span data-ttu-id="7ef7d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="7ef7d-119">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ef7d-120">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="7ef7d-120">Element Type</span></span> <br/>   | <span data-ttu-id="7ef7d-121">Компонент</span><span class="sxs-lookup"><span data-stu-id="7ef7d-121">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="7ef7d-122">Префикс области</span><span class="sxs-lookup"><span data-stu-id="7ef7d-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7ef7d-123">Документ</span><span class="sxs-lookup"><span data-stu-id="7ef7d-123">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="7ef7d-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="7ef7d-124">Notes</span></span> <br/>          | <span data-ttu-id="7ef7d-125">Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-125">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="7ef7d-126">Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-126">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="7ef7d-127">Эти параметры относятся к формату XPS.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-127">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="7ef7d-128">URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-128">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="7ef7d-129">Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-129">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="7ef7d-130">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="7ef7d-130">Structural Content</span></span>

<span data-ttu-id="7ef7d-131">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="7ef7d-131">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="7ef7d-132">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="7ef7d-132">Structure Variables</span></span>

<span data-ttu-id="7ef7d-133">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-133">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7ef7d-134">Имя</span><span class="sxs-lookup"><span data-stu-id="7ef7d-134">Name</span></span>                               | <span data-ttu-id="7ef7d-135">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7ef7d-135">Data type</span></span>         | <span data-ttu-id="7ef7d-136">Unit</span><span class="sxs-lookup"><span data-stu-id="7ef7d-136">Unit</span></span>                   | <span data-ttu-id="7ef7d-137">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="7ef7d-137">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7ef7d-138">Итоги</span><span class="sxs-lookup"><span data-stu-id="7ef7d-138">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7ef7d-139">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="7ef7d-139">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7ef7d-140">строка</span><span class="sxs-lookup"><span data-stu-id="7ef7d-140">string</span></span><br/> | <span data-ttu-id="7ef7d-141">characters</span><span class="sxs-lookup"><span data-stu-id="7ef7d-141">characters</span></span> <br/> | <span data-ttu-id="7ef7d-142">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="7ef7d-142">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7ef7d-143">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-143">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7ef7d-144">Имя параметра</span><span class="sxs-lookup"><span data-stu-id="7ef7d-144">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="7ef7d-145">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="7ef7d-145">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7ef7d-146">строка</span><span class="sxs-lookup"><span data-stu-id="7ef7d-146">string</span></span><br/> | <span data-ttu-id="7ef7d-147">Н/Д</span><span class="sxs-lookup"><span data-stu-id="7ef7d-147">n/a</span></span><br/>         | <span data-ttu-id="7ef7d-148">True, False</span><span class="sxs-lookup"><span data-stu-id="7ef7d-148">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="7ef7d-149">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-149">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7ef7d-150">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="7ef7d-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7ef7d-151">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="7ef7d-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7ef7d-152">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="7ef7d-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="7ef7d-153">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="7ef7d-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ef7d-154">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="7ef7d-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




