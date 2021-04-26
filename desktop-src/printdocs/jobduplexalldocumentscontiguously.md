---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: жобдуплексаллдокументсконтигуаусли
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e5ae88213af15b53f71e406b4caf791b80f286f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998221"
---
# <a name="jobduplexalldocumentscontiguously"></a><span data-ttu-id="52084-104">жобдуплексаллдокументсконтигуаусли</span><span class="sxs-lookup"><span data-stu-id="52084-104">JobDuplexAllDocumentsContiguously</span></span>

<span data-ttu-id="52084-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="52084-105">This topic is not current.</span></span> <span data-ttu-id="52084-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="52084-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="52084-107">Описывает дуплексные характеристики выходных данных.</span><span class="sxs-lookup"><span data-stu-id="52084-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="52084-108">Дуплексная функция позволяет печатать на обеих сторонах носителя.</span><span class="sxs-lookup"><span data-stu-id="52084-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="52084-109">Все документы в задании объединяются последовательно.</span><span class="sxs-lookup"><span data-stu-id="52084-109">All Documents in the job are duplexed together contiguously.</span></span> <span data-ttu-id="52084-110">Жобдуплексаллдокументсконтигуаусли и Документдуплекс являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="52084-110">JobDuplexAllDocumentsContiguously and DocumentDuplex are mutually exclusive.</span></span> <span data-ttu-id="52084-111">Драйвер определяет обработку ограничений между этими ключевыми словами.</span><span class="sxs-lookup"><span data-stu-id="52084-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="52084-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="52084-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="52084-113">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="52084-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="52084-114">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="52084-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="52084-115">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="52084-115">Element Information</span></span>



| <span data-ttu-id="52084-116">Имя</span><span class="sxs-lookup"><span data-stu-id="52084-116">Name</span></span> | <span data-ttu-id="52084-117">Значение</span><span class="sxs-lookup"><span data-stu-id="52084-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="52084-118">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="52084-118">Element Type</span></span> <br/>   | <span data-ttu-id="52084-119">Компонент</span><span class="sxs-lookup"><span data-stu-id="52084-119">Feature</span></span><br/> |
| <span data-ttu-id="52084-120">Префикс области</span><span class="sxs-lookup"><span data-stu-id="52084-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="52084-121">Задание</span><span class="sxs-lookup"><span data-stu-id="52084-121">Job</span></span><br/>     |
| <span data-ttu-id="52084-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="52084-122">Notes</span></span> <br/>          | <span data-ttu-id="52084-123">Нет</span><span class="sxs-lookup"><span data-stu-id="52084-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="52084-124">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="52084-124">Structural Content</span></span>

<span data-ttu-id="52084-125">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="52084-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
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

## <a name="structure-variables"></a><span data-ttu-id="52084-126">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="52084-126">Structure Variables</span></span>

<span data-ttu-id="52084-127">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="52084-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="52084-128">Имя</span><span class="sxs-lookup"><span data-stu-id="52084-128">Name</span></span>                               | <span data-ttu-id="52084-129">Тип данных</span><span class="sxs-lookup"><span data-stu-id="52084-129">Data type</span></span>         | <span data-ttu-id="52084-130">Unit</span><span class="sxs-lookup"><span data-stu-id="52084-130">Unit</span></span>                  | <span data-ttu-id="52084-131">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="52084-131">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="52084-132">Сводка</span><span class="sxs-lookup"><span data-stu-id="52084-132">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52084-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="52084-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="52084-134">строка</span><span class="sxs-lookup"><span data-stu-id="52084-134">string</span></span><br/> | <span data-ttu-id="52084-135">characters</span><span class="sxs-lookup"><span data-stu-id="52084-135">characters</span></span><br/> | <span data-ttu-id="52084-136">Допустимое полное имя, как определено в https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="52084-136">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="52084-137">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52084-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="52084-138">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="52084-138">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="52084-139">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="52084-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="52084-140">строка</span><span class="sxs-lookup"><span data-stu-id="52084-140">string</span></span><br/> | <span data-ttu-id="52084-141">Недоступно</span><span class="sxs-lookup"><span data-stu-id="52084-141">n/a</span></span><br/>        | <span data-ttu-id="52084-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="52084-142">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="52084-143">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="52084-143">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="52084-144">\_дуплексмодевалуе\_</span><span class="sxs-lookup"><span data-stu-id="52084-144">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="52084-145">строка</span><span class="sxs-lookup"><span data-stu-id="52084-145">string</span></span><br/> | <span data-ttu-id="52084-146">Недоступно</span><span class="sxs-lookup"><span data-stu-id="52084-146">n/a</span></span><br/>        | <span data-ttu-id="52084-147">Автоматически, вручную.</span><span class="sxs-lookup"><span data-stu-id="52084-147">Automatic, Manual.</span></span><br/>                                                                                                                                                | <span data-ttu-id="52084-148">Определяет режим дуплекса.</span><span class="sxs-lookup"><span data-stu-id="52084-148">Defines the duplex mode.</span></span> <span data-ttu-id="52084-149">Автоматический дуплекс выполняется оборудованием.</span><span class="sxs-lookup"><span data-stu-id="52084-149">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="52084-150">Ручная двусторонняя печать выполняется программным обеспечением и пользователем.</span><span class="sxs-lookup"><span data-stu-id="52084-150">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="52084-151">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="52084-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="52084-152">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="52084-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="52084-153">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="52084-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
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

## <a name="related-topics"></a><span data-ttu-id="52084-154">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="52084-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52084-155">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="52084-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




