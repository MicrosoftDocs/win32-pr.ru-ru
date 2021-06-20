---
description: Узнайте, как элемент Документкопиесаллпажес, указывающий количество копий документа.
ms.assetid: 6319e8fc-787f-4bc8-8436-1b498b3882d2
title: документкопиесаллпажес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bf82c23b764f3fe1f8257f4cdb2e7fa03374bd
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409447"
---
# <a name="documentcopiesallpages"></a><span data-ttu-id="cc368-103">документкопиесаллпажес</span><span class="sxs-lookup"><span data-stu-id="cc368-103">DocumentCopiesAllPages</span></span>

<span data-ttu-id="cc368-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="cc368-104">This topic is not current.</span></span> <span data-ttu-id="cc368-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cc368-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cc368-106">Указывает количество копий документа.</span><span class="sxs-lookup"><span data-stu-id="cc368-106">Specifies the number of copies of a document.</span></span>

-   [<span data-ttu-id="cc368-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="cc368-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cc368-108">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="cc368-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="cc368-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="cc368-109">Element Information</span></span>



| <span data-ttu-id="cc368-110">Имя</span><span class="sxs-lookup"><span data-stu-id="cc368-110">Name</span></span> | <span data-ttu-id="cc368-111">Значение</span><span class="sxs-lookup"><span data-stu-id="cc368-111">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="cc368-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="cc368-112">Element Type</span></span> <br/>   | <span data-ttu-id="cc368-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="cc368-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="cc368-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="cc368-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cc368-115">Документ</span><span class="sxs-lookup"><span data-stu-id="cc368-115">Document</span></span><br/>     |
| <span data-ttu-id="cc368-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="cc368-116">Notes</span></span> <br/>          | <span data-ttu-id="cc368-117">Нет</span><span class="sxs-lookup"><span data-stu-id="cc368-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="cc368-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="cc368-118">Structure Content</span></span>

<span data-ttu-id="cc368-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="cc368-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCopiesAllPages">
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

## <a name="structure-properties"></a><span data-ttu-id="cc368-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="cc368-120">Structure Properties</span></span>

<span data-ttu-id="cc368-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="cc368-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cc368-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="cc368-122">Property</span></span>                | <span data-ttu-id="cc368-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="cc368-123">xsi:type</span></span>           | <span data-ttu-id="cc368-124">Значение</span><span class="sxs-lookup"><span data-stu-id="cc368-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="cc368-125">DataType</span><span class="sxs-lookup"><span data-stu-id="cc368-125">DataType</span></span><br/>     | <span data-ttu-id="cc368-126">строка</span><span class="sxs-lookup"><span data-stu-id="cc368-126">string</span></span><br/>  | <span data-ttu-id="cc368-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cc368-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="cc368-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="cc368-128">DefaultValue</span></span><br/> | <span data-ttu-id="cc368-129">целое число</span><span class="sxs-lookup"><span data-stu-id="cc368-129">integer</span></span><br/> | <span data-ttu-id="cc368-130">1</span><span class="sxs-lookup"><span data-stu-id="cc368-130">1</span></span><br/>                 |
| <span data-ttu-id="cc368-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="cc368-131">MaxValue</span></span><br/>     | <span data-ttu-id="cc368-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="cc368-132">integer</span></span><br/> | <span data-ttu-id="cc368-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="cc368-133">undefined</span></span><br/>         |
| <span data-ttu-id="cc368-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="cc368-134">MinValue</span></span><br/>     | <span data-ttu-id="cc368-135">целое число</span><span class="sxs-lookup"><span data-stu-id="cc368-135">integer</span></span><br/> | <span data-ttu-id="cc368-136">1</span><span class="sxs-lookup"><span data-stu-id="cc368-136">1</span></span><br/>                 |
| <span data-ttu-id="cc368-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cc368-137">Mandatory</span></span><br/>    | <span data-ttu-id="cc368-138">строка</span><span class="sxs-lookup"><span data-stu-id="cc368-138">string</span></span><br/>  | <span data-ttu-id="cc368-139">PSK: безусловное</span><span class="sxs-lookup"><span data-stu-id="cc368-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="cc368-140">Несколько</span><span class="sxs-lookup"><span data-stu-id="cc368-140">Multiple</span></span><br/>     | <span data-ttu-id="cc368-141">целое число</span><span class="sxs-lookup"><span data-stu-id="cc368-141">integer</span></span><br/> | <span data-ttu-id="cc368-142">1</span><span class="sxs-lookup"><span data-stu-id="cc368-142">1</span></span><br/>                 |
| <span data-ttu-id="cc368-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="cc368-143">UnitType</span></span><br/>     | <span data-ttu-id="cc368-144">строка</span><span class="sxs-lookup"><span data-stu-id="cc368-144">string</span></span><br/>  | <span data-ttu-id="cc368-145">Копи</span><span class="sxs-lookup"><span data-stu-id="cc368-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="cc368-146">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="cc368-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc368-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="cc368-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




