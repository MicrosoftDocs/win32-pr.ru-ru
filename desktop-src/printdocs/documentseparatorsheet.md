---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: f0b2192d-4bb7-4ba2-8dd0-35a20183ea31
title: документсепараторшит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8722e5db4f1a3bfebe8895c8a0777a849a88f11e
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351985"
---
# <a name="documentseparatorsheet"></a><span data-ttu-id="42635-104">документсепараторшит</span><span class="sxs-lookup"><span data-stu-id="42635-104">DocumentSeparatorSheet</span></span>

<span data-ttu-id="42635-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="42635-105">This topic is not current.</span></span> <span data-ttu-id="42635-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="42635-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="42635-107">Описывает использование таблицы разделителей для документа.</span><span class="sxs-lookup"><span data-stu-id="42635-107">Describes the separator sheet usage for a document.</span></span> <span data-ttu-id="42635-108">В выходных данных должны появиться таблицы разделителей, как показано в параметре, указанном ниже.</span><span class="sxs-lookup"><span data-stu-id="42635-108">Separator sheets should appear in the output as indicated by the Option specified below.</span></span>

-   [<span data-ttu-id="42635-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="42635-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="42635-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="42635-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="42635-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="42635-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="42635-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="42635-112">Element Information</span></span>



| <span data-ttu-id="42635-113">Имя</span><span class="sxs-lookup"><span data-stu-id="42635-113">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="42635-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="42635-114">Element Type</span></span> <br/>   | <span data-ttu-id="42635-115">Функция</span><span class="sxs-lookup"><span data-stu-id="42635-115">Feature</span></span><br/>  |
| <span data-ttu-id="42635-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="42635-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="42635-117">Документ</span><span class="sxs-lookup"><span data-stu-id="42635-117">Document</span></span><br/> |
| <span data-ttu-id="42635-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="42635-118">Notes</span></span> <br/>          | <span data-ttu-id="42635-119">Нет</span><span class="sxs-lookup"><span data-stu-id="42635-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="42635-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="42635-120">Structural Content</span></span>

<span data-ttu-id="42635-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="42635-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="42635-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="42635-122">Structure Variables</span></span>

<span data-ttu-id="42635-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="42635-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="42635-124">Имя</span><span class="sxs-lookup"><span data-stu-id="42635-124">Name</span></span>                               | <span data-ttu-id="42635-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="42635-125">Data type</span></span>         | <span data-ttu-id="42635-126">Unit</span><span class="sxs-lookup"><span data-stu-id="42635-126">Unit</span></span>                  | <span data-ttu-id="42635-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="42635-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="42635-128">Сводка</span><span class="sxs-lookup"><span data-stu-id="42635-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="42635-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="42635-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="42635-130">строка</span><span class="sxs-lookup"><span data-stu-id="42635-130">string</span></span><br/> | <span data-ttu-id="42635-131">characters</span><span class="sxs-lookup"><span data-stu-id="42635-131">characters</span></span><br/> | <span data-ttu-id="42635-132">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="42635-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="42635-133">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="42635-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="42635-134">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="42635-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="42635-135">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="42635-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="42635-136">строка</span><span class="sxs-lookup"><span data-stu-id="42635-136">string</span></span><br/> | <span data-ttu-id="42635-137">Недоступно</span><span class="sxs-lookup"><span data-stu-id="42635-137">n/a</span></span><br/>        | <span data-ttu-id="42635-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="42635-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="42635-139">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="42635-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="42635-140">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="42635-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="42635-141">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="42635-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="42635-142">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="42635-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="42635-143">См. также</span><span class="sxs-lookup"><span data-stu-id="42635-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42635-144">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="42635-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




