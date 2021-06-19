---
description: Ознакомьтесь с элементом Пажересолутион, настраиваемым пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: пажересолутион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760384ff900e7b35e37105fdb19e3635a434aa5a
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394827"
---
# <a name="pageresolution"></a><span data-ttu-id="00eb6-105">пажересолутион</span><span class="sxs-lookup"><span data-stu-id="00eb6-105">PageResolution</span></span>

<span data-ttu-id="00eb6-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="00eb6-106">This topic is not current.</span></span> <span data-ttu-id="00eb6-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="00eb6-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="00eb6-108">Определяет разрешение печатаемых страниц в виде качественного значения, в виде количественного значения, выраженного в точках на дюйм или оба представления.</span><span class="sxs-lookup"><span data-stu-id="00eb6-108">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="00eb6-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="00eb6-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="00eb6-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="00eb6-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="00eb6-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="00eb6-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="00eb6-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="00eb6-112">Element Information</span></span>



| <span data-ttu-id="00eb6-113">Имя</span><span class="sxs-lookup"><span data-stu-id="00eb6-113">Name</span></span> | <span data-ttu-id="00eb6-114">Значение</span><span class="sxs-lookup"><span data-stu-id="00eb6-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="00eb6-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="00eb6-115">Element Type</span></span> <br/>   | <span data-ttu-id="00eb6-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="00eb6-116">Feature</span></span><br/> |
| <span data-ttu-id="00eb6-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="00eb6-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="00eb6-118">Страница</span><span class="sxs-lookup"><span data-stu-id="00eb6-118">Page</span></span><br/>    |
| <span data-ttu-id="00eb6-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="00eb6-119">Notes</span></span> <br/>          | <span data-ttu-id="00eb6-120">Нет</span><span class="sxs-lookup"><span data-stu-id="00eb6-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="00eb6-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="00eb6-121">Structural Content</span></span>

<span data-ttu-id="00eb6-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="00eb6-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="00eb6-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="00eb6-123">Structure Variables</span></span>

<span data-ttu-id="00eb6-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="00eb6-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="00eb6-125">Имя</span><span class="sxs-lookup"><span data-stu-id="00eb6-125">Name</span></span>                                      | <span data-ttu-id="00eb6-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="00eb6-126">Data type</span></span>          | <span data-ttu-id="00eb6-127">Unit</span><span class="sxs-lookup"><span data-stu-id="00eb6-127">Unit</span></span>                  | <span data-ttu-id="00eb6-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="00eb6-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="00eb6-129">Итоги</span><span class="sxs-lookup"><span data-stu-id="00eb6-129">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00eb6-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="00eb6-130">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="00eb6-131">строка</span><span class="sxs-lookup"><span data-stu-id="00eb6-131">string</span></span><br/>  | <span data-ttu-id="00eb6-132">characters</span><span class="sxs-lookup"><span data-stu-id="00eb6-132">characters</span></span><br/> | <span data-ttu-id="00eb6-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="00eb6-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="00eb6-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="00eb6-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="00eb6-135">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="00eb6-135">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="00eb6-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="00eb6-136">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="00eb6-137">строка</span><span class="sxs-lookup"><span data-stu-id="00eb6-137">string</span></span><br/>  | <span data-ttu-id="00eb6-138">Недоступно</span><span class="sxs-lookup"><span data-stu-id="00eb6-138">n/a</span></span><br/>        | <span data-ttu-id="00eb6-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="00eb6-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="00eb6-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="00eb6-140">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="00eb6-141">\_ресолутионксвалуе\_</span><span class="sxs-lookup"><span data-stu-id="00eb6-141">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="00eb6-142">Целое число</span><span class="sxs-lookup"><span data-stu-id="00eb6-142">integer</span></span><br/> | <span data-ttu-id="00eb6-143">DPI</span><span class="sxs-lookup"><span data-stu-id="00eb6-143">DPI</span></span><br/>        | <span data-ttu-id="00eb6-144">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="00eb6-144">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="00eb6-145">Указывает компонент x разрешения относительно Пажеимажеаблесизе в точках на дюйм (относительно Пажемедиасизе и направления носителя).</span><span class="sxs-lookup"><span data-stu-id="00eb6-145">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="00eb6-146">\_ресолутионивалуе\_</span><span class="sxs-lookup"><span data-stu-id="00eb6-146">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="00eb6-147">Целое число</span><span class="sxs-lookup"><span data-stu-id="00eb6-147">integer</span></span><br/> | <span data-ttu-id="00eb6-148">DPI</span><span class="sxs-lookup"><span data-stu-id="00eb6-148">DPI</span></span><br/>        | <span data-ttu-id="00eb6-149">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="00eb6-149">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="00eb6-150">Задает компонент y разрешения, относительно Пажеимажеаблесизе в точках на дюйм (относительно Пажемедиасизе и направления потока медиа).</span><span class="sxs-lookup"><span data-stu-id="00eb6-150">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="00eb6-151">\_куалитативересолутионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="00eb6-151">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="00eb6-152">строка</span><span class="sxs-lookup"><span data-stu-id="00eb6-152">string</span></span><br/>  | <span data-ttu-id="00eb6-153">Недоступно</span><span class="sxs-lookup"><span data-stu-id="00eb6-153">n/a</span></span><br/>        | <span data-ttu-id="00eb6-154">По умолчанию, черновик, высокий, нормальный, другой.</span><span class="sxs-lookup"><span data-stu-id="00eb6-154">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="00eb6-155">Задает метку качества для разрешения.</span><span class="sxs-lookup"><span data-stu-id="00eb6-155">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="00eb6-156">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="00eb6-156">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="00eb6-157">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="00eb6-157">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="00eb6-158">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="00eb6-158">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="00eb6-159">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="00eb6-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00eb6-160">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="00eb6-160">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




