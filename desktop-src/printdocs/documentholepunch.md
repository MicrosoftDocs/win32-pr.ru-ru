---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 46fd5e22-a2f3-424d-8c2f-2d5ac089a230
title: докуменсолепунч
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 825120996d0d488af347ed871386a12d7f8014a7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997891"
---
# <a name="documentholepunch"></a><span data-ttu-id="c3568-104">докуменсолепунч</span><span class="sxs-lookup"><span data-stu-id="c3568-104">DocumentHolePunch</span></span>

<span data-ttu-id="c3568-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="c3568-105">This topic is not current.</span></span> <span data-ttu-id="c3568-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c3568-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c3568-107">Описывает характеристики дырокола выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c3568-107">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="c3568-108">Каждый документ помещается отдельно.</span><span class="sxs-lookup"><span data-stu-id="c3568-108">Each document is punched separately.</span></span> <span data-ttu-id="c3568-109">Ключевые слова Жобхолепунч и Докуменсолепунч являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="c3568-109">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="c3568-110">Оба значения не должны одновременно указываться в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="c3568-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="c3568-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c3568-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c3568-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="c3568-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c3568-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c3568-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c3568-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c3568-114">Element Information</span></span>



| <span data-ttu-id="c3568-115">Имя</span><span class="sxs-lookup"><span data-stu-id="c3568-115">Name</span></span> | <span data-ttu-id="c3568-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c3568-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="c3568-117">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="c3568-117">Element Type</span></span> <br/>   | <span data-ttu-id="c3568-118">Компонент</span><span class="sxs-lookup"><span data-stu-id="c3568-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="c3568-119">Префикс области</span><span class="sxs-lookup"><span data-stu-id="c3568-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c3568-120">Документ</span><span class="sxs-lookup"><span data-stu-id="c3568-120">Document</span></span><br/>                                                            |
| <span data-ttu-id="c3568-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="c3568-121">Notes</span></span> <br/>          | <span data-ttu-id="c3568-122">Верхняя, Нижняя, левая и правая относительные относятся к Пажеимажеаблесизе.</span><span class="sxs-lookup"><span data-stu-id="c3568-122">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="c3568-123">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="c3568-123">Structural Content</span></span>

<span data-ttu-id="c3568-124">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="c3568-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentHolePunch">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="c3568-125">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="c3568-125">Structure Variables</span></span>

<span data-ttu-id="c3568-126">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="c3568-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c3568-127">Имя</span><span class="sxs-lookup"><span data-stu-id="c3568-127">Name</span></span>                               | <span data-ttu-id="c3568-128">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c3568-128">Data type</span></span>         | <span data-ttu-id="c3568-129">Unit</span><span class="sxs-lookup"><span data-stu-id="c3568-129">Unit</span></span>                  | <span data-ttu-id="c3568-130">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="c3568-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c3568-131">Сводка</span><span class="sxs-lookup"><span data-stu-id="c3568-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c3568-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="c3568-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c3568-133">строка</span><span class="sxs-lookup"><span data-stu-id="c3568-133">string</span></span><br/> | <span data-ttu-id="c3568-134">characters</span><span class="sxs-lookup"><span data-stu-id="c3568-134">characters</span></span><br/> | <span data-ttu-id="c3568-135">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="c3568-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c3568-136">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c3568-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c3568-137">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="c3568-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="c3568-138">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="c3568-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c3568-139">строка</span><span class="sxs-lookup"><span data-stu-id="c3568-139">string</span></span><br/> | <span data-ttu-id="c3568-140">Недоступно</span><span class="sxs-lookup"><span data-stu-id="c3568-140">n/a</span></span><br/>        | <span data-ttu-id="c3568-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="c3568-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c3568-142">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="c3568-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c3568-143">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c3568-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c3568-144">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="c3568-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c3568-145">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="c3568-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentHolePunch">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies hole(s) along the bottom edge. -->
  <psf:Option name="psk:BottomEdge" />
  <!-- Specifies hole(s) along the left edge. -->
  <psf:Option name="psk:LeftEdge" />
  <!-- Specifies no hole punching. -->
  <psf:Option name="psk:None" />
  <!-- Specifies hole(s) along the right edge. -->
  <psf:Option name="psk:RightEdge" />
  <!-- Specifies hole(s) along the top edge. -->
  <psf:Option name="psk:TopEdge" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="c3568-146">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c3568-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3568-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="c3568-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




