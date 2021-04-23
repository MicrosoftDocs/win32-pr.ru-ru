---
description: Разработчики установщик Windowsных пакетов могут использовать настраиваемое действие типа 54, если стандартные действия недостаточны для выполнения установки.
ms.assetid: ab348a8e-f5df-4e03-a1b7-1ab1a7fbcb3b
title: Тип настраиваемого действия 54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623e8d4ffe955c73ef95a5948aa6e043702a35f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497871"
---
# <a name="custom-action-type-54"></a><span data-ttu-id="9400d-103">Тип настраиваемого действия 54</span><span class="sxs-lookup"><span data-stu-id="9400d-103">Custom Action Type 54</span></span>

<span data-ttu-id="9400d-104">Это настраиваемое действие написано на языке VBScript.</span><span class="sxs-lookup"><span data-stu-id="9400d-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="9400d-105">См. также [скрипты](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="9400d-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="9400d-106">Источник</span><span class="sxs-lookup"><span data-stu-id="9400d-106">Source</span></span>

<span data-ttu-id="9400d-107">Исходное поле [таблицы CustomAction](customaction-table.md) содержит имя свойства или ключ для [таблицы свойств](property-table.md) для свойства, содержащего текст скрипта.</span><span class="sxs-lookup"><span data-stu-id="9400d-107">The Source field of the [CustomAction table](customaction-table.md) contains a property name or a key to the [Property table](property-table.md) for a property containing the script text.</span></span>

## <a name="type-value"></a><span data-ttu-id="9400d-108">Значение типа</span><span class="sxs-lookup"><span data-stu-id="9400d-108">Type Value</span></span>

<span data-ttu-id="9400d-109">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип 32-разрядного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="9400d-109">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="9400d-110">Константы</span><span class="sxs-lookup"><span data-stu-id="9400d-110">Constants</span></span>                                                             | <span data-ttu-id="9400d-111">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="9400d-111">Hexadecimal</span></span> | <span data-ttu-id="9400d-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="9400d-112">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="9400d-113">**мсидбкустомактионтипевбскрипт**  +  **мсидбкустомактионтипепроперти**</span><span class="sxs-lookup"><span data-stu-id="9400d-113">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="9400d-114">0x036</span><span class="sxs-lookup"><span data-stu-id="9400d-114">0x036</span></span>       | <span data-ttu-id="9400d-115">54</span><span class="sxs-lookup"><span data-stu-id="9400d-115">54</span></span>      |



 

<span data-ttu-id="9400d-116">Установщик Windows могут использовать 64-разрядные пользовательские действия в 64-разрядных операционных системах.</span><span class="sxs-lookup"><span data-stu-id="9400d-116">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="9400d-117">64-разрядное пользовательское действие на основе скриптов должно включать бит **msidbCustomActionType64BitScript** в его числовой тип.</span><span class="sxs-lookup"><span data-stu-id="9400d-117">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="9400d-118">Дополнительные сведения см. в статье [64-разрядные пользовательские действия](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="9400d-118">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="9400d-119">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип 64-разрядного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="9400d-119">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="9400d-120">Константы</span><span class="sxs-lookup"><span data-stu-id="9400d-120">Constants</span></span>                                                                                                    | <span data-ttu-id="9400d-121">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="9400d-121">Hexadecimal</span></span> | <span data-ttu-id="9400d-122">Decimal</span><span class="sxs-lookup"><span data-stu-id="9400d-122">Decimal</span></span> |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="9400d-123">**мсидбкустомактионтипевбскрипт**  +  **мсидбкустомактионтипепроперти**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="9400d-123">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeProperty** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="9400d-124">0x0001036</span><span class="sxs-lookup"><span data-stu-id="9400d-124">0x0001036</span></span>   | <span data-ttu-id="9400d-125">4150</span><span class="sxs-lookup"><span data-stu-id="9400d-125">4150</span></span>    |



 

## <a name="target"></a><span data-ttu-id="9400d-126">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="9400d-126">Target</span></span>

<span data-ttu-id="9400d-127">Целевое поле [таблицы CustomAction](customaction-table.md) содержит необязательную функцию скрипта.</span><span class="sxs-lookup"><span data-stu-id="9400d-127">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="9400d-128">Сначала обработка отправляет скрипт для синтаксического анализа, а затем вызывает необязательную функцию скрипта.</span><span class="sxs-lookup"><span data-stu-id="9400d-128">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="9400d-129">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="9400d-129">Return Processing Options</span></span>

<span data-ttu-id="9400d-130">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры обработки возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="9400d-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="9400d-131">Описание параметров и значений см. в разделе [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="9400d-131">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="9400d-132">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="9400d-132">Execution Scheduling Options</span></span>

<span data-ttu-id="9400d-133">Включите дополнительные биты флагов в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры планирования выполнения.</span><span class="sxs-lookup"><span data-stu-id="9400d-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="9400d-134">Эти параметры управляют несколькими выполнениями пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="9400d-134">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="9400d-135">Описание параметров см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="9400d-135">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="9400d-136">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="9400d-136">In-Script Execution Options</span></span>

<span data-ttu-id="9400d-137">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметр выполнения в скрипте.</span><span class="sxs-lookup"><span data-stu-id="9400d-137">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="9400d-138">Эти параметры копируют код действия в скрипт выполнения, отката или фиксации.</span><span class="sxs-lookup"><span data-stu-id="9400d-138">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="9400d-139">Описание параметров см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="9400d-139">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="9400d-140">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9400d-140">Return Values</span></span>

<span data-ttu-id="9400d-141">Необязательные функции, написанные в скрипте, должны возвращать одно из значений, описанных в разделе [возвращаемые значения настраиваемых действий JScript и VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="9400d-141">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9400d-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9400d-142">Remarks</span></span>

<span data-ttu-id="9400d-143">Для пользовательского действия, написанного на JScript или VBScript, требуется объект [**сеанса**](session-object.md) установки.</span><span class="sxs-lookup"><span data-stu-id="9400d-143">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="9400d-144">Установщик присоединяет **объект сеанса** к скрипту с именем *Session*.</span><span class="sxs-lookup"><span data-stu-id="9400d-144">The installer attaches the **Session Object** to the script with the name *Session*.</span></span> <span data-ttu-id="9400d-145">Так как объект **сеанса** может не существовать во время отката установки, отложенное настраиваемое действие, написанное в скрипте, должно использовать один из методов или свойств объекта **Session** , описанный в разделе [Получение сведений о контексте для отложенного выполнения настраиваемых действий](obtaining-context-information-for-deferred-execution-custom-actions.md) для получения контекста.</span><span class="sxs-lookup"><span data-stu-id="9400d-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9400d-146">См. также</span><span class="sxs-lookup"><span data-stu-id="9400d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9400d-147">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="9400d-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



