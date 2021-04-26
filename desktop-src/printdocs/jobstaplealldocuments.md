---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: a6721c13-a3dc-4273-b40f-2a28184b04a9
title: жобстаплеаллдокументс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9abf6184c3164e0e5a1492911e15794ea7e1d948
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993911"
---
# <a name="jobstaplealldocuments"></a><span data-ttu-id="1de08-104">жобстаплеаллдокументс</span><span class="sxs-lookup"><span data-stu-id="1de08-104">JobStapleAllDocuments</span></span>

<span data-ttu-id="1de08-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="1de08-105">This topic is not current.</span></span> <span data-ttu-id="1de08-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1de08-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1de08-107">Описывает характеристики сшивания выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1de08-107">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="1de08-108">Все документы в задании будут сшиты вместе.</span><span class="sxs-lookup"><span data-stu-id="1de08-108">All documents in the job are stapled together.</span></span> <span data-ttu-id="1de08-109">Ключевые слова Жобстаплеаллдокументс и Документстапле являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="1de08-109">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="1de08-110">Драйвер определяет обработку ограничений между этими ключевыми словами.</span><span class="sxs-lookup"><span data-stu-id="1de08-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="1de08-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1de08-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1de08-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="1de08-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1de08-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="1de08-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1de08-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1de08-114">Element Information</span></span>



| <span data-ttu-id="1de08-115">Имя</span><span class="sxs-lookup"><span data-stu-id="1de08-115">Name</span></span> | <span data-ttu-id="1de08-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1de08-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1de08-117">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="1de08-117">Element Type</span></span> <br/>   | <span data-ttu-id="1de08-118">Компонент</span><span class="sxs-lookup"><span data-stu-id="1de08-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="1de08-119">Префикс области</span><span class="sxs-lookup"><span data-stu-id="1de08-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1de08-120">Задание</span><span class="sxs-lookup"><span data-stu-id="1de08-120">Job</span></span><br/>                                                                 |
| <span data-ttu-id="1de08-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="1de08-121">Notes</span></span> <br/>          | <span data-ttu-id="1de08-122">Верхняя, Нижняя, левая и правая относительные относятся к Пажеимажеаблесизе</span><span class="sxs-lookup"><span data-stu-id="1de08-122">Top, Bottom, Left, and Right are relative to the PageImageableSize</span></span> <br/> |



 

## <a name="structural-content"></a><span data-ttu-id="1de08-123">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="1de08-123">Structural Content</span></span>

<span data-ttu-id="1de08-124">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1de08-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:JobStapleAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:Angle" >
      <psf:Value xsi:type="xs:integer">_AngleValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_SheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="1de08-125">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="1de08-125">Structure Variables</span></span>

<span data-ttu-id="1de08-126">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="1de08-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1de08-127">Имя</span><span class="sxs-lookup"><span data-stu-id="1de08-127">Name</span></span>                               | <span data-ttu-id="1de08-128">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1de08-128">Data type</span></span>          | <span data-ttu-id="1de08-129">Unit</span><span class="sxs-lookup"><span data-stu-id="1de08-129">Unit</span></span>                       | <span data-ttu-id="1de08-130">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="1de08-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1de08-131">Сводка</span><span class="sxs-lookup"><span data-stu-id="1de08-131">Summary</span></span>                                                                                                                                               |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1de08-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1de08-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="1de08-133">строка</span><span class="sxs-lookup"><span data-stu-id="1de08-133">string</span></span><br/>  | <span data-ttu-id="1de08-134">Characters</span><span class="sxs-lookup"><span data-stu-id="1de08-134">Characters</span></span><br/>      | <span data-ttu-id="1de08-135">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="1de08-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1de08-136">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1de08-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1de08-137">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="1de08-137">The name of the option.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="1de08-138">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="1de08-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="1de08-139">строка</span><span class="sxs-lookup"><span data-stu-id="1de08-139">string</span></span><br/>  | <span data-ttu-id="1de08-140">Недоступно</span><span class="sxs-lookup"><span data-stu-id="1de08-140">n/a</span></span><br/>             | <span data-ttu-id="1de08-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="1de08-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1de08-142">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="1de08-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                          |
| <span data-ttu-id="1de08-143">\_англевалуе\_</span><span class="sxs-lookup"><span data-stu-id="1de08-143">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="1de08-144">Целое число</span><span class="sxs-lookup"><span data-stu-id="1de08-144">integer</span></span><br/> | <span data-ttu-id="1de08-145">градусы</span><span class="sxs-lookup"><span data-stu-id="1de08-145">degrees</span></span><br/>         | <span data-ttu-id="1de08-146">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="1de08-146">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="1de08-147">Задает угол сшивания относительно ширины Пажеимажеаблесизе.</span><span class="sxs-lookup"><span data-stu-id="1de08-147">Specifies the staple angle, relative to the width of the PageImageableSize.</span></span> <span data-ttu-id="1de08-148">Угол сшивания измеряется в направлении против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="1de08-148">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="1de08-149">\_шиткапаЦитивалуе\_</span><span class="sxs-lookup"><span data-stu-id="1de08-149">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="1de08-150">Целое число</span><span class="sxs-lookup"><span data-stu-id="1de08-150">integer</span></span><br/> | <span data-ttu-id="1de08-151">листы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1de08-151">sheets of media</span></span><br/> | <span data-ttu-id="1de08-152">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="1de08-152">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="1de08-153">Указывает число листов, поддерживаемое параметром сшивания для выбранного в данный момент носителя.</span><span class="sxs-lookup"><span data-stu-id="1de08-153">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                          |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1de08-154">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="1de08-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1de08-155">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="1de08-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1de08-156">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="1de08-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobStapleAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies saddle stitch stapling -->
  <psf:Option name="psk:SaddleStitch">
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, left corner. -->
  <psf:Option name="psk:StapleBottomLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, right corner. -->
  <psf:Option name="psk:StapleBottomRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the left edge. -->
  <psf:Option name="psk:StapleDualLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the right edge. -->
  <psf:Option name="psk:StapleDualRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the top edge. -->
  <psf:Option name="psk:StapleDualTop">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no stapling. -->
  <psf:Option name="psk:None">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the top, left corner. -->
  <psf:Option name="psk:StapleTopLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the top, right corner. -->
  <psf:Option name="psk:StapleTopRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the bottom edge. -->
  <psf:Option name="psk:StapleDualBottom">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="1de08-157">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1de08-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1de08-158">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="1de08-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




