---
description: Сведения об элементе JobID, который указывает уникальный идентификатор для задания. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfd17d068f34b56d45e4851c06b7ed1d9bd6fcc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408887"
---
# <a name="jobid"></a><span data-ttu-id="773d8-104">JobID</span><span class="sxs-lookup"><span data-stu-id="773d8-104">JobID</span></span>

<span data-ttu-id="773d8-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="773d8-105">This topic is not current.</span></span> <span data-ttu-id="773d8-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="773d8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="773d8-107">Указывает уникальный идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="773d8-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="773d8-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="773d8-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="773d8-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="773d8-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="773d8-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="773d8-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="773d8-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="773d8-111">Element Information</span></span>



| <span data-ttu-id="773d8-112">Имя</span><span class="sxs-lookup"><span data-stu-id="773d8-112">Name</span></span> | <span data-ttu-id="773d8-113">Значение</span><span class="sxs-lookup"><span data-stu-id="773d8-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="773d8-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="773d8-114">Element Type</span></span> <br/>   | <span data-ttu-id="773d8-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="773d8-115">Property</span></span><br/> |
| <span data-ttu-id="773d8-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="773d8-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="773d8-117">Задание</span><span class="sxs-lookup"><span data-stu-id="773d8-117">Job</span></span><br/>      |
| <span data-ttu-id="773d8-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="773d8-118">Notes</span></span> <br/>          | <span data-ttu-id="773d8-119">Нет</span><span class="sxs-lookup"><span data-stu-id="773d8-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="773d8-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="773d8-120">Structural Content</span></span>

<span data-ttu-id="773d8-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="773d8-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="773d8-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="773d8-122">Structure Variables</span></span>

<span data-ttu-id="773d8-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="773d8-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="773d8-124">Имя</span><span class="sxs-lookup"><span data-stu-id="773d8-124">Name</span></span>                      | <span data-ttu-id="773d8-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="773d8-125">Data type</span></span>         | <span data-ttu-id="773d8-126">Unit</span><span class="sxs-lookup"><span data-stu-id="773d8-126">Unit</span></span> | <span data-ttu-id="773d8-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="773d8-127">Supported values</span></span> | <span data-ttu-id="773d8-128">Итоги</span><span class="sxs-lookup"><span data-stu-id="773d8-128">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="773d8-129">\_жобидвалуе\_</span><span class="sxs-lookup"><span data-stu-id="773d8-129">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="773d8-130">строка</span><span class="sxs-lookup"><span data-stu-id="773d8-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="773d8-131">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="773d8-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="773d8-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="773d8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="773d8-133">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="773d8-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




