---
description: Разработчики установщик Windowsных пакетов могут использовать тип настраиваемого действия 23, если стандартные действия недостаточны для выполнения установки.
ms.assetid: 8219f157-585d-4733-8e10-c05813b398ba
title: Тип настраиваемого действия 23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05576c44ab634dc117501a89e6b86594f5483458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913871"
---
# <a name="custom-action-type-23"></a><span data-ttu-id="c76ba-103">Тип настраиваемого действия 23</span><span class="sxs-lookup"><span data-stu-id="c76ba-103">Custom Action Type 23</span></span>

<span data-ttu-id="c76ba-104">Тип пользовательского действия 23 используется с параллельными установками.</span><span class="sxs-lookup"><span data-stu-id="c76ba-104">The Custom Action Type 23 is used with concurrent installations.</span></span> <span data-ttu-id="c76ba-105">Параллельные установки не рекомендуются для установки приложений, предназначенных для выпуска в общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="c76ba-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="c76ba-106">Сведения о параллельных установках см. в разделе [одновременная установка](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="c76ba-106">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="c76ba-107">Это пользовательское действие устанавливает другой пакет установщика, который находится в исходном дереве приложения.</span><span class="sxs-lookup"><span data-stu-id="c76ba-107">This custom action installs another installer package that resides in the application's source tree.</span></span>

## <a name="source"></a><span data-ttu-id="c76ba-108">Источник</span><span class="sxs-lookup"><span data-stu-id="c76ba-108">Source</span></span>

<span data-ttu-id="c76ba-109">Расположение параллельно выполняемого пакета установки указывается относительно корня исходного расположения, отображаемого в поле Источник [таблицы CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="c76ba-109">The location of the concurrent installation package is specified relative to the root of the source location shown in the Source field of the [CustomAction table](customaction-table.md).</span></span>

## <a name="numeric-type"></a><span data-ttu-id="c76ba-110">Числовой тип</span><span class="sxs-lookup"><span data-stu-id="c76ba-110">Numeric Type</span></span>



| <span data-ttu-id="c76ba-111">Имя типа</span><span class="sxs-lookup"><span data-stu-id="c76ba-111">Type name</span></span>                                                      | <span data-ttu-id="c76ba-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c76ba-112">Value</span></span> |
|----------------------------------------------------------------|-------|
| <span data-ttu-id="c76ba-113">Мсидбкустомактионтипеинсталл + Мсидбкустомактионтипесаурцефиле</span><span class="sxs-lookup"><span data-stu-id="c76ba-113">msidbCustomActionTypeInstall + msidbCustomActionTypeSourceFile</span></span> | <span data-ttu-id="c76ba-114">23</span><span class="sxs-lookup"><span data-stu-id="c76ba-114">23</span></span>    |



 

## <a name="target"></a><span data-ttu-id="c76ba-115">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="c76ba-115">Target</span></span>

<span data-ttu-id="c76ba-116">Целевое поле [таблицы CustomAction](customaction-table.md) содержит параметры свойств, которые должны быть переданы в параллельную установку.</span><span class="sxs-lookup"><span data-stu-id="c76ba-116">The Target field of the [CustomAction table](customaction-table.md) contains property settings that are to be passed to the concurrent installation.</span></span> <span data-ttu-id="c76ba-117">Эти параметры свойств могут задавать функции.</span><span class="sxs-lookup"><span data-stu-id="c76ba-117">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="c76ba-118">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="c76ba-118">Return Processing Options</span></span>

<span data-ttu-id="c76ba-119">Одновременный сеанс установки выполняется в виде отдельного потока в текущем процессе.</span><span class="sxs-lookup"><span data-stu-id="c76ba-119">The concurrent installation session runs as a separate thread in the current process.</span></span> <span data-ttu-id="c76ba-120">Параллельная установка не может выполняться асинхронно.</span><span class="sxs-lookup"><span data-stu-id="c76ba-120">A concurrent installation cannot run asynchronously.</span></span>

<span data-ttu-id="c76ba-121">Дополнительные сведения см. в разделе [Параметры обработки возвращаемых данных пользовательского действия](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="c76ba-121">For more information, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="c76ba-122">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="c76ba-122">Execution Scheduling Options</span></span>

<span data-ttu-id="c76ba-123">Доступны флаги параметров для управления возможным множественным выполнением пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="c76ba-123">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="c76ba-124">Дополнительные сведения см. в разделе [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="c76ba-124">For more information, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="c76ba-125">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="c76ba-125">In-Script Execution Options</span></span>

<span data-ttu-id="c76ba-126">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c76ba-126">Not used.</span></span>

## <a name="return-values"></a><span data-ttu-id="c76ba-127">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c76ba-127">Return Values</span></span>

<span data-ttu-id="c76ba-128">Возвращаемое состояние выхода пользователя, сбоя, приостановки или успешного выполнения при параллельной установке обрабатывается так же, как любое другое действие.</span><span class="sxs-lookup"><span data-stu-id="c76ba-128">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="c76ba-129">Однако обратите внимание, что установщик Windows преобразует возвращаемые значения из всех действий при записи возвращаемого значения в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="c76ba-129">Note however, that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="c76ba-130">Например, если возвращаемое значение действия отображается как 1 в файле журнала, это означает, что действие вернуло ошибку \_ успешно.</span><span class="sxs-lookup"><span data-stu-id="c76ba-130">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="c76ba-131">Дополнительные сведения см. в разделе [ведение журнала возвращаемых значений действий](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c76ba-131">For more information, see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="c76ba-132">Обратите внимание, что если во время параллельной установки установлено **мсидбкустомактионтипеконтинуе** , то возвращается сообщение об ошибке Install УСЕРЕКСИТ, ошибка Install rereboot, ошибка установить перезагрузку, \_ \_ \_ \_ \_ \_ \_ или \_ \_ требуется перезагрузка после успешного выполнения \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c76ba-132">Note that if a concurrent installation has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="c76ba-133">Это означает, что если вы настроили **мсидбкустомактионтипеконтинуе** и для параллельной установки требуется перезагрузка, требование перезагрузки будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="c76ba-133">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="c76ba-134">Кроме того, код ошибки из настраиваемого действия параллельной установки будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="c76ba-134">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="c76ba-135">Если **мсидбкустомактионтипеконтинуе** не задан, следующие коды возврата \_ и успешная ошибка будут считаться успешными и иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="c76ba-135">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="c76ba-136">Другие коды возврата обрабатываются как сбой.</span><span class="sxs-lookup"><span data-stu-id="c76ba-136">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="c76ba-137">Сообщение</span><span class="sxs-lookup"><span data-stu-id="c76ba-137">Message</span></span>                          | <span data-ttu-id="c76ba-138">Значение</span><span class="sxs-lookup"><span data-stu-id="c76ba-138">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c76ba-139">Ошибка при \_ установке \_ перезагрузки</span><span class="sxs-lookup"><span data-stu-id="c76ba-139">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="c76ba-140">В конце установки будет установлен флаг перезапуска.</span><span class="sxs-lookup"><span data-stu-id="c76ba-140">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="c76ba-141">Ошибка при \_ установке \_ перезагрузки \_</span><span class="sxs-lookup"><span data-stu-id="c76ba-141">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="c76ba-142">Перед завершением установки требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="c76ba-142">A restart is required before completing the installation.</span></span> <span data-ttu-id="c76ba-143">Перезагрузка будет обработана немедленно.</span><span class="sxs-lookup"><span data-stu-id="c76ba-143">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="c76ba-144">Ошибка \_ " \_ требуется перезагрузка при успешном выполнении" \_</span><span class="sxs-lookup"><span data-stu-id="c76ba-144">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="c76ba-145">Требуется перезагрузка, но она была подавлена.</span><span class="sxs-lookup"><span data-stu-id="c76ba-145">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="c76ba-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c76ba-146">Remarks</span></span>

<span data-ttu-id="c76ba-147">Условное выражение требуется для включения параллельной установки при установке или удалении связанного компонента или компонента.</span><span class="sxs-lookup"><span data-stu-id="c76ba-147">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c76ba-148">См. также</span><span class="sxs-lookup"><span data-stu-id="c76ba-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c76ba-149">Параллельные установки</span><span class="sxs-lookup"><span data-stu-id="c76ba-149">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="c76ba-150">Ссылка на настраиваемое действие</span><span class="sxs-lookup"><span data-stu-id="c76ba-150">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="c76ba-151">Сведения о настраиваемых действиях</span><span class="sxs-lookup"><span data-stu-id="c76ba-151">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="c76ba-152">Использование настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="c76ba-152">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="c76ba-153">Возвращаемые значения настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="c76ba-153">Custom Action Return Values</span></span>](custom-action-return-values.md)
</dt> </dl>

 

 



