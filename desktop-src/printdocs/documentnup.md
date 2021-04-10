---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: документнуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fdf22fa557ce1da4fde20ad1d8ea14625a1b77
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104273371"
---
# <a name="documentnup"></a><span data-ttu-id="e8fc3-104">документнуп</span><span class="sxs-lookup"><span data-stu-id="e8fc3-104">DocumentNUp</span></span>

<span data-ttu-id="e8fc3-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-105">This topic is not current.</span></span> <span data-ttu-id="e8fc3-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e8fc3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e8fc3-107">Описывает выходные данные и формат нескольких логических страниц на одном физическом листе.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-107">Describes the output and format of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="e8fc3-108">Каждый документ компилируется отдельно.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-108">Each document is compiled separately.</span></span> <span data-ttu-id="e8fc3-109">Документнуп и Жобнупаллдокументсконтигуаусли являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-109">DocumentNUp and JobNUpAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="e8fc3-110">Драйвер определяет обработку ограничений между этими ключевыми словами.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="e8fc3-111">На следующей схеме показан пример с документом 1, содержащим 3 страницы, а также документ 2, содержащий 2 страницы.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="e8fc3-112">Каждый документ расдуплексен отдельно.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-112">Each document is duplexed separately.</span></span> <span data-ttu-id="e8fc3-113">Направление презентации, показанное ниже, является параметром Ригхтботтом.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-113">The presentation direction shown below is the RightBottom option.</span></span>

![Диаграмма, показывающая, как размещаются страницы документа на одном листе, основанном на параметре документнуп](images/local-1663869164-docduplex1.gif)

-   [<span data-ttu-id="e8fc3-115">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e8fc3-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e8fc3-116">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="e8fc3-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e8fc3-117">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="e8fc3-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e8fc3-118">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e8fc3-118">Element Information</span></span>



| <span data-ttu-id="e8fc3-119">Имя</span><span class="sxs-lookup"><span data-stu-id="e8fc3-119">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8fc3-120">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="e8fc3-120">Element Type</span></span> <br/>   | <span data-ttu-id="e8fc3-121">Функция</span><span class="sxs-lookup"><span data-stu-id="e8fc3-121">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="e8fc3-122">Префикс области</span><span class="sxs-lookup"><span data-stu-id="e8fc3-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e8fc3-123">Документ</span><span class="sxs-lookup"><span data-stu-id="e8fc3-123">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="e8fc3-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8fc3-124">Notes</span></span> <br/>          | <span data-ttu-id="e8fc3-125">Верхние, нижние, левые и правая относятся относительно Пажеимажеаблесизе, где Топлефт обозначается исходными значениями оси x и оси y.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="e8fc3-126">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="e8fc3-126">Structural Content</span></span>

<span data-ttu-id="e8fc3-127">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e8fc3-127">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_PagesPerSheetValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the ordering direction of the pages.  First direction followed by second direction. -->
  <psf:Feature name="psk:PresentationDirection">
    <psf:Option name="psk:_PresentationDirectionOptionName_" />
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="e8fc3-128">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="e8fc3-128">Structure Variables</span></span>

<span data-ttu-id="e8fc3-129">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e8fc3-130">Имя</span><span class="sxs-lookup"><span data-stu-id="e8fc3-130">Name</span></span>                                           | <span data-ttu-id="e8fc3-131">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e8fc3-131">Data type</span></span>          | <span data-ttu-id="e8fc3-132">Unit</span><span class="sxs-lookup"><span data-stu-id="e8fc3-132">Unit</span></span>                     | <span data-ttu-id="e8fc3-133">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="e8fc3-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e8fc3-134">Сводка</span><span class="sxs-lookup"><span data-stu-id="e8fc3-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8fc3-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e8fc3-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="e8fc3-136">строка</span><span class="sxs-lookup"><span data-stu-id="e8fc3-136">string</span></span><br/>  | <span data-ttu-id="e8fc3-137">characters</span><span class="sxs-lookup"><span data-stu-id="e8fc3-137">characters</span></span><br/>    | <span data-ttu-id="e8fc3-138">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="e8fc3-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e8fc3-139">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e8fc3-140">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="e8fc3-141">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="e8fc3-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="e8fc3-142">строка</span><span class="sxs-lookup"><span data-stu-id="e8fc3-142">string</span></span><br/>  | <span data-ttu-id="e8fc3-143">Недоступно</span><span class="sxs-lookup"><span data-stu-id="e8fc3-143">n/a</span></span><br/>           | <span data-ttu-id="e8fc3-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e8fc3-145">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="e8fc3-146">\_пажеспершитвалуе\_</span><span class="sxs-lookup"><span data-stu-id="e8fc3-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="e8fc3-147">Целое число</span><span class="sxs-lookup"><span data-stu-id="e8fc3-147">integer</span></span><br/> | <span data-ttu-id="e8fc3-148">Логические страницы</span><span class="sxs-lookup"><span data-stu-id="e8fc3-148">Logical pages</span></span><br/> | <span data-ttu-id="e8fc3-149">Все целые числа (больше нуля).</span><span class="sxs-lookup"><span data-stu-id="e8fc3-149">All integers (Greater than Zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="e8fc3-150">Указывает число логических страниц на физический лист.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="e8fc3-151">Поддерживаемым набором может быть любой набор целых чисел, например</span><span class="sxs-lookup"><span data-stu-id="e8fc3-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="e8fc3-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="e8fc3-153">\_пресентатиондиректионоптионнаме\_</span><span class="sxs-lookup"><span data-stu-id="e8fc3-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="e8fc3-154">строка</span><span class="sxs-lookup"><span data-stu-id="e8fc3-154">string</span></span><br/>  | <span data-ttu-id="e8fc3-155">characters</span><span class="sxs-lookup"><span data-stu-id="e8fc3-155">characters</span></span><br/>    | <span data-ttu-id="e8fc3-156">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="e8fc3-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e8fc3-157">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e8fc3-158">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e8fc3-159">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="e8fc3-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e8fc3-160">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="e8fc3-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e8fc3-161">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="e8fc3-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies format left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies format top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies format right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies format top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies format left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies format bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies format right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies format bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="e8fc3-162">См. также</span><span class="sxs-lookup"><span data-stu-id="e8fc3-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8fc3-163">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="e8fc3-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




