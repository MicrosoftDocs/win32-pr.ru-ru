---
description: ICE54 проверяет наличие компонентов, использующих сопутствующий файл в качестве пути к ключу.
ms.assetid: 94fcabfe-4500-42f2-acea-13b9a6681ca6
title: ICE54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df2ba90ccb44e33b67aaf8ecdcadc723e8d2fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910095"
---
# <a name="ice54"></a><span data-ttu-id="4558b-103">ICE54</span><span class="sxs-lookup"><span data-stu-id="4558b-103">ICE54</span></span>

<span data-ttu-id="4558b-104">ICE54 проверяет наличие компонентов, использующих сопутствующий файл в качестве пути к ключу.</span><span class="sxs-lookup"><span data-stu-id="4558b-104">ICE54 checks for components that use a companion file as their key path.</span></span>

<span data-ttu-id="4558b-105">Файл пути к ключу компонента не должен наследовать версию от другого файла.</span><span class="sxs-lookup"><span data-stu-id="4558b-105">The key path file of a component must not derive its version from a different file.</span></span> <span data-ttu-id="4558b-106">Это может привести к сбою установки некоторых файлов.</span><span class="sxs-lookup"><span data-stu-id="4558b-106">This can cause some files to fail to install.</span></span> <span data-ttu-id="4558b-107">Дополнительные сведения о сопутствующих файлах см. в [таблице File](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="4558b-107">See the [File table](file-table.md) for more information about companion files.</span></span>

## <a name="result"></a><span data-ttu-id="4558b-108">Результат</span><span class="sxs-lookup"><span data-stu-id="4558b-108">Result</span></span>

<span data-ttu-id="4558b-109">ICE54 отправляет предупреждение, если какой-либо компонент имеет файл пути к ключу, который получает версию из другого файла.</span><span class="sxs-lookup"><span data-stu-id="4558b-109">ICE54 posts a warning if any component has a key path file that derives its version from another file.</span></span>

## <a name="example"></a><span data-ttu-id="4558b-110">Пример</span><span class="sxs-lookup"><span data-stu-id="4558b-110">Example</span></span>

<span data-ttu-id="4558b-111">ICE54 возвращает следующее предупреждение для показанного примера.</span><span class="sxs-lookup"><span data-stu-id="4558b-111">ICE54 returns the following warning for the example shown.</span></span>

``` syntax
Component 'Component1' uses file 'File1' as its KeyPath, but the file's version is provided by the file 'File2'.
```

<span data-ttu-id="4558b-112">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="4558b-112">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="4558b-113">Компонент</span><span class="sxs-lookup"><span data-stu-id="4558b-113">Component</span></span>  | <span data-ttu-id="4558b-114">attribute</span><span class="sxs-lookup"><span data-stu-id="4558b-114">Attribute</span></span> | <span data-ttu-id="4558b-115">Путь</span><span class="sxs-lookup"><span data-stu-id="4558b-115">KeyPath</span></span> |
|------------|-----------|---------|
| <span data-ttu-id="4558b-116">Component1</span><span class="sxs-lookup"><span data-stu-id="4558b-116">Component1</span></span> | <span data-ttu-id="4558b-117">0</span><span class="sxs-lookup"><span data-stu-id="4558b-117">0</span></span>         | <span data-ttu-id="4558b-118">Файл1</span><span class="sxs-lookup"><span data-stu-id="4558b-118">File1</span></span>   |



 

<span data-ttu-id="4558b-119">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="4558b-119">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="4558b-120">Файл</span><span class="sxs-lookup"><span data-stu-id="4558b-120">File</span></span>  | <span data-ttu-id="4558b-121">Версия</span><span class="sxs-lookup"><span data-stu-id="4558b-121">Version</span></span> | <span data-ttu-id="4558b-122">Язык</span><span class="sxs-lookup"><span data-stu-id="4558b-122">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="4558b-123">Файл1</span><span class="sxs-lookup"><span data-stu-id="4558b-123">File1</span></span> | <span data-ttu-id="4558b-124">Файл2</span><span class="sxs-lookup"><span data-stu-id="4558b-124">File2</span></span>   |          |
| <span data-ttu-id="4558b-125">Файл2</span><span class="sxs-lookup"><span data-stu-id="4558b-125">File2</span></span> | <span data-ttu-id="4558b-126">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="4558b-126">1.0.0.0</span></span> | <span data-ttu-id="4558b-127">1033</span><span class="sxs-lookup"><span data-stu-id="4558b-127">1033</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="4558b-128">См. также</span><span class="sxs-lookup"><span data-stu-id="4558b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4558b-129">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="4558b-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



