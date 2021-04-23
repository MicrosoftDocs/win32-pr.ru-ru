---
description: Разработчики установщик Windowsных пакетов могут использовать настраиваемое действие типа 18, если стандартные действия недостаточны для выполнения установки.
ms.assetid: 8a7311a6-41c6-431e-982d-60bacf06454e
title: Тип настраиваемого действия 18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a669fe3caa532b3a365f1056ca2b36f490ab95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999472"
---
# <a name="custom-action-type-18"></a><span data-ttu-id="28ec3-103">Тип настраиваемого действия 18</span><span class="sxs-lookup"><span data-stu-id="28ec3-103">Custom Action Type 18</span></span>

<span data-ttu-id="28ec3-104">Это пользовательское действие вызывает исполняемый файл, запущенный с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="28ec3-104">This custom action calls an executable launched with a command line.</span></span>

## <a name="source"></a><span data-ttu-id="28ec3-105">Источник</span><span class="sxs-lookup"><span data-stu-id="28ec3-105">Source</span></span>

<span data-ttu-id="28ec3-106">Исполняемый файл создается из файла, установленного вместе с приложением.</span><span class="sxs-lookup"><span data-stu-id="28ec3-106">The executable is generated from a file installed with the application.</span></span> <span data-ttu-id="28ec3-107">Исходное поле [таблицы CustomAction](customaction-table.md) содержит ключ к [таблице File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="28ec3-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="28ec3-108">Расположение кода настраиваемого действия определяется разрешением целевого пути для этого файла; Поэтому это настраиваемое действие должно быть вызвано после установки файла и перед его удалением.</span><span class="sxs-lookup"><span data-stu-id="28ec3-108">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="28ec3-109">Значение типа</span><span class="sxs-lookup"><span data-stu-id="28ec3-109">Type Value</span></span>

<span data-ttu-id="28ec3-110">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип.</span><span class="sxs-lookup"><span data-stu-id="28ec3-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="28ec3-111">Константы</span><span class="sxs-lookup"><span data-stu-id="28ec3-111">Constants</span></span>                                                          | <span data-ttu-id="28ec3-112">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="28ec3-112">Hexadecimal</span></span> | <span data-ttu-id="28ec3-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="28ec3-113">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="28ec3-114">**мсидбкустомактионтипиксе**  +  **мсидбкустомактионтипесаурцефиле**</span><span class="sxs-lookup"><span data-stu-id="28ec3-114">**msidbCustomActionTypeExe** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="28ec3-115">0x012</span><span class="sxs-lookup"><span data-stu-id="28ec3-115">0x012</span></span>       | <span data-ttu-id="28ec3-116">18</span><span class="sxs-lookup"><span data-stu-id="28ec3-116">18</span></span>      |



 

## <a name="target"></a><span data-ttu-id="28ec3-117">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="28ec3-117">Target</span></span>

<span data-ttu-id="28ec3-118">Целевой столбец [таблицы CustomAction](customaction-table.md) содержит строку командной строки для исполняемого файла, указанного в исходном столбце.</span><span class="sxs-lookup"><span data-stu-id="28ec3-118">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable identified in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="28ec3-119">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="28ec3-119">Return Processing Options</span></span>

<span data-ttu-id="28ec3-120">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры обработки возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="28ec3-120">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="28ec3-121">Описание параметров и значений см. в разделе [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="28ec3-121">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="28ec3-122">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="28ec3-122">Execution Scheduling Options</span></span>

<span data-ttu-id="28ec3-123">Включите дополнительные биты флагов в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры планирования выполнения.</span><span class="sxs-lookup"><span data-stu-id="28ec3-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="28ec3-124">Эти параметры управляют несколькими выполнениями пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="28ec3-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="28ec3-125">Описание параметров см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="28ec3-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="28ec3-126">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="28ec3-126">In-Script Execution Options</span></span>

<span data-ttu-id="28ec3-127">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметр выполнения в скрипте.</span><span class="sxs-lookup"><span data-stu-id="28ec3-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="28ec3-128">Эти параметры копируют код действия в скрипт выполнения, отката или фиксации.</span><span class="sxs-lookup"><span data-stu-id="28ec3-128">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="28ec3-129">Описание параметров см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="28ec3-129">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="28ec3-130">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="28ec3-130">Return Values</span></span>

<span data-ttu-id="28ec3-131">Настраиваемые действия, являющиеся [исполняемыми файлами](executable-files.md) , должны возвращать значение 0 для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="28ec3-131">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="28ec3-132">Установщик интерпретирует любое другое возвращаемое значение как сбой.</span><span class="sxs-lookup"><span data-stu-id="28ec3-132">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="28ec3-133">Чтобы игнорировать возвращаемые значения, установите флаг битов **мсидбкустомактионтипеконтинуе** в поле Тип таблицы CustomAction.</span><span class="sxs-lookup"><span data-stu-id="28ec3-133">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="28ec3-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28ec3-134">Remarks</span></span>

<span data-ttu-id="28ec3-135">Пользовательское действие, запускающее исполняемый файл, принимает командную строку, которая обычно содержит свойства, которые определены динамически.</span><span class="sxs-lookup"><span data-stu-id="28ec3-135">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="28ec3-136">Если это также [Отложенное настраиваемое действие выполнения](deferred-execution-custom-actions.md), установщик использует [**параметр CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) или [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) для создания процесса при вызове настраиваемого действия из скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="28ec3-136">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

<span data-ttu-id="28ec3-137">Настраиваемые действия, которые ссылаются на установленный файл в качестве источника, например тип настраиваемого действия 18 (EXE), должны соответствовать следующим ограничениям последовательности.</span><span class="sxs-lookup"><span data-stu-id="28ec3-137">Custom actions that reference an installed file as their source, such as Custom Action Type 18 (EXE), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="28ec3-138">Настраиваемое действие должно быть упорядочено после [действия костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="28ec3-138">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="28ec3-139">Это необходимо для того, чтобы пользовательское действие могло разрешить путь, необходимый для поиска EXE-файла.</span><span class="sxs-lookup"><span data-stu-id="28ec3-139">This is so that the custom action can resolve the path needed to locate the EXE.</span></span>
-   <span data-ttu-id="28ec3-140">Если исходный файл еще не установлен на компьютере, отложенные (в скрипте) настраиваемые действия этого типа должны быть упорядочены после [действия инсталлфилес](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="28ec3-140">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="28ec3-141">Если исходный файл еще не установлен на компьютере, неотложенные настраиваемые действия этого типа должны быть упорядочены после [действия функции InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="28ec3-141">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28ec3-142">См. также</span><span class="sxs-lookup"><span data-stu-id="28ec3-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28ec3-143">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="28ec3-143">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="28ec3-144">Исполняемые файлы</span><span class="sxs-lookup"><span data-stu-id="28ec3-144">Executable Files</span></span>](executable-files.md)
</dt> </dl>

 

 
