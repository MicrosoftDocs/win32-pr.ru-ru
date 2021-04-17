---
description: Разработчики установщик Windowsных пакетов могут использовать настраиваемое действие типа 34, если стандартные действия недостаточны для выполнения установки.
ms.assetid: 4d0e4f01-0530-4202-bc78-b6e52670b8e5
title: Тип настраиваемого действия 34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ba17c9a4dc5b35d8d03e9cca2707079cb15bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651002"
---
# <a name="custom-action-type-34"></a><span data-ttu-id="64202-103">Тип настраиваемого действия 34</span><span class="sxs-lookup"><span data-stu-id="64202-103">Custom Action Type 34</span></span>

<span data-ttu-id="64202-104">Это пользовательское действие вызывает исполняемый файл, запущенный с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="64202-104">This custom action calls an executable launched with a command line.</span></span> <span data-ttu-id="64202-105">Дополнительные сведения см. в разделе [исполняемые файлы](executable-files.md).</span><span class="sxs-lookup"><span data-stu-id="64202-105">For more information, see [Executable Files](executable-files.md).</span></span>

## <a name="source"></a><span data-ttu-id="64202-106">Источник</span><span class="sxs-lookup"><span data-stu-id="64202-106">Source</span></span>

<span data-ttu-id="64202-107">Исполняемый файл создается из файла.</span><span class="sxs-lookup"><span data-stu-id="64202-107">The executable is generated from a file.</span></span> <span data-ttu-id="64202-108">Исходное поле таблицы [CustomAction](customaction-table.md) содержит ключ в таблице [Directory](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="64202-108">The Source field of the [CustomAction](customaction-table.md) table contains a key into the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="64202-109">Указанная запись в таблице каталогов используется для разрешения полного пути к рабочему каталогу.</span><span class="sxs-lookup"><span data-stu-id="64202-109">The referenced Directory table entry is used to resolve the full path to a working directory.</span></span> <span data-ttu-id="64202-110">Это не обязательно должен быть путь к каталогу, содержащему исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="64202-110">This is not required to be the path to the directory containing the executable.</span></span>

## <a name="type-value"></a><span data-ttu-id="64202-111">Значение типа</span><span class="sxs-lookup"><span data-stu-id="64202-111">Type Value</span></span>

<span data-ttu-id="64202-112">Включите следующее значение в столбец Type таблицы [CustomAction](customaction-table.md) , чтобы указать базовый числовой тип.</span><span class="sxs-lookup"><span data-stu-id="64202-112">Include the following value in the Type column of the [CustomAction](customaction-table.md) table to specify the basic numeric type.</span></span>



| <span data-ttu-id="64202-113">Константы</span><span class="sxs-lookup"><span data-stu-id="64202-113">Constants</span></span>                                                         | <span data-ttu-id="64202-114">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="64202-114">Hexadecimal</span></span> | <span data-ttu-id="64202-115">Decimal</span><span class="sxs-lookup"><span data-stu-id="64202-115">Decimal</span></span> |
|-------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="64202-116">**мсидбкустомактионтипиксе**  +  **мсидбкустомактионтипедиректори**</span><span class="sxs-lookup"><span data-stu-id="64202-116">**msidbCustomActionTypeExe** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="64202-117">0x022</span><span class="sxs-lookup"><span data-stu-id="64202-117">0x022</span></span>       | <span data-ttu-id="64202-118">34</span><span class="sxs-lookup"><span data-stu-id="64202-118">34</span></span>      |



 

## <a name="target"></a><span data-ttu-id="64202-119">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="64202-119">Target</span></span>

<span data-ttu-id="64202-120">Целевой столбец таблицы [CustomAction](customaction-table.md) содержит полный путь и имя исполняемого файла, за которым следуют необязательные аргументы к исполняемому файлу.</span><span class="sxs-lookup"><span data-stu-id="64202-120">The Target column of the [CustomAction](customaction-table.md) table contains the full path and name of the executable file followed by optional arguments to the executable.</span></span> <span data-ttu-id="64202-121">Требуется полный путь и имя исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="64202-121">The full path and name to the executable file is required.</span></span> <span data-ttu-id="64202-122">Кавычки должны использоваться вокруг длинных имен файлов или путей.</span><span class="sxs-lookup"><span data-stu-id="64202-122">Quotation marks must be used around long file names or paths.</span></span> <span data-ttu-id="64202-123">Значение рассматривается как [форматированный](formatted.md) текст и может содержать ссылки на свойства, файлы, каталоги или другие атрибуты форматированного текста.</span><span class="sxs-lookup"><span data-stu-id="64202-123">The value is treated as [formatted](formatted.md) text and may contain references to properties, files, directories, or other formatted text attributes.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="64202-124">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="64202-124">Return Processing Options</span></span>

<span data-ttu-id="64202-125">Включите дополнительные биты флага в столбец Type таблицы [CustomAction](customaction-table.md) , чтобы указать параметры обработки возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="64202-125">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify return processing options.</span></span> <span data-ttu-id="64202-126">Описание параметров и значений см. в разделе [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="64202-126">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="64202-127">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="64202-127">Execution Scheduling Options</span></span>

<span data-ttu-id="64202-128">Включите дополнительные биты флагов в столбец Type таблицы [CustomAction](customaction-table.md) , чтобы указать параметры планирования выполнения.</span><span class="sxs-lookup"><span data-stu-id="64202-128">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify execution scheduling options.</span></span> <span data-ttu-id="64202-129">Эти параметры управляют несколькими выполнениями пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="64202-129">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="64202-130">Описание параметров см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="64202-130">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="64202-131">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="64202-131">In-Script Execution Options</span></span>

<span data-ttu-id="64202-132">Включите дополнительные биты флага в столбец Type таблицы [CustomAction](customaction-table.md) , чтобы указать параметр выполнения в скрипте.</span><span class="sxs-lookup"><span data-stu-id="64202-132">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify an in-script execution option.</span></span> <span data-ttu-id="64202-133">Эти параметры копируют код действия в скрипт выполнения, отката или фиксации.</span><span class="sxs-lookup"><span data-stu-id="64202-133">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="64202-134">Описание параметров см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="64202-134">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="64202-135">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="64202-135">Return Values</span></span>

<span data-ttu-id="64202-136">Настраиваемые действия, являющиеся [исполняемыми файлами](executable-files.md) , должны возвращать значение 0 для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="64202-136">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="64202-137">Установщик интерпретирует любое другое возвращаемое значение как сбой.</span><span class="sxs-lookup"><span data-stu-id="64202-137">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="64202-138">Чтобы игнорировать возвращаемые значения, установите флаг битов **мсидбкустомактионтипеконтинуе** в поле Тип таблицы [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="64202-138">To ignore return values set the **msidbCustomActionTypeContinue** bit flag in the Type field of the [CustomAction](customaction-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="64202-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64202-139">Remarks</span></span>

<span data-ttu-id="64202-140">Пользовательское действие, запускающее исполняемый файл, принимает командную строку, которая обычно содержит свойства, которые определены динамически.</span><span class="sxs-lookup"><span data-stu-id="64202-140">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="64202-141">Если это также [Отложенное настраиваемое действие выполнения](deferred-execution-custom-actions.md), установщик использует [**параметр CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) или [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) для создания процесса при вызове настраиваемого действия из скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="64202-141">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64202-142">См. также</span><span class="sxs-lookup"><span data-stu-id="64202-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64202-143">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="64202-143">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 
