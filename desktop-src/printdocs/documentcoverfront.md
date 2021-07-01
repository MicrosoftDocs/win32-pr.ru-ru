---
description: Сведения об элементе Документковерфронт, настраиваемом пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 25dbd083-5815-4b25-bfdc-4d14f96d2b45
title: документковерфронт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301b67c9a741caa48024646854b208ac5dffbb20
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119829"
---
# <a name="documentcoverfront"></a><span data-ttu-id="c28fe-105">документковерфронт</span><span class="sxs-lookup"><span data-stu-id="c28fe-105">DocumentCoverFront</span></span>

<span data-ttu-id="c28fe-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="c28fe-106">This topic is not current.</span></span> <span data-ttu-id="c28fe-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c28fe-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c28fe-108">Описывает передний (начальный) Титульный лист.</span><span class="sxs-lookup"><span data-stu-id="c28fe-108">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="c28fe-109">Каждый документ будет иметь отдельный лист.</span><span class="sxs-lookup"><span data-stu-id="c28fe-109">Each document will have a separate sheet.</span></span> <span data-ttu-id="c28fe-110">Лист должен быть напечатан на Пажемедиасизе и Пажемедиатипе, используемый для первой страницы документа.</span><span class="sxs-lookup"><span data-stu-id="c28fe-110">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the document.</span></span> <span data-ttu-id="c28fe-111">Лист должен быть интегрирован в параметры обработки (например, Документдуплекс, Документнуп), как указано в указанном параметре.</span><span class="sxs-lookup"><span data-stu-id="c28fe-111">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="c28fe-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c28fe-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c28fe-113">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="c28fe-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c28fe-114">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c28fe-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c28fe-115">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c28fe-115">Element Information</span></span>



| <span data-ttu-id="c28fe-116">Имя</span><span class="sxs-lookup"><span data-stu-id="c28fe-116">Name</span></span> | <span data-ttu-id="c28fe-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c28fe-117">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c28fe-118">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="c28fe-118">Element Type</span></span> <br/>   | <span data-ttu-id="c28fe-119">Компонент</span><span class="sxs-lookup"><span data-stu-id="c28fe-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="c28fe-120">Префикс области</span><span class="sxs-lookup"><span data-stu-id="c28fe-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c28fe-121">Документ</span><span class="sxs-lookup"><span data-stu-id="c28fe-121">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="c28fe-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="c28fe-122">Notes</span></span> <br/>          | <span data-ttu-id="c28fe-123">Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="c28fe-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="c28fe-124">Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части.</span><span class="sxs-lookup"><span data-stu-id="c28fe-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="c28fe-125">Эти параметры относятся к формату XPS.</span><span class="sxs-lookup"><span data-stu-id="c28fe-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="c28fe-126">URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="c28fe-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="c28fe-127">Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c28fe-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="c28fe-128">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="c28fe-128">Structural Content</span></span>

<span data-ttu-id="c28fe-129">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="c28fe-129">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name for the front cover sheet. -->
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="c28fe-130">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="c28fe-130">Structure Variables</span></span>

<span data-ttu-id="c28fe-131">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="c28fe-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c28fe-132">Имя</span><span class="sxs-lookup"><span data-stu-id="c28fe-132">Name</span></span>                               | <span data-ttu-id="c28fe-133">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c28fe-133">Data type</span></span>         | <span data-ttu-id="c28fe-134">Unit</span><span class="sxs-lookup"><span data-stu-id="c28fe-134">Unit</span></span>                  | <span data-ttu-id="c28fe-135">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="c28fe-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c28fe-136">Сводка</span><span class="sxs-lookup"><span data-stu-id="c28fe-136">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c28fe-137">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="c28fe-137">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c28fe-138">строка</span><span class="sxs-lookup"><span data-stu-id="c28fe-138">string</span></span><br/> | <span data-ttu-id="c28fe-139">characters</span><span class="sxs-lookup"><span data-stu-id="c28fe-139">characters</span></span><br/> | <span data-ttu-id="c28fe-140">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="c28fe-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c28fe-141">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c28fe-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c28fe-142">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="c28fe-142">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="c28fe-143">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="c28fe-143">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c28fe-144">строка</span><span class="sxs-lookup"><span data-stu-id="c28fe-144">string</span></span><br/> | <span data-ttu-id="c28fe-145">Недоступно</span><span class="sxs-lookup"><span data-stu-id="c28fe-145">n/a</span></span><br/>        | <span data-ttu-id="c28fe-146">True, False.</span><span class="sxs-lookup"><span data-stu-id="c28fe-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c28fe-147">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="c28fe-147">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c28fe-148">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c28fe-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c28fe-149">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="c28fe-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c28fe-150">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="c28fe-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the back side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" may be printed on either side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the front side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="c28fe-151">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c28fe-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c28fe-152">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="c28fe-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




