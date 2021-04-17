---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 36a7c360-2d26-46b9-b829-0fb35b36c79c
title: документбиндинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 139cc40701624041a57e4fa69edc084f88c1972b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105713348"
---
# <a name="documentbinding"></a><span data-ttu-id="17f93-104">документбиндинг</span><span class="sxs-lookup"><span data-stu-id="17f93-104">DocumentBinding</span></span>

<span data-ttu-id="17f93-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="17f93-105">This topic is not current.</span></span> <span data-ttu-id="17f93-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="17f93-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="17f93-107">Описывает метод привязки.</span><span class="sxs-lookup"><span data-stu-id="17f93-107">Describes the method of binding.</span></span> <span data-ttu-id="17f93-108">Каждый документ привязывается отдельно.</span><span class="sxs-lookup"><span data-stu-id="17f93-108">Each document is bound separately.</span></span> <span data-ttu-id="17f93-109">Документбиндинг и Жоббиндаллдокументс являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="17f93-109">DocumentBinding and JobBindAllDocuments are mutually exclusive.</span></span> <span data-ttu-id="17f93-110">Драйвер определяет обработку ограничений между ключевыми словами.</span><span class="sxs-lookup"><span data-stu-id="17f93-110">It is up to the driver to determine constraint handling between keywords.</span></span>

-   [<span data-ttu-id="17f93-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="17f93-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="17f93-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="17f93-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="17f93-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="17f93-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="17f93-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="17f93-114">Element Information</span></span>



| <span data-ttu-id="17f93-115">Имя</span><span class="sxs-lookup"><span data-stu-id="17f93-115">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17f93-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="17f93-116">Element Type</span></span> <br/>   | <span data-ttu-id="17f93-117">Функция</span><span class="sxs-lookup"><span data-stu-id="17f93-117">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="17f93-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="17f93-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="17f93-119">Документ</span><span class="sxs-lookup"><span data-stu-id="17f93-119">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="17f93-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="17f93-120">Notes</span></span> <br/>          | <span data-ttu-id="17f93-121">Верхние, нижние, левые и правая относятся относительно Пажеимажеаблесизе, где Топлефт обозначается исходными значениями оси x и оси y.</span><span class="sxs-lookup"><span data-stu-id="17f93-121">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="17f93-122">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="17f93-122">Structural Content</span></span>

<span data-ttu-id="17f93-123">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="17f93-123">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="17f93-124">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="17f93-124">Structure Variables</span></span>

<span data-ttu-id="17f93-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="17f93-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="17f93-126">Имя</span><span class="sxs-lookup"><span data-stu-id="17f93-126">Name</span></span>                               | <span data-ttu-id="17f93-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="17f93-127">Data type</span></span>          | <span data-ttu-id="17f93-128">Unit</span><span class="sxs-lookup"><span data-stu-id="17f93-128">Unit</span></span>                  | <span data-ttu-id="17f93-129">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="17f93-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="17f93-130">Сводка</span><span class="sxs-lookup"><span data-stu-id="17f93-130">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17f93-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="17f93-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="17f93-132">строка</span><span class="sxs-lookup"><span data-stu-id="17f93-132">string</span></span><br/>  | <span data-ttu-id="17f93-133">characters</span><span class="sxs-lookup"><span data-stu-id="17f93-133">characters</span></span><br/> | <span data-ttu-id="17f93-134">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="17f93-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="17f93-135">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="17f93-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="17f93-136">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="17f93-136">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="17f93-137">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="17f93-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="17f93-138">строка</span><span class="sxs-lookup"><span data-stu-id="17f93-138">string</span></span><br/>  | <span data-ttu-id="17f93-139">Недоступно</span><span class="sxs-lookup"><span data-stu-id="17f93-139">n/a</span></span><br/>        | <span data-ttu-id="17f93-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="17f93-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="17f93-141">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="17f93-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="17f93-142">\_биндинггуттервалуе\_</span><span class="sxs-lookup"><span data-stu-id="17f93-142">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="17f93-143">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="17f93-143">Integer</span></span><br/> | <span data-ttu-id="17f93-144">мкм</span><span class="sxs-lookup"><span data-stu-id="17f93-144">microns</span></span><br/>    | <span data-ttu-id="17f93-145">Больше или равно 0.</span><span class="sxs-lookup"><span data-stu-id="17f93-145">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="17f93-146">Определяет минимальную внутреннюю область привязки для указанной законченной привязки.</span><span class="sxs-lookup"><span data-stu-id="17f93-146">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="17f93-147">Внутреннее поле измеряется в микронах по отношению к границе физического измерения носителя.</span><span class="sxs-lookup"><span data-stu-id="17f93-147">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="17f93-148">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="17f93-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="17f93-149">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="17f93-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="17f93-150">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="17f93-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="17f93-151">См. также</span><span class="sxs-lookup"><span data-stu-id="17f93-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17f93-152">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="17f93-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




