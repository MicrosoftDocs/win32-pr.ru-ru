---
description: Сведения об элементе Пажеимажеаблесизе, настраиваемом пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: пажеимажеаблесизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4e44bc9afe33b87d32b43c93eafc3b6d4ba4b0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395309"
---
# <a name="pageimageablesize"></a><span data-ttu-id="4491c-105">пажеимажеаблесизе</span><span class="sxs-lookup"><span data-stu-id="4491c-105">PageImageableSize</span></span>

<span data-ttu-id="4491c-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="4491c-106">This topic is not current.</span></span> <span data-ttu-id="4491c-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4491c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4491c-108">Описывает полотно с изображением для макета и отрисовки.</span><span class="sxs-lookup"><span data-stu-id="4491c-108">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="4491c-109">Это будет сообщено на основе Пажемедиасизе и Пажеориентатион.</span><span class="sxs-lookup"><span data-stu-id="4491c-109">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="4491c-110">На следующих диаграммах показаны переменные использования Пажеимажеаблесизе, основанные на Пажеориентатион.</span><span class="sxs-lookup"><span data-stu-id="4491c-110">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![Диаграмма, на которой показаны измерения страниц](images/local-1641910626-image.png)

-   [<span data-ttu-id="4491c-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4491c-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4491c-113">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="4491c-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="4491c-114">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="4491c-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4491c-115">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4491c-115">Element Information</span></span>

| <span data-ttu-id="4491c-116">Имя</span><span class="sxs-lookup"><span data-stu-id="4491c-116">Name</span></span>                 | <span data-ttu-id="4491c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4491c-117">Value</span></span>         |
|----------------------|---------------|
| <span data-ttu-id="4491c-118">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="4491c-118">Element Type</span></span><br/>    | <span data-ttu-id="4491c-119">Свойство</span><span class="sxs-lookup"><span data-stu-id="4491c-119">Property</span></span><br/> |
| <span data-ttu-id="4491c-120">Префикс области</span><span class="sxs-lookup"><span data-stu-id="4491c-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4491c-121">Страница</span><span class="sxs-lookup"><span data-stu-id="4491c-121">Page</span></span><br/>     |
| <span data-ttu-id="4491c-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="4491c-122">Notes</span></span> <br/>          | <span data-ttu-id="4491c-123">Нет</span><span class="sxs-lookup"><span data-stu-id="4491c-123">None</span></span><br/>     |

## <a name="structural-content"></a><span data-ttu-id="4491c-124">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="4491c-124">Structural Content</span></span>

<span data-ttu-id="4491c-125">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="4491c-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="4491c-126">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="4491c-126">Structure Variables</span></span>

<span data-ttu-id="4491c-127">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="4491c-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4491c-128">Имя</span><span class="sxs-lookup"><span data-stu-id="4491c-128">Name</span></span>                                    | <span data-ttu-id="4491c-129">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4491c-129">Data type</span></span>          | <span data-ttu-id="4491c-130">Unit</span><span class="sxs-lookup"><span data-stu-id="4491c-130">Unit</span></span>               | <span data-ttu-id="4491c-131">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="4491c-131">Supported values</span></span>                       | <span data-ttu-id="4491c-132">Итоги</span><span class="sxs-lookup"><span data-stu-id="4491c-132">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4491c-133">\_имажеаблесизевидсвалуе\_</span><span class="sxs-lookup"><span data-stu-id="4491c-133">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="4491c-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="4491c-134">integer</span></span><br/> | <span data-ttu-id="4491c-135">мкм</span><span class="sxs-lookup"><span data-stu-id="4491c-135">microns</span></span><br/> | <span data-ttu-id="4491c-136">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="4491c-136">Greater than 0.</span></span><br/>             | <span data-ttu-id="4491c-137">Задает горизонтальное измерение размера носителя приложения относительно Пажеориентатион.</span><span class="sxs-lookup"><span data-stu-id="4491c-137">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="4491c-138">\_имажеаблесизехеигхтвалуе\_</span><span class="sxs-lookup"><span data-stu-id="4491c-138">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="4491c-139">Целое число</span><span class="sxs-lookup"><span data-stu-id="4491c-139">integer</span></span><br/> | <span data-ttu-id="4491c-140">мкм</span><span class="sxs-lookup"><span data-stu-id="4491c-140">microns</span></span><br/> | <span data-ttu-id="4491c-141">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="4491c-141">Greater than 0.</span></span><br/>             | <span data-ttu-id="4491c-142">Задает вертикальное измерение размера носителя приложения относительно Пажеориентатион.</span><span class="sxs-lookup"><span data-stu-id="4491c-142">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="4491c-143">\_оригинвидсвалуе\_</span><span class="sxs-lookup"><span data-stu-id="4491c-143">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="4491c-144">Целое число</span><span class="sxs-lookup"><span data-stu-id="4491c-144">integer</span></span><br/> | <span data-ttu-id="4491c-145">мкм</span><span class="sxs-lookup"><span data-stu-id="4491c-145">microns</span></span><br/> | <span data-ttu-id="4491c-146">Больше или равно 0.</span><span class="sxs-lookup"><span data-stu-id="4491c-146">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="4491c-147">Указывает горизонтальный источник области изображения относительно размера носителя приложения.</span><span class="sxs-lookup"><span data-stu-id="4491c-147">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="4491c-148">\_оригинхеигхтвалуе\_</span><span class="sxs-lookup"><span data-stu-id="4491c-148">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="4491c-149">Целое число</span><span class="sxs-lookup"><span data-stu-id="4491c-149">integer</span></span><br/> | <span data-ttu-id="4491c-150">мкм</span><span class="sxs-lookup"><span data-stu-id="4491c-150">microns</span></span><br/> | <span data-ttu-id="4491c-151">Больше или равно 0.</span><span class="sxs-lookup"><span data-stu-id="4491c-151">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="4491c-152">Задает вертикальный источник области изображения относительно размера носителя приложения.</span><span class="sxs-lookup"><span data-stu-id="4491c-152">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="4491c-153">\_екстентвидсвалуе\_</span><span class="sxs-lookup"><span data-stu-id="4491c-153">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="4491c-154">Целое число</span><span class="sxs-lookup"><span data-stu-id="4491c-154">integer</span></span><br/> | <span data-ttu-id="4491c-155">мкм</span><span class="sxs-lookup"><span data-stu-id="4491c-155">microns</span></span><br/> | <span data-ttu-id="4491c-156">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="4491c-156">Greater than 0.</span></span><br/>             | <span data-ttu-id="4491c-157">Указывает расстояние по горизонтали между началом и ограничивающим пределом размера носителя приложения.</span><span class="sxs-lookup"><span data-stu-id="4491c-157">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="4491c-158">\_екстенсеигхтвалуе\_</span><span class="sxs-lookup"><span data-stu-id="4491c-158">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="4491c-159">Целое число</span><span class="sxs-lookup"><span data-stu-id="4491c-159">integer</span></span><br/> | <span data-ttu-id="4491c-160">мкм</span><span class="sxs-lookup"><span data-stu-id="4491c-160">microns</span></span><br/> | <span data-ttu-id="4491c-161">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="4491c-161">Greater than 0.</span></span><br/>             | <span data-ttu-id="4491c-162">Задает расстояние по вертикали между источником и ограничивающим пределом размера носителя приложения Canvas.</span><span class="sxs-lookup"><span data-stu-id="4491c-162">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4491c-163">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="4491c-163">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4491c-164">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="4491c-164">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4491c-165">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="4491c-165">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="4491c-166">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="4491c-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4491c-167">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="4491c-167">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




