---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 3894d9fa-2bf7-447a-bac3-e72a0fdb7187
title: жобдевицелангуаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5b128cd8a0bd06cc259d3da0daf834f3c2aebf
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351975"
---
# <a name="jobdevicelanguage"></a><span data-ttu-id="ba9fb-104">жобдевицелангуаже</span><span class="sxs-lookup"><span data-stu-id="ba9fb-104">JobDeviceLanguage</span></span>

<span data-ttu-id="ba9fb-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="ba9fb-105">This topic is not current.</span></span> <span data-ttu-id="ba9fb-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ba9fb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ba9fb-107">Описывает языки устройств, поддерживаемые для отправки данных с драйвера на физическое устройство.</span><span class="sxs-lookup"><span data-stu-id="ba9fb-107">Describes the device languages supported for sending data from driver to physical device.</span></span> <span data-ttu-id="ba9fb-108">Часто это называется «языком описания страниц».</span><span class="sxs-lookup"><span data-stu-id="ba9fb-108">This is often called "Page Description Language".</span></span> <span data-ttu-id="ba9fb-109">Это ключевое слово определяет, какой язык описания страниц поддерживается драйвером и физическим устройством.</span><span class="sxs-lookup"><span data-stu-id="ba9fb-109">This keyword defines what page description language is supported by the driver and physical device.</span></span>

-   [<span data-ttu-id="ba9fb-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ba9fb-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ba9fb-111">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="ba9fb-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ba9fb-112">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ba9fb-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ba9fb-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ba9fb-113">Element Information</span></span>



| <span data-ttu-id="ba9fb-114">Имя</span><span class="sxs-lookup"><span data-stu-id="ba9fb-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="ba9fb-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="ba9fb-115">Element Type</span></span> <br/>   | <span data-ttu-id="ba9fb-116">Функция</span><span class="sxs-lookup"><span data-stu-id="ba9fb-116">Feature</span></span><br/> |
| <span data-ttu-id="ba9fb-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="ba9fb-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ba9fb-118">Задание</span><span class="sxs-lookup"><span data-stu-id="ba9fb-118">Job</span></span><br/>     |
| <span data-ttu-id="ba9fb-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="ba9fb-119">Notes</span></span> <br/>          | <span data-ttu-id="ba9fb-120">Нет</span><span class="sxs-lookup"><span data-stu-id="ba9fb-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ba9fb-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="ba9fb-121">Structural Content</span></span>

<span data-ttu-id="ba9fb-122">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="ba9fb-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_value_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_LanguageEncodingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_LanguageVersionValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="ba9fb-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="ba9fb-123">Structure Variables</span></span>

<span data-ttu-id="ba9fb-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="ba9fb-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ba9fb-125">Имя</span><span class="sxs-lookup"><span data-stu-id="ba9fb-125">Name</span></span>                                 | <span data-ttu-id="ba9fb-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ba9fb-126">Data type</span></span>         | <span data-ttu-id="ba9fb-127">Unit</span><span class="sxs-lookup"><span data-stu-id="ba9fb-127">Unit</span></span>                  | <span data-ttu-id="ba9fb-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="ba9fb-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ba9fb-129">Сводка</span><span class="sxs-lookup"><span data-stu-id="ba9fb-129">Summary</span></span>                                                                      |
|--------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ba9fb-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ba9fb-130">\_OptionName\_</span></span><br/>            | <span data-ttu-id="ba9fb-131">строка</span><span class="sxs-lookup"><span data-stu-id="ba9fb-131">string</span></span><br/> | <span data-ttu-id="ba9fb-132">characters</span><span class="sxs-lookup"><span data-stu-id="ba9fb-132">characters</span></span><br/> | <span data-ttu-id="ba9fb-133">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ba9fb-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ba9fb-134">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ba9fb-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ba9fb-135">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="ba9fb-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ba9fb-136">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="ba9fb-136">\_IdentityOptionValue\_</span></span><br/>   | <span data-ttu-id="ba9fb-137">строка</span><span class="sxs-lookup"><span data-stu-id="ba9fb-137">string</span></span><br/> | <span data-ttu-id="ba9fb-138">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ba9fb-138">n/a</span></span><br/>        | <span data-ttu-id="ba9fb-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="ba9fb-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ba9fb-140">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="ba9fb-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="ba9fb-141">\_лангуажелевелвалуе\_</span><span class="sxs-lookup"><span data-stu-id="ba9fb-141">\_LanguageLevelValue\_</span></span><br/>    | <span data-ttu-id="ba9fb-142">строка</span><span class="sxs-lookup"><span data-stu-id="ba9fb-142">string</span></span><br/> | <span data-ttu-id="ba9fb-143">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ba9fb-143">n/a</span></span><br/>        | <span data-ttu-id="ba9fb-144">Нет.</span><span class="sxs-lookup"><span data-stu-id="ba9fb-144">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="ba9fb-145">Задает языковой уровень (например, уровень PS 2).</span><span class="sxs-lookup"><span data-stu-id="ba9fb-145">Specifies the language level (for example, PS Level 2).</span></span><br/>           |
| <span data-ttu-id="ba9fb-146">\_лангуажеенкодингвалуе\_</span><span class="sxs-lookup"><span data-stu-id="ba9fb-146">\_LanguageEncodingValue\_</span></span><br/> | <span data-ttu-id="ba9fb-147">строка</span><span class="sxs-lookup"><span data-stu-id="ba9fb-147">string</span></span><br/> | <span data-ttu-id="ba9fb-148">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ba9fb-148">n/a</span></span><br/>        | <span data-ttu-id="ba9fb-149">Нет.</span><span class="sxs-lookup"><span data-stu-id="ba9fb-149">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="ba9fb-150">Задает кодировку языка (например, ISOLatin1).</span><span class="sxs-lookup"><span data-stu-id="ba9fb-150">Specifies the language encoding (for example, ISOLatin1).</span></span><br/>         |
| <span data-ttu-id="ba9fb-151">\_лангуажеверсионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="ba9fb-151">\_LanguageVersionValue\_</span></span><br/>  | <span data-ttu-id="ba9fb-152">строка</span><span class="sxs-lookup"><span data-stu-id="ba9fb-152">string</span></span><br/> | <span data-ttu-id="ba9fb-153">Недоступно</span><span class="sxs-lookup"><span data-stu-id="ba9fb-153">n/a</span></span><br/>        | <span data-ttu-id="ba9fb-154">Нет.</span><span class="sxs-lookup"><span data-stu-id="ba9fb-154">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="ba9fb-155">Указывает версию языка.</span><span class="sxs-lookup"><span data-stu-id="ba9fb-155">Specifies the language version.</span></span><br/>                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ba9fb-156">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ba9fb-156">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ba9fb-157">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="ba9fb-157">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ba9fb-158">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="ba9fb-158">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies device language is XPS-->
  <psf:Option name="psk:XPS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specifies device language is PC-PR201 -->
  <psf:Option name="psk:_201PL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ART -->
  <psf:Option name="psk:ART">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ASCII -->
  <psf:Option name="psk:ASCII">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is CaPSL-->
  <psf:Option name="psk:CaPSL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/P2-->
  <psf:Option name="psk:ESCP2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/Page-->
  <psf:Option name="psk:ESCPage">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is HP-GL/2-->
  <psf:Option name="psk:HPGL2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KPDL -->
  <psf:Option name="psk:KPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KS -->
  <psf:Option name="psk:KS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KSSM -->
  <psf:Option name="psk:KSSM">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL -->
  <psf:Option name="psk:PCL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5c -->
  <psf:Option name="psk:PCL5c">
    <psf:ScoredProperty name="LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5e -->
  <psf:Option name="psk:PCL5e">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL-XL -->
  <psf:Option name="psk:PCL-XL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PostScript -->
  <psf:Option name="psk:PostScript">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PPDS -->
  <psf:Option name="psk:PPDS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RPDL -->
  <psf:Option name="psk:RPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RTL -->
  <psf:Option name="psk:RTL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="ba9fb-159">См. также</span><span class="sxs-lookup"><span data-stu-id="ba9fb-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba9fb-160">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="ba9fb-160">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




