---
description: Разработчики установщик Windowsных пакетов могут использовать тип настраиваемого действия 21, если стандартные действия недостаточны для выполнения установки.
ms.assetid: 0b28ad22-4e3a-49f2-8eed-2341a91eb67c
title: Тип настраиваемого действия 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5bb7482c2f7c7b6cbd85af7a6f01cc83edbb89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348995"
---
# <a name="custom-action-type-21"></a><span data-ttu-id="3b9f8-103">Тип настраиваемого действия 21</span><span class="sxs-lookup"><span data-stu-id="3b9f8-103">Custom Action Type 21</span></span>

<span data-ttu-id="3b9f8-104">Это пользовательское действие написано на языке JScript, например ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="3b9f8-105">Установщик Windows не поддерживает JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="3b9f8-106">Дополнительные сведения см. в разделе [сценарии](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="3b9f8-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="3b9f8-107">Источник</span><span class="sxs-lookup"><span data-stu-id="3b9f8-107">Source</span></span>

<span data-ttu-id="3b9f8-108">Скрипт устанавливается вместе с приложением во время текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-108">The script is installed with the application during the current session.</span></span> <span data-ttu-id="3b9f8-109">Исходное поле [таблицы CustomAction](customaction-table.md) содержит ключ к [таблице File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="3b9f8-109">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="3b9f8-110">Расположение кода настраиваемого действия определяется разрешением целевого пути для этого файла; Поэтому это настраиваемое действие должно быть вызвано после установки файла и перед его удалением.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-110">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="3b9f8-111">Значение типа</span><span class="sxs-lookup"><span data-stu-id="3b9f8-111">Type Value</span></span>

<span data-ttu-id="3b9f8-112">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип 32-разрядного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-112">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="3b9f8-113">Константы</span><span class="sxs-lookup"><span data-stu-id="3b9f8-113">Constants</span></span>                                                              | <span data-ttu-id="3b9f8-114">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="3b9f8-114">Hexadecimal</span></span> | <span data-ttu-id="3b9f8-115">Decimal</span><span class="sxs-lookup"><span data-stu-id="3b9f8-115">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="3b9f8-116">**мсидбкустомактионтипежскрипт**  +  **мсидбкустомактионтипесаурцефиле**</span><span class="sxs-lookup"><span data-stu-id="3b9f8-116">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="3b9f8-117">0x015</span><span class="sxs-lookup"><span data-stu-id="3b9f8-117">0x015</span></span>       | <span data-ttu-id="3b9f8-118">21</span><span class="sxs-lookup"><span data-stu-id="3b9f8-118">21</span></span>      |



 

<span data-ttu-id="3b9f8-119">Установщик Windows могут использовать [64-разрядные пользовательские действия](64-bit-custom-actions.md) в 64-разрядных операционных системах.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-119">Windows Installer may use [64-bit Custom Actions](64-bit-custom-actions.md) on 64-bit operating systems.</span></span> <span data-ttu-id="3b9f8-120">64-разрядное пользовательское действие на основе скриптов должно включать бит **msidbCustomActionType64BitScript** в его числовой тип.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-120">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="3b9f8-121">Дополнительные сведения см. в статье 64-разрядные пользовательские действия.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-121">For information see 64-bit Custom Actions.</span></span> <span data-ttu-id="3b9f8-122">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип 64-разрядного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-122">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="3b9f8-123">Константы</span><span class="sxs-lookup"><span data-stu-id="3b9f8-123">Constants</span></span>                                                                                                     | <span data-ttu-id="3b9f8-124">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="3b9f8-124">Hexadecimal</span></span> | <span data-ttu-id="3b9f8-125">Decimal</span><span class="sxs-lookup"><span data-stu-id="3b9f8-125">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="3b9f8-126">**мсидбкустомактионтипежскрипт**  +  **мсидбкустомактионтипесаурцефиле**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="3b9f8-126">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeSourceFile** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="3b9f8-127">0x0001015</span><span class="sxs-lookup"><span data-stu-id="3b9f8-127">0x0001015</span></span>   | <span data-ttu-id="3b9f8-128">4117</span><span class="sxs-lookup"><span data-stu-id="3b9f8-128">4117</span></span>    |



 

## <a name="target"></a><span data-ttu-id="3b9f8-129">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3b9f8-129">Target</span></span>

<span data-ttu-id="3b9f8-130">Целевое поле [таблицы CustomAction](customaction-table.md) содержит необязательную функцию скрипта.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-130">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="3b9f8-131">Сначала обработка отправляет скрипт для синтаксического анализа, а затем вызывает необязательную функцию скрипта.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-131">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="3b9f8-132">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="3b9f8-132">Return Processing Options</span></span>

<span data-ttu-id="3b9f8-133">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры обработки возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="3b9f8-134">Описание параметров и значений см. в разделе [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="3b9f8-134">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="3b9f8-135">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="3b9f8-135">Execution Scheduling Options</span></span>

<span data-ttu-id="3b9f8-136">Включите дополнительные биты флагов в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры планирования выполнения.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-136">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="3b9f8-137">Эти параметры управляют несколькими выполнениями пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-137">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="3b9f8-138">Описание параметров см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="3b9f8-138">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="3b9f8-139">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="3b9f8-139">In-Script Execution Options</span></span>

<span data-ttu-id="3b9f8-140">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметр выполнения в скрипте.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-140">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="3b9f8-141">Эти параметры копируют код действия в скрипт выполнения, отката или фиксации.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-141">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="3b9f8-142">Описание параметров см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="3b9f8-142">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="3b9f8-143">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3b9f8-143">Return Values</span></span>

<span data-ttu-id="3b9f8-144">Необязательные функции, написанные в скрипте, должны возвращать одно из значений, описанных в разделе [возвращаемые значения настраиваемых действий JScript и VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="3b9f8-144">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3b9f8-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b9f8-145">Remarks</span></span>

<span data-ttu-id="3b9f8-146">Для пользовательского действия, написанного на JScript или VBScript, требуется объект [**сеанса**](session-object.md) установки.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-146">A custom action that is written in JScript or VBScript requires the installation [**Session**](session-object.md) object.</span></span> <span data-ttu-id="3b9f8-147">Установщик присоединяет **объект сеанса** к сценарию с именем Session.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-147">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="3b9f8-148">Так как объект **сеанса** может не существовать во время отката установки, отложенное настраиваемое действие, написанное в скрипте, должно использовать один из методов или свойств объекта **Session** , описанный в разделе [Получение сведений о контексте для отложенного выполнения настраиваемых действий](obtaining-context-information-for-deferred-execution-custom-actions.md) для получения контекста.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-148">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="3b9f8-149">Настраиваемые действия, которые ссылаются на установленный файл в качестве источника, например тип настраиваемого действия 21 (JScript), должны соответствовать следующим ограничениям последовательности.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-149">Custom actions that reference an installed file as their source, such as Custom Action Type 21 (JScript), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="3b9f8-150">Настраиваемое действие должно быть упорядочено после [действия костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="3b9f8-150">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="3b9f8-151">Это необходимо для того, чтобы пользовательское действие могло разрешить путь, необходимый для поиска исходного файла, содержащего JScript.</span><span class="sxs-lookup"><span data-stu-id="3b9f8-151">This is so that the custom action can resolve the path needed to locate the source file containing the JScript.</span></span>
-   <span data-ttu-id="3b9f8-152">Если исходный файл еще не установлен на компьютере, отложенные (в скрипте) настраиваемые действия этого типа должны быть упорядочены после [действия инсталлфилес](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="3b9f8-152">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="3b9f8-153">Если исходный файл еще не установлен на компьютере, неотложенные настраиваемые действия этого типа должны быть упорядочены после [действия функции InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="3b9f8-153">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b9f8-154">См. также</span><span class="sxs-lookup"><span data-stu-id="3b9f8-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b9f8-155">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="3b9f8-155">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



