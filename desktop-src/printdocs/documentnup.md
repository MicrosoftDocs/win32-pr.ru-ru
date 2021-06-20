---
description: Сведения об элементе Документнуп, который описывает выходные данные и формат нескольких логических страниц на одном физическом листе.
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: документнуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b49bd4fa3eb9f2b3b0083fc8022dbd6f41d090e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409267"
---
# <a name="documentnup"></a><span data-ttu-id="2f6fb-103">документнуп</span><span class="sxs-lookup"><span data-stu-id="2f6fb-103">DocumentNUp</span></span>

<span data-ttu-id="2f6fb-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-104">This topic is not current.</span></span> <span data-ttu-id="2f6fb-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2f6fb-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2f6fb-106">Описывает выходные данные и формат нескольких логических страниц на одном физическом листе.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-106">Describes the output and format of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="2f6fb-107">Каждый документ компилируется отдельно.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-107">Each document is compiled separately.</span></span> <span data-ttu-id="2f6fb-108">Документнуп и Жобнупаллдокументсконтигуаусли являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-108">DocumentNUp and JobNUpAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="2f6fb-109">Драйвер определяет обработку ограничений между этими ключевыми словами.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-109">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="2f6fb-110">На следующей схеме показан пример с документом 1, содержащим 3 страницы, а также документ 2, содержащий 2 страницы.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-110">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="2f6fb-111">Каждый документ расдуплексен отдельно.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-111">Each document is duplexed separately.</span></span> <span data-ttu-id="2f6fb-112">Направление презентации, показанное ниже, является параметром Ригхтботтом.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-112">The presentation direction shown below is the RightBottom option.</span></span>

![Диаграмма, показывающая, как размещаются страницы документа на одном листе, основанном на параметре документнуп](images/local-1663869164-docduplex1.gif)

-   [<span data-ttu-id="2f6fb-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2f6fb-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2f6fb-115">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="2f6fb-115">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2f6fb-116">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="2f6fb-116">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2f6fb-117">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2f6fb-117">Element Information</span></span>



| <span data-ttu-id="2f6fb-118">Имя</span><span class="sxs-lookup"><span data-stu-id="2f6fb-118">Name</span></span> | <span data-ttu-id="2f6fb-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2f6fb-119">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f6fb-120">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="2f6fb-120">Element Type</span></span> <br/>   | <span data-ttu-id="2f6fb-121">Компонент</span><span class="sxs-lookup"><span data-stu-id="2f6fb-121">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="2f6fb-122">Префикс области</span><span class="sxs-lookup"><span data-stu-id="2f6fb-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2f6fb-123">Документ</span><span class="sxs-lookup"><span data-stu-id="2f6fb-123">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="2f6fb-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="2f6fb-124">Notes</span></span> <br/>          | <span data-ttu-id="2f6fb-125">Верхние, нижние, левые и правая относятся относительно Пажеимажеаблесизе, где Топлефт обозначается исходными значениями оси x и оси y.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="2f6fb-126">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="2f6fb-126">Structural Content</span></span>

<span data-ttu-id="2f6fb-127">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2f6fb-127">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="2f6fb-128">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="2f6fb-128">Structure Variables</span></span>

<span data-ttu-id="2f6fb-129">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2f6fb-130">Имя</span><span class="sxs-lookup"><span data-stu-id="2f6fb-130">Name</span></span>                                           | <span data-ttu-id="2f6fb-131">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2f6fb-131">Data type</span></span>          | <span data-ttu-id="2f6fb-132">Unit</span><span class="sxs-lookup"><span data-stu-id="2f6fb-132">Unit</span></span>                     | <span data-ttu-id="2f6fb-133">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="2f6fb-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="2f6fb-134">Итоги</span><span class="sxs-lookup"><span data-stu-id="2f6fb-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f6fb-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="2f6fb-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="2f6fb-136">строка</span><span class="sxs-lookup"><span data-stu-id="2f6fb-136">string</span></span><br/>  | <span data-ttu-id="2f6fb-137">characters</span><span class="sxs-lookup"><span data-stu-id="2f6fb-137">characters</span></span><br/>    | <span data-ttu-id="2f6fb-138">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="2f6fb-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="2f6fb-139">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="2f6fb-140">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="2f6fb-141">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="2f6fb-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="2f6fb-142">строка</span><span class="sxs-lookup"><span data-stu-id="2f6fb-142">string</span></span><br/>  | <span data-ttu-id="2f6fb-143">Недоступно</span><span class="sxs-lookup"><span data-stu-id="2f6fb-143">n/a</span></span><br/>           | <span data-ttu-id="2f6fb-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="2f6fb-145">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="2f6fb-146">\_пажеспершитвалуе\_</span><span class="sxs-lookup"><span data-stu-id="2f6fb-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="2f6fb-147">Целое число</span><span class="sxs-lookup"><span data-stu-id="2f6fb-147">integer</span></span><br/> | <span data-ttu-id="2f6fb-148">Логические страницы</span><span class="sxs-lookup"><span data-stu-id="2f6fb-148">Logical pages</span></span><br/> | <span data-ttu-id="2f6fb-149">Все целые числа (больше нуля).</span><span class="sxs-lookup"><span data-stu-id="2f6fb-149">All integers (Greater than Zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="2f6fb-150">Указывает число логических страниц на физический лист.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="2f6fb-151">Поддерживаемым набором может быть любой набор целых чисел, например</span><span class="sxs-lookup"><span data-stu-id="2f6fb-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="2f6fb-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="2f6fb-153">\_пресентатиондиректионоптионнаме\_</span><span class="sxs-lookup"><span data-stu-id="2f6fb-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="2f6fb-154">строка</span><span class="sxs-lookup"><span data-stu-id="2f6fb-154">string</span></span><br/>  | <span data-ttu-id="2f6fb-155">characters</span><span class="sxs-lookup"><span data-stu-id="2f6fb-155">characters</span></span><br/>    | <span data-ttu-id="2f6fb-156">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="2f6fb-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="2f6fb-157">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="2f6fb-158">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2f6fb-159">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="2f6fb-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2f6fb-160">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2f6fb-161">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="2f6fb-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="2f6fb-162">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2f6fb-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f6fb-163">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="2f6fb-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




