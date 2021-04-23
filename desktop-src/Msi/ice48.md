---
description: ICE48 проверяет наличие каталогов, которые жестко запрограммированы на локальные пути в таблице свойств.
ms.assetid: 9dcc2475-23a3-4f77-8828-4d0a036670d4
title: ICE48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c9c9ace086d044109e5f9b91bbc471c37094de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663657"
---
# <a name="ice48"></a><span data-ttu-id="9f8a8-103">ICE48</span><span class="sxs-lookup"><span data-stu-id="9f8a8-103">ICE48</span></span>

<span data-ttu-id="9f8a8-104">ICE48 проверяет наличие каталогов, которые жестко запрограммированы на локальные пути в [таблице свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="9f8a8-104">ICE48 checks for directories that are hard-coded to local paths in the [Property table](property-table.md).</span></span>

<span data-ttu-id="9f8a8-105">Не следует жестко кодировать пути к каталогам на локальных дисках, так как компьютеры отличаются в процессе установки локального диска.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-105">Do not hard-code directory paths to local drives because computers differ in the setup of the local drive.</span></span> <span data-ttu-id="9f8a8-106">Такой подход может быть приемлемым при развертывании приложения на большом количестве компьютеров, где все соответствующие части дисков одинаковы.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-106">This practice may be acceptable if deploying an application to a large number of computers on which the relevant portions of the drives are all the same.</span></span>

## <a name="result"></a><span data-ttu-id="9f8a8-107">Результат</span><span class="sxs-lookup"><span data-stu-id="9f8a8-107">Result</span></span>

<span data-ttu-id="9f8a8-108">ICE48 отправляет сообщение об ошибке, если имеется каталог с жестко запрограммированным локальным путем в таблице свойств.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-108">ICE48 posts an error message if there is a directory that is hard-coded to a local path in the Property table.</span></span>

## <a name="example"></a><span data-ttu-id="9f8a8-109">Пример</span><span class="sxs-lookup"><span data-stu-id="9f8a8-109">Example</span></span>

<span data-ttu-id="9f8a8-110">ICE48 сообщит о следующем предупреждении для показанного примера.</span><span class="sxs-lookup"><span data-stu-id="9f8a8-110">ICE48 would report the following warning for the example shown.</span></span>

``` syntax
Directory 'Dir1' appears to be hardcoded in the property 
    table to a local drive.
```

<span data-ttu-id="9f8a8-111">[Таблица каталогов](directory-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="9f8a8-111">[Directory Table](directory-table.md) (partial)</span></span>



| <span data-ttu-id="9f8a8-112">Каталог</span><span class="sxs-lookup"><span data-stu-id="9f8a8-112">Directory</span></span> | <span data-ttu-id="9f8a8-113">\_Родительский каталог</span><span class="sxs-lookup"><span data-stu-id="9f8a8-113">Directory\_Parent</span></span> | <span data-ttu-id="9f8a8-114">дефаултдир</span><span class="sxs-lookup"><span data-stu-id="9f8a8-114">DefaultDir</span></span> |
|-----------|-------------------|------------|
| <span data-ttu-id="9f8a8-115">Dir1</span><span class="sxs-lookup"><span data-stu-id="9f8a8-115">Dir1</span></span>      |                   | <span data-ttu-id="9f8a8-116">SourceDir</span><span class="sxs-lookup"><span data-stu-id="9f8a8-116">SourceDir</span></span>  |



 

<span data-ttu-id="9f8a8-117">[Таблица свойств](property-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="9f8a8-117">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="9f8a8-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="9f8a8-118">Property</span></span> | <span data-ttu-id="9f8a8-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9f8a8-119">Value</span></span>      |
|----------|------------|
| <span data-ttu-id="9f8a8-120">Dir1</span><span class="sxs-lookup"><span data-stu-id="9f8a8-120">Dir1</span></span>     | <span data-ttu-id="9f8a8-121">d: \\ источник</span><span class="sxs-lookup"><span data-stu-id="9f8a8-121">d:\\source</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9f8a8-122">См. также</span><span class="sxs-lookup"><span data-stu-id="9f8a8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f8a8-123">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="9f8a8-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



