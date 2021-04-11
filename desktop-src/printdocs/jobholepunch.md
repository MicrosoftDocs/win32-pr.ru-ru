---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 26e9e7d6-7c01-4687-aa64-7aea867b4e58
title: жобхолепунч
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bcd709c6115a9f4af3084c28ca047950d1b81fd
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104273356"
---
# <a name="jobholepunch"></a><span data-ttu-id="fcddf-104">жобхолепунч</span><span class="sxs-lookup"><span data-stu-id="fcddf-104">JobHolePunch</span></span>

<span data-ttu-id="fcddf-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="fcddf-105">This topic is not current.</span></span> <span data-ttu-id="fcddf-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fcddf-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fcddf-107">Описывает характеристики дырокола выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fcddf-107">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="fcddf-108">Все документы удаляются вместе.</span><span class="sxs-lookup"><span data-stu-id="fcddf-108">All documents are punched together.</span></span> <span data-ttu-id="fcddf-109">Ключевые слова Жобхолепунч и Докуменсолепунч являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="fcddf-109">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="fcddf-110">Оба значения не должны одновременно указываться в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="fcddf-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="fcddf-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fcddf-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fcddf-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="fcddf-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="fcddf-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="fcddf-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="fcddf-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fcddf-114">Element Information</span></span>



| <span data-ttu-id="fcddf-115">Имя</span><span class="sxs-lookup"><span data-stu-id="fcddf-115">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcddf-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="fcddf-116">Element Type</span></span> <br/>   | <span data-ttu-id="fcddf-117">Функция</span><span class="sxs-lookup"><span data-stu-id="fcddf-117">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="fcddf-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="fcddf-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fcddf-119">Задание</span><span class="sxs-lookup"><span data-stu-id="fcddf-119">Job</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="fcddf-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="fcddf-120">Notes</span></span> <br/>          | <span data-ttu-id="fcddf-121">Верхние, нижние, левые и правая относятся относительно Пажеимажеаблесизе, где Топлефт обозначается исходными значениями оси x и оси y.</span><span class="sxs-lookup"><span data-stu-id="fcddf-121">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="fcddf-122">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="fcddf-122">Structural Content</span></span>

<span data-ttu-id="fcddf-123">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="fcddf-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="fcddf-124">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="fcddf-124">Structure Variables</span></span>

<span data-ttu-id="fcddf-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="fcddf-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fcddf-126">Имя</span><span class="sxs-lookup"><span data-stu-id="fcddf-126">Name</span></span>                               | <span data-ttu-id="fcddf-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fcddf-127">Data type</span></span>         | <span data-ttu-id="fcddf-128">Unit</span><span class="sxs-lookup"><span data-stu-id="fcddf-128">Unit</span></span>                  | <span data-ttu-id="fcddf-129">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="fcddf-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="fcddf-130">Сводка</span><span class="sxs-lookup"><span data-stu-id="fcddf-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="fcddf-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="fcddf-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="fcddf-132">строка</span><span class="sxs-lookup"><span data-stu-id="fcddf-132">string</span></span><br/> | <span data-ttu-id="fcddf-133">characters</span><span class="sxs-lookup"><span data-stu-id="fcddf-133">characters</span></span><br/> | <span data-ttu-id="fcddf-134">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="fcddf-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="fcddf-135">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fcddf-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="fcddf-136">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="fcddf-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="fcddf-137">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="fcddf-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="fcddf-138">строка</span><span class="sxs-lookup"><span data-stu-id="fcddf-138">string</span></span><br/> | <span data-ttu-id="fcddf-139">Недоступно</span><span class="sxs-lookup"><span data-stu-id="fcddf-139">n/a</span></span><br/>        | <span data-ttu-id="fcddf-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="fcddf-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="fcddf-141">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="fcddf-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="fcddf-142">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="fcddf-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="fcddf-143">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="fcddf-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="fcddf-144">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="fcddf-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="fcddf-145">См. также</span><span class="sxs-lookup"><span data-stu-id="fcddf-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcddf-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="fcddf-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




