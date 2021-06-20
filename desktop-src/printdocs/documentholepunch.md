---
description: Сведения об элементе Докуменсолепунч, описывающем характеристики дырокола выходного отверстия.
ms.assetid: 46fd5e22-a2f3-424d-8c2f-2d5ac089a230
title: докуменсолепунч
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760559d3bb155030ff72a616096e5a860ba0d6b0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409297"
---
# <a name="documentholepunch"></a><span data-ttu-id="1a0b0-103">докуменсолепунч</span><span class="sxs-lookup"><span data-stu-id="1a0b0-103">DocumentHolePunch</span></span>

<span data-ttu-id="1a0b0-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="1a0b0-104">This topic is not current.</span></span> <span data-ttu-id="1a0b0-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1a0b0-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1a0b0-106">Описывает характеристики дырокола выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1a0b0-106">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="1a0b0-107">Каждый документ помещается отдельно.</span><span class="sxs-lookup"><span data-stu-id="1a0b0-107">Each document is punched separately.</span></span> <span data-ttu-id="1a0b0-108">Ключевые слова Жобхолепунч и Докуменсолепунч являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="1a0b0-108">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="1a0b0-109">Оба значения не должны одновременно указываться в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="1a0b0-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="1a0b0-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1a0b0-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a0b0-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="1a0b0-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1a0b0-112">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="1a0b0-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1a0b0-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1a0b0-113">Element Information</span></span>



| <span data-ttu-id="1a0b0-114">Имя</span><span class="sxs-lookup"><span data-stu-id="1a0b0-114">Name</span></span> | <span data-ttu-id="1a0b0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1a0b0-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1a0b0-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="1a0b0-116">Element Type</span></span> <br/>   | <span data-ttu-id="1a0b0-117">Компонент</span><span class="sxs-lookup"><span data-stu-id="1a0b0-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="1a0b0-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="1a0b0-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1a0b0-119">Документ</span><span class="sxs-lookup"><span data-stu-id="1a0b0-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="1a0b0-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="1a0b0-120">Notes</span></span> <br/>          | <span data-ttu-id="1a0b0-121">Верхняя, Нижняя, левая и правая относительные относятся к Пажеимажеаблесизе.</span><span class="sxs-lookup"><span data-stu-id="1a0b0-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="1a0b0-122">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="1a0b0-122">Structural Content</span></span>

<span data-ttu-id="1a0b0-123">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="1a0b0-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="1a0b0-124">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="1a0b0-124">Structure Variables</span></span>

<span data-ttu-id="1a0b0-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="1a0b0-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1a0b0-126">Имя</span><span class="sxs-lookup"><span data-stu-id="1a0b0-126">Name</span></span>                               | <span data-ttu-id="1a0b0-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1a0b0-127">Data type</span></span>         | <span data-ttu-id="1a0b0-128">Unit</span><span class="sxs-lookup"><span data-stu-id="1a0b0-128">Unit</span></span>                  | <span data-ttu-id="1a0b0-129">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="1a0b0-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1a0b0-130">Итоги</span><span class="sxs-lookup"><span data-stu-id="1a0b0-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1a0b0-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1a0b0-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="1a0b0-132">строка</span><span class="sxs-lookup"><span data-stu-id="1a0b0-132">string</span></span><br/> | <span data-ttu-id="1a0b0-133">characters</span><span class="sxs-lookup"><span data-stu-id="1a0b0-133">characters</span></span><br/> | <span data-ttu-id="1a0b0-134">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="1a0b0-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1a0b0-135">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1a0b0-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1a0b0-136">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="1a0b0-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="1a0b0-137">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="1a0b0-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="1a0b0-138">строка</span><span class="sxs-lookup"><span data-stu-id="1a0b0-138">string</span></span><br/> | <span data-ttu-id="1a0b0-139">Недоступно</span><span class="sxs-lookup"><span data-stu-id="1a0b0-139">n/a</span></span><br/>        | <span data-ttu-id="1a0b0-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="1a0b0-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1a0b0-141">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="1a0b0-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1a0b0-142">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="1a0b0-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1a0b0-143">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="1a0b0-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1a0b0-144">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="1a0b0-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1a0b0-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1a0b0-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a0b0-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="1a0b0-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




