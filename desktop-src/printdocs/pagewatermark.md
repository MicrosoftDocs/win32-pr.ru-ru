---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: d1c36c47-107c-4012-a839-1018c2652209
title: пажеватермарк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d0e0e47aa89a3cb6380a78dd49312d17f88ab8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105713355"
---
# <a name="pagewatermark"></a><span data-ttu-id="5cab3-104">пажеватермарк</span><span class="sxs-lookup"><span data-stu-id="5cab3-104">PageWatermark</span></span>

<span data-ttu-id="5cab3-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="5cab3-105">This topic is not current.</span></span> <span data-ttu-id="5cab3-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5cab3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5cab3-107">Описание настройки водяного знака для выходных данных и характеристик водяного знака.</span><span class="sxs-lookup"><span data-stu-id="5cab3-107">Describes the watermark setting of the output and the watermark characteristics.</span></span> <span data-ttu-id="5cab3-108">Водяные знаки применяются к логической странице, а не к физической странице.</span><span class="sxs-lookup"><span data-stu-id="5cab3-108">Watermarks apply to the logical page, not the physical page.</span></span> <span data-ttu-id="5cab3-109">Например, если Документдуплекс включен, на каждой странице чистки на каждом листе появится водяной знак.</span><span class="sxs-lookup"><span data-stu-id="5cab3-109">For example, if DocumentDuplex is enabled, a watermark will appear on each NUp page on each sheet.</span></span> <span data-ttu-id="5cab3-110">Если Документдуплекс, Пажеспершит = 2, то каждый лист будет иметь 2 водяных знака.</span><span class="sxs-lookup"><span data-stu-id="5cab3-110">If DocumentDuplex, PagesPerSheet=2, then each sheet will have 2 watermarks.</span></span>

-   [<span data-ttu-id="5cab3-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5cab3-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5cab3-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="5cab3-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5cab3-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5cab3-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5cab3-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5cab3-114">Element Information</span></span>



| <span data-ttu-id="5cab3-115">Имя</span><span class="sxs-lookup"><span data-stu-id="5cab3-115">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cab3-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="5cab3-116">Element Type</span></span> <br/>   | <span data-ttu-id="5cab3-117">Функция</span><span class="sxs-lookup"><span data-stu-id="5cab3-117">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="5cab3-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="5cab3-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5cab3-119">Страница</span><span class="sxs-lookup"><span data-stu-id="5cab3-119">Page</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="5cab3-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="5cab3-120">Notes</span></span> <br/>          | <span data-ttu-id="5cab3-121">Координаты задаются относительно Пажеимажеаблесизе, где источник водяного знака отсчитывается относительно начала Пажеимажеаблесизе.</span><span class="sxs-lookup"><span data-stu-id="5cab3-121">Coordinates are relative to PageImageableSize, where the origin of the watermark is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="5cab3-122">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="5cab3-122">Structural Content</span></span>

<span data-ttu-id="5cab3-123">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5cab3-123">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:PageWatermark">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Defines the width origin of the watermark. See the PageWatermarkOriginWidth ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:OriginWidth">
      <psf:ParameterRef name="psk:PageWatermarkOriginWidth" />
    </psf:ScoredProperty>
    <!-- Defines the height origin of the watermark. See the PageWatermarkOriginHeight ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:OriginHeight">
      <psf:ParameterRef name="psk:PageWatermarkOriginHeight" />
    </psf:ScoredProperty>
    <!-- Defines the transparency value of the watermark.  Transparency should be applied to all content, including transparent content. See the PageWatermarkTransparency ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:Transparency">
      <psf:ParameterRef name="psk:PageWatermarkTransparency" />
    </psf:ScoredProperty>
    <!-- Defines the angle value of the watermark.  See the PageWatermarkAngle ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:Angle">
      <psf:ParameterRef name="psk:PageWatermarkAngle" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include bitmaps.  -->
    <!-- Specifies the text font color -->
    <!-- Applicable to options that include text. Defines the sRGB color for the watermark text.  Format is ARGB: #AARRGGBB.   -->
    <psf:ScoredProperty name="psk:FontColor">
      <psf:ParameterRef name="psk:PageWatermarkTextColor" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include text.  Defines the available font sizes for the watermark text. Measured in points.-->
    <psf:ScoredProperty name="psk:FontSize">
      <psf:ParameterRef name="psk:PageWatermarkTextFontSize" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include text. Defines the text to be displayed in the watermark. -->
    <psf:ScoredProperty name="psk:Text">
      <psf:ParameterRef name="psk:PageWatermarkTextText" />
    </psf:ScoredProperty>
  </psf:Option>
  <!--Defines the layering behavior of the watermark. -->
  <psf:Feature name="psk:Layering">
    <!-- Watermark appears over page content. -->
    <psf:Option name="psk:Overlay" />
    <!-- Watermark appear under page content. -->
    <psf:Option name="psk:Underlay" />
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="5cab3-124">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="5cab3-124">Structure Variables</span></span>

<span data-ttu-id="5cab3-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="5cab3-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5cab3-126">Имя</span><span class="sxs-lookup"><span data-stu-id="5cab3-126">Name</span></span>                               | <span data-ttu-id="5cab3-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5cab3-127">Data type</span></span>         | <span data-ttu-id="5cab3-128">Unit</span><span class="sxs-lookup"><span data-stu-id="5cab3-128">Unit</span></span>                  | <span data-ttu-id="5cab3-129">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="5cab3-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5cab3-130">Сводка</span><span class="sxs-lookup"><span data-stu-id="5cab3-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5cab3-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5cab3-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5cab3-132">строка</span><span class="sxs-lookup"><span data-stu-id="5cab3-132">string</span></span><br/> | <span data-ttu-id="5cab3-133">characters</span><span class="sxs-lookup"><span data-stu-id="5cab3-133">characters</span></span><br/> | <span data-ttu-id="5cab3-134">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="5cab3-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5cab3-135">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5cab3-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5cab3-136">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="5cab3-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5cab3-137">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="5cab3-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5cab3-138">строка</span><span class="sxs-lookup"><span data-stu-id="5cab3-138">string</span></span><br/> | <span data-ttu-id="5cab3-139">Недоступно</span><span class="sxs-lookup"><span data-stu-id="5cab3-139">n/a</span></span><br/>        | <span data-ttu-id="5cab3-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="5cab3-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5cab3-141">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="5cab3-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5cab3-142">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5cab3-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5cab3-143">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="5cab3-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5cab3-144">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="5cab3-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageWatermark">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a text only watermark -->
  <psf:Option name="psk:Text">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">True</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:OriginWidth">
      <psf:ParameterRef name="psk:PageWatermarkOriginWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OriginHeight">
      <psf:ParameterRef name="psk:PageWatermarkOriginHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FontColor">
      <psf:ParameterRef name="psk:PageWatermarkTextColor" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FontSize">
      <psf:ParameterRef name="psk:PageWatermarkTextFontSize" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Text">
      <psf:ParameterRef name="psk:PageWatermarkTextText" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Transparency">
      <psf:ParameterRef name="psk:PageWatermarkTransparency" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Angle">
      <psf:ParameterRef name="psk:PageWatermarkTextAngle" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:Layering">
    <!--Specifies Overlay Layering-->
    <psf:Option name="psk:Overlay" />
    <!--Specifies Underlay Layering-->
    <psf:Option name="psk:Underlay" />
  </psf:Feature>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="5cab3-145">См. также</span><span class="sxs-lookup"><span data-stu-id="5cab3-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cab3-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="5cab3-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




