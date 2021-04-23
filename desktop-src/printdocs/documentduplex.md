---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: dadc52e8-1733-4267-85aa-33d0ddd3dfa2
title: документдуплекс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2d65ac1007b8413f9e5e6cc12802e0ac27dac3
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104273367"
---
# <a name="documentduplex"></a><span data-ttu-id="7031e-104">документдуплекс</span><span class="sxs-lookup"><span data-stu-id="7031e-104">DocumentDuplex</span></span>

<span data-ttu-id="7031e-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="7031e-105">This topic is not current.</span></span> <span data-ttu-id="7031e-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7031e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7031e-107">Описывает дуплексные характеристики выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7031e-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="7031e-108">Дуплексная функция позволяет печатать на обеих сторонах носителя.</span><span class="sxs-lookup"><span data-stu-id="7031e-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="7031e-109">Каждый документ расдуплексен отдельно.</span><span class="sxs-lookup"><span data-stu-id="7031e-109">Each document is duplexed separately.</span></span> <span data-ttu-id="7031e-110">Документдуплекс и Жобдуплексаллдокументсконтигуаусли являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="7031e-110">DocumentDuplex and JobDuplexAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="7031e-111">Драйвер определяет обработку ограничений между этими ключевыми словами.</span><span class="sxs-lookup"><span data-stu-id="7031e-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="7031e-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7031e-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7031e-113">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="7031e-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7031e-114">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="7031e-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7031e-115">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7031e-115">Element Information</span></span>



| <span data-ttu-id="7031e-116">Имя</span><span class="sxs-lookup"><span data-stu-id="7031e-116">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="7031e-117">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="7031e-117">Element Type</span></span> <br/>   | <span data-ttu-id="7031e-118">Функция</span><span class="sxs-lookup"><span data-stu-id="7031e-118">Feature</span></span><br/>  |
| <span data-ttu-id="7031e-119">Префикс области</span><span class="sxs-lookup"><span data-stu-id="7031e-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7031e-120">Документ</span><span class="sxs-lookup"><span data-stu-id="7031e-120">Document</span></span><br/> |
| <span data-ttu-id="7031e-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="7031e-121">Notes</span></span> <br/>          | <span data-ttu-id="7031e-122">Нет</span><span class="sxs-lookup"><span data-stu-id="7031e-122">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="7031e-123">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="7031e-123">Structural Content</span></span>

<span data-ttu-id="7031e-124">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7031e-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentDuplex">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_DuplexModeValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="7031e-125">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="7031e-125">Structure Variables</span></span>

<span data-ttu-id="7031e-126">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="7031e-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7031e-127">Имя</span><span class="sxs-lookup"><span data-stu-id="7031e-127">Name</span></span>                               | <span data-ttu-id="7031e-128">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7031e-128">Data type</span></span>         | <span data-ttu-id="7031e-129">Unit</span><span class="sxs-lookup"><span data-stu-id="7031e-129">Unit</span></span>                  | <span data-ttu-id="7031e-130">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="7031e-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7031e-131">Сводка</span><span class="sxs-lookup"><span data-stu-id="7031e-131">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7031e-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="7031e-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7031e-133">строка</span><span class="sxs-lookup"><span data-stu-id="7031e-133">string</span></span><br/> | <span data-ttu-id="7031e-134">characters</span><span class="sxs-lookup"><span data-stu-id="7031e-134">characters</span></span><br/> | <span data-ttu-id="7031e-135">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="7031e-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7031e-136">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7031e-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7031e-137">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="7031e-137">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="7031e-138">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="7031e-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7031e-139">строка</span><span class="sxs-lookup"><span data-stu-id="7031e-139">string</span></span><br/> | <span data-ttu-id="7031e-140">Недоступно</span><span class="sxs-lookup"><span data-stu-id="7031e-140">n/a</span></span><br/>        | <span data-ttu-id="7031e-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="7031e-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7031e-142">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="7031e-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="7031e-143">\_дуплексмодевалуе\_</span><span class="sxs-lookup"><span data-stu-id="7031e-143">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="7031e-144">строка</span><span class="sxs-lookup"><span data-stu-id="7031e-144">string</span></span><br/> | <span data-ttu-id="7031e-145">Недоступно</span><span class="sxs-lookup"><span data-stu-id="7031e-145">n/a</span></span><br/>        | <span data-ttu-id="7031e-146">Автоматически, вручную.</span><span class="sxs-lookup"><span data-stu-id="7031e-146">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="7031e-147">Определяет режим дуплекса.</span><span class="sxs-lookup"><span data-stu-id="7031e-147">Defines the duplex mode.</span></span> <span data-ttu-id="7031e-148">Автоматический дуплекс выполняется оборудованием.</span><span class="sxs-lookup"><span data-stu-id="7031e-148">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="7031e-149">Ручная двусторонняя печать выполняется программным обеспечением и пользователем.</span><span class="sxs-lookup"><span data-stu-id="7031e-149">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7031e-150">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="7031e-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7031e-151">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="7031e-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7031e-152">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="7031e-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentDuplex">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies one sided printing. -->
  <psf:Option name="psk:OneSided" />
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:TwoSidedShortEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:TwoSidedLongEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="7031e-153">См. также</span><span class="sxs-lookup"><span data-stu-id="7031e-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7031e-154">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="7031e-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




