---
description: Сведения об элементе Жобстаплеаллдокументс, описывающем характеристики сшивания выходных данных задания.
ms.assetid: a6721c13-a3dc-4273-b40f-2a28184b04a9
title: жобстаплеаллдокументс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9598f09181a225bf10d097b8c2aedaf19373a1
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408647"
---
# <a name="jobstaplealldocuments"></a><span data-ttu-id="53ebd-103">жобстаплеаллдокументс</span><span class="sxs-lookup"><span data-stu-id="53ebd-103">JobStapleAllDocuments</span></span>

<span data-ttu-id="53ebd-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="53ebd-104">This topic is not current.</span></span> <span data-ttu-id="53ebd-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="53ebd-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="53ebd-106">Описывает характеристики сшивания выходных данных.</span><span class="sxs-lookup"><span data-stu-id="53ebd-106">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="53ebd-107">Все документы в задании будут сшиты вместе.</span><span class="sxs-lookup"><span data-stu-id="53ebd-107">All documents in the job are stapled together.</span></span> <span data-ttu-id="53ebd-108">Ключевые слова Жобстаплеаллдокументс и Документстапле являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="53ebd-108">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="53ebd-109">Драйвер определяет обработку ограничений между этими ключевыми словами.</span><span class="sxs-lookup"><span data-stu-id="53ebd-109">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="53ebd-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="53ebd-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="53ebd-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="53ebd-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="53ebd-112">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="53ebd-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="53ebd-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="53ebd-113">Element Information</span></span>



| <span data-ttu-id="53ebd-114">Имя</span><span class="sxs-lookup"><span data-stu-id="53ebd-114">Name</span></span> | <span data-ttu-id="53ebd-115">Значение</span><span class="sxs-lookup"><span data-stu-id="53ebd-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="53ebd-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="53ebd-116">Element Type</span></span> <br/>   | <span data-ttu-id="53ebd-117">Компонент</span><span class="sxs-lookup"><span data-stu-id="53ebd-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="53ebd-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="53ebd-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="53ebd-119">Задание</span><span class="sxs-lookup"><span data-stu-id="53ebd-119">Job</span></span><br/>                                                                 |
| <span data-ttu-id="53ebd-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="53ebd-120">Notes</span></span> <br/>          | <span data-ttu-id="53ebd-121">Верхняя, Нижняя, левая и правая относительные относятся к Пажеимажеаблесизе</span><span class="sxs-lookup"><span data-stu-id="53ebd-121">Top, Bottom, Left, and Right are relative to the PageImageableSize</span></span> <br/> |



 

## <a name="structural-content"></a><span data-ttu-id="53ebd-122">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="53ebd-122">Structural Content</span></span>

<span data-ttu-id="53ebd-123">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="53ebd-123">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="53ebd-124">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="53ebd-124">Structure Variables</span></span>

<span data-ttu-id="53ebd-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="53ebd-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="53ebd-126">Имя</span><span class="sxs-lookup"><span data-stu-id="53ebd-126">Name</span></span>                               | <span data-ttu-id="53ebd-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="53ebd-127">Data type</span></span>          | <span data-ttu-id="53ebd-128">Unit</span><span class="sxs-lookup"><span data-stu-id="53ebd-128">Unit</span></span>                       | <span data-ttu-id="53ebd-129">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="53ebd-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="53ebd-130">Итоги</span><span class="sxs-lookup"><span data-stu-id="53ebd-130">Summary</span></span>                                                                                                                                               |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53ebd-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="53ebd-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="53ebd-132">строка</span><span class="sxs-lookup"><span data-stu-id="53ebd-132">string</span></span><br/>  | <span data-ttu-id="53ebd-133">Characters</span><span class="sxs-lookup"><span data-stu-id="53ebd-133">Characters</span></span><br/>      | <span data-ttu-id="53ebd-134">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="53ebd-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="53ebd-135">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="53ebd-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="53ebd-136">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="53ebd-136">The name of the option.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="53ebd-137">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="53ebd-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="53ebd-138">строка</span><span class="sxs-lookup"><span data-stu-id="53ebd-138">string</span></span><br/>  | <span data-ttu-id="53ebd-139">Недоступно</span><span class="sxs-lookup"><span data-stu-id="53ebd-139">n/a</span></span><br/>             | <span data-ttu-id="53ebd-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="53ebd-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="53ebd-141">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="53ebd-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                          |
| <span data-ttu-id="53ebd-142">\_англевалуе\_</span><span class="sxs-lookup"><span data-stu-id="53ebd-142">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="53ebd-143">Целое число</span><span class="sxs-lookup"><span data-stu-id="53ebd-143">integer</span></span><br/> | <span data-ttu-id="53ebd-144">градусы</span><span class="sxs-lookup"><span data-stu-id="53ebd-144">degrees</span></span><br/>         | <span data-ttu-id="53ebd-145">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="53ebd-145">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="53ebd-146">Задает угол сшивания относительно ширины Пажеимажеаблесизе.</span><span class="sxs-lookup"><span data-stu-id="53ebd-146">Specifies the staple angle, relative to the width of the PageImageableSize.</span></span> <span data-ttu-id="53ebd-147">Угол сшивания измеряется в направлении против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="53ebd-147">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="53ebd-148">\_шиткапаЦитивалуе\_</span><span class="sxs-lookup"><span data-stu-id="53ebd-148">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="53ebd-149">Целое число</span><span class="sxs-lookup"><span data-stu-id="53ebd-149">integer</span></span><br/> | <span data-ttu-id="53ebd-150">листы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="53ebd-150">sheets of media</span></span><br/> | <span data-ttu-id="53ebd-151">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="53ebd-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="53ebd-152">Указывает число листов, поддерживаемое параметром сшивания для выбранного в данный момент носителя.</span><span class="sxs-lookup"><span data-stu-id="53ebd-152">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                          |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="53ebd-153">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="53ebd-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="53ebd-154">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="53ebd-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="53ebd-155">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="53ebd-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="53ebd-156">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="53ebd-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53ebd-157">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="53ebd-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




