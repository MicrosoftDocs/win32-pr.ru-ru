---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 9192ceb1-90c4-480e-9247-68d457976f42
title: жобинпутбин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e48cb6bc5de419ffdda2e1c352c72623baf3ba9
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104273360"
---
# <a name="jobinputbin"></a><span data-ttu-id="2c469-104">жобинпутбин</span><span class="sxs-lookup"><span data-stu-id="2c469-104">JobInputBin</span></span>

<span data-ttu-id="2c469-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="2c469-105">This topic is not current.</span></span> <span data-ttu-id="2c469-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2c469-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2c469-107">Описывает установленную входную ячейку на устройстве или полный список поддерживаемых ячеек для устройства.</span><span class="sxs-lookup"><span data-stu-id="2c469-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="2c469-108">Разрешает указание входной ячейки для каждого задания.</span><span class="sxs-lookup"><span data-stu-id="2c469-108">Allows specification of input bin on a per job basis.</span></span> <span data-ttu-id="2c469-109">Ключевые слова Жобинпутбин, Документинпутбин и Пажеинпутбин являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="2c469-109">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="2c469-110">Оба значения не должны одновременно указываться в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="2c469-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="2c469-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2c469-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2c469-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="2c469-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2c469-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="2c469-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2c469-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2c469-114">Element Information</span></span>



| <span data-ttu-id="2c469-115">Имя</span><span class="sxs-lookup"><span data-stu-id="2c469-115">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="2c469-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="2c469-116">Element Type</span></span> <br/>   | <span data-ttu-id="2c469-117">Функция</span><span class="sxs-lookup"><span data-stu-id="2c469-117">Feature</span></span><br/> |
| <span data-ttu-id="2c469-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="2c469-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2c469-119">Задание</span><span class="sxs-lookup"><span data-stu-id="2c469-119">Job</span></span><br/>     |
| <span data-ttu-id="2c469-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="2c469-120">Notes</span></span> <br/>          | <span data-ttu-id="2c469-121">Нет</span><span class="sxs-lookup"><span data-stu-id="2c469-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="2c469-122">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="2c469-122">Structural Content</span></span>

<span data-ttu-id="2c469-123">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2c469-123">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="2c469-124">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="2c469-124">Structure Variables</span></span>

<span data-ttu-id="2c469-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="2c469-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2c469-126">Имя</span><span class="sxs-lookup"><span data-stu-id="2c469-126">Name</span></span>                                   | <span data-ttu-id="2c469-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2c469-127">Data type</span></span>          | <span data-ttu-id="2c469-128">Unit</span><span class="sxs-lookup"><span data-stu-id="2c469-128">Unit</span></span>                  | <span data-ttu-id="2c469-129">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="2c469-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="2c469-130">Сводка</span><span class="sxs-lookup"><span data-stu-id="2c469-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2c469-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="2c469-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="2c469-132">строка</span><span class="sxs-lookup"><span data-stu-id="2c469-132">string</span></span><br/>  | <span data-ttu-id="2c469-133">characters</span><span class="sxs-lookup"><span data-stu-id="2c469-133">characters</span></span><br/> | <span data-ttu-id="2c469-134">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="2c469-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="2c469-135">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c469-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="2c469-136">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="2c469-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="2c469-137">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="2c469-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="2c469-138">строка</span><span class="sxs-lookup"><span data-stu-id="2c469-138">string</span></span><br/>  | <span data-ttu-id="2c469-139">Недоступно</span><span class="sxs-lookup"><span data-stu-id="2c469-139">n/a</span></span><br/>        | <span data-ttu-id="2c469-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="2c469-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="2c469-141">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="2c469-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="2c469-142">\_енвелопеоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="2c469-142">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="2c469-143">строка</span><span class="sxs-lookup"><span data-stu-id="2c469-143">string</span></span><br/>  | <span data-ttu-id="2c469-144">Недоступно</span><span class="sxs-lookup"><span data-stu-id="2c469-144">n/a</span></span><br/>        | <span data-ttu-id="2c469-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="2c469-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="2c469-146">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="2c469-146">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="2c469-147">\_бинтипевалуе\_</span><span class="sxs-lookup"><span data-stu-id="2c469-147">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="2c469-148">строка</span><span class="sxs-lookup"><span data-stu-id="2c469-148">string</span></span><br/>  | <span data-ttu-id="2c469-149">Недоступно</span><span class="sxs-lookup"><span data-stu-id="2c469-149">n/a</span></span><br/>        | <span data-ttu-id="2c469-150">Континуаусфид, Шитфид.</span><span class="sxs-lookup"><span data-stu-id="2c469-150">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="2c469-151">Указывает тип ячейки.</span><span class="sxs-lookup"><span data-stu-id="2c469-151">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="2c469-152">\_фидтипевалуе\_</span><span class="sxs-lookup"><span data-stu-id="2c469-152">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="2c469-153">строка</span><span class="sxs-lookup"><span data-stu-id="2c469-153">string</span></span><br/>  | <span data-ttu-id="2c469-154">Недоступно</span><span class="sxs-lookup"><span data-stu-id="2c469-154">n/a</span></span><br/>        | <span data-ttu-id="2c469-155">Автоматически, вручную.</span><span class="sxs-lookup"><span data-stu-id="2c469-155">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="2c469-156">Указывает механизм подачи для ячейки.</span><span class="sxs-lookup"><span data-stu-id="2c469-156">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="2c469-157">\_медиакапаЦитивалуе\_</span><span class="sxs-lookup"><span data-stu-id="2c469-157">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="2c469-158">строка</span><span class="sxs-lookup"><span data-stu-id="2c469-158">string</span></span><br/>  | <span data-ttu-id="2c469-159">Недоступно</span><span class="sxs-lookup"><span data-stu-id="2c469-159">n/a</span></span><br/>        | <span data-ttu-id="2c469-160">Высокий, Стандартный.</span><span class="sxs-lookup"><span data-stu-id="2c469-160">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="2c469-161">Указывает, является ли ячейка ячейкой высокой емкости (качественная).</span><span class="sxs-lookup"><span data-stu-id="2c469-161">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="2c469-162">\_медиасизеаутосенсевалуе\_</span><span class="sxs-lookup"><span data-stu-id="2c469-162">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="2c469-163">строка</span><span class="sxs-lookup"><span data-stu-id="2c469-163">string</span></span><br/>  | <span data-ttu-id="2c469-164">Недоступно</span><span class="sxs-lookup"><span data-stu-id="2c469-164">n/a</span></span><br/>        | <span data-ttu-id="2c469-165">Поддерживается, нет.</span><span class="sxs-lookup"><span data-stu-id="2c469-165">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="2c469-166">Указывает функцию автоматического датчика размера носителя для устройства.</span><span class="sxs-lookup"><span data-stu-id="2c469-166">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="2c469-167">\_медиатипеаутосенсевалуе\_</span><span class="sxs-lookup"><span data-stu-id="2c469-167">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="2c469-168">строка</span><span class="sxs-lookup"><span data-stu-id="2c469-168">string</span></span><br/>  | <span data-ttu-id="2c469-169">Недоступно</span><span class="sxs-lookup"><span data-stu-id="2c469-169">n/a</span></span><br/>        | <span data-ttu-id="2c469-170">Поддерживается, нет.</span><span class="sxs-lookup"><span data-stu-id="2c469-170">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="2c469-171">Указывает функцию автоматического датчика типа носителя для устройства.</span><span class="sxs-lookup"><span data-stu-id="2c469-171">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="2c469-172">\_медиашиткапаЦитивалуе\_</span><span class="sxs-lookup"><span data-stu-id="2c469-172">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="2c469-173">Целое число</span><span class="sxs-lookup"><span data-stu-id="2c469-173">integer</span></span><br/> | <span data-ttu-id="2c469-174">свойств</span><span class="sxs-lookup"><span data-stu-id="2c469-174">sheets</span></span><br/>     | <span data-ttu-id="2c469-175">Максимальное целочисленное ограничение, разрешенное устройством.</span><span class="sxs-lookup"><span data-stu-id="2c469-175">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="2c469-176">Указывает емкость носителя в количестве страниц (полный уровень) ячейки.</span><span class="sxs-lookup"><span data-stu-id="2c469-176">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="2c469-177">\_медиапасвалуе\_</span><span class="sxs-lookup"><span data-stu-id="2c469-177">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="2c469-178">строка</span><span class="sxs-lookup"><span data-stu-id="2c469-178">string</span></span><br/>  | <span data-ttu-id="2c469-179">Недоступно</span><span class="sxs-lookup"><span data-stu-id="2c469-179">n/a</span></span><br/>        | <span data-ttu-id="2c469-180">Прямая, серпентине.</span><span class="sxs-lookup"><span data-stu-id="2c469-180">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="2c469-181">Задает характеристики пути к носителю.</span><span class="sxs-lookup"><span data-stu-id="2c469-181">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="2c469-182">\_фидфацевалуе\_</span><span class="sxs-lookup"><span data-stu-id="2c469-182">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="2c469-183">строка</span><span class="sxs-lookup"><span data-stu-id="2c469-183">string</span></span><br/>  | <span data-ttu-id="2c469-184">Недоступно</span><span class="sxs-lookup"><span data-stu-id="2c469-184">n/a</span></span><br/>        | <span data-ttu-id="2c469-185">Фацеуп, Фацедовн</span><span class="sxs-lookup"><span data-stu-id="2c469-185">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="2c469-186">Указывает, следует ли печатать мультимедиа лицевой или лицевой стороны.</span><span class="sxs-lookup"><span data-stu-id="2c469-186">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="2c469-187">\_фиддиректионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="2c469-187">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="2c469-188">строка</span><span class="sxs-lookup"><span data-stu-id="2c469-188">string</span></span><br/>  | <span data-ttu-id="2c469-189">Недоступно</span><span class="sxs-lookup"><span data-stu-id="2c469-189">n/a</span></span><br/>        | <span data-ttu-id="2c469-190">Лонжеджефирст, Шортеджефирст</span><span class="sxs-lookup"><span data-stu-id="2c469-190">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="2c469-191">Указывает, будет ли мультимедиа сначала выдаваться длинная или короткая сторона.</span><span class="sxs-lookup"><span data-stu-id="2c469-191">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2c469-192">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="2c469-192">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2c469-193">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="2c469-193">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2c469-194">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="2c469-194">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="2c469-195">См. также</span><span class="sxs-lookup"><span data-stu-id="2c469-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c469-196">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="2c469-196">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




