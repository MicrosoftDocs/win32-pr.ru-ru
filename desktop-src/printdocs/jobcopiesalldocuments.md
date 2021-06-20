---
description: Сведения об элементе Жобкопиесаллдокументс, который указывает количество копий задания.
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: жобкопиесаллдокументс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05166715a5985c5ddee33fa6808d0fb6b150774b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409037"
---
# <a name="jobcopiesalldocuments"></a><span data-ttu-id="19d74-103">жобкопиесаллдокументс</span><span class="sxs-lookup"><span data-stu-id="19d74-103">JobCopiesAllDocuments</span></span>

<span data-ttu-id="19d74-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="19d74-104">This topic is not current.</span></span> <span data-ttu-id="19d74-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="19d74-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="19d74-106">Указывает количество копий задания.</span><span class="sxs-lookup"><span data-stu-id="19d74-106">Specifies the number of copies of a job.</span></span>

-   [<span data-ttu-id="19d74-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="19d74-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="19d74-108">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="19d74-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="19d74-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="19d74-109">Element Information</span></span>



| <span data-ttu-id="19d74-110">Имя</span><span class="sxs-lookup"><span data-stu-id="19d74-110">Name</span></span> | <span data-ttu-id="19d74-111">Значение</span><span class="sxs-lookup"><span data-stu-id="19d74-111">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="19d74-112">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="19d74-112">Element Type</span></span> <br/>   | <span data-ttu-id="19d74-113">параметердеф</span><span class="sxs-lookup"><span data-stu-id="19d74-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="19d74-114">Префикс области</span><span class="sxs-lookup"><span data-stu-id="19d74-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="19d74-115">Задание</span><span class="sxs-lookup"><span data-stu-id="19d74-115">Job</span></span><br/>          |
| <span data-ttu-id="19d74-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="19d74-116">Notes</span></span> <br/>          | <span data-ttu-id="19d74-117">Нет</span><span class="sxs-lookup"><span data-stu-id="19d74-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="19d74-118">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="19d74-118">Structure Content</span></span>

<span data-ttu-id="19d74-119">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="19d74-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobCopiesAllDocuments">
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

## <a name="structure-properties"></a><span data-ttu-id="19d74-120">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="19d74-120">Structure Properties</span></span>

<span data-ttu-id="19d74-121">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="19d74-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="19d74-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="19d74-122">Property</span></span>                | <span data-ttu-id="19d74-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="19d74-123">xsi:type</span></span>           | <span data-ttu-id="19d74-124">Значение</span><span class="sxs-lookup"><span data-stu-id="19d74-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="19d74-125">DataType</span><span class="sxs-lookup"><span data-stu-id="19d74-125">DataType</span></span><br/>     | <span data-ttu-id="19d74-126">строка</span><span class="sxs-lookup"><span data-stu-id="19d74-126">string</span></span><br/>  | <span data-ttu-id="19d74-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="19d74-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="19d74-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="19d74-128">DefaultValue</span></span><br/> | <span data-ttu-id="19d74-129">целое число</span><span class="sxs-lookup"><span data-stu-id="19d74-129">integer</span></span><br/> | <span data-ttu-id="19d74-130">1</span><span class="sxs-lookup"><span data-stu-id="19d74-130">1</span></span><br/>                 |
| <span data-ttu-id="19d74-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="19d74-131">MaxValue</span></span><br/>     | <span data-ttu-id="19d74-132">Целое число</span><span class="sxs-lookup"><span data-stu-id="19d74-132">integer</span></span><br/> | <span data-ttu-id="19d74-133">неопределенный</span><span class="sxs-lookup"><span data-stu-id="19d74-133">undefined</span></span><br/>         |
| <span data-ttu-id="19d74-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="19d74-134">MinValue</span></span><br/>     | <span data-ttu-id="19d74-135">целое число</span><span class="sxs-lookup"><span data-stu-id="19d74-135">integer</span></span><br/> | <span data-ttu-id="19d74-136">1</span><span class="sxs-lookup"><span data-stu-id="19d74-136">1</span></span><br/>                 |
| <span data-ttu-id="19d74-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="19d74-137">Mandatory</span></span><br/>    | <span data-ttu-id="19d74-138">строка</span><span class="sxs-lookup"><span data-stu-id="19d74-138">string</span></span><br/>  | <span data-ttu-id="19d74-139">PSK: безусловное</span><span class="sxs-lookup"><span data-stu-id="19d74-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="19d74-140">Несколько</span><span class="sxs-lookup"><span data-stu-id="19d74-140">Multiple</span></span><br/>     | <span data-ttu-id="19d74-141">целое число</span><span class="sxs-lookup"><span data-stu-id="19d74-141">integer</span></span><br/> | <span data-ttu-id="19d74-142">1</span><span class="sxs-lookup"><span data-stu-id="19d74-142">1</span></span><br/>                 |
| <span data-ttu-id="19d74-143">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="19d74-143">UnitType</span></span><br/>     | <span data-ttu-id="19d74-144">строка</span><span class="sxs-lookup"><span data-stu-id="19d74-144">string</span></span><br/>  | <span data-ttu-id="19d74-145">Копи</span><span class="sxs-lookup"><span data-stu-id="19d74-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="19d74-146">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="19d74-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19d74-147">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="19d74-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




