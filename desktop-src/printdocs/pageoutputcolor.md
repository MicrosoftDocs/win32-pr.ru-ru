---
description: Сведения об элементе Пажеаутпутколор, настраиваемом пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: пажеаутпутколор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79fc71f58bde44224642d3a5f6979e3aef929976
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548992"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="c9d28-105">пажеаутпутколор</span><span class="sxs-lookup"><span data-stu-id="c9d28-105">PageOutputColor</span></span>

<span data-ttu-id="c9d28-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="c9d28-106">This topic is not current.</span></span> <span data-ttu-id="c9d28-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c9d28-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c9d28-108">Описывает характеристики параметров цвета для выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c9d28-108">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="c9d28-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c9d28-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c9d28-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="c9d28-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c9d28-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c9d28-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c9d28-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c9d28-112">Element Information</span></span>



| <span data-ttu-id="c9d28-113">Имя</span><span class="sxs-lookup"><span data-stu-id="c9d28-113">Name</span></span> | <span data-ttu-id="c9d28-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c9d28-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="c9d28-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="c9d28-115">Element Type</span></span> <br/>   | <span data-ttu-id="c9d28-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="c9d28-116">Feature</span></span><br/> |
| <span data-ttu-id="c9d28-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="c9d28-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c9d28-118">Страница</span><span class="sxs-lookup"><span data-stu-id="c9d28-118">Page</span></span><br/>    |
| <span data-ttu-id="c9d28-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="c9d28-119">Notes</span></span> <br/>          | <span data-ttu-id="c9d28-120">Нет</span><span class="sxs-lookup"><span data-stu-id="c9d28-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="c9d28-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="c9d28-121">Structural Content</span></span>

<span data-ttu-id="c9d28-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="c9d28-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="c9d28-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="c9d28-123">Structure Variables</span></span>

<span data-ttu-id="c9d28-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="c9d28-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c9d28-125">Имя</span><span class="sxs-lookup"><span data-stu-id="c9d28-125">Name</span></span>                                   | <span data-ttu-id="c9d28-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c9d28-126">Data type</span></span>          | <span data-ttu-id="c9d28-127">Unit</span><span class="sxs-lookup"><span data-stu-id="c9d28-127">Unit</span></span>                      | <span data-ttu-id="c9d28-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="c9d28-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c9d28-129">Итоги</span><span class="sxs-lookup"><span data-stu-id="c9d28-129">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d28-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="c9d28-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="c9d28-131">строка</span><span class="sxs-lookup"><span data-stu-id="c9d28-131">string</span></span><br/>  | <span data-ttu-id="c9d28-132">characters</span><span class="sxs-lookup"><span data-stu-id="c9d28-132">characters</span></span><br/>     | <span data-ttu-id="c9d28-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="c9d28-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c9d28-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c9d28-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c9d28-135">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="c9d28-135">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="c9d28-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="c9d28-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="c9d28-137">строка</span><span class="sxs-lookup"><span data-stu-id="c9d28-137">string</span></span><br/>  | <span data-ttu-id="c9d28-138">Н/Д</span><span class="sxs-lookup"><span data-stu-id="c9d28-138">n/a</span></span><br/>            | <span data-ttu-id="c9d28-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="c9d28-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c9d28-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="c9d28-140">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="c9d28-141">\_девицебитсперпикселвалуе\_</span><span class="sxs-lookup"><span data-stu-id="c9d28-141">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="c9d28-142">Целое число</span><span class="sxs-lookup"><span data-stu-id="c9d28-142">integer</span></span><br/> | <span data-ttu-id="c9d28-143">бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="c9d28-143">bits per pixel</span></span><br/> | <span data-ttu-id="c9d28-144">Больше 0, меньше, чем максимальное значение поддержки устройства.</span><span class="sxs-lookup"><span data-stu-id="c9d28-144">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="c9d28-145">Числовое значение, указывающее число бит на пиксель данных о цвете, поддерживаемое принтером.</span><span class="sxs-lookup"><span data-stu-id="c9d28-145">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="c9d28-146">\_дривербитсперпикселвалуе\_</span><span class="sxs-lookup"><span data-stu-id="c9d28-146">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="c9d28-147">Целое число</span><span class="sxs-lookup"><span data-stu-id="c9d28-147">integer</span></span><br/> | <span data-ttu-id="c9d28-148">бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="c9d28-148">bits per pixel</span></span><br/> | <span data-ttu-id="c9d28-149">Больше 0, меньше, чем максимальное значение поддержки устройства.</span><span class="sxs-lookup"><span data-stu-id="c9d28-149">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="c9d28-150">Числовое значение, указывающее количество бит на пиксель, которое основной драйвер должен использовать для буфера отрисовки растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="c9d28-150">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c9d28-151">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c9d28-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c9d28-152">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="c9d28-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c9d28-153">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="c9d28-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="c9d28-154">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c9d28-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9d28-155">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="c9d28-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




