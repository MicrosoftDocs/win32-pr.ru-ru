---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 6f99f54b-c401-42ea-8715-95a2aad73042
title: пажемедиасизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b549d7bd81579424125908fc71c9b81e839aff05
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104559450"
---
# <a name="pagemediasize"></a><span data-ttu-id="59d32-104">пажемедиасизе</span><span class="sxs-lookup"><span data-stu-id="59d32-104">PageMediaSize</span></span>

<span data-ttu-id="59d32-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="59d32-105">This topic is not current.</span></span> <span data-ttu-id="59d32-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="59d32-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="59d32-107">Описывает размеры физических носителей, используемые для выходных данных.</span><span class="sxs-lookup"><span data-stu-id="59d32-107">Describes the physical media dimensions used for the output.</span></span>

<span data-ttu-id="59d32-108">На следующей схеме показано использование переменной Пажемедиасизе (в качестве примера используется параметр ISOA4).</span><span class="sxs-lookup"><span data-stu-id="59d32-108">The following diagram illustrates the PageMediaSize variable usage (option ISOA4 is used as an example).</span></span>

![Диаграмма, показывающая размеры страницы](images/local-1594393517-pagemediasizepic.gif)

-   [<span data-ttu-id="59d32-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="59d32-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="59d32-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="59d32-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="59d32-112">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="59d32-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="59d32-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="59d32-113">Element Information</span></span>



|                            |                    |
|----------------------------|--------------------|
| <span data-ttu-id="59d32-114">Имя</span><span class="sxs-lookup"><span data-stu-id="59d32-114">Name</span></span>                       |                    |
| <span data-ttu-id="59d32-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="59d32-115">Element Type</span></span> <br/>   | <span data-ttu-id="59d32-116">Функция</span><span class="sxs-lookup"><span data-stu-id="59d32-116">Feature</span></span><br/> |
| <span data-ttu-id="59d32-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="59d32-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="59d32-118">Страница</span><span class="sxs-lookup"><span data-stu-id="59d32-118">Page</span></span><br/>    |
| <span data-ttu-id="59d32-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="59d32-119">Notes</span></span> <br/>          | <span data-ttu-id="59d32-120">Нет</span><span class="sxs-lookup"><span data-stu-id="59d32-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="59d32-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="59d32-121">Structural Content</span></span>

<span data-ttu-id="59d32-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="59d32-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaSize">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">_MediaSizeWidth_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">_MediaSizeHeight_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="59d32-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="59d32-123">Structure Variables</span></span>

<span data-ttu-id="59d32-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="59d32-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="59d32-125">Имя</span><span class="sxs-lookup"><span data-stu-id="59d32-125">Name</span></span>                                | <span data-ttu-id="59d32-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="59d32-126">Data type</span></span>          | <span data-ttu-id="59d32-127">Unit</span><span class="sxs-lookup"><span data-stu-id="59d32-127">Unit</span></span>                  | <span data-ttu-id="59d32-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="59d32-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="59d32-129">Сводка</span><span class="sxs-lookup"><span data-stu-id="59d32-129">Summary</span></span>                                                                                                                                                                   |
|-------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59d32-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="59d32-130">\_OptionName\_</span></span><br/>           | <span data-ttu-id="59d32-131">строка</span><span class="sxs-lookup"><span data-stu-id="59d32-131">string</span></span><br/>  | <span data-ttu-id="59d32-132">characters</span><span class="sxs-lookup"><span data-stu-id="59d32-132">characters</span></span><br/> | <span data-ttu-id="59d32-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="59d32-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="59d32-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="59d32-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="59d32-135">Указывает имя носителя.</span><span class="sxs-lookup"><span data-stu-id="59d32-135">Specifies the name of the media.</span></span> <span data-ttu-id="59d32-136">При именовании следует использовать следующее соглашение: " \_ оптионнаместандард \_ " " \_ оптионнамекоммоннаме \_ " " \_ оптионнамедескриптор \_ ".</span><span class="sxs-lookup"><span data-stu-id="59d32-136">The naming should use the following convention: "\_OptionNameStandard\_""\_OptionNameCommonName\_""\_OptionNameDescriptor\_".</span></span><br/> |
| <span data-ttu-id="59d32-137">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="59d32-137">\_IdentityOptionValue\_</span></span><br/>  | <span data-ttu-id="59d32-138">строка</span><span class="sxs-lookup"><span data-stu-id="59d32-138">string</span></span><br/>  | <span data-ttu-id="59d32-139">Недоступно</span><span class="sxs-lookup"><span data-stu-id="59d32-139">n/a</span></span><br/>        | <span data-ttu-id="59d32-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="59d32-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="59d32-141">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="59d32-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                              |
| <span data-ttu-id="59d32-142">\_оптионнаместандард\_</span><span class="sxs-lookup"><span data-stu-id="59d32-142">\_OptionNameStandard\_</span></span><br/>   | <span data-ttu-id="59d32-143">строка</span><span class="sxs-lookup"><span data-stu-id="59d32-143">string</span></span><br/>  | <span data-ttu-id="59d32-144">characters</span><span class="sxs-lookup"><span data-stu-id="59d32-144">characters</span></span><br/> | <span data-ttu-id="59d32-145">"ISO", "JIS", "Япония", "Норсамерика", "Осерметрик", "PRC", нет.</span><span class="sxs-lookup"><span data-stu-id="59d32-145">'ISO', 'JIS', 'Japan', 'NorthAmerica', 'OtherMetric', 'PRC', none.</span></span><br/>                                                                                                         | <span data-ttu-id="59d32-146">Указывает, определяется ли размер носителя определенным стандартом.</span><span class="sxs-lookup"><span data-stu-id="59d32-146">Indicates if the media size is defined by a particular standard.</span></span><br/>                                                                                               |
| <span data-ttu-id="59d32-147">\_оптионнамекоммоннаме\_</span><span class="sxs-lookup"><span data-stu-id="59d32-147">\_OptionNameCommonName\_</span></span><br/> | <span data-ttu-id="59d32-148">строка</span><span class="sxs-lookup"><span data-stu-id="59d32-148">string</span></span><br/>  | <span data-ttu-id="59d32-149">characters</span><span class="sxs-lookup"><span data-stu-id="59d32-149">characters</span></span><br/> | <span data-ttu-id="59d32-150">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="59d32-150">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="59d32-151">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="59d32-151">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="59d32-152">Общее имя для размера носителя.</span><span class="sxs-lookup"><span data-stu-id="59d32-152">Common Name for the media size.</span></span><br/>                                                                                                                                |
| <span data-ttu-id="59d32-153">\_оптионнамедескриптор\_</span><span class="sxs-lookup"><span data-stu-id="59d32-153">\_OptionNameDescriptor\_</span></span><br/> | <span data-ttu-id="59d32-154">строка</span><span class="sxs-lookup"><span data-stu-id="59d32-154">string</span></span><br/>  | <span data-ttu-id="59d32-155">characters</span><span class="sxs-lookup"><span data-stu-id="59d32-155">characters</span></span><br/> | <span data-ttu-id="59d32-156">Крупный, конверт, дополнительный, плюс, почтовая открытка, поворот, лист, "нет".</span><span class="sxs-lookup"><span data-stu-id="59d32-156">Big, Envelope, Extra, Plus, Postcard, Rotated, Sheet, 'none'.</span></span><br/>                                                                                                              | <span data-ttu-id="59d32-157">Крупный, конверт, дополнительный, плюс, почтовая открытка, поворот, лист, "нет".</span><span class="sxs-lookup"><span data-stu-id="59d32-157">Big, Envelope, Extra, Plus, Postcard, Rotated, Sheet, 'none'.</span></span><br/>                                                                                                  |
| <span data-ttu-id="59d32-158">\_медиасизевидс\_</span><span class="sxs-lookup"><span data-stu-id="59d32-158">\_MediaSizeWidth\_</span></span><br/>       | <span data-ttu-id="59d32-159">Целое число</span><span class="sxs-lookup"><span data-stu-id="59d32-159">integer</span></span><br/> | <span data-ttu-id="59d32-160">мкм</span><span class="sxs-lookup"><span data-stu-id="59d32-160">microns</span></span><br/>    | <span data-ttu-id="59d32-161">Больше 0, меньше, чем максимальный размер носителя поддержки для устройства.</span><span class="sxs-lookup"><span data-stu-id="59d32-161">Greater than 0, less than maximum support media size for device.</span></span><br/>                                                                                                           | <span data-ttu-id="59d32-162">Задает ширину физического носителя.</span><span class="sxs-lookup"><span data-stu-id="59d32-162">Specifies the width of the physical media.</span></span><br/>                                                                                                                     |
| <span data-ttu-id="59d32-163">\_медиасизехеигхт\_</span><span class="sxs-lookup"><span data-stu-id="59d32-163">\_MediaSizeHeight\_</span></span><br/>      | <span data-ttu-id="59d32-164">Целое число</span><span class="sxs-lookup"><span data-stu-id="59d32-164">integer</span></span><br/> | <span data-ttu-id="59d32-165">мкм</span><span class="sxs-lookup"><span data-stu-id="59d32-165">microns</span></span><br/>    | <span data-ttu-id="59d32-166">Больше 0, меньше, чем максимальный размер носителя поддержки для устройства.</span><span class="sxs-lookup"><span data-stu-id="59d32-166">Greater than 0, less than maximum support media size for device.</span></span><br/>                                                                                                           | <span data-ttu-id="59d32-167">Указывает высоту физического носителя.</span><span class="sxs-lookup"><span data-stu-id="59d32-167">Specifies the height of the physical media.</span></span><br/>                                                                                                                    |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="59d32-168">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="59d32-168">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="59d32-169">Ключевые слова общедоступной схемы печати определены в `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="59d32-169">The public Print Schema keywords are defined in the `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span></span> <span data-ttu-id="59d32-170">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="59d32-170">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaSize">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom media size.  Must be validated again DeviceMediaSize. -->
  <psf:Option name="psk:CustomMediaSize">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom media size (PostScript specific).  Must be validated again DeviceMediaSize. -->
  <psf:Option name="psk:PSCustomMediaSize">
    <!-- Specifies the height of the page parallel to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSHeight">
      <psf:ParameterRef name="psk:PageMediaSizePSHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the offset parallel to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSHeightOffset">
      <psf:ParameterRef name="psk:PageMediaSizePSHeightOffset" />
    </psf:ScoredProperty>
    <!-- Specifies the orientation relative to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSOrientation">
      <psf:ParameterRef name="psk:PageMediaSizePSOrientation" />
    </psf:ScoredProperty>
    <!-- Specifies the width of the page perpendicular to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSWidth">
      <psf:ParameterRef name="psk:PageMediaSizePSWidth" />
    </psf:ScoredProperty>
    <!-- Specifies the offset perpendicular to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSWidthOffset">
      <psf:ParameterRef name="psk:PageMediaSizePSWidthOffset" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA0">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">841000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1189000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA1">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">594000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">841000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">26000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">37000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA2">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">420000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">594000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">297000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">420000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA3Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">420000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">297000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA3Extra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">322000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">445000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA4">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">297000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA4Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">297000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA4Extra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">235500</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">322300</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA5">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA5Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA5Extra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">174000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">235000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA6">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">105000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA6Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">105000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">74000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">105000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">52000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">74000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA9">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">37000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">52000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB0">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">1000000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1414000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB1">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">707000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1000000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">31000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">44000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB2">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">500000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">707000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">353000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">500000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB4">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">250000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">353000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">250000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">353000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB5Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">250000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB5Extra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">201000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">276000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">88000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">125000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">62000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">88000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB9">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">44000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">62000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC0">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">917000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1297000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC1">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">648000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">917000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">28000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">40000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC2">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">648000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC4">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC5">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">162000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC5Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">162000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC6">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">114000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">162000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC6Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">114000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">162000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC6C5Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">114000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">81000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">114000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">57000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">81000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC9">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">40000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">57000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISODLEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISODLEnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOSRA3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">320000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">450000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanQuadrupleHagakiPostcard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">200000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">296000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB0">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">1030000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1456000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB1">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">728000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1030000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">32000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">45000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB2">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">515000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">728000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">364000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">515000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB4">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">257000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">364000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB4Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">364000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">257000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB5">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">182000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">257000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB5Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">257000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">182000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB6">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">128000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">182000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB6Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">182000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">128000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">91000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">128000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">64000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">91000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB9">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">45000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">64000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanChou3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">235000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanChou3EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">235000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanChou4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">90000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">205000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanChou4EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">205000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">90000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanHagakiPostcard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">100000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanHagakiPostcardRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">100000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanKaku2Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">240000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">332000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanKaku2EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">332000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">240000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanKaku3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">216000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">277000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanKaku3EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">277000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">216000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">105000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">235000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica10x11">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">254000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica10x14">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">254000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">355600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica11x17">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">431800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica9x11">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">228600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureASheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">228600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureBSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">457200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureCSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">457200</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">609600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureDSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">609600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">914400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureESheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">914400</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1219200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaCSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">431800</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">558800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaDSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">558800</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">863600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaESheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">863600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1117600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaExecutive">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">184150</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">266700</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaGermanLegalFanfold">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">330200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaGermanStandardFanfold">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLegal">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">355600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLegalExtra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">241300</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">381000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLetter">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLetterRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLetterExtra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">241300</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLetterPlus">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">322326</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaMonarchEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">98425</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">177800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNote">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber10Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">104775</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">241300</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber10EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">241300</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">104775</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber9Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">98425</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">225425</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber11Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">114300</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">263525</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber12Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">120650</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber14Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">127000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">292100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaPersonalEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">92075</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">165100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaQuarto">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">275000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaStatement">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">139700</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaSuperA">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">227000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">356000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaSuperB">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">305000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">487000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaTabloid">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">431800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaTabloidExtra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">296926</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">457200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricA4Plus">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">330000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricA3Plus">
    - <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">329000</psf:Value>
    </psf:ScoredProperty>
    - <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">483000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricFolio">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">330200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricInviteEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricItalianEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC1Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">102000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">165000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC1EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">165000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">102000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC10Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC10EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC16K">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">146000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">215000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC16KRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">146000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC2Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">102000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC2EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">102000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC32K">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">97000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">151000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC32KRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">151000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">97000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC32KBig">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">97000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">151000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">125000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC3EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">125000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">208000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC4EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">208000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC5Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC5EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC6Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC6EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC7Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">160000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC7EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">160000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC8Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">309000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC8EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">309000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC9Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC9EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Roll04Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">101600</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll06Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">152400</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll08Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">203200</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll12Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll15Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">381000</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll18Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">457200</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll22Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">558800</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll24Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">609600</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll30Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">762000</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll36Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">914400</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll54Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">1371600</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:JapanDoubleHagakiPostcard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">200000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanDoubleHagakiPostcardRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">148000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">200000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanLPhoto">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">89000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">127000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Japan2LPhoto">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">127000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">178000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou1Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">120000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">176000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou2Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">114000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">162000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">98000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou4EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">235000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">105000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou6Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">98000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">190000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou6EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">190000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">98000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica4x6">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">101600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">152400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica4x8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">101600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">203200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica5x7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">127000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">177800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica8x10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">203200</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">254000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica10x12">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">254000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">304800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica14x17">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">355600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">431800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:BusinessCard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">55000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">91000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:CreditCard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">54000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">86000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>   
```

## <a name="related-topics"></a><span data-ttu-id="59d32-171">См. также</span><span class="sxs-lookup"><span data-stu-id="59d32-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59d32-172">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="59d32-172">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
