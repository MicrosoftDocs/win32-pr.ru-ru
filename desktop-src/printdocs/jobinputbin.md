---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 9192ceb1-90c4-480e-9247-68d457976f42
title: жобинпутбин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f87782d6cf9aae5c34d36603f025e803f47db3e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998101"
---
# <a name="jobinputbin"></a><span data-ttu-id="70a7b-104">жобинпутбин</span><span class="sxs-lookup"><span data-stu-id="70a7b-104">JobInputBin</span></span>

<span data-ttu-id="70a7b-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="70a7b-105">This topic is not current.</span></span> <span data-ttu-id="70a7b-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="70a7b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="70a7b-107">Описывает установленную входную ячейку на устройстве или полный список поддерживаемых ячеек для устройства.</span><span class="sxs-lookup"><span data-stu-id="70a7b-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="70a7b-108">Разрешает указание входной ячейки для каждого задания.</span><span class="sxs-lookup"><span data-stu-id="70a7b-108">Allows specification of input bin on a per job basis.</span></span> <span data-ttu-id="70a7b-109">Ключевые слова Жобинпутбин, Документинпутбин и Пажеинпутбин являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="70a7b-109">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="70a7b-110">Оба значения не должны одновременно указываться в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="70a7b-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="70a7b-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="70a7b-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="70a7b-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="70a7b-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="70a7b-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="70a7b-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="70a7b-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="70a7b-114">Element Information</span></span>



| <span data-ttu-id="70a7b-115">Имя</span><span class="sxs-lookup"><span data-stu-id="70a7b-115">Name</span></span> | <span data-ttu-id="70a7b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="70a7b-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="70a7b-117">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="70a7b-117">Element Type</span></span> <br/>   | <span data-ttu-id="70a7b-118">Компонент</span><span class="sxs-lookup"><span data-stu-id="70a7b-118">Feature</span></span><br/> |
| <span data-ttu-id="70a7b-119">Префикс области</span><span class="sxs-lookup"><span data-stu-id="70a7b-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="70a7b-120">Задание</span><span class="sxs-lookup"><span data-stu-id="70a7b-120">Job</span></span><br/>     |
| <span data-ttu-id="70a7b-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="70a7b-121">Notes</span></span> <br/>          | <span data-ttu-id="70a7b-122">Нет</span><span class="sxs-lookup"><span data-stu-id="70a7b-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="70a7b-123">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="70a7b-123">Structural Content</span></span>

<span data-ttu-id="70a7b-124">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="70a7b-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:JobInputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="70a7b-125">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="70a7b-125">Structure Variables</span></span>

<span data-ttu-id="70a7b-126">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="70a7b-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="70a7b-127">Имя</span><span class="sxs-lookup"><span data-stu-id="70a7b-127">Name</span></span>                                   | <span data-ttu-id="70a7b-128">Тип данных</span><span class="sxs-lookup"><span data-stu-id="70a7b-128">Data type</span></span>          | <span data-ttu-id="70a7b-129">Unit</span><span class="sxs-lookup"><span data-stu-id="70a7b-129">Unit</span></span>                  | <span data-ttu-id="70a7b-130">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="70a7b-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="70a7b-131">Сводка</span><span class="sxs-lookup"><span data-stu-id="70a7b-131">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="70a7b-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="70a7b-132">\_OptionName\_</span></span><br/>              | <span data-ttu-id="70a7b-133">строка</span><span class="sxs-lookup"><span data-stu-id="70a7b-133">string</span></span><br/>  | <span data-ttu-id="70a7b-134">characters</span><span class="sxs-lookup"><span data-stu-id="70a7b-134">characters</span></span><br/> | <span data-ttu-id="70a7b-135">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="70a7b-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="70a7b-136">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="70a7b-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="70a7b-137">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="70a7b-137">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="70a7b-138">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="70a7b-138">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="70a7b-139">строка</span><span class="sxs-lookup"><span data-stu-id="70a7b-139">string</span></span><br/>  | <span data-ttu-id="70a7b-140">Недоступно</span><span class="sxs-lookup"><span data-stu-id="70a7b-140">n/a</span></span><br/>        | <span data-ttu-id="70a7b-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="70a7b-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="70a7b-142">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="70a7b-142">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="70a7b-143">\_енвелопеоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="70a7b-143">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="70a7b-144">строка</span><span class="sxs-lookup"><span data-stu-id="70a7b-144">string</span></span><br/>  | <span data-ttu-id="70a7b-145">Недоступно</span><span class="sxs-lookup"><span data-stu-id="70a7b-145">n/a</span></span><br/>        | <span data-ttu-id="70a7b-146">True, False.</span><span class="sxs-lookup"><span data-stu-id="70a7b-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="70a7b-147">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="70a7b-147">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="70a7b-148">\_бинтипевалуе\_</span><span class="sxs-lookup"><span data-stu-id="70a7b-148">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="70a7b-149">строка</span><span class="sxs-lookup"><span data-stu-id="70a7b-149">string</span></span><br/>  | <span data-ttu-id="70a7b-150">Недоступно</span><span class="sxs-lookup"><span data-stu-id="70a7b-150">n/a</span></span><br/>        | <span data-ttu-id="70a7b-151">Континуаусфид, Шитфид.</span><span class="sxs-lookup"><span data-stu-id="70a7b-151">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="70a7b-152">Указывает тип ячейки.</span><span class="sxs-lookup"><span data-stu-id="70a7b-152">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="70a7b-153">\_фидтипевалуе\_</span><span class="sxs-lookup"><span data-stu-id="70a7b-153">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="70a7b-154">строка</span><span class="sxs-lookup"><span data-stu-id="70a7b-154">string</span></span><br/>  | <span data-ttu-id="70a7b-155">Недоступно</span><span class="sxs-lookup"><span data-stu-id="70a7b-155">n/a</span></span><br/>        | <span data-ttu-id="70a7b-156">Автоматически, вручную.</span><span class="sxs-lookup"><span data-stu-id="70a7b-156">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="70a7b-157">Указывает механизм подачи для ячейки.</span><span class="sxs-lookup"><span data-stu-id="70a7b-157">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="70a7b-158">\_медиакапаЦитивалуе\_</span><span class="sxs-lookup"><span data-stu-id="70a7b-158">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="70a7b-159">строка</span><span class="sxs-lookup"><span data-stu-id="70a7b-159">string</span></span><br/>  | <span data-ttu-id="70a7b-160">Недоступно</span><span class="sxs-lookup"><span data-stu-id="70a7b-160">n/a</span></span><br/>        | <span data-ttu-id="70a7b-161">Высокий, Стандартный.</span><span class="sxs-lookup"><span data-stu-id="70a7b-161">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="70a7b-162">Указывает, является ли ячейка ячейкой высокой емкости (качественная).</span><span class="sxs-lookup"><span data-stu-id="70a7b-162">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="70a7b-163">\_медиасизеаутосенсевалуе\_</span><span class="sxs-lookup"><span data-stu-id="70a7b-163">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="70a7b-164">строка</span><span class="sxs-lookup"><span data-stu-id="70a7b-164">string</span></span><br/>  | <span data-ttu-id="70a7b-165">Недоступно</span><span class="sxs-lookup"><span data-stu-id="70a7b-165">n/a</span></span><br/>        | <span data-ttu-id="70a7b-166">Поддерживается, нет.</span><span class="sxs-lookup"><span data-stu-id="70a7b-166">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="70a7b-167">Указывает функцию автоматического датчика размера носителя для устройства.</span><span class="sxs-lookup"><span data-stu-id="70a7b-167">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="70a7b-168">\_медиатипеаутосенсевалуе\_</span><span class="sxs-lookup"><span data-stu-id="70a7b-168">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="70a7b-169">строка</span><span class="sxs-lookup"><span data-stu-id="70a7b-169">string</span></span><br/>  | <span data-ttu-id="70a7b-170">Недоступно</span><span class="sxs-lookup"><span data-stu-id="70a7b-170">n/a</span></span><br/>        | <span data-ttu-id="70a7b-171">Поддерживается, нет.</span><span class="sxs-lookup"><span data-stu-id="70a7b-171">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="70a7b-172">Указывает функцию автоматического датчика типа носителя для устройства.</span><span class="sxs-lookup"><span data-stu-id="70a7b-172">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="70a7b-173">\_медиашиткапаЦитивалуе\_</span><span class="sxs-lookup"><span data-stu-id="70a7b-173">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="70a7b-174">Целое число</span><span class="sxs-lookup"><span data-stu-id="70a7b-174">integer</span></span><br/> | <span data-ttu-id="70a7b-175">свойств</span><span class="sxs-lookup"><span data-stu-id="70a7b-175">sheets</span></span><br/>     | <span data-ttu-id="70a7b-176">Максимальное целочисленное ограничение, разрешенное устройством.</span><span class="sxs-lookup"><span data-stu-id="70a7b-176">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="70a7b-177">Указывает емкость носителя в количестве страниц (полный уровень) ячейки.</span><span class="sxs-lookup"><span data-stu-id="70a7b-177">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="70a7b-178">\_медиапасвалуе\_</span><span class="sxs-lookup"><span data-stu-id="70a7b-178">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="70a7b-179">строка</span><span class="sxs-lookup"><span data-stu-id="70a7b-179">string</span></span><br/>  | <span data-ttu-id="70a7b-180">Недоступно</span><span class="sxs-lookup"><span data-stu-id="70a7b-180">n/a</span></span><br/>        | <span data-ttu-id="70a7b-181">Прямая, серпентине.</span><span class="sxs-lookup"><span data-stu-id="70a7b-181">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="70a7b-182">Задает характеристики пути к носителю.</span><span class="sxs-lookup"><span data-stu-id="70a7b-182">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="70a7b-183">\_фидфацевалуе\_</span><span class="sxs-lookup"><span data-stu-id="70a7b-183">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="70a7b-184">строка</span><span class="sxs-lookup"><span data-stu-id="70a7b-184">string</span></span><br/>  | <span data-ttu-id="70a7b-185">Недоступно</span><span class="sxs-lookup"><span data-stu-id="70a7b-185">n/a</span></span><br/>        | <span data-ttu-id="70a7b-186">Фацеуп, Фацедовн</span><span class="sxs-lookup"><span data-stu-id="70a7b-186">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="70a7b-187">Указывает, следует ли печатать мультимедиа лицевой или лицевой стороны.</span><span class="sxs-lookup"><span data-stu-id="70a7b-187">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="70a7b-188">\_фиддиректионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="70a7b-188">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="70a7b-189">строка</span><span class="sxs-lookup"><span data-stu-id="70a7b-189">string</span></span><br/>  | <span data-ttu-id="70a7b-190">Недоступно</span><span class="sxs-lookup"><span data-stu-id="70a7b-190">n/a</span></span><br/>        | <span data-ttu-id="70a7b-191">Лонжеджефирст, Шортеджефирст</span><span class="sxs-lookup"><span data-stu-id="70a7b-191">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="70a7b-192">Указывает, будет ли мультимедиа сначала выдаваться длинная или короткая сторона.</span><span class="sxs-lookup"><span data-stu-id="70a7b-192">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="70a7b-193">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="70a7b-193">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="70a7b-194">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="70a7b-194">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="70a7b-195">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="70a7b-195">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobInputBin">
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

## <a name="related-topics"></a><span data-ttu-id="70a7b-196">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="70a7b-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70a7b-197">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="70a7b-197">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




