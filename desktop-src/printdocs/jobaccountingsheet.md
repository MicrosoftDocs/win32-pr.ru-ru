---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: fd16bd46-32e3-4896-ac5c-03c1bf6ad515
title: жобаккаунтингшит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ffb70ba0ac1a78eefc1024d8e93dc642439aed
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998431"
---
# <a name="jobaccountingsheet"></a><span data-ttu-id="66b7a-104">жобаккаунтингшит</span><span class="sxs-lookup"><span data-stu-id="66b7a-104">JobAccountingSheet</span></span>

<span data-ttu-id="66b7a-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="66b7a-105">This topic is not current.</span></span> <span data-ttu-id="66b7a-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="66b7a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="66b7a-107">Описывает лист учета, который будет выводиться для задания.</span><span class="sxs-lookup"><span data-stu-id="66b7a-107">Describes the accounting sheet to be output for the job.</span></span> <span data-ttu-id="66b7a-108">Лист учета должен быть выведен на экран по умолчанию Пажемедиасизе и использовать Пажемедиатипе по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="66b7a-108">The accounting sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="66b7a-109">Лист учета должен быть изолирован от оставшейся части задания.</span><span class="sxs-lookup"><span data-stu-id="66b7a-109">The accounting sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="66b7a-110">Это означает, что любые параметры завершения или обработки (например, Жобдуплекс, Жобстапле или Жоббиндинг) не должны включать таблицу учета.</span><span class="sxs-lookup"><span data-stu-id="66b7a-110">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the accounting sheet.</span></span> <span data-ttu-id="66b7a-111">Лист учета может быть первой или последней страницей задания на усмотрение разработчика.</span><span class="sxs-lookup"><span data-stu-id="66b7a-111">The accounting sheet may occur as the first or last page of the job at the implementer's discretion.</span></span>

-   [<span data-ttu-id="66b7a-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="66b7a-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="66b7a-113">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="66b7a-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="66b7a-114">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="66b7a-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="66b7a-115">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="66b7a-115">Element Information</span></span>



| <span data-ttu-id="66b7a-116">Имя</span><span class="sxs-lookup"><span data-stu-id="66b7a-116">Name</span></span> | <span data-ttu-id="66b7a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="66b7a-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="66b7a-118">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="66b7a-118">Element Type</span></span> <br/>   | <span data-ttu-id="66b7a-119">Компонент</span><span class="sxs-lookup"><span data-stu-id="66b7a-119">Feature</span></span><br/> |
| <span data-ttu-id="66b7a-120">Префикс области</span><span class="sxs-lookup"><span data-stu-id="66b7a-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="66b7a-121">Задание</span><span class="sxs-lookup"><span data-stu-id="66b7a-121">Job</span></span><br/>     |
| <span data-ttu-id="66b7a-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="66b7a-122">Notes</span></span> <br/>          | <span data-ttu-id="66b7a-123">Нет</span><span class="sxs-lookup"><span data-stu-id="66b7a-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="66b7a-124">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="66b7a-124">Structural Content</span></span>

<span data-ttu-id="66b7a-125">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="66b7a-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobAccountingSheet">
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

## <a name="structure-variables"></a><span data-ttu-id="66b7a-126">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="66b7a-126">Structure Variables</span></span>

<span data-ttu-id="66b7a-127">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="66b7a-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="66b7a-128">Имя</span><span class="sxs-lookup"><span data-stu-id="66b7a-128">Name</span></span>                               | <span data-ttu-id="66b7a-129">Тип данных</span><span class="sxs-lookup"><span data-stu-id="66b7a-129">Data type</span></span>         | <span data-ttu-id="66b7a-130">Unit</span><span class="sxs-lookup"><span data-stu-id="66b7a-130">Unit</span></span>                  | <span data-ttu-id="66b7a-131">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="66b7a-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="66b7a-132">Сводка</span><span class="sxs-lookup"><span data-stu-id="66b7a-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="66b7a-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="66b7a-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="66b7a-134">строка</span><span class="sxs-lookup"><span data-stu-id="66b7a-134">string</span></span><br/> | <span data-ttu-id="66b7a-135">characters</span><span class="sxs-lookup"><span data-stu-id="66b7a-135">characters</span></span><br/> | <span data-ttu-id="66b7a-136">Допустимое полное имя, определяемое [пространствами имен в XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="66b7a-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="66b7a-137">Если пространство имен не указано, предполагается использование пространства имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="66b7a-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="66b7a-138">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="66b7a-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="66b7a-139">\_идентитйоптионвалуе\_</span><span class="sxs-lookup"><span data-stu-id="66b7a-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="66b7a-140">строка</span><span class="sxs-lookup"><span data-stu-id="66b7a-140">string</span></span><br/> | <span data-ttu-id="66b7a-141">Недоступно</span><span class="sxs-lookup"><span data-stu-id="66b7a-141">n/a</span></span><br/>        | <span data-ttu-id="66b7a-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="66b7a-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="66b7a-143">Определяет параметр, который при выборе этого параметра отключит эту функцию.</span><span class="sxs-lookup"><span data-stu-id="66b7a-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="66b7a-144">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="66b7a-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="66b7a-145">Ключевые слова общедоступной схемы печати определены в https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="66b7a-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="66b7a-146">Содержимое общедоступного язык XML (XML) для этого ключевого слова определено ниже:</span><span class="sxs-lookup"><span data-stu-id="66b7a-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobAccountingSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no accounting sheet will be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) accounting sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
        
```

## <a name="related-topics"></a><span data-ttu-id="66b7a-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="66b7a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66b7a-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="66b7a-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




