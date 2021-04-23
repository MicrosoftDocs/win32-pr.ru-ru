---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: пажеаутпутколор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71796bae9528fe6b32397f3467113630159c9954
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104273375"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="17f19-104">пажеаутпутколор</span><span class="sxs-lookup"><span data-stu-id="17f19-104">PageOutputColor</span></span>

<span data-ttu-id="17f19-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="17f19-105">This topic is not current.</span></span> <span data-ttu-id="17f19-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="17f19-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="17f19-107">Описывает характеристики параметров цвета для выходных данных.</span><span class="sxs-lookup"><span data-stu-id="17f19-107">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="17f19-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="17f19-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="17f19-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="17f19-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="17f19-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="17f19-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="17f19-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="17f19-111">Element Information</span></span>



| <span data-ttu-id="17f19-112">Имя</span><span class="sxs-lookup"><span data-stu-id="17f19-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="17f19-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="17f19-113">Element Type</span></span> <br/>   | <span data-ttu-id="17f19-114">Функция</span><span class="sxs-lookup"><span data-stu-id="17f19-114">Feature</span></span><br/> |
| <span data-ttu-id="17f19-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="17f19-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="17f19-116">Страница</span><span class="sxs-lookup"><span data-stu-id="17f19-116">Page</span></span><br/>    |
| <span data-ttu-id="17f19-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="17f19-117">Notes</span></span> <br/>          | <span data-ttu-id="17f19-118">Нет</span><span class="sxs-lookup"><span data-stu-id="17f19-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="17f19-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="17f19-119">Structural Content</span></span>

<span data-ttu-id="17f19-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="17f19-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name=psk:DeviceBitsPerPixel>
      <psf:Value xsi:type="xs:integer">_DeviceBitsPerPixelValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=psk:DriverBitsPerPixel>
      <psf:Value xsi:type="xs:integer">_DriverBitsPerPixelValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="17f19-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="17f19-121">Structure Variables</span></span>

<span data-ttu-id="17f19-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="17f19-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="17f19-123">Имя</span><span class="sxs-lookup"><span data-stu-id="17f19-123">Name</span></span>                                   | <span data-ttu-id="17f19-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="17f19-124">Data type</span></span>          | <span data-ttu-id="17f19-125">Unit</span><span class="sxs-lookup"><span data-stu-id="17f19-125">Unit</span></span>                      | <span data-ttu-id="17f19-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="17f19-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="17f19-127">Сводка</span><span class="sxs-lookup"><span data-stu-id="17f19-127">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17f19-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="17f19-128">\_OptionName\_</span></span><br/>              | <span data-ttu-id="17f19-129">строка</span><span class="sxs-lookup"><span data-stu-id="17f19-129">string</span></span><br/>  | <span data-ttu-id="17f19-130">characters</span><span class="sxs-lookup"><span data-stu-id="17f19-130">characters</span></span><br/>     | <span data-ttu-id="17f19-131">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="17f19-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="17f19-132">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="17f19-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="17f19-133">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="17f19-133">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="17f19-134">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="17f19-134">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="17f19-135">строка</span><span class="sxs-lookup"><span data-stu-id="17f19-135">string</span></span><br/>  | <span data-ttu-id="17f19-136">Недоступно</span><span class="sxs-lookup"><span data-stu-id="17f19-136">n/a</span></span><br/>            | <span data-ttu-id="17f19-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="17f19-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="17f19-138">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="17f19-138">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="17f19-139">\_девицебитсперпикселвалуе\_</span><span class="sxs-lookup"><span data-stu-id="17f19-139">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="17f19-140">Целое число</span><span class="sxs-lookup"><span data-stu-id="17f19-140">integer</span></span><br/> | <span data-ttu-id="17f19-141">бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="17f19-141">bits per pixel</span></span><br/> | <span data-ttu-id="17f19-142">Больше 0, меньше, чем максимальное значение поддержки устройства.</span><span class="sxs-lookup"><span data-stu-id="17f19-142">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="17f19-143">Числовое значение, указывающее число бит на пиксель данных о цвете, поддерживаемое принтером.</span><span class="sxs-lookup"><span data-stu-id="17f19-143">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="17f19-144">\_дривербитсперпикселвалуе\_</span><span class="sxs-lookup"><span data-stu-id="17f19-144">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="17f19-145">Целое число</span><span class="sxs-lookup"><span data-stu-id="17f19-145">integer</span></span><br/> | <span data-ttu-id="17f19-146">бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="17f19-146">bits per pixel</span></span><br/> | <span data-ttu-id="17f19-147">Больше 0, меньше, чем максимальное значение поддержки устройства.</span><span class="sxs-lookup"><span data-stu-id="17f19-147">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="17f19-148">Числовое значение, указывающее количество бит на пиксель, которое основной драйвер должен использовать для буфера отрисовки растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="17f19-148">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="17f19-149">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="17f19-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="17f19-150">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="17f19-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="17f19-151">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="17f19-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be in color. -->
  <psf:Option name="psk:Color">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the output should be in grayscale. -->
  <psf:Option name="psk:Grayscale">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the output should be in monochrome (Black). -->
  <psf:Option name="psk:Monochrome">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="17f19-152">См. также</span><span class="sxs-lookup"><span data-stu-id="17f19-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17f19-153">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="17f19-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




