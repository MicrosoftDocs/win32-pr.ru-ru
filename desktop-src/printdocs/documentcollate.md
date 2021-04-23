---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: документколлате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b022d9c8067f330e14697932382c4c8f058a8f3
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105720835"
---
# <a name="documentcollate"></a><span data-ttu-id="7ea8c-104">документколлате</span><span class="sxs-lookup"><span data-stu-id="7ea8c-104">DocumentCollate</span></span>

<span data-ttu-id="7ea8c-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-105">This topic is not current.</span></span> <span data-ttu-id="7ea8c-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7ea8c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7ea8c-107">Описывает характеристики сортировки выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-107">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="7ea8c-108">Все страницы в каждом отдельном документе сортируются по копиям.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-108">All pages in each individual document are collated.</span></span> <span data-ttu-id="7ea8c-109">Документколлате и Жобколлатеаллдокументс являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-109">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="7ea8c-110">Поведение и реализация того, является ли реализованным только одно из этих ключевых слов, остается драйвером.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-110">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="7ea8c-111">Ниже приведены правила, которые следует соблюдать при реализации параметров сортировки.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-111">The following are the rules which should be followed for Collate implementation</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="7ea8c-112">Определение элемента и правила</span><span class="sxs-lookup"><span data-stu-id="7ea8c-112">Element Definition and Rules</span></span>

<span data-ttu-id="7ea8c-113">Необходимо сначала следовать правилам для Жобколлатеаллдокумент, а затем применить правила для Документколлате, чтобы сценарии работали.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-113">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="7ea8c-114">Обратите внимание, что в параметре преобразования PrintTicket в DEVMODE, где Жобколлатеаллдокументс не поддерживается драйвером, следует выбрать драйвер для выбора нужного поведения (Жобколлатеаллдокументс = ON или OFF).</span><span class="sxs-lookup"><span data-stu-id="7ea8c-114">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="7ea8c-115">Кроме того, выбранный вариант можно изменить в зависимости от других параметров PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-115">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="7ea8c-116">жобколлатеаллдокументс</span><span class="sxs-lookup"><span data-stu-id="7ea8c-116">JobCollateAllDocuments</span></span>

<span data-ttu-id="7ea8c-117">ON: Print (Документкопиесаллпажес) копии каждого документа, повторите Жобкопиесаллдокументс раз.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-117">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="7ea8c-118">Выкл. для каждого документа, Print (Жобкопиесаллдокументс x Документкопиесаллпажес), копируется вместе.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-118">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="7ea8c-119">документколлате</span><span class="sxs-lookup"><span data-stu-id="7ea8c-119">DocumentCollate</span></span>

<span data-ttu-id="7ea8c-120">ON: для всех копий (Жобкопиесаллдокументс x Документкопиесаллпажес) документа, напечатанных непрерывно, выполняется сортировка листов в этом документе.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-120">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="7ea8c-121">Выкл. для всех копий (Жобкопиесаллдокументс x Документкопиесаллпажес), напечатанных непрерывно, напечатайте все копии (Жобкопиесаллдокументс x Документкопиесаллпажес) каждого листа вместе.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-121">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="7ea8c-122">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7ea8c-122">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="7ea8c-123">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="7ea8c-123">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="7ea8c-124">XML-содержимое</span><span class="sxs-lookup"><span data-stu-id="7ea8c-124">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7ea8c-125">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7ea8c-125">Element Information</span></span>



| <span data-ttu-id="7ea8c-126">Имя</span><span class="sxs-lookup"><span data-stu-id="7ea8c-126">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="7ea8c-127">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="7ea8c-127">Element Type</span></span> <br/>   | <span data-ttu-id="7ea8c-128">Функция</span><span class="sxs-lookup"><span data-stu-id="7ea8c-128">Feature</span></span><br/>  |
| <span data-ttu-id="7ea8c-129">Префикс области</span><span class="sxs-lookup"><span data-stu-id="7ea8c-129">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7ea8c-130">Документ</span><span class="sxs-lookup"><span data-stu-id="7ea8c-130">Document</span></span><br/> |
| <span data-ttu-id="7ea8c-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="7ea8c-131">Notes</span></span> <br/>          | <span data-ttu-id="7ea8c-132">Нет</span><span class="sxs-lookup"><span data-stu-id="7ea8c-132">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="7ea8c-133">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="7ea8c-133">Structural Content</span></span>

<span data-ttu-id="7ea8c-134">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="7ea8c-134">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCollate">
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

## <a name="structure-variables"></a><span data-ttu-id="7ea8c-135">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="7ea8c-135">Structure Variables</span></span>

<span data-ttu-id="7ea8c-136">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-136">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7ea8c-137">Имя</span><span class="sxs-lookup"><span data-stu-id="7ea8c-137">Name</span></span>                               | <span data-ttu-id="7ea8c-138">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7ea8c-138">Data type</span></span>         | <span data-ttu-id="7ea8c-139">Unit</span><span class="sxs-lookup"><span data-stu-id="7ea8c-139">Unit</span></span>                  | <span data-ttu-id="7ea8c-140">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="7ea8c-140">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7ea8c-141">Сводка</span><span class="sxs-lookup"><span data-stu-id="7ea8c-141">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7ea8c-142">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="7ea8c-142">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7ea8c-143">строка</span><span class="sxs-lookup"><span data-stu-id="7ea8c-143">string</span></span><br/> | <span data-ttu-id="7ea8c-144">characters</span><span class="sxs-lookup"><span data-stu-id="7ea8c-144">characters</span></span><br/> | <span data-ttu-id="7ea8c-145">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="7ea8c-145">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7ea8c-146">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-146">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7ea8c-147">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-147">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="7ea8c-148">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="7ea8c-148">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7ea8c-149">строка</span><span class="sxs-lookup"><span data-stu-id="7ea8c-149">string</span></span><br/> | <span data-ttu-id="7ea8c-150">Недоступно</span><span class="sxs-lookup"><span data-stu-id="7ea8c-150">n/a</span></span><br/>        | <span data-ttu-id="7ea8c-151">True, False.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-151">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7ea8c-152">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-152">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7ea8c-153">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="7ea8c-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7ea8c-154">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7ea8c-155">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="7ea8c-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCollate">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="7ea8c-156">См. также</span><span class="sxs-lookup"><span data-stu-id="7ea8c-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ea8c-157">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="7ea8c-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




