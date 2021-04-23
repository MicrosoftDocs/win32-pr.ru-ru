---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 25dbd083-5815-4b25-bfdc-4d14f96d2b45
title: документковерфронт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b143ea6a3e1edd667d56619c190d99d1de93496f
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105713347"
---
# <a name="documentcoverfront"></a><span data-ttu-id="5d34f-104">документковерфронт</span><span class="sxs-lookup"><span data-stu-id="5d34f-104">DocumentCoverFront</span></span>

<span data-ttu-id="5d34f-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="5d34f-105">This topic is not current.</span></span> <span data-ttu-id="5d34f-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5d34f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5d34f-107">Описывает передний (начальный) Титульный лист.</span><span class="sxs-lookup"><span data-stu-id="5d34f-107">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="5d34f-108">Каждый документ будет иметь отдельный лист.</span><span class="sxs-lookup"><span data-stu-id="5d34f-108">Each document will have a separate sheet.</span></span> <span data-ttu-id="5d34f-109">Лист должен быть напечатан на Пажемедиасизе и Пажемедиатипе, используемый для первой страницы документа.</span><span class="sxs-lookup"><span data-stu-id="5d34f-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the document.</span></span> <span data-ttu-id="5d34f-110">Лист должен быть интегрирован в параметры обработки (например, Документдуплекс, Документнуп), как указано в указанном параметре.</span><span class="sxs-lookup"><span data-stu-id="5d34f-110">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="5d34f-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5d34f-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5d34f-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="5d34f-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5d34f-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5d34f-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5d34f-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5d34f-114">Element Information</span></span>



| <span data-ttu-id="5d34f-115">Имя</span><span class="sxs-lookup"><span data-stu-id="5d34f-115">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d34f-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="5d34f-116">Element Type</span></span> <br/>   | <span data-ttu-id="5d34f-117">Функция</span><span class="sxs-lookup"><span data-stu-id="5d34f-117">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="5d34f-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="5d34f-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5d34f-119">Документ</span><span class="sxs-lookup"><span data-stu-id="5d34f-119">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="5d34f-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="5d34f-120">Notes</span></span> <br/>          | <span data-ttu-id="5d34f-121">Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="5d34f-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="5d34f-122">Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части.</span><span class="sxs-lookup"><span data-stu-id="5d34f-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="5d34f-123">Эти параметры относятся к формату XPS.</span><span class="sxs-lookup"><span data-stu-id="5d34f-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="5d34f-124">URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="5d34f-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="5d34f-125">Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5d34f-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="5d34f-126">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="5d34f-126">Structural Content</span></span>

<span data-ttu-id="5d34f-127">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="5d34f-127">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="5d34f-128">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="5d34f-128">Structure Variables</span></span>

<span data-ttu-id="5d34f-129">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="5d34f-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5d34f-130">Имя</span><span class="sxs-lookup"><span data-stu-id="5d34f-130">Name</span></span>                               | <span data-ttu-id="5d34f-131">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5d34f-131">Data type</span></span>         | <span data-ttu-id="5d34f-132">Unit</span><span class="sxs-lookup"><span data-stu-id="5d34f-132">Unit</span></span>                  | <span data-ttu-id="5d34f-133">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="5d34f-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5d34f-134">Сводка</span><span class="sxs-lookup"><span data-stu-id="5d34f-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5d34f-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5d34f-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5d34f-136">строка</span><span class="sxs-lookup"><span data-stu-id="5d34f-136">string</span></span><br/> | <span data-ttu-id="5d34f-137">characters</span><span class="sxs-lookup"><span data-stu-id="5d34f-137">characters</span></span><br/> | <span data-ttu-id="5d34f-138">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="5d34f-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5d34f-139">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5d34f-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5d34f-140">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="5d34f-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5d34f-141">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="5d34f-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5d34f-142">строка</span><span class="sxs-lookup"><span data-stu-id="5d34f-142">string</span></span><br/> | <span data-ttu-id="5d34f-143">Недоступно</span><span class="sxs-lookup"><span data-stu-id="5d34f-143">n/a</span></span><br/>        | <span data-ttu-id="5d34f-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="5d34f-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5d34f-145">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="5d34f-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5d34f-146">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5d34f-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5d34f-147">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="5d34f-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5d34f-148">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="5d34f-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="5d34f-149">См. также</span><span class="sxs-lookup"><span data-stu-id="5d34f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d34f-150">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="5d34f-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




