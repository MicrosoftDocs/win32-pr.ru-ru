---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 4f6ff85c-8cad-4b9b-8a1d-ce41ed7dfbed
title: паженегативеимаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8882c1a5aa026d06b43055a6a74a58c266ea009
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994500"
---
# <a name="pagenegativeimage"></a><span data-ttu-id="b0cbb-104">паженегативеимаже</span><span class="sxs-lookup"><span data-stu-id="b0cbb-104">PageNegativeImage</span></span>

<span data-ttu-id="b0cbb-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="b0cbb-105">This topic is not current.</span></span> <span data-ttu-id="b0cbb-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b0cbb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b0cbb-107">Описывает отрицательное значение параметра OUTPUT.</span><span class="sxs-lookup"><span data-stu-id="b0cbb-107">Describes the negative setting of the output.</span></span>

-   [<span data-ttu-id="b0cbb-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b0cbb-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b0cbb-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="b0cbb-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b0cbb-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b0cbb-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b0cbb-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b0cbb-111">Element Information</span></span>



| <span data-ttu-id="b0cbb-112">Имя</span><span class="sxs-lookup"><span data-stu-id="b0cbb-112">Name</span></span> | <span data-ttu-id="b0cbb-113">Значение</span><span class="sxs-lookup"><span data-stu-id="b0cbb-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="b0cbb-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="b0cbb-114">Element Type</span></span> <br/>   | <span data-ttu-id="b0cbb-115">Компонент</span><span class="sxs-lookup"><span data-stu-id="b0cbb-115">Feature</span></span><br/> |
| <span data-ttu-id="b0cbb-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="b0cbb-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b0cbb-117">Страница</span><span class="sxs-lookup"><span data-stu-id="b0cbb-117">Page</span></span><br/>    |
| <span data-ttu-id="b0cbb-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0cbb-118">Notes</span></span> <br/>          | <span data-ttu-id="b0cbb-119">Нет</span><span class="sxs-lookup"><span data-stu-id="b0cbb-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="b0cbb-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="b0cbb-120">Structural Content</span></span>

<span data-ttu-id="b0cbb-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="b0cbb-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="b0cbb-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="b0cbb-122">Structure Variables</span></span>

<span data-ttu-id="b0cbb-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="b0cbb-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b0cbb-124">Имя</span><span class="sxs-lookup"><span data-stu-id="b0cbb-124">Name</span></span>                               | <span data-ttu-id="b0cbb-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b0cbb-125">Data type</span></span>         | <span data-ttu-id="b0cbb-126">Unit</span><span class="sxs-lookup"><span data-stu-id="b0cbb-126">Unit</span></span>                  | <span data-ttu-id="b0cbb-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="b0cbb-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b0cbb-128">Сводка</span><span class="sxs-lookup"><span data-stu-id="b0cbb-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b0cbb-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="b0cbb-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b0cbb-130">строка</span><span class="sxs-lookup"><span data-stu-id="b0cbb-130">string</span></span><br/> | <span data-ttu-id="b0cbb-131">characters</span><span class="sxs-lookup"><span data-stu-id="b0cbb-131">characters</span></span><br/> | <span data-ttu-id="b0cbb-132">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="b0cbb-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b0cbb-133">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b0cbb-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b0cbb-134">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="b0cbb-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="b0cbb-135">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="b0cbb-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b0cbb-136">строка</span><span class="sxs-lookup"><span data-stu-id="b0cbb-136">string</span></span><br/> | <span data-ttu-id="b0cbb-137">Недоступно</span><span class="sxs-lookup"><span data-stu-id="b0cbb-137">n/a</span></span><br/>        | <span data-ttu-id="b0cbb-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="b0cbb-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b0cbb-139">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="b0cbb-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b0cbb-140">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b0cbb-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b0cbb-141">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="b0cbb-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b0cbb-142">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="b0cbb-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="b0cbb-143">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b0cbb-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0cbb-144">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="b0cbb-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




