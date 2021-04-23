---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: cf35bb37-bf67-4e86-bfef-9838606982a5
title: пажескалинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41af04cc5657360fcc8d4b15812e9c2dd6b9fb06
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105703551"
---
# <a name="pagescaling"></a><span data-ttu-id="f0142-104">пажескалинг</span><span class="sxs-lookup"><span data-stu-id="f0142-104">PageScaling</span></span>

<span data-ttu-id="f0142-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="f0142-105">This topic is not current.</span></span> <span data-ttu-id="f0142-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f0142-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f0142-107">Описывает характеристики масштабирования выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f0142-107">Describes the scaling characteristics of the output.</span></span> <span data-ttu-id="f0142-108">Для некоторых параметров этой функции потребитель должен иметь возможность определить характеристики "измерения содержимого приложения".</span><span class="sxs-lookup"><span data-stu-id="f0142-108">Certain Options of this Feature requires the consumer to be able to determine characteristics of the "application content dimensions."</span></span> <span data-ttu-id="f0142-109">При отсутствии возможности определить эти характеристики потребитель должен по умолчанию иметь значение Identity.</span><span class="sxs-lookup"><span data-stu-id="f0142-109">In the absence of the ability to determine these characteristics, the consumer should default to the identity option.</span></span> <span data-ttu-id="f0142-110">Эти характеристики:</span><span class="sxs-lookup"><span data-stu-id="f0142-110">These characteristics are:</span></span>



|                          |                                                                                                                                                                                                                                                       |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0142-111">Размер носителя приложения</span><span class="sxs-lookup"><span data-stu-id="f0142-111">Application Media Size</span></span>   | <span data-ttu-id="f0142-112">Размеры мультимедиа, определяемые макетом приложения.</span><span class="sxs-lookup"><span data-stu-id="f0142-112">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="f0142-113">Размер носителя приложения может быть или не соответствовать Пажемедиасизе, поддерживаемому потребителем.</span><span class="sxs-lookup"><span data-stu-id="f0142-113">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="f0142-114">Размер содержимого приложения</span><span class="sxs-lookup"><span data-stu-id="f0142-114">Application Content Size</span></span> | <span data-ttu-id="f0142-115">Размеры мультимедиа, определяемые макетом приложения.</span><span class="sxs-lookup"><span data-stu-id="f0142-115">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="f0142-116">Размер носителя приложения может быть или не соответствовать Пажемедиасизе, поддерживаемому потребителем.</span><span class="sxs-lookup"><span data-stu-id="f0142-116">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="f0142-117">Размер выпуска приложения</span><span class="sxs-lookup"><span data-stu-id="f0142-117">Application Bleed Size</span></span>   | <span data-ttu-id="f0142-118">Смещение и экстент области выпуска приложения, область переполнения, используемая приложением для регистрации и разметки относительно размера носителя приложения.</span><span class="sxs-lookup"><span data-stu-id="f0142-118">The offset and extent of the application bleed area, an overflow box used by application for registration and layout, in relation to the application media size.</span></span> <span data-ttu-id="f0142-119">Область выпуска за обрез будет отличной от размера носителя приложения или равна ему.</span><span class="sxs-lookup"><span data-stu-id="f0142-119">The bleed area will be great than or equal to the application media size.</span></span><br/> |



 

-   [<span data-ttu-id="f0142-120">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f0142-120">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f0142-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="f0142-121">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f0142-122">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="f0142-122">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f0142-123">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f0142-123">Element Information</span></span>



| <span data-ttu-id="f0142-124">Имя</span><span class="sxs-lookup"><span data-stu-id="f0142-124">Name</span></span>                       |                                                                                                                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0142-125">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="f0142-125">Element Type</span></span> <br/>   | <span data-ttu-id="f0142-126">Функция</span><span class="sxs-lookup"><span data-stu-id="f0142-126">Feature</span></span><br/>                                                                                                                                                                                    |
| <span data-ttu-id="f0142-127">Префикс области</span><span class="sxs-lookup"><span data-stu-id="f0142-127">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f0142-128">Страница</span><span class="sxs-lookup"><span data-stu-id="f0142-128">Page</span></span><br/>                                                                                                                                                                                       |
| <span data-ttu-id="f0142-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="f0142-129">Notes</span></span> <br/>          | <span data-ttu-id="f0142-130">Верхняя, Нижняя, левая и правая относительные относятся к Пажеимажеаблесизе.</span><span class="sxs-lookup"><span data-stu-id="f0142-130">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span> <span data-ttu-id="f0142-131">Координаты задаются относительно Пажеимажеаблесизе, где источник — относительно начала Пажеимажеаблесизе.</span><span class="sxs-lookup"><span data-stu-id="f0142-131">Coordinates are relative to PageImageableSize, where the origin of is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="f0142-132">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="f0142-132">Structural Content</span></span>

<span data-ttu-id="f0142-133">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="f0142-133">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageScaling">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies offset of the width relative to the PageImageableSize.  
         Measured in microns. -->
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <!-- Specifies offset of the height relative to the PageImageableSize.  
         Measured in microns. -->
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for the width dimension relative to the PageImageableSize. -->
    <psf:ScoredProperty name="psk:ScaleWidth">
      <psf:ParameterRef name="psk:PageScalingScaleWidth" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for the height dimension relative to the PageImageableSize. -->
    <psf:ScoredProperty name="psk:ScaleHeight">
      <psf:ParameterRef name="psk:PageScalingScaleHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for square scaling (both dimensions are scaled equally). -->
    <psf:ScoredProperty name="psk:Scale">
      <psf:ParameterRef name="psk:PageScalingScale" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the alignment of the scaled content. -->
  <psf:Feature name="psk:ScaleOffsetAlignment">
    <!-- Specifies the scaling should be aligned on the center of the bottom edge of the media. -->
    <psf:Option name="psk:BottomCenter"/>
    <!-- Specifies the scaling should be aligned on the bottom left corner of the media. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies the scaling should be aligned on the bottom right corner of the media. -->
    <psf:Option name="psk:BottomRight "/>
    <!-- Specifies the scaling should be aligned on the bottom right corner of the media. -->
    <psf:Option name="psk:Center"/>
    <!-- Specifies the scaling should be aligned on the center of the left edge of the media. -->
    <psf:Option name="psk:LeftCenter"/>
    <!-- Specifies the scaling should be aligned on the center of the right edge of the media. -->
    <psf:Option name="psk:RightCenter"/>
    <!-- Specifies the scaling should be aligned on the center of the top edge of the media. -->
    <psf:Option name="psk:TopCenter"/>
    <!-- Specifies the scaling should be aligned on the top left corner of the media. -->
    <psf:Option name="psk:TopLeft"/>
    <!-- Specifies the scaling should be aligned on the top right corner of the media. -->
    <psf:Option name="psk:TopRight"/>
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="f0142-134">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="f0142-134">Structure Variables</span></span>

<span data-ttu-id="f0142-135">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="f0142-135">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f0142-136">Имя</span><span class="sxs-lookup"><span data-stu-id="f0142-136">Name</span></span>                               | <span data-ttu-id="f0142-137">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f0142-137">Data type</span></span>         | <span data-ttu-id="f0142-138">Unit</span><span class="sxs-lookup"><span data-stu-id="f0142-138">Unit</span></span>                  | <span data-ttu-id="f0142-139">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="f0142-139">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f0142-140">Сводка</span><span class="sxs-lookup"><span data-stu-id="f0142-140">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f0142-141">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="f0142-141">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f0142-142">строка</span><span class="sxs-lookup"><span data-stu-id="f0142-142">string</span></span><br/> | <span data-ttu-id="f0142-143">characters</span><span class="sxs-lookup"><span data-stu-id="f0142-143">characters</span></span><br/> | <span data-ttu-id="f0142-144">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="f0142-144">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f0142-145">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f0142-145">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f0142-146">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="f0142-146">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="f0142-147">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="f0142-147">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f0142-148">строка</span><span class="sxs-lookup"><span data-stu-id="f0142-148">string</span></span><br/> | <span data-ttu-id="f0142-149">Недоступно</span><span class="sxs-lookup"><span data-stu-id="f0142-149">n/a</span></span><br/>        | <span data-ttu-id="f0142-150">True, False.</span><span class="sxs-lookup"><span data-stu-id="f0142-150">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f0142-151">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="f0142-151">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f0142-152">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="f0142-152">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f0142-153">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="f0142-153">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f0142-154">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="f0142-154">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageScaling">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ScaleWidth">
      <psf:ParameterRef name="psk:PageScalingScaleWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ScaleHeight">
      <psf:ParameterRef name="psk:PageScalingScaleHeight" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom square scaling should be applied to the Application Media Size. -->
  <psf:Option name="psk:CustomSquare">
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Scale">
      <psf:ParameterRef name="psk:PageScalingScale" />
    </psf:ScoredProperty>
  </psf:Option>

  <!-- Specifies the application bleed size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationBleedSizeToPageImageableSize" />
  <!-- Specifies the application content size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationContentSizeToPageImageableSize" />
  <!-- Specifies the application media size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationMediaSizeToPageImageableSize" />
  <!-- Specifies the application media size should be scaled to the PageMediaSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationMediaSizeToPageMediaSize" />

  <!-- Specifies that no scaling should be applied. -->
  <psf:Option name="psk:None" />

  <!-- Specifies the alignment of the scaled content. -->
  <psf:Feature name="psk:ScaleOffsetAlignment">
    <!-- Specifies the scaling should be aligned on the center of the bottom edge of the media. -->
    <psf:Option name="psk:BottomCenter" />
    <!-- Specifies the scaling should be aligned on the bottom left corner of the media.-->
    <psf:Option name="psk:BottomLeft" />
    <!--Specifies the scaling should be aligned on the bottom right corner of the media.-->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies the scaling should be centered on the media.-->
    <psf:Option name="psk:Center" />
    <!-- Specifies the scaling should be aligned on the center of the left edge of the media.-->
    <psf:Option name="psk:LeftCenter" />
    <!--Specifies the scaling should be aligned on the center of the right edge of the media.-->
    <psf:Option name="psk:RightCenter" />
    <!-- Specifies the scaling should be aligned on the center of the top edge of the media.-->
    <psf:Option name="psk:TopCenter" />
    <!--  Specifies the scaling should be aligned on the top left corner of the media.-->
    <psf:Option name="psk:TopLeft" />
    <!-- Specifies the scaling should be aligned on the top right corner of the media.-->
    <psf:Option name="psk:TopRight" />
  </psf:Feature>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="f0142-155">См. также</span><span class="sxs-lookup"><span data-stu-id="f0142-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0142-156">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="f0142-156">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




