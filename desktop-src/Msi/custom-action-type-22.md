---
description: Разработчики установщик Windowsных пакетов могут использовать тип настраиваемого действия 22, если стандартные действия недостаточны для выполнения установки.
ms.assetid: 6838f59b-e1bc-42c6-a7fe-3d32791adfac
title: Тип настраиваемого действия 22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00b4772b1d2532c0291223cc5c4b6a63ead9324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350632"
---
# <a name="custom-action-type-22"></a><span data-ttu-id="3d8ad-103">Тип настраиваемого действия 22</span><span class="sxs-lookup"><span data-stu-id="3d8ad-103">Custom Action Type 22</span></span>

<span data-ttu-id="3d8ad-104">Это настраиваемое действие написано на языке VBScript.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="3d8ad-105">См. также [скрипты](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="3d8ad-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="3d8ad-106">Источник</span><span class="sxs-lookup"><span data-stu-id="3d8ad-106">Source</span></span>

<span data-ttu-id="3d8ad-107">Скрипт устанавливается вместе с приложением во время текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-107">The script is installed with the application during the current session.</span></span> <span data-ttu-id="3d8ad-108">Исходное поле [таблицы CustomAction](customaction-table.md) содержит ключ к [таблице File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="3d8ad-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="3d8ad-109">Расположение кода настраиваемого действия определяется разрешением целевого пути для этого файла; Поэтому это настраиваемое действие должно быть вызвано после установки файла и перед его удалением.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-109">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="3d8ad-110">Значение типа</span><span class="sxs-lookup"><span data-stu-id="3d8ad-110">Type Value</span></span>

<span data-ttu-id="3d8ad-111">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип 32-разрядного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-111">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="3d8ad-112">Константы</span><span class="sxs-lookup"><span data-stu-id="3d8ad-112">Constants</span></span>                                                               | <span data-ttu-id="3d8ad-113">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="3d8ad-113">Hexadecimal</span></span> | <span data-ttu-id="3d8ad-114">Decimal</span><span class="sxs-lookup"><span data-stu-id="3d8ad-114">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="3d8ad-115">**мсидбкустомактионтипевбскрипт**  +  **мсидбкустомактионтипесаурцефиле**</span><span class="sxs-lookup"><span data-stu-id="3d8ad-115">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="3d8ad-116">0x016</span><span class="sxs-lookup"><span data-stu-id="3d8ad-116">0x016</span></span>       | <span data-ttu-id="3d8ad-117">22</span><span class="sxs-lookup"><span data-stu-id="3d8ad-117">22</span></span>      |



 

<span data-ttu-id="3d8ad-118">Установщик Windows могут использовать 64-разрядные пользовательские действия в 64-разрядных операционных системах.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-118">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="3d8ad-119">64-разрядное пользовательское действие на основе скриптов должно включать бит **msidbCustomActionType64BitScript** в его числовой тип.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-119">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="3d8ad-120">Дополнительные сведения см. в статье [64-разрядные пользовательские действия](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="3d8ad-120">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="3d8ad-121">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип 64-разрядного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-121">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="3d8ad-122">Константы</span><span class="sxs-lookup"><span data-stu-id="3d8ad-122">Constants</span></span>                                                                                                      | <span data-ttu-id="3d8ad-123">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="3d8ad-123">Hexadecimal</span></span> | <span data-ttu-id="3d8ad-124">Decimal</span><span class="sxs-lookup"><span data-stu-id="3d8ad-124">Decimal</span></span> |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="3d8ad-125">**мсидбкустомактионтипевбскрипт**  +  **мсидбкустомактионтипесаурцефиле**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="3d8ad-125">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeSourceFile** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="3d8ad-126">0x0001016</span><span class="sxs-lookup"><span data-stu-id="3d8ad-126">0x0001016</span></span>   | <span data-ttu-id="3d8ad-127">4118</span><span class="sxs-lookup"><span data-stu-id="3d8ad-127">4118</span></span>    |



 

## <a name="target"></a><span data-ttu-id="3d8ad-128">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="3d8ad-128">Target</span></span>

<span data-ttu-id="3d8ad-129">Целевое поле [таблицы CustomAction](customaction-table.md) содержит необязательную функцию скрипта.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-129">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="3d8ad-130">Сначала обработка отправляет скрипт для синтаксического анализа, а затем вызывает необязательную функцию скрипта.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-130">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="3d8ad-131">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="3d8ad-131">Return Processing Options</span></span>

<span data-ttu-id="3d8ad-132">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры обработки возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-132">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="3d8ad-133">Описание параметров и значений см. в разделе [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="3d8ad-133">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="3d8ad-134">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="3d8ad-134">Execution Scheduling Options</span></span>

<span data-ttu-id="3d8ad-135">Включите дополнительные биты флагов в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры планирования выполнения.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-135">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="3d8ad-136">Эти параметры управляют несколькими выполнениями пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-136">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="3d8ad-137">Описание параметров см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="3d8ad-137">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="3d8ad-138">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="3d8ad-138">In-Script Execution Options</span></span>

<span data-ttu-id="3d8ad-139">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметр выполнения в скрипте.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-139">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="3d8ad-140">Эти параметры копируют код действия в скрипт выполнения, отката или фиксации.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-140">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="3d8ad-141">Описание параметров см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="3d8ad-141">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="3d8ad-142">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3d8ad-142">Return Values</span></span>

<span data-ttu-id="3d8ad-143">Необязательные функции, написанные в скрипте, должны возвращать одно из значений, описанных в разделе [возвращаемые значения настраиваемых действий JScript и VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="3d8ad-143">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3d8ad-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d8ad-144">Remarks</span></span>

<span data-ttu-id="3d8ad-145">Для пользовательского действия, написанного на JScript или VBScript, требуется [**объект сеанса**](session-object.md)установки.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-145">A custom action that is written in JScript or VBScript requires the install [**Session Object**](session-object.md).</span></span> <span data-ttu-id="3d8ad-146">Это относится к объекту типа **Session** , а Установщик прикрепляет его к сценарию с именем Session.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-146">This is of the type **Session Object** and the installer attaches it to the script with the name "Session".</span></span> <span data-ttu-id="3d8ad-147">Так как объект **сеанса** может не существовать во время отката установки, отложенное настраиваемое действие, написанное в скрипте, должно использовать один из методов или свойств объекта **Session** , описанный в разделе [Получение сведений о контексте для отложенного выполнения настраиваемых действий](obtaining-context-information-for-deferred-execution-custom-actions.md) для получения контекста.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-147">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="3d8ad-148">Настраиваемые действия, которые ссылаются на установленный файл в качестве источника, например тип настраиваемого действия 22 (Вбкрипт), должны соответствовать следующим ограничениям последовательности.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-148">Custom actions that reference an installed file as their source, such as Custom Action Type 22 (VBcript), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="3d8ad-149">Настраиваемое действие должно быть упорядочено после [действия костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="3d8ad-149">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="3d8ad-150">Это необходимо для того, чтобы пользовательское действие могло разрешить путь, необходимый для поиска исходного файла, содержащего сценарий VBScript.</span><span class="sxs-lookup"><span data-stu-id="3d8ad-150">This is so that the custom action can resolve the path needed to locate the source file containing the VBScript.</span></span>
-   <span data-ttu-id="3d8ad-151">Если исходный файл еще не установлен на компьютере, отложенные (в скрипте) настраиваемые действия этого типа должны быть упорядочены после [действия инсталлфилес](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="3d8ad-151">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="3d8ad-152">Если исходный файл еще не установлен на компьютере, неотложенные настраиваемые действия этого типа должны быть упорядочены после [действия функции InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="3d8ad-152">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d8ad-153">См. также</span><span class="sxs-lookup"><span data-stu-id="3d8ad-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d8ad-154">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="3d8ad-154">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



