---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 40925dfe-494c-49b5-ae57-de369723ba76
title: жобаутпутоптимизатион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d07bb98ea639753acc1b99b53d3785480a283a5
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105720830"
---
# <a name="joboutputoptimization"></a><span data-ttu-id="f4616-104">жобаутпутоптимизатион</span><span class="sxs-lookup"><span data-stu-id="f4616-104">JobOutputOptimization</span></span>

<span data-ttu-id="f4616-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="f4616-105">This topic is not current.</span></span> <span data-ttu-id="f4616-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f4616-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f4616-107">Описывает обработку заданий, предназначенную для оптимизации выходных данных для определенных сценариев использования, как указано в указанном параметре.</span><span class="sxs-lookup"><span data-stu-id="f4616-107">Describes the job processing, intended to optimize the output for particular use scenarios as indicated by the option specified.</span></span>

-   [<span data-ttu-id="f4616-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f4616-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f4616-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="f4616-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f4616-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="f4616-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f4616-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f4616-111">Element Information</span></span>



| <span data-ttu-id="f4616-112">Имя</span><span class="sxs-lookup"><span data-stu-id="f4616-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="f4616-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="f4616-113">Element Type</span></span> <br/>   | <span data-ttu-id="f4616-114">Функция</span><span class="sxs-lookup"><span data-stu-id="f4616-114">Feature</span></span><br/> |
| <span data-ttu-id="f4616-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="f4616-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f4616-116">Задание</span><span class="sxs-lookup"><span data-stu-id="f4616-116">Job</span></span><br/>     |
| <span data-ttu-id="f4616-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="f4616-117">Notes</span></span> <br/>          | <span data-ttu-id="f4616-118">Нет</span><span class="sxs-lookup"><span data-stu-id="f4616-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="f4616-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="f4616-119">Structural Content</span></span>

<span data-ttu-id="f4616-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="f4616-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputOptimization">
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

## <a name="structure-variables"></a><span data-ttu-id="f4616-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="f4616-121">Structure Variables</span></span>

<span data-ttu-id="f4616-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="f4616-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f4616-123">Имя</span><span class="sxs-lookup"><span data-stu-id="f4616-123">Name</span></span>                               | <span data-ttu-id="f4616-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f4616-124">Data type</span></span>         | <span data-ttu-id="f4616-125">Unit</span><span class="sxs-lookup"><span data-stu-id="f4616-125">Unit</span></span>                  | <span data-ttu-id="f4616-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="f4616-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f4616-127">Сводка</span><span class="sxs-lookup"><span data-stu-id="f4616-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f4616-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="f4616-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f4616-129">строка</span><span class="sxs-lookup"><span data-stu-id="f4616-129">string</span></span><br/> | <span data-ttu-id="f4616-130">characters</span><span class="sxs-lookup"><span data-stu-id="f4616-130">characters</span></span><br/> | <span data-ttu-id="f4616-131">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="f4616-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f4616-132">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4616-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f4616-133">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="f4616-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="f4616-134">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="f4616-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f4616-135">строка</span><span class="sxs-lookup"><span data-stu-id="f4616-135">string</span></span><br/> | <span data-ttu-id="f4616-136">Недоступно</span><span class="sxs-lookup"><span data-stu-id="f4616-136">n/a</span></span><br/>        | <span data-ttu-id="f4616-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="f4616-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f4616-138">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="f4616-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f4616-139">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="f4616-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f4616-140">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="f4616-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f4616-141">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="f4616-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputOptimization">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the job processing be optimized for archive output. -->
  <psf:Option name="psk:ArchiveFormat" />
  <!-- Specifies the job processing be optimized for portability (cross-device) of output. -->
  <psf:Option name="psk:OptimizeForPortability" />
  <!-- Specifies the job processing be optimized for quality of output. -->
  <psf:Option name="psk:OptimizeForQuality" />
  <!-- Specifies the job processing be optimized for speed of output. -->
  <psf:Option name="psk:OptimizeForSpeed" />
  <!-- Specifies the job processing should not be optimized for a particular scenario. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="f4616-142">См. также</span><span class="sxs-lookup"><span data-stu-id="f4616-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4616-143">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="f4616-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




