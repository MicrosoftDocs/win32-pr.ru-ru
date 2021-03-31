---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: документаутпутбин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444ca63fee0b76f17909b1aa08e65cd468537dee
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104273359"
---
# <a name="documentoutputbin"></a><span data-ttu-id="aaeec-104">документаутпутбин</span><span class="sxs-lookup"><span data-stu-id="aaeec-104">DocumentOutputBin</span></span>

<span data-ttu-id="aaeec-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="aaeec-105">This topic is not current.</span></span> <span data-ttu-id="aaeec-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="aaeec-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="aaeec-107">Содержит полный список поддерживаемых ячеек для устройства.</span><span class="sxs-lookup"><span data-stu-id="aaeec-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="aaeec-108">Разрешает указание выходной ячейки для каждого документа.</span><span class="sxs-lookup"><span data-stu-id="aaeec-108">Allows specification of output bin on a per document basis.</span></span> <span data-ttu-id="aaeec-109">Ключевые слова Жобаутпутбин, Документаутпутбин и Пажеаутпутбин являются взаимоисключающими только один из них должен быть указан в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="aaeec-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="aaeec-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="aaeec-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="aaeec-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="aaeec-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="aaeec-112">XML-содержимое</span><span class="sxs-lookup"><span data-stu-id="aaeec-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="aaeec-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="aaeec-113">Element Information</span></span>



| <span data-ttu-id="aaeec-114">Имя</span><span class="sxs-lookup"><span data-stu-id="aaeec-114">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="aaeec-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="aaeec-115">Element Type</span></span> <br/>   | <span data-ttu-id="aaeec-116">Функция</span><span class="sxs-lookup"><span data-stu-id="aaeec-116">Feature</span></span><br/>  |
| <span data-ttu-id="aaeec-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="aaeec-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="aaeec-118">Документ</span><span class="sxs-lookup"><span data-stu-id="aaeec-118">Document</span></span><br/> |
| <span data-ttu-id="aaeec-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="aaeec-119">Notes</span></span> <br/>          | <span data-ttu-id="aaeec-120">Нет</span><span class="sxs-lookup"><span data-stu-id="aaeec-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="aaeec-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="aaeec-121">Structural Content</span></span>

<span data-ttu-id="aaeec-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="aaeec-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="aaeec-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="aaeec-123">Structure Variables</span></span>

<span data-ttu-id="aaeec-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="aaeec-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="aaeec-125">Имя</span><span class="sxs-lookup"><span data-stu-id="aaeec-125">Name</span></span>                                   | <span data-ttu-id="aaeec-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="aaeec-126">Data type</span></span>          | <span data-ttu-id="aaeec-127">Unit</span><span class="sxs-lookup"><span data-stu-id="aaeec-127">Unit</span></span>                  | <span data-ttu-id="aaeec-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="aaeec-128">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="aaeec-129">Сводка</span><span class="sxs-lookup"><span data-stu-id="aaeec-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aaeec-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="aaeec-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="aaeec-131">строка</span><span class="sxs-lookup"><span data-stu-id="aaeec-131">string</span></span><br/>  | <span data-ttu-id="aaeec-132">characters</span><span class="sxs-lookup"><span data-stu-id="aaeec-132">characters</span></span><br/> | <span data-ttu-id="aaeec-133">Допустимое полное имя, как определено в https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="aaeec-133">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="aaeec-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aaeec-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="aaeec-135">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="aaeec-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="aaeec-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="aaeec-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="aaeec-137">строка</span><span class="sxs-lookup"><span data-stu-id="aaeec-137">string</span></span><br/>  | <span data-ttu-id="aaeec-138">Недоступно</span><span class="sxs-lookup"><span data-stu-id="aaeec-138">n/a</span></span><br/>        | <span data-ttu-id="aaeec-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="aaeec-139">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="aaeec-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="aaeec-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="aaeec-141">\_бинтипевалуе\_</span><span class="sxs-lookup"><span data-stu-id="aaeec-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="aaeec-142">строка</span><span class="sxs-lookup"><span data-stu-id="aaeec-142">string</span></span><br/>  | <span data-ttu-id="aaeec-143">Недоступно</span><span class="sxs-lookup"><span data-stu-id="aaeec-143">n/a</span></span><br/>        | <span data-ttu-id="aaeec-144">Почтовый ящик, сортировщик, укладчик, финишер, нет.</span><span class="sxs-lookup"><span data-stu-id="aaeec-144">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                         | <span data-ttu-id="aaeec-145">Указывает общий тип ячейки.</span><span class="sxs-lookup"><span data-stu-id="aaeec-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="aaeec-146">\_медиашиткапаЦитивалуе\_</span><span class="sxs-lookup"><span data-stu-id="aaeec-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="aaeec-147">Целое число</span><span class="sxs-lookup"><span data-stu-id="aaeec-147">integer</span></span><br/> | <span data-ttu-id="aaeec-148">свойств</span><span class="sxs-lookup"><span data-stu-id="aaeec-148">sheets</span></span><br/>     | <span data-ttu-id="aaeec-149">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="aaeec-149">Greater than 0.</span></span><br/>                                                                                                                                                   | <span data-ttu-id="aaeec-150">Указывает емкость носителя в количестве страниц (полный уровень) ячейки.</span><span class="sxs-lookup"><span data-stu-id="aaeec-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="aaeec-151">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="aaeec-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="aaeec-152">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="aaeec-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="aaeec-153">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="aaeec-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="aaeec-154">См. также</span><span class="sxs-lookup"><span data-stu-id="aaeec-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaeec-155">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="aaeec-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




