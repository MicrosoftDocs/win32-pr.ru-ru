---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: пажеимажеаблесизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1eef9012a7fda3eed6afd16add1d483c35c1111
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996111"
---
# <a name="pageimageablesize"></a><span data-ttu-id="8b105-104">пажеимажеаблесизе</span><span class="sxs-lookup"><span data-stu-id="8b105-104">PageImageableSize</span></span>

<span data-ttu-id="8b105-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="8b105-105">This topic is not current.</span></span> <span data-ttu-id="8b105-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8b105-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8b105-107">Описывает полотно с изображением для макета и отрисовки.</span><span class="sxs-lookup"><span data-stu-id="8b105-107">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="8b105-108">Это будет сообщено на основе Пажемедиасизе и Пажеориентатион.</span><span class="sxs-lookup"><span data-stu-id="8b105-108">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="8b105-109">На следующих диаграммах показаны переменные использования Пажеимажеаблесизе, основанные на Пажеориентатион.</span><span class="sxs-lookup"><span data-stu-id="8b105-109">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![Диаграмма, на которой показаны измерения страниц](images/local-1641910626-image.png)

-   [<span data-ttu-id="8b105-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8b105-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8b105-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="8b105-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="8b105-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="8b105-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8b105-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8b105-114">Element Information</span></span>



|                            |                     |
|----------------------------|---------------------|
| <span data-ttu-id="8b105-115">Имя</span><span class="sxs-lookup"><span data-stu-id="8b105-115">Name</span></span> | <span data-ttu-id="8b105-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8b105-116">Value</span></span> |
| <span data-ttu-id="8b105-117">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="8b105-117">Element Type</span></span><br/>    | <span data-ttu-id="8b105-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="8b105-118">Property</span></span><br/> |
| <span data-ttu-id="8b105-119">Префикс области</span><span class="sxs-lookup"><span data-stu-id="8b105-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8b105-120">Страница</span><span class="sxs-lookup"><span data-stu-id="8b105-120">Page</span></span><br/>     |
| <span data-ttu-id="8b105-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="8b105-121">Notes</span></span> <br/>          | <span data-ttu-id="8b105-122">Нет</span><span class="sxs-lookup"><span data-stu-id="8b105-122">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="8b105-123">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="8b105-123">Structural Content</span></span>

<span data-ttu-id="8b105-124">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="8b105-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_ImageableSizeWidthValue_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_ImageableSizeHeightValue_</psf:Value>
  </psf:Property>
  <!--Specifies the imageable area within the logical page.  -->
  <psf:Property name="psk:ImageableArea">
    <psf:Property name="psk:OriginWidth">
      <psf:Value xsi:type="xs:integer">_OriginWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_OriginHeightValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_ExtentWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_ExtentHeightValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="8b105-125">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="8b105-125">Structure Variables</span></span>

<span data-ttu-id="8b105-126">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="8b105-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8b105-127">Имя</span><span class="sxs-lookup"><span data-stu-id="8b105-127">Name</span></span>                                    | <span data-ttu-id="8b105-128">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8b105-128">Data type</span></span>          | <span data-ttu-id="8b105-129">Unit</span><span class="sxs-lookup"><span data-stu-id="8b105-129">Unit</span></span>               | <span data-ttu-id="8b105-130">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="8b105-130">Supported values</span></span>                       | <span data-ttu-id="8b105-131">Сводка</span><span class="sxs-lookup"><span data-stu-id="8b105-131">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b105-132">\_имажеаблесизевидсвалуе\_</span><span class="sxs-lookup"><span data-stu-id="8b105-132">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="8b105-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="8b105-133">integer</span></span><br/> | <span data-ttu-id="8b105-134">мкм</span><span class="sxs-lookup"><span data-stu-id="8b105-134">microns</span></span><br/> | <span data-ttu-id="8b105-135">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="8b105-135">Greater than 0.</span></span><br/>             | <span data-ttu-id="8b105-136">Задает горизонтальное измерение размера носителя приложения относительно Пажеориентатион.</span><span class="sxs-lookup"><span data-stu-id="8b105-136">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="8b105-137">\_имажеаблесизехеигхтвалуе\_</span><span class="sxs-lookup"><span data-stu-id="8b105-137">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="8b105-138">Целое число</span><span class="sxs-lookup"><span data-stu-id="8b105-138">integer</span></span><br/> | <span data-ttu-id="8b105-139">мкм</span><span class="sxs-lookup"><span data-stu-id="8b105-139">microns</span></span><br/> | <span data-ttu-id="8b105-140">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="8b105-140">Greater than 0.</span></span><br/>             | <span data-ttu-id="8b105-141">Задает вертикальное измерение размера носителя приложения относительно Пажеориентатион.</span><span class="sxs-lookup"><span data-stu-id="8b105-141">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="8b105-142">\_оригинвидсвалуе\_</span><span class="sxs-lookup"><span data-stu-id="8b105-142">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="8b105-143">Целое число</span><span class="sxs-lookup"><span data-stu-id="8b105-143">integer</span></span><br/> | <span data-ttu-id="8b105-144">мкм</span><span class="sxs-lookup"><span data-stu-id="8b105-144">microns</span></span><br/> | <span data-ttu-id="8b105-145">Больше или равно 0.</span><span class="sxs-lookup"><span data-stu-id="8b105-145">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="8b105-146">Указывает горизонтальный источник области изображения относительно размера носителя приложения.</span><span class="sxs-lookup"><span data-stu-id="8b105-146">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="8b105-147">\_оригинхеигхтвалуе\_</span><span class="sxs-lookup"><span data-stu-id="8b105-147">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="8b105-148">Целое число</span><span class="sxs-lookup"><span data-stu-id="8b105-148">integer</span></span><br/> | <span data-ttu-id="8b105-149">мкм</span><span class="sxs-lookup"><span data-stu-id="8b105-149">microns</span></span><br/> | <span data-ttu-id="8b105-150">Больше или равно 0.</span><span class="sxs-lookup"><span data-stu-id="8b105-150">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="8b105-151">Задает вертикальный источник области изображения относительно размера носителя приложения.</span><span class="sxs-lookup"><span data-stu-id="8b105-151">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="8b105-152">\_екстентвидсвалуе\_</span><span class="sxs-lookup"><span data-stu-id="8b105-152">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="8b105-153">Целое число</span><span class="sxs-lookup"><span data-stu-id="8b105-153">integer</span></span><br/> | <span data-ttu-id="8b105-154">мкм</span><span class="sxs-lookup"><span data-stu-id="8b105-154">microns</span></span><br/> | <span data-ttu-id="8b105-155">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="8b105-155">Greater than 0.</span></span><br/>             | <span data-ttu-id="8b105-156">Указывает расстояние по горизонтали между началом и ограничивающим пределом размера носителя приложения.</span><span class="sxs-lookup"><span data-stu-id="8b105-156">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="8b105-157">\_екстенсеигхтвалуе\_</span><span class="sxs-lookup"><span data-stu-id="8b105-157">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="8b105-158">Целое число</span><span class="sxs-lookup"><span data-stu-id="8b105-158">integer</span></span><br/> | <span data-ttu-id="8b105-159">мкм</span><span class="sxs-lookup"><span data-stu-id="8b105-159">microns</span></span><br/> | <span data-ttu-id="8b105-160">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="8b105-160">Greater than 0.</span></span><br/>             | <span data-ttu-id="8b105-161">Задает расстояние по вертикали между источником и ограничивающим пределом размера носителя приложения Canvas.</span><span class="sxs-lookup"><span data-stu-id="8b105-161">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8b105-162">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="8b105-162">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8b105-163">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="8b105-163">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8b105-164">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="8b105-164">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
    <psf:Property name="psk:ImageableArea">
      <psf:Property name="psk:OriginWidth">
        <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
      </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
  
```

## <a name="related-topics"></a><span data-ttu-id="8b105-165">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8b105-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b105-166">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="8b105-166">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




