---
description: Разработчики установщик Windowsных пакетов могут использовать настраиваемое действие типа 17, если стандартные действия недостаточны для выполнения установки.
ms.assetid: 99efd6d5-e0a3-4e66-ae55-252d19090d31
title: Тип настраиваемого действия 17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53d0046cb7515d701eb1bae3d10de0570ee5843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349002"
---
# <a name="custom-action-type-17"></a><span data-ttu-id="5e564-103">Тип настраиваемого действия 17</span><span class="sxs-lookup"><span data-stu-id="5e564-103">Custom Action Type 17</span></span>

<span data-ttu-id="5e564-104">Это пользовательское действие вызывает библиотеку динамической компоновки (DLL), написанную на языке C или C++.</span><span class="sxs-lookup"><span data-stu-id="5e564-104">This custom action calls a dynamic link library (DLL) written in C or C++.</span></span>

## <a name="source"></a><span data-ttu-id="5e564-105">Источник</span><span class="sxs-lookup"><span data-stu-id="5e564-105">Source</span></span>

<span data-ttu-id="5e564-106">Библиотека DLL устанавливается вместе с приложением во время текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="5e564-106">The DLL is installed with the application during the current session.</span></span> <span data-ttu-id="5e564-107">Исходное поле [таблицы CustomAction](customaction-table.md) содержит ключ к [таблице File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="5e564-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="5e564-108">Расположение кода настраиваемого действия определяется разрешением целевого пути для этого файла; Поэтому это настраиваемое действие должно быть вызвано после установки этого файла и до его удаления.</span><span class="sxs-lookup"><span data-stu-id="5e564-108">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after that file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="5e564-109">Значение типа</span><span class="sxs-lookup"><span data-stu-id="5e564-109">Type Value</span></span>

<span data-ttu-id="5e564-110">Включите следующее значение в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать базовый числовой тип.</span><span class="sxs-lookup"><span data-stu-id="5e564-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="5e564-111">Константы</span><span class="sxs-lookup"><span data-stu-id="5e564-111">Constants</span></span>                                                          | <span data-ttu-id="5e564-112">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="5e564-112">Hexadecimal</span></span> | <span data-ttu-id="5e564-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="5e564-113">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="5e564-114">**мсидбкустомактионтипедлл**  +  **мсидбкустомактионтипесаурцефиле**</span><span class="sxs-lookup"><span data-stu-id="5e564-114">**msidbCustomActionTypeDll** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="5e564-115">0x011</span><span class="sxs-lookup"><span data-stu-id="5e564-115">0x011</span></span>       | <span data-ttu-id="5e564-116">17</span><span class="sxs-lookup"><span data-stu-id="5e564-116">17</span></span>      |



 

## <a name="target"></a><span data-ttu-id="5e564-117">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="5e564-117">Target</span></span>

<span data-ttu-id="5e564-118">Библиотека DLL вызывается через точку входа с именем в поле Target [таблицы CustomAction](customaction-table.md), передавая один аргумент, который является обработчиком текущего сеанса установки.</span><span class="sxs-lookup"><span data-stu-id="5e564-118">The DLL is called through the entry point named in the Target field of the [CustomAction table](customaction-table.md), passing a single argument that is the handle to the current install session.</span></span> <span data-ttu-id="5e564-119">Имя точки входа, указанное в таблице, должно совпадать с именем, экспортированным из библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="5e564-119">The entry point name specified in the table must match that exported from the DLL.</span></span> <span data-ttu-id="5e564-120">Обратите внимание, что если функция записи не указана с помощью. DEF-файл или спецификация "/EXPORT: компоновщик" имя может содержать символ подчеркивания в начале и @4 суффикс "".</span><span class="sxs-lookup"><span data-stu-id="5e564-120">Note that if the entry function is not specified by a .DEF file or by a /EXPORT: linker specification, the name may have a leading underscore and a "@4" suffix.</span></span> <span data-ttu-id="5e564-121">Вызываемая функция должна задавать \_ \_ соглашение о вызовах STDCALL.</span><span class="sxs-lookup"><span data-stu-id="5e564-121">The called function must specify the \_\_stdcall calling convention.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="5e564-122">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="5e564-122">Return Processing Options</span></span>

<span data-ttu-id="5e564-123">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры обработки возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="5e564-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="5e564-124">Описание параметров и значений см. в разделе [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="5e564-124">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="5e564-125">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="5e564-125">Execution Scheduling Options</span></span>

<span data-ttu-id="5e564-126">Включите дополнительные биты флагов в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметры планирования выполнения.</span><span class="sxs-lookup"><span data-stu-id="5e564-126">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="5e564-127">Эти параметры управляют несколькими выполнениями пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="5e564-127">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="5e564-128">Описание параметров см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="5e564-128">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="5e564-129">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="5e564-129">In-Script Execution Options</span></span>

<span data-ttu-id="5e564-130">Включите дополнительные биты флага в столбец Type [таблицы CustomAction](customaction-table.md) , чтобы указать параметр выполнения в скрипте.</span><span class="sxs-lookup"><span data-stu-id="5e564-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="5e564-131">Эти параметры копируют код действия в скрипт выполнения, отката или фиксации.</span><span class="sxs-lookup"><span data-stu-id="5e564-131">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="5e564-132">Описание параметров см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="5e564-132">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="5e564-133">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="5e564-133">Return Values</span></span>

<span data-ttu-id="5e564-134">См. раздел [возвращаемые значения пользовательских действий](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="5e564-134">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5e564-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e564-135">Remarks</span></span>

<span data-ttu-id="5e564-136">Для пользовательского действия, которое вызывает библиотеку динамической компоновки (DLL), требуется маркер сеанса установки.</span><span class="sxs-lookup"><span data-stu-id="5e564-136">A custom action that calls a dynamic-link library (DLL) requires a handle to the installation session.</span></span> <span data-ttu-id="5e564-137">Если это также отложенное настраиваемое действие выполнения, сеанс может больше не существовать во время выполнения скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="5e564-137">If this is also a deferred execution custom action, the session may no longer exist during execution of the installation script.</span></span> <span data-ttu-id="5e564-138">Сведения о том, как пользовательское действие этого типа может получить сведения о контексте, см. в разделе [Получение контекстных сведений для отложенного выполнения настраиваемых действий](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="5e564-138">For information on how a custom action of this type can obtain context information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="5e564-139">Пользовательские действия выполняются в отдельном потоке и могут иметь ограниченный доступ к системе.</span><span class="sxs-lookup"><span data-stu-id="5e564-139">Custom actions execute in a separate thread, and may have limited access to the system.</span></span> <span data-ttu-id="5e564-140">Настраиваемые действия, которые выполняются асинхронно, блокируют основной поток при завершении текущей последовательности или сеанса установки до тех пор, пока они не будут возвращены.</span><span class="sxs-lookup"><span data-stu-id="5e564-140">Custom actions that run asynchronously block the main thread at the termination of either the current sequence or the install session until they return.</span></span>

<span data-ttu-id="5e564-141">Настраиваемые действия, которые ссылаются на установленный файл в качестве источника, например тип настраиваемого действия 17 (DLL), должны соответствовать следующим ограничениям последовательности.</span><span class="sxs-lookup"><span data-stu-id="5e564-141">Custom actions that reference an installed file as their source, such as Custom Action Type 17 (DLL), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="5e564-142">Настраиваемое действие должно быть упорядочено после [действия костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="5e564-142">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="5e564-143">Это необходимо для того, чтобы пользовательское действие могло разрешить путь, необходимый для поиска библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="5e564-143">This is so that the custom action can resolve the path needed to locate the DLL.</span></span>
-   <span data-ttu-id="5e564-144">Если исходный файл еще не установлен на компьютере, отложенные (в скрипте) настраиваемые действия этого типа должны быть упорядочены после [действия инсталлфилес](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="5e564-144">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="5e564-145">Если исходный файл еще не установлен на компьютере, неотложенные настраиваемые действия этого типа должны быть упорядочены после [действия функции InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="5e564-145">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e564-146">См. также</span><span class="sxs-lookup"><span data-stu-id="5e564-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e564-147">Настраиваемые \_ действия</span><span class="sxs-lookup"><span data-stu-id="5e564-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="5e564-148">Пользовательские действия отложенного выполнения</span><span class="sxs-lookup"><span data-stu-id="5e564-148">Deferred Execution Custom Actions</span></span>](deferred-execution-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="5e564-149">Библиотеки динамической компоновки</span><span class="sxs-lookup"><span data-stu-id="5e564-149">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)
</dt> </dl>

 

 



