---
description: ICE76 проверяет использование каталога SFP (WFP) в пакетах установщик Windows для Windows Me. Этот ICE также проверяет отсутствие файлов в справочнике по таблицам BindImage.
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5beb0157053e9bd3e4bf0d896f52af04a511ac24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650579"
---
# <a name="ice76"></a><span data-ttu-id="23edb-104">ICE76</span><span class="sxs-lookup"><span data-stu-id="23edb-104">ICE76</span></span>

<span data-ttu-id="23edb-105">ICE76 проверяет использование каталога SFP (WFP) в пакетах установщик Windows для Windows Me.</span><span class="sxs-lookup"><span data-stu-id="23edb-105">ICE76 verifies the use of the SFP (WFP) catalog within Windows Installer packages for Windows Me.</span></span> <span data-ttu-id="23edb-106">Этот ICE также проверяет отсутствие файлов в справочнике по [таблицам](bindimage-table.md) BindImage.</span><span class="sxs-lookup"><span data-stu-id="23edb-106">This ICE also verifies that no files in the BindImage [table](bindimage-table.md) reference SFP catalogs.</span></span>

<span data-ttu-id="23edb-107">Для защиты файлов Windows требуется точное соответствие между файлом и подписью, внедренной в файл каталога.</span><span class="sxs-lookup"><span data-stu-id="23edb-107">Windows File Protection requires an exact match between the file and the signature embedded in the catalog file.</span></span> <span data-ttu-id="23edb-108">Файлы, ссылающиеся на каталог SFP, не должны быть перечислены в таблице BindImage, так как [действие BindImage](bindimage-action.md) для этих файлов различается на разных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="23edb-108">Files that reference a SFP catalog must not be listed in the BindImage table because the effect of the [BindImage action](bindimage-action.md) on these files differs between computers.</span></span> <span data-ttu-id="23edb-109">Файлы, на которые ссылаются каталоги SFP, должны находиться в компонентах, которые являются постоянными или установлены локально.</span><span class="sxs-lookup"><span data-stu-id="23edb-109">Files referenced by SFP catalogs must be in components that are permanent or installed locally.</span></span>

## <a name="result"></a><span data-ttu-id="23edb-110">Результат</span><span class="sxs-lookup"><span data-stu-id="23edb-110">Result</span></span>

<span data-ttu-id="23edb-111">ICE76 отправляет ошибку для каждого файла в [таблице BindImage](bindimage-table.md) , которая также находится в [таблице филесфпкаталог](filesfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="23edb-111">ICE76 posts an error for each file in the [BindImage table](bindimage-table.md) that is also in the [FileSFPCatalog table](filesfpcatalog-table.md).</span></span>

<span data-ttu-id="23edb-112">ICE76 выводит ошибку, если файл в таблице Филесфпкаталог принадлежит компоненту со следующим значением true:</span><span class="sxs-lookup"><span data-stu-id="23edb-112">ICE76 outputs an error if a file in the FileSFPCatalog table belongs to a component with any of the following true:</span></span>

-   <span data-ttu-id="23edb-113">**мсидбкомпонентаттрибутесперманент** не задан в столбце Attributes [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="23edb-113">**msidbComponentAttributesPermanent** is not set in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="23edb-114">**мсидбкомпонентаттрибутессаурцеонли** задается в столбце Attributes таблицы Component.</span><span class="sxs-lookup"><span data-stu-id="23edb-114">**msidbComponentAttributesSourceOnly** is set in the Attributes column of the Component table.</span></span>
-   <span data-ttu-id="23edb-115">**мсидбаттрибутесоптионал** задается в столбце Attributes таблицы Component.</span><span class="sxs-lookup"><span data-stu-id="23edb-115">**msidbAttributesOptional** is set in the Attributes column of the Component table.</span></span>

## <a name="example"></a><span data-ttu-id="23edb-116">Пример</span><span class="sxs-lookup"><span data-stu-id="23edb-116">Example</span></span>

<span data-ttu-id="23edb-117">ICE76 сообщает о следующей ошибке в примере:</span><span class="sxs-lookup"><span data-stu-id="23edb-117">ICE76 reports the following error for the example:</span></span>

``` syntax
File 'File1' references a SFP catalog. Therefore it cannot be in the BindImage table.
```

<span data-ttu-id="23edb-118">[Таблица филесфпкаталог](filesfpcatalog-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="23edb-118">[FileSFPCatalog Table](filesfpcatalog-table.md) (partial)</span></span>



| <span data-ttu-id="23edb-119">Файл\_</span><span class="sxs-lookup"><span data-stu-id="23edb-119">File\_</span></span> | <span data-ttu-id="23edb-120">сфпкаталог\_</span><span class="sxs-lookup"><span data-stu-id="23edb-120">SFPCatalog\_</span></span> |
|--------|--------------|
| <span data-ttu-id="23edb-121">Файл1</span><span class="sxs-lookup"><span data-stu-id="23edb-121">File1</span></span>  | <span data-ttu-id="23edb-122">Catalog1.Cat</span><span class="sxs-lookup"><span data-stu-id="23edb-122">Catalog1.Cat</span></span> |



 

<span data-ttu-id="23edb-123">[Таблица BindImage](bindimage-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="23edb-123">[BindImage Table](bindimage-table.md) (partial)</span></span>



| <span data-ttu-id="23edb-124">Файл\_</span><span class="sxs-lookup"><span data-stu-id="23edb-124">File\_</span></span> |
|--------|
| <span data-ttu-id="23edb-125">Файл1</span><span class="sxs-lookup"><span data-stu-id="23edb-125">File1</span></span>  |



 

<span data-ttu-id="23edb-126">Чтобы исправить это, не вводите файлы, ссылающиеся на каталоги SFP, в таблицу BindImage.</span><span class="sxs-lookup"><span data-stu-id="23edb-126">To fix this do not enter any files that reference SFP catalogs into the BindImage table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23edb-127">См. также</span><span class="sxs-lookup"><span data-stu-id="23edb-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23edb-128">Таблица BindImage</span><span class="sxs-lookup"><span data-stu-id="23edb-128">BindImage Table</span></span>](bindimage-table.md)
</dt> <dt>

[<span data-ttu-id="23edb-129">Таблица компонентов</span><span class="sxs-lookup"><span data-stu-id="23edb-129">Component Table</span></span>](component-table.md)
</dt> <dt>

[<span data-ttu-id="23edb-130">Таблица Филесфпкаталог</span><span class="sxs-lookup"><span data-stu-id="23edb-130">FileSFPCatalog Table</span></span>](filesfpcatalog-table.md)
</dt> <dt>

[<span data-ttu-id="23edb-131">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="23edb-131">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



