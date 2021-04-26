---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 8eb4e574-3209-459c-9a25-95377b2f7439
title: документроллкут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d4bfb09a1c3f6f43f11886685a0edfcf2bbd92
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997051"
---
# <a name="documentrollcut"></a><span data-ttu-id="feaa7-104">документроллкут</span><span class="sxs-lookup"><span data-stu-id="feaa7-104">DocumentRollCut</span></span>

<span data-ttu-id="feaa7-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="feaa7-105">This topic is not current.</span></span> <span data-ttu-id="feaa7-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="feaa7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="feaa7-107">Описывает метод обрезания рулонной бумаги.</span><span class="sxs-lookup"><span data-stu-id="feaa7-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="feaa7-108">Каждый документ обрабатывается отдельно.</span><span class="sxs-lookup"><span data-stu-id="feaa7-108">Each document is handled separately.</span></span> <span data-ttu-id="feaa7-109">Указанные параметры описывают различные методы для свертывания.</span><span class="sxs-lookup"><span data-stu-id="feaa7-109">The specified options describe the different methods for roll cut.</span></span>

-   [<span data-ttu-id="feaa7-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="feaa7-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="feaa7-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="feaa7-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="feaa7-112">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="feaa7-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="feaa7-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="feaa7-113">Element Information</span></span>



| <span data-ttu-id="feaa7-114">Имя</span><span class="sxs-lookup"><span data-stu-id="feaa7-114">Name</span></span> | <span data-ttu-id="feaa7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="feaa7-115">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="feaa7-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="feaa7-116">Element Type</span></span> <br/>   | <span data-ttu-id="feaa7-117">Компонент</span><span class="sxs-lookup"><span data-stu-id="feaa7-117">Feature</span></span><br/>  |
| <span data-ttu-id="feaa7-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="feaa7-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="feaa7-119">Документ</span><span class="sxs-lookup"><span data-stu-id="feaa7-119">Document</span></span><br/> |
| <span data-ttu-id="feaa7-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="feaa7-120">Notes</span></span> <br/>          | <span data-ttu-id="feaa7-121">Нет</span><span class="sxs-lookup"><span data-stu-id="feaa7-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="feaa7-122">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="feaa7-122">Structural Content</span></span>

<span data-ttu-id="feaa7-123">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="feaa7-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="feaa7-124">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="feaa7-124">Structure Variables</span></span>

<span data-ttu-id="feaa7-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="feaa7-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="feaa7-126">Имя</span><span class="sxs-lookup"><span data-stu-id="feaa7-126">Name</span></span>                               | <span data-ttu-id="feaa7-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="feaa7-127">Data type</span></span>         | <span data-ttu-id="feaa7-128">Unit</span><span class="sxs-lookup"><span data-stu-id="feaa7-128">Unit</span></span>                  | <span data-ttu-id="feaa7-129">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="feaa7-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="feaa7-130">Сводка</span><span class="sxs-lookup"><span data-stu-id="feaa7-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="feaa7-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="feaa7-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="feaa7-132">строка</span><span class="sxs-lookup"><span data-stu-id="feaa7-132">string</span></span><br/> | <span data-ttu-id="feaa7-133">characters</span><span class="sxs-lookup"><span data-stu-id="feaa7-133">characters</span></span><br/> | <span data-ttu-id="feaa7-134">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="feaa7-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="feaa7-135">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="feaa7-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="feaa7-136">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="feaa7-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="feaa7-137">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="feaa7-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="feaa7-138">строка</span><span class="sxs-lookup"><span data-stu-id="feaa7-138">string</span></span><br/> | <span data-ttu-id="feaa7-139">Недоступно</span><span class="sxs-lookup"><span data-stu-id="feaa7-139">n/a</span></span><br/>        | <span data-ttu-id="feaa7-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="feaa7-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="feaa7-141">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="feaa7-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="feaa7-142">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="feaa7-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="feaa7-143">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="feaa7-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="feaa7-144">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="feaa7-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="feaa7-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="feaa7-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="feaa7-146">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="feaa7-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




