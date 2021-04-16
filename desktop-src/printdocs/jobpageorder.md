---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 0c255d50-8b0e-4ecd-876d-eaaccdca7b27
title: жобпажеордер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e554da890464afdaed033490def1a915f9d7d800
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105720829"
---
# <a name="jobpageorder"></a><span data-ttu-id="e19f8-104">жобпажеордер</span><span class="sxs-lookup"><span data-stu-id="e19f8-104">JobPageOrder</span></span>

<span data-ttu-id="e19f8-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="e19f8-105">This topic is not current.</span></span> <span data-ttu-id="e19f8-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e19f8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e19f8-107">Определяет порядок физических страниц для выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e19f8-107">Defines the order of physical pages for the output.</span></span>

-   [<span data-ttu-id="e19f8-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e19f8-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e19f8-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="e19f8-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e19f8-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="e19f8-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e19f8-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e19f8-111">Element Information</span></span>



| <span data-ttu-id="e19f8-112">Имя</span><span class="sxs-lookup"><span data-stu-id="e19f8-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="e19f8-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="e19f8-113">Element Type</span></span> <br/>   | <span data-ttu-id="e19f8-114">Функция</span><span class="sxs-lookup"><span data-stu-id="e19f8-114">Feature</span></span><br/> |
| <span data-ttu-id="e19f8-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="e19f8-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e19f8-116">Задание</span><span class="sxs-lookup"><span data-stu-id="e19f8-116">Job</span></span><br/>     |
| <span data-ttu-id="e19f8-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="e19f8-117">Notes</span></span> <br/>          | <span data-ttu-id="e19f8-118">Нет</span><span class="sxs-lookup"><span data-stu-id="e19f8-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="e19f8-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="e19f8-119">Structural Content</span></span>

<span data-ttu-id="e19f8-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="e19f8-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPageOrder">
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

## <a name="structure-variables"></a><span data-ttu-id="e19f8-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="e19f8-121">Structure Variables</span></span>

<span data-ttu-id="e19f8-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="e19f8-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e19f8-123">Имя</span><span class="sxs-lookup"><span data-stu-id="e19f8-123">Name</span></span>                               | <span data-ttu-id="e19f8-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e19f8-124">Data type</span></span>         | <span data-ttu-id="e19f8-125">Unit</span><span class="sxs-lookup"><span data-stu-id="e19f8-125">Unit</span></span>                  | <span data-ttu-id="e19f8-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="e19f8-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e19f8-127">Сводка</span><span class="sxs-lookup"><span data-stu-id="e19f8-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e19f8-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e19f8-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e19f8-129">строка</span><span class="sxs-lookup"><span data-stu-id="e19f8-129">string</span></span><br/> | <span data-ttu-id="e19f8-130">characters</span><span class="sxs-lookup"><span data-stu-id="e19f8-130">characters</span></span><br/> | <span data-ttu-id="e19f8-131">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="e19f8-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e19f8-132">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e19f8-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e19f8-133">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="e19f8-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="e19f8-134">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="e19f8-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e19f8-135">строка</span><span class="sxs-lookup"><span data-stu-id="e19f8-135">string</span></span><br/> | <span data-ttu-id="e19f8-136">Недоступно</span><span class="sxs-lookup"><span data-stu-id="e19f8-136">n/a</span></span><br/>        | <span data-ttu-id="e19f8-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="e19f8-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e19f8-138">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="e19f8-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e19f8-139">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="e19f8-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e19f8-140">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="e19f8-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e19f8-141">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="e19f8-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPageOrder">
  <psf:Property name="psf:SelectionType">
   <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies front to back page order. -->
  <psf:Option name="psk:Standard" />
  <!-- Specifies back to front page order. -->
  <psf:Option name="psk:Reverse" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="e19f8-142">См. также</span><span class="sxs-lookup"><span data-stu-id="e19f8-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e19f8-143">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="e19f8-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




