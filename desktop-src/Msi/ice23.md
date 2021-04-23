---
description: ICE23 проверяет порядок табуляции элементов управления для каждого диалогового окна.
ms.assetid: d425f8c6-4615-439d-8194-3a0325eb3cc3
title: ICE23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c1823a70e50d7dd3c42c2e90d6a2d0f11f2fa5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663665"
---
# <a name="ice23"></a><span data-ttu-id="2c26e-103">ICE23</span><span class="sxs-lookup"><span data-stu-id="2c26e-103">ICE23</span></span>

<span data-ttu-id="2c26e-104">ICE23 проверяет порядок табуляции элементов управления для каждого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="2c26e-104">ICE23 validates the control tab order for each dialog box.</span></span>

<span data-ttu-id="2c26e-105">ICE23 проверяет следующее в [диалоговом окне](dialog-table.md) и таблице [элементов управления](control-table.md):</span><span class="sxs-lookup"><span data-stu-id="2c26e-105">ICE23 validates the following in the [Dialog table](dialog-table.md) and [Control table](control-table.md):</span></span>

-   <span data-ttu-id="2c26e-106">Каждая запись в диалоговой таблице указывает элемент управления в \_ первом столбце элемента управления, который существует в диалоговом окне, указанном в столбце диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="2c26e-106">That every record in the Dialog table specifies a control in the Control\_First column that exists in the dialog box specified by the Dialog column.</span></span>
-   <span data-ttu-id="2c26e-107">Каждая запись в таблице элементов управления указывает элемент управления в \_ следующем столбце, который находится в том же диалоговом окне, что и элемент управления, указанный в столбце Control, или элемент управления \_ Next содержит значение null.</span><span class="sxs-lookup"><span data-stu-id="2c26e-107">That every record in the Control table specifies a control in the Control\_Next column that is on the same dialog as the control listed in the Control column, or Control\_Next contains the Null value.</span></span>
-   <span data-ttu-id="2c26e-108">После управления следующими \_ записями элемента управления в таблице элементов управления создается один замкнутый цикл, который возвращается к первоначальному элементу управления.</span><span class="sxs-lookup"><span data-stu-id="2c26e-108">That following the Control\_Next entries from control to control in the Control table makes a single, closed, loop that comes back to the initial control.</span></span> <span data-ttu-id="2c26e-109">Не каждый элемент управления должен находиться в цикле, но цикл должен проходить через каждый элемент управления, имеющий запись в \_ следующем столбце элемента управления.</span><span class="sxs-lookup"><span data-stu-id="2c26e-109">Not every control needs to be in the loop, but the loop must pass through every control that has an entry in the Control\_Next column.</span></span>

## <a name="result"></a><span data-ttu-id="2c26e-110">Результат</span><span class="sxs-lookup"><span data-stu-id="2c26e-110">Result</span></span>

<span data-ttu-id="2c26e-111">ICE23 отправляет сообщение об ошибке, если порядок табуляции элементов управления не формирует в диалоговом окне один замкнутый цикл.</span><span class="sxs-lookup"><span data-stu-id="2c26e-111">ICE23 posts an error message if the tab order of controls does not form a single closed loop in the dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="2c26e-112">Пример</span><span class="sxs-lookup"><span data-stu-id="2c26e-112">Example</span></span>

<span data-ttu-id="2c26e-113">ICE23 выводит следующие сообщения об ошибках для приведенного примера.</span><span class="sxs-lookup"><span data-stu-id="2c26e-113">ICE23 would post the following error messages for the example shown.</span></span>

-   <span data-ttu-id="2c26e-114">Dialog1 не имеет контроля в \_ первую очередь.</span><span class="sxs-lookup"><span data-stu-id="2c26e-114">Dialog1 has no Control\_First.</span></span>
-   <span data-ttu-id="2c26e-115">\_Первым элементом диалогового окна Dialog2 называется несуществующий элемент управления контролкс.</span><span class="sxs-lookup"><span data-stu-id="2c26e-115">Control\_First of dialog Dialog2 refers to nonexistent control ControlX.</span></span>
-   <span data-ttu-id="2c26e-116">Dialog3 имеет незавершенный порядок табуляции в элементе управления Контролб.</span><span class="sxs-lookup"><span data-stu-id="2c26e-116">Dialog3 has dead-end tab order at control ControlB.</span></span>
-   <span data-ttu-id="2c26e-117">Dialog4 имеет неправильный порядок табуляции в элементе управления Контролк</span><span class="sxs-lookup"><span data-stu-id="2c26e-117">Dialog4 has malformed tab order at control ControlC</span></span>
-   <span data-ttu-id="2c26e-118">Dialog5 имеет неправильный порядок табуляции в элементе управления Контролк.</span><span class="sxs-lookup"><span data-stu-id="2c26e-118">Dialog5 has malformed tab order at control ControlC.</span></span>
-   <span data-ttu-id="2c26e-119">Управление \_ следующим элементом управления Dialog6. контролк ссылается на неизвестный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="2c26e-119">Control\_Next of control Dialog6.ControlC links to unknown control.</span></span>

<span data-ttu-id="2c26e-120">[Таблица диалоговых окон](dialog-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="2c26e-120">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="2c26e-121">Диалог</span><span class="sxs-lookup"><span data-stu-id="2c26e-121">Dialog</span></span>  | <span data-ttu-id="2c26e-122">Сначала элемент управления \_</span><span class="sxs-lookup"><span data-stu-id="2c26e-122">Control\_First</span></span> |
|---------|----------------|
| <span data-ttu-id="2c26e-123">Dialog1</span><span class="sxs-lookup"><span data-stu-id="2c26e-123">Dialog1</span></span> |                |
| <span data-ttu-id="2c26e-124">Dialog2</span><span class="sxs-lookup"><span data-stu-id="2c26e-124">Dialog2</span></span> | <span data-ttu-id="2c26e-125">контролкс</span><span class="sxs-lookup"><span data-stu-id="2c26e-125">ControlX</span></span>       |
| <span data-ttu-id="2c26e-126">Dialog3</span><span class="sxs-lookup"><span data-stu-id="2c26e-126">Dialog3</span></span> | <span data-ttu-id="2c26e-127">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="2c26e-127">ControlA</span></span>       |
| <span data-ttu-id="2c26e-128">Dialog4</span><span class="sxs-lookup"><span data-stu-id="2c26e-128">Dialog4</span></span> | <span data-ttu-id="2c26e-129">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="2c26e-129">ControlA</span></span>       |
| <span data-ttu-id="2c26e-130">Dialog5</span><span class="sxs-lookup"><span data-stu-id="2c26e-130">Dialog5</span></span> | <span data-ttu-id="2c26e-131">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="2c26e-131">ControlA</span></span>       |



 

<span data-ttu-id="2c26e-132">[Таблица управления](control-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="2c26e-132">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="2c26e-133">Диалог</span><span class="sxs-lookup"><span data-stu-id="2c26e-133">Dialog</span></span>  | <span data-ttu-id="2c26e-134">Control</span><span class="sxs-lookup"><span data-stu-id="2c26e-134">Control</span></span>  | <span data-ttu-id="2c26e-135">Управление \_ следующим</span><span class="sxs-lookup"><span data-stu-id="2c26e-135">Control\_Next</span></span> |
|---------|----------|---------------|
| <span data-ttu-id="2c26e-136">Dialog1</span><span class="sxs-lookup"><span data-stu-id="2c26e-136">Dialog1</span></span> | <span data-ttu-id="2c26e-137">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="2c26e-137">ControlA</span></span> |               |
| <span data-ttu-id="2c26e-138">Dialog1</span><span class="sxs-lookup"><span data-stu-id="2c26e-138">Dialog1</span></span> | <span data-ttu-id="2c26e-139">контролб</span><span class="sxs-lookup"><span data-stu-id="2c26e-139">ControlB</span></span> | <span data-ttu-id="2c26e-140">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="2c26e-140">ControlA</span></span>      |
| <span data-ttu-id="2c26e-141">Dialog2</span><span class="sxs-lookup"><span data-stu-id="2c26e-141">Dialog2</span></span> | <span data-ttu-id="2c26e-142">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="2c26e-142">ControlA</span></span> | <span data-ttu-id="2c26e-143">контролб</span><span class="sxs-lookup"><span data-stu-id="2c26e-143">ControlB</span></span>      |
| <span data-ttu-id="2c26e-144">Dialog2</span><span class="sxs-lookup"><span data-stu-id="2c26e-144">Dialog2</span></span> | <span data-ttu-id="2c26e-145">контролб</span><span class="sxs-lookup"><span data-stu-id="2c26e-145">ControlB</span></span> | <span data-ttu-id="2c26e-146">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="2c26e-146">ControlA</span></span>      |
| <span data-ttu-id="2c26e-147">Dialog3</span><span class="sxs-lookup"><span data-stu-id="2c26e-147">Dialog3</span></span> | <span data-ttu-id="2c26e-148">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="2c26e-148">ControlA</span></span> | <span data-ttu-id="2c26e-149">контролб</span><span class="sxs-lookup"><span data-stu-id="2c26e-149">ControlB</span></span>      |
| <span data-ttu-id="2c26e-150">Dialog3</span><span class="sxs-lookup"><span data-stu-id="2c26e-150">Dialog3</span></span> | <span data-ttu-id="2c26e-151">контролб</span><span class="sxs-lookup"><span data-stu-id="2c26e-151">ControlB</span></span> |               |
| <span data-ttu-id="2c26e-152">Dialog4</span><span class="sxs-lookup"><span data-stu-id="2c26e-152">Dialog4</span></span> | <span data-ttu-id="2c26e-153">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="2c26e-153">ControlA</span></span> | <span data-ttu-id="2c26e-154">контролб</span><span class="sxs-lookup"><span data-stu-id="2c26e-154">ControlB</span></span>      |
| <span data-ttu-id="2c26e-155">Dialog4</span><span class="sxs-lookup"><span data-stu-id="2c26e-155">Dialog4</span></span> | <span data-ttu-id="2c26e-156">контролб</span><span class="sxs-lookup"><span data-stu-id="2c26e-156">ControlB</span></span> | <span data-ttu-id="2c26e-157">контролк</span><span class="sxs-lookup"><span data-stu-id="2c26e-157">ControlC</span></span>      |
| <span data-ttu-id="2c26e-158">Dialog4</span><span class="sxs-lookup"><span data-stu-id="2c26e-158">Dialog4</span></span> | <span data-ttu-id="2c26e-159">контролк</span><span class="sxs-lookup"><span data-stu-id="2c26e-159">ControlC</span></span> | <span data-ttu-id="2c26e-160">контролб</span><span class="sxs-lookup"><span data-stu-id="2c26e-160">ControlB</span></span>      |
| <span data-ttu-id="2c26e-161">Dialog5</span><span class="sxs-lookup"><span data-stu-id="2c26e-161">Dialog5</span></span> | <span data-ttu-id="2c26e-162">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="2c26e-162">ControlA</span></span> | <span data-ttu-id="2c26e-163">контролб</span><span class="sxs-lookup"><span data-stu-id="2c26e-163">ControlB</span></span>      |
| <span data-ttu-id="2c26e-164">Dialog5</span><span class="sxs-lookup"><span data-stu-id="2c26e-164">Dialog5</span></span> | <span data-ttu-id="2c26e-165">контролб</span><span class="sxs-lookup"><span data-stu-id="2c26e-165">ControlB</span></span> | <span data-ttu-id="2c26e-166">контролк</span><span class="sxs-lookup"><span data-stu-id="2c26e-166">ControlC</span></span>      |
| <span data-ttu-id="2c26e-167">Dialog5</span><span class="sxs-lookup"><span data-stu-id="2c26e-167">Dialog5</span></span> | <span data-ttu-id="2c26e-168">контролк</span><span class="sxs-lookup"><span data-stu-id="2c26e-168">ControlC</span></span> | <span data-ttu-id="2c26e-169">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="2c26e-169">ControlA</span></span>      |
| <span data-ttu-id="2c26e-170">Dialog5</span><span class="sxs-lookup"><span data-stu-id="2c26e-170">Dialog5</span></span> | <span data-ttu-id="2c26e-171">С контролем</span><span class="sxs-lookup"><span data-stu-id="2c26e-171">ControlD</span></span> | <span data-ttu-id="2c26e-172">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="2c26e-172">ControlA</span></span>      |
| <span data-ttu-id="2c26e-173">Dialog6</span><span class="sxs-lookup"><span data-stu-id="2c26e-173">Dialog6</span></span> | <span data-ttu-id="2c26e-174">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="2c26e-174">ControlA</span></span> | <span data-ttu-id="2c26e-175">контролб</span><span class="sxs-lookup"><span data-stu-id="2c26e-175">ControlB</span></span>      |
| <span data-ttu-id="2c26e-176">Dialog6</span><span class="sxs-lookup"><span data-stu-id="2c26e-176">Dialog6</span></span> | <span data-ttu-id="2c26e-177">контролб</span><span class="sxs-lookup"><span data-stu-id="2c26e-177">ControlB</span></span> | <span data-ttu-id="2c26e-178">контролк</span><span class="sxs-lookup"><span data-stu-id="2c26e-178">ControlC</span></span>      |
| <span data-ttu-id="2c26e-179">Dialog6</span><span class="sxs-lookup"><span data-stu-id="2c26e-179">Dialog6</span></span> | <span data-ttu-id="2c26e-180">контролк</span><span class="sxs-lookup"><span data-stu-id="2c26e-180">ControlC</span></span> | <span data-ttu-id="2c26e-181">контролкс</span><span class="sxs-lookup"><span data-stu-id="2c26e-181">ControlX</span></span>      |
| <span data-ttu-id="2c26e-182">Dialog6</span><span class="sxs-lookup"><span data-stu-id="2c26e-182">Dialog6</span></span> | <span data-ttu-id="2c26e-183">С контролем</span><span class="sxs-lookup"><span data-stu-id="2c26e-183">ControlD</span></span> | <span data-ttu-id="2c26e-184">Элемент управления</span><span class="sxs-lookup"><span data-stu-id="2c26e-184">ControlA</span></span>      |



 

<span data-ttu-id="2c26e-185">Чтобы устранить эти ошибки, обратите внимание на следующее в приведенных выше таблицах и внесите указанные изменения.</span><span class="sxs-lookup"><span data-stu-id="2c26e-185">To fix these errors note the following in the above tables and make the indicated changes.</span></span>

<span data-ttu-id="2c26e-186">Не каждая строка в таблице диалога содержит элемент управления, указанный в \_ первом столбце элемента управления.</span><span class="sxs-lookup"><span data-stu-id="2c26e-186">Not every row in the Dialog table has a control specified in the Control\_First column.</span></span> <span data-ttu-id="2c26e-187">Измените \_ первый столбец элемента управления в записи Dialog1 в диалоговой таблице на элемент управления, существующий в Dialog1.</span><span class="sxs-lookup"><span data-stu-id="2c26e-187">Change the Control\_First column of the Dialog1 record in the Dialog table to a control that exists in Dialog1.</span></span>

<span data-ttu-id="2c26e-188">Не каждая строка в диалоговой таблице содержит элемент управления, указанный в \_ первом столбце элемента управления, который существует в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="2c26e-188">Not every row in the Dialog table has a control specified in the Control\_First column that exists on the dialog box.</span></span> <span data-ttu-id="2c26e-189">Измените \_ первый столбец элемента управления Dialog2 на элемент управления, существующий в Dialog2.</span><span class="sxs-lookup"><span data-stu-id="2c26e-189">Change the Control\_First column of the Dialog2 to a control that exists in Dialog2.</span></span>

<span data-ttu-id="2c26e-190">После управления следующими \_ записями в таблице элементов управления из элемента управления в элемент управления в каждом случае не создается замкнутый цикл.</span><span class="sxs-lookup"><span data-stu-id="2c26e-190">Following the Control\_Next entries in the Control table from control to control does not make a closed loop in every case.</span></span> <span data-ttu-id="2c26e-191">Измените \_ следующий столбец элемента управления для контролб в Dialog3 на элемент управления.</span><span class="sxs-lookup"><span data-stu-id="2c26e-191">Change the Control\_Next column for ControlB in Dialog3 to ControlA.</span></span>

<span data-ttu-id="2c26e-192">После управления следующими \_ записями в таблице элементов управления от Control к Control не происходит возврат к первоначальному элементу управления в каждом случае.</span><span class="sxs-lookup"><span data-stu-id="2c26e-192">Following the Control\_Next entries in the Control table from control to control does not lead back to the initial control in every case.</span></span> <span data-ttu-id="2c26e-193">Измените \_ следующий столбец элемента управления для контролк в Dialog4, чтобы он ссылался на элемент управления.</span><span class="sxs-lookup"><span data-stu-id="2c26e-193">Change the Control\_Next column for ControlC in Dialog4 to refer to ControlA.</span></span>

<span data-ttu-id="2c26e-194">После управления следующими \_ записями в таблице элементов управления от Control к Control не передается каждый элемент управления в диалоговом окне, имеющий запись в \_ следующем столбце.</span><span class="sxs-lookup"><span data-stu-id="2c26e-194">Following the Control\_Next entries in the Control table from control to control does not pass through every control in the dialog box having an entry in the Control\_Next column.</span></span> <span data-ttu-id="2c26e-195">Измените значение элемента управления \_ следующий столбец для контролк в Dialog5 на управление.</span><span class="sxs-lookup"><span data-stu-id="2c26e-195">Change the Control\_Next column for ControlC in Dialog5 to ControlD.</span></span>

<span data-ttu-id="2c26e-196">Элемент управления \_ Next не ссылается на допустимый элемент управления, который находится в том же диалоговом окне, что и элемент управления, указанный в столбце Control.</span><span class="sxs-lookup"><span data-stu-id="2c26e-196">Control\_Next does not refer to a valid control that is in the same dialog as the control listed in the Control column.</span></span> <span data-ttu-id="2c26e-197">Измените \_ следующий столбец элемента управления для контролк в Dialog6, чтобы он ссылался на элемент управления.</span><span class="sxs-lookup"><span data-stu-id="2c26e-197">Change the Control\_Next column for ControlC in Dialog6 to refer to ControlD.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c26e-198">См. также</span><span class="sxs-lookup"><span data-stu-id="2c26e-198">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c26e-199">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="2c26e-199">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



