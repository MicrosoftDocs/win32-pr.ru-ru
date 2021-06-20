---
description: Сведения о свойстве Имя_документа, которое указывает описательное имя документа.
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: Имя_документа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d202ff1f5bac85fec3feac9f141834adfcd37e70
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409277"
---
# <a name="documentname"></a><span data-ttu-id="3683d-103">Имя_документа</span><span class="sxs-lookup"><span data-stu-id="3683d-103">DocumentName</span></span>

<span data-ttu-id="3683d-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="3683d-104">This topic is not current.</span></span> <span data-ttu-id="3683d-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3683d-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3683d-106">Указывает описательное имя документа.</span><span class="sxs-lookup"><span data-stu-id="3683d-106">Specifies a descriptive name for the document.</span></span>

-   [<span data-ttu-id="3683d-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3683d-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3683d-108">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="3683d-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3683d-109">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="3683d-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3683d-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3683d-110">Element Information</span></span>



| <span data-ttu-id="3683d-111">Имя</span><span class="sxs-lookup"><span data-stu-id="3683d-111">Name</span></span> | <span data-ttu-id="3683d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="3683d-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="3683d-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="3683d-113">Element Type</span></span> <br/>   | <span data-ttu-id="3683d-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="3683d-114">Property</span></span><br/> |
| <span data-ttu-id="3683d-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="3683d-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3683d-116">Документ</span><span class="sxs-lookup"><span data-stu-id="3683d-116">Document</span></span><br/> |
| <span data-ttu-id="3683d-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="3683d-117">Notes</span></span> <br/>          | <span data-ttu-id="3683d-118">Нет</span><span class="sxs-lookup"><span data-stu-id="3683d-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="3683d-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="3683d-119">Structural Content</span></span>

<span data-ttu-id="3683d-120">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3683d-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string">_DocumentNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="3683d-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="3683d-121">Structure Variables</span></span>

<span data-ttu-id="3683d-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="3683d-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3683d-123">Имя</span><span class="sxs-lookup"><span data-stu-id="3683d-123">Name</span></span>                             | <span data-ttu-id="3683d-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3683d-124">Data type</span></span>         | <span data-ttu-id="3683d-125">Unit</span><span class="sxs-lookup"><span data-stu-id="3683d-125">Unit</span></span> | <span data-ttu-id="3683d-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="3683d-126">Supported values</span></span> | <span data-ttu-id="3683d-127">Итоги</span><span class="sxs-lookup"><span data-stu-id="3683d-127">Summary</span></span> |
|----------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="3683d-128">\_документнамевалуе\_</span><span class="sxs-lookup"><span data-stu-id="3683d-128">\_DocumentNameValue\_</span></span><br/> | <span data-ttu-id="3683d-129">строка</span><span class="sxs-lookup"><span data-stu-id="3683d-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3683d-130">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="3683d-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="3683d-131">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="3683d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3683d-132">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="3683d-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




