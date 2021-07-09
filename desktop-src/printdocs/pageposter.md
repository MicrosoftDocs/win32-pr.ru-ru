---
description: Получение сведений о настраиваемом пользователем элементе Пажепостер. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 66a3ac9a-674e-4f16-a2d8-8f5b753f876c
title: пажепостер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b8bb7b57074fe058c7cc5be8dd609577ceb6c1
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548972"
---
# <a name="pageposter"></a><span data-ttu-id="1c472-105">пажепостер</span><span class="sxs-lookup"><span data-stu-id="1c472-105">PagePoster</span></span>

<span data-ttu-id="1c472-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="1c472-106">This topic is not current.</span></span> <span data-ttu-id="1c472-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1c472-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1c472-108">Описывает вывод одной страницы на несколько страниц физических носителей.</span><span class="sxs-lookup"><span data-stu-id="1c472-108">Describes the output of a single page to multiple physical media sheets.</span></span>

-   [<span data-ttu-id="1c472-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1c472-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1c472-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="1c472-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1c472-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="1c472-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1c472-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1c472-112">Element Information</span></span>



| <span data-ttu-id="1c472-113">Имя</span><span class="sxs-lookup"><span data-stu-id="1c472-113">Name</span></span> | <span data-ttu-id="1c472-114">Значение</span><span class="sxs-lookup"><span data-stu-id="1c472-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="1c472-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="1c472-115">Element Type</span></span> <br/>   | <span data-ttu-id="1c472-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="1c472-116">Feature</span></span><br/> |
| <span data-ttu-id="1c472-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="1c472-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1c472-118">Страница</span><span class="sxs-lookup"><span data-stu-id="1c472-118">Page</span></span><br/>    |
| <span data-ttu-id="1c472-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="1c472-119">Notes</span></span> <br/>          | <span data-ttu-id="1c472-120">Нет</span><span class="sxs-lookup"><span data-stu-id="1c472-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="1c472-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="1c472-121">Structural Content</span></span>

<span data-ttu-id="1c472-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="1c472-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="1c472-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="1c472-123">Structure Variables</span></span>

<span data-ttu-id="1c472-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="1c472-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1c472-125">Имя</span><span class="sxs-lookup"><span data-stu-id="1c472-125">Name</span></span>                               | <span data-ttu-id="1c472-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1c472-126">Data type</span></span>          | <span data-ttu-id="1c472-127">Unit</span><span class="sxs-lookup"><span data-stu-id="1c472-127">Unit</span></span>                  | <span data-ttu-id="1c472-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="1c472-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1c472-129">Итоги</span><span class="sxs-lookup"><span data-stu-id="1c472-129">Summary</span></span>                                                                      |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1c472-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1c472-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="1c472-131">строка</span><span class="sxs-lookup"><span data-stu-id="1c472-131">string</span></span><br/>  | <span data-ttu-id="1c472-132">characters</span><span class="sxs-lookup"><span data-stu-id="1c472-132">characters</span></span><br/> | <span data-ttu-id="1c472-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="1c472-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1c472-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1c472-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1c472-135">Имя параметра</span><span class="sxs-lookup"><span data-stu-id="1c472-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="1c472-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="1c472-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="1c472-137">строка</span><span class="sxs-lookup"><span data-stu-id="1c472-137">string</span></span><br/>  | <span data-ttu-id="1c472-138">Н/Д</span><span class="sxs-lookup"><span data-stu-id="1c472-138">n/a</span></span><br/>        | <span data-ttu-id="1c472-139">True, False</span><span class="sxs-lookup"><span data-stu-id="1c472-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="1c472-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="1c472-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="1c472-141">\_шитсперпажевалуе\_</span><span class="sxs-lookup"><span data-stu-id="1c472-141">\_SheetsPerPageValue\_</span></span><br/>  | <span data-ttu-id="1c472-142">Целое число</span><span class="sxs-lookup"><span data-stu-id="1c472-142">integer</span></span><br/> | <span data-ttu-id="1c472-143">страницы</span><span class="sxs-lookup"><span data-stu-id="1c472-143">pages</span></span><br/>      | <span data-ttu-id="1c472-144">Больше или равно 0.</span><span class="sxs-lookup"><span data-stu-id="1c472-144">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="1c472-145">Указывает число физических страниц на логическую страницу.</span><span class="sxs-lookup"><span data-stu-id="1c472-145">Specifies the number of physical sheets per logical page.</span></span><br/>         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1c472-146">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="1c472-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1c472-147">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="1c472-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1c472-148">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="1c472-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1c472-149">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1c472-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c472-150">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="1c472-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




