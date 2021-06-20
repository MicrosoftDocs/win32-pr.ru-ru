---
description: Сведения об элементе Документбиндинг, описывающем метод привязки. Документбиндинг и Жоббиндаллдокументс являются взаимоисключающими.
ms.assetid: 36a7c360-2d26-46b9-b829-0fb35b36c79c
title: документбиндинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf2b8f44c90cdef37a6599bf25904949748c82ba
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409467"
---
# <a name="documentbinding"></a><span data-ttu-id="d49a4-104">документбиндинг</span><span class="sxs-lookup"><span data-stu-id="d49a4-104">DocumentBinding</span></span>

<span data-ttu-id="d49a4-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="d49a4-105">This topic is not current.</span></span> <span data-ttu-id="d49a4-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d49a4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d49a4-107">Описывает метод привязки.</span><span class="sxs-lookup"><span data-stu-id="d49a4-107">Describes the method of binding.</span></span> <span data-ttu-id="d49a4-108">Каждый документ привязывается отдельно.</span><span class="sxs-lookup"><span data-stu-id="d49a4-108">Each document is bound separately.</span></span> <span data-ttu-id="d49a4-109">Документбиндинг и Жоббиндаллдокументс являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="d49a4-109">DocumentBinding and JobBindAllDocuments are mutually exclusive.</span></span> <span data-ttu-id="d49a4-110">Драйвер определяет обработку ограничений между ключевыми словами.</span><span class="sxs-lookup"><span data-stu-id="d49a4-110">It is up to the driver to determine constraint handling between keywords.</span></span>

-   [<span data-ttu-id="d49a4-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d49a4-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d49a4-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="d49a4-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d49a4-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="d49a4-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d49a4-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d49a4-114">Element Information</span></span>



| <span data-ttu-id="d49a4-115">Имя</span><span class="sxs-lookup"><span data-stu-id="d49a4-115">Name</span></span> | <span data-ttu-id="d49a4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d49a4-116">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d49a4-117">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="d49a4-117">Element Type</span></span> <br/>   | <span data-ttu-id="d49a4-118">Компонент</span><span class="sxs-lookup"><span data-stu-id="d49a4-118">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="d49a4-119">Префикс области</span><span class="sxs-lookup"><span data-stu-id="d49a4-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d49a4-120">Документ</span><span class="sxs-lookup"><span data-stu-id="d49a4-120">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="d49a4-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="d49a4-121">Notes</span></span> <br/>          | <span data-ttu-id="d49a4-122">Верхние, нижние, левые и правая относятся относительно Пажеимажеаблесизе, где Топлефт обозначается исходными значениями оси x и оси y.</span><span class="sxs-lookup"><span data-stu-id="d49a4-122">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="d49a4-123">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="d49a4-123">Structural Content</span></span>

<span data-ttu-id="d49a4-124">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d49a4-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBinding">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:Value xsi:type="xs:integer">_BindingGutterValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="d49a4-125">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="d49a4-125">Structure Variables</span></span>

<span data-ttu-id="d49a4-126">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="d49a4-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d49a4-127">Имя</span><span class="sxs-lookup"><span data-stu-id="d49a4-127">Name</span></span>                               | <span data-ttu-id="d49a4-128">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d49a4-128">Data type</span></span>          | <span data-ttu-id="d49a4-129">Unit</span><span class="sxs-lookup"><span data-stu-id="d49a4-129">Unit</span></span>                  | <span data-ttu-id="d49a4-130">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="d49a4-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="d49a4-131">Итоги</span><span class="sxs-lookup"><span data-stu-id="d49a4-131">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d49a4-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="d49a4-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="d49a4-133">строка</span><span class="sxs-lookup"><span data-stu-id="d49a4-133">string</span></span><br/>  | <span data-ttu-id="d49a4-134">characters</span><span class="sxs-lookup"><span data-stu-id="d49a4-134">characters</span></span><br/> | <span data-ttu-id="d49a4-135">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="d49a4-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="d49a4-136">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d49a4-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="d49a4-137">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="d49a4-137">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="d49a4-138">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="d49a4-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="d49a4-139">строка</span><span class="sxs-lookup"><span data-stu-id="d49a4-139">string</span></span><br/>  | <span data-ttu-id="d49a4-140">Недоступно</span><span class="sxs-lookup"><span data-stu-id="d49a4-140">n/a</span></span><br/>        | <span data-ttu-id="d49a4-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="d49a4-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="d49a4-142">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="d49a4-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="d49a4-143">\_биндинггуттервалуе\_</span><span class="sxs-lookup"><span data-stu-id="d49a4-143">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="d49a4-144">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="d49a4-144">Integer</span></span><br/> | <span data-ttu-id="d49a4-145">мкм</span><span class="sxs-lookup"><span data-stu-id="d49a4-145">microns</span></span><br/>    | <span data-ttu-id="d49a4-146">Больше или равно 0.</span><span class="sxs-lookup"><span data-stu-id="d49a4-146">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="d49a4-147">Определяет минимальную внутреннюю область привязки для указанной законченной привязки.</span><span class="sxs-lookup"><span data-stu-id="d49a4-147">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="d49a4-148">Внутреннее поле измеряется в микронах по отношению к границе физического измерения носителя.</span><span class="sxs-lookup"><span data-stu-id="d49a4-148">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d49a4-149">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="d49a4-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d49a4-150">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="d49a4-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d49a4-151">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="d49a4-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBinding">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies bale binding. -->
  <psf:Option name="psk:Bale" >
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the bottom edge. -->
  <psf:Option name="psk:BindBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the left edge. -->
  <psf:Option name="psk:BindLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the right edge. -->
  <psf:Option name="psk:BindRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the top edge. -->
  <psf:Option name="psk:BindTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies booklet binding. -->
  <psf:Option name="psk:Booklet" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the bottom edge. -->
  <psf:Option name="psk:EdgeStitchBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the left edge. -->
  <psf:Option name="psk:EdgeStitchLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the right edge. -->
  <psf:Option name="psk:EdgeStitchRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the top edge. -->
  <psf:Option name="psk:EdgeStitchTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a folded binding. -->
  <psf:Option name="psk:Fold" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies jog offset binding. -->
  <psf:Option name="psk:JogOffset" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies trimming binding. -->
  <psf:Option name="psk:Trim" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no binding. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="d49a4-152">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d49a4-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d49a4-153">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="d49a4-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




