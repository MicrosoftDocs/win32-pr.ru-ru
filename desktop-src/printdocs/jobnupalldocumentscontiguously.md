---
description: Сведения об элементе Жобнупаллдокументсконтигуаусли, который описывает вывод нескольких логических страниц на один физический лист.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: жобнупаллдокументсконтигуаусли
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9106259c80a7efb89cc4481780bfb55af4f07e23
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408867"
---
# <a name="jobnupalldocumentscontiguously"></a><span data-ttu-id="39600-103">жобнупаллдокументсконтигуаусли</span><span class="sxs-lookup"><span data-stu-id="39600-103">JobNUpAllDocumentsContiguously</span></span>

<span data-ttu-id="39600-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="39600-104">This topic is not current.</span></span> <span data-ttu-id="39600-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="39600-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="39600-106">Описывает вывод нескольких логических страниц на один физический лист.</span><span class="sxs-lookup"><span data-stu-id="39600-106">Describes the output of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="39600-107">Все документы в задании компилируются последовательно.</span><span class="sxs-lookup"><span data-stu-id="39600-107">All documents in the job are compiled together contiguously.</span></span> <span data-ttu-id="39600-108">Жобнупаллдокументсконтигуаусли и Документнуп являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="39600-108">JobNUpAllDocumentsContiguously and DocumentNUp are mutually exclusive.</span></span> <span data-ttu-id="39600-109">Драйвер определяет обработку ограничений между этими ключевыми словами.</span><span class="sxs-lookup"><span data-stu-id="39600-109">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="39600-110">На следующей схеме показан пример с документом 1, содержащим 3 страницы, а также документ 2, содержащий 2 страницы.</span><span class="sxs-lookup"><span data-stu-id="39600-110">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="39600-111">Каждый документ в задании последовательно расдуплексует.</span><span class="sxs-lookup"><span data-stu-id="39600-111">Each document in the job is duplexed contiguously.</span></span> <span data-ttu-id="39600-112">В этом примере показаны направления, представленные в виде параметра Ригхтботтом.</span><span class="sxs-lookup"><span data-stu-id="39600-112">The presentation directions shown in the example is the RightBottom option.</span></span>

![Диаграмма, показывающая, как размещаются страницы документа на одном листе, основанном на параметре документнуп](images/local-1242234459-jobduplexpics.gif)

-   [<span data-ttu-id="39600-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="39600-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="39600-115">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="39600-115">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="39600-116">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="39600-116">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="39600-117">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="39600-117">Element Information</span></span>



| <span data-ttu-id="39600-118">Имя</span><span class="sxs-lookup"><span data-stu-id="39600-118">Name</span></span> | <span data-ttu-id="39600-119">Значение</span><span class="sxs-lookup"><span data-stu-id="39600-119">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39600-120">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="39600-120">Element Type</span></span> <br/>   | <span data-ttu-id="39600-121">Компонент</span><span class="sxs-lookup"><span data-stu-id="39600-121">Feature</span></span><br/>                                                                                                                             |
| <span data-ttu-id="39600-122">Префикс области</span><span class="sxs-lookup"><span data-stu-id="39600-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="39600-123">Задание</span><span class="sxs-lookup"><span data-stu-id="39600-123">Job</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="39600-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="39600-124">Notes</span></span> <br/>          | <span data-ttu-id="39600-125">Верхняя, Нижняя, левая и правая относительные относятся к Пажеимажеаблесизе, где Топлефт обозначается исходными значениями высоты и ширины.</span><span class="sxs-lookup"><span data-stu-id="39600-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the height and width.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="39600-126">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="39600-126">Structural Content</span></span>

<span data-ttu-id="39600-127">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="39600-127">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
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

## <a name="structure-variables"></a><span data-ttu-id="39600-128">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="39600-128">Structure Variables</span></span>

<span data-ttu-id="39600-129">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="39600-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="39600-130">Имя</span><span class="sxs-lookup"><span data-stu-id="39600-130">Name</span></span>                                           | <span data-ttu-id="39600-131">Тип данных</span><span class="sxs-lookup"><span data-stu-id="39600-131">Data type</span></span>          | <span data-ttu-id="39600-132">Unit</span><span class="sxs-lookup"><span data-stu-id="39600-132">Unit</span></span>                     | <span data-ttu-id="39600-133">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="39600-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="39600-134">Итоги</span><span class="sxs-lookup"><span data-stu-id="39600-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39600-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="39600-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="39600-136">строка</span><span class="sxs-lookup"><span data-stu-id="39600-136">string</span></span><br/>  | <span data-ttu-id="39600-137">characters</span><span class="sxs-lookup"><span data-stu-id="39600-137">characters</span></span><br/>    | <span data-ttu-id="39600-138">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="39600-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="39600-139">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="39600-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="39600-140">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="39600-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="39600-141">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="39600-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="39600-142">строка</span><span class="sxs-lookup"><span data-stu-id="39600-142">string</span></span><br/>  | <span data-ttu-id="39600-143">Недоступно</span><span class="sxs-lookup"><span data-stu-id="39600-143">n/a</span></span><br/>           | <span data-ttu-id="39600-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="39600-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="39600-145">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="39600-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="39600-146">\_пажеспершитвалуе\_</span><span class="sxs-lookup"><span data-stu-id="39600-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="39600-147">Целое число</span><span class="sxs-lookup"><span data-stu-id="39600-147">integer</span></span><br/> | <span data-ttu-id="39600-148">Логические страницы</span><span class="sxs-lookup"><span data-stu-id="39600-148">Logical pages</span></span><br/> | <span data-ttu-id="39600-149">Все целые числа (больше нуля).</span><span class="sxs-lookup"><span data-stu-id="39600-149">All integers (Greater than zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="39600-150">Указывает число логических страниц на физический лист.</span><span class="sxs-lookup"><span data-stu-id="39600-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="39600-151">Поддерживаемым набором может быть любой набор целых чисел, например</span><span class="sxs-lookup"><span data-stu-id="39600-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="39600-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="39600-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="39600-153">\_пресентатиондиректионоптионнаме\_</span><span class="sxs-lookup"><span data-stu-id="39600-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="39600-154">строка</span><span class="sxs-lookup"><span data-stu-id="39600-154">string</span></span><br/>  | <span data-ttu-id="39600-155">characters</span><span class="sxs-lookup"><span data-stu-id="39600-155">characters</span></span><br/>    | <span data-ttu-id="39600-156">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="39600-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="39600-157">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="39600-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="39600-158">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="39600-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="39600-159">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="39600-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="39600-160">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="39600-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="39600-161">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="39600-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="39600-162">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="39600-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39600-163">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="39600-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




