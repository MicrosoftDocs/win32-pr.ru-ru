---
description: Разработчики установщик Windowsных пакетов могут использовать настраиваемое действие типа 38, если стандартные действия недостаточны для выполнения установки.
ms.assetid: bb50fcbf-3de5-4f5a-b799-cec5d68fdd9d
title: Тип настраиваемого действия 38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9372cd5035d27c02feaef3ed455ddeb756c449
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999026"
---
# <a name="custom-action-type-38"></a><span data-ttu-id="e896c-103">Тип настраиваемого действия 38</span><span class="sxs-lookup"><span data-stu-id="e896c-103">Custom Action Type 38</span></span>

<span data-ttu-id="e896c-104">Это настраиваемое действие написано на языке VBScript.</span><span class="sxs-lookup"><span data-stu-id="e896c-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="e896c-105">См. также [скрипты](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="e896c-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="e896c-106">Источник</span><span class="sxs-lookup"><span data-stu-id="e896c-106">Source</span></span>

<span data-ttu-id="e896c-107">Исходное поле [таблицы CustomAction](customaction-table.md) содержит значение null.</span><span class="sxs-lookup"><span data-stu-id="e896c-107">The Source field of the [CustomAction table](customaction-table.md) contains the null value.</span></span> <span data-ttu-id="e896c-108">Код скрипта для настраиваемого действия хранится в виде строки литерального текста скрипта в целевом поле.</span><span class="sxs-lookup"><span data-stu-id="e896c-108">The script code for the custom action is stored as a string of literal script text in the Target field.</span></span>

## <a name="type-value"></a><span data-ttu-id="e896c-109">Значение типа</span><span class="sxs-lookup"><span data-stu-id="e896c-109">Type Value</span></span>

<span data-ttu-id="e896c-110">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип 32-разрядного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="e896c-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="e896c-111">Константы</span><span class="sxs-lookup"><span data-stu-id="e896c-111">Constants</span></span>                                                              | <span data-ttu-id="e896c-112">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="e896c-112">Hexadecimal</span></span> | <span data-ttu-id="e896c-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="e896c-113">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="e896c-114">**мсидбкустомактионтипевбскрипт**  +  **мсидбкустомактионтипедиректори**</span><span class="sxs-lookup"><span data-stu-id="e896c-114">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="e896c-115">0x026</span><span class="sxs-lookup"><span data-stu-id="e896c-115">0x026</span></span>       | <span data-ttu-id="e896c-116">38</span><span class="sxs-lookup"><span data-stu-id="e896c-116">38</span></span>      |



 

<span data-ttu-id="e896c-117">Установщик Windows могут использовать 64-разрядные пользовательские действия в 64-разрядных операционных системах.</span><span class="sxs-lookup"><span data-stu-id="e896c-117">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="e896c-118">64-разрядное пользовательское действие на основе скриптов должно включать бит **msidbCustomActionType64BitScript** в его числовой тип.</span><span class="sxs-lookup"><span data-stu-id="e896c-118">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="e896c-119">Дополнительные сведения см. в статье [64-разрядные пользовательские действия](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="e896c-119">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="e896c-120">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип 64-разрядного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="e896c-120">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="e896c-121">Константы</span><span class="sxs-lookup"><span data-stu-id="e896c-121">Constants</span></span>                                                                                                     | <span data-ttu-id="e896c-122">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="e896c-122">Hexadecimal</span></span> | <span data-ttu-id="e896c-123">Decimal</span><span class="sxs-lookup"><span data-stu-id="e896c-123">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="e896c-124">**мсидбкустомактионтипевбскрипт**  +  **мсидбкустомактионтипедиректори**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="e896c-124">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeDirectory** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="e896c-125">0x0001026</span><span class="sxs-lookup"><span data-stu-id="e896c-125">0x0001026</span></span>   | <span data-ttu-id="e896c-126">4134</span><span class="sxs-lookup"><span data-stu-id="e896c-126">4134</span></span>    |



 

## <a name="target"></a><span data-ttu-id="e896c-127">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="e896c-127">Target</span></span>

<span data-ttu-id="e896c-128">Целевое поле [таблицы CustomAction](customaction-table.md) содержит код скрипта для настраиваемого действия в виде строки литерального текста скрипта.</span><span class="sxs-lookup"><span data-stu-id="e896c-128">The Target field of the [CustomAction table](customaction-table.md) contains the script code for the custom action as a string of literal script text.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="e896c-129">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="e896c-129">Return Processing Options</span></span>

<span data-ttu-id="e896c-130">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры обработки возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="e896c-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="e896c-131">Описание параметров и значений см. в разделе [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="e896c-131">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="e896c-132">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="e896c-132">Execution Scheduling Options</span></span>

<span data-ttu-id="e896c-133">Включите дополнительные биты флагов в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры планирования выполнения.</span><span class="sxs-lookup"><span data-stu-id="e896c-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="e896c-134">Эти параметры управляют несколькими выполнениями пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="e896c-134">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="e896c-135">Описание параметров см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="e896c-135">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="e896c-136">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="e896c-136">In-Script Execution Options</span></span>

<span data-ttu-id="e896c-137">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметр выполнения в скрипте.</span><span class="sxs-lookup"><span data-stu-id="e896c-137">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="e896c-138">Эти параметры копируют код действия в скрипт выполнения, отката или фиксации.</span><span class="sxs-lookup"><span data-stu-id="e896c-138">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="e896c-139">Описание параметров см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="e896c-139">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="e896c-140">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e896c-140">Return Values</span></span>

<span data-ttu-id="e896c-141">Этот тип настраиваемого действия всегда возвращает значение Success.</span><span class="sxs-lookup"><span data-stu-id="e896c-141">This custom action type always returns success.</span></span>

## <a name="remarks"></a><span data-ttu-id="e896c-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e896c-142">Remarks</span></span>

<span data-ttu-id="e896c-143">Для пользовательского действия, написанного на JScript или VBScript, требуется объект [**сеанса**](session-object.md) установки.</span><span class="sxs-lookup"><span data-stu-id="e896c-143">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="e896c-144">Установщик присоединяет **объект сеанса** к сценарию с именем Session.</span><span class="sxs-lookup"><span data-stu-id="e896c-144">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="e896c-145">Так как объект **сеанса** может не существовать во время отката установки, отложенное настраиваемое действие, написанное в скрипте, должно использовать один из методов или свойств объекта **Session** , описанный в разделе [Получение сведений о контексте для отложенного выполнения настраиваемых действий](obtaining-context-information-for-deferred-execution-custom-actions.md) для получения контекста.</span><span class="sxs-lookup"><span data-stu-id="e896c-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e896c-146">См. также</span><span class="sxs-lookup"><span data-stu-id="e896c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e896c-147">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="e896c-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



