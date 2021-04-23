---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 4f6ff85c-8cad-4b9b-8a1d-ce41ed7dfbed
title: паженегативеимаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ec60b0250469bc7035a4add19e0de382e3121bd
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104352022"
---
# <a name="pagenegativeimage"></a><span data-ttu-id="b7697-104">паженегативеимаже</span><span class="sxs-lookup"><span data-stu-id="b7697-104">PageNegativeImage</span></span>

<span data-ttu-id="b7697-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="b7697-105">This topic is not current.</span></span> <span data-ttu-id="b7697-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b7697-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b7697-107">Описывает отрицательное значение параметра OUTPUT.</span><span class="sxs-lookup"><span data-stu-id="b7697-107">Describes the negative setting of the output.</span></span>

-   [<span data-ttu-id="b7697-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b7697-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b7697-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="b7697-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b7697-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b7697-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b7697-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b7697-111">Element Information</span></span>



| <span data-ttu-id="b7697-112">Имя</span><span class="sxs-lookup"><span data-stu-id="b7697-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="b7697-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="b7697-113">Element Type</span></span> <br/>   | <span data-ttu-id="b7697-114">Функция</span><span class="sxs-lookup"><span data-stu-id="b7697-114">Feature</span></span><br/> |
| <span data-ttu-id="b7697-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="b7697-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b7697-116">Страница</span><span class="sxs-lookup"><span data-stu-id="b7697-116">Page</span></span><br/>    |
| <span data-ttu-id="b7697-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="b7697-117">Notes</span></span> <br/>          | <span data-ttu-id="b7697-118">Нет</span><span class="sxs-lookup"><span data-stu-id="b7697-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="b7697-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="b7697-119">Structural Content</span></span>

<span data-ttu-id="b7697-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="b7697-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="b7697-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="b7697-121">Structure Variables</span></span>

<span data-ttu-id="b7697-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="b7697-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b7697-123">Имя</span><span class="sxs-lookup"><span data-stu-id="b7697-123">Name</span></span>                               | <span data-ttu-id="b7697-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b7697-124">Data type</span></span>         | <span data-ttu-id="b7697-125">Unit</span><span class="sxs-lookup"><span data-stu-id="b7697-125">Unit</span></span>                  | <span data-ttu-id="b7697-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="b7697-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b7697-127">Сводка</span><span class="sxs-lookup"><span data-stu-id="b7697-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b7697-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="b7697-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b7697-129">строка</span><span class="sxs-lookup"><span data-stu-id="b7697-129">string</span></span><br/> | <span data-ttu-id="b7697-130">characters</span><span class="sxs-lookup"><span data-stu-id="b7697-130">characters</span></span><br/> | <span data-ttu-id="b7697-131">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="b7697-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b7697-132">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b7697-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b7697-133">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="b7697-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="b7697-134">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="b7697-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b7697-135">строка</span><span class="sxs-lookup"><span data-stu-id="b7697-135">string</span></span><br/> | <span data-ttu-id="b7697-136">Недоступно</span><span class="sxs-lookup"><span data-stu-id="b7697-136">n/a</span></span><br/>        | <span data-ttu-id="b7697-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="b7697-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b7697-138">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="b7697-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b7697-139">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b7697-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b7697-140">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="b7697-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b7697-141">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="b7697-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="b7697-142">См. также</span><span class="sxs-lookup"><span data-stu-id="b7697-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7697-143">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="b7697-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




