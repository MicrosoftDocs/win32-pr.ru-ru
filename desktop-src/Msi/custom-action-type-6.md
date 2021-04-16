---
description: Разработчики установщик Windowsных пакетов могут использовать тип настраиваемого действия 6, если стандартные действия недостаточны для выполнения установки.
ms.assetid: d63449e1-231a-4601-b39e-1b69857ccb86
title: Тип настраиваемого действия 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007cd224caff801592bdde7389cfe3e77820f650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650951"
---
# <a name="custom-action-type-6"></a><span data-ttu-id="f134d-103">Тип настраиваемого действия 6</span><span class="sxs-lookup"><span data-stu-id="f134d-103">Custom Action Type 6</span></span>

<span data-ttu-id="f134d-104">Это настраиваемое действие написано на языке VBScript.</span><span class="sxs-lookup"><span data-stu-id="f134d-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="f134d-105">Дополнительные сведения см. в разделе [сценарии](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="f134d-105">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="f134d-106">Источник</span><span class="sxs-lookup"><span data-stu-id="f134d-106">Source</span></span>

<span data-ttu-id="f134d-107">Скрипт создается из временного двоичного потока.</span><span class="sxs-lookup"><span data-stu-id="f134d-107">The script is generated from a temporary binary stream.</span></span> <span data-ttu-id="f134d-108">Исходное поле [таблицы CustomAction](customaction-table.md) содержит ключ к [двоичной таблице](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="f134d-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="f134d-109">Столбец данных в таблице binary содержит данные потока.</span><span class="sxs-lookup"><span data-stu-id="f134d-109">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="f134d-110">Для каждой строки выделяется отдельный поток.</span><span class="sxs-lookup"><span data-stu-id="f134d-110">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="f134d-111">Новые двоичные данные можно вставить из файла с помощью [**мсирекордсетстреам**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) , за которым следует [**мсивиевмодифи**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) , чтобы вставить запись в таблицу.</span><span class="sxs-lookup"><span data-stu-id="f134d-111">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="f134d-112">При вызове настраиваемого действия потоковые данные копируются во временный файл, который затем обрабатывается в зависимости от типа настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="f134d-112">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="f134d-113">Значение типа</span><span class="sxs-lookup"><span data-stu-id="f134d-113">Type Value</span></span>

<span data-ttu-id="f134d-114">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип 32-разрядного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="f134d-114">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="f134d-115">Константы</span><span class="sxs-lookup"><span data-stu-id="f134d-115">Constants</span></span>                                                               | <span data-ttu-id="f134d-116">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="f134d-116">Hexadecimal</span></span> | <span data-ttu-id="f134d-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="f134d-117">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="f134d-118">**мсидбкустомактионтипевбскрипт**  +  **мсидбкустомактионтипебинаридата**</span><span class="sxs-lookup"><span data-stu-id="f134d-118">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="f134d-119">0x006</span><span class="sxs-lookup"><span data-stu-id="f134d-119">0x006</span></span>       | <span data-ttu-id="f134d-120">6</span><span class="sxs-lookup"><span data-stu-id="f134d-120">6</span></span>       |



 

<span data-ttu-id="f134d-121">Установщик Windows могут использовать 64-разрядные пользовательские действия в 64-разрядных операционных системах.</span><span class="sxs-lookup"><span data-stu-id="f134d-121">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="f134d-122">64-разрядное пользовательское действие на основе скриптов должно включать бит **msidbCustomActionType64BitScript** в его числовой тип.</span><span class="sxs-lookup"><span data-stu-id="f134d-122">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="f134d-123">Дополнительные сведения см. в статье [64-разрядные пользовательские действия](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="f134d-123">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="f134d-124">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип 64-разрядного настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="f134d-124">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="f134d-125">Константы</span><span class="sxs-lookup"><span data-stu-id="f134d-125">Constants</span></span>                                                                                                      | <span data-ttu-id="f134d-126">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="f134d-126">Hexadecimal</span></span> | <span data-ttu-id="f134d-127">Decimal</span><span class="sxs-lookup"><span data-stu-id="f134d-127">Decimal</span></span> |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="f134d-128">**мсидбкустомактионтипевбскрипт**  +  **мсидбкустомактионтипебинаридата**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="f134d-128">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeBinaryData** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="f134d-129">0x0001006</span><span class="sxs-lookup"><span data-stu-id="f134d-129">0x0001006</span></span>   | <span data-ttu-id="f134d-130">4102</span><span class="sxs-lookup"><span data-stu-id="f134d-130">4102</span></span>    |



 

## <a name="target"></a><span data-ttu-id="f134d-131">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="f134d-131">Target</span></span>

<span data-ttu-id="f134d-132">Целевое поле [таблицы CustomAction](customaction-table.md) содержит необязательную функцию скрипта.</span><span class="sxs-lookup"><span data-stu-id="f134d-132">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="f134d-133">Сначала обработка отправляет скрипт для синтаксического анализа, а затем вызывает необязательную функцию скрипта.</span><span class="sxs-lookup"><span data-stu-id="f134d-133">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="f134d-134">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="f134d-134">Return Processing Options</span></span>

<span data-ttu-id="f134d-135">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры обработки возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="f134d-135">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="f134d-136">Описание параметров и значений см. в разделе [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="f134d-136">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="f134d-137">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="f134d-137">Execution Scheduling Options</span></span>

<span data-ttu-id="f134d-138">Включите дополнительные биты флагов в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры планирования выполнения.</span><span class="sxs-lookup"><span data-stu-id="f134d-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="f134d-139">Эти параметры управляют несколькими выполнениями пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="f134d-139">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="f134d-140">Описание параметров см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="f134d-140">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="f134d-141">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="f134d-141">In-Script Execution Options</span></span>

<span data-ttu-id="f134d-142">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметр выполнения в скрипте.</span><span class="sxs-lookup"><span data-stu-id="f134d-142">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="f134d-143">Эти параметры копируют код действия в скрипт выполнения, отката или фиксации.</span><span class="sxs-lookup"><span data-stu-id="f134d-143">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="f134d-144">Описание параметров см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="f134d-144">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="f134d-145">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f134d-145">Return Values</span></span>

<span data-ttu-id="f134d-146">Необязательные функции, написанные в скрипте, должны возвращать одно из значений, описанных в разделе [возвращаемые значения настраиваемых действий JScript и VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="f134d-146">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f134d-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f134d-147">Remarks</span></span>

<span data-ttu-id="f134d-148">Для пользовательского действия, написанного на JScript или VBScript, требуется установка [**объекта Session**](session-object.md).</span><span class="sxs-lookup"><span data-stu-id="f134d-148">A custom action that is written in JScript or VBScript requires the installation of the [**Session Object**](session-object.md).</span></span> <span data-ttu-id="f134d-149">Установщик Присоединяет объект **сеанса** к скрипту с именем *Session*.</span><span class="sxs-lookup"><span data-stu-id="f134d-149">The installer attaches the **Session** object to the script with the name *Session*.</span></span> <span data-ttu-id="f134d-150">Так как объект **сеанса** может не существовать во время отката установки, отложенное настраиваемое действие, написанное в скрипте, должно использовать один из методов или свойств объекта **Session** , описанный в разделе [Получение сведений о контексте для отложенного выполнения настраиваемых действий](obtaining-context-information-for-deferred-execution-custom-actions.md) для получения контекста.</span><span class="sxs-lookup"><span data-stu-id="f134d-150">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="f134d-151">При экспорте таблицы базы данных каждый поток записывается в виде отдельного файла в подпапке с именем после таблицы с использованием первичного ключа в качестве имени файла (столбца имени для двоичной таблицы) и расширения по умолчанию ". ИБД".</span><span class="sxs-lookup"><span data-stu-id="f134d-151">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="f134d-152">Имя должно использовать формат имени файла 8,3, если файловая система или система управления версиями не поддерживает длинные имена файлов.</span><span class="sxs-lookup"><span data-stu-id="f134d-152">The name should use the 8.3 file name format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="f134d-153">Файл постоянного архива заменяет данные потока с использованием имени файла, чтобы при импорте таблицы можно было найти данные.</span><span class="sxs-lookup"><span data-stu-id="f134d-153">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f134d-154">См. также</span><span class="sxs-lookup"><span data-stu-id="f134d-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f134d-155">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="f134d-155">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



