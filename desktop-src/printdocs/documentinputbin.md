---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: документинпутбин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4459f621ac4455a69e891c2eeda6f785b6d8b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105713351"
---
# <a name="documentinputbin"></a><span data-ttu-id="5ae7b-104">документинпутбин</span><span class="sxs-lookup"><span data-stu-id="5ae7b-104">DocumentInputBin</span></span>

<span data-ttu-id="5ae7b-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-105">This topic is not current.</span></span> <span data-ttu-id="5ae7b-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5ae7b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5ae7b-107">Описывает установленную входную ячейку на устройстве или полный список поддерживаемых ячеек для устройства.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="5ae7b-108">Ключевые слова Жобинпутбин, Документинпутбин и Пажеинпутбин являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="5ae7b-109">Оба значения не должны одновременно указываться в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="5ae7b-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5ae7b-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="5ae7b-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="5ae7b-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="5ae7b-112">XML-содержимое</span><span class="sxs-lookup"><span data-stu-id="5ae7b-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5ae7b-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5ae7b-113">Element Information</span></span>



| <span data-ttu-id="5ae7b-114">Имя</span><span class="sxs-lookup"><span data-stu-id="5ae7b-114">Name</span></span>                       |                                                                                                                                |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae7b-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="5ae7b-115">Element Type</span></span> <br/>   | <span data-ttu-id="5ae7b-116">Функция</span><span class="sxs-lookup"><span data-stu-id="5ae7b-116">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="5ae7b-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="5ae7b-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5ae7b-118">Документ</span><span class="sxs-lookup"><span data-stu-id="5ae7b-118">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="5ae7b-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="5ae7b-119">Notes</span></span> <br/>          | <span data-ttu-id="5ae7b-120">Поддерживаемые ячейки, которые не установлены в настоящий момент, должны помечаться как ограниченные в документе PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-120">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="5ae7b-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="5ae7b-121">Structural Content</span></span>

<span data-ttu-id="5ae7b-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="5ae7b-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="5ae7b-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="5ae7b-123">Structure Variables</span></span>

<span data-ttu-id="5ae7b-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5ae7b-125">Имя</span><span class="sxs-lookup"><span data-stu-id="5ae7b-125">Name</span></span>                                   | <span data-ttu-id="5ae7b-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5ae7b-126">Data type</span></span>          | <span data-ttu-id="5ae7b-127">Unit</span><span class="sxs-lookup"><span data-stu-id="5ae7b-127">Unit</span></span>                  | <span data-ttu-id="5ae7b-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="5ae7b-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5ae7b-129">Сводка</span><span class="sxs-lookup"><span data-stu-id="5ae7b-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae7b-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5ae7b-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="5ae7b-131">строка</span><span class="sxs-lookup"><span data-stu-id="5ae7b-131">string</span></span><br/>  | <span data-ttu-id="5ae7b-132">characters</span><span class="sxs-lookup"><span data-stu-id="5ae7b-132">characters</span></span><br/> | <span data-ttu-id="5ae7b-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="5ae7b-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5ae7b-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5ae7b-135">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="5ae7b-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="5ae7b-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="5ae7b-137">строка</span><span class="sxs-lookup"><span data-stu-id="5ae7b-137">string</span></span><br/>  | <span data-ttu-id="5ae7b-138">Недоступно</span><span class="sxs-lookup"><span data-stu-id="5ae7b-138">n/a</span></span><br/>        | <span data-ttu-id="5ae7b-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5ae7b-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="5ae7b-141">\_енвелопеоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="5ae7b-141">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="5ae7b-142">строка</span><span class="sxs-lookup"><span data-stu-id="5ae7b-142">string</span></span><br/>  | <span data-ttu-id="5ae7b-143">Недоступно</span><span class="sxs-lookup"><span data-stu-id="5ae7b-143">n/a</span></span><br/>        | <span data-ttu-id="5ae7b-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5ae7b-145">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-145">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="5ae7b-146">\_бинтипевалуе\_</span><span class="sxs-lookup"><span data-stu-id="5ae7b-146">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="5ae7b-147">строка</span><span class="sxs-lookup"><span data-stu-id="5ae7b-147">string</span></span><br/>  | <span data-ttu-id="5ae7b-148">Недоступно</span><span class="sxs-lookup"><span data-stu-id="5ae7b-148">n/a</span></span><br/>        | <span data-ttu-id="5ae7b-149">Континуаусфид, Шитфид.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-149">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="5ae7b-150">Указывает тип ячейки.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-150">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="5ae7b-151">\_фидтипевалуе\_</span><span class="sxs-lookup"><span data-stu-id="5ae7b-151">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="5ae7b-152">строка</span><span class="sxs-lookup"><span data-stu-id="5ae7b-152">string</span></span><br/>  | <span data-ttu-id="5ae7b-153">Недоступно</span><span class="sxs-lookup"><span data-stu-id="5ae7b-153">n/a</span></span><br/>        | <span data-ttu-id="5ae7b-154">Автоматически, вручную.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-154">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="5ae7b-155">Указывает механизм подачи для ячейки.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-155">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="5ae7b-156">\_медиакапаЦитивалуе\_</span><span class="sxs-lookup"><span data-stu-id="5ae7b-156">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="5ae7b-157">Целое число</span><span class="sxs-lookup"><span data-stu-id="5ae7b-157">integer</span></span><br/> | <span data-ttu-id="5ae7b-158">свойств</span><span class="sxs-lookup"><span data-stu-id="5ae7b-158">sheets</span></span><br/>     | <span data-ttu-id="5ae7b-159">Максимальное целочисленное ограничение, разрешенное устройством.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-159">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="5ae7b-160">Указывает, является ли ячейка ячейкой высокой емкости (качественная).</span><span class="sxs-lookup"><span data-stu-id="5ae7b-160">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="5ae7b-161">\_медиасизеаутосенсевалуе\_</span><span class="sxs-lookup"><span data-stu-id="5ae7b-161">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="5ae7b-162">строка</span><span class="sxs-lookup"><span data-stu-id="5ae7b-162">string</span></span><br/>  | <span data-ttu-id="5ae7b-163">Недоступно</span><span class="sxs-lookup"><span data-stu-id="5ae7b-163">n/a</span></span><br/>        | <span data-ttu-id="5ae7b-164">Поддерживается, нет.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-164">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="5ae7b-165">Указывает функцию автоматического датчика размера носителя для устройства.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-165">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="5ae7b-166">\_медиатипеаутосенсевалуе\_</span><span class="sxs-lookup"><span data-stu-id="5ae7b-166">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="5ae7b-167">строка</span><span class="sxs-lookup"><span data-stu-id="5ae7b-167">string</span></span><br/>  | <span data-ttu-id="5ae7b-168">Недоступно</span><span class="sxs-lookup"><span data-stu-id="5ae7b-168">n/a</span></span><br/>        | <span data-ttu-id="5ae7b-169">Поддерживается, нет.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-169">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="5ae7b-170">Указывает емкость носителя в количестве страниц (полный уровень) ячейки.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-170">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="5ae7b-171">\_медиапасвалуе\_</span><span class="sxs-lookup"><span data-stu-id="5ae7b-171">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="5ae7b-172">строка</span><span class="sxs-lookup"><span data-stu-id="5ae7b-172">string</span></span><br/>  | <span data-ttu-id="5ae7b-173">Недоступно</span><span class="sxs-lookup"><span data-stu-id="5ae7b-173">n/a</span></span><br/>        | <span data-ttu-id="5ae7b-174">Прямая, серпентине.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-174">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="5ae7b-175">Задает характеристики пути к носителю.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-175">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="5ae7b-176">\_фидфацевалуе\_</span><span class="sxs-lookup"><span data-stu-id="5ae7b-176">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="5ae7b-177">строка</span><span class="sxs-lookup"><span data-stu-id="5ae7b-177">string</span></span><br/>  | <span data-ttu-id="5ae7b-178">Недоступно</span><span class="sxs-lookup"><span data-stu-id="5ae7b-178">n/a</span></span><br/>        | <span data-ttu-id="5ae7b-179">Фацеуп, Фацедовн</span><span class="sxs-lookup"><span data-stu-id="5ae7b-179">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="5ae7b-180">Указывает, следует ли печатать мультимедиа лицевой или лицевой стороны.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-180">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="5ae7b-181">\_фиддиректионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="5ae7b-181">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="5ae7b-182">строка</span><span class="sxs-lookup"><span data-stu-id="5ae7b-182">string</span></span><br/>  | <span data-ttu-id="5ae7b-183">Недоступно</span><span class="sxs-lookup"><span data-stu-id="5ae7b-183">n/a</span></span><br/>        | <span data-ttu-id="5ae7b-184">Лонжеджефирст, Шортеджефирст</span><span class="sxs-lookup"><span data-stu-id="5ae7b-184">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="5ae7b-185">Указывает, будет ли мультимедиа сначала выдаваться длинная или короткая сторона.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-185">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5ae7b-186">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5ae7b-186">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5ae7b-187">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="5ae7b-187">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5ae7b-188">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="5ae7b-188">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="5ae7b-189">См. также</span><span class="sxs-lookup"><span data-stu-id="5ae7b-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ae7b-190">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="5ae7b-190">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




