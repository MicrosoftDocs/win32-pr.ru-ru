---
description: Разработчики установщик Windowsных пакетов могут использовать настраиваемое действие типа 2, если стандартные действия недостаточны для выполнения установки.
ms.assetid: 79ae0582-c991-4c0a-860b-0f5197ad0c7c
title: Тип настраиваемого действия 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0497b2a76dc2fac7f5e56f7347b50deac867757f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651003"
---
# <a name="custom-action-type-2"></a><span data-ttu-id="7258f-103">Тип настраиваемого действия 2</span><span class="sxs-lookup"><span data-stu-id="7258f-103">Custom Action Type 2</span></span>

<span data-ttu-id="7258f-104">Это пользовательское действие вызывает исполняемый файл, запущенный с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="7258f-104">This custom action calls an executable launched with a command line.</span></span>

## <a name="source"></a><span data-ttu-id="7258f-105">Источник</span><span class="sxs-lookup"><span data-stu-id="7258f-105">Source</span></span>

<span data-ttu-id="7258f-106">Исполняемый объект создается из временного двоичного потока.</span><span class="sxs-lookup"><span data-stu-id="7258f-106">The executable is generated from a temporary binary stream.</span></span> <span data-ttu-id="7258f-107">Исходное поле [таблицы CustomAction](customaction-table.md) содержит ключ к [двоичной таблице](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="7258f-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="7258f-108">Столбец данных в таблице binary содержит данные потока.</span><span class="sxs-lookup"><span data-stu-id="7258f-108">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="7258f-109">Для каждой строки выделяется отдельный поток.</span><span class="sxs-lookup"><span data-stu-id="7258f-109">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="7258f-110">Новые двоичные данные можно вставить из файла с помощью [**мсирекордсетстреам**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) , за которым следует [**мсивиевмодифи**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) , чтобы вставить запись в таблицу.</span><span class="sxs-lookup"><span data-stu-id="7258f-110">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="7258f-111">При вызове настраиваемого действия потоковые данные копируются во временный файл, который затем обрабатывается в зависимости от типа настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="7258f-111">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="7258f-112">Значение типа</span><span class="sxs-lookup"><span data-stu-id="7258f-112">Type Value</span></span>

<span data-ttu-id="7258f-113">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип.</span><span class="sxs-lookup"><span data-stu-id="7258f-113">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="7258f-114">Константы</span><span class="sxs-lookup"><span data-stu-id="7258f-114">Constants</span></span>                                                          | <span data-ttu-id="7258f-115">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="7258f-115">Hexadecimal</span></span> | <span data-ttu-id="7258f-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="7258f-116">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="7258f-117">**мсидбкустомактионтипиксе**  +  **мсидбкустомактионтипебинаридата**</span><span class="sxs-lookup"><span data-stu-id="7258f-117">**msidbCustomActionTypeExe** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="7258f-118">0x002</span><span class="sxs-lookup"><span data-stu-id="7258f-118">0x002</span></span>       | <span data-ttu-id="7258f-119">2</span><span class="sxs-lookup"><span data-stu-id="7258f-119">2</span></span>       |



 

## <a name="target"></a><span data-ttu-id="7258f-120">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="7258f-120">Target</span></span>

<span data-ttu-id="7258f-121">Целевой столбец [таблицы CustomAction](customaction-table.md) содержит строку командной строки для исполняемого файла, указанного в исходном столбце.</span><span class="sxs-lookup"><span data-stu-id="7258f-121">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable named in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="7258f-122">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="7258f-122">Return Processing Options</span></span>

<span data-ttu-id="7258f-123">Включите дополнительные биты флага в столбец Type таблицы CustomAction, чтобы указать параметры обработки возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="7258f-123">Include optional flag bits in the Type column of the CustomAction table to specify return processing options.</span></span> <span data-ttu-id="7258f-124">Описание параметров и значений см. в разделе [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="7258f-124">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="7258f-125">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="7258f-125">Execution Scheduling Options</span></span>

<span data-ttu-id="7258f-126">Включите дополнительные биты флагов в столбец Type таблицы CustomAction, чтобы указать параметры планирования выполнения.</span><span class="sxs-lookup"><span data-stu-id="7258f-126">Include optional flag bits in the Type column of the CustomAction table to specify execution scheduling options.</span></span> <span data-ttu-id="7258f-127">Эти параметры управляют несколькими выполнениями пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="7258f-127">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="7258f-128">Описание параметров см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="7258f-128">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="7258f-129">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="7258f-129">In-Script Execution Options</span></span>

<span data-ttu-id="7258f-130">Включите дополнительные биты флага в столбец Type таблицы CustomAction, чтобы указать параметр выполнения в скрипте.</span><span class="sxs-lookup"><span data-stu-id="7258f-130">Include optional flag bits in the Type column of the CustomAction table to specify an in-script execution option.</span></span> <span data-ttu-id="7258f-131">Эти параметры копируют код действия в скрипт выполнения, отката или фиксации.</span><span class="sxs-lookup"><span data-stu-id="7258f-131">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="7258f-132">Описание параметров см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="7258f-132">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="7258f-133">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7258f-133">Return Values</span></span>

<span data-ttu-id="7258f-134">Настраиваемые действия, являющиеся [исполняемыми файлами](executable-files.md) , должны возвращать значение 0 для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="7258f-134">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="7258f-135">Установщик интерпретирует любое другое возвращаемое значение как сбой.</span><span class="sxs-lookup"><span data-stu-id="7258f-135">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="7258f-136">Чтобы игнорировать возвращаемые значения, установите флаг битов **мсидбкустомактионтипеконтинуе** в поле Тип таблицы CustomAction.</span><span class="sxs-lookup"><span data-stu-id="7258f-136">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="7258f-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7258f-137">Remarks</span></span>

<span data-ttu-id="7258f-138">Пользовательское действие, запускающее исполняемый файл, принимает командную строку, которая обычно содержит свойства, которые определены динамически.</span><span class="sxs-lookup"><span data-stu-id="7258f-138">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="7258f-139">Если это также [Отложенное настраиваемое действие выполнения](deferred-execution-custom-actions.md), установщик использует [**параметр CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) или [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) для создания процесса при вызове настраиваемого действия из скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="7258f-139">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

<span data-ttu-id="7258f-140">При экспорте таблицы базы данных каждый поток записывается в виде отдельного файла в подпапке с именем после таблицы с использованием первичного ключа в качестве имени файла (столбца имени для двоичной таблицы) и расширения по умолчанию ". ИБД".</span><span class="sxs-lookup"><span data-stu-id="7258f-140">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="7258f-141">Имя должно использовать формат 8,3, если файловая система или система управления версиями не поддерживает длинные имена файлов.</span><span class="sxs-lookup"><span data-stu-id="7258f-141">The name should use the 8.3 format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="7258f-142">Файл постоянного архива заменяет данные потока с использованием имени файла, чтобы при импорте таблицы можно было найти данные.</span><span class="sxs-lookup"><span data-stu-id="7258f-142">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7258f-143">См. также</span><span class="sxs-lookup"><span data-stu-id="7258f-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7258f-144">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="7258f-144">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="7258f-145">Исполняемые файлы</span><span class="sxs-lookup"><span data-stu-id="7258f-145">Executable Files</span></span>](executable-files.md)
</dt> </dl>

 

 
