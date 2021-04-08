---
description: Разработчики установщик Windowsных пакетов могут использовать настраиваемое действие типа 39, если стандартные действия недостаточны для выполнения установки.
ms.assetid: edf96cc6-ef32-4660-b4ee-50c130626e15
title: Тип настраиваемого действия 39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49667fbad6e71aa8b2197b00ae9dd49f7dfff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910708"
---
# <a name="custom-action-type-39"></a><span data-ttu-id="f9d4e-103">Тип настраиваемого действия 39</span><span class="sxs-lookup"><span data-stu-id="f9d4e-103">Custom Action Type 39</span></span>

<span data-ttu-id="f9d4e-104">Тип настраиваемого действия 39 используется с параллельными установками.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-104">The Custom Action Type 39 is used with concurrent installations.</span></span> <span data-ttu-id="f9d4e-105">Параллельные установки не рекомендуются для установки приложений, предназначенных для выпуска в общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="f9d4e-106">Сведения о параллельных установках см. в разделе [одновременная установка](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="f9d4e-106">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="f9d4e-107">Тип 39 настраиваемое действие устанавливает приложение, которое объявлено или уже установлено.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-107">Type 39 custom action installs an application that is advertised or already installed.</span></span> <span data-ttu-id="f9d4e-108">Этот тип настраиваемого действия может использоваться для переустановки или удаления продукта, установленного в качестве параллельной установки текущего пакета установки продукта.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-108">This custom action type may be used to reinstall or remove a product that has been installed as a concurrent installation by the current product's installation package.</span></span> <span data-ttu-id="f9d4e-109">Настраиваемое действие Type 39 нельзя использовать для переустановки или удаления любого продукта, установленного ранее другими способами.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-109">The Type 39 custom action cannot be used to reinstall or remove any product previously installed by any other means.</span></span> <span data-ttu-id="f9d4e-110">Например, если дополнительный продукт установлен с помощью настраиваемого действия типа 39, типа 23 или 7 во время установки основного продукта, то для удаления дополнительного продукта при удалении основного продукта может использоваться настраиваемое действие типа 39.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-110">For example, if the secondary product is installed using a Type 39, Type 23, or Type 7 custom action during the installation of the primary product, a Type 39 custom action may be used to remove the secondary product when the primary product is uninstalled.</span></span>

## <a name="source"></a><span data-ttu-id="f9d4e-111">Источник</span><span class="sxs-lookup"><span data-stu-id="f9d4e-111">Source</span></span>

<span data-ttu-id="f9d4e-112">Поле Source [таблицы CustomAction](customaction-table.md) содержит код продукта для приложения.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-112">The Source field of the [CustomAction table](customaction-table.md) contains the product code for the application.</span></span>

## <a name="numeric-type"></a><span data-ttu-id="f9d4e-113">Числовой тип</span><span class="sxs-lookup"><span data-stu-id="f9d4e-113">Numeric Type</span></span>



| <span data-ttu-id="f9d4e-114">Имя типа</span><span class="sxs-lookup"><span data-stu-id="f9d4e-114">Type name</span></span>                                                     | <span data-ttu-id="f9d4e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f9d4e-115">Value</span></span> |
|---------------------------------------------------------------|-------|
| <span data-ttu-id="f9d4e-116">Мсидбкустомактионтипеинсталл + Мсидбкустомактионтипедиректори</span><span class="sxs-lookup"><span data-stu-id="f9d4e-116">msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory</span></span> | <span data-ttu-id="f9d4e-117">39</span><span class="sxs-lookup"><span data-stu-id="f9d4e-117">39</span></span>    |



 

## <a name="target"></a><span data-ttu-id="f9d4e-118">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="f9d4e-118">Target</span></span>

<span data-ttu-id="f9d4e-119">Целевое поле [таблицы CustomAction](customaction-table.md) содержит параметры свойств, которые должны быть переданы в параллельную установку.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-119">The Target field of the [CustomAction table](customaction-table.md) contains property settings that are to be passed to the concurrent installation.</span></span> <span data-ttu-id="f9d4e-120">Эти параметры свойств могут задавать функции.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-120">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="f9d4e-121">Параметры обработки возвращаемых значений</span><span class="sxs-lookup"><span data-stu-id="f9d4e-121">Return Processing Options</span></span>

<span data-ttu-id="f9d4e-122">Тип настраиваемого действия 39 завершается ошибкой, если приложение не объявлено или установлено.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-122">The custom action type 39 fails if the application is not advertised or installed.</span></span> <span data-ttu-id="f9d4e-123">Чтобы избежать этой ошибки, необходимо задать параметр **мсидбкустомактионтипеконтинуефлаг**.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-123">To avoid this failure, you must set the **msidbCustomActionTypeContinueflag**.</span></span>

<span data-ttu-id="f9d4e-124">Параллельная установка не может выполняться асинхронно.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-124">A concurrent install cannot run asynchronously.</span></span>

<span data-ttu-id="f9d4e-125">См. раздел [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="f9d4e-125">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="f9d4e-126">Параметры планирования выполнения</span><span class="sxs-lookup"><span data-stu-id="f9d4e-126">Execution Scheduling Options</span></span>

<span data-ttu-id="f9d4e-127">Доступны флаги параметров для управления возможным множественным выполнением пользовательских действий.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-127">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="f9d4e-128">См. раздел [Параметры планирования выполнения пользовательских действий](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="f9d4e-128">See [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="f9d4e-129">Параметры выполнения In-Script</span><span class="sxs-lookup"><span data-stu-id="f9d4e-129">In-Script Execution Options</span></span>

<span data-ttu-id="f9d4e-130">В настраиваемом действии этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-130">The custom action does not use this option.</span></span>

## <a name="return-values"></a><span data-ttu-id="f9d4e-131">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f9d4e-131">Return Values</span></span>

<span data-ttu-id="f9d4e-132">Возвращаемое состояние выхода пользователя, сбоя, приостановки или успешного выполнения при параллельной установке обрабатывается так же, как любое другое действие.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-132">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="f9d4e-133">Обратите внимание, что установщик Windows преобразует возвращаемые значения из всех действий при записи возвращаемого значения в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-133">Note however that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="f9d4e-134">Например, если возвращаемое значение действия отображается как 1 в файле журнала, это означает, что действие вернуло ошибку \_ успешно.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-134">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="f9d4e-135">Дополнительные сведения см. в разделе [ведение журнала возвращаемых значений действий](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f9d4e-135">For more information, see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="f9d4e-136">Обратите внимание, что если во время параллельной установки установлено **мсидбкустомактионтипеконтинуе** , то возвращается сообщение об ошибке Install УСЕРЕКСИТ, ошибка Install rereboot, ошибка установить перезагрузку, \_ \_ \_ \_ \_ \_ \_ или \_ \_ требуется перезагрузка после успешного выполнения \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f9d4e-136">Note that if a concurrent installation has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="f9d4e-137">Это означает, что если вы настроили **мсидбкустомактионтипеконтинуе** и для параллельной установки требуется перезагрузка, требование перезагрузки будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-137">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="f9d4e-138">Кроме того, код ошибки из настраиваемого действия параллельной установки будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-138">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="f9d4e-139">Если **мсидбкустомактионтипеконтинуе** не задан, следующие коды возврата \_ и успешная ошибка будут считаться успешными и иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-139">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="f9d4e-140">Другие коды возврата обрабатываются как сбой.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-140">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="f9d4e-141">Сообщение</span><span class="sxs-lookup"><span data-stu-id="f9d4e-141">Message</span></span>                          | <span data-ttu-id="f9d4e-142">Значение</span><span class="sxs-lookup"><span data-stu-id="f9d4e-142">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9d4e-143">Ошибка при \_ установке \_ перезагрузки</span><span class="sxs-lookup"><span data-stu-id="f9d4e-143">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="f9d4e-144">В конце установки будет установлен флаг перезапуска.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-144">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="f9d4e-145">Ошибка при \_ установке \_ перезагрузки \_</span><span class="sxs-lookup"><span data-stu-id="f9d4e-145">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="f9d4e-146">Перед завершением установки требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-146">A restart is required before completing the installation.</span></span> <span data-ttu-id="f9d4e-147">Перезагрузка будет обработана немедленно.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-147">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="f9d4e-148">Ошибка \_ " \_ требуется перезагрузка при успешном выполнении" \_</span><span class="sxs-lookup"><span data-stu-id="f9d4e-148">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="f9d4e-149">Требуется перезагрузка, но она была подавлена.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-149">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="f9d4e-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9d4e-150">Remarks</span></span>

<span data-ttu-id="f9d4e-151">Условное выражение требуется для включения параллельной установки при установке или удалении связанного компонента или компонента.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-151">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9d4e-152">См. также</span><span class="sxs-lookup"><span data-stu-id="f9d4e-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9d4e-153">Параллельные установки</span><span class="sxs-lookup"><span data-stu-id="f9d4e-153">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="f9d4e-154">Ссылка на настраиваемое действие</span><span class="sxs-lookup"><span data-stu-id="f9d4e-154">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="f9d4e-155">Сведения о настраиваемых действиях</span><span class="sxs-lookup"><span data-stu-id="f9d4e-155">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="f9d4e-156">Использование настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="f9d4e-156">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 



