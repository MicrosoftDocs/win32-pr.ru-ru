---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: документаутпутбин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f6d16ca000e76b01cd2c3165054d7acc81351b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997141"
---
# <a name="documentoutputbin"></a><span data-ttu-id="f284d-104">документаутпутбин</span><span class="sxs-lookup"><span data-stu-id="f284d-104">DocumentOutputBin</span></span>

<span data-ttu-id="f284d-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="f284d-105">This topic is not current.</span></span> <span data-ttu-id="f284d-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f284d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f284d-107">Содержит полный список поддерживаемых ячеек для устройства.</span><span class="sxs-lookup"><span data-stu-id="f284d-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="f284d-108">Разрешает указание выходной ячейки для каждого документа.</span><span class="sxs-lookup"><span data-stu-id="f284d-108">Allows specification of output bin on a per document basis.</span></span> <span data-ttu-id="f284d-109">Ключевые слова Жобаутпутбин, Документаутпутбин и Пажеаутпутбин являются взаимоисключающими только один из них должен быть указан в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="f284d-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="f284d-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f284d-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="f284d-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="f284d-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="f284d-112">XML-содержимое</span><span class="sxs-lookup"><span data-stu-id="f284d-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f284d-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f284d-113">Element Information</span></span>



| <span data-ttu-id="f284d-114">Имя</span><span class="sxs-lookup"><span data-stu-id="f284d-114">Name</span></span> | <span data-ttu-id="f284d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f284d-115">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="f284d-116">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="f284d-116">Element Type</span></span> <br/>   | <span data-ttu-id="f284d-117">Компонент</span><span class="sxs-lookup"><span data-stu-id="f284d-117">Feature</span></span><br/>  |
| <span data-ttu-id="f284d-118">Префикс области</span><span class="sxs-lookup"><span data-stu-id="f284d-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f284d-119">Документ</span><span class="sxs-lookup"><span data-stu-id="f284d-119">Document</span></span><br/> |
| <span data-ttu-id="f284d-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="f284d-120">Notes</span></span> <br/>          | <span data-ttu-id="f284d-121">Нет</span><span class="sxs-lookup"><span data-stu-id="f284d-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="f284d-122">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="f284d-122">Structural Content</span></span>

<span data-ttu-id="f284d-123">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="f284d-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="f284d-124">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="f284d-124">Structure Variables</span></span>

<span data-ttu-id="f284d-125">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="f284d-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f284d-126">Имя</span><span class="sxs-lookup"><span data-stu-id="f284d-126">Name</span></span>                                   | <span data-ttu-id="f284d-127">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f284d-127">Data type</span></span>          | <span data-ttu-id="f284d-128">Unit</span><span class="sxs-lookup"><span data-stu-id="f284d-128">Unit</span></span>                  | <span data-ttu-id="f284d-129">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="f284d-129">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="f284d-130">Сводка</span><span class="sxs-lookup"><span data-stu-id="f284d-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f284d-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="f284d-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="f284d-132">строка</span><span class="sxs-lookup"><span data-stu-id="f284d-132">string</span></span><br/>  | <span data-ttu-id="f284d-133">characters</span><span class="sxs-lookup"><span data-stu-id="f284d-133">characters</span></span><br/> | <span data-ttu-id="f284d-134">Допустимое полное имя, как определено в https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="f284d-134">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="f284d-135">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f284d-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f284d-136">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="f284d-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="f284d-137">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="f284d-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="f284d-138">строка</span><span class="sxs-lookup"><span data-stu-id="f284d-138">string</span></span><br/>  | <span data-ttu-id="f284d-139">Недоступно</span><span class="sxs-lookup"><span data-stu-id="f284d-139">n/a</span></span><br/>        | <span data-ttu-id="f284d-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="f284d-140">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="f284d-141">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="f284d-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="f284d-142">\_бинтипевалуе\_</span><span class="sxs-lookup"><span data-stu-id="f284d-142">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="f284d-143">строка</span><span class="sxs-lookup"><span data-stu-id="f284d-143">string</span></span><br/>  | <span data-ttu-id="f284d-144">Недоступно</span><span class="sxs-lookup"><span data-stu-id="f284d-144">n/a</span></span><br/>        | <span data-ttu-id="f284d-145">Почтовый ящик, сортировщик, укладчик, финишер, нет.</span><span class="sxs-lookup"><span data-stu-id="f284d-145">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                         | <span data-ttu-id="f284d-146">Указывает общий тип ячейки.</span><span class="sxs-lookup"><span data-stu-id="f284d-146">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="f284d-147">\_медиашиткапаЦитивалуе\_</span><span class="sxs-lookup"><span data-stu-id="f284d-147">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="f284d-148">Целое число</span><span class="sxs-lookup"><span data-stu-id="f284d-148">integer</span></span><br/> | <span data-ttu-id="f284d-149">свойств</span><span class="sxs-lookup"><span data-stu-id="f284d-149">sheets</span></span><br/>     | <span data-ttu-id="f284d-150">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="f284d-150">Greater than 0.</span></span><br/>                                                                                                                                                   | <span data-ttu-id="f284d-151">Указывает емкость носителя в количестве страниц (полный уровень) ячейки.</span><span class="sxs-lookup"><span data-stu-id="f284d-151">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f284d-152">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="f284d-152">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f284d-153">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="f284d-153">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f284d-154">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="f284d-154">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="f284d-155">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="f284d-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f284d-156">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="f284d-156">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




