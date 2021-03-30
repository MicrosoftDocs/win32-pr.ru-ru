---
description: Разработчики установщик Windowsных пакетов могут использовать настраиваемое действие типа 53, если стандартные действия недостаточны для выполнения установки.
ms.assetid: d024c73e-c2dc-4187-a8ae-ed96dc7c107e
title: Тип настраиваемого действия 53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a016d3b3f5a282567b909215d6ab7b32759417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998826"
---
# <a name="custom-action-type-53"></a><span data-ttu-id="998ba-103">Тип настраиваемого действия 53</span><span class="sxs-lookup"><span data-stu-id="998ba-103">Custom Action Type 53</span></span>

<span data-ttu-id="998ba-104">Это пользовательское действие написано на языке JScript, например ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="998ba-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="998ba-105">Установщик Windows не поддерживает JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="998ba-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="998ba-106">Дополнительные сведения см. в разделе [сценарии](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="998ba-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="998ba-107">Источник</span><span class="sxs-lookup"><span data-stu-id="998ba-107">Source</span></span>

<span data-ttu-id="998ba-108">Исходное поле [таблицы CustomAction](customaction-table.md) содержит имя свойства или ключ для [таблицы свойств](property-table.md) для свойства, содержащего текст скрипта.</span><span class="sxs-lookup"><span data-stu-id="998ba-108">The Source field of the [CustomAction table](customaction-table.md) contains a property name or a key to the [Property table](property-table.md) for a property containing the script text.</span></span>

## <a name="type-value"></a><span data-ttu-id="998ba-109">Значение типа</span><span class="sxs-lookup"><span data-stu-id="998ba-109">Type Value</span></span>

<span data-ttu-id="998ba-110">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип 32-разрядного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="998ba-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="998ba-111">Константы</span><span class="sxs-lookup"><span data-stu-id="998ba-111">Constants</span></span>                                                            | <span data-ttu-id="998ba-112">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="998ba-112">Hexadecimal</span></span> | <span data-ttu-id="998ba-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="998ba-113">Decimal</span></span> |
|----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="998ba-114">**мсидбкустомактионтипежскрипт**  +  **мсидбкустомактионтипепроперти**</span><span class="sxs-lookup"><span data-stu-id="998ba-114">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="998ba-115">0x035</span><span class="sxs-lookup"><span data-stu-id="998ba-115">0x035</span></span>       | <span data-ttu-id="998ba-116">53</span><span class="sxs-lookup"><span data-stu-id="998ba-116">53</span></span>      |



 

<span data-ttu-id="998ba-117">Установщик Windows могут использовать 64-разрядные пользовательские действия в 64-разрядных операционных системах.</span><span class="sxs-lookup"><span data-stu-id="998ba-117">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="998ba-118">64-разрядное пользовательское действие на основе скриптов должно включать бит **msidbCustomActionType64BitScript** в его числовой тип.</span><span class="sxs-lookup"><span data-stu-id="998ba-118">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="998ba-119">Дополнительные сведения см. в статье [64-разрядные пользовательские действия](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="998ba-119">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="998ba-120">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип 64-разрядного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="998ba-120">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="998ba-121">Константы</span><span class="sxs-lookup"><span data-stu-id="998ba-121">Constants</span></span>                                                                                                   | <span data-ttu-id="998ba-122">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="998ba-122">Hexadecimal</span></span> | <span data-ttu-id="998ba-123">Decimal</span><span class="sxs-lookup"><span data-stu-id="998ba-123">Decimal</span></span> |
|-------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="998ba-124">**мсидбкустомактионтипежскрипт**  +  **мсидбкустомактионтипепроперти**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="998ba-124">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeProperty** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="998ba-125">0x0001035</span><span class="sxs-lookup"><span data-stu-id="998ba-125">0x0001035</span></span>   | <span data-ttu-id="998ba-126">4149</span><span class="sxs-lookup"><span data-stu-id="998ba-126">4149</span></span>    |



 

## <a name="target"></a><span data-ttu-id="998ba-127">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="998ba-127">Target</span></span>

<span data-ttu-id="998ba-128">Целевое поле [таблицы CustomAction](customaction-table.md) содержит необязательную функцию скрипта.</span><span class="sxs-lookup"><span data-stu-id="998ba-128">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="998ba-129">Сначала обработка отправляет скрипт для синтаксического анализа, а затем вызывает необязательную функцию скрипта.</span><span class="sxs-lookup"><span data-stu-id="998ba-129">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="998ba-130">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="998ba-130">Return Processing Options</span></span>

<span data-ttu-id="998ba-131">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры обработки возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="998ba-131">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="998ba-132">Описание параметров и значений см. в разделе [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="998ba-132">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="998ba-133">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="998ba-133">Execution Scheduling Options</span></span>

<span data-ttu-id="998ba-134">Включите дополнительные биты флагов в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры планирования выполнения.</span><span class="sxs-lookup"><span data-stu-id="998ba-134">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="998ba-135">Эти параметры управляют несколькими выполнениями пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="998ba-135">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="998ba-136">Описание параметров см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="998ba-136">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="998ba-137">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="998ba-137">In-Script Execution Options</span></span>

<span data-ttu-id="998ba-138">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметр выполнения в скрипте.</span><span class="sxs-lookup"><span data-stu-id="998ba-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="998ba-139">Эти параметры копируют код действия в скрипт выполнения, отката или фиксации.</span><span class="sxs-lookup"><span data-stu-id="998ba-139">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="998ba-140">Описание параметров см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="998ba-140">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="998ba-141">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="998ba-141">Return Values</span></span>

<span data-ttu-id="998ba-142">Необязательные функции, написанные в скрипте, должны возвращать одно из значений, описанных в разделе [возвращаемые значения настраиваемых действий JScript и VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="998ba-142">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="998ba-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="998ba-143">Remarks</span></span>

<span data-ttu-id="998ba-144">Для пользовательского действия, написанного на языке JScript, требуется объект [**сеанса**](session-object.md) установки.</span><span class="sxs-lookup"><span data-stu-id="998ba-144">A custom action that is written in JScript requires the installation [**Session**](session-object.md) object.</span></span> <span data-ttu-id="998ba-145">Так как объект **сеанса** может не существовать во время отката установки, отложенное настраиваемое действие, написанное в скрипте, использует один из методов, описанных в разделе [Получение сведений о контексте для отложенного выполнения настраиваемых действий](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="998ba-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script uses one of the methods described in [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="998ba-146">См. также</span><span class="sxs-lookup"><span data-stu-id="998ba-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="998ba-147">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="998ba-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



