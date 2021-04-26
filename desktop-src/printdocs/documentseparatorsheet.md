---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: f0b2192d-4bb7-4ba2-8dd0-35a20183ea31
title: документсепараторшит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6bd0d58c5b361b167d22c672b7e080e4498d3e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997061"
---
# <a name="documentseparatorsheet"></a><span data-ttu-id="84c02-104">документсепараторшит</span><span class="sxs-lookup"><span data-stu-id="84c02-104">DocumentSeparatorSheet</span></span>

<span data-ttu-id="84c02-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="84c02-105">This topic is not current.</span></span> <span data-ttu-id="84c02-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="84c02-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="84c02-107">Описывает использование таблицы разделителей для документа.</span><span class="sxs-lookup"><span data-stu-id="84c02-107">Describes the separator sheet usage for a document.</span></span> <span data-ttu-id="84c02-108">В выходных данных должны появиться таблицы разделителей, как показано в параметре, указанном ниже.</span><span class="sxs-lookup"><span data-stu-id="84c02-108">Separator sheets should appear in the output as indicated by the Option specified below.</span></span>

-   [<span data-ttu-id="84c02-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="84c02-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="84c02-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="84c02-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="84c02-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="84c02-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="84c02-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="84c02-112">Element Information</span></span>



| <span data-ttu-id="84c02-113">Имя</span><span class="sxs-lookup"><span data-stu-id="84c02-113">Name</span></span> | <span data-ttu-id="84c02-114">Значение</span><span class="sxs-lookup"><span data-stu-id="84c02-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="84c02-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="84c02-115">Element Type</span></span> <br/>   | <span data-ttu-id="84c02-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="84c02-116">Feature</span></span><br/>  |
| <span data-ttu-id="84c02-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="84c02-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="84c02-118">Документ</span><span class="sxs-lookup"><span data-stu-id="84c02-118">Document</span></span><br/> |
| <span data-ttu-id="84c02-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="84c02-119">Notes</span></span> <br/>          | <span data-ttu-id="84c02-120">Нет</span><span class="sxs-lookup"><span data-stu-id="84c02-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="84c02-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="84c02-121">Structural Content</span></span>

<span data-ttu-id="84c02-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="84c02-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentSeparatorSheet">
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

## <a name="structure-variables"></a><span data-ttu-id="84c02-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="84c02-123">Structure Variables</span></span>

<span data-ttu-id="84c02-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="84c02-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="84c02-125">Имя</span><span class="sxs-lookup"><span data-stu-id="84c02-125">Name</span></span>                               | <span data-ttu-id="84c02-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="84c02-126">Data type</span></span>         | <span data-ttu-id="84c02-127">Unit</span><span class="sxs-lookup"><span data-stu-id="84c02-127">Unit</span></span>                  | <span data-ttu-id="84c02-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="84c02-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="84c02-129">Сводка</span><span class="sxs-lookup"><span data-stu-id="84c02-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="84c02-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="84c02-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="84c02-131">строка</span><span class="sxs-lookup"><span data-stu-id="84c02-131">string</span></span><br/> | <span data-ttu-id="84c02-132">characters</span><span class="sxs-lookup"><span data-stu-id="84c02-132">characters</span></span><br/> | <span data-ttu-id="84c02-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="84c02-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="84c02-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84c02-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="84c02-135">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="84c02-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="84c02-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="84c02-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="84c02-137">строка</span><span class="sxs-lookup"><span data-stu-id="84c02-137">string</span></span><br/> | <span data-ttu-id="84c02-138">Недоступно</span><span class="sxs-lookup"><span data-stu-id="84c02-138">n/a</span></span><br/>        | <span data-ttu-id="84c02-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="84c02-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="84c02-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="84c02-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="84c02-141">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="84c02-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="84c02-142">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="84c02-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="84c02-143">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="84c02-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentSeparatorSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a separator sheet at the start and end of the document. -->
  <psf:Option name="psk:BothSheets" />
  <!-- Specifies a separator sheet at the end of the document. -->
  <psf:Option name="psk:EndSheet" />
  <!-- Specifies no separator sheet(s). -->
  <psf:Option name="psk:None" />
  <!-- Specifies a separator sheet at the start of the document. -->
  <psf:Option name="psk:StartSheet" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="84c02-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="84c02-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84c02-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="84c02-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




