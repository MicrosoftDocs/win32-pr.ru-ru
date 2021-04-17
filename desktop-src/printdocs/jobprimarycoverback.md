---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 83626e3c-1ce8-4c91-b656-9f0c06c5b1ec
title: жобпримариковербакк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073e65f80c3bee31423d0cf813d454a32e6f559b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105693942"
---
# <a name="jobprimarycoverback"></a><span data-ttu-id="7a398-104">жобпримариковербакк</span><span class="sxs-lookup"><span data-stu-id="7a398-104">JobPrimaryCoverBack</span></span>

<span data-ttu-id="7a398-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="7a398-105">This topic is not current.</span></span> <span data-ttu-id="7a398-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7a398-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7a398-107">Описывает заднюю (конечную) обложку листа.</span><span class="sxs-lookup"><span data-stu-id="7a398-107">Describes the back (ending) cover sheet.</span></span> <span data-ttu-id="7a398-108">Каждое задание будет иметь отдельный первичный лист.</span><span class="sxs-lookup"><span data-stu-id="7a398-108">Each job will have a separate primary sheet.</span></span> <span data-ttu-id="7a398-109">Лист должен быть напечатан на Пажемедиасизе и Пажемедиатипе, используемый для последней страницы задания.</span><span class="sxs-lookup"><span data-stu-id="7a398-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the final page of the job.</span></span> <span data-ttu-id="7a398-110">Лист должен быть интегрирован в параметры обработки (например, Жобдуплексаллдокументсконтигуаусли, Жобнупаллдокументсконтигуаусли), как указано в указанном параметре.</span><span class="sxs-lookup"><span data-stu-id="7a398-110">The cover sheet should be integrated into processing options (such as JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="7a398-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7a398-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7a398-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="7a398-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7a398-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="7a398-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7a398-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7a398-114">Element Information</span></span>



| <span data-ttu-id="7a398-115">Имя</span><span class="sxs-lookup"><span data-stu-id="7a398-115">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a398-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="7a398-116">Element Type</span></span> <br/>   | <span data-ttu-id="7a398-117">Функция</span><span class="sxs-lookup"><span data-stu-id="7a398-117">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="7a398-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="7a398-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7a398-119">Задание</span><span class="sxs-lookup"><span data-stu-id="7a398-119">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="7a398-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="7a398-120">Notes</span></span> <br/>          | <span data-ttu-id="7a398-121">Потребители, совместимые с XPS, должны обеспечить, чтобы ссылка URI для ресурса, такого как изображение или цветовой профиль в документе возможностей печати или PrintTicket, ссылалась на имя части (относительный URI для корня пакета) в том же пакете документа XPS, который содержит итоговый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="7a398-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="7a398-122">Совместимый потребитель XPS не должен использовать URI, который не соответствует синтаксису имени части.</span><span class="sxs-lookup"><span data-stu-id="7a398-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="7a398-123">Эти параметры относятся к формату XPS.</span><span class="sxs-lookup"><span data-stu-id="7a398-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="7a398-124">URI, на которые есть ссылки в документе возможностей печати или PrintTicket, не должны разрешаться как URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="7a398-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="7a398-125">Это небезопасно, так как они могут не распознаться должным образом и могут создавать опасные риски безопасности для драйвера и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7a398-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="7a398-126">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="7a398-126">Structural Content</span></span>

<span data-ttu-id="7a398-127">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="7a398-127">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
  <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  <!-- Specifies the XPS part name for the back cover sheet. -->
  <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="7a398-128">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="7a398-128">Structure Variables</span></span>

<span data-ttu-id="7a398-129">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="7a398-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7a398-130">Имя</span><span class="sxs-lookup"><span data-stu-id="7a398-130">Name</span></span>                               | <span data-ttu-id="7a398-131">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7a398-131">Data type</span></span>         | <span data-ttu-id="7a398-132">Unit</span><span class="sxs-lookup"><span data-stu-id="7a398-132">Unit</span></span>                  | <span data-ttu-id="7a398-133">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="7a398-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7a398-134">Сводка</span><span class="sxs-lookup"><span data-stu-id="7a398-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7a398-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="7a398-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7a398-136">строка</span><span class="sxs-lookup"><span data-stu-id="7a398-136">string</span></span><br/> | <span data-ttu-id="7a398-137">characters</span><span class="sxs-lookup"><span data-stu-id="7a398-137">characters</span></span><br/> | <span data-ttu-id="7a398-138">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="7a398-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7a398-139">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7a398-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7a398-140">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="7a398-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="7a398-141">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="7a398-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7a398-142">строка</span><span class="sxs-lookup"><span data-stu-id="7a398-142">string</span></span><br/> | <span data-ttu-id="7a398-143">Недоступно</span><span class="sxs-lookup"><span data-stu-id="7a398-143">n/a</span></span><br/>        | <span data-ttu-id="7a398-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="7a398-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7a398-145">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="7a398-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7a398-146">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="7a398-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7a398-147">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="7a398-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7a398-148">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="7a398-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the back side 
       of the cover sheet.  If a JobPrimaryCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" may be printed on either sides 
       of the cover sheet.  If a JobPrimaryCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the front side 
       of the cover sheet.  If a JobPrimaryCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="7a398-149">См. также</span><span class="sxs-lookup"><span data-stu-id="7a398-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a398-150">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="7a398-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




