---
description: ICE19 проверяет, что объявленные компоненты ссылаются на файл в столбце ключевого пути таблицы Component и что объявленное контекстное меню ссылается на каталог в этом столбце.
ms.assetid: 438153c1-bc4b-4ecf-ab85-d66ad69c987c
title: ICE19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53aa3268a1c77f674d4a130c9de02c44b56243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265224"
---
# <a name="ice19"></a><span data-ttu-id="914d2-103">ICE19</span><span class="sxs-lookup"><span data-stu-id="914d2-103">ICE19</span></span>

<span data-ttu-id="914d2-104">ICE19 проверяет, что объявленные компоненты ссылаются на файл в столбце ключевого пути [таблицы Component](component-table.md) и что объявленное контекстное меню ссылается на каталог в этом столбце.</span><span class="sxs-lookup"><span data-stu-id="914d2-104">ICE19 validates that advertised components reference a file in the KeyPath column of the [Component table](component-table.md) and that an advertised shortcut references a directory in this column.</span></span>

<span data-ttu-id="914d2-105">ICE19 проверяет, что объявленные компоненты или ярлыки имеют ИД компонента.</span><span class="sxs-lookup"><span data-stu-id="914d2-105">ICE19 validates that advertised components or shortcuts have a ComponentId.</span></span> <span data-ttu-id="914d2-106">Компоненты в [таблице публишкомпонент](publishcomponent-table.md), которые не объявлены в другой таблице, проверяются только на наличие у них ИД компонента.</span><span class="sxs-lookup"><span data-stu-id="914d2-106">Components in the [PublishComponent table](publishcomponent-table.md), which are not advertised in another table, are only checked to see whether they have a ComponentId.</span></span>

## <a name="result"></a><span data-ttu-id="914d2-107">Результат</span><span class="sxs-lookup"><span data-stu-id="914d2-107">Result</span></span>

<span data-ttu-id="914d2-108">ICE19 отправляет сообщение об ошибке, если ключевой столбец в таблице Component не ссылается на файл в случае объявленного компонента или каталога в случае объявленного ярлыка.</span><span class="sxs-lookup"><span data-stu-id="914d2-108">ICE19 posts an error message if the KeyPath column of the Component table does not reference a file in the case of an advertised component or a directory in the case of an advertised shortcut.</span></span> <span data-ttu-id="914d2-109">ICE19 отправляет сообщение об ошибке, если ни один из объявленных компонентов или ярлыков не имеет ИД компонента.</span><span class="sxs-lookup"><span data-stu-id="914d2-109">ICE19 posts an error message if any advertised components or shortcuts do not have a ComponentId.</span></span>

## <a name="example"></a><span data-ttu-id="914d2-110">Пример</span><span class="sxs-lookup"><span data-stu-id="914d2-110">Example</span></span>

<span data-ttu-id="914d2-111">ICE19 отправляет следующие сообщения об ошибках в приведенном примере:</span><span class="sxs-lookup"><span data-stu-id="914d2-111">ICE19 posts the following error messages for the example shown:</span></span>

-   <span data-ttu-id="914d2-112">Расширение FLP ссылается на компонент comp1, который не имеет ИД компонента, указанного в [таблице Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="914d2-112">Extension flp references the component Comp1 which does not have a ComponentId specified in the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="914d2-113">Расширение EXE ссылается на компонент Comp4, который ссылается на каталог в качестве ключевого пути.</span><span class="sxs-lookup"><span data-stu-id="914d2-113">Extension exe references the component Comp4 which references a directory as its KeyPath.</span></span> <span data-ttu-id="914d2-114">Ключевой путь имеет значение NULL в таблице Component.</span><span class="sxs-lookup"><span data-stu-id="914d2-114">The KeyPath is Null in the Component table.</span></span>
-   <span data-ttu-id="914d2-115">Ярлык Shortcut2 ссылается на компонент Comp3, который ссылается на запись реестра в качестве пути к ключу.</span><span class="sxs-lookup"><span data-stu-id="914d2-115">Shortcut Shortcut2 references the component Comp3 which references a Registry entry as the key path.</span></span> <span data-ttu-id="914d2-116">Значение столбца Attributes в таблице Component равно 4.</span><span class="sxs-lookup"><span data-stu-id="914d2-116">The value of the Attributes column in the Component table is 4.</span></span>

<span data-ttu-id="914d2-117">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="914d2-117">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="914d2-118">Компонент</span><span class="sxs-lookup"><span data-stu-id="914d2-118">Component</span></span> | <span data-ttu-id="914d2-119">ComponentId</span><span class="sxs-lookup"><span data-stu-id="914d2-119">ComponentId</span></span>                            | <span data-ttu-id="914d2-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="914d2-120">Attributes</span></span> | <span data-ttu-id="914d2-121">Путь</span><span class="sxs-lookup"><span data-stu-id="914d2-121">KeyPath</span></span> |
|-----------|----------------------------------------|------------|---------|
| <span data-ttu-id="914d2-122">Comp1</span><span class="sxs-lookup"><span data-stu-id="914d2-122">Comp1</span></span>     | <span data-ttu-id="914d2-123">NULL</span><span class="sxs-lookup"><span data-stu-id="914d2-123">Null</span></span>                                   | <span data-ttu-id="914d2-124">0</span><span class="sxs-lookup"><span data-stu-id="914d2-124">0</span></span>          | <span data-ttu-id="914d2-125">Файл1</span><span class="sxs-lookup"><span data-stu-id="914d2-125">File1</span></span>   |
| <span data-ttu-id="914d2-126">Comp2</span><span class="sxs-lookup"><span data-stu-id="914d2-126">Comp2</span></span>     | {00000002-0003-0000-0000-624474736554} | <span data-ttu-id="914d2-127">0</span><span class="sxs-lookup"><span data-stu-id="914d2-127">0</span></span>          | <span data-ttu-id="914d2-128">Файл2</span><span class="sxs-lookup"><span data-stu-id="914d2-128">File2</span></span>   |
| <span data-ttu-id="914d2-129">Comp3</span><span class="sxs-lookup"><span data-stu-id="914d2-129">Comp3</span></span>     | {00000003-0003-0000-0000-624474736554} | <span data-ttu-id="914d2-130">4</span><span class="sxs-lookup"><span data-stu-id="914d2-130">4</span></span>          | <span data-ttu-id="914d2-131">Reg3</span><span class="sxs-lookup"><span data-stu-id="914d2-131">Reg3</span></span>    |
| <span data-ttu-id="914d2-132">Comp4</span><span class="sxs-lookup"><span data-stu-id="914d2-132">Comp4</span></span>     | {00000004-0003-0000-0000-624474736554} | <span data-ttu-id="914d2-133">0</span><span class="sxs-lookup"><span data-stu-id="914d2-133">0</span></span>          | <span data-ttu-id="914d2-134">NULL</span><span class="sxs-lookup"><span data-stu-id="914d2-134">Null</span></span>    |



 

<span data-ttu-id="914d2-135">[Таблица расширения](extension-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="914d2-135">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="914d2-136">Расширение</span><span class="sxs-lookup"><span data-stu-id="914d2-136">Extension</span></span> | <span data-ttu-id="914d2-137">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="914d2-137">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="914d2-138">FLP</span><span class="sxs-lookup"><span data-stu-id="914d2-138">flp</span></span>       | <span data-ttu-id="914d2-139">Comp1</span><span class="sxs-lookup"><span data-stu-id="914d2-139">Comp1</span></span>       |
| <span data-ttu-id="914d2-140">TST</span><span class="sxs-lookup"><span data-stu-id="914d2-140">tst</span></span>       | <span data-ttu-id="914d2-141">Comp2</span><span class="sxs-lookup"><span data-stu-id="914d2-141">Comp2</span></span>       |
| <span data-ttu-id="914d2-142">exe</span><span class="sxs-lookup"><span data-stu-id="914d2-142">exe</span></span>       | <span data-ttu-id="914d2-143">Comp4</span><span class="sxs-lookup"><span data-stu-id="914d2-143">Comp4</span></span>       |



 

<span data-ttu-id="914d2-144">[Таблица ярлыков](shortcut-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="914d2-144">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="914d2-145">Сочетание клавиш</span><span class="sxs-lookup"><span data-stu-id="914d2-145">Shortcut</span></span>  | <span data-ttu-id="914d2-146">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="914d2-146">Component\_</span></span> | <span data-ttu-id="914d2-147">Функция\_</span><span class="sxs-lookup"><span data-stu-id="914d2-147">Feature\_</span></span>      |
|-----------|-------------|----------------|
| <span data-ttu-id="914d2-148">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="914d2-148">Shortcut1</span></span> | <span data-ttu-id="914d2-149">Comp4</span><span class="sxs-lookup"><span data-stu-id="914d2-149">Comp4</span></span>       | <span data-ttu-id="914d2-150">продуктфеатуре</span><span class="sxs-lookup"><span data-stu-id="914d2-150">ProductFeature</span></span> |
| <span data-ttu-id="914d2-151">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="914d2-151">Shortcut2</span></span> | <span data-ttu-id="914d2-152">Comp3</span><span class="sxs-lookup"><span data-stu-id="914d2-152">Comp3</span></span>       | <span data-ttu-id="914d2-153">продуктфеатуре</span><span class="sxs-lookup"><span data-stu-id="914d2-153">ProductFeature</span></span> |



 

<span data-ttu-id="914d2-154">[Таблица компонентов](feature-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="914d2-154">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="914d2-155">Функция</span><span class="sxs-lookup"><span data-stu-id="914d2-155">Feature</span></span>        |
|----------------|
| <span data-ttu-id="914d2-156">продуктфеатуре</span><span class="sxs-lookup"><span data-stu-id="914d2-156">ProductFeature</span></span> |



 

> [!Note]  
> <span data-ttu-id="914d2-157">Если расширение FLP и exe ссылается на один и тот же компонент, то исполняемый файл или COM-сервер, который их открывает, должен быть одинаковым.</span><span class="sxs-lookup"><span data-stu-id="914d2-157">If the extension flp and exe both reference the same component, the EXE or COM server that opens them must be the same.</span></span> <span data-ttu-id="914d2-158">Обычно этот EXE-файл является ключевой целью для компонента.</span><span class="sxs-lookup"><span data-stu-id="914d2-158">This EXE is normally the KeyPath for the Component.</span></span> <span data-ttu-id="914d2-159">Для OFFICE модули doc и XLS не могут ссылаться на один и тот же компонент, так как один и тот же исполняемый файл не открывает оба расширения.</span><span class="sxs-lookup"><span data-stu-id="914d2-159">For OFFICE, the extensions doc and xls cannot reference the same component because the same EXE does not open both extensions.</span></span> <span data-ttu-id="914d2-160">Чтобы открыть расширения DOC, необходимо winword.exe, а для открытия модулей XLS необходимо excel.exe.</span><span class="sxs-lookup"><span data-stu-id="914d2-160">You need winword.exe to open doc extensions and you need excel.exe to open xls extensions.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="914d2-161">См. также</span><span class="sxs-lookup"><span data-stu-id="914d2-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="914d2-162">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="914d2-162">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



