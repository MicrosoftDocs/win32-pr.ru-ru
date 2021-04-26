---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: b360f870-bfaa-4d4d-adce-17fcfc48b6a6
title: пажедестинатионколорпрофилимбеддед
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7053cfaf82d7fdfccfe79cebcd76e49befeb125
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996131"
---
# <a name="pagedestinationcolorprofileembedded"></a><span data-ttu-id="db1f5-104">пажедестинатионколорпрофилимбеддед</span><span class="sxs-lookup"><span data-stu-id="db1f5-104">PageDestinationColorProfileEmbedded</span></span>

<span data-ttu-id="db1f5-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="db1f5-105">This topic is not current.</span></span> <span data-ttu-id="db1f5-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="db1f5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="db1f5-107">Задает встроенный цветовой профиль назначения.</span><span class="sxs-lookup"><span data-stu-id="db1f5-107">Specifies the embedded destination color profile.</span></span>

-   [<span data-ttu-id="db1f5-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="db1f5-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="db1f5-109">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="db1f5-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="db1f5-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="db1f5-110">Element Information</span></span>



| <span data-ttu-id="db1f5-111">Имя</span><span class="sxs-lookup"><span data-stu-id="db1f5-111">Name</span></span> | <span data-ttu-id="db1f5-112">Значение</span><span class="sxs-lookup"><span data-stu-id="db1f5-112">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="db1f5-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="db1f5-113">Element Type</span></span> <br/>   | <span data-ttu-id="db1f5-114">параметердеф</span><span class="sxs-lookup"><span data-stu-id="db1f5-114">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="db1f5-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="db1f5-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="db1f5-116">Страница</span><span class="sxs-lookup"><span data-stu-id="db1f5-116">Page</span></span><br/>                                          |
| <span data-ttu-id="db1f5-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="db1f5-117">Notes</span></span> <br/>          | <span data-ttu-id="db1f5-118">Связано с элементом Пажедестинатионколорпрофиле</span><span class="sxs-lookup"><span data-stu-id="db1f5-118">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="db1f5-119">Содержимое структуры</span><span class="sxs-lookup"><span data-stu-id="db1f5-119">Structure Content</span></span>

<span data-ttu-id="db1f5-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="db1f5-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileEmbedded">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="db1f5-121">Свойства структуры</span><span class="sxs-lookup"><span data-stu-id="db1f5-121">Structure Properties</span></span>

<span data-ttu-id="db1f5-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="db1f5-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="db1f5-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="db1f5-123">Property</span></span>                | <span data-ttu-id="db1f5-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="db1f5-124">xsi:type</span></span>           | <span data-ttu-id="db1f5-125">Значение</span><span class="sxs-lookup"><span data-stu-id="db1f5-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="db1f5-126">DataType</span><span class="sxs-lookup"><span data-stu-id="db1f5-126">DataType</span></span><br/>     | <span data-ttu-id="db1f5-127">строка</span><span class="sxs-lookup"><span data-stu-id="db1f5-127">string</span></span><br/>  | <span data-ttu-id="db1f5-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="db1f5-128">xs:string</span></span><br/>       |
| <span data-ttu-id="db1f5-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="db1f5-129">DefaultValue</span></span><br/> | <span data-ttu-id="db1f5-130">строка</span><span class="sxs-lookup"><span data-stu-id="db1f5-130">string</span></span><br/>  | <span data-ttu-id="db1f5-131">неопределенный</span><span class="sxs-lookup"><span data-stu-id="db1f5-131">undefined</span></span><br/>       |
| <span data-ttu-id="db1f5-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="db1f5-132">MaxLength</span></span><br/>    | <span data-ttu-id="db1f5-133">Целое число</span><span class="sxs-lookup"><span data-stu-id="db1f5-133">integer</span></span><br/> | <span data-ttu-id="db1f5-134">неопределенный</span><span class="sxs-lookup"><span data-stu-id="db1f5-134">undefined</span></span><br/>       |
| <span data-ttu-id="db1f5-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="db1f5-135">MinLength</span></span><br/>    | <span data-ttu-id="db1f5-136">целое число</span><span class="sxs-lookup"><span data-stu-id="db1f5-136">integer</span></span><br/> | <span data-ttu-id="db1f5-137">1</span><span class="sxs-lookup"><span data-stu-id="db1f5-137">1</span></span><br/>               |
| <span data-ttu-id="db1f5-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="db1f5-138">Mandatory</span></span><br/>    | <span data-ttu-id="db1f5-139">строка</span><span class="sxs-lookup"><span data-stu-id="db1f5-139">string</span></span><br/>  | <span data-ttu-id="db1f5-140">PSK: условный</span><span class="sxs-lookup"><span data-stu-id="db1f5-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="db1f5-141">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="db1f5-141">UnitType</span></span><br/>     | <span data-ttu-id="db1f5-142">строка</span><span class="sxs-lookup"><span data-stu-id="db1f5-142">string</span></span><br/>  | <span data-ttu-id="db1f5-143">characters</span><span class="sxs-lookup"><span data-stu-id="db1f5-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="db1f5-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="db1f5-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db1f5-145">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="db1f5-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




