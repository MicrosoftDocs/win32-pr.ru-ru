---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ad30df59-0051-4471-8c0e-3207bcc7bfbe
title: жоберроршит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6724e72a9351efc1d3cc5912b9806fb8d65a85
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998151"
---
# <a name="joberrorsheet"></a><span data-ttu-id="cc55f-104">жоберроршит</span><span class="sxs-lookup"><span data-stu-id="cc55f-104">JobErrorSheet</span></span>

<span data-ttu-id="cc55f-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="cc55f-105">This topic is not current.</span></span> <span data-ttu-id="cc55f-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cc55f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cc55f-107">Описывает вывод листа ошибок.</span><span class="sxs-lookup"><span data-stu-id="cc55f-107">Describes the error sheet output.</span></span> <span data-ttu-id="cc55f-108">У всего задания будет один лист ошибок.</span><span class="sxs-lookup"><span data-stu-id="cc55f-108">The entire job will have a single error sheet.</span></span> <span data-ttu-id="cc55f-109">Лист ошибок должен быть выведен на экран по умолчанию Пажемедиасизе и использовать Пажемедиатипе по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cc55f-109">The error sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="cc55f-110">Лист ошибок должен быть изолирован от оставшейся части задания.</span><span class="sxs-lookup"><span data-stu-id="cc55f-110">The error sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="cc55f-111">Это означает, что любые параметры завершения или обработки (например, Жобдуплекс, Жобстапле или Жоббиндинг) не должны включать лист ошибок.</span><span class="sxs-lookup"><span data-stu-id="cc55f-111">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the error sheet.</span></span> <span data-ttu-id="cc55f-112">Лист ошибок должен быть последним листом задания.</span><span class="sxs-lookup"><span data-stu-id="cc55f-112">The error sheet should occur as the final sheet of the job.</span></span>

-   [<span data-ttu-id="cc55f-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="cc55f-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cc55f-114">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="cc55f-114">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="cc55f-115">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="cc55f-115">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="cc55f-116">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="cc55f-116">Element Information</span></span>



| <span data-ttu-id="cc55f-117">Имя</span><span class="sxs-lookup"><span data-stu-id="cc55f-117">Name</span></span> | <span data-ttu-id="cc55f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="cc55f-118">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc55f-119">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="cc55f-119">Element Type</span></span> <br/>   | <span data-ttu-id="cc55f-120">Компонент</span><span class="sxs-lookup"><span data-stu-id="cc55f-120">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="cc55f-121">Префикс области</span><span class="sxs-lookup"><span data-stu-id="cc55f-121">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cc55f-122">Задание</span><span class="sxs-lookup"><span data-stu-id="cc55f-122">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cc55f-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="cc55f-123">Notes</span></span> <br/>          | <span data-ttu-id="cc55f-124">Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="cc55f-124">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="cc55f-125">Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части.</span><span class="sxs-lookup"><span data-stu-id="cc55f-125">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="cc55f-126">Эти параметры относятся к формату XPS.</span><span class="sxs-lookup"><span data-stu-id="cc55f-126">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="cc55f-127">URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="cc55f-127">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="cc55f-128">Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="cc55f-128">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="cc55f-129">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="cc55f-129">Structural Content</span></span>

<span data-ttu-id="cc55f-130">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="cc55f-130">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <!--Describes when an error sheet should be output. -->
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <psf:Option name="psk:_ErrorSheetWhenOptionName_">
      <psf:Property name="psf:IdentityOption">
        <psf:Value xsi:type="xs:string">_ErrorSheetWhenIdentityOptionValue_</psf:Value>
      </psf:Property>
    </psf:Option>
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the error sheet. -->
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="cc55f-131">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="cc55f-131">Structure Variables</span></span>

<span data-ttu-id="cc55f-132">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="cc55f-132">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cc55f-133">Имя</span><span class="sxs-lookup"><span data-stu-id="cc55f-133">Name</span></span>                                             | <span data-ttu-id="cc55f-134">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cc55f-134">Data type</span></span>         | <span data-ttu-id="cc55f-135">Unit</span><span class="sxs-lookup"><span data-stu-id="cc55f-135">Unit</span></span>                  | <span data-ttu-id="cc55f-136">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="cc55f-136">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="cc55f-137">Сводка</span><span class="sxs-lookup"><span data-stu-id="cc55f-137">Summary</span></span>                                                                      |
|--------------------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="cc55f-138">\_ерроршитвхеноптионнаме\_</span><span class="sxs-lookup"><span data-stu-id="cc55f-138">\_ErrorSheetWhenOptionName\_</span></span><br/>          | <span data-ttu-id="cc55f-139">строка</span><span class="sxs-lookup"><span data-stu-id="cc55f-139">string</span></span><br/> | <span data-ttu-id="cc55f-140">characters</span><span class="sxs-lookup"><span data-stu-id="cc55f-140">characters</span></span><br/> | <span data-ttu-id="cc55f-141">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="cc55f-141">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="cc55f-142">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cc55f-142">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="cc55f-143">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="cc55f-143">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="cc55f-144">\_ерроршитвхенидентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="cc55f-144">\_ErrorSheetWhenIdentityOptionValue\_</span></span><br/> | <span data-ttu-id="cc55f-145">строка</span><span class="sxs-lookup"><span data-stu-id="cc55f-145">string</span></span><br/> | <span data-ttu-id="cc55f-146">Недоступно</span><span class="sxs-lookup"><span data-stu-id="cc55f-146">n/a</span></span><br/>        | <span data-ttu-id="cc55f-147">True, False.</span><span class="sxs-lookup"><span data-stu-id="cc55f-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="cc55f-148">Определяет критерии выбора пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cc55f-148">Defines the user interface (UI) selection criteria.</span></span><br/>               |
| <span data-ttu-id="cc55f-149">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="cc55f-149">\_OptionName\_</span></span><br/>                        | <span data-ttu-id="cc55f-150">строка</span><span class="sxs-lookup"><span data-stu-id="cc55f-150">string</span></span><br/> | <span data-ttu-id="cc55f-151">Недоступно</span><span class="sxs-lookup"><span data-stu-id="cc55f-151">n/a</span></span><br/>        | <span data-ttu-id="cc55f-152">Допустимое полное имя, как определено в https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="cc55f-152">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="cc55f-153">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cc55f-153">If no namespace is specified, default namespace is assumed.</span></span><br/>          | <span data-ttu-id="cc55f-154">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="cc55f-154">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="cc55f-155">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="cc55f-155">\_IdentityOptionValue\_</span></span><br/>               | <span data-ttu-id="cc55f-156">строка</span><span class="sxs-lookup"><span data-stu-id="cc55f-156">string</span></span><br/> | <span data-ttu-id="cc55f-157">Недоступно</span><span class="sxs-lookup"><span data-stu-id="cc55f-157">n/a</span></span><br/>        | <span data-ttu-id="cc55f-158">True, False.</span><span class="sxs-lookup"><span data-stu-id="cc55f-158">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="cc55f-159">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="cc55f-159">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="cc55f-160">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="cc55f-160">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="cc55f-161">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="cc55f-161">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="cc55f-162">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="cc55f-162">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <!-- Specifies an error sheet will be output for every job. -->
    <psf:Option name="psk:Always" />
    <!-- Specifies an error sheet will be output only on error. -->
    <psf:Option name="psk:OnError" />
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom error sheet should be output. If a JobErrorSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no error sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) error sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="cc55f-163">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="cc55f-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc55f-164">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="cc55f-164">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




