---
description: Разработчики установщик Windowsных пакетов могут использовать тип настраиваемого действия 19, если стандартные действия недостаточны для выполнения установки.
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: Тип настраиваемого действия 19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695f86db0848bd65884ce5e233b4d9a249275c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664742"
---
# <a name="custom-action-type-19"></a><span data-ttu-id="172a0-103">Тип настраиваемого действия 19</span><span class="sxs-lookup"><span data-stu-id="172a0-103">Custom Action Type 19</span></span>

<span data-ttu-id="172a0-104">Это пользовательское действие отображает указанное сообщение об ошибке, возвращает ошибку, а затем завершает установку.</span><span class="sxs-lookup"><span data-stu-id="172a0-104">This custom action displays a specified error message, returns failure, and then terminates the installation.</span></span> <span data-ttu-id="172a0-105">Отображаемое сообщение об ошибке может быть представлено в виде строки или индекса в [таблице ошибок](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="172a0-105">The error message displayed can be supplied as a string or as an index into the [Error table](error-table.md).</span></span>

## <a name="source"></a><span data-ttu-id="172a0-106">Источник</span><span class="sxs-lookup"><span data-stu-id="172a0-106">Source</span></span>

<span data-ttu-id="172a0-107">Оставьте поле Исходный столбец [таблицы CustomAction](customaction-table.md) пустым.</span><span class="sxs-lookup"><span data-stu-id="172a0-107">Leave the Source column of the [CustomAction table](customaction-table.md) blank.</span></span>

## <a name="type-value"></a><span data-ttu-id="172a0-108">Значение типа</span><span class="sxs-lookup"><span data-stu-id="172a0-108">Type Value</span></span>

<span data-ttu-id="172a0-109">Включите следующее значение в столбец Type таблицы CustomAction, чтобы указать базовый числовой тип.</span><span class="sxs-lookup"><span data-stu-id="172a0-109">Include the following value in the Type column of the CustomAction table to specify the basic numeric type.</span></span>



| <span data-ttu-id="172a0-110">Константы</span><span class="sxs-lookup"><span data-stu-id="172a0-110">Constants</span></span>                                                               | <span data-ttu-id="172a0-111">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="172a0-111">Hexadecimal</span></span> | <span data-ttu-id="172a0-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="172a0-112">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="172a0-113">**мсидбкустомактионтипетекстдата**  +  **мсидбкустомактионтипесаурцефиле**</span><span class="sxs-lookup"><span data-stu-id="172a0-113">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="172a0-114">0x013</span><span class="sxs-lookup"><span data-stu-id="172a0-114">0x013</span></span>       | <span data-ttu-id="172a0-115">19</span><span class="sxs-lookup"><span data-stu-id="172a0-115">19</span></span>      |



 

## <a name="target"></a><span data-ttu-id="172a0-116">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="172a0-116">Target</span></span>

<span data-ttu-id="172a0-117">Целевой столбец [таблицы CustomAction](customaction-table.md) содержит текстовую строку, отформатированную с помощью функций, указанных в [**мсиформатрекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (без описателей числовых полей).</span><span class="sxs-lookup"><span data-stu-id="172a0-117">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="172a0-118">Заменяемые параметры заключаются в квадратные скобки,.. \[ . \] и могут быть свойствами, переменными среды (% prefix), путями к файлам ( \# префиксом) или путями к каталогам компонентов ($ prefix).</span><span class="sxs-lookup"><span data-stu-id="172a0-118">Parameters to be replaced are enclosed in square brackets, \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span> <span data-ttu-id="172a0-119">Если после форматирования строки возвращается целое число, это целое число используется как индекс в [таблице ошибок](error-table.md) , чтобы получить отображаемое сообщение.</span><span class="sxs-lookup"><span data-stu-id="172a0-119">If after formatting the string evaluates to an integer, that integer is used as an index into the [Error table](error-table.md) to retrieve the message to display.</span></span> <span data-ttu-id="172a0-120">Если после форматирования строки содержатся нечисловые символы, сама строка отображается как сообщение.</span><span class="sxs-lookup"><span data-stu-id="172a0-120">If after formatting the string contains non-numeric characters, the string itself is displayed as the message.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="172a0-121">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="172a0-121">Return Processing Options</span></span>

<span data-ttu-id="172a0-122">В настраиваемом действии не используются никакие параметры.</span><span class="sxs-lookup"><span data-stu-id="172a0-122">The custom action does not use any options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="172a0-123">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="172a0-123">Execution Scheduling Options</span></span>

<span data-ttu-id="172a0-124">В настраиваемом действии не используются никакие параметры.</span><span class="sxs-lookup"><span data-stu-id="172a0-124">The custom action does not use any options.</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="172a0-125">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="172a0-125">In-Script Execution Options</span></span>

<span data-ttu-id="172a0-126">В настраиваемом действии не используются никакие параметры.</span><span class="sxs-lookup"><span data-stu-id="172a0-126">The custom action does not use any options.</span></span>

## <a name="return-values"></a><span data-ttu-id="172a0-127">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="172a0-127">Return Values</span></span>

<span data-ttu-id="172a0-128">См. раздел [возвращаемые значения пользовательских действий](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="172a0-128">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="172a0-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="172a0-129">Remarks</span></span>

<span data-ttu-id="172a0-130">Например, пользовательские действия CAError1, CAError2, CAError3 и CAError4 возвращают эти сообщения.</span><span class="sxs-lookup"><span data-stu-id="172a0-130">For example, the custom actions CAError1, CAError2, CAError3, and CAError4 return these messages.</span></span>

[<span data-ttu-id="172a0-131">Таблица CustomAction</span><span class="sxs-lookup"><span data-stu-id="172a0-131">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="172a0-132">Действие</span><span class="sxs-lookup"><span data-stu-id="172a0-132">Action</span></span>   | <span data-ttu-id="172a0-133">Тип</span><span class="sxs-lookup"><span data-stu-id="172a0-133">Type</span></span> | <span data-ttu-id="172a0-134">Источник</span><span class="sxs-lookup"><span data-stu-id="172a0-134">Source</span></span> | <span data-ttu-id="172a0-135">Назначение</span><span class="sxs-lookup"><span data-stu-id="172a0-135">Target</span></span>                              |
|----------|------|--------|-------------------------------------|
| <span data-ttu-id="172a0-136">CAError1</span><span class="sxs-lookup"><span data-stu-id="172a0-136">CAError1</span></span> | <span data-ttu-id="172a0-137">19</span><span class="sxs-lookup"><span data-stu-id="172a0-137">19</span></span>   |        | <span data-ttu-id="172a0-138">\[Prop1\]</span><span class="sxs-lookup"><span data-stu-id="172a0-138">\[Prop1\]</span></span>                           |
| <span data-ttu-id="172a0-139">CAError2</span><span class="sxs-lookup"><span data-stu-id="172a0-139">CAError2</span></span> | <span data-ttu-id="172a0-140">19</span><span class="sxs-lookup"><span data-stu-id="172a0-140">19</span></span>   |        | <span data-ttu-id="172a0-141">Сбой установки из-за Error2.</span><span class="sxs-lookup"><span data-stu-id="172a0-141">Installation failure due to Error2.</span></span> |
| <span data-ttu-id="172a0-142">CAError3</span><span class="sxs-lookup"><span data-stu-id="172a0-142">CAError3</span></span> | <span data-ttu-id="172a0-143">19</span><span class="sxs-lookup"><span data-stu-id="172a0-143">19</span></span>   |        | <span data-ttu-id="172a0-144">25000</span><span class="sxs-lookup"><span data-stu-id="172a0-144">25000</span></span>                               |
| <span data-ttu-id="172a0-145">CAError4</span><span class="sxs-lookup"><span data-stu-id="172a0-145">CAError4</span></span> | <span data-ttu-id="172a0-146">19</span><span class="sxs-lookup"><span data-stu-id="172a0-146">19</span></span>   |        | <span data-ttu-id="172a0-147">\[Prop2\]</span><span class="sxs-lookup"><span data-stu-id="172a0-147">\[Prop2\]</span></span>                           |



 

[<span data-ttu-id="172a0-148">Таблица свойств</span><span class="sxs-lookup"><span data-stu-id="172a0-148">Property Table</span></span>](property-table.md)



| <span data-ttu-id="172a0-149">Свойство</span><span class="sxs-lookup"><span data-stu-id="172a0-149">Property</span></span> | <span data-ttu-id="172a0-150">Значение</span><span class="sxs-lookup"><span data-stu-id="172a0-150">Value</span></span>                                 |
|----------|---------------------------------------|
| <span data-ttu-id="172a0-151">Prop1</span><span class="sxs-lookup"><span data-stu-id="172a0-151">Prop1</span></span>    | <span data-ttu-id="172a0-152">«Сбой установки из-за Error1».</span><span class="sxs-lookup"><span data-stu-id="172a0-152">"Installation failure due to Error1."</span></span> |
| <span data-ttu-id="172a0-153">Prop2</span><span class="sxs-lookup"><span data-stu-id="172a0-153">Prop2</span></span>    | <span data-ttu-id="172a0-154">"25100"</span><span class="sxs-lookup"><span data-stu-id="172a0-154">"25100"</span></span>                               |



 

[<span data-ttu-id="172a0-155">Таблица ошибок</span><span class="sxs-lookup"><span data-stu-id="172a0-155">Error Table</span></span>](error-table.md)



| <span data-ttu-id="172a0-156">Код</span><span class="sxs-lookup"><span data-stu-id="172a0-156">Code</span></span>  | <span data-ttu-id="172a0-157">Сообщение</span><span class="sxs-lookup"><span data-stu-id="172a0-157">Message</span></span>                             |
|-------|-------------------------------------|
| <span data-ttu-id="172a0-158">25000</span><span class="sxs-lookup"><span data-stu-id="172a0-158">25000</span></span> | <span data-ttu-id="172a0-159">Сбой установки из-за Error3.</span><span class="sxs-lookup"><span data-stu-id="172a0-159">Installation failure due to Error3.</span></span> |
| <span data-ttu-id="172a0-160">25100</span><span class="sxs-lookup"><span data-stu-id="172a0-160">25100</span></span> | <span data-ttu-id="172a0-161">Сбой установки из-за Error4.</span><span class="sxs-lookup"><span data-stu-id="172a0-161">Installation failure due to Error4.</span></span> |



 

<span data-ttu-id="172a0-162">Эти настраиваемые действия возвращают следующие сообщения об ошибках:</span><span class="sxs-lookup"><span data-stu-id="172a0-162">These custom actions return the following error messages:</span></span>



| <span data-ttu-id="172a0-163">Пользовательское действие</span><span class="sxs-lookup"><span data-stu-id="172a0-163">Custom action</span></span> | <span data-ttu-id="172a0-164">Возвращенная строка сообщения</span><span class="sxs-lookup"><span data-stu-id="172a0-164">Returned message string</span></span>             |
|---------------|-------------------------------------|
| <span data-ttu-id="172a0-165">CAError1</span><span class="sxs-lookup"><span data-stu-id="172a0-165">CAError1</span></span>      | <span data-ttu-id="172a0-166">Сбой установки из-за Error1.</span><span class="sxs-lookup"><span data-stu-id="172a0-166">Installation failure due to Error1.</span></span> |
| <span data-ttu-id="172a0-167">CAError2</span><span class="sxs-lookup"><span data-stu-id="172a0-167">CAError2</span></span>      | <span data-ttu-id="172a0-168">Сбой установки из-за Error2.</span><span class="sxs-lookup"><span data-stu-id="172a0-168">Installation failure due to Error2.</span></span> |
| <span data-ttu-id="172a0-169">CAError3</span><span class="sxs-lookup"><span data-stu-id="172a0-169">CAError3</span></span>      | <span data-ttu-id="172a0-170">Сбой установки из-за Error3.</span><span class="sxs-lookup"><span data-stu-id="172a0-170">Installation failure due to Error3.</span></span> |
| <span data-ttu-id="172a0-171">CAError4</span><span class="sxs-lookup"><span data-stu-id="172a0-171">CAError4</span></span>      | <span data-ttu-id="172a0-172">Сбой установки из-за Error4.</span><span class="sxs-lookup"><span data-stu-id="172a0-172">Installation failure due to Error4.</span></span> |



 

<span data-ttu-id="172a0-173">Обратите внимание, что поскольку порядок вычисления условий запуска не гарантируется путем создания [таблицы лаунчкондитион](launchcondition-table.md), для оценки условий в определенном порядке следует использовать настраиваемые действия типа 19.</span><span class="sxs-lookup"><span data-stu-id="172a0-173">Note that because the order of evaluation of launch conditions cannot be guaranteed by authoring the [LaunchCondition table](launchcondition-table.md), you should use Custom Action Type 19 custom actions in your installation to evaluate conditions in a specific order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="172a0-174">См. также</span><span class="sxs-lookup"><span data-stu-id="172a0-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="172a0-175">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="172a0-175">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



