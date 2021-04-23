---
description: Разработчики установщик Windowsных пакетов могут использовать настраиваемое действие типа 1, если стандартные действия недостаточны для выполнения установки.
ms.assetid: 277b875f-37f1-4f4d-98ae-7a18131de4f0
title: Тип настраиваемого действия 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72efd083b2cd547ff1dbd7f3bc81a617b5da88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081493"
---
# <a name="custom-action-type-1"></a><span data-ttu-id="d81b7-103">Тип настраиваемого действия 1</span><span class="sxs-lookup"><span data-stu-id="d81b7-103">Custom Action Type 1</span></span>

<span data-ttu-id="d81b7-104">Это пользовательское действие вызывает библиотеку динамической компоновки (DLL), написанную на языке C или C++.</span><span class="sxs-lookup"><span data-stu-id="d81b7-104">This custom action calls a dynamic link library (DLL) written in C or C++.</span></span>

## <a name="source"></a><span data-ttu-id="d81b7-105">Источник</span><span class="sxs-lookup"><span data-stu-id="d81b7-105">Source</span></span>

<span data-ttu-id="d81b7-106">Библиотека DLL создается из временного двоичного потока.</span><span class="sxs-lookup"><span data-stu-id="d81b7-106">The DLL is generated from a temporary binary stream.</span></span> <span data-ttu-id="d81b7-107">Исходное поле [таблицы CustomAction](customaction-table.md) содержит ключ к [двоичной таблице](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="d81b7-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="d81b7-108">Столбец данных в таблице binary содержит данные потока.</span><span class="sxs-lookup"><span data-stu-id="d81b7-108">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="d81b7-109">Для каждой строки выделяется отдельный поток.</span><span class="sxs-lookup"><span data-stu-id="d81b7-109">A separate stream is allocated for each row.</span></span> <span data-ttu-id="d81b7-110">Новые двоичные данные можно вставить из файла с помощью [**мсирекордсетстреам**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) , за которым следует [**мсивиевмодифи**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) , чтобы вставить запись в таблицу.</span><span class="sxs-lookup"><span data-stu-id="d81b7-110">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="d81b7-111">При вызове настраиваемого действия потоковые данные копируются во временный файл, который затем обрабатывается в зависимости от типа настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="d81b7-111">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="d81b7-112">Значение типа</span><span class="sxs-lookup"><span data-stu-id="d81b7-112">Type Value</span></span>

<span data-ttu-id="d81b7-113">Включите следующие биты флагов в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип.</span><span class="sxs-lookup"><span data-stu-id="d81b7-113">Include the following flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="d81b7-114">Константы</span><span class="sxs-lookup"><span data-stu-id="d81b7-114">Constants</span></span>                                                          | <span data-ttu-id="d81b7-115">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="d81b7-115">Hexadecimal</span></span> | <span data-ttu-id="d81b7-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="d81b7-116">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="d81b7-117">**мсидбкустомактионтипедлл**  +  **мсидбкустомактионтипебинаридата**</span><span class="sxs-lookup"><span data-stu-id="d81b7-117">**msidbCustomActionTypeDll** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="d81b7-118">0x001</span><span class="sxs-lookup"><span data-stu-id="d81b7-118">0x001</span></span>       | <span data-ttu-id="d81b7-119">1</span><span class="sxs-lookup"><span data-stu-id="d81b7-119">1</span></span>       |



 

## <a name="target"></a><span data-ttu-id="d81b7-120">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="d81b7-120">Target</span></span>

<span data-ttu-id="d81b7-121">Библиотека DLL вызывается через точку входа с именем в поле Target [таблицы CustomAction](customaction-table.md), передавая один аргумент, который является обработчиком текущего сеанса установки.</span><span class="sxs-lookup"><span data-stu-id="d81b7-121">The DLL is called through the entry point named in the Target field of the [CustomAction table](customaction-table.md), passing a single argument that is the handle to the current install session.</span></span> <span data-ttu-id="d81b7-122">Имя точки входа, указанное в таблице, должно совпадать с именем, экспортированным из библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="d81b7-122">The entry point name specified in the table must match that exported from the DLL.</span></span> <span data-ttu-id="d81b7-123">Обратите внимание, что если функция записи не указана с помощью. DEF-файл или спецификация "/EXPORT: компоновщик" имя может содержать символ подчеркивания в начале и @4 суффикс "".</span><span class="sxs-lookup"><span data-stu-id="d81b7-123">Note that if the entry function is not specified by a .DEF file or by a /EXPORT: linker specification, the name may have a leading underscore and a "@4" suffix.</span></span> <span data-ttu-id="d81b7-124">Вызываемая функция должна задавать \_ \_ соглашение о вызовах STDCALL.</span><span class="sxs-lookup"><span data-stu-id="d81b7-124">The called function must specify the \_\_stdcall calling convention.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="d81b7-125">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="d81b7-125">Return Processing Options</span></span>

<span data-ttu-id="d81b7-126">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры обработки возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="d81b7-126">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="d81b7-127">Описание параметров и значений см. в разделе [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="d81b7-127">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="d81b7-128">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="d81b7-128">Execution Scheduling Options</span></span>

<span data-ttu-id="d81b7-129">Включите дополнительные биты флагов в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры планирования выполнения.</span><span class="sxs-lookup"><span data-stu-id="d81b7-129">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="d81b7-130">Эти параметры управляют несколькими выполнениями пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="d81b7-130">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="d81b7-131">Описание параметров см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="d81b7-131">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="d81b7-132">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="d81b7-132">In-Script Execution Options</span></span>

<span data-ttu-id="d81b7-133">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметр выполнения в скрипте.</span><span class="sxs-lookup"><span data-stu-id="d81b7-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="d81b7-134">Эти параметры копируют код действия в скрипт выполнения, отката или фиксации.</span><span class="sxs-lookup"><span data-stu-id="d81b7-134">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="d81b7-135">Описание параметров см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="d81b7-135">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="d81b7-136">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d81b7-136">Return Values</span></span>

<span data-ttu-id="d81b7-137">См. раздел [возвращаемые значения пользовательских действий](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d81b7-137">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d81b7-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d81b7-138">Remarks</span></span>

<span data-ttu-id="d81b7-139">Для пользовательского действия, которое вызывает библиотеку динамической компоновки (DLL), требуется маркер сеанса установки.</span><span class="sxs-lookup"><span data-stu-id="d81b7-139">A custom action that calls a dynamic-link library (DLL) requires a handle to the installation session.</span></span> <span data-ttu-id="d81b7-140">Если это также отложенное настраиваемое действие выполнения, сеанс может больше не существовать во время выполнения скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="d81b7-140">If this is also a deferred execution custom action, the session may no longer exist during execution of the installation script.</span></span> <span data-ttu-id="d81b7-141">Сведения о том, как пользовательское действие этого типа может получить сведения о контексте, см. в разделе [Получение контекстных сведений для отложенного выполнения настраиваемых действий](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="d81b7-141">For information on how a custom action of this type can obtain context information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="d81b7-142">При экспорте таблицы базы данных каждый поток записывается в виде отдельного файла в подпапке с именем после таблицы с использованием первичного ключа в качестве имени файла (столбца имени для двоичной таблицы) и расширения по умолчанию ". ИБД".</span><span class="sxs-lookup"><span data-stu-id="d81b7-142">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="d81b7-143">Имя должно использовать формат 8,3, если файловая система или система управления версиями не поддерживает длинные имена файлов.</span><span class="sxs-lookup"><span data-stu-id="d81b7-143">The name should use the 8.3 format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="d81b7-144">Файл постоянного архива заменяет данные потока с использованием имени файла, чтобы при импорте таблицы можно было найти данные.</span><span class="sxs-lookup"><span data-stu-id="d81b7-144">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d81b7-145">См. также</span><span class="sxs-lookup"><span data-stu-id="d81b7-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d81b7-146">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="d81b7-146">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="d81b7-147">Библиотеки динамической компоновки</span><span class="sxs-lookup"><span data-stu-id="d81b7-147">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)
</dt> <dt>

[<span data-ttu-id="d81b7-148">Получение сведений о контексте для отложенных настраиваемых действий выполнения</span><span class="sxs-lookup"><span data-stu-id="d81b7-148">Obtaining Context Information for Deferred Execution Custom Actions</span></span>](obtaining-context-information-for-deferred-execution-custom-actions.md)
</dt> </dl>

 

 



