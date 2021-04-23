---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: жобнупаллдокументсконтигуаусли
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e307883a25fc977b9086259789c04f4b3a7cbf
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351995"
---
# <a name="jobnupalldocumentscontiguously"></a><span data-ttu-id="890a1-104">жобнупаллдокументсконтигуаусли</span><span class="sxs-lookup"><span data-stu-id="890a1-104">JobNUpAllDocumentsContiguously</span></span>

<span data-ttu-id="890a1-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="890a1-105">This topic is not current.</span></span> <span data-ttu-id="890a1-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="890a1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="890a1-107">Описывает вывод нескольких логических страниц на один физический лист.</span><span class="sxs-lookup"><span data-stu-id="890a1-107">Describes the output of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="890a1-108">Все документы в задании компилируются последовательно.</span><span class="sxs-lookup"><span data-stu-id="890a1-108">All documents in the job are compiled together contiguously.</span></span> <span data-ttu-id="890a1-109">Жобнупаллдокументсконтигуаусли и Документнуп являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="890a1-109">JobNUpAllDocumentsContiguously and DocumentNUp are mutually exclusive.</span></span> <span data-ttu-id="890a1-110">Драйвер определяет обработку ограничений между этими ключевыми словами.</span><span class="sxs-lookup"><span data-stu-id="890a1-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="890a1-111">На следующей схеме показан пример с документом 1, содержащим 3 страницы, а также документ 2, содержащий 2 страницы.</span><span class="sxs-lookup"><span data-stu-id="890a1-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="890a1-112">Каждый документ в задании последовательно расдуплексует.</span><span class="sxs-lookup"><span data-stu-id="890a1-112">Each document in the job is duplexed contiguously.</span></span> <span data-ttu-id="890a1-113">В этом примере показаны направления, представленные в виде параметра Ригхтботтом.</span><span class="sxs-lookup"><span data-stu-id="890a1-113">The presentation directions shown in the example is the RightBottom option.</span></span>

![Диаграмма, показывающая, как размещаются страницы документа на одном листе, основанном на параметре документнуп](images/local-1242234459-jobduplexpics.gif)

-   [<span data-ttu-id="890a1-115">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="890a1-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="890a1-116">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="890a1-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="890a1-117">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="890a1-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="890a1-118">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="890a1-118">Element Information</span></span>



| <span data-ttu-id="890a1-119">Имя</span><span class="sxs-lookup"><span data-stu-id="890a1-119">Name</span></span>                       |                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="890a1-120">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="890a1-120">Element Type</span></span> <br/>   | <span data-ttu-id="890a1-121">Функция</span><span class="sxs-lookup"><span data-stu-id="890a1-121">Feature</span></span><br/>                                                                                                                             |
| <span data-ttu-id="890a1-122">Префикс области</span><span class="sxs-lookup"><span data-stu-id="890a1-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="890a1-123">Задание</span><span class="sxs-lookup"><span data-stu-id="890a1-123">Job</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="890a1-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="890a1-124">Notes</span></span> <br/>          | <span data-ttu-id="890a1-125">Верхняя, Нижняя, левая и правая относительные относятся к Пажеимажеаблесизе, где Топлефт обозначается исходными значениями высоты и ширины.</span><span class="sxs-lookup"><span data-stu-id="890a1-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the height and width.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="890a1-126">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="890a1-126">Structural Content</span></span>

<span data-ttu-id="890a1-127">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="890a1-127">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="890a1-128">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="890a1-128">Structure Variables</span></span>

<span data-ttu-id="890a1-129">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="890a1-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="890a1-130">Имя</span><span class="sxs-lookup"><span data-stu-id="890a1-130">Name</span></span>                                           | <span data-ttu-id="890a1-131">Тип данных</span><span class="sxs-lookup"><span data-stu-id="890a1-131">Data type</span></span>          | <span data-ttu-id="890a1-132">Unit</span><span class="sxs-lookup"><span data-stu-id="890a1-132">Unit</span></span>                     | <span data-ttu-id="890a1-133">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="890a1-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="890a1-134">Сводка</span><span class="sxs-lookup"><span data-stu-id="890a1-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="890a1-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="890a1-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="890a1-136">строка</span><span class="sxs-lookup"><span data-stu-id="890a1-136">string</span></span><br/>  | <span data-ttu-id="890a1-137">characters</span><span class="sxs-lookup"><span data-stu-id="890a1-137">characters</span></span><br/>    | <span data-ttu-id="890a1-138">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="890a1-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="890a1-139">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="890a1-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="890a1-140">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="890a1-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="890a1-141">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="890a1-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="890a1-142">строка</span><span class="sxs-lookup"><span data-stu-id="890a1-142">string</span></span><br/>  | <span data-ttu-id="890a1-143">Недоступно</span><span class="sxs-lookup"><span data-stu-id="890a1-143">n/a</span></span><br/>           | <span data-ttu-id="890a1-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="890a1-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="890a1-145">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="890a1-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="890a1-146">\_пажеспершитвалуе\_</span><span class="sxs-lookup"><span data-stu-id="890a1-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="890a1-147">Целое число</span><span class="sxs-lookup"><span data-stu-id="890a1-147">integer</span></span><br/> | <span data-ttu-id="890a1-148">Логические страницы</span><span class="sxs-lookup"><span data-stu-id="890a1-148">Logical pages</span></span><br/> | <span data-ttu-id="890a1-149">Все целые числа (больше нуля).</span><span class="sxs-lookup"><span data-stu-id="890a1-149">All integers (Greater than zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="890a1-150">Указывает число логических страниц на физический лист.</span><span class="sxs-lookup"><span data-stu-id="890a1-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="890a1-151">Поддерживаемым набором может быть любой набор целых чисел, например</span><span class="sxs-lookup"><span data-stu-id="890a1-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="890a1-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="890a1-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="890a1-153">\_пресентатиондиректионоптионнаме\_</span><span class="sxs-lookup"><span data-stu-id="890a1-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="890a1-154">строка</span><span class="sxs-lookup"><span data-stu-id="890a1-154">string</span></span><br/>  | <span data-ttu-id="890a1-155">characters</span><span class="sxs-lookup"><span data-stu-id="890a1-155">characters</span></span><br/>    | <span data-ttu-id="890a1-156">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="890a1-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="890a1-157">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="890a1-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="890a1-158">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="890a1-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="890a1-159">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="890a1-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="890a1-160">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="890a1-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="890a1-161">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="890a1-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="890a1-162">См. также</span><span class="sxs-lookup"><span data-stu-id="890a1-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="890a1-163">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="890a1-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




