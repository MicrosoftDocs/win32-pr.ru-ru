---
description: Сведения об элементе Жобаутпутбин, который описывает установленный выходной лоток на устройстве или полный список поддерживаемых ячеек для устройства.
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: жобаутпутбин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1243e9409f781b8babde6d6310ce7a2b083f8703
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408857"
---
# <a name="joboutputbin"></a><span data-ttu-id="19c36-103">жобаутпутбин</span><span class="sxs-lookup"><span data-stu-id="19c36-103">JobOutputBin</span></span>

<span data-ttu-id="19c36-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="19c36-104">This topic is not current.</span></span> <span data-ttu-id="19c36-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="19c36-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="19c36-106">Описывает установленный выходной лоток на устройстве или полный список поддерживаемых ячеек для устройства.</span><span class="sxs-lookup"><span data-stu-id="19c36-106">Describes the installed output bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="19c36-107">Ключевые слова Жобаутпутбин, Документаутпутбин и Пажеаутпутбин являются взаимоисключающими только один из них должен быть указан в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="19c36-107">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="19c36-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="19c36-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="19c36-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="19c36-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="19c36-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="19c36-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="19c36-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="19c36-111">Element Information</span></span>



| <span data-ttu-id="19c36-112">Имя</span><span class="sxs-lookup"><span data-stu-id="19c36-112">Name</span></span> | <span data-ttu-id="19c36-113">Значение</span><span class="sxs-lookup"><span data-stu-id="19c36-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="19c36-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="19c36-114">Element Type</span></span> <br/>   | <span data-ttu-id="19c36-115">Компонент</span><span class="sxs-lookup"><span data-stu-id="19c36-115">Feature</span></span><br/> |
| <span data-ttu-id="19c36-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="19c36-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="19c36-117">Задание</span><span class="sxs-lookup"><span data-stu-id="19c36-117">Job</span></span><br/>     |
| <span data-ttu-id="19c36-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="19c36-118">Notes</span></span> <br/>          | <span data-ttu-id="19c36-119">Нет</span><span class="sxs-lookup"><span data-stu-id="19c36-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="19c36-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="19c36-120">Structural Content</span></span>

<span data-ttu-id="19c36-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="19c36-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="19c36-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="19c36-122">Structure Variables</span></span>

<span data-ttu-id="19c36-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="19c36-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="19c36-124">Имя</span><span class="sxs-lookup"><span data-stu-id="19c36-124">Name</span></span>                                   | <span data-ttu-id="19c36-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="19c36-125">Data type</span></span>          | <span data-ttu-id="19c36-126">Unit</span><span class="sxs-lookup"><span data-stu-id="19c36-126">Unit</span></span>                  | <span data-ttu-id="19c36-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="19c36-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="19c36-128">Итоги</span><span class="sxs-lookup"><span data-stu-id="19c36-128">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="19c36-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="19c36-129">\_OptionName\_</span></span><br/>              | <span data-ttu-id="19c36-130">строка</span><span class="sxs-lookup"><span data-stu-id="19c36-130">string</span></span><br/>  | <span data-ttu-id="19c36-131">characters</span><span class="sxs-lookup"><span data-stu-id="19c36-131">characters</span></span><br/> | <span data-ttu-id="19c36-132">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="19c36-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="19c36-133">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19c36-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="19c36-134">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="19c36-134">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="19c36-135">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="19c36-135">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="19c36-136">строка</span><span class="sxs-lookup"><span data-stu-id="19c36-136">string</span></span><br/>  | <span data-ttu-id="19c36-137">Недоступно</span><span class="sxs-lookup"><span data-stu-id="19c36-137">n/a</span></span><br/>        | <span data-ttu-id="19c36-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="19c36-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="19c36-139">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="19c36-139">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="19c36-140">\_бинтипевалуе\_</span><span class="sxs-lookup"><span data-stu-id="19c36-140">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="19c36-141">строка</span><span class="sxs-lookup"><span data-stu-id="19c36-141">string</span></span><br/>  | <span data-ttu-id="19c36-142">Недоступно</span><span class="sxs-lookup"><span data-stu-id="19c36-142">n/a</span></span><br/>        | <span data-ttu-id="19c36-143">Почтовый ящик, сортировщик, укладчик, финишер, нет.</span><span class="sxs-lookup"><span data-stu-id="19c36-143">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                                  | <span data-ttu-id="19c36-144">Указывает общий тип ячейки.</span><span class="sxs-lookup"><span data-stu-id="19c36-144">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="19c36-145">\_медиашиткапаЦитивалуе\_</span><span class="sxs-lookup"><span data-stu-id="19c36-145">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="19c36-146">Целое число</span><span class="sxs-lookup"><span data-stu-id="19c36-146">integer</span></span><br/> | <span data-ttu-id="19c36-147">свойств</span><span class="sxs-lookup"><span data-stu-id="19c36-147">sheets</span></span><br/>     | <span data-ttu-id="19c36-148">Максимальное целочисленное ограничение, разрешенное устройством.</span><span class="sxs-lookup"><span data-stu-id="19c36-148">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="19c36-149">Указывает емкость носителя в количестве страниц (полный уровень) ячейки.</span><span class="sxs-lookup"><span data-stu-id="19c36-149">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="19c36-150">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="19c36-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="19c36-151">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="19c36-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="19c36-152">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="19c36-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="19c36-153">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="19c36-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19c36-154">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="19c36-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




