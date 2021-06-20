---
description: Сведения об элементе Жобпажеордер, который определяет порядок физических страниц для выходных данных.
ms.assetid: 0c255d50-8b0e-4ecd-876d-eaaccdca7b27
title: жобпажеордер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2216330034c458095af7e67ff0904100126451
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408747"
---
# <a name="jobpageorder"></a><span data-ttu-id="706cb-103">жобпажеордер</span><span class="sxs-lookup"><span data-stu-id="706cb-103">JobPageOrder</span></span>

<span data-ttu-id="706cb-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="706cb-104">This topic is not current.</span></span> <span data-ttu-id="706cb-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="706cb-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="706cb-106">Определяет порядок физических страниц для выходных данных.</span><span class="sxs-lookup"><span data-stu-id="706cb-106">Defines the order of physical pages for the output.</span></span>

-   [<span data-ttu-id="706cb-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="706cb-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="706cb-108">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="706cb-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="706cb-109">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="706cb-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="706cb-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="706cb-110">Element Information</span></span>



| <span data-ttu-id="706cb-111">Имя</span><span class="sxs-lookup"><span data-stu-id="706cb-111">Name</span></span> | <span data-ttu-id="706cb-112">Значение</span><span class="sxs-lookup"><span data-stu-id="706cb-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="706cb-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="706cb-113">Element Type</span></span> <br/>   | <span data-ttu-id="706cb-114">Компонент</span><span class="sxs-lookup"><span data-stu-id="706cb-114">Feature</span></span><br/> |
| <span data-ttu-id="706cb-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="706cb-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="706cb-116">Задание</span><span class="sxs-lookup"><span data-stu-id="706cb-116">Job</span></span><br/>     |
| <span data-ttu-id="706cb-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="706cb-117">Notes</span></span> <br/>          | <span data-ttu-id="706cb-118">Нет</span><span class="sxs-lookup"><span data-stu-id="706cb-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="706cb-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="706cb-119">Structural Content</span></span>

<span data-ttu-id="706cb-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="706cb-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="706cb-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="706cb-121">Structure Variables</span></span>

<span data-ttu-id="706cb-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="706cb-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="706cb-123">Имя</span><span class="sxs-lookup"><span data-stu-id="706cb-123">Name</span></span>                               | <span data-ttu-id="706cb-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="706cb-124">Data type</span></span>         | <span data-ttu-id="706cb-125">Unit</span><span class="sxs-lookup"><span data-stu-id="706cb-125">Unit</span></span>                  | <span data-ttu-id="706cb-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="706cb-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="706cb-127">Итоги</span><span class="sxs-lookup"><span data-stu-id="706cb-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="706cb-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="706cb-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="706cb-129">строка</span><span class="sxs-lookup"><span data-stu-id="706cb-129">string</span></span><br/> | <span data-ttu-id="706cb-130">characters</span><span class="sxs-lookup"><span data-stu-id="706cb-130">characters</span></span><br/> | <span data-ttu-id="706cb-131">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="706cb-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="706cb-132">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="706cb-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="706cb-133">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="706cb-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="706cb-134">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="706cb-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="706cb-135">строка</span><span class="sxs-lookup"><span data-stu-id="706cb-135">string</span></span><br/> | <span data-ttu-id="706cb-136">Недоступно</span><span class="sxs-lookup"><span data-stu-id="706cb-136">n/a</span></span><br/>        | <span data-ttu-id="706cb-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="706cb-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="706cb-138">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="706cb-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="706cb-139">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="706cb-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="706cb-140">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="706cb-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="706cb-141">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="706cb-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="706cb-142">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="706cb-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="706cb-143">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="706cb-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




