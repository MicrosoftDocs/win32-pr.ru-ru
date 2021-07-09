---
description: Ознакомьтесь с элементом Пажеаутпутбин, настраиваемым пользователем. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: c5050804-0e77-4d26-bf00-5d9690102b18
title: пажеаутпутбин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a9963bf2ca7a2dd60be37c797a27c6ff09b1206
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549002"
---
# <a name="pageoutputbin"></a><span data-ttu-id="dae8f-105">пажеаутпутбин</span><span class="sxs-lookup"><span data-stu-id="dae8f-105">PageOutputBin</span></span>

<span data-ttu-id="dae8f-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="dae8f-106">This topic is not current.</span></span> <span data-ttu-id="dae8f-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dae8f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dae8f-108">Содержит полный список поддерживаемых ячеек для устройства.</span><span class="sxs-lookup"><span data-stu-id="dae8f-108">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="dae8f-109">Разрешает указание выходного лотка на уровне страницы.</span><span class="sxs-lookup"><span data-stu-id="dae8f-109">Allows specification of output bin on a per page basis.</span></span> <span data-ttu-id="dae8f-110">Ключевые слова Жобаутпутбин, Документаутпутбин и Пажеаутпутбин являются взаимоисключающими только один из них должен быть указан в документе PrintTicket или возможности печати.</span><span class="sxs-lookup"><span data-stu-id="dae8f-110">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="dae8f-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="dae8f-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dae8f-112">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="dae8f-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="dae8f-113">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="dae8f-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="dae8f-114">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="dae8f-114">Element Information</span></span>



| <span data-ttu-id="dae8f-115">Имя</span><span class="sxs-lookup"><span data-stu-id="dae8f-115">Name</span></span> | <span data-ttu-id="dae8f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="dae8f-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="dae8f-117">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="dae8f-117">Element Type</span></span> <br/>   | <span data-ttu-id="dae8f-118">Компонент</span><span class="sxs-lookup"><span data-stu-id="dae8f-118">Feature</span></span><br/> |
| <span data-ttu-id="dae8f-119">Префикс области</span><span class="sxs-lookup"><span data-stu-id="dae8f-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dae8f-120">Страница</span><span class="sxs-lookup"><span data-stu-id="dae8f-120">Page</span></span><br/>    |
| <span data-ttu-id="dae8f-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="dae8f-121">Notes</span></span> <br/>          | <span data-ttu-id="dae8f-122">Нет</span><span class="sxs-lookup"><span data-stu-id="dae8f-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="dae8f-123">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="dae8f-123">Structural Content</span></span>

<span data-ttu-id="dae8f-124">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="dae8f-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="dae8f-125">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="dae8f-125">Structure Variables</span></span>

<span data-ttu-id="dae8f-126">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="dae8f-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dae8f-127">Имя</span><span class="sxs-lookup"><span data-stu-id="dae8f-127">Name</span></span>                                   | <span data-ttu-id="dae8f-128">Тип данных</span><span class="sxs-lookup"><span data-stu-id="dae8f-128">Data type</span></span>          | <span data-ttu-id="dae8f-129">Unit</span><span class="sxs-lookup"><span data-stu-id="dae8f-129">Unit</span></span>                  | <span data-ttu-id="dae8f-130">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="dae8f-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="dae8f-131">Итоги</span><span class="sxs-lookup"><span data-stu-id="dae8f-131">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dae8f-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="dae8f-132">\_OptionName\_</span></span><br/>              | <span data-ttu-id="dae8f-133">строка</span><span class="sxs-lookup"><span data-stu-id="dae8f-133">string</span></span><br/>  | <span data-ttu-id="dae8f-134">characters</span><span class="sxs-lookup"><span data-stu-id="dae8f-134">characters</span></span><br/> | <span data-ttu-id="dae8f-135">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="dae8f-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="dae8f-136">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dae8f-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="dae8f-137">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="dae8f-137">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="dae8f-138">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="dae8f-138">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="dae8f-139">строка</span><span class="sxs-lookup"><span data-stu-id="dae8f-139">string</span></span><br/>  | <span data-ttu-id="dae8f-140">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dae8f-140">n/a</span></span><br/>        | <span data-ttu-id="dae8f-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="dae8f-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="dae8f-142">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="dae8f-142">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="dae8f-143">\_бинтипевалуе\_</span><span class="sxs-lookup"><span data-stu-id="dae8f-143">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="dae8f-144">строка</span><span class="sxs-lookup"><span data-stu-id="dae8f-144">string</span></span><br/>  | <span data-ttu-id="dae8f-145">Н/Д</span><span class="sxs-lookup"><span data-stu-id="dae8f-145">n/a</span></span><br/>        | <span data-ttu-id="dae8f-146">Фацедовнтрай, Фацеуптрай, MailBox, сортировщик, укладчик, финишер нет.</span><span class="sxs-lookup"><span data-stu-id="dae8f-146">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span></span><br/>                                                                                                         | <span data-ttu-id="dae8f-147">Указывает общий тип ячейки.</span><span class="sxs-lookup"><span data-stu-id="dae8f-147">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="dae8f-148">\_медиашиткапаЦитивалуе\_</span><span class="sxs-lookup"><span data-stu-id="dae8f-148">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="dae8f-149">Целое число</span><span class="sxs-lookup"><span data-stu-id="dae8f-149">integer</span></span><br/> | <span data-ttu-id="dae8f-150">свойств</span><span class="sxs-lookup"><span data-stu-id="dae8f-150">sheets</span></span><br/>     | <span data-ttu-id="dae8f-151">Больше 0.</span><span class="sxs-lookup"><span data-stu-id="dae8f-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="dae8f-152">Указывает емкость носителя в количестве страниц (полный уровень) ячейки.</span><span class="sxs-lookup"><span data-stu-id="dae8f-152">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="dae8f-153">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="dae8f-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="dae8f-154">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="dae8f-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="dae8f-155">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="dae8f-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputBin">
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

## <a name="related-topics"></a><span data-ttu-id="dae8f-156">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="dae8f-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dae8f-157">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="dae8f-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




