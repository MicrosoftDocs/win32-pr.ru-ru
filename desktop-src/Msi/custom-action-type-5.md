---
description: Разработчики установщик Windowsных пакетов могут использовать настраиваемое действие типа 5, если стандартные действия недостаточны для выполнения установки.
ms.assetid: 32b10271-44b1-4c5d-9c8b-eed1b4cd31e2
title: Тип настраиваемого действия 5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85460c9a41dca060ca2634c013999c2c340ddfa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663528"
---
# <a name="custom-action-type-5"></a><span data-ttu-id="0108b-103">Тип настраиваемого действия 5</span><span class="sxs-lookup"><span data-stu-id="0108b-103">Custom Action Type 5</span></span>

<span data-ttu-id="0108b-104">Это пользовательское действие написано на языке JScript, например ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="0108b-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="0108b-105">Установщик Windows не поддерживает JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="0108b-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="0108b-106">Дополнительные сведения см. в разделе [сценарии](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="0108b-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="0108b-107">Источник</span><span class="sxs-lookup"><span data-stu-id="0108b-107">Source</span></span>

<span data-ttu-id="0108b-108">Скрипт создается из временного двоичного потока.</span><span class="sxs-lookup"><span data-stu-id="0108b-108">The script is generated from a temporary binary stream.</span></span> <span data-ttu-id="0108b-109">Исходное поле [таблицы CustomAction](customaction-table.md) содержит ключ к [двоичной таблице](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="0108b-109">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="0108b-110">Столбец данных в таблице binary содержит данные потока.</span><span class="sxs-lookup"><span data-stu-id="0108b-110">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="0108b-111">Для каждой строки выделяется отдельный поток.</span><span class="sxs-lookup"><span data-stu-id="0108b-111">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="0108b-112">Новые двоичные данные можно вставить из файла с помощью [**мсирекордсетстреам**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) , за которым следует [**мсивиевмодифи**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) , чтобы вставить запись в таблицу.</span><span class="sxs-lookup"><span data-stu-id="0108b-112">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="0108b-113">При вызове настраиваемого действия потоковые данные копируются во временный файл, который затем обрабатывается в соответствии с типом настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="0108b-113">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed according to the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="0108b-114">Значение типа</span><span class="sxs-lookup"><span data-stu-id="0108b-114">Type Value</span></span>

<span data-ttu-id="0108b-115">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип 32-разрядного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="0108b-115">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of 32-bit custom action.</span></span>



| <span data-ttu-id="0108b-116">Константы</span><span class="sxs-lookup"><span data-stu-id="0108b-116">Constants</span></span>                                                              | <span data-ttu-id="0108b-117">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="0108b-117">Hexadecimal</span></span> | <span data-ttu-id="0108b-118">Decimal</span><span class="sxs-lookup"><span data-stu-id="0108b-118">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="0108b-119">**мсидбкустомактионтипежскрипт**  +  **мсидбкустомактионтипебинаридата**</span><span class="sxs-lookup"><span data-stu-id="0108b-119">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="0108b-120">0x05</span><span class="sxs-lookup"><span data-stu-id="0108b-120">0x05</span></span>        | <span data-ttu-id="0108b-121">5</span><span class="sxs-lookup"><span data-stu-id="0108b-121">5</span></span>       |



 

<span data-ttu-id="0108b-122">Установщик Windows могут использовать 64-разрядные пользовательские действия в 64-разрядных операционных системах.</span><span class="sxs-lookup"><span data-stu-id="0108b-122">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="0108b-123">64-разрядное пользовательское действие на основе скриптов должно включать бит **msidbCustomActionType64BitScript** в его числовой тип.</span><span class="sxs-lookup"><span data-stu-id="0108b-123">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="0108b-124">Дополнительные сведения см. в статье [64-разрядные пользовательские действия](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="0108b-124">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="0108b-125">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип 64-разрядного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="0108b-125">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="0108b-126">Константы</span><span class="sxs-lookup"><span data-stu-id="0108b-126">Constants</span></span>                                                                                                     | <span data-ttu-id="0108b-127">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="0108b-127">Hexadecimal</span></span> | <span data-ttu-id="0108b-128">Decimal</span><span class="sxs-lookup"><span data-stu-id="0108b-128">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="0108b-129">**мсидбкустомактионтипежскрипт**  +  **мсидбкустомактионтипебинаридата**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="0108b-129">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeBinaryData** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="0108b-130">0x0001005</span><span class="sxs-lookup"><span data-stu-id="0108b-130">0x0001005</span></span>   | <span data-ttu-id="0108b-131">4101</span><span class="sxs-lookup"><span data-stu-id="0108b-131">4101</span></span>    |



 

## <a name="target"></a><span data-ttu-id="0108b-132">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="0108b-132">Target</span></span>

<span data-ttu-id="0108b-133">Целевое поле [таблицы CustomAction](customaction-table.md) содержит необязательную функцию скрипта.</span><span class="sxs-lookup"><span data-stu-id="0108b-133">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="0108b-134">Сначала обработка отправляет скрипт для синтаксического анализа, а затем вызывает необязательную функцию скрипта.</span><span class="sxs-lookup"><span data-stu-id="0108b-134">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="0108b-135">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="0108b-135">Return Processing Options</span></span>

<span data-ttu-id="0108b-136">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры обработки возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="0108b-136">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="0108b-137">Описание параметров и значений см. в разделе [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="0108b-137">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="0108b-138">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="0108b-138">Execution Scheduling Options</span></span>

<span data-ttu-id="0108b-139">Включите дополнительные биты флагов в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры планирования выполнения.</span><span class="sxs-lookup"><span data-stu-id="0108b-139">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="0108b-140">Эти параметры управляют несколькими выполнениями пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="0108b-140">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="0108b-141">Описание параметров см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="0108b-141">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="0108b-142">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="0108b-142">In-Script Execution Options</span></span>

<span data-ttu-id="0108b-143">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметр выполнения в скрипте.</span><span class="sxs-lookup"><span data-stu-id="0108b-143">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="0108b-144">Эти параметры копируют код действия в скрипт выполнения, отката или фиксации.</span><span class="sxs-lookup"><span data-stu-id="0108b-144">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="0108b-145">Описание параметров см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="0108b-145">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="0108b-146">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="0108b-146">Return Values</span></span>

<span data-ttu-id="0108b-147">Необязательные функции, написанные в скрипте, должны возвращать одно из значений, описанных в разделе [возвращаемые значения настраиваемых действий JScript и VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="0108b-147">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0108b-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0108b-148">Remarks</span></span>

<span data-ttu-id="0108b-149">Для пользовательского действия, написанного на JScript или VBScript, требуется установка [**объекта сеанса**](session-object.md).</span><span class="sxs-lookup"><span data-stu-id="0108b-149">A custom action that is written in JScript or VBScript requires the installation of [**Session Object**](session-object.md).</span></span> <span data-ttu-id="0108b-150">Установщик Присоединяет объект **сеанса** к скрипту с именем *Session*.</span><span class="sxs-lookup"><span data-stu-id="0108b-150">The installer attaches the **Session** object to the script with the name *Session*.</span></span> <span data-ttu-id="0108b-151">Так как объект **сеанса** может не существовать во время отката установки, отложенное настраиваемое действие, написанное в скрипте, должно использовать один из методов или свойств объекта **Session** , описанный в разделе [Получение сведений о контексте для отложенного выполнения настраиваемых действий](obtaining-context-information-for-deferred-execution-custom-actions.md) для получения контекста.</span><span class="sxs-lookup"><span data-stu-id="0108b-151">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="0108b-152">При экспорте таблицы базы данных каждый поток записывается в виде отдельного файла в подпапке с именем после таблицы с использованием первичного ключа в качестве имени файла (столбца имени для двоичной таблицы) и расширения по умолчанию ". ИБД".</span><span class="sxs-lookup"><span data-stu-id="0108b-152">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="0108b-153">Имя должно использовать формат имени файла 8,3, если файловая система или система управления версиями не поддерживает длинные имена файлов.</span><span class="sxs-lookup"><span data-stu-id="0108b-153">The name should use the 8.3 file name format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="0108b-154">Файл постоянного архива заменяет данные потока с использованием имени файла, чтобы при импорте таблицы можно было найти данные.</span><span class="sxs-lookup"><span data-stu-id="0108b-154">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0108b-155">См. также</span><span class="sxs-lookup"><span data-stu-id="0108b-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0108b-156">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="0108b-156">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



