---
description: Разработчики установщик Windowsных пакетов могут использовать настраиваемое действие типа 37, если стандартные действия недостаточны для выполнения установки.
ms.assetid: 1c1e4f4f-1ccb-444c-940a-a1963d97714d
title: Тип настраиваемого действия 37
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30a42d4837af6fe2878f33624251d9c06550855b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081234"
---
# <a name="custom-action-type-37"></a><span data-ttu-id="16c04-103">Тип настраиваемого действия 37</span><span class="sxs-lookup"><span data-stu-id="16c04-103">Custom Action Type 37</span></span>

<span data-ttu-id="16c04-104">Это пользовательское действие написано на языке JScript, например ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="16c04-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="16c04-105">Установщик Windows не поддерживает JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="16c04-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="16c04-106">Дополнительные сведения см. в разделе [сценарии](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="16c04-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="16c04-107">Источник</span><span class="sxs-lookup"><span data-stu-id="16c04-107">Source</span></span>

<span data-ttu-id="16c04-108">Исходное поле [таблицы CustomAction](customaction-table.md) содержит значение null.</span><span class="sxs-lookup"><span data-stu-id="16c04-108">The Source field of the [CustomAction table](customaction-table.md) contains the null value.</span></span> <span data-ttu-id="16c04-109">Код скрипта для настраиваемого действия хранится в виде строки литерального текста скрипта в целевом поле.</span><span class="sxs-lookup"><span data-stu-id="16c04-109">The script code for the custom action is stored as a string of literal script text in the Target field.</span></span>

## <a name="type-value"></a><span data-ttu-id="16c04-110">Значение типа</span><span class="sxs-lookup"><span data-stu-id="16c04-110">Type Value</span></span>

<span data-ttu-id="16c04-111">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип 32-разрядного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="16c04-111">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="16c04-112">Константы</span><span class="sxs-lookup"><span data-stu-id="16c04-112">Constants</span></span>                                                             | <span data-ttu-id="16c04-113">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="16c04-113">Hexadecimal</span></span> | <span data-ttu-id="16c04-114">Decimal</span><span class="sxs-lookup"><span data-stu-id="16c04-114">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="16c04-115">**мсидбкустомактионтипежскрипт**  +  **мсидбкустомактионтипедиректори**</span><span class="sxs-lookup"><span data-stu-id="16c04-115">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="16c04-116">0x025</span><span class="sxs-lookup"><span data-stu-id="16c04-116">0x025</span></span>       | <span data-ttu-id="16c04-117">37</span><span class="sxs-lookup"><span data-stu-id="16c04-117">37</span></span>      |



 

<span data-ttu-id="16c04-118">Установщик Windows могут использовать 64-разрядные пользовательские действия в 64-разрядных операционных системах.</span><span class="sxs-lookup"><span data-stu-id="16c04-118">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="16c04-119">64-разрядное пользовательское действие на основе скриптов должно включать бит **msidbCustomActionType64BitScript** в его числовой тип.</span><span class="sxs-lookup"><span data-stu-id="16c04-119">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="16c04-120">Дополнительные сведения см. в статье [64-разрядные пользовательские действия](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="16c04-120">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="16c04-121">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип 64-разрядного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="16c04-121">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="16c04-122">Константы</span><span class="sxs-lookup"><span data-stu-id="16c04-122">Constants</span></span>                                                                                                    | <span data-ttu-id="16c04-123">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="16c04-123">Hexadecimal</span></span> | <span data-ttu-id="16c04-124">Decimal</span><span class="sxs-lookup"><span data-stu-id="16c04-124">Decimal</span></span> |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="16c04-125">**мсидбкустомактионтипежскрипт**  +  **мсидбкустомактионтипедиректори**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="16c04-125">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeDirectory** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="16c04-126">0x0001025</span><span class="sxs-lookup"><span data-stu-id="16c04-126">0x0001025</span></span>   | <span data-ttu-id="16c04-127">4133</span><span class="sxs-lookup"><span data-stu-id="16c04-127">4133</span></span>    |



 

## <a name="target"></a><span data-ttu-id="16c04-128">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="16c04-128">Target</span></span>

<span data-ttu-id="16c04-129">Целевое поле [таблицы CustomAction](customaction-table.md) содержит код скрипта для настраиваемого действия в виде строки литерального текста скрипта.</span><span class="sxs-lookup"><span data-stu-id="16c04-129">The Target field of the [CustomAction table](customaction-table.md) contains the script code for the custom action as a string of literal script text.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="16c04-130">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="16c04-130">Return Processing Options</span></span>

<span data-ttu-id="16c04-131">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры обработки возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="16c04-131">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="16c04-132">Описание параметров и значений см. в разделе [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="16c04-132">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="16c04-133">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="16c04-133">Execution Scheduling Options</span></span>

<span data-ttu-id="16c04-134">Включите дополнительные биты флагов в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры планирования выполнения.</span><span class="sxs-lookup"><span data-stu-id="16c04-134">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="16c04-135">Эти параметры управляют несколькими выполнениями пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="16c04-135">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="16c04-136">Описание параметров см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="16c04-136">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="16c04-137">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="16c04-137">In-Script Execution Options</span></span>

<span data-ttu-id="16c04-138">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметр выполнения в скрипте.</span><span class="sxs-lookup"><span data-stu-id="16c04-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="16c04-139">Эти параметры копируют код действия в скрипт выполнения, отката или фиксации.</span><span class="sxs-lookup"><span data-stu-id="16c04-139">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="16c04-140">Описание параметров см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="16c04-140">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="16c04-141">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="16c04-141">Return Values</span></span>

<span data-ttu-id="16c04-142">Этот тип настраиваемого действия всегда возвращает значение Success.</span><span class="sxs-lookup"><span data-stu-id="16c04-142">This custom action type always returns success.</span></span>

## <a name="remarks"></a><span data-ttu-id="16c04-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16c04-143">Remarks</span></span>

<span data-ttu-id="16c04-144">Для пользовательского действия, написанного на JScript или VBScript, требуется объект [**сеанса**](session-object.md) установки.</span><span class="sxs-lookup"><span data-stu-id="16c04-144">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="16c04-145">Установщик присоединяет **объект сеанса** к сценарию с именем Session.</span><span class="sxs-lookup"><span data-stu-id="16c04-145">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="16c04-146">Так как объект **сеанса** может не существовать во время отката установки, отложенное настраиваемое действие, написанное в скрипте, должно использовать один из методов или свойств объекта **Session** , описанный в разделе [Получение сведений о контексте для отложенного выполнения настраиваемых действий](obtaining-context-information-for-deferred-execution-custom-actions.md) для получения контекста.</span><span class="sxs-lookup"><span data-stu-id="16c04-146">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16c04-147">См. также</span><span class="sxs-lookup"><span data-stu-id="16c04-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16c04-148">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="16c04-148">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



