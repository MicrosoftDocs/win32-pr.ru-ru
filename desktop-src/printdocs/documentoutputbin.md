---
description: Сведения о Документаутпутбин, описывающем полный список поддерживаемых ячеек для устройства, и возможность указания выходного лотка для каждого документа.
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: документаутпутбин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afc20f15aed8d3076afb79d755c54791573b393
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409247"
---
# <a name="documentoutputbin"></a><span data-ttu-id="57af1-103">документаутпутбин</span><span class="sxs-lookup"><span data-stu-id="57af1-103">DocumentOutputBin</span></span>

<span data-ttu-id="57af1-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="57af1-104">This topic is not current.</span></span> <span data-ttu-id="57af1-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="57af1-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="57af1-106">Содержит полный список поддерживаемых ячеек для устройства.</span><span class="sxs-lookup"><span data-stu-id="57af1-106">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="57af1-107">Разрешает указание выходной ячейки для каждого документа.</span><span class="sxs-lookup"><span data-stu-id="57af1-107">Allows specification of output bin on a per document basis.</span></span> <span data-ttu-id="57af1-108">Ключевые слова Жобаутпутбин, Документаутпутбин и Пажеаутпутбин являются взаимоисключающими только один из них должен быть указан в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="57af1-108">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="57af1-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="57af1-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="57af1-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="57af1-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="57af1-111">XML-содержимое</span><span class="sxs-lookup"><span data-stu-id="57af1-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="57af1-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="57af1-112">Element Information</span></span>



| <span data-ttu-id="57af1-113">Имя</span><span class="sxs-lookup"><span data-stu-id="57af1-113">Name</span></span> | <span data-ttu-id="57af1-114">Значение</span><span class="sxs-lookup"><span data-stu-id="57af1-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="57af1-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="57af1-115">Element Type</span></span> <br/>   | <span data-ttu-id="57af1-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="57af1-116">Feature</span></span><br/>  |
| <span data-ttu-id="57af1-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="57af1-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="57af1-118">Документ</span><span class="sxs-lookup"><span data-stu-id="57af1-118">Document</span></span><br/> |
| <span data-ttu-id="57af1-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="57af1-119">Notes</span></span> <br/>          | <span data-ttu-id="57af1-120">Нет</span><span class="sxs-lookup"><span data-stu-id="57af1-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="57af1-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="57af1-121">Structural Content</span></span>

<span data-ttu-id="57af1-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="57af1-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="57af1-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="57af1-123">Structure Variables</span></span>

<span data-ttu-id="57af1-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="57af1-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="57af1-125">Имя</span><span class="sxs-lookup"><span data-stu-id="57af1-125">Name</span></span>                                   | <span data-ttu-id="57af1-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="57af1-126">Data type</span></span>          | <span data-ttu-id="57af1-127">Unit</span><span class="sxs-lookup"><span data-stu-id="57af1-127">Unit</span></span>                  | <span data-ttu-id="57af1-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="57af1-128">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="57af1-129">Итоги</span><span class="sxs-lookup"><span data-stu-id="57af1-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="57af1-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="57af1-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="57af1-131">строка</span><span class="sxs-lookup"><span data-stu-id="57af1-131">string</span></span><br/>  | <span data-ttu-id="57af1-132">characters</span><span class="sxs-lookup"><span data-stu-id="57af1-132">characters</span></span><br/> | <span data-ttu-id="57af1-133">Допустимое полное имя, как определено в https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="57af1-133">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="57af1-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="57af1-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="57af1-135">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="57af1-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="57af1-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="57af1-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="57af1-137">строка</span><span class="sxs-lookup"><span data-stu-id="57af1-137">string</span></span><br/>  | <span data-ttu-id="57af1-138">Недоступно</span><span class="sxs-lookup"><span data-stu-id="57af1-138">n/a</span></span><br/>        | <span data-ttu-id="57af1-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="57af1-139">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="57af1-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="57af1-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="57af1-141">\_бинтипевалуе\_</span><span class="sxs-lookup"><span data-stu-id="57af1-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="57af1-142">строка</span><span class="sxs-lookup"><span data-stu-id="57af1-142">string</span></span><br/>  | <span data-ttu-id="57af1-143">Недоступно</span><span class="sxs-lookup"><span data-stu-id="57af1-143">n/a</span></span><br/>        | <span data-ttu-id="57af1-144">Почтовый ящик, сортировщик, укладчик, финишер, нет.</span><span class="sxs-lookup"><span data-stu-id="57af1-144">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                         | <span data-ttu-id="57af1-145">Указывает общий тип ячейки.</span><span class="sxs-lookup"><span data-stu-id="57af1-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="57af1-146">\_медиашиткапаЦитивалуе\_</span><span class="sxs-lookup"><span data-stu-id="57af1-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="57af1-147">Целое число</span><span class="sxs-lookup"><span data-stu-id="57af1-147">integer</span></span><br/> | <span data-ttu-id="57af1-148">свойств</span><span class="sxs-lookup"><span data-stu-id="57af1-148">sheets</span></span><br/>     | <span data-ttu-id="57af1-149">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="57af1-149">Greater than 0.</span></span><br/>                                                                                                                                                   | <span data-ttu-id="57af1-150">Указывает емкость носителя в количестве страниц (полный уровень) ячейки.</span><span class="sxs-lookup"><span data-stu-id="57af1-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="57af1-151">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="57af1-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="57af1-152">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="57af1-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="57af1-153">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="57af1-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!--Specifies type of output bin-->
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!--Specifies media capacity for output bin-->
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="57af1-154">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="57af1-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57af1-155">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="57af1-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




