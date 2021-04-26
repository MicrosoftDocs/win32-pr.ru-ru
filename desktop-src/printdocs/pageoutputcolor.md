---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: пажеаутпутколор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4791ca4a53b8bdcc43a32c5c7aa5a1e38bbe1e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998051"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="85476-104">пажеаутпутколор</span><span class="sxs-lookup"><span data-stu-id="85476-104">PageOutputColor</span></span>

<span data-ttu-id="85476-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="85476-105">This topic is not current.</span></span> <span data-ttu-id="85476-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="85476-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="85476-107">Описывает характеристики параметров цвета для выходных данных.</span><span class="sxs-lookup"><span data-stu-id="85476-107">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="85476-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="85476-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="85476-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="85476-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="85476-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="85476-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="85476-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="85476-111">Element Information</span></span>



| <span data-ttu-id="85476-112">Имя</span><span class="sxs-lookup"><span data-stu-id="85476-112">Name</span></span> | <span data-ttu-id="85476-113">Значение</span><span class="sxs-lookup"><span data-stu-id="85476-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="85476-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="85476-114">Element Type</span></span> <br/>   | <span data-ttu-id="85476-115">Компонент</span><span class="sxs-lookup"><span data-stu-id="85476-115">Feature</span></span><br/> |
| <span data-ttu-id="85476-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="85476-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="85476-117">Страница</span><span class="sxs-lookup"><span data-stu-id="85476-117">Page</span></span><br/>    |
| <span data-ttu-id="85476-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="85476-118">Notes</span></span> <br/>          | <span data-ttu-id="85476-119">Нет</span><span class="sxs-lookup"><span data-stu-id="85476-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="85476-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="85476-120">Structural Content</span></span>

<span data-ttu-id="85476-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="85476-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="85476-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="85476-122">Structure Variables</span></span>

<span data-ttu-id="85476-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="85476-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="85476-124">Имя</span><span class="sxs-lookup"><span data-stu-id="85476-124">Name</span></span>                                   | <span data-ttu-id="85476-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="85476-125">Data type</span></span>          | <span data-ttu-id="85476-126">Unit</span><span class="sxs-lookup"><span data-stu-id="85476-126">Unit</span></span>                      | <span data-ttu-id="85476-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="85476-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="85476-128">Сводка</span><span class="sxs-lookup"><span data-stu-id="85476-128">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85476-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="85476-129">\_OptionName\_</span></span><br/>              | <span data-ttu-id="85476-130">строка</span><span class="sxs-lookup"><span data-stu-id="85476-130">string</span></span><br/>  | <span data-ttu-id="85476-131">characters</span><span class="sxs-lookup"><span data-stu-id="85476-131">characters</span></span><br/>     | <span data-ttu-id="85476-132">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="85476-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="85476-133">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="85476-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="85476-134">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="85476-134">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="85476-135">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="85476-135">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="85476-136">строка</span><span class="sxs-lookup"><span data-stu-id="85476-136">string</span></span><br/>  | <span data-ttu-id="85476-137">Недоступно</span><span class="sxs-lookup"><span data-stu-id="85476-137">n/a</span></span><br/>            | <span data-ttu-id="85476-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="85476-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="85476-139">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="85476-139">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="85476-140">\_девицебитсперпикселвалуе\_</span><span class="sxs-lookup"><span data-stu-id="85476-140">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="85476-141">Целое число</span><span class="sxs-lookup"><span data-stu-id="85476-141">integer</span></span><br/> | <span data-ttu-id="85476-142">бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="85476-142">bits per pixel</span></span><br/> | <span data-ttu-id="85476-143">Больше 0, меньше, чем максимальное значение поддержки устройства.</span><span class="sxs-lookup"><span data-stu-id="85476-143">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="85476-144">Числовое значение, указывающее число бит на пиксель данных о цвете, поддерживаемое принтером.</span><span class="sxs-lookup"><span data-stu-id="85476-144">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="85476-145">\_дривербитсперпикселвалуе\_</span><span class="sxs-lookup"><span data-stu-id="85476-145">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="85476-146">Целое число</span><span class="sxs-lookup"><span data-stu-id="85476-146">integer</span></span><br/> | <span data-ttu-id="85476-147">бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="85476-147">bits per pixel</span></span><br/> | <span data-ttu-id="85476-148">Больше 0, меньше, чем максимальное значение поддержки устройства.</span><span class="sxs-lookup"><span data-stu-id="85476-148">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="85476-149">Числовое значение, указывающее количество бит на пиксель, которое основной драйвер должен использовать для буфера отрисовки растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="85476-149">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="85476-150">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="85476-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="85476-151">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="85476-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="85476-152">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="85476-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="85476-153">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="85476-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85476-154">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="85476-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




