---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: жобдуплексаллдокументсконтигуаусли
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c14e9c536d0ab24fafe308a8b11fa769842aab
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105703538"
---
# <a name="jobduplexalldocumentscontiguously"></a><span data-ttu-id="7b37a-104">жобдуплексаллдокументсконтигуаусли</span><span class="sxs-lookup"><span data-stu-id="7b37a-104">JobDuplexAllDocumentsContiguously</span></span>

<span data-ttu-id="7b37a-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="7b37a-105">This topic is not current.</span></span> <span data-ttu-id="7b37a-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7b37a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7b37a-107">Описывает дуплексные характеристики выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7b37a-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="7b37a-108">Дуплексная функция позволяет печатать на обеих сторонах носителя.</span><span class="sxs-lookup"><span data-stu-id="7b37a-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="7b37a-109">Все документы в задании объединяются последовательно.</span><span class="sxs-lookup"><span data-stu-id="7b37a-109">All Documents in the job are duplexed together contiguously.</span></span> <span data-ttu-id="7b37a-110">Жобдуплексаллдокументсконтигуаусли и Документдуплекс являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="7b37a-110">JobDuplexAllDocumentsContiguously and DocumentDuplex are mutually exclusive.</span></span> <span data-ttu-id="7b37a-111">Драйвер определяет обработку ограничений между этими ключевыми словами.</span><span class="sxs-lookup"><span data-stu-id="7b37a-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="7b37a-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7b37a-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7b37a-113">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="7b37a-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7b37a-114">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="7b37a-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7b37a-115">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7b37a-115">Element Information</span></span>



| <span data-ttu-id="7b37a-116">Имя</span><span class="sxs-lookup"><span data-stu-id="7b37a-116">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="7b37a-117">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="7b37a-117">Element Type</span></span> <br/>   | <span data-ttu-id="7b37a-118">Функция</span><span class="sxs-lookup"><span data-stu-id="7b37a-118">Feature</span></span><br/> |
| <span data-ttu-id="7b37a-119">Префикс области</span><span class="sxs-lookup"><span data-stu-id="7b37a-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7b37a-120">Задание</span><span class="sxs-lookup"><span data-stu-id="7b37a-120">Job</span></span><br/>     |
| <span data-ttu-id="7b37a-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="7b37a-121">Notes</span></span> <br/>          | <span data-ttu-id="7b37a-122">Нет</span><span class="sxs-lookup"><span data-stu-id="7b37a-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="7b37a-123">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="7b37a-123">Structural Content</span></span>

<span data-ttu-id="7b37a-124">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="7b37a-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="7b37a-125">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="7b37a-125">Structure Variables</span></span>

<span data-ttu-id="7b37a-126">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="7b37a-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7b37a-127">Имя</span><span class="sxs-lookup"><span data-stu-id="7b37a-127">Name</span></span>                               | <span data-ttu-id="7b37a-128">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7b37a-128">Data type</span></span>         | <span data-ttu-id="7b37a-129">Unit</span><span class="sxs-lookup"><span data-stu-id="7b37a-129">Unit</span></span>                  | <span data-ttu-id="7b37a-130">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="7b37a-130">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="7b37a-131">Сводка</span><span class="sxs-lookup"><span data-stu-id="7b37a-131">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b37a-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="7b37a-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7b37a-133">строка</span><span class="sxs-lookup"><span data-stu-id="7b37a-133">string</span></span><br/> | <span data-ttu-id="7b37a-134">characters</span><span class="sxs-lookup"><span data-stu-id="7b37a-134">characters</span></span><br/> | <span data-ttu-id="7b37a-135">Допустимое полное имя, как определено в https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="7b37a-135">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="7b37a-136">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7b37a-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7b37a-137">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="7b37a-137">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="7b37a-138">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="7b37a-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7b37a-139">строка</span><span class="sxs-lookup"><span data-stu-id="7b37a-139">string</span></span><br/> | <span data-ttu-id="7b37a-140">Недоступно</span><span class="sxs-lookup"><span data-stu-id="7b37a-140">n/a</span></span><br/>        | <span data-ttu-id="7b37a-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="7b37a-141">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="7b37a-142">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="7b37a-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="7b37a-143">\_дуплексмодевалуе\_</span><span class="sxs-lookup"><span data-stu-id="7b37a-143">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="7b37a-144">строка</span><span class="sxs-lookup"><span data-stu-id="7b37a-144">string</span></span><br/> | <span data-ttu-id="7b37a-145">Недоступно</span><span class="sxs-lookup"><span data-stu-id="7b37a-145">n/a</span></span><br/>        | <span data-ttu-id="7b37a-146">Автоматически, вручную.</span><span class="sxs-lookup"><span data-stu-id="7b37a-146">Automatic, Manual.</span></span><br/>                                                                                                                                                | <span data-ttu-id="7b37a-147">Определяет режим дуплекса.</span><span class="sxs-lookup"><span data-stu-id="7b37a-147">Defines the duplex mode.</span></span> <span data-ttu-id="7b37a-148">Автоматический дуплекс выполняется оборудованием.</span><span class="sxs-lookup"><span data-stu-id="7b37a-148">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="7b37a-149">Ручная двусторонняя печать выполняется программным обеспечением и пользователем.</span><span class="sxs-lookup"><span data-stu-id="7b37a-149">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7b37a-150">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="7b37a-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7b37a-151">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="7b37a-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7b37a-152">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="7b37a-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="7b37a-153">См. также</span><span class="sxs-lookup"><span data-stu-id="7b37a-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b37a-154">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="7b37a-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




