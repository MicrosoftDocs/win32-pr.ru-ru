---
description: Прочитайте справочные сведения о параметре Пажекопиес. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: пажекопиес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5002850fa1df5a86b0022a941e3b2a1f7e414a44
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396689"
---
# <a name="pagecopies"></a><span data-ttu-id="c7362-105">пажекопиес</span><span class="sxs-lookup"><span data-stu-id="c7362-105">PageCopies</span></span>

<span data-ttu-id="c7362-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="c7362-106">This topic is not current.</span></span> <span data-ttu-id="c7362-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c7362-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c7362-108">Указывает количество копий страницы.</span><span class="sxs-lookup"><span data-stu-id="c7362-108">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="c7362-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c7362-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c7362-110">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="c7362-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c7362-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c7362-111">Element Information</span></span>



| <span data-ttu-id="c7362-112">Имя</span><span class="sxs-lookup"><span data-stu-id="c7362-112">Name</span></span> | <span data-ttu-id="c7362-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c7362-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="c7362-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="c7362-114">Element Type</span></span> <br/>   | <span data-ttu-id="c7362-115">параметердеф</span><span class="sxs-lookup"><span data-stu-id="c7362-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="c7362-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="c7362-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c7362-117">Страница</span><span class="sxs-lookup"><span data-stu-id="c7362-117">Page</span></span><br/>         |
| <span data-ttu-id="c7362-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="c7362-118">Notes</span></span> <br/>          | <span data-ttu-id="c7362-119">Нет</span><span class="sxs-lookup"><span data-stu-id="c7362-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="c7362-120">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="c7362-120">Structure Content</span></span>

<span data-ttu-id="c7362-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="c7362-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageCopies">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="c7362-122">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="c7362-122">Structure Properties</span></span>

<span data-ttu-id="c7362-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="c7362-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c7362-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="c7362-124">Property</span></span>                | <span data-ttu-id="c7362-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c7362-125">xsi:type</span></span>           | <span data-ttu-id="c7362-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c7362-126">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="c7362-127">DataType</span><span class="sxs-lookup"><span data-stu-id="c7362-127">DataType</span></span><br/>     | <span data-ttu-id="c7362-128">строка</span><span class="sxs-lookup"><span data-stu-id="c7362-128">string</span></span><br/>  | <span data-ttu-id="c7362-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="c7362-129">xs:integer</span></span><br/>        |
| <span data-ttu-id="c7362-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c7362-130">DefaultValue</span></span><br/> | <span data-ttu-id="c7362-131">целое число</span><span class="sxs-lookup"><span data-stu-id="c7362-131">integer</span></span><br/> | <span data-ttu-id="c7362-132">1</span><span class="sxs-lookup"><span data-stu-id="c7362-132">1</span></span><br/>                 |
| <span data-ttu-id="c7362-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="c7362-133">MaxValue</span></span><br/>     | <span data-ttu-id="c7362-134">Целое число</span><span class="sxs-lookup"><span data-stu-id="c7362-134">integer</span></span><br/> | <span data-ttu-id="c7362-135">неопределенный</span><span class="sxs-lookup"><span data-stu-id="c7362-135">undefined</span></span><br/>         |
| <span data-ttu-id="c7362-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="c7362-136">MinValue</span></span><br/>     | <span data-ttu-id="c7362-137">целое число</span><span class="sxs-lookup"><span data-stu-id="c7362-137">integer</span></span><br/> | <span data-ttu-id="c7362-138">1</span><span class="sxs-lookup"><span data-stu-id="c7362-138">1</span></span><br/>                 |
| <span data-ttu-id="c7362-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c7362-139">Mandatory</span></span><br/>    | <span data-ttu-id="c7362-140">строка</span><span class="sxs-lookup"><span data-stu-id="c7362-140">string</span></span><br/>  | <span data-ttu-id="c7362-141">PSK: безусловное</span><span class="sxs-lookup"><span data-stu-id="c7362-141">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="c7362-142">Несколько</span><span class="sxs-lookup"><span data-stu-id="c7362-142">Multiple</span></span><br/>     | <span data-ttu-id="c7362-143">целое число</span><span class="sxs-lookup"><span data-stu-id="c7362-143">integer</span></span><br/> | <span data-ttu-id="c7362-144">1</span><span class="sxs-lookup"><span data-stu-id="c7362-144">1</span></span><br/>                 |
| <span data-ttu-id="c7362-145">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="c7362-145">UnitType</span></span><br/>     | <span data-ttu-id="c7362-146">строка</span><span class="sxs-lookup"><span data-stu-id="c7362-146">string</span></span><br/>  | <span data-ttu-id="c7362-147">Копи</span><span class="sxs-lookup"><span data-stu-id="c7362-147">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="c7362-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c7362-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7362-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="c7362-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




