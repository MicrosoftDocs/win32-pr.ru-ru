---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: пажеимажеаблесизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca243defc08b43a79e897bfa91913a954bf37
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104562229"
---
# <a name="pageimageablesize"></a><span data-ttu-id="c4188-104">пажеимажеаблесизе</span><span class="sxs-lookup"><span data-stu-id="c4188-104">PageImageableSize</span></span>

<span data-ttu-id="c4188-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="c4188-105">This topic is not current.</span></span> <span data-ttu-id="c4188-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c4188-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c4188-107">Описывает полотно с изображением для макета и отрисовки.</span><span class="sxs-lookup"><span data-stu-id="c4188-107">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="c4188-108">Это будет сообщено на основе Пажемедиасизе и Пажеориентатион.</span><span class="sxs-lookup"><span data-stu-id="c4188-108">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="c4188-109">На следующих диаграммах показаны переменные использования Пажеимажеаблесизе, основанные на Пажеориентатион.</span><span class="sxs-lookup"><span data-stu-id="c4188-109">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![Диаграмма, на которой показаны измерения страниц](images/local-1641910626-image.png)

-   [<span data-ttu-id="c4188-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c4188-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c4188-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="c4188-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c4188-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c4188-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c4188-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c4188-114">Element Information</span></span>



|                            |                     |
|----------------------------|---------------------|
| <span data-ttu-id="c4188-115">Имя</span><span class="sxs-lookup"><span data-stu-id="c4188-115">Name</span></span>                       |                     |
| <span data-ttu-id="c4188-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="c4188-116">Element Type</span></span><br/>    | <span data-ttu-id="c4188-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="c4188-117">Property</span></span><br/> |
| <span data-ttu-id="c4188-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="c4188-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c4188-119">Страница</span><span class="sxs-lookup"><span data-stu-id="c4188-119">Page</span></span><br/>     |
| <span data-ttu-id="c4188-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4188-120">Notes</span></span> <br/>          | <span data-ttu-id="c4188-121">Нет</span><span class="sxs-lookup"><span data-stu-id="c4188-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="c4188-122">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="c4188-122">Structural Content</span></span>

<span data-ttu-id="c4188-123">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="c4188-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="c4188-124">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="c4188-124">Structure Variables</span></span>

<span data-ttu-id="c4188-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="c4188-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c4188-126">Имя</span><span class="sxs-lookup"><span data-stu-id="c4188-126">Name</span></span>                                    | <span data-ttu-id="c4188-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c4188-127">Data type</span></span>          | <span data-ttu-id="c4188-128">Unit</span><span class="sxs-lookup"><span data-stu-id="c4188-128">Unit</span></span>               | <span data-ttu-id="c4188-129">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="c4188-129">Supported values</span></span>                       | <span data-ttu-id="c4188-130">Сводка</span><span class="sxs-lookup"><span data-stu-id="c4188-130">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4188-131">\_имажеаблесизевидсвалуе\_</span><span class="sxs-lookup"><span data-stu-id="c4188-131">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="c4188-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="c4188-132">integer</span></span><br/> | <span data-ttu-id="c4188-133">мкм</span><span class="sxs-lookup"><span data-stu-id="c4188-133">microns</span></span><br/> | <span data-ttu-id="c4188-134">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="c4188-134">Greater than 0.</span></span><br/>             | <span data-ttu-id="c4188-135">Задает горизонтальное измерение размера носителя приложения относительно Пажеориентатион.</span><span class="sxs-lookup"><span data-stu-id="c4188-135">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="c4188-136">\_имажеаблесизехеигхтвалуе\_</span><span class="sxs-lookup"><span data-stu-id="c4188-136">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="c4188-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="c4188-137">integer</span></span><br/> | <span data-ttu-id="c4188-138">мкм</span><span class="sxs-lookup"><span data-stu-id="c4188-138">microns</span></span><br/> | <span data-ttu-id="c4188-139">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="c4188-139">Greater than 0.</span></span><br/>             | <span data-ttu-id="c4188-140">Задает вертикальное измерение размера носителя приложения относительно Пажеориентатион.</span><span class="sxs-lookup"><span data-stu-id="c4188-140">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="c4188-141">\_оригинвидсвалуе\_</span><span class="sxs-lookup"><span data-stu-id="c4188-141">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="c4188-142">Целое число</span><span class="sxs-lookup"><span data-stu-id="c4188-142">integer</span></span><br/> | <span data-ttu-id="c4188-143">мкм</span><span class="sxs-lookup"><span data-stu-id="c4188-143">microns</span></span><br/> | <span data-ttu-id="c4188-144">Больше или равно 0.</span><span class="sxs-lookup"><span data-stu-id="c4188-144">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="c4188-145">Указывает горизонтальный источник области изображения относительно размера носителя приложения.</span><span class="sxs-lookup"><span data-stu-id="c4188-145">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="c4188-146">\_оригинхеигхтвалуе\_</span><span class="sxs-lookup"><span data-stu-id="c4188-146">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="c4188-147">Целое число</span><span class="sxs-lookup"><span data-stu-id="c4188-147">integer</span></span><br/> | <span data-ttu-id="c4188-148">мкм</span><span class="sxs-lookup"><span data-stu-id="c4188-148">microns</span></span><br/> | <span data-ttu-id="c4188-149">Больше или равно 0.</span><span class="sxs-lookup"><span data-stu-id="c4188-149">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="c4188-150">Задает вертикальный источник области изображения относительно размера носителя приложения.</span><span class="sxs-lookup"><span data-stu-id="c4188-150">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="c4188-151">\_екстентвидсвалуе\_</span><span class="sxs-lookup"><span data-stu-id="c4188-151">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="c4188-152">Целое число</span><span class="sxs-lookup"><span data-stu-id="c4188-152">integer</span></span><br/> | <span data-ttu-id="c4188-153">мкм</span><span class="sxs-lookup"><span data-stu-id="c4188-153">microns</span></span><br/> | <span data-ttu-id="c4188-154">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="c4188-154">Greater than 0.</span></span><br/>             | <span data-ttu-id="c4188-155">Указывает расстояние по горизонтали между началом и ограничивающим пределом размера носителя приложения.</span><span class="sxs-lookup"><span data-stu-id="c4188-155">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="c4188-156">\_екстенсеигхтвалуе\_</span><span class="sxs-lookup"><span data-stu-id="c4188-156">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="c4188-157">Целое число</span><span class="sxs-lookup"><span data-stu-id="c4188-157">integer</span></span><br/> | <span data-ttu-id="c4188-158">мкм</span><span class="sxs-lookup"><span data-stu-id="c4188-158">microns</span></span><br/> | <span data-ttu-id="c4188-159">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="c4188-159">Greater than 0.</span></span><br/>             | <span data-ttu-id="c4188-160">Задает расстояние по вертикали между источником и ограничивающим пределом размера носителя приложения Canvas.</span><span class="sxs-lookup"><span data-stu-id="c4188-160">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c4188-161">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c4188-161">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c4188-162">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="c4188-162">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c4188-163">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="c4188-163">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="c4188-164">См. также</span><span class="sxs-lookup"><span data-stu-id="c4188-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4188-165">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="c4188-165">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




