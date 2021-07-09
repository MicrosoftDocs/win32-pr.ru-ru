---
description: Получение сведений о настраиваемом пользователем элементе Пажеинпутбин. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 78eb3119-a52f-4ff8-83bb-903e181c8a11
title: пажеинпутбин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc53d377106b95b26e694d531af2952cea98a8b1
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549172"
---
# <a name="pageinputbin"></a><span data-ttu-id="6f672-105">пажеинпутбин</span><span class="sxs-lookup"><span data-stu-id="6f672-105">PageInputBin</span></span>

<span data-ttu-id="6f672-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="6f672-106">This topic is not current.</span></span> <span data-ttu-id="6f672-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6f672-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6f672-108">Описывает установленную входную ячейку на устройстве или полный список поддерживаемых ячеек для устройства.</span><span class="sxs-lookup"><span data-stu-id="6f672-108">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="6f672-109">Разрешает указание входной ячейки для каждой страницы.</span><span class="sxs-lookup"><span data-stu-id="6f672-109">Allows specification of input bin on a per page basis.</span></span> <span data-ttu-id="6f672-110">Ключевые слова Жобинпутбин, Документинпутбин и Пажеинпутбин являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="6f672-110">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="6f672-111">Оба значения не должны одновременно указываться в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="6f672-111">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="6f672-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6f672-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6f672-113">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="6f672-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6f672-114">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="6f672-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6f672-115">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6f672-115">Element Information</span></span>



| <span data-ttu-id="6f672-116">Имя</span><span class="sxs-lookup"><span data-stu-id="6f672-116">Name</span></span> | <span data-ttu-id="6f672-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6f672-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="6f672-118">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="6f672-118">Element Type</span></span> <br/>   | <span data-ttu-id="6f672-119">Компонент</span><span class="sxs-lookup"><span data-stu-id="6f672-119">Feature</span></span><br/> |
| <span data-ttu-id="6f672-120">Префикс области</span><span class="sxs-lookup"><span data-stu-id="6f672-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6f672-121">Страница</span><span class="sxs-lookup"><span data-stu-id="6f672-121">Page</span></span><br/>    |
| <span data-ttu-id="6f672-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="6f672-122">Notes</span></span> <br/>          | <span data-ttu-id="6f672-123">Нет</span><span class="sxs-lookup"><span data-stu-id="6f672-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="6f672-124">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="6f672-124">Structural Content</span></span>

<span data-ttu-id="6f672-125">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="6f672-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageInputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="6f672-126">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="6f672-126">Structure Variables</span></span>

<span data-ttu-id="6f672-127">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="6f672-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6f672-128">Имя</span><span class="sxs-lookup"><span data-stu-id="6f672-128">Name</span></span>                                   | <span data-ttu-id="6f672-129">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6f672-129">Data type</span></span>          | <span data-ttu-id="6f672-130">Unit</span><span class="sxs-lookup"><span data-stu-id="6f672-130">Unit</span></span>                  | <span data-ttu-id="6f672-131">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="6f672-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6f672-132">Итоги</span><span class="sxs-lookup"><span data-stu-id="6f672-132">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6f672-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6f672-133">\_OptionName\_</span></span><br/>              | <span data-ttu-id="6f672-134">строка</span><span class="sxs-lookup"><span data-stu-id="6f672-134">string</span></span><br/>  | <span data-ttu-id="6f672-135">characters</span><span class="sxs-lookup"><span data-stu-id="6f672-135">characters</span></span><br/> | <span data-ttu-id="6f672-136">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="6f672-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6f672-137">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6f672-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6f672-138">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="6f672-138">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="6f672-139">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="6f672-139">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="6f672-140">строка</span><span class="sxs-lookup"><span data-stu-id="6f672-140">string</span></span><br/>  | <span data-ttu-id="6f672-141">Н/Д</span><span class="sxs-lookup"><span data-stu-id="6f672-141">n/a</span></span><br/>        | <span data-ttu-id="6f672-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="6f672-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6f672-143">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="6f672-143">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="6f672-144">\_енвелопеоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="6f672-144">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="6f672-145">строка</span><span class="sxs-lookup"><span data-stu-id="6f672-145">string</span></span><br/>  | <span data-ttu-id="6f672-146">Н/Д</span><span class="sxs-lookup"><span data-stu-id="6f672-146">n/a</span></span><br/>        | <span data-ttu-id="6f672-147">True, False.</span><span class="sxs-lookup"><span data-stu-id="6f672-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6f672-148">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="6f672-148">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="6f672-149">\_бинтипевалуе\_</span><span class="sxs-lookup"><span data-stu-id="6f672-149">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="6f672-150">строка</span><span class="sxs-lookup"><span data-stu-id="6f672-150">string</span></span><br/>  | <span data-ttu-id="6f672-151">Н/Д</span><span class="sxs-lookup"><span data-stu-id="6f672-151">n/a</span></span><br/>        | <span data-ttu-id="6f672-152">Континуаусфид, Шитфид.</span><span class="sxs-lookup"><span data-stu-id="6f672-152">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="6f672-153">Указывает тип ячейки.</span><span class="sxs-lookup"><span data-stu-id="6f672-153">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="6f672-154">\_фидтипевалуе\_</span><span class="sxs-lookup"><span data-stu-id="6f672-154">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="6f672-155">строка</span><span class="sxs-lookup"><span data-stu-id="6f672-155">string</span></span><br/>  | <span data-ttu-id="6f672-156">Н/Д</span><span class="sxs-lookup"><span data-stu-id="6f672-156">n/a</span></span><br/>        | <span data-ttu-id="6f672-157">Автоматически, вручную.</span><span class="sxs-lookup"><span data-stu-id="6f672-157">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="6f672-158">Указывает механизм подачи для ячейки.</span><span class="sxs-lookup"><span data-stu-id="6f672-158">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="6f672-159">\_медиакапаЦитивалуе\_</span><span class="sxs-lookup"><span data-stu-id="6f672-159">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="6f672-160">строка</span><span class="sxs-lookup"><span data-stu-id="6f672-160">string</span></span><br/>  | <span data-ttu-id="6f672-161">Н/Д</span><span class="sxs-lookup"><span data-stu-id="6f672-161">n/a</span></span><br/>        | <span data-ttu-id="6f672-162">Высокий, Стандартный.</span><span class="sxs-lookup"><span data-stu-id="6f672-162">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="6f672-163">Указывает, является ли ячейка ячейкой высокой емкости (качественная).</span><span class="sxs-lookup"><span data-stu-id="6f672-163">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="6f672-164">\_медиасизеаутосенсевалуе\_</span><span class="sxs-lookup"><span data-stu-id="6f672-164">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="6f672-165">строка</span><span class="sxs-lookup"><span data-stu-id="6f672-165">string</span></span><br/>  | <span data-ttu-id="6f672-166">Н/Д</span><span class="sxs-lookup"><span data-stu-id="6f672-166">n/a</span></span><br/>        | <span data-ttu-id="6f672-167">Поддерживается, нет.</span><span class="sxs-lookup"><span data-stu-id="6f672-167">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="6f672-168">Указывает функцию автоматического датчика размера носителя для устройства.</span><span class="sxs-lookup"><span data-stu-id="6f672-168">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="6f672-169">\_медиатипеаутосенсевалуе\_</span><span class="sxs-lookup"><span data-stu-id="6f672-169">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="6f672-170">строка</span><span class="sxs-lookup"><span data-stu-id="6f672-170">string</span></span><br/>  | <span data-ttu-id="6f672-171">Н/Д</span><span class="sxs-lookup"><span data-stu-id="6f672-171">n/a</span></span><br/>        | <span data-ttu-id="6f672-172">Поддерживается, нет.</span><span class="sxs-lookup"><span data-stu-id="6f672-172">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="6f672-173">Указывает функцию автоматического датчика типа носителя для устройства.</span><span class="sxs-lookup"><span data-stu-id="6f672-173">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="6f672-174">\_медиашиткапаЦитивалуе\_</span><span class="sxs-lookup"><span data-stu-id="6f672-174">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="6f672-175">Целое число</span><span class="sxs-lookup"><span data-stu-id="6f672-175">integer</span></span><br/> | <span data-ttu-id="6f672-176">свойств</span><span class="sxs-lookup"><span data-stu-id="6f672-176">sheets</span></span><br/>     | <span data-ttu-id="6f672-177">Максимальное целочисленное ограничение, разрешенное устройством.</span><span class="sxs-lookup"><span data-stu-id="6f672-177">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="6f672-178">Указывает емкость носителя в количестве страниц (полный уровень) ячейки.</span><span class="sxs-lookup"><span data-stu-id="6f672-178">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="6f672-179">\_медиапасвалуе\_</span><span class="sxs-lookup"><span data-stu-id="6f672-179">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="6f672-180">строка</span><span class="sxs-lookup"><span data-stu-id="6f672-180">string</span></span><br/>  | <span data-ttu-id="6f672-181">Н/Д</span><span class="sxs-lookup"><span data-stu-id="6f672-181">n/a</span></span><br/>        | <span data-ttu-id="6f672-182">Прямая, серпентине.</span><span class="sxs-lookup"><span data-stu-id="6f672-182">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="6f672-183">Задает характеристики пути к носителю.</span><span class="sxs-lookup"><span data-stu-id="6f672-183">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="6f672-184">\_фидфацевалуе\_</span><span class="sxs-lookup"><span data-stu-id="6f672-184">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="6f672-185">строка</span><span class="sxs-lookup"><span data-stu-id="6f672-185">string</span></span><br/>  | <span data-ttu-id="6f672-186">Н/Д</span><span class="sxs-lookup"><span data-stu-id="6f672-186">n/a</span></span><br/>        | <span data-ttu-id="6f672-187">Фацеуп, Фацедовн</span><span class="sxs-lookup"><span data-stu-id="6f672-187">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="6f672-188">Указывает, следует ли печатать мультимедиа лицевой или лицевой стороны.</span><span class="sxs-lookup"><span data-stu-id="6f672-188">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="6f672-189">\_фиддиректионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="6f672-189">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="6f672-190">строка</span><span class="sxs-lookup"><span data-stu-id="6f672-190">string</span></span><br/>  | <span data-ttu-id="6f672-191">Н/Д</span><span class="sxs-lookup"><span data-stu-id="6f672-191">n/a</span></span><br/>        | <span data-ttu-id="6f672-192">Лонжеджефирст, Шортеджефирст</span><span class="sxs-lookup"><span data-stu-id="6f672-192">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="6f672-193">Указывает, будет ли мультимедиа сначала выдаваться длинная или короткая сторона.</span><span class="sxs-lookup"><span data-stu-id="6f672-193">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6f672-194">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="6f672-194">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6f672-195">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="6f672-195">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6f672-196">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="6f672-196">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageInputBin">
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

## <a name="related-topics"></a><span data-ttu-id="6f672-197">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="6f672-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f672-198">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="6f672-198">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




