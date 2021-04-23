---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: пажересолутион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e0fdd16cf3dc0beb6a418b23d8ee6a93e4a6a61
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105703552"
---
# <a name="pageresolution"></a><span data-ttu-id="54158-104">пажересолутион</span><span class="sxs-lookup"><span data-stu-id="54158-104">PageResolution</span></span>

<span data-ttu-id="54158-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="54158-105">This topic is not current.</span></span> <span data-ttu-id="54158-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="54158-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="54158-107">Определяет разрешение печатаемых страниц в виде качественного значения, в виде количественного значения, выраженного в точках на дюйм или оба представления.</span><span class="sxs-lookup"><span data-stu-id="54158-107">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="54158-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="54158-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="54158-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="54158-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="54158-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="54158-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="54158-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="54158-111">Element Information</span></span>



| <span data-ttu-id="54158-112">Имя</span><span class="sxs-lookup"><span data-stu-id="54158-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="54158-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="54158-113">Element Type</span></span> <br/>   | <span data-ttu-id="54158-114">Функция</span><span class="sxs-lookup"><span data-stu-id="54158-114">Feature</span></span><br/> |
| <span data-ttu-id="54158-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="54158-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="54158-116">Страница</span><span class="sxs-lookup"><span data-stu-id="54158-116">Page</span></span><br/>    |
| <span data-ttu-id="54158-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="54158-117">Notes</span></span> <br/>          | <span data-ttu-id="54158-118">Нет</span><span class="sxs-lookup"><span data-stu-id="54158-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="54158-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="54158-119">Structural Content</span></span>

<span data-ttu-id="54158-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="54158-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_ResolutionXValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_ResolutionYValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">_QualitativeResolutionValue_</psf:Value>
    </psf:ScoredProperty> 
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="54158-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="54158-121">Structure Variables</span></span>

<span data-ttu-id="54158-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="54158-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="54158-123">Имя</span><span class="sxs-lookup"><span data-stu-id="54158-123">Name</span></span>                                      | <span data-ttu-id="54158-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="54158-124">Data type</span></span>          | <span data-ttu-id="54158-125">Unit</span><span class="sxs-lookup"><span data-stu-id="54158-125">Unit</span></span>                  | <span data-ttu-id="54158-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="54158-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="54158-127">Сводка</span><span class="sxs-lookup"><span data-stu-id="54158-127">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54158-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="54158-128">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="54158-129">строка</span><span class="sxs-lookup"><span data-stu-id="54158-129">string</span></span><br/>  | <span data-ttu-id="54158-130">characters</span><span class="sxs-lookup"><span data-stu-id="54158-130">characters</span></span><br/> | <span data-ttu-id="54158-131">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="54158-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="54158-132">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="54158-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="54158-133">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="54158-133">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="54158-134">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="54158-134">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="54158-135">строка</span><span class="sxs-lookup"><span data-stu-id="54158-135">string</span></span><br/>  | <span data-ttu-id="54158-136">Недоступно</span><span class="sxs-lookup"><span data-stu-id="54158-136">n/a</span></span><br/>        | <span data-ttu-id="54158-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="54158-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="54158-138">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="54158-138">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="54158-139">\_ресолутионксвалуе\_</span><span class="sxs-lookup"><span data-stu-id="54158-139">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="54158-140">Целое число</span><span class="sxs-lookup"><span data-stu-id="54158-140">integer</span></span><br/> | <span data-ttu-id="54158-141">DPI</span><span class="sxs-lookup"><span data-stu-id="54158-141">DPI</span></span><br/>        | <span data-ttu-id="54158-142">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="54158-142">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="54158-143">Указывает компонент x разрешения относительно Пажеимажеаблесизе в точках на дюйм (относительно Пажемедиасизе и направления носителя).</span><span class="sxs-lookup"><span data-stu-id="54158-143">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="54158-144">\_ресолутионивалуе\_</span><span class="sxs-lookup"><span data-stu-id="54158-144">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="54158-145">Целое число</span><span class="sxs-lookup"><span data-stu-id="54158-145">integer</span></span><br/> | <span data-ttu-id="54158-146">DPI</span><span class="sxs-lookup"><span data-stu-id="54158-146">DPI</span></span><br/>        | <span data-ttu-id="54158-147">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="54158-147">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="54158-148">Задает компонент y разрешения, относительно Пажеимажеаблесизе в точках на дюйм (относительно Пажемедиасизе и направления потока медиа).</span><span class="sxs-lookup"><span data-stu-id="54158-148">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="54158-149">\_куалитативересолутионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="54158-149">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="54158-150">строка</span><span class="sxs-lookup"><span data-stu-id="54158-150">string</span></span><br/>  | <span data-ttu-id="54158-151">Недоступно</span><span class="sxs-lookup"><span data-stu-id="54158-151">n/a</span></span><br/>        | <span data-ttu-id="54158-152">По умолчанию, черновик, высокий, нормальный, другой.</span><span class="sxs-lookup"><span data-stu-id="54158-152">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="54158-153">Задает метку качества для разрешения.</span><span class="sxs-lookup"><span data-stu-id="54158-153">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="54158-154">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="54158-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="54158-155">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="54158-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="54158-156">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="54158-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!-- The horizontal resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- The vertical resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- Value representing the resolution -->
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">Other</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="54158-157">См. также</span><span class="sxs-lookup"><span data-stu-id="54158-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54158-158">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="54158-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




