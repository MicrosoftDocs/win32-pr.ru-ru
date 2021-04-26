---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 741aa729-35c3-43c2-93d8-e25ed508cfa6
title: пажедевицефонтсубститутион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f40b86d6d81603e2ff9929275571ff6be72d839b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995591"
---
# <a name="pagedevicefontsubstitution"></a><span data-ttu-id="0f5e3-104">пажедевицефонтсубститутион</span><span class="sxs-lookup"><span data-stu-id="0f5e3-104">PageDeviceFontSubstitution</span></span>

<span data-ttu-id="0f5e3-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="0f5e3-105">This topic is not current.</span></span> <span data-ttu-id="0f5e3-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0f5e3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0f5e3-107">Описание состояния включения или выключения подстановки шрифтов устройства.</span><span class="sxs-lookup"><span data-stu-id="0f5e3-107">Describes the enabled/disabled state of device font substitution.</span></span>

-   [<span data-ttu-id="0f5e3-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0f5e3-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0f5e3-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="0f5e3-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0f5e3-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="0f5e3-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0f5e3-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0f5e3-111">Element Information</span></span>



| <span data-ttu-id="0f5e3-112">Имя</span><span class="sxs-lookup"><span data-stu-id="0f5e3-112">Name</span></span> | <span data-ttu-id="0f5e3-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0f5e3-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="0f5e3-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="0f5e3-114">Element Type</span></span> <br/>   | <span data-ttu-id="0f5e3-115">Компонент</span><span class="sxs-lookup"><span data-stu-id="0f5e3-115">Feature</span></span><br/> |
| <span data-ttu-id="0f5e3-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="0f5e3-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0f5e3-117">Страница</span><span class="sxs-lookup"><span data-stu-id="0f5e3-117">Page</span></span><br/>    |
| <span data-ttu-id="0f5e3-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="0f5e3-118">Notes</span></span> <br/>          | <span data-ttu-id="0f5e3-119">Нет</span><span class="sxs-lookup"><span data-stu-id="0f5e3-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="0f5e3-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="0f5e3-120">Structural Content</span></span>

<span data-ttu-id="0f5e3-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="0f5e3-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceFontSubstitution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="0f5e3-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="0f5e3-122">Structure Variables</span></span>

<span data-ttu-id="0f5e3-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="0f5e3-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0f5e3-124">Имя</span><span class="sxs-lookup"><span data-stu-id="0f5e3-124">Name</span></span>                               | <span data-ttu-id="0f5e3-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0f5e3-125">Data type</span></span>         | <span data-ttu-id="0f5e3-126">Unit</span><span class="sxs-lookup"><span data-stu-id="0f5e3-126">Unit</span></span>                  | <span data-ttu-id="0f5e3-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="0f5e3-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0f5e3-128">Сводка</span><span class="sxs-lookup"><span data-stu-id="0f5e3-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0f5e3-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0f5e3-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0f5e3-130">строка</span><span class="sxs-lookup"><span data-stu-id="0f5e3-130">string</span></span><br/> | <span data-ttu-id="0f5e3-131">characters</span><span class="sxs-lookup"><span data-stu-id="0f5e3-131">characters</span></span><br/> | <span data-ttu-id="0f5e3-132">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="0f5e3-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0f5e3-133">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f5e3-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0f5e3-134">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="0f5e3-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="0f5e3-135">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="0f5e3-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0f5e3-136">строка</span><span class="sxs-lookup"><span data-stu-id="0f5e3-136">string</span></span><br/> | <span data-ttu-id="0f5e3-137">Недоступно</span><span class="sxs-lookup"><span data-stu-id="0f5e3-137">n/a</span></span><br/>        | <span data-ttu-id="0f5e3-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="0f5e3-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0f5e3-139">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="0f5e3-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0f5e3-140">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="0f5e3-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0f5e3-141">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="0f5e3-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0f5e3-142">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="0f5e3-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceFontSubstitution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Page device font substitution is off -->
  <psf:Option name="psk:Off" />
  <!--Page device font substitution is on -->
  <psf:Option name="psk:On" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="0f5e3-143">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0f5e3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f5e3-144">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="0f5e3-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




