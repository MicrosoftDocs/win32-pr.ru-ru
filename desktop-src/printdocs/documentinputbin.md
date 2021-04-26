---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: документинпутбин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57890492ed5f0b575e6d462351282dd199f34f45
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997771"
---
# <a name="documentinputbin"></a><span data-ttu-id="08e84-104">документинпутбин</span><span class="sxs-lookup"><span data-stu-id="08e84-104">DocumentInputBin</span></span>

<span data-ttu-id="08e84-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="08e84-105">This topic is not current.</span></span> <span data-ttu-id="08e84-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="08e84-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="08e84-107">Описывает установленную входную ячейку на устройстве или полный список поддерживаемых ячеек для устройства.</span><span class="sxs-lookup"><span data-stu-id="08e84-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="08e84-108">Ключевые слова Жобинпутбин, Документинпутбин и Пажеинпутбин являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="08e84-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="08e84-109">Оба значения не должны одновременно указываться в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="08e84-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="08e84-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="08e84-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="08e84-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="08e84-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="08e84-112">XML-содержимое</span><span class="sxs-lookup"><span data-stu-id="08e84-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="08e84-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="08e84-113">Element Information</span></span>



| <span data-ttu-id="08e84-114">Имя</span><span class="sxs-lookup"><span data-stu-id="08e84-114">Name</span></span> | <span data-ttu-id="08e84-115">Значение</span><span class="sxs-lookup"><span data-stu-id="08e84-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08e84-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="08e84-116">Element Type</span></span> <br/>   | <span data-ttu-id="08e84-117">Компонент</span><span class="sxs-lookup"><span data-stu-id="08e84-117">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="08e84-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="08e84-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="08e84-119">Документ</span><span class="sxs-lookup"><span data-stu-id="08e84-119">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="08e84-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="08e84-120">Notes</span></span> <br/>          | <span data-ttu-id="08e84-121">Поддерживаемые ячейки, которые не установлены в настоящий момент, должны помечаться как ограниченные в документе PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="08e84-121">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="08e84-122">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="08e84-122">Structural Content</span></span>

<span data-ttu-id="08e84-123">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="08e84-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentInputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psf:_EnvelopeOptionValue_">
      <psf:Value xsi:type="xs:string">_EnvelopeOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_FeedTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_MediaCapacityValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_MediaSizeAutoSenseValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_MediaTypeAutoSenseValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_MediaPathValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_FeedFaceValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_FeedDirectionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="08e84-124">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="08e84-124">Structure Variables</span></span>

<span data-ttu-id="08e84-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="08e84-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="08e84-126">Имя</span><span class="sxs-lookup"><span data-stu-id="08e84-126">Name</span></span>                                   | <span data-ttu-id="08e84-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="08e84-127">Data type</span></span>          | <span data-ttu-id="08e84-128">Unit</span><span class="sxs-lookup"><span data-stu-id="08e84-128">Unit</span></span>                  | <span data-ttu-id="08e84-129">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="08e84-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="08e84-130">Сводка</span><span class="sxs-lookup"><span data-stu-id="08e84-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="08e84-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="08e84-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="08e84-132">строка</span><span class="sxs-lookup"><span data-stu-id="08e84-132">string</span></span><br/>  | <span data-ttu-id="08e84-133">characters</span><span class="sxs-lookup"><span data-stu-id="08e84-133">characters</span></span><br/> | <span data-ttu-id="08e84-134">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="08e84-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="08e84-135">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="08e84-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="08e84-136">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="08e84-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="08e84-137">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="08e84-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="08e84-138">строка</span><span class="sxs-lookup"><span data-stu-id="08e84-138">string</span></span><br/>  | <span data-ttu-id="08e84-139">Недоступно</span><span class="sxs-lookup"><span data-stu-id="08e84-139">n/a</span></span><br/>        | <span data-ttu-id="08e84-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="08e84-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="08e84-141">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="08e84-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="08e84-142">\_енвелопеоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="08e84-142">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="08e84-143">строка</span><span class="sxs-lookup"><span data-stu-id="08e84-143">string</span></span><br/>  | <span data-ttu-id="08e84-144">Недоступно</span><span class="sxs-lookup"><span data-stu-id="08e84-144">n/a</span></span><br/>        | <span data-ttu-id="08e84-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="08e84-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="08e84-146">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="08e84-146">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="08e84-147">\_бинтипевалуе\_</span><span class="sxs-lookup"><span data-stu-id="08e84-147">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="08e84-148">строка</span><span class="sxs-lookup"><span data-stu-id="08e84-148">string</span></span><br/>  | <span data-ttu-id="08e84-149">Недоступно</span><span class="sxs-lookup"><span data-stu-id="08e84-149">n/a</span></span><br/>        | <span data-ttu-id="08e84-150">Континуаусфид, Шитфид.</span><span class="sxs-lookup"><span data-stu-id="08e84-150">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="08e84-151">Указывает тип ячейки.</span><span class="sxs-lookup"><span data-stu-id="08e84-151">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="08e84-152">\_фидтипевалуе\_</span><span class="sxs-lookup"><span data-stu-id="08e84-152">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="08e84-153">строка</span><span class="sxs-lookup"><span data-stu-id="08e84-153">string</span></span><br/>  | <span data-ttu-id="08e84-154">Недоступно</span><span class="sxs-lookup"><span data-stu-id="08e84-154">n/a</span></span><br/>        | <span data-ttu-id="08e84-155">Автоматически, вручную.</span><span class="sxs-lookup"><span data-stu-id="08e84-155">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="08e84-156">Указывает механизм подачи для ячейки.</span><span class="sxs-lookup"><span data-stu-id="08e84-156">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="08e84-157">\_медиакапаЦитивалуе\_</span><span class="sxs-lookup"><span data-stu-id="08e84-157">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="08e84-158">Целое число</span><span class="sxs-lookup"><span data-stu-id="08e84-158">integer</span></span><br/> | <span data-ttu-id="08e84-159">свойств</span><span class="sxs-lookup"><span data-stu-id="08e84-159">sheets</span></span><br/>     | <span data-ttu-id="08e84-160">Максимальное целочисленное ограничение, разрешенное устройством.</span><span class="sxs-lookup"><span data-stu-id="08e84-160">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="08e84-161">Указывает, является ли ячейка ячейкой высокой емкости (качественная).</span><span class="sxs-lookup"><span data-stu-id="08e84-161">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="08e84-162">\_медиасизеаутосенсевалуе\_</span><span class="sxs-lookup"><span data-stu-id="08e84-162">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="08e84-163">строка</span><span class="sxs-lookup"><span data-stu-id="08e84-163">string</span></span><br/>  | <span data-ttu-id="08e84-164">Недоступно</span><span class="sxs-lookup"><span data-stu-id="08e84-164">n/a</span></span><br/>        | <span data-ttu-id="08e84-165">Поддерживается, нет.</span><span class="sxs-lookup"><span data-stu-id="08e84-165">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="08e84-166">Указывает функцию автоматического датчика размера носителя для устройства.</span><span class="sxs-lookup"><span data-stu-id="08e84-166">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="08e84-167">\_медиатипеаутосенсевалуе\_</span><span class="sxs-lookup"><span data-stu-id="08e84-167">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="08e84-168">строка</span><span class="sxs-lookup"><span data-stu-id="08e84-168">string</span></span><br/>  | <span data-ttu-id="08e84-169">Недоступно</span><span class="sxs-lookup"><span data-stu-id="08e84-169">n/a</span></span><br/>        | <span data-ttu-id="08e84-170">Поддерживается, нет.</span><span class="sxs-lookup"><span data-stu-id="08e84-170">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="08e84-171">Указывает емкость носителя в количестве страниц (полный уровень) ячейки.</span><span class="sxs-lookup"><span data-stu-id="08e84-171">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="08e84-172">\_медиапасвалуе\_</span><span class="sxs-lookup"><span data-stu-id="08e84-172">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="08e84-173">строка</span><span class="sxs-lookup"><span data-stu-id="08e84-173">string</span></span><br/>  | <span data-ttu-id="08e84-174">Недоступно</span><span class="sxs-lookup"><span data-stu-id="08e84-174">n/a</span></span><br/>        | <span data-ttu-id="08e84-175">Прямая, серпентине.</span><span class="sxs-lookup"><span data-stu-id="08e84-175">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="08e84-176">Задает характеристики пути к носителю.</span><span class="sxs-lookup"><span data-stu-id="08e84-176">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="08e84-177">\_фидфацевалуе\_</span><span class="sxs-lookup"><span data-stu-id="08e84-177">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="08e84-178">строка</span><span class="sxs-lookup"><span data-stu-id="08e84-178">string</span></span><br/>  | <span data-ttu-id="08e84-179">Недоступно</span><span class="sxs-lookup"><span data-stu-id="08e84-179">n/a</span></span><br/>        | <span data-ttu-id="08e84-180">Фацеуп, Фацедовн</span><span class="sxs-lookup"><span data-stu-id="08e84-180">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="08e84-181">Указывает, следует ли печатать мультимедиа лицевой или лицевой стороны.</span><span class="sxs-lookup"><span data-stu-id="08e84-181">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="08e84-182">\_фиддиректионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="08e84-182">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="08e84-183">строка</span><span class="sxs-lookup"><span data-stu-id="08e84-183">string</span></span><br/>  | <span data-ttu-id="08e84-184">Недоступно</span><span class="sxs-lookup"><span data-stu-id="08e84-184">n/a</span></span><br/>        | <span data-ttu-id="08e84-185">Лонжеджефирст, Шортеджефирст</span><span class="sxs-lookup"><span data-stu-id="08e84-185">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="08e84-186">Указывает, будет ли мультимедиа сначала выдаваться длинная или короткая сторона.</span><span class="sxs-lookup"><span data-stu-id="08e84-186">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="08e84-187">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="08e84-187">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="08e84-188">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="08e84-188">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="08e84-189">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="08e84-189">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentInputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Device will automatically choose best option based on configuration -->
  <psf:Option name="psk:AutoSelect">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the default manual feed bin -->
  <psf:Option name="psk:Manual">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">Manual</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the feed bin is a cassette-->
  <psf:Option name="psk:Cassette">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">SheetFeed</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the feed bin is a tractor-->
  <psf:Option name="psk:Tractor">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">ContinuousFeed</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!-- Device Input tray for Inkjet Printers -->
  <psf:Option name="psk:AutoSheetFeeder">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="08e84-190">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="08e84-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08e84-191">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="08e84-191">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




