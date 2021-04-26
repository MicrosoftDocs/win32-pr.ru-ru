---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: жобаутпутбин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 973433ac7f6e051d4656777696cc3a37cedd953b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999221"
---
# <a name="joboutputbin"></a><span data-ttu-id="fec21-104">жобаутпутбин</span><span class="sxs-lookup"><span data-stu-id="fec21-104">JobOutputBin</span></span>

<span data-ttu-id="fec21-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="fec21-105">This topic is not current.</span></span> <span data-ttu-id="fec21-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fec21-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fec21-107">Описывает установленный выходной лоток на устройстве или полный список поддерживаемых ячеек для устройства.</span><span class="sxs-lookup"><span data-stu-id="fec21-107">Describes the installed output bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="fec21-108">Ключевые слова Жобаутпутбин, Документаутпутбин и Пажеаутпутбин являются взаимоисключающими только один из них должен быть указан в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="fec21-108">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="fec21-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fec21-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fec21-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="fec21-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="fec21-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="fec21-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="fec21-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fec21-112">Element Information</span></span>



| <span data-ttu-id="fec21-113">Имя</span><span class="sxs-lookup"><span data-stu-id="fec21-113">Name</span></span> | <span data-ttu-id="fec21-114">Значение</span><span class="sxs-lookup"><span data-stu-id="fec21-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="fec21-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="fec21-115">Element Type</span></span> <br/>   | <span data-ttu-id="fec21-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="fec21-116">Feature</span></span><br/> |
| <span data-ttu-id="fec21-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="fec21-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fec21-118">Задание</span><span class="sxs-lookup"><span data-stu-id="fec21-118">Job</span></span><br/>     |
| <span data-ttu-id="fec21-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="fec21-119">Notes</span></span> <br/>          | <span data-ttu-id="fec21-120">Нет</span><span class="sxs-lookup"><span data-stu-id="fec21-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="fec21-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="fec21-121">Structural Content</span></span>

<span data-ttu-id="fec21-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="fec21-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="fec21-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="fec21-123">Structure Variables</span></span>

<span data-ttu-id="fec21-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="fec21-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fec21-125">Имя</span><span class="sxs-lookup"><span data-stu-id="fec21-125">Name</span></span>                                   | <span data-ttu-id="fec21-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fec21-126">Data type</span></span>          | <span data-ttu-id="fec21-127">Unit</span><span class="sxs-lookup"><span data-stu-id="fec21-127">Unit</span></span>                  | <span data-ttu-id="fec21-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="fec21-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="fec21-129">Сводка</span><span class="sxs-lookup"><span data-stu-id="fec21-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fec21-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="fec21-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="fec21-131">строка</span><span class="sxs-lookup"><span data-stu-id="fec21-131">string</span></span><br/>  | <span data-ttu-id="fec21-132">characters</span><span class="sxs-lookup"><span data-stu-id="fec21-132">characters</span></span><br/> | <span data-ttu-id="fec21-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="fec21-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="fec21-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fec21-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="fec21-135">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="fec21-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="fec21-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="fec21-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="fec21-137">строка</span><span class="sxs-lookup"><span data-stu-id="fec21-137">string</span></span><br/>  | <span data-ttu-id="fec21-138">Недоступно</span><span class="sxs-lookup"><span data-stu-id="fec21-138">n/a</span></span><br/>        | <span data-ttu-id="fec21-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="fec21-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="fec21-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="fec21-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="fec21-141">\_бинтипевалуе\_</span><span class="sxs-lookup"><span data-stu-id="fec21-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="fec21-142">строка</span><span class="sxs-lookup"><span data-stu-id="fec21-142">string</span></span><br/>  | <span data-ttu-id="fec21-143">Недоступно</span><span class="sxs-lookup"><span data-stu-id="fec21-143">n/a</span></span><br/>        | <span data-ttu-id="fec21-144">Почтовый ящик, сортировщик, укладчик, финишер, нет.</span><span class="sxs-lookup"><span data-stu-id="fec21-144">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                                  | <span data-ttu-id="fec21-145">Указывает общий тип ячейки.</span><span class="sxs-lookup"><span data-stu-id="fec21-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="fec21-146">\_медиашиткапаЦитивалуе\_</span><span class="sxs-lookup"><span data-stu-id="fec21-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="fec21-147">Целое число</span><span class="sxs-lookup"><span data-stu-id="fec21-147">integer</span></span><br/> | <span data-ttu-id="fec21-148">свойств</span><span class="sxs-lookup"><span data-stu-id="fec21-148">sheets</span></span><br/>     | <span data-ttu-id="fec21-149">Максимальное целочисленное ограничение, разрешенное устройством.</span><span class="sxs-lookup"><span data-stu-id="fec21-149">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="fec21-150">Указывает емкость носителя в количестве страниц (полный уровень) ячейки.</span><span class="sxs-lookup"><span data-stu-id="fec21-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="fec21-151">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="fec21-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="fec21-152">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="fec21-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="fec21-153">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="fec21-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="fec21-154">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="fec21-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fec21-155">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="fec21-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




