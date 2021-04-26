---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: c8f9001e-9f92-405a-8f3a-bc59b47c9e35
title: жобпримарибаннершит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c438cd0f33bc7b3a80fc3e654e0d64831e3b6777
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996931"
---
# <a name="jobprimarybannersheet"></a><span data-ttu-id="87935-104">жобпримарибаннершит</span><span class="sxs-lookup"><span data-stu-id="87935-104">JobPrimaryBannerSheet</span></span>

<span data-ttu-id="87935-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="87935-105">This topic is not current.</span></span> <span data-ttu-id="87935-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="87935-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="87935-107">Описывает лист заголовка для вывода задания.</span><span class="sxs-lookup"><span data-stu-id="87935-107">Describes the banner sheet to be output for the job.</span></span> <span data-ttu-id="87935-108">Лист заголовков должен быть выведен на экран по умолчанию Пажемедиасизе и использовать Пажемедиатипе по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="87935-108">The banner sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="87935-109">Лист заголовков должен быть изолирован от оставшейся части задания.</span><span class="sxs-lookup"><span data-stu-id="87935-109">The banner sheet should be isolated from the remainder of the job.</span></span> <span data-ttu-id="87935-110">Это означает, что любые параметры завершения или обработки (например, Жобдуплексаллдокументсконтигуаусли, Жобстаплеаллдокументс или Жоббиндаллдокументс) не должны включать лист заголовков.</span><span class="sxs-lookup"><span data-stu-id="87935-110">This means that any finishing or processing options (such as JobDuplexAllDocumentsContiguously, JobStapleAllDocuments, or JobBindAllDocuments) should not include the banner sheet.</span></span> <span data-ttu-id="87935-111">Лист заголовков должен быть первым листом задания.</span><span class="sxs-lookup"><span data-stu-id="87935-111">The banner sheet should occur as the first sheet of the job.</span></span>

-   [<span data-ttu-id="87935-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="87935-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="87935-113">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="87935-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="87935-114">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="87935-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="87935-115">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="87935-115">Element Information</span></span>



| <span data-ttu-id="87935-116">Имя</span><span class="sxs-lookup"><span data-stu-id="87935-116">Name</span></span> | <span data-ttu-id="87935-117">Значение</span><span class="sxs-lookup"><span data-stu-id="87935-117">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87935-118">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="87935-118">Element Type</span></span> <br/>   | <span data-ttu-id="87935-119">Компонент</span><span class="sxs-lookup"><span data-stu-id="87935-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="87935-120">Префикс области</span><span class="sxs-lookup"><span data-stu-id="87935-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="87935-121">Задание</span><span class="sxs-lookup"><span data-stu-id="87935-121">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="87935-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="87935-122">Notes</span></span> <br/>          | <span data-ttu-id="87935-123">Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="87935-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="87935-124">Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части.</span><span class="sxs-lookup"><span data-stu-id="87935-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="87935-125">Эти параметры относятся к формату XPS.</span><span class="sxs-lookup"><span data-stu-id="87935-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="87935-126">URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="87935-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="87935-127">Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="87935-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="87935-128">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="87935-128">Structural Content</span></span>

<span data-ttu-id="87935-129">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="87935-129">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the banner sheet. -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="87935-130">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="87935-130">Structure Variables</span></span>

<span data-ttu-id="87935-131">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="87935-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="87935-132">Имя</span><span class="sxs-lookup"><span data-stu-id="87935-132">Name</span></span>                               | <span data-ttu-id="87935-133">Тип данных</span><span class="sxs-lookup"><span data-stu-id="87935-133">Data type</span></span>         | <span data-ttu-id="87935-134">Unit</span><span class="sxs-lookup"><span data-stu-id="87935-134">Unit</span></span>                  | <span data-ttu-id="87935-135">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="87935-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="87935-136">Сводка</span><span class="sxs-lookup"><span data-stu-id="87935-136">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="87935-137">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="87935-137">\_OptionName\_</span></span><br/>          | <span data-ttu-id="87935-138">строка</span><span class="sxs-lookup"><span data-stu-id="87935-138">string</span></span><br/> | <span data-ttu-id="87935-139">characters</span><span class="sxs-lookup"><span data-stu-id="87935-139">characters</span></span><br/> | <span data-ttu-id="87935-140">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="87935-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="87935-141">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="87935-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="87935-142">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="87935-142">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="87935-143">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="87935-143">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="87935-144">строка</span><span class="sxs-lookup"><span data-stu-id="87935-144">string</span></span><br/> | <span data-ttu-id="87935-145">Недоступно</span><span class="sxs-lookup"><span data-stu-id="87935-145">n/a</span></span><br/>        | <span data-ttu-id="87935-146">True, False.</span><span class="sxs-lookup"><span data-stu-id="87935-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="87935-147">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="87935-147">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="87935-148">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="87935-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="87935-149">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="87935-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="87935-150">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="87935-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a JobPrimaryBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored.  -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="87935-151">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="87935-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87935-152">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="87935-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




