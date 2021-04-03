---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 46fd5e22-a2f3-424d-8c2f-2d5ac089a230
title: докуменсолепунч
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42783248213f1ccffd0c0fb7f3a416ee6ae801d
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104000029"
---
# <a name="documentholepunch"></a><span data-ttu-id="bca80-104">докуменсолепунч</span><span class="sxs-lookup"><span data-stu-id="bca80-104">DocumentHolePunch</span></span>

<span data-ttu-id="bca80-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="bca80-105">This topic is not current.</span></span> <span data-ttu-id="bca80-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bca80-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bca80-107">Описывает характеристики дырокола выходных данных.</span><span class="sxs-lookup"><span data-stu-id="bca80-107">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="bca80-108">Каждый документ помещается отдельно.</span><span class="sxs-lookup"><span data-stu-id="bca80-108">Each document is punched separately.</span></span> <span data-ttu-id="bca80-109">Ключевые слова Жобхолепунч и Докуменсолепунч являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="bca80-109">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="bca80-110">Оба значения не должны одновременно указываться в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="bca80-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="bca80-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="bca80-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bca80-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="bca80-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="bca80-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="bca80-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="bca80-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="bca80-114">Element Information</span></span>



| <span data-ttu-id="bca80-115">Имя</span><span class="sxs-lookup"><span data-stu-id="bca80-115">Name</span></span>                       |                                                                                |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="bca80-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="bca80-116">Element Type</span></span> <br/>   | <span data-ttu-id="bca80-117">Функция</span><span class="sxs-lookup"><span data-stu-id="bca80-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="bca80-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="bca80-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bca80-119">Документ</span><span class="sxs-lookup"><span data-stu-id="bca80-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="bca80-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="bca80-120">Notes</span></span> <br/>          | <span data-ttu-id="bca80-121">Верхняя, Нижняя, левая и правая относительные относятся к Пажеимажеаблесизе.</span><span class="sxs-lookup"><span data-stu-id="bca80-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="bca80-122">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="bca80-122">Structural Content</span></span>

<span data-ttu-id="bca80-123">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="bca80-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="bca80-124">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="bca80-124">Structure Variables</span></span>

<span data-ttu-id="bca80-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="bca80-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bca80-126">Имя</span><span class="sxs-lookup"><span data-stu-id="bca80-126">Name</span></span>                               | <span data-ttu-id="bca80-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="bca80-127">Data type</span></span>         | <span data-ttu-id="bca80-128">Unit</span><span class="sxs-lookup"><span data-stu-id="bca80-128">Unit</span></span>                  | <span data-ttu-id="bca80-129">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="bca80-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="bca80-130">Сводка</span><span class="sxs-lookup"><span data-stu-id="bca80-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="bca80-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="bca80-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="bca80-132">строка</span><span class="sxs-lookup"><span data-stu-id="bca80-132">string</span></span><br/> | <span data-ttu-id="bca80-133">characters</span><span class="sxs-lookup"><span data-stu-id="bca80-133">characters</span></span><br/> | <span data-ttu-id="bca80-134">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="bca80-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="bca80-135">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bca80-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="bca80-136">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="bca80-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="bca80-137">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="bca80-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="bca80-138">строка</span><span class="sxs-lookup"><span data-stu-id="bca80-138">string</span></span><br/> | <span data-ttu-id="bca80-139">Недоступно</span><span class="sxs-lookup"><span data-stu-id="bca80-139">n/a</span></span><br/>        | <span data-ttu-id="bca80-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="bca80-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="bca80-141">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="bca80-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="bca80-142">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="bca80-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="bca80-143">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="bca80-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="bca80-144">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="bca80-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="bca80-145">См. также</span><span class="sxs-lookup"><span data-stu-id="bca80-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bca80-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="bca80-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




