---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 25dbd083-5815-4b25-bfdc-4d14f96d2b45
title: документковерфронт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd89bea06d3004b435cb55ff51612b1b91380c7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996271"
---
# <a name="documentcoverfront"></a><span data-ttu-id="e5c08-104">документковерфронт</span><span class="sxs-lookup"><span data-stu-id="e5c08-104">DocumentCoverFront</span></span>

<span data-ttu-id="e5c08-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="e5c08-105">This topic is not current.</span></span> <span data-ttu-id="e5c08-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e5c08-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e5c08-107">Описывает передний (начальный) Титульный лист.</span><span class="sxs-lookup"><span data-stu-id="e5c08-107">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="e5c08-108">Каждый документ будет иметь отдельный лист.</span><span class="sxs-lookup"><span data-stu-id="e5c08-108">Each document will have a separate sheet.</span></span> <span data-ttu-id="e5c08-109">Лист должен быть напечатан на Пажемедиасизе и Пажемедиатипе, используемый для первой страницы документа.</span><span class="sxs-lookup"><span data-stu-id="e5c08-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the document.</span></span> <span data-ttu-id="e5c08-110">Лист должен быть интегрирован в параметры обработки (например, Документдуплекс, Документнуп), как указано в указанном параметре.</span><span class="sxs-lookup"><span data-stu-id="e5c08-110">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="e5c08-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e5c08-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e5c08-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="e5c08-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e5c08-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="e5c08-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e5c08-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e5c08-114">Element Information</span></span>



| <span data-ttu-id="e5c08-115">Имя</span><span class="sxs-lookup"><span data-stu-id="e5c08-115">Name</span></span> | <span data-ttu-id="e5c08-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e5c08-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c08-117">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="e5c08-117">Element Type</span></span> <br/>   | <span data-ttu-id="e5c08-118">Компонент</span><span class="sxs-lookup"><span data-stu-id="e5c08-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e5c08-119">Префикс области</span><span class="sxs-lookup"><span data-stu-id="e5c08-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e5c08-120">Документ</span><span class="sxs-lookup"><span data-stu-id="e5c08-120">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e5c08-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="e5c08-121">Notes</span></span> <br/>          | <span data-ttu-id="e5c08-122">Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="e5c08-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="e5c08-123">Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части.</span><span class="sxs-lookup"><span data-stu-id="e5c08-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="e5c08-124">Эти параметры относятся к формату XPS.</span><span class="sxs-lookup"><span data-stu-id="e5c08-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="e5c08-125">URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="e5c08-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="e5c08-126">Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e5c08-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="e5c08-127">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="e5c08-127">Structural Content</span></span>

<span data-ttu-id="e5c08-128">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="e5c08-128">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="e5c08-129">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="e5c08-129">Structure Variables</span></span>

<span data-ttu-id="e5c08-130">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="e5c08-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e5c08-131">Имя</span><span class="sxs-lookup"><span data-stu-id="e5c08-131">Name</span></span>                               | <span data-ttu-id="e5c08-132">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e5c08-132">Data type</span></span>         | <span data-ttu-id="e5c08-133">Unit</span><span class="sxs-lookup"><span data-stu-id="e5c08-133">Unit</span></span>                  | <span data-ttu-id="e5c08-134">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="e5c08-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e5c08-135">Сводка</span><span class="sxs-lookup"><span data-stu-id="e5c08-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e5c08-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e5c08-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e5c08-137">строка</span><span class="sxs-lookup"><span data-stu-id="e5c08-137">string</span></span><br/> | <span data-ttu-id="e5c08-138">characters</span><span class="sxs-lookup"><span data-stu-id="e5c08-138">characters</span></span><br/> | <span data-ttu-id="e5c08-139">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="e5c08-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e5c08-140">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5c08-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e5c08-141">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="e5c08-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="e5c08-142">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="e5c08-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e5c08-143">строка</span><span class="sxs-lookup"><span data-stu-id="e5c08-143">string</span></span><br/> | <span data-ttu-id="e5c08-144">Недоступно</span><span class="sxs-lookup"><span data-stu-id="e5c08-144">n/a</span></span><br/>        | <span data-ttu-id="e5c08-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="e5c08-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e5c08-146">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="e5c08-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e5c08-147">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="e5c08-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e5c08-148">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="e5c08-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e5c08-149">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="e5c08-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="e5c08-150">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e5c08-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5c08-151">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="e5c08-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




