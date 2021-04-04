---
description: ICE35 проверяет, что компоненты, содержащие сжатые файлы, хранящиеся в CAB-файле, не настроены для запуска из источника. При использовании установщик Windows 2,0 или более поздней версии это ограничение было удалено.
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea6a98079d3c57e0c796332cf0cd5f11045a07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998798"
---
# <a name="ice35"></a><span data-ttu-id="a4b32-104">ICE35</span><span class="sxs-lookup"><span data-stu-id="a4b32-104">ICE35</span></span>

<span data-ttu-id="a4b32-105">ICE35 проверяет, что компоненты, содержащие сжатые файлы, хранящиеся в [CAB-файле](cabinet-files.md) , не настроены для запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="a4b32-105">ICE35 validates that components containing compressed files stored in a [cabinet file](cabinet-files.md) are not set to run from source.</span></span> <span data-ttu-id="a4b32-106">При использовании установщик Windows 2,0 или более поздней версии это ограничение было удалено.</span><span class="sxs-lookup"><span data-stu-id="a4b32-106">With Windows Installer 2.0 or later, this restriction has been removed.</span></span>

<span data-ttu-id="a4b32-107">ICE35 запрашивает столбец CAB-файла [таблицы Media](media-table.md) , чтобы определить, какие файлы сжаты и хранятся в CAB-файле.</span><span class="sxs-lookup"><span data-stu-id="a4b32-107">ICE35 queries the Cabinet column of the [Media table](media-table.md) to determine which files are compressed and stored in a cabinet file.</span></span> <span data-ttu-id="a4b32-108">Он запрашивает [таблицу файлов](file-table.md) , чтобы определить, какие компоненты содержат эти файлы.</span><span class="sxs-lookup"><span data-stu-id="a4b32-108">It queries the [File table](file-table.md) to determine which components contain these files.</span></span> <span data-ttu-id="a4b32-109">Наконец, он проверяет [таблицу Component](component-table.md) , чтобы определить, заданы ли биты запуска от источника в столбце Attributes.</span><span class="sxs-lookup"><span data-stu-id="a4b32-109">Finally, it checks the [Component table](component-table.md) to determine whether the run-from-source bits are set in the Attributes column.</span></span>

## <a name="result"></a><span data-ttu-id="a4b32-110">Результат</span><span class="sxs-lookup"><span data-stu-id="a4b32-110">Result</span></span>

<span data-ttu-id="a4b32-111">ICE35 отправляет сообщение об ошибке, если имеется сжатый файл, хранящийся в CAB-файле, принадлежащем компоненту с установленным битом Мсидбкомпонентаттрибутессаурцеонли в столбце Attributes [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a4b32-111">ICE35 posts an error message if there is a compressed file stored in a cabinet file belonging to a component with the msidbComponentAttributesSourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="a4b32-112">При использовании установщик Windows 2,0 или более поздней версии это сообщение об ошибке меняется на предупреждение.</span><span class="sxs-lookup"><span data-stu-id="a4b32-112">With Windows Installer 2.0 or later, this is changed from an error to a warning message.</span></span> <span data-ttu-id="a4b32-113">В пакете, поддерживающем только установщик Windows 2,0 и более поздних версий, \_ свойство PID PAGECOUNT потока сводных данных имеет значение не менее 200.</span><span class="sxs-lookup"><span data-stu-id="a4b32-113">A package that supports only Windows Installer 2.0 and later has the PID\_PAGECOUNT property of the Summary Information Stream set to a value of at least 200.</span></span>

<span data-ttu-id="a4b32-114">ICE35 отправляет предупреждение, если имеется сжатый файл, хранящийся в CAB-файле, принадлежащем компоненту с установленным битом Мсидбкомпонентаттрибутесоптионал в столбце Attributes [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a4b32-114">ICE35 posts warning message if there is a compressed file stored in a cabinet file belonging to a component with the msidbComponentAttributesOptional bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="a4b32-115">Это предупреждающее сообщение было удалено с установщик Windows 2,0 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a4b32-115">This warning message has been removed with Windows Installer 2.0 and later.</span></span>

<span data-ttu-id="a4b32-116">Если несколько файлов в компоненте находятся в CAB-файле, ICE35 сообщает об ошибках для каждого файла с установленным битом запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="a4b32-116">If multiple files in a component are in a cabinet file, ICE35 reports errors for each file that has the run from source bit set.</span></span>

## <a name="example"></a><span data-ttu-id="a4b32-117">Пример</span><span class="sxs-lookup"><span data-stu-id="a4b32-117">Example</span></span>

<span data-ttu-id="a4b32-118">ICE35 сообщает о следующих ошибках и предупреждениях в примере с использованием более ранней версии, чем установщик Windows версии 2,0.</span><span class="sxs-lookup"><span data-stu-id="a4b32-118">ICE35 reports the following errors and warnings for the example shown using a version earlier than Windows Installer version 2.0.</span></span>



| <span data-ttu-id="a4b32-119">ICE35, ошибка</span><span class="sxs-lookup"><span data-stu-id="a4b32-119">ICE35 Error</span></span>                                                                                                | <span data-ttu-id="a4b32-120">Описание</span><span class="sxs-lookup"><span data-stu-id="a4b32-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b32-121">Ошибка: Component3 компонента невозможно запустить только из источника, так как файл его члена "Файл3" сжат.</span><span class="sxs-lookup"><span data-stu-id="a4b32-121">ERROR: Component Component3 cannot be Run From Source only, because its member file 'File3' is compressed.</span></span> | <span data-ttu-id="a4b32-122">Существует сжатый файл, хранящийся в CAB-файле, и этот файл принадлежит компоненту с Саурцеонли битом, заданным в столбце Attributes [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a4b32-122">There is a compressed file stored in a cabinet file and this file belongs to a component with the SourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="a4b32-123">Чтобы устранить эту ошибку, измените младшие 2 бита значения атрибутов Component2's на "00", то есть только локально или удалите "Файл4" из CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="a4b32-123">To fix this error change the lower 2 bits of Component2's Attributes value to "00", meaning Local only, or remove File4 from the CAB file.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="a4b32-124">Ошибка: Component3 компонента невозможно запустить только из источника, так как файл его члена "Файл3" сжат.</span><span class="sxs-lookup"><span data-stu-id="a4b32-124">ERROR: Component Component3 cannot be Run From Source only, because its member file 'File3' is compressed.</span></span> | <span data-ttu-id="a4b32-125">Существует сжатый файл, хранящийся в CAB-файле, и этот файл принадлежит компоненту с Саурцеонли битом, заданным в столбце Attributes [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a4b32-125">There is a compressed file stored in a cabinet file and this file belongs to a component with the SourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="a4b32-126">Поскольку файлы в компоненте не должны исходить из одного носителя, ICE35 сообщает об ошибках для каждого файла в компоненте, который находится в CAB-файле.</span><span class="sxs-lookup"><span data-stu-id="a4b32-126">Because the files in a component do not all have to originate from the same media, ICE35 reports errors for each file in the component that is in a cabinet.</span></span><br/> <span data-ttu-id="a4b32-127">Чтобы устранить эту ошибку, измените младшие 2 бита значения атрибутов Component2's на "00", то есть только локально или удалите "Файл4" из CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="a4b32-127">To fix this error change the lower 2 bits of Component2's Attributes value to "00", meaning Local only, or remove File4 from the CAB file.</span></span><br/> |



 

<span data-ttu-id="a4b32-128">[Таблица мультимедиа](media-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="a4b32-128">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="a4b32-129">DiskID</span><span class="sxs-lookup"><span data-stu-id="a4b32-129">DiskID</span></span> | <span data-ttu-id="a4b32-130">ластсекуенце</span><span class="sxs-lookup"><span data-stu-id="a4b32-130">LastSequence</span></span> | <span data-ttu-id="a4b32-131">Файле</span><span class="sxs-lookup"><span data-stu-id="a4b32-131">Cabinet</span></span>   |
|--------|--------------|-----------|
| <span data-ttu-id="a4b32-132">1</span><span class="sxs-lookup"><span data-stu-id="a4b32-132">1</span></span>      | <span data-ttu-id="a4b32-133">2</span><span class="sxs-lookup"><span data-stu-id="a4b32-133">2</span></span>            |           |
| <span data-ttu-id="a4b32-134">2</span><span class="sxs-lookup"><span data-stu-id="a4b32-134">2</span></span>      | <span data-ttu-id="a4b32-135">4</span><span class="sxs-lookup"><span data-stu-id="a4b32-135">4</span></span>            | <span data-ttu-id="a4b32-136">One.cab</span><span class="sxs-lookup"><span data-stu-id="a4b32-136">One.cab</span></span>   |
| <span data-ttu-id="a4b32-137">3</span><span class="sxs-lookup"><span data-stu-id="a4b32-137">3</span></span>      | <span data-ttu-id="a4b32-138">5</span><span class="sxs-lookup"><span data-stu-id="a4b32-138">5</span></span>            | <span data-ttu-id="a4b32-139">\#Two.cab</span><span class="sxs-lookup"><span data-stu-id="a4b32-139">\#Two.cab</span></span> |



 

<span data-ttu-id="a4b32-140">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="a4b32-140">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="a4b32-141">Файл</span><span class="sxs-lookup"><span data-stu-id="a4b32-141">File</span></span>  | <span data-ttu-id="a4b32-142">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="a4b32-142">Component\_</span></span> | <span data-ttu-id="a4b32-143">Последовательность</span><span class="sxs-lookup"><span data-stu-id="a4b32-143">Sequence</span></span> |
|-------|-------------|----------|
| <span data-ttu-id="a4b32-144">Файл1</span><span class="sxs-lookup"><span data-stu-id="a4b32-144">File1</span></span> | <span data-ttu-id="a4b32-145">Component1</span><span class="sxs-lookup"><span data-stu-id="a4b32-145">Component1</span></span>  | <span data-ttu-id="a4b32-146">1</span><span class="sxs-lookup"><span data-stu-id="a4b32-146">1</span></span>        |
| <span data-ttu-id="a4b32-147">Файл2</span><span class="sxs-lookup"><span data-stu-id="a4b32-147">File2</span></span> | <span data-ttu-id="a4b32-148">Component2</span><span class="sxs-lookup"><span data-stu-id="a4b32-148">Component2</span></span>  | <span data-ttu-id="a4b32-149">2</span><span class="sxs-lookup"><span data-stu-id="a4b32-149">2</span></span>        |
| <span data-ttu-id="a4b32-150">Файл3</span><span class="sxs-lookup"><span data-stu-id="a4b32-150">File3</span></span> | <span data-ttu-id="a4b32-151">Component2</span><span class="sxs-lookup"><span data-stu-id="a4b32-151">Component2</span></span>  | <span data-ttu-id="a4b32-152">3</span><span class="sxs-lookup"><span data-stu-id="a4b32-152">3</span></span>        |
| <span data-ttu-id="a4b32-153">Файл4</span><span class="sxs-lookup"><span data-stu-id="a4b32-153">File4</span></span> | <span data-ttu-id="a4b32-154">Component3</span><span class="sxs-lookup"><span data-stu-id="a4b32-154">Component3</span></span>  | <span data-ttu-id="a4b32-155">4</span><span class="sxs-lookup"><span data-stu-id="a4b32-155">4</span></span>        |
| <span data-ttu-id="a4b32-156">Файл5</span><span class="sxs-lookup"><span data-stu-id="a4b32-156">File5</span></span> | <span data-ttu-id="a4b32-157">Component3</span><span class="sxs-lookup"><span data-stu-id="a4b32-157">Component3</span></span>  | <span data-ttu-id="a4b32-158">5</span><span class="sxs-lookup"><span data-stu-id="a4b32-158">5</span></span>        |



 

<span data-ttu-id="a4b32-159">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="a4b32-159">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="a4b32-160">Компонент</span><span class="sxs-lookup"><span data-stu-id="a4b32-160">Component</span></span>  | <span data-ttu-id="a4b32-161">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a4b32-161">Attributes</span></span> |
|------------|------------|
| <span data-ttu-id="a4b32-162">Component1</span><span class="sxs-lookup"><span data-stu-id="a4b32-162">Component1</span></span> | <span data-ttu-id="a4b32-163">0</span><span class="sxs-lookup"><span data-stu-id="a4b32-163">0</span></span>          |
| <span data-ttu-id="a4b32-164">Component2</span><span class="sxs-lookup"><span data-stu-id="a4b32-164">Component2</span></span> | <span data-ttu-id="a4b32-165">2</span><span class="sxs-lookup"><span data-stu-id="a4b32-165">2</span></span>          |
| <span data-ttu-id="a4b32-166">Component3</span><span class="sxs-lookup"><span data-stu-id="a4b32-166">Component3</span></span> | <span data-ttu-id="a4b32-167">1</span><span class="sxs-lookup"><span data-stu-id="a4b32-167">1</span></span>          |



 

<span data-ttu-id="a4b32-168">[Таблица ярлыков](shortcut-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="a4b32-168">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="a4b32-169">Сочетание клавиш</span><span class="sxs-lookup"><span data-stu-id="a4b32-169">Shortcut</span></span>  | <span data-ttu-id="a4b32-170">Значок\_</span><span class="sxs-lookup"><span data-stu-id="a4b32-170">Icon\_</span></span> |
|-----------|--------|
| <span data-ttu-id="a4b32-171">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="a4b32-171">Shortcut1</span></span> | <span data-ttu-id="a4b32-172">Icon2</span><span class="sxs-lookup"><span data-stu-id="a4b32-172">Icon2</span></span>  |



 

<span data-ttu-id="a4b32-173">Обратите внимание, что файлы также можно пометить как сжатые с помощью свойства [**Сводка по количеству слов**](word-count-summary.md) в [информационном потоке сводки](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="a4b32-173">Note that files can also be marked as compressed using the [**Word Count Summary**](word-count-summary.md) Property of the [Summary Information stream](summary-information-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4b32-174">См. также</span><span class="sxs-lookup"><span data-stu-id="a4b32-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4b32-175">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="a4b32-175">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




