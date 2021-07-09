---
description: Получение сведений о настраиваемом пользователем элементе Жобхолепунч. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 26e9e7d6-7c01-4687-aa64-7aea867b4e58
title: жобхолепунч
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c82a36784ab6a1fb5eb0c8d682c45cce574ee9e
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549362"
---
# <a name="jobholepunch"></a><span data-ttu-id="effa7-105">жобхолепунч</span><span class="sxs-lookup"><span data-stu-id="effa7-105">JobHolePunch</span></span>

<span data-ttu-id="effa7-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="effa7-106">This topic is not current.</span></span> <span data-ttu-id="effa7-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="effa7-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="effa7-108">Описывает характеристики дырокола выходных данных.</span><span class="sxs-lookup"><span data-stu-id="effa7-108">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="effa7-109">Все документы удаляются вместе.</span><span class="sxs-lookup"><span data-stu-id="effa7-109">All documents are punched together.</span></span> <span data-ttu-id="effa7-110">Ключевые слова Жобхолепунч и Докуменсолепунч являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="effa7-110">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="effa7-111">Оба значения не должны одновременно указываться в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="effa7-111">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="effa7-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="effa7-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="effa7-113">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="effa7-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="effa7-114">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="effa7-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="effa7-115">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="effa7-115">Element Information</span></span>



| <span data-ttu-id="effa7-116">Имя</span><span class="sxs-lookup"><span data-stu-id="effa7-116">Name</span></span> | <span data-ttu-id="effa7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="effa7-117">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="effa7-118">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="effa7-118">Element Type</span></span> <br/>   | <span data-ttu-id="effa7-119">Компонент</span><span class="sxs-lookup"><span data-stu-id="effa7-119">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="effa7-120">Префикс области</span><span class="sxs-lookup"><span data-stu-id="effa7-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="effa7-121">Задание</span><span class="sxs-lookup"><span data-stu-id="effa7-121">Job</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="effa7-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="effa7-122">Notes</span></span> <br/>          | <span data-ttu-id="effa7-123">Верхние, нижние, левые и правая относятся относительно Пажеимажеаблесизе, где Топлефт обозначается исходными значениями оси x и оси y.</span><span class="sxs-lookup"><span data-stu-id="effa7-123">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="effa7-124">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="effa7-124">Structural Content</span></span>

<span data-ttu-id="effa7-125">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="effa7-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="effa7-126">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="effa7-126">Structure Variables</span></span>

<span data-ttu-id="effa7-127">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="effa7-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="effa7-128">Имя</span><span class="sxs-lookup"><span data-stu-id="effa7-128">Name</span></span>                               | <span data-ttu-id="effa7-129">Тип данных</span><span class="sxs-lookup"><span data-stu-id="effa7-129">Data type</span></span>         | <span data-ttu-id="effa7-130">Unit</span><span class="sxs-lookup"><span data-stu-id="effa7-130">Unit</span></span>                  | <span data-ttu-id="effa7-131">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="effa7-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="effa7-132">Итоги</span><span class="sxs-lookup"><span data-stu-id="effa7-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="effa7-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="effa7-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="effa7-134">строка</span><span class="sxs-lookup"><span data-stu-id="effa7-134">string</span></span><br/> | <span data-ttu-id="effa7-135">characters</span><span class="sxs-lookup"><span data-stu-id="effa7-135">characters</span></span><br/> | <span data-ttu-id="effa7-136">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="effa7-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="effa7-137">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="effa7-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="effa7-138">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="effa7-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="effa7-139">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="effa7-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="effa7-140">строка</span><span class="sxs-lookup"><span data-stu-id="effa7-140">string</span></span><br/> | <span data-ttu-id="effa7-141">Н/Д</span><span class="sxs-lookup"><span data-stu-id="effa7-141">n/a</span></span><br/>        | <span data-ttu-id="effa7-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="effa7-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="effa7-143">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="effa7-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="effa7-144">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="effa7-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="effa7-145">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="effa7-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="effa7-146">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="effa7-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="effa7-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="effa7-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="effa7-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="effa7-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




