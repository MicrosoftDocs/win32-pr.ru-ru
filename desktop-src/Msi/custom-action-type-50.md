---
description: Разработчики установщик Windowsных пакетов могут использовать настраиваемое действие типа 50, если стандартные действия недостаточны для выполнения установки.
ms.assetid: fc8a875d-21e3-452a-8455-80835b52b256
title: Тип настраиваемого действия 50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5f3a80de730eb727c40c871070ab9e5b2470f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651036"
---
# <a name="custom-action-type-50"></a><span data-ttu-id="afdb0-103">Тип настраиваемого действия 50</span><span class="sxs-lookup"><span data-stu-id="afdb0-103">Custom Action Type 50</span></span>

<span data-ttu-id="afdb0-104">Это пользовательское действие вызывает исполняемый файл, запущенный с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="afdb0-104">This custom action calls an executable launched with a command line.</span></span>

<span data-ttu-id="afdb0-105">См. также [исполняемые файлы](executable-files.md).</span><span class="sxs-lookup"><span data-stu-id="afdb0-105">See also [Executable Files](executable-files.md).</span></span>

## <a name="source"></a><span data-ttu-id="afdb0-106">Источник</span><span class="sxs-lookup"><span data-stu-id="afdb0-106">Source</span></span>

<span data-ttu-id="afdb0-107">Исполняемый файл создается на основе существующего файла.</span><span class="sxs-lookup"><span data-stu-id="afdb0-107">The executable is generated from an existing file.</span></span> <span data-ttu-id="afdb0-108">Исходное поле [таблицы CustomAction](customaction-table.md) содержит ключ к [таблице свойств](property-table.md) для свойства, которое содержит полный путь к исполняемому файлу.</span><span class="sxs-lookup"><span data-stu-id="afdb0-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Property table](property-table.md) for a property that contains the full path to the executable file.</span></span>

## <a name="type-value"></a><span data-ttu-id="afdb0-109">Значение типа</span><span class="sxs-lookup"><span data-stu-id="afdb0-109">Type Value</span></span>

<span data-ttu-id="afdb0-110">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип.</span><span class="sxs-lookup"><span data-stu-id="afdb0-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="afdb0-111">Константы</span><span class="sxs-lookup"><span data-stu-id="afdb0-111">Constants</span></span>                                                        | <span data-ttu-id="afdb0-112">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="afdb0-112">Hexadecimal</span></span> | <span data-ttu-id="afdb0-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="afdb0-113">Decimal</span></span> |
|------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="afdb0-114">**мсидбкустомактионтипиксе**  +  **мсидбкустомактионтипепроперти**</span><span class="sxs-lookup"><span data-stu-id="afdb0-114">**msidbCustomActionTypeExe** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="afdb0-115">0x032</span><span class="sxs-lookup"><span data-stu-id="afdb0-115">0x032</span></span>       | <span data-ttu-id="afdb0-116">50</span><span class="sxs-lookup"><span data-stu-id="afdb0-116">50</span></span>      |



 

## <a name="target"></a><span data-ttu-id="afdb0-117">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="afdb0-117">Target</span></span>

<span data-ttu-id="afdb0-118">Целевой столбец [таблицы CustomAction](customaction-table.md) содержит строку командной строки для исполняемого файла, указанного в исходном столбце.</span><span class="sxs-lookup"><span data-stu-id="afdb0-118">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable identified in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="afdb0-119">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="afdb0-119">Return Processing Options</span></span>

<span data-ttu-id="afdb0-120">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры обработки возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="afdb0-120">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="afdb0-121">Описание параметров и значений см. в разделе [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="afdb0-121">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="afdb0-122">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="afdb0-122">Execution Scheduling Options</span></span>

<span data-ttu-id="afdb0-123">Включите дополнительные биты флагов в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры планирования выполнения.</span><span class="sxs-lookup"><span data-stu-id="afdb0-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="afdb0-124">Эти параметры управляют несколькими выполнениями пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="afdb0-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="afdb0-125">Описание параметров см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="afdb0-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="afdb0-126">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="afdb0-126">In-Script Execution Options</span></span>

<span data-ttu-id="afdb0-127">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметр выполнения в скрипте.</span><span class="sxs-lookup"><span data-stu-id="afdb0-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="afdb0-128">Эти параметры копируют код действия в скрипт выполнения, отката или фиксации.</span><span class="sxs-lookup"><span data-stu-id="afdb0-128">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="afdb0-129">Описание параметров см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="afdb0-129">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="afdb0-130">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="afdb0-130">Return Values</span></span>

<span data-ttu-id="afdb0-131">Настраиваемые действия, являющиеся [исполняемыми файлами](executable-files.md) , должны возвращать значение 0 для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="afdb0-131">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="afdb0-132">Установщик интерпретирует любое другое возвращаемое значение как сбой.</span><span class="sxs-lookup"><span data-stu-id="afdb0-132">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="afdb0-133">Чтобы игнорировать возвращаемые значения, установите флаг битов **мсидбкустомактионтипеконтинуе** в поле Тип таблицы CustomAction.</span><span class="sxs-lookup"><span data-stu-id="afdb0-133">To ignore return values set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="afdb0-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="afdb0-134">Remarks</span></span>

<span data-ttu-id="afdb0-135">Пользовательское действие, запускающее исполняемый файл, принимает командную строку, которая обычно содержит свойства, которые определены динамически.</span><span class="sxs-lookup"><span data-stu-id="afdb0-135">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="afdb0-136">Если это также [Отложенное настраиваемое действие выполнения](deferred-execution-custom-actions.md), установщик использует параметр CreateProcessAsUser или CreateProcess для создания процесса при вызове настраиваемого действия из скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="afdb0-136">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses CreateProcessAsUser or CreateProcess to create the process when the custom action is invoked from the installation script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="afdb0-137">См. также</span><span class="sxs-lookup"><span data-stu-id="afdb0-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afdb0-138">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="afdb0-138">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



