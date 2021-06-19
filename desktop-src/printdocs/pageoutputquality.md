---
description: Сведения об элементе Пажеаутпуткуалити, настраиваемом пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 4720f812-a71a-458f-85fa-7885cca0dbbb
title: пажеаутпуткуалити
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8001d8ffd6bb3ead50a27b9ea36c9849c475576f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395596"
---
# <a name="pageoutputquality"></a><span data-ttu-id="eefb1-105">пажеаутпуткуалити</span><span class="sxs-lookup"><span data-stu-id="eefb1-105">PageOutputQuality</span></span>

<span data-ttu-id="eefb1-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="eefb1-106">This topic is not current.</span></span> <span data-ttu-id="eefb1-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="eefb1-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="eefb1-108">Описывает уровень качества выходных данных.</span><span class="sxs-lookup"><span data-stu-id="eefb1-108">Describes the quality level of the output.</span></span>

-   [<span data-ttu-id="eefb1-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="eefb1-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="eefb1-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="eefb1-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="eefb1-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="eefb1-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="eefb1-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="eefb1-112">Element Information</span></span>



| <span data-ttu-id="eefb1-113">Имя</span><span class="sxs-lookup"><span data-stu-id="eefb1-113">Name</span></span> | <span data-ttu-id="eefb1-114">Значение</span><span class="sxs-lookup"><span data-stu-id="eefb1-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="eefb1-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="eefb1-115">Element Type</span></span> <br/>   | <span data-ttu-id="eefb1-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="eefb1-116">Feature</span></span><br/> |
| <span data-ttu-id="eefb1-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="eefb1-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="eefb1-118">Страница</span><span class="sxs-lookup"><span data-stu-id="eefb1-118">Page</span></span><br/>    |
| <span data-ttu-id="eefb1-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="eefb1-119">Notes</span></span> <br/>          | <span data-ttu-id="eefb1-120">Нет</span><span class="sxs-lookup"><span data-stu-id="eefb1-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="eefb1-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="eefb1-121">Structural Content</span></span>

<span data-ttu-id="eefb1-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="eefb1-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
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

## <a name="structure-variables"></a><span data-ttu-id="eefb1-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="eefb1-123">Structure Variables</span></span>

<span data-ttu-id="eefb1-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="eefb1-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="eefb1-125">Имя</span><span class="sxs-lookup"><span data-stu-id="eefb1-125">Name</span></span>                               | <span data-ttu-id="eefb1-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="eefb1-126">Data type</span></span>         | <span data-ttu-id="eefb1-127">Unit</span><span class="sxs-lookup"><span data-stu-id="eefb1-127">Unit</span></span>                  | <span data-ttu-id="eefb1-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="eefb1-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="eefb1-129">Итоги</span><span class="sxs-lookup"><span data-stu-id="eefb1-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="eefb1-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="eefb1-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="eefb1-131">строка</span><span class="sxs-lookup"><span data-stu-id="eefb1-131">string</span></span><br/> | <span data-ttu-id="eefb1-132">characters</span><span class="sxs-lookup"><span data-stu-id="eefb1-132">characters</span></span><br/> | <span data-ttu-id="eefb1-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="eefb1-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="eefb1-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eefb1-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="eefb1-135">Имя параметра</span><span class="sxs-lookup"><span data-stu-id="eefb1-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="eefb1-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="eefb1-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="eefb1-137">строка</span><span class="sxs-lookup"><span data-stu-id="eefb1-137">string</span></span><br/> | <span data-ttu-id="eefb1-138">Недоступно</span><span class="sxs-lookup"><span data-stu-id="eefb1-138">n/a</span></span><br/>        | <span data-ttu-id="eefb1-139">True, False</span><span class="sxs-lookup"><span data-stu-id="eefb1-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="eefb1-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="eefb1-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="eefb1-141">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="eefb1-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="eefb1-142">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="eefb1-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="eefb1-143">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="eefb1-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the intent for automatic output (allow the client to automatically choose the best settings). -->
  <psf:Option name="psk:Automatic" />
  <!-- Specifies the intent for draft output (balanced for draft quality text and graphics). -->
  <psf:Option name="psk:Draft" />
  <!-- Specifies the intent for fax output (balanced for standard fax quality). -->
  <psf:Option name="psk:Fax" />
  <!-- Specifies the intent for high quality output (balanced for high quality text and graphics). -->
  <psf:Option name="psk:High" />
  <!-- Specifies the intent for normal output (balanced for good quality text and graphics). -->
  <psf:Option name="psk:Normal" />
  <!-- Specifies the intent for photographic output (images should have the highest quality). -->
  <psf:Option name="psk:Photographic" />
  <!-- Specifies the intent for text only output (graphics may output poorly or not at all). -->
  <psf:Option name="psk:Text" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="eefb1-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="eefb1-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eefb1-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="eefb1-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




