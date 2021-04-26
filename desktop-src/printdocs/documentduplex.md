---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: dadc52e8-1733-4267-85aa-33d0ddd3dfa2
title: документдуплекс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959bbddbfa06e47fe2bc744af3ead0a72b13af7b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998421"
---
# <a name="documentduplex"></a><span data-ttu-id="10183-104">документдуплекс</span><span class="sxs-lookup"><span data-stu-id="10183-104">DocumentDuplex</span></span>

<span data-ttu-id="10183-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="10183-105">This topic is not current.</span></span> <span data-ttu-id="10183-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="10183-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="10183-107">Описывает дуплексные характеристики выходных данных.</span><span class="sxs-lookup"><span data-stu-id="10183-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="10183-108">Дуплексная функция позволяет печатать на обеих сторонах носителя.</span><span class="sxs-lookup"><span data-stu-id="10183-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="10183-109">Каждый документ расдуплексен отдельно.</span><span class="sxs-lookup"><span data-stu-id="10183-109">Each document is duplexed separately.</span></span> <span data-ttu-id="10183-110">Документдуплекс и Жобдуплексаллдокументсконтигуаусли являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="10183-110">DocumentDuplex and JobDuplexAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="10183-111">Драйвер определяет обработку ограничений между этими ключевыми словами.</span><span class="sxs-lookup"><span data-stu-id="10183-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="10183-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="10183-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="10183-113">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="10183-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="10183-114">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="10183-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="10183-115">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="10183-115">Element Information</span></span>



| <span data-ttu-id="10183-116">Имя</span><span class="sxs-lookup"><span data-stu-id="10183-116">Name</span></span> | <span data-ttu-id="10183-117">Значение</span><span class="sxs-lookup"><span data-stu-id="10183-117">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="10183-118">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="10183-118">Element Type</span></span> <br/>   | <span data-ttu-id="10183-119">Компонент</span><span class="sxs-lookup"><span data-stu-id="10183-119">Feature</span></span><br/>  |
| <span data-ttu-id="10183-120">Префикс области</span><span class="sxs-lookup"><span data-stu-id="10183-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="10183-121">Документ</span><span class="sxs-lookup"><span data-stu-id="10183-121">Document</span></span><br/> |
| <span data-ttu-id="10183-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="10183-122">Notes</span></span> <br/>          | <span data-ttu-id="10183-123">Нет</span><span class="sxs-lookup"><span data-stu-id="10183-123">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="10183-124">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="10183-124">Structural Content</span></span>

<span data-ttu-id="10183-125">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="10183-125">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="10183-126">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="10183-126">Structure Variables</span></span>

<span data-ttu-id="10183-127">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="10183-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="10183-128">Имя</span><span class="sxs-lookup"><span data-stu-id="10183-128">Name</span></span>                               | <span data-ttu-id="10183-129">Тип данных</span><span class="sxs-lookup"><span data-stu-id="10183-129">Data type</span></span>         | <span data-ttu-id="10183-130">Unit</span><span class="sxs-lookup"><span data-stu-id="10183-130">Unit</span></span>                  | <span data-ttu-id="10183-131">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="10183-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="10183-132">Сводка</span><span class="sxs-lookup"><span data-stu-id="10183-132">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10183-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="10183-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="10183-134">строка</span><span class="sxs-lookup"><span data-stu-id="10183-134">string</span></span><br/> | <span data-ttu-id="10183-135">characters</span><span class="sxs-lookup"><span data-stu-id="10183-135">characters</span></span><br/> | <span data-ttu-id="10183-136">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="10183-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="10183-137">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="10183-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="10183-138">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="10183-138">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="10183-139">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="10183-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="10183-140">строка</span><span class="sxs-lookup"><span data-stu-id="10183-140">string</span></span><br/> | <span data-ttu-id="10183-141">Недоступно</span><span class="sxs-lookup"><span data-stu-id="10183-141">n/a</span></span><br/>        | <span data-ttu-id="10183-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="10183-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="10183-143">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="10183-143">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="10183-144">\_дуплексмодевалуе\_</span><span class="sxs-lookup"><span data-stu-id="10183-144">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="10183-145">строка</span><span class="sxs-lookup"><span data-stu-id="10183-145">string</span></span><br/> | <span data-ttu-id="10183-146">Недоступно</span><span class="sxs-lookup"><span data-stu-id="10183-146">n/a</span></span><br/>        | <span data-ttu-id="10183-147">Автоматически, вручную.</span><span class="sxs-lookup"><span data-stu-id="10183-147">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="10183-148">Определяет режим дуплекса.</span><span class="sxs-lookup"><span data-stu-id="10183-148">Defines the duplex mode.</span></span> <span data-ttu-id="10183-149">Автоматический дуплекс выполняется оборудованием.</span><span class="sxs-lookup"><span data-stu-id="10183-149">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="10183-150">Ручная двусторонняя печать выполняется программным обеспечением и пользователем.</span><span class="sxs-lookup"><span data-stu-id="10183-150">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="10183-151">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="10183-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="10183-152">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="10183-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="10183-153">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="10183-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="10183-154">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="10183-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10183-155">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="10183-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




