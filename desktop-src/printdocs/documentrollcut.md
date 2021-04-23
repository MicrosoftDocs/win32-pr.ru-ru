---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 8eb4e574-3209-459c-9a25-95377b2f7439
title: документроллкут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3a20c02c50638d532660845efc1b3894f4a7e1
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104273364"
---
# <a name="documentrollcut"></a><span data-ttu-id="9ae28-104">документроллкут</span><span class="sxs-lookup"><span data-stu-id="9ae28-104">DocumentRollCut</span></span>

<span data-ttu-id="9ae28-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="9ae28-105">This topic is not current.</span></span> <span data-ttu-id="9ae28-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9ae28-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9ae28-107">Описывает метод обрезания рулонной бумаги.</span><span class="sxs-lookup"><span data-stu-id="9ae28-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="9ae28-108">Каждый документ обрабатывается отдельно.</span><span class="sxs-lookup"><span data-stu-id="9ae28-108">Each document is handled separately.</span></span> <span data-ttu-id="9ae28-109">Указанные параметры описывают различные методы для свертывания.</span><span class="sxs-lookup"><span data-stu-id="9ae28-109">The specified options describe the different methods for roll cut.</span></span>

-   [<span data-ttu-id="9ae28-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9ae28-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9ae28-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="9ae28-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9ae28-112">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="9ae28-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9ae28-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9ae28-113">Element Information</span></span>



| <span data-ttu-id="9ae28-114">Имя</span><span class="sxs-lookup"><span data-stu-id="9ae28-114">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="9ae28-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="9ae28-115">Element Type</span></span> <br/>   | <span data-ttu-id="9ae28-116">Функция</span><span class="sxs-lookup"><span data-stu-id="9ae28-116">Feature</span></span><br/>  |
| <span data-ttu-id="9ae28-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="9ae28-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9ae28-118">Документ</span><span class="sxs-lookup"><span data-stu-id="9ae28-118">Document</span></span><br/> |
| <span data-ttu-id="9ae28-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="9ae28-119">Notes</span></span> <br/>          | <span data-ttu-id="9ae28-120">Нет</span><span class="sxs-lookup"><span data-stu-id="9ae28-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="9ae28-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="9ae28-121">Structural Content</span></span>

<span data-ttu-id="9ae28-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="9ae28-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentRollCut">
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

## <a name="structure-variables"></a><span data-ttu-id="9ae28-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="9ae28-123">Structure Variables</span></span>

<span data-ttu-id="9ae28-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="9ae28-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9ae28-125">Имя</span><span class="sxs-lookup"><span data-stu-id="9ae28-125">Name</span></span>                               | <span data-ttu-id="9ae28-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9ae28-126">Data type</span></span>         | <span data-ttu-id="9ae28-127">Unit</span><span class="sxs-lookup"><span data-stu-id="9ae28-127">Unit</span></span>                  | <span data-ttu-id="9ae28-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="9ae28-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9ae28-129">Сводка</span><span class="sxs-lookup"><span data-stu-id="9ae28-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9ae28-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="9ae28-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9ae28-131">строка</span><span class="sxs-lookup"><span data-stu-id="9ae28-131">string</span></span><br/> | <span data-ttu-id="9ae28-132">characters</span><span class="sxs-lookup"><span data-stu-id="9ae28-132">characters</span></span><br/> | <span data-ttu-id="9ae28-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="9ae28-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9ae28-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9ae28-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9ae28-135">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="9ae28-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9ae28-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="9ae28-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9ae28-137">строка</span><span class="sxs-lookup"><span data-stu-id="9ae28-137">string</span></span><br/> | <span data-ttu-id="9ae28-138">Недоступно</span><span class="sxs-lookup"><span data-stu-id="9ae28-138">n/a</span></span><br/>        | <span data-ttu-id="9ae28-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="9ae28-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9ae28-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="9ae28-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9ae28-141">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="9ae28-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9ae28-142">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="9ae28-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9ae28-143">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="9ae28-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentRollCut">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies cutting method for banner -->
  <psf:Option name="psk:Banner" />
  <!-- Specifies cutting at the edge of the image --> 
  <psf:Option name="psk:CutSheetAtImageEdge" />
  <!-- Specifies cutting for media size selected for PageMediaSize -->
  <psf:Option name="psk:CutSheetAtStandardMediaSize" />
  <!-- Specifies no document roll cut -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="9ae28-144">См. также</span><span class="sxs-lookup"><span data-stu-id="9ae28-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ae28-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="9ae28-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




