---
description: 'Этот образец иллюстрирует компоновку файла. CUB, содержащего два объекта ICEs. Установщик выполняет пользовательские действия в последовательности: ICE01 и ICE08.'
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: Пример файла Sample. cub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e937b779e2a620ffc17cf936e37f74867f3dfdd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991072"
---
# <a name="sample-cub-file"></a><span data-ttu-id="0e6df-104">Пример файла Sample. cub</span><span class="sxs-lookup"><span data-stu-id="0e6df-104">Sample .cub File</span></span>

<span data-ttu-id="0e6df-105">Этот образец иллюстрирует компоновку файла. CUB, содержащего два объекта [ICEs](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="0e6df-105">This sample illustrates the layout of a .cub file containing two [ICEs](internal-consistency-evaluators-ices.md).</span></span> <span data-ttu-id="0e6df-106">Установщик выполняет пользовательские действия в последовательности: ICE01 и ICE08.</span><span class="sxs-lookup"><span data-stu-id="0e6df-106">The installer executes the custom actions in the sequence: ICE01 and ICE08.</span></span>

<span data-ttu-id="0e6df-107">Настраиваемое действие ICE01 — это [тип настраиваемого действия 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="0e6df-107">The custom action ICE01 is a [Custom Action Type 1](custom-action-type-1.md).</span></span> <span data-ttu-id="0e6df-108">Это точка входа в библиотеку DLL, которая хранится в виде потока в файле. cub.</span><span class="sxs-lookup"><span data-stu-id="0e6df-108">It is an entry point to a DLL that is stored as a stream in the .cub file.</span></span> <span data-ttu-id="0e6df-109">Этот поток указан в ice.dll двоичной таблицы.</span><span class="sxs-lookup"><span data-stu-id="0e6df-109">This stream is listed in the Binary Table ice.dll.</span></span>

<span data-ttu-id="0e6df-110">Настраиваемое действие ICE08 — это [тип настраиваемого действия 6](custom-action-type-6.md).</span><span class="sxs-lookup"><span data-stu-id="0e6df-110">The custom action ICE08 is a [Custom Action Type 6](custom-action-type-6.md).</span></span> <span data-ttu-id="0e6df-111">Это точка входа для функции в VBScript, которая хранится в виде потока в файле. cub.</span><span class="sxs-lookup"><span data-stu-id="0e6df-111">It is an entry point to a function in VBScript that is stored as a stream in the .cub file.</span></span> <span data-ttu-id="0e6df-112">Этот поток указан в двоичной таблице как ice.vbs.</span><span class="sxs-lookup"><span data-stu-id="0e6df-112">This stream is listed in the Binary Table as ice.vbs.</span></span>

[<span data-ttu-id="0e6df-113">Двоичная таблица</span><span class="sxs-lookup"><span data-stu-id="0e6df-113">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="0e6df-114">Имя</span><span class="sxs-lookup"><span data-stu-id="0e6df-114">Name</span></span>    | <span data-ttu-id="0e6df-115">Данные</span><span class="sxs-lookup"><span data-stu-id="0e6df-115">Data</span></span>                               |
|---------|------------------------------------|
| <span data-ttu-id="0e6df-116">ice.vbs</span><span class="sxs-lookup"><span data-stu-id="0e6df-116">ice.vbs</span></span> | <span data-ttu-id="0e6df-117">Неформатированные двоичные данные ice.vbs</span><span class="sxs-lookup"><span data-stu-id="0e6df-117">Unformatted binary data of ice.vbs</span></span> |
| <span data-ttu-id="0e6df-118">ice.dll</span><span class="sxs-lookup"><span data-stu-id="0e6df-118">ice.dll</span></span> | <span data-ttu-id="0e6df-119">Неформатированные двоичные данные ice.dll</span><span class="sxs-lookup"><span data-stu-id="0e6df-119">Unformatted binary data of ice.dll</span></span> |



 

[<span data-ttu-id="0e6df-120">Таблица CustomAction</span><span class="sxs-lookup"><span data-stu-id="0e6df-120">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="0e6df-121">Действие</span><span class="sxs-lookup"><span data-stu-id="0e6df-121">Action</span></span> | <span data-ttu-id="0e6df-122">Тип</span><span class="sxs-lookup"><span data-stu-id="0e6df-122">Type</span></span> | <span data-ttu-id="0e6df-123">Источник</span><span class="sxs-lookup"><span data-stu-id="0e6df-123">Source</span></span>  | <span data-ttu-id="0e6df-124">Назначение</span><span class="sxs-lookup"><span data-stu-id="0e6df-124">Target</span></span> |
|--------|------|---------|--------|
| <span data-ttu-id="0e6df-125">ICE01</span><span class="sxs-lookup"><span data-stu-id="0e6df-125">ICE01</span></span>  | <span data-ttu-id="0e6df-126">1</span><span class="sxs-lookup"><span data-stu-id="0e6df-126">1</span></span>    | <span data-ttu-id="0e6df-127">ice.dll</span><span class="sxs-lookup"><span data-stu-id="0e6df-127">ice.dll</span></span> | <span data-ttu-id="0e6df-128">ICE01</span><span class="sxs-lookup"><span data-stu-id="0e6df-128">ICE01</span></span>  |
| <span data-ttu-id="0e6df-129">ICE08</span><span class="sxs-lookup"><span data-stu-id="0e6df-129">ICE08</span></span>  | <span data-ttu-id="0e6df-130">6</span><span class="sxs-lookup"><span data-stu-id="0e6df-130">6</span></span>    | <span data-ttu-id="0e6df-131">ice.vbs</span><span class="sxs-lookup"><span data-stu-id="0e6df-131">ice.vbs</span></span> | <span data-ttu-id="0e6df-132">ICE02</span><span class="sxs-lookup"><span data-stu-id="0e6df-132">ICE02</span></span>  |



 

<span data-ttu-id="0e6df-133">\_Таблица Ицесекуенце</span><span class="sxs-lookup"><span data-stu-id="0e6df-133">\_ICESequence Table</span></span>



| <span data-ttu-id="0e6df-134">Действие</span><span class="sxs-lookup"><span data-stu-id="0e6df-134">Action</span></span> | <span data-ttu-id="0e6df-135">Условие</span><span class="sxs-lookup"><span data-stu-id="0e6df-135">Condition</span></span> | <span data-ttu-id="0e6df-136">Последовательность</span><span class="sxs-lookup"><span data-stu-id="0e6df-136">Sequence</span></span> |
|--------|-----------|----------|
| <span data-ttu-id="0e6df-137">ICE01</span><span class="sxs-lookup"><span data-stu-id="0e6df-137">ICE01</span></span>  |           | <span data-ttu-id="0e6df-138">10</span><span class="sxs-lookup"><span data-stu-id="0e6df-138">10</span></span>       |
| <span data-ttu-id="0e6df-139">ICE08</span><span class="sxs-lookup"><span data-stu-id="0e6df-139">ICE08</span></span>  |           | <span data-ttu-id="0e6df-140">20</span><span class="sxs-lookup"><span data-stu-id="0e6df-140">20</span></span>       |



 

<span data-ttu-id="0e6df-141">\_Специальная таблица</span><span class="sxs-lookup"><span data-stu-id="0e6df-141">\_Special Table</span></span>

<span data-ttu-id="0e6df-142">ICE01 и ICE08 не нуждаются в включении специальных таблиц обработки.</span><span class="sxs-lookup"><span data-stu-id="0e6df-142">ICE01 and ICE08 do not require the inclusion of special processing tables.</span></span> <span data-ttu-id="0e6df-143">Если файл. cub содержит специальные таблицы, они также должны быть включены в \_ таблицу проверки.</span><span class="sxs-lookup"><span data-stu-id="0e6df-143">When the .cub file contains special tables they must also be included in the \_Validation Table.</span></span>

[<span data-ttu-id="0e6df-144">\_Таблица проверки</span><span class="sxs-lookup"><span data-stu-id="0e6df-144">\_Validation Table</span></span>](-validation-table.md)



| <span data-ttu-id="0e6df-145">Таблица</span><span class="sxs-lookup"><span data-stu-id="0e6df-145">Table</span></span>         | <span data-ttu-id="0e6df-146">Столбец</span><span class="sxs-lookup"><span data-stu-id="0e6df-146">Column</span></span>    | <span data-ttu-id="0e6df-147">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="0e6df-147">Nullable</span></span> | <span data-ttu-id="0e6df-148">MinValue</span><span class="sxs-lookup"><span data-stu-id="0e6df-148">MinValue</span></span> | <span data-ttu-id="0e6df-149">MaxValue</span><span class="sxs-lookup"><span data-stu-id="0e6df-149">MaxValue</span></span> | <span data-ttu-id="0e6df-150">кэйтабле</span><span class="sxs-lookup"><span data-stu-id="0e6df-150">KeyTable</span></span> | <span data-ttu-id="0e6df-151">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="0e6df-151">KeyColumn</span></span> | <span data-ttu-id="0e6df-152">Категория</span><span class="sxs-lookup"><span data-stu-id="0e6df-152">Category</span></span>                         | <span data-ttu-id="0e6df-153">Присвойте параметру</span><span class="sxs-lookup"><span data-stu-id="0e6df-153">Set</span></span> | <span data-ttu-id="0e6df-154">Описание</span><span class="sxs-lookup"><span data-stu-id="0e6df-154">Description</span></span> |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| <span data-ttu-id="0e6df-155">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="0e6df-155">Binary</span></span>        | <span data-ttu-id="0e6df-156">Имя</span><span class="sxs-lookup"><span data-stu-id="0e6df-156">Name</span></span>      | <span data-ttu-id="0e6df-157">Нет</span><span class="sxs-lookup"><span data-stu-id="0e6df-157">N</span></span>        |          |          |          |           | [<span data-ttu-id="0e6df-158">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0e6df-158">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="0e6df-159">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="0e6df-159">Binary</span></span>        | <span data-ttu-id="0e6df-160">Данные</span><span class="sxs-lookup"><span data-stu-id="0e6df-160">Data</span></span>      | <span data-ttu-id="0e6df-161">Нет</span><span class="sxs-lookup"><span data-stu-id="0e6df-161">N</span></span>        |          |          |          |           | [<span data-ttu-id="0e6df-162">Двоичный</span><span class="sxs-lookup"><span data-stu-id="0e6df-162">Binary</span></span>](binary.md)             |     |             |
| <span data-ttu-id="0e6df-163">CustomAction</span><span class="sxs-lookup"><span data-stu-id="0e6df-163">CustomAction</span></span>  | <span data-ttu-id="0e6df-164">Действие</span><span class="sxs-lookup"><span data-stu-id="0e6df-164">Action</span></span>    | <span data-ttu-id="0e6df-165">Нет</span><span class="sxs-lookup"><span data-stu-id="0e6df-165">N</span></span>        |          |          |          |           | [<span data-ttu-id="0e6df-166">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0e6df-166">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="0e6df-167">CustomAction</span><span class="sxs-lookup"><span data-stu-id="0e6df-167">CustomAction</span></span>  | <span data-ttu-id="0e6df-168">Тип</span><span class="sxs-lookup"><span data-stu-id="0e6df-168">Type</span></span>      | <span data-ttu-id="0e6df-169">Нет</span><span class="sxs-lookup"><span data-stu-id="0e6df-169">N</span></span>        |          |          |          |           | [<span data-ttu-id="0e6df-170">Integer</span><span class="sxs-lookup"><span data-stu-id="0e6df-170">Integer</span></span>](integer.md)           |     |             |
| <span data-ttu-id="0e6df-171">CustomAction</span><span class="sxs-lookup"><span data-stu-id="0e6df-171">CustomAction</span></span>  | <span data-ttu-id="0e6df-172">Источник</span><span class="sxs-lookup"><span data-stu-id="0e6df-172">Source</span></span>    | <span data-ttu-id="0e6df-173">Да</span><span class="sxs-lookup"><span data-stu-id="0e6df-173">Y</span></span>        |          |          |          |           | [<span data-ttu-id="0e6df-174">кустомсаурце</span><span class="sxs-lookup"><span data-stu-id="0e6df-174">CustomSource</span></span>](customsource.md) |     |             |
| <span data-ttu-id="0e6df-175">CustomAction</span><span class="sxs-lookup"><span data-stu-id="0e6df-175">CustomAction</span></span>  | <span data-ttu-id="0e6df-176">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="0e6df-176">Target</span></span>    | <span data-ttu-id="0e6df-177">Да</span><span class="sxs-lookup"><span data-stu-id="0e6df-177">Y</span></span>        |          |          |          |           | [<span data-ttu-id="0e6df-178">Формате</span><span class="sxs-lookup"><span data-stu-id="0e6df-178">Formatted</span></span>](formatted.md)       |     |             |
| <span data-ttu-id="0e6df-179">\_ицесекуенце</span><span class="sxs-lookup"><span data-stu-id="0e6df-179">\_ICESequence</span></span> | <span data-ttu-id="0e6df-180">Действие</span><span class="sxs-lookup"><span data-stu-id="0e6df-180">Action</span></span>    | <span data-ttu-id="0e6df-181">Нет</span><span class="sxs-lookup"><span data-stu-id="0e6df-181">N</span></span>        |          |          |          |           | [<span data-ttu-id="0e6df-182">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0e6df-182">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="0e6df-183">\_ицесекуенце</span><span class="sxs-lookup"><span data-stu-id="0e6df-183">\_ICESequence</span></span> | <span data-ttu-id="0e6df-184">Условие</span><span class="sxs-lookup"><span data-stu-id="0e6df-184">Condition</span></span> | <span data-ttu-id="0e6df-185">Да</span><span class="sxs-lookup"><span data-stu-id="0e6df-185">Y</span></span>        |          |          |          |           | [<span data-ttu-id="0e6df-186">Condition</span><span class="sxs-lookup"><span data-stu-id="0e6df-186">Condition</span></span>](condition.md)       |     |             |
| <span data-ttu-id="0e6df-187">\_ицесекуенце</span><span class="sxs-lookup"><span data-stu-id="0e6df-187">\_ICESequence</span></span> | <span data-ttu-id="0e6df-188">Последовательность</span><span class="sxs-lookup"><span data-stu-id="0e6df-188">Sequence</span></span>  | <span data-ttu-id="0e6df-189">Да</span><span class="sxs-lookup"><span data-stu-id="0e6df-189">Y</span></span>        |          |          |          |           | [<span data-ttu-id="0e6df-190">Integer</span><span class="sxs-lookup"><span data-stu-id="0e6df-190">Integer</span></span>](integer.md)           |     |             |



 

 

 



