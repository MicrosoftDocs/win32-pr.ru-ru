---
description: Сведения об элементе Пажеблаккженератионпроцессинг, который указывает поведение черного поколения при цветоделении CMYK.
ms.assetid: 4edd1fdf-9601-440d-b967-82ffa6dceeb1
title: пажеблаккженератионпроцессинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21861595917b67390857b380a416e441d454081
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408517"
---
# <a name="pageblackgenerationprocessing"></a><span data-ttu-id="9b0b3-103">пажеблаккженератионпроцессинг</span><span class="sxs-lookup"><span data-stu-id="9b0b3-103">PageBlackGenerationProcessing</span></span>

<span data-ttu-id="9b0b3-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="9b0b3-104">This topic is not current.</span></span> <span data-ttu-id="9b0b3-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9b0b3-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9b0b3-106">Задает поведение черного поколения при цветоделении CMYK.</span><span class="sxs-lookup"><span data-stu-id="9b0b3-106">Specifies black generation behavior for CMYK separations.</span></span>

-   [<span data-ttu-id="9b0b3-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9b0b3-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9b0b3-108">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="9b0b3-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9b0b3-109">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="9b0b3-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9b0b3-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9b0b3-110">Element Information</span></span>



| <span data-ttu-id="9b0b3-111">Имя</span><span class="sxs-lookup"><span data-stu-id="9b0b3-111">Name</span></span> | <span data-ttu-id="9b0b3-112">Значение</span><span class="sxs-lookup"><span data-stu-id="9b0b3-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="9b0b3-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="9b0b3-113">Element Type</span></span> <br/>   | <span data-ttu-id="9b0b3-114">Компонент</span><span class="sxs-lookup"><span data-stu-id="9b0b3-114">Feature</span></span><br/> |
| <span data-ttu-id="9b0b3-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="9b0b3-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9b0b3-116">Страница</span><span class="sxs-lookup"><span data-stu-id="9b0b3-116">Page</span></span><br/>    |
| <span data-ttu-id="9b0b3-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="9b0b3-117">Notes</span></span> <br/>          | <span data-ttu-id="9b0b3-118">Нет</span><span class="sxs-lookup"><span data-stu-id="9b0b3-118">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="9b0b3-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="9b0b3-119">Structural Content</span></span>

<span data-ttu-id="9b0b3-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="9b0b3-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
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

## <a name="structure-variables"></a><span data-ttu-id="9b0b3-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="9b0b3-121">Structure Variables</span></span>

<span data-ttu-id="9b0b3-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="9b0b3-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9b0b3-123">Имя</span><span class="sxs-lookup"><span data-stu-id="9b0b3-123">Name</span></span>                               | <span data-ttu-id="9b0b3-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9b0b3-124">Data type</span></span>         | <span data-ttu-id="9b0b3-125">Unit</span><span class="sxs-lookup"><span data-stu-id="9b0b3-125">Unit</span></span>                  | <span data-ttu-id="9b0b3-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="9b0b3-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9b0b3-127">Итоги</span><span class="sxs-lookup"><span data-stu-id="9b0b3-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9b0b3-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="9b0b3-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9b0b3-129">строка</span><span class="sxs-lookup"><span data-stu-id="9b0b3-129">string</span></span><br/> | <span data-ttu-id="9b0b3-130">characters</span><span class="sxs-lookup"><span data-stu-id="9b0b3-130">characters</span></span><br/> | <span data-ttu-id="9b0b3-131">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="9b0b3-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9b0b3-132">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9b0b3-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9b0b3-133">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="9b0b3-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9b0b3-134">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="9b0b3-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9b0b3-135">строка</span><span class="sxs-lookup"><span data-stu-id="9b0b3-135">string</span></span><br/> | <span data-ttu-id="9b0b3-136">Недоступно</span><span class="sxs-lookup"><span data-stu-id="9b0b3-136">n/a</span></span><br/>        | <span data-ttu-id="9b0b3-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="9b0b3-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9b0b3-138">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="9b0b3-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9b0b3-139">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="9b0b3-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9b0b3-140">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="9b0b3-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9b0b3-141">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="9b0b3-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
  <psf:Option name="psk:Automatic" />
  <psf:Option name="psk:Custom">
    <!-- The max allowable sum of the four ink coverages anywhere in an image. -->
    <psf:ScoredProperty name="psk:TotalInkCoverageLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit" />
    </psf:ScoredProperty>
    <!-- The maximum allowed K channel value. -->
    <psf:ScoredProperty name="psk:BlackInkLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingBlackInkLimit" />
    </psf:ScoredProperty>
    <!-- The percentage of gray component replacement to perform. -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel" />
    </psf:ScoredProperty>
    <!-- The point in the highlight to shadow range where GCR should start (100% = darkest shadow). -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart" />
    </psf:ScoredProperty>
    <!-- The extented beyond neutrals (into chromatic colors) that GCR applies.  0% = Undercolor component replacement, 100% = Gray component replacement.  -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementExtent">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent" />
    </psf:ScoredProperty>
    <!-- The shadow level below which UCA will be applied.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart" />
    </psf:ScoredProperty>
    <!-- The amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature> 
```

## <a name="related-topics"></a><span data-ttu-id="9b0b3-142">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="9b0b3-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b0b3-143">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="9b0b3-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




