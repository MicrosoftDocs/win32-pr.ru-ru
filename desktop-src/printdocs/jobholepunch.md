---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 26e9e7d6-7c01-4687-aa64-7aea867b4e58
title: жобхолепунч
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56316c94dc56a2646446a8cd63885cceaa1407fa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999301"
---
# <a name="jobholepunch"></a><span data-ttu-id="e27f1-104">жобхолепунч</span><span class="sxs-lookup"><span data-stu-id="e27f1-104">JobHolePunch</span></span>

<span data-ttu-id="e27f1-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="e27f1-105">This topic is not current.</span></span> <span data-ttu-id="e27f1-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e27f1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e27f1-107">Описывает характеристики дырокола выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e27f1-107">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="e27f1-108">Все документы удаляются вместе.</span><span class="sxs-lookup"><span data-stu-id="e27f1-108">All documents are punched together.</span></span> <span data-ttu-id="e27f1-109">Ключевые слова Жобхолепунч и Докуменсолепунч являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="e27f1-109">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="e27f1-110">Оба значения не должны одновременно указываться в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="e27f1-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="e27f1-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e27f1-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e27f1-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="e27f1-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e27f1-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="e27f1-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e27f1-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e27f1-114">Element Information</span></span>



| <span data-ttu-id="e27f1-115">Имя</span><span class="sxs-lookup"><span data-stu-id="e27f1-115">Name</span></span> | <span data-ttu-id="e27f1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e27f1-116">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e27f1-117">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="e27f1-117">Element Type</span></span> <br/>   | <span data-ttu-id="e27f1-118">Компонент</span><span class="sxs-lookup"><span data-stu-id="e27f1-118">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="e27f1-119">Префикс области</span><span class="sxs-lookup"><span data-stu-id="e27f1-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e27f1-120">Задание</span><span class="sxs-lookup"><span data-stu-id="e27f1-120">Job</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="e27f1-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="e27f1-121">Notes</span></span> <br/>          | <span data-ttu-id="e27f1-122">Верхние, нижние, левые и правая относятся относительно Пажеимажеаблесизе, где Топлефт обозначается исходными значениями оси x и оси y.</span><span class="sxs-lookup"><span data-stu-id="e27f1-122">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="e27f1-123">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="e27f1-123">Structural Content</span></span>

<span data-ttu-id="e27f1-124">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="e27f1-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
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

## <a name="structure-variables"></a><span data-ttu-id="e27f1-125">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="e27f1-125">Structure Variables</span></span>

<span data-ttu-id="e27f1-126">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="e27f1-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e27f1-127">Имя</span><span class="sxs-lookup"><span data-stu-id="e27f1-127">Name</span></span>                               | <span data-ttu-id="e27f1-128">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e27f1-128">Data type</span></span>         | <span data-ttu-id="e27f1-129">Unit</span><span class="sxs-lookup"><span data-stu-id="e27f1-129">Unit</span></span>                  | <span data-ttu-id="e27f1-130">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="e27f1-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e27f1-131">Сводка</span><span class="sxs-lookup"><span data-stu-id="e27f1-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e27f1-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e27f1-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e27f1-133">строка</span><span class="sxs-lookup"><span data-stu-id="e27f1-133">string</span></span><br/> | <span data-ttu-id="e27f1-134">characters</span><span class="sxs-lookup"><span data-stu-id="e27f1-134">characters</span></span><br/> | <span data-ttu-id="e27f1-135">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="e27f1-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e27f1-136">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e27f1-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e27f1-137">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="e27f1-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="e27f1-138">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="e27f1-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e27f1-139">строка</span><span class="sxs-lookup"><span data-stu-id="e27f1-139">string</span></span><br/> | <span data-ttu-id="e27f1-140">Недоступно</span><span class="sxs-lookup"><span data-stu-id="e27f1-140">n/a</span></span><br/>        | <span data-ttu-id="e27f1-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="e27f1-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e27f1-142">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="e27f1-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e27f1-143">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="e27f1-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e27f1-144">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="e27f1-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e27f1-145">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="e27f1-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
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

## <a name="related-topics"></a><span data-ttu-id="e27f1-146">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e27f1-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e27f1-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="e27f1-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




