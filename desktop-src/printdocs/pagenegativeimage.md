---
description: Ознакомьтесь с элементом Паженегативеимаже, настраиваемым пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 4f6ff85c-8cad-4b9b-8a1d-ce41ed7dfbed
title: паженегативеимаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1e1a9de2d82135adb82c68f45785ee3763e41a
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395659"
---
# <a name="pagenegativeimage"></a><span data-ttu-id="b9071-105">паженегативеимаже</span><span class="sxs-lookup"><span data-stu-id="b9071-105">PageNegativeImage</span></span>

<span data-ttu-id="b9071-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="b9071-106">This topic is not current.</span></span> <span data-ttu-id="b9071-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b9071-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b9071-108">Описывает отрицательное значение параметра OUTPUT.</span><span class="sxs-lookup"><span data-stu-id="b9071-108">Describes the negative setting of the output.</span></span>

-   [<span data-ttu-id="b9071-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b9071-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b9071-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="b9071-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b9071-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b9071-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b9071-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b9071-112">Element Information</span></span>



| <span data-ttu-id="b9071-113">Имя</span><span class="sxs-lookup"><span data-stu-id="b9071-113">Name</span></span> | <span data-ttu-id="b9071-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b9071-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="b9071-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="b9071-115">Element Type</span></span> <br/>   | <span data-ttu-id="b9071-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="b9071-116">Feature</span></span><br/> |
| <span data-ttu-id="b9071-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="b9071-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b9071-118">Страница</span><span class="sxs-lookup"><span data-stu-id="b9071-118">Page</span></span><br/>    |
| <span data-ttu-id="b9071-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="b9071-119">Notes</span></span> <br/>          | <span data-ttu-id="b9071-120">Нет</span><span class="sxs-lookup"><span data-stu-id="b9071-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="b9071-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="b9071-121">Structural Content</span></span>

<span data-ttu-id="b9071-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="b9071-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageNegativeImage">
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

## <a name="structure-variables"></a><span data-ttu-id="b9071-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="b9071-123">Structure Variables</span></span>

<span data-ttu-id="b9071-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="b9071-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b9071-125">Имя</span><span class="sxs-lookup"><span data-stu-id="b9071-125">Name</span></span>                               | <span data-ttu-id="b9071-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b9071-126">Data type</span></span>         | <span data-ttu-id="b9071-127">Unit</span><span class="sxs-lookup"><span data-stu-id="b9071-127">Unit</span></span>                  | <span data-ttu-id="b9071-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="b9071-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b9071-129">Итоги</span><span class="sxs-lookup"><span data-stu-id="b9071-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b9071-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="b9071-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b9071-131">строка</span><span class="sxs-lookup"><span data-stu-id="b9071-131">string</span></span><br/> | <span data-ttu-id="b9071-132">characters</span><span class="sxs-lookup"><span data-stu-id="b9071-132">characters</span></span><br/> | <span data-ttu-id="b9071-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="b9071-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b9071-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b9071-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b9071-135">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="b9071-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="b9071-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="b9071-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b9071-137">строка</span><span class="sxs-lookup"><span data-stu-id="b9071-137">string</span></span><br/> | <span data-ttu-id="b9071-138">Недоступно</span><span class="sxs-lookup"><span data-stu-id="b9071-138">n/a</span></span><br/>        | <span data-ttu-id="b9071-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="b9071-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b9071-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="b9071-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b9071-141">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b9071-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b9071-142">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="b9071-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b9071-143">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="b9071-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageNegativeImage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be the negative image. -->
  <psf:Option name="psk:Negative" />
  <!-- Specifies the output should be the non-negative image. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="b9071-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b9071-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9071-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="b9071-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




