---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 64fcd03f-8e0a-498d-82ea-0c69be0a3886
title: жобколлатеаллдокументс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7d3ba5b55ece6d7237846ae8ef969c0a3d17e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998361"
---
# <a name="jobcollatealldocuments"></a><span data-ttu-id="8f123-104">жобколлатеаллдокументс</span><span class="sxs-lookup"><span data-stu-id="8f123-104">JobCollateAllDocuments</span></span>

<span data-ttu-id="8f123-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="8f123-105">This topic is not current.</span></span> <span data-ttu-id="8f123-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8f123-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8f123-107">Описывает характеристики сортировки выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8f123-107">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="8f123-108">Все документы в каждом отдельном задании сортируются по копиям.</span><span class="sxs-lookup"><span data-stu-id="8f123-108">All documents in each individual job are collated.</span></span> <span data-ttu-id="8f123-109">Документколлате и Жобколлатеаллдокументс являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="8f123-109">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="8f123-110">Поведение и реализация того, является ли реализованным только одно из этих ключевых слов, остается драйвером.</span><span class="sxs-lookup"><span data-stu-id="8f123-110">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="8f123-111">Ниже приведены правила, которые следует соблюдать при реализации параметров сортировки.</span><span class="sxs-lookup"><span data-stu-id="8f123-111">The following are the rules that should be followed for Collate implementation.</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="8f123-112">Определение элемента и правила</span><span class="sxs-lookup"><span data-stu-id="8f123-112">Element Definition and Rules</span></span>

<span data-ttu-id="8f123-113">Необходимо сначала следовать правилам для Жобколлатеаллдокумент, а затем применить правила для Документколлате, чтобы сценарии работали.</span><span class="sxs-lookup"><span data-stu-id="8f123-113">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="8f123-114">Обратите внимание, что в параметре преобразования PrintTicket в DEVMODE, где Жобколлатеаллдокументс не поддерживается драйвером, следует выбрать драйвер для выбора нужного поведения (Жобколлатеаллдокументс = ON или OFF).</span><span class="sxs-lookup"><span data-stu-id="8f123-114">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="8f123-115">Кроме того, выбранный вариант можно изменить в зависимости от других параметров PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="8f123-115">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="8f123-116">жобколлатеаллдокументс</span><span class="sxs-lookup"><span data-stu-id="8f123-116">JobCollateAllDocuments</span></span>

<span data-ttu-id="8f123-117">ON: Print (Документкопиесаллпажес) копии каждого документа, повторите Жобкопиесаллдокументс раз.</span><span class="sxs-lookup"><span data-stu-id="8f123-117">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="8f123-118">Выкл. для каждого документа, Print (Жобкопиесаллдокументс x Документкопиесаллпажес), копируется вместе.</span><span class="sxs-lookup"><span data-stu-id="8f123-118">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="8f123-119">документколлате</span><span class="sxs-lookup"><span data-stu-id="8f123-119">DocumentCollate</span></span>

<span data-ttu-id="8f123-120">ON: для всех копий (Жобкопиесаллдокументс x Документкопиесаллпажес) документа, напечатанных непрерывно, выполняется сортировка листов в этом документе.</span><span class="sxs-lookup"><span data-stu-id="8f123-120">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="8f123-121">Выкл. для всех копий (Жобкопиесаллдокументс x Документкопиесаллпажес), напечатанных непрерывно, напечатайте все копии (Жобкопиесаллдокументс x Документкопиесаллпажес) каждого листа вместе.</span><span class="sxs-lookup"><span data-stu-id="8f123-121">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="8f123-122">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8f123-122">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8f123-123">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="8f123-123">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="8f123-124">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="8f123-124">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

### <a name="element-information"></a><span data-ttu-id="8f123-125">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8f123-125">Element Information</span></span>



| <span data-ttu-id="8f123-126">Имя</span><span class="sxs-lookup"><span data-stu-id="8f123-126">Name</span></span> | <span data-ttu-id="8f123-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8f123-127">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="8f123-128">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="8f123-128">Element Type</span></span> <br/>   | <span data-ttu-id="8f123-129">Компонент</span><span class="sxs-lookup"><span data-stu-id="8f123-129">Feature</span></span><br/> |
| <span data-ttu-id="8f123-130">Префикс области</span><span class="sxs-lookup"><span data-stu-id="8f123-130">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8f123-131">Задание</span><span class="sxs-lookup"><span data-stu-id="8f123-131">Job</span></span><br/>     |
| <span data-ttu-id="8f123-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="8f123-132">Notes</span></span> <br/>          | <span data-ttu-id="8f123-133">Нет</span><span class="sxs-lookup"><span data-stu-id="8f123-133">None</span></span><br/>    |



 

### <a name="structural-content"></a><span data-ttu-id="8f123-134">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="8f123-134">Structural Content</span></span>

<span data-ttu-id="8f123-135">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="8f123-135">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
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

### <a name="structure-variables"></a><span data-ttu-id="8f123-136">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="8f123-136">Structure Variables</span></span>

<span data-ttu-id="8f123-137">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="8f123-137">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8f123-138">Имя</span><span class="sxs-lookup"><span data-stu-id="8f123-138">Name</span></span>                               | <span data-ttu-id="8f123-139">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8f123-139">Data type</span></span>         | <span data-ttu-id="8f123-140">Unit</span><span class="sxs-lookup"><span data-stu-id="8f123-140">Unit</span></span>                  | <span data-ttu-id="8f123-141">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="8f123-141">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="8f123-142">Сводка</span><span class="sxs-lookup"><span data-stu-id="8f123-142">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8f123-143">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="8f123-143">\_OptionName\_</span></span><br/>          | <span data-ttu-id="8f123-144">строка</span><span class="sxs-lookup"><span data-stu-id="8f123-144">string</span></span><br/> | <span data-ttu-id="8f123-145">characters</span><span class="sxs-lookup"><span data-stu-id="8f123-145">characters</span></span><br/> | <span data-ttu-id="8f123-146">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="8f123-146">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="8f123-147">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8f123-147">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8f123-148">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="8f123-148">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="8f123-149">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="8f123-149">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="8f123-150">строка</span><span class="sxs-lookup"><span data-stu-id="8f123-150">string</span></span><br/> | <span data-ttu-id="8f123-151">Недоступно</span><span class="sxs-lookup"><span data-stu-id="8f123-151">n/a</span></span><br/>        | <span data-ttu-id="8f123-152">True, False.</span><span class="sxs-lookup"><span data-stu-id="8f123-152">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="8f123-153">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="8f123-153">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

### <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8f123-154">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="8f123-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8f123-155">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="8f123-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8f123-156">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="8f123-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

 

 




