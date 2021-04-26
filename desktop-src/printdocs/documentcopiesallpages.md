---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 6319e8fc-787f-4bc8-8436-1b498b3882d2
title: документкопиесаллпажес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723242ddd127113b573f167e6902b27fcca9665a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993991"
---
# <a name="documentcopiesallpages"></a><span data-ttu-id="8456a-104">документкопиесаллпажес</span><span class="sxs-lookup"><span data-stu-id="8456a-104">DocumentCopiesAllPages</span></span>

<span data-ttu-id="8456a-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="8456a-105">This topic is not current.</span></span> <span data-ttu-id="8456a-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8456a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8456a-107">Указывает количество копий документа.</span><span class="sxs-lookup"><span data-stu-id="8456a-107">Specifies the number of copies of a document.</span></span>

-   [<span data-ttu-id="8456a-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8456a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8456a-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="8456a-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8456a-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8456a-110">Element Information</span></span>



| <span data-ttu-id="8456a-111">Имя</span><span class="sxs-lookup"><span data-stu-id="8456a-111">Name</span></span> | <span data-ttu-id="8456a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="8456a-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="8456a-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="8456a-113">Element Type</span></span> <br/>   | <span data-ttu-id="8456a-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="8456a-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="8456a-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="8456a-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8456a-116">Документ</span><span class="sxs-lookup"><span data-stu-id="8456a-116">Document</span></span><br/>     |
| <span data-ttu-id="8456a-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="8456a-117">Notes</span></span> <br/>          | <span data-ttu-id="8456a-118">Нет</span><span class="sxs-lookup"><span data-stu-id="8456a-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="8456a-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="8456a-119">Structure Content</span></span>

<span data-ttu-id="8456a-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="8456a-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="8456a-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="8456a-121">Structure Properties</span></span>

<span data-ttu-id="8456a-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="8456a-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8456a-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="8456a-123">Property</span></span>                | <span data-ttu-id="8456a-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8456a-124">xsi:type</span></span>           | <span data-ttu-id="8456a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8456a-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="8456a-126">DataType</span><span class="sxs-lookup"><span data-stu-id="8456a-126">DataType</span></span><br/>     | <span data-ttu-id="8456a-127">строка</span><span class="sxs-lookup"><span data-stu-id="8456a-127">string</span></span><br/>  | <span data-ttu-id="8456a-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8456a-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="8456a-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8456a-129">DefaultValue</span></span><br/> | <span data-ttu-id="8456a-130">целое число</span><span class="sxs-lookup"><span data-stu-id="8456a-130">integer</span></span><br/> | <span data-ttu-id="8456a-131">1</span><span class="sxs-lookup"><span data-stu-id="8456a-131">1</span></span><br/>                 |
| <span data-ttu-id="8456a-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="8456a-132">MaxValue</span></span><br/>     | <span data-ttu-id="8456a-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="8456a-133">integer</span></span><br/> | <span data-ttu-id="8456a-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="8456a-134">undefined</span></span><br/>         |
| <span data-ttu-id="8456a-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="8456a-135">MinValue</span></span><br/>     | <span data-ttu-id="8456a-136">целое число</span><span class="sxs-lookup"><span data-stu-id="8456a-136">integer</span></span><br/> | <span data-ttu-id="8456a-137">1</span><span class="sxs-lookup"><span data-stu-id="8456a-137">1</span></span><br/>                 |
| <span data-ttu-id="8456a-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8456a-138">Mandatory</span></span><br/>    | <span data-ttu-id="8456a-139">строка</span><span class="sxs-lookup"><span data-stu-id="8456a-139">string</span></span><br/>  | <span data-ttu-id="8456a-140">PSK: безусловное</span><span class="sxs-lookup"><span data-stu-id="8456a-140">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="8456a-141">Несколько</span><span class="sxs-lookup"><span data-stu-id="8456a-141">Multiple</span></span><br/>     | <span data-ttu-id="8456a-142">целое число</span><span class="sxs-lookup"><span data-stu-id="8456a-142">integer</span></span><br/> | <span data-ttu-id="8456a-143">1</span><span class="sxs-lookup"><span data-stu-id="8456a-143">1</span></span><br/>                 |
| <span data-ttu-id="8456a-144">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="8456a-144">UnitType</span></span><br/>     | <span data-ttu-id="8456a-145">строка</span><span class="sxs-lookup"><span data-stu-id="8456a-145">string</span></span><br/>  | <span data-ttu-id="8456a-146">Копи</span><span class="sxs-lookup"><span data-stu-id="8456a-146">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="8456a-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8456a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8456a-148">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="8456a-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




