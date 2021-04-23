---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 66a3ac9a-674e-4f16-a2d8-8f5b753f876c
title: пажепостер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281da67f3f6b90e4e49d0cdc57ba3065d719397b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105703553"
---
# <a name="pageposter"></a><span data-ttu-id="d9d89-104">пажепостер</span><span class="sxs-lookup"><span data-stu-id="d9d89-104">PagePoster</span></span>

<span data-ttu-id="d9d89-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="d9d89-105">This topic is not current.</span></span> <span data-ttu-id="d9d89-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d9d89-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d9d89-107">Описывает вывод одной страницы на несколько страниц физических носителей.</span><span class="sxs-lookup"><span data-stu-id="d9d89-107">Describes the output of a single page to multiple physical media sheets.</span></span>

-   [<span data-ttu-id="d9d89-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d9d89-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d9d89-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="d9d89-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d9d89-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="d9d89-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d9d89-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d9d89-111">Element Information</span></span>



| <span data-ttu-id="d9d89-112">Имя</span><span class="sxs-lookup"><span data-stu-id="d9d89-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="d9d89-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="d9d89-113">Element Type</span></span> <br/>   | <span data-ttu-id="d9d89-114">Функция</span><span class="sxs-lookup"><span data-stu-id="d9d89-114">Feature</span></span><br/> |
| <span data-ttu-id="d9d89-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="d9d89-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d9d89-116">Страница</span><span class="sxs-lookup"><span data-stu-id="d9d89-116">Page</span></span><br/>    |
| <span data-ttu-id="d9d89-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="d9d89-117">Notes</span></span> <br/>          | <span data-ttu-id="d9d89-118">Нет</span><span class="sxs-lookup"><span data-stu-id="d9d89-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="d9d89-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="d9d89-119">Structural Content</span></span>

<span data-ttu-id="d9d89-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="d9d89-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PagePoster">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:SheetsPerPage">
      <psf:Value xsi:type="xs:integer">_SheetsPerPageValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="d9d89-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="d9d89-121">Structure Variables</span></span>

<span data-ttu-id="d9d89-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="d9d89-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d9d89-123">Имя</span><span class="sxs-lookup"><span data-stu-id="d9d89-123">Name</span></span>                               | <span data-ttu-id="d9d89-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d9d89-124">Data type</span></span>          | <span data-ttu-id="d9d89-125">Unit</span><span class="sxs-lookup"><span data-stu-id="d9d89-125">Unit</span></span>                  | <span data-ttu-id="d9d89-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="d9d89-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="d9d89-127">Сводка</span><span class="sxs-lookup"><span data-stu-id="d9d89-127">Summary</span></span>                                                                      |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d9d89-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="d9d89-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="d9d89-129">строка</span><span class="sxs-lookup"><span data-stu-id="d9d89-129">string</span></span><br/>  | <span data-ttu-id="d9d89-130">characters</span><span class="sxs-lookup"><span data-stu-id="d9d89-130">characters</span></span><br/> | <span data-ttu-id="d9d89-131">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="d9d89-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="d9d89-132">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d9d89-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="d9d89-133">Имя параметра</span><span class="sxs-lookup"><span data-stu-id="d9d89-133">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="d9d89-134">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="d9d89-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="d9d89-135">строка</span><span class="sxs-lookup"><span data-stu-id="d9d89-135">string</span></span><br/>  | <span data-ttu-id="d9d89-136">Недоступно</span><span class="sxs-lookup"><span data-stu-id="d9d89-136">n/a</span></span><br/>        | <span data-ttu-id="d9d89-137">True, False</span><span class="sxs-lookup"><span data-stu-id="d9d89-137">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="d9d89-138">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="d9d89-138">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="d9d89-139">\_шитсперпажевалуе\_</span><span class="sxs-lookup"><span data-stu-id="d9d89-139">\_SheetsPerPageValue\_</span></span><br/>  | <span data-ttu-id="d9d89-140">Целое число</span><span class="sxs-lookup"><span data-stu-id="d9d89-140">integer</span></span><br/> | <span data-ttu-id="d9d89-141">страницы</span><span class="sxs-lookup"><span data-stu-id="d9d89-141">pages</span></span><br/>      | <span data-ttu-id="d9d89-142">Больше или равно 0.</span><span class="sxs-lookup"><span data-stu-id="d9d89-142">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="d9d89-143">Указывает число физических страниц на логическую страницу.</span><span class="sxs-lookup"><span data-stu-id="d9d89-143">Specifies the number of physical sheets per logical page.</span></span><br/>         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d9d89-144">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="d9d89-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d9d89-145">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="d9d89-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d9d89-146">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="d9d89-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PagePoster">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies media sheets per page. -->
  <psf:Option>
    <psf:ScoredProperty name="psk:SheetsPerPage">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="d9d89-147">См. также</span><span class="sxs-lookup"><span data-stu-id="d9d89-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9d89-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="d9d89-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




