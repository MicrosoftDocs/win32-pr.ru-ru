---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: пажекопиес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6feef0745e3f9a86b3697b7e0ab65111fc3dfcb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104273329"
---
# <a name="pagecopies"></a><span data-ttu-id="d6d92-104">пажекопиес</span><span class="sxs-lookup"><span data-stu-id="d6d92-104">PageCopies</span></span>

<span data-ttu-id="d6d92-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="d6d92-105">This topic is not current.</span></span> <span data-ttu-id="d6d92-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d6d92-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d6d92-107">Указывает количество копий страницы.</span><span class="sxs-lookup"><span data-stu-id="d6d92-107">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="d6d92-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d6d92-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d6d92-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="d6d92-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d6d92-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d6d92-110">Element Information</span></span>



| <span data-ttu-id="d6d92-111">Имя</span><span class="sxs-lookup"><span data-stu-id="d6d92-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="d6d92-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="d6d92-112">Element Type</span></span> <br/>   | <span data-ttu-id="d6d92-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="d6d92-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="d6d92-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="d6d92-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d6d92-115">Страница</span><span class="sxs-lookup"><span data-stu-id="d6d92-115">Page</span></span><br/>         |
| <span data-ttu-id="d6d92-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="d6d92-116">Notes</span></span> <br/>          | <span data-ttu-id="d6d92-117">Нет</span><span class="sxs-lookup"><span data-stu-id="d6d92-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="d6d92-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="d6d92-118">Structure Content</span></span>

<span data-ttu-id="d6d92-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="d6d92-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="d6d92-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="d6d92-120">Structure Properties</span></span>

<span data-ttu-id="d6d92-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="d6d92-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d6d92-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="d6d92-122">Property</span></span>                | <span data-ttu-id="d6d92-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d6d92-123">xsi:type</span></span>           | <span data-ttu-id="d6d92-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d6d92-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="d6d92-125">DataType</span><span class="sxs-lookup"><span data-stu-id="d6d92-125">DataType</span></span><br/>     | <span data-ttu-id="d6d92-126">строка</span><span class="sxs-lookup"><span data-stu-id="d6d92-126">string</span></span><br/>  | <span data-ttu-id="d6d92-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d6d92-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="d6d92-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d6d92-128">DefaultValue</span></span><br/> | <span data-ttu-id="d6d92-129">целое число</span><span class="sxs-lookup"><span data-stu-id="d6d92-129">integer</span></span><br/> | <span data-ttu-id="d6d92-130">1</span><span class="sxs-lookup"><span data-stu-id="d6d92-130">1</span></span><br/>                 |
| <span data-ttu-id="d6d92-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="d6d92-131">MaxValue</span></span><br/>     | <span data-ttu-id="d6d92-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="d6d92-132">integer</span></span><br/> | <span data-ttu-id="d6d92-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="d6d92-133">undefined</span></span><br/>         |
| <span data-ttu-id="d6d92-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="d6d92-134">MinValue</span></span><br/>     | <span data-ttu-id="d6d92-135">целое число</span><span class="sxs-lookup"><span data-stu-id="d6d92-135">integer</span></span><br/> | <span data-ttu-id="d6d92-136">1</span><span class="sxs-lookup"><span data-stu-id="d6d92-136">1</span></span><br/>                 |
| <span data-ttu-id="d6d92-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d6d92-137">Mandatory</span></span><br/>    | <span data-ttu-id="d6d92-138">строка</span><span class="sxs-lookup"><span data-stu-id="d6d92-138">string</span></span><br/>  | <span data-ttu-id="d6d92-139">PSK: безусловное</span><span class="sxs-lookup"><span data-stu-id="d6d92-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="d6d92-140">Несколько</span><span class="sxs-lookup"><span data-stu-id="d6d92-140">Multiple</span></span><br/>     | <span data-ttu-id="d6d92-141">целое число</span><span class="sxs-lookup"><span data-stu-id="d6d92-141">integer</span></span><br/> | <span data-ttu-id="d6d92-142">1</span><span class="sxs-lookup"><span data-stu-id="d6d92-142">1</span></span><br/>                 |
| <span data-ttu-id="d6d92-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="d6d92-143">UnitType</span></span><br/>     | <span data-ttu-id="d6d92-144">строка</span><span class="sxs-lookup"><span data-stu-id="d6d92-144">string</span></span><br/>  | <span data-ttu-id="d6d92-145">Копи</span><span class="sxs-lookup"><span data-stu-id="d6d92-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="d6d92-146">См. также</span><span class="sxs-lookup"><span data-stu-id="d6d92-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6d92-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="d6d92-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




