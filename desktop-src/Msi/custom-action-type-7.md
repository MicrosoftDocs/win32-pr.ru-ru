---
description: Разработчики установщик Windowsных пакетов могут использовать тип настраиваемого действия 7, если стандартные действия недостаточны для выполнения установки.
ms.assetid: 4a8f35f9-58a8-417e-b72e-159f4af7d83f
title: Тип настраиваемого действия 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d3cc1c68fae098c6ef70797ed87df887ff898a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080925"
---
# <a name="custom-action-type-7"></a><span data-ttu-id="0221e-103">Тип настраиваемого действия 7</span><span class="sxs-lookup"><span data-stu-id="0221e-103">Custom Action Type 7</span></span>

<span data-ttu-id="0221e-104">Тип настраиваемого действия 7 используется с параллельными установками.</span><span class="sxs-lookup"><span data-stu-id="0221e-104">The Custom Action Type 7 is used with concurrent installations.</span></span> <span data-ttu-id="0221e-105">Параллельные установки не рекомендуются для установки приложений, предназначенных для выпуска в общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="0221e-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="0221e-106">Дополнительные сведения о параллельных установках см. в разделе [одновременная установка](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="0221e-106">For more information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="0221e-107">Это пользовательское действие устанавливает другой пакет установщика, вложенный в первый пакет.</span><span class="sxs-lookup"><span data-stu-id="0221e-107">This custom action installs another installer package that is nested inside of the first package.</span></span>

## <a name="source"></a><span data-ttu-id="0221e-108">Источник</span><span class="sxs-lookup"><span data-stu-id="0221e-108">Source</span></span>

<span data-ttu-id="0221e-109">База данных параллельного приложения хранится в виде подхранилища пакета, а имя подхранилища — в поле Source [таблицы CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="0221e-109">The database of the concurrent application is stored as a substorage of the package, and the name of the substorage is designated in the Source field of the [CustomAction table](customaction-table.md).</span></span>

## <a name="numeric-type"></a><span data-ttu-id="0221e-110">Числовой тип</span><span class="sxs-lookup"><span data-stu-id="0221e-110">Numeric Type</span></span>



| <span data-ttu-id="0221e-111">Имя типа</span><span class="sxs-lookup"><span data-stu-id="0221e-111">Type name</span></span>                                                      | <span data-ttu-id="0221e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="0221e-112">Value</span></span> |
|----------------------------------------------------------------|-------|
| <span data-ttu-id="0221e-113">Мсидбкустомактионтипеинсталл + Мсидбкустомактионтипебинаридата</span><span class="sxs-lookup"><span data-stu-id="0221e-113">msidbCustomActionTypeInstall + msidbCustomActionTypeBinaryData</span></span> | <span data-ttu-id="0221e-114">7</span><span class="sxs-lookup"><span data-stu-id="0221e-114">7</span></span>     |



 

## <a name="target"></a><span data-ttu-id="0221e-115">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="0221e-115">Target</span></span>

<span data-ttu-id="0221e-116">Целевое поле [таблицы CustomAction](customaction-table.md) содержит параметры свойств, которые должны быть переданы в параллельную установку.</span><span class="sxs-lookup"><span data-stu-id="0221e-116">The Target field of the [CustomAction table](customaction-table.md) contains property settings to be passed to the concurrent installation.</span></span> <span data-ttu-id="0221e-117">Эти параметры свойств могут задавать функции.</span><span class="sxs-lookup"><span data-stu-id="0221e-117">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="0221e-118">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="0221e-118">Return Processing Options</span></span>

<span data-ttu-id="0221e-119">Одновременный сеанс установки выполняется в виде отдельного потока в текущем процессе.</span><span class="sxs-lookup"><span data-stu-id="0221e-119">The concurrent installation session runs as a separate thread in the current process.</span></span> <span data-ttu-id="0221e-120">Параллельная установка не может выполняться асинхронно.</span><span class="sxs-lookup"><span data-stu-id="0221e-120">A concurrent installation cannot run asynchronously.</span></span>

<span data-ttu-id="0221e-121">См. раздел [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="0221e-121">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="0221e-122">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="0221e-122">Execution Scheduling Options</span></span>

<span data-ttu-id="0221e-123">Доступны флаги параметров для управления возможным множественным выполнением пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="0221e-123">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="0221e-124">См. раздел [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="0221e-124">See [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="0221e-125">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="0221e-125">In-Script Execution Options</span></span>

<span data-ttu-id="0221e-126">Это настраиваемое действие не использует этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0221e-126">This custom action does not use this option.</span></span>

## <a name="return-values"></a><span data-ttu-id="0221e-127">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="0221e-127">Return Values</span></span>

<span data-ttu-id="0221e-128">Возвращаемое состояние выхода пользователя, сбоя, приостановки или успешного выполнения при параллельной установке обрабатывается так же, как любое другое действие.</span><span class="sxs-lookup"><span data-stu-id="0221e-128">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="0221e-129">Обратите внимание, что установщик Windows преобразует возвращаемые значения из всех действий при записи возвращаемого значения в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="0221e-129">Note however that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="0221e-130">Например, если возвращаемое значение действия отображается как 1 в файле журнала, это означает, что действие вернуло ошибку \_ успешно.</span><span class="sxs-lookup"><span data-stu-id="0221e-130">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="0221e-131">Дополнительные сведения об этом переводе см. в разделе [ведение журнала возвращаемых значений действий](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0221e-131">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="0221e-132">Обратите внимание, что если одновременная установка имеет **мсидбкустомактионтипеконтинуе** , то возвращается сообщение об ошибке \_ Install \_ усерексит, ошибка установки, перезагрузка \_ \_ , ошибка \_ установки \_ \_ сейчас, или \_ \_ требуется перезагрузка с ошибкой, \_ \_ Если ошибка возникает успешно.</span><span class="sxs-lookup"><span data-stu-id="0221e-132">Note that if a concurrent install has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="0221e-133">Это означает, что если вы настроили **мсидбкустомактионтипеконтинуе** и для параллельной установки требуется перезагрузка, требование перезагрузки будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="0221e-133">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="0221e-134">Кроме того, код ошибки из настраиваемого действия параллельной установки будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="0221e-134">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="0221e-135">Если **мсидбкустомактионтипеконтинуе** не задан, следующие коды возврата \_ и успешная ошибка будут считаться успешными и иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="0221e-135">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="0221e-136">Другие коды возврата обрабатываются как сбой.</span><span class="sxs-lookup"><span data-stu-id="0221e-136">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="0221e-137">Сообщение</span><span class="sxs-lookup"><span data-stu-id="0221e-137">Message</span></span>                          | <span data-ttu-id="0221e-138">Значение</span><span class="sxs-lookup"><span data-stu-id="0221e-138">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0221e-139">Ошибка при \_ установке \_ перезагрузки</span><span class="sxs-lookup"><span data-stu-id="0221e-139">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="0221e-140">В конце установки будет установлен флаг перезапуска.</span><span class="sxs-lookup"><span data-stu-id="0221e-140">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="0221e-141">Ошибка при \_ установке \_ перезагрузки \_</span><span class="sxs-lookup"><span data-stu-id="0221e-141">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="0221e-142">Перед завершением установки требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="0221e-142">A restart is required before completing the installation.</span></span> <span data-ttu-id="0221e-143">Перезагрузка будет обработана немедленно.</span><span class="sxs-lookup"><span data-stu-id="0221e-143">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="0221e-144">Ошибка \_ " \_ требуется перезагрузка при успешном выполнении" \_</span><span class="sxs-lookup"><span data-stu-id="0221e-144">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="0221e-145">Требуется перезагрузка, но она была подавлена.</span><span class="sxs-lookup"><span data-stu-id="0221e-145">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="0221e-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0221e-146">Remarks</span></span>

<span data-ttu-id="0221e-147">Условное выражение требуется для включения параллельной установки при установке или удалении связанного компонента или компонента.</span><span class="sxs-lookup"><span data-stu-id="0221e-147">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0221e-148">См. также</span><span class="sxs-lookup"><span data-stu-id="0221e-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0221e-149">Параллельные установки</span><span class="sxs-lookup"><span data-stu-id="0221e-149">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="0221e-150">Ссылка на настраиваемое действие</span><span class="sxs-lookup"><span data-stu-id="0221e-150">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="0221e-151">Сведения о настраиваемых действиях</span><span class="sxs-lookup"><span data-stu-id="0221e-151">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="0221e-152">Использование настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="0221e-152">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="0221e-153">Возвращаемые значения настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="0221e-153">Custom Action Return Values</span></span>](custom-action-return-values.md)
</dt> </dl>

 

 



