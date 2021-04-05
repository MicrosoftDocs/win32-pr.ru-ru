---
description: Таблица ServiceControl используется для управления установленными или удаленными службами. Обратите внимание, что службы, зависящие от наличия сборки в глобальном кэше сборок (GAC), не могут быть установлены или запущены с помощью таблиц Сервицеинсталл и ServiceControl.
ms.assetid: c51cd9bd-3c55-4eec-ab67-172765adc51c
title: Таблица ServiceControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2abd123e937673694dffd53773a16fcbd704c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815192"
---
# <a name="servicecontrol-table"></a><span data-ttu-id="c3b93-103">Таблица ServiceControl</span><span class="sxs-lookup"><span data-stu-id="c3b93-103">ServiceControl Table</span></span>

<span data-ttu-id="c3b93-104">Таблица ServiceControl используется для управления установленными или удаленными службами.</span><span class="sxs-lookup"><span data-stu-id="c3b93-104">The ServiceControl table is used to control installed or uninstalled services.</span></span>

> [!Note]  
> <span data-ttu-id="c3b93-105">Службы, зависящие от наличия [сборки](assemblies.md) в глобальном кэше сборок (GAC), не могут быть установлены или запущены с помощью таблиц [сервицеинсталл](serviceinstall-table.md) и ServiceControl.</span><span class="sxs-lookup"><span data-stu-id="c3b93-105">Services that rely on the presence of an [assembly](assemblies.md) in the Global Assembly Cache (GAC) cannot be installed or started using the [ServiceInstall](serviceinstall-table.md) and ServiceControl tables.</span></span> <span data-ttu-id="c3b93-106">Если необходимо запустить службу, которая зависит от сборки в глобальном кэше сборок, необходимо использовать настраиваемое действие, упорядоченное после [действия функции InstallFinalize](installfinalize-action.md) или [действия фиксации](commit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="c3b93-106">If you need to start a service that depends on an assembly in the GAC, you must use a custom action sequenced after the [InstallFinalize action](installfinalize-action.md) or a [commit custom action](commit-custom-actions.md).</span></span> <span data-ttu-id="c3b93-107">Дополнительные сведения об установке сборок в глобальном кэше сборок см. в разделе [Установка сборок в глобальный кэш сборок](installation-of-assemblies-to-the-global-assembly-cache.md).</span><span class="sxs-lookup"><span data-stu-id="c3b93-107">For information about installing assemblies to the GAC see [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md).</span></span>

 

<span data-ttu-id="c3b93-108">Таблица ServiceControl содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="c3b93-108">The ServiceControl table has the following columns.</span></span>



| <span data-ttu-id="c3b93-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="c3b93-109">Column</span></span>         | <span data-ttu-id="c3b93-110">Type</span><span class="sxs-lookup"><span data-stu-id="c3b93-110">Type</span></span>                         | <span data-ttu-id="c3b93-111">Ключ</span><span class="sxs-lookup"><span data-stu-id="c3b93-111">Key</span></span> | <span data-ttu-id="c3b93-112">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="c3b93-112">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="c3b93-113">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="c3b93-113">ServiceControl</span></span> | [<span data-ttu-id="c3b93-114">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="c3b93-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="c3b93-115">Да</span><span class="sxs-lookup"><span data-stu-id="c3b93-115">Y</span></span>   | <span data-ttu-id="c3b93-116">Нет</span><span class="sxs-lookup"><span data-stu-id="c3b93-116">N</span></span>        |
| <span data-ttu-id="c3b93-117">Имя</span><span class="sxs-lookup"><span data-stu-id="c3b93-117">Name</span></span>           | [<span data-ttu-id="c3b93-118">Формате</span><span class="sxs-lookup"><span data-stu-id="c3b93-118">Formatted</span></span>](formatted.md)   | <span data-ttu-id="c3b93-119">Нет</span><span class="sxs-lookup"><span data-stu-id="c3b93-119">N</span></span>   | <span data-ttu-id="c3b93-120">Нет</span><span class="sxs-lookup"><span data-stu-id="c3b93-120">N</span></span>        |
| <span data-ttu-id="c3b93-121">Событие</span><span class="sxs-lookup"><span data-stu-id="c3b93-121">Event</span></span>          | [<span data-ttu-id="c3b93-122">Integer</span><span class="sxs-lookup"><span data-stu-id="c3b93-122">Integer</span></span>](integer.md)       | <span data-ttu-id="c3b93-123">Нет</span><span class="sxs-lookup"><span data-stu-id="c3b93-123">N</span></span>   | <span data-ttu-id="c3b93-124">Нет</span><span class="sxs-lookup"><span data-stu-id="c3b93-124">N</span></span>        |
| <span data-ttu-id="c3b93-125">Аргументы</span><span class="sxs-lookup"><span data-stu-id="c3b93-125">Arguments</span></span>      | [<span data-ttu-id="c3b93-126">Формате</span><span class="sxs-lookup"><span data-stu-id="c3b93-126">Formatted</span></span>](formatted.md)   | <span data-ttu-id="c3b93-127">Нет</span><span class="sxs-lookup"><span data-stu-id="c3b93-127">N</span></span>   | <span data-ttu-id="c3b93-128">Да</span><span class="sxs-lookup"><span data-stu-id="c3b93-128">Y</span></span>        |
| <span data-ttu-id="c3b93-129">Ожидание</span><span class="sxs-lookup"><span data-stu-id="c3b93-129">Wait</span></span>           | [<span data-ttu-id="c3b93-130">Integer</span><span class="sxs-lookup"><span data-stu-id="c3b93-130">Integer</span></span>](integer.md)       | <span data-ttu-id="c3b93-131">Нет</span><span class="sxs-lookup"><span data-stu-id="c3b93-131">N</span></span>   | <span data-ttu-id="c3b93-132">Да</span><span class="sxs-lookup"><span data-stu-id="c3b93-132">Y</span></span>        |
| <span data-ttu-id="c3b93-133">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="c3b93-133">Component\_</span></span>    | [<span data-ttu-id="c3b93-134">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="c3b93-134">Identifier</span></span>](identifier.md) | <span data-ttu-id="c3b93-135">Нет</span><span class="sxs-lookup"><span data-stu-id="c3b93-135">N</span></span>   | <span data-ttu-id="c3b93-136">Нет</span><span class="sxs-lookup"><span data-stu-id="c3b93-136">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c3b93-137">Столбцы</span><span class="sxs-lookup"><span data-stu-id="c3b93-137">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c3b93-138"><span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl</span><span class="sxs-lookup"><span data-stu-id="c3b93-138"><span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl</span></span>
</dt> <dd>

<span data-ttu-id="c3b93-139">Это первичный ключ этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="c3b93-139">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="c3b93-140"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян</span><span class="sxs-lookup"><span data-stu-id="c3b93-140"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="c3b93-141">Этот столбец представляет собой строку именования службы.</span><span class="sxs-lookup"><span data-stu-id="c3b93-141">This column is the string naming the service.</span></span> <span data-ttu-id="c3b93-142">Этот столбец можно использовать для управления службой, которая не установлена.</span><span class="sxs-lookup"><span data-stu-id="c3b93-142">This column can be used to control a service that is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="c3b93-143"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Журнале</span><span class="sxs-lookup"><span data-stu-id="c3b93-143"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="c3b93-144">Этот столбец содержит операции, выполняемые с помощью именованной службы.</span><span class="sxs-lookup"><span data-stu-id="c3b93-144">This column contains the operations to be performed on the named service.</span></span> <span data-ttu-id="c3b93-145">Обратите внимание, что при остановке службы также останавливаются все службы, зависящие от этой службы.</span><span class="sxs-lookup"><span data-stu-id="c3b93-145">Note that when stopping a service, all services that depend on that service are also stopped.</span></span> <span data-ttu-id="c3b93-146">При удалении службы, которая работает, установщик останавливает службу.</span><span class="sxs-lookup"><span data-stu-id="c3b93-146">When deleting a service that is running, the installer stops the service.</span></span>

<span data-ttu-id="c3b93-147">Значения в этом поле являются битовыми полями, которые можно объединить в одно значение, представляющее несколько операций.</span><span class="sxs-lookup"><span data-stu-id="c3b93-147">The values in this field are bit fields that can be combined into a single value that represents several operations.</span></span>

<span data-ttu-id="c3b93-148">Следующие значения используются только во время установки.</span><span class="sxs-lookup"><span data-stu-id="c3b93-148">The following values are only used during an installation.</span></span>



| <span data-ttu-id="c3b93-149">Константа</span><span class="sxs-lookup"><span data-stu-id="c3b93-149">Constant</span></span>                           | <span data-ttu-id="c3b93-150">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="c3b93-150">Hexadecimal</span></span> | <span data-ttu-id="c3b93-151">Decimal</span><span class="sxs-lookup"><span data-stu-id="c3b93-151">Decimal</span></span> | <span data-ttu-id="c3b93-152">Описание</span><span class="sxs-lookup"><span data-stu-id="c3b93-152">Description</span></span>                                                                        |
|------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3b93-153">**мсидбсервицеконтролевентстарт**</span><span class="sxs-lookup"><span data-stu-id="c3b93-153">**msidbServiceControlEventStart**</span></span>  | <span data-ttu-id="c3b93-154">0x001</span><span class="sxs-lookup"><span data-stu-id="c3b93-154">0x001</span></span>       | <span data-ttu-id="c3b93-155">1</span><span class="sxs-lookup"><span data-stu-id="c3b93-155">1</span></span>       | <span data-ttu-id="c3b93-156">Запускает службу во время [действия стартсервицес](startservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="c3b93-156">Starts the service during the [StartServices action](startservices-action.md).</span></span>    |
| <span data-ttu-id="c3b93-157">**мсидбсервицеконтролевентстоп**</span><span class="sxs-lookup"><span data-stu-id="c3b93-157">**msidbServiceControlEventStop**</span></span>   | <span data-ttu-id="c3b93-158">0x002</span><span class="sxs-lookup"><span data-stu-id="c3b93-158">0x002</span></span>       | <span data-ttu-id="c3b93-159">2</span><span class="sxs-lookup"><span data-stu-id="c3b93-159">2</span></span>       | <span data-ttu-id="c3b93-160">Останавливает службу во время [действия стопсервицес](stopservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="c3b93-160">Stops the service during the [StopServices action](stopservices-action.md).</span></span>       |
| <span data-ttu-id="c3b93-161">(нет)</span><span class="sxs-lookup"><span data-stu-id="c3b93-161">(none)</span></span>                             | <span data-ttu-id="c3b93-162">0x004</span><span class="sxs-lookup"><span data-stu-id="c3b93-162">0x004</span></span>       | <span data-ttu-id="c3b93-163">4</span><span class="sxs-lookup"><span data-stu-id="c3b93-163">4</span></span>       | <reserved>                                                                   |
| <span data-ttu-id="c3b93-164">**мсидбсервицеконтролевентделете**</span><span class="sxs-lookup"><span data-stu-id="c3b93-164">**msidbServiceControlEventDelete**</span></span> | <span data-ttu-id="c3b93-165">0x008</span><span class="sxs-lookup"><span data-stu-id="c3b93-165">0x008</span></span>       | <span data-ttu-id="c3b93-166">8</span><span class="sxs-lookup"><span data-stu-id="c3b93-166">8</span></span>       | <span data-ttu-id="c3b93-167">Удаляет службу во время [действия делетесервицес](deleteservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="c3b93-167">Deletes the service during the [DeleteServices action](deleteservices-action.md).</span></span> |



 

<span data-ttu-id="c3b93-168">Следующие значения используются только во время удаления.</span><span class="sxs-lookup"><span data-stu-id="c3b93-168">The following values are only used during an uninstall.</span></span>



| <span data-ttu-id="c3b93-169">Константа</span><span class="sxs-lookup"><span data-stu-id="c3b93-169">Constant</span></span>                                    | <span data-ttu-id="c3b93-170">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="c3b93-170">Hexadecimal</span></span> | <span data-ttu-id="c3b93-171">Decimal</span><span class="sxs-lookup"><span data-stu-id="c3b93-171">Decimal</span></span> | <span data-ttu-id="c3b93-172">Описание</span><span class="sxs-lookup"><span data-stu-id="c3b93-172">Description</span></span>                                                                        |
|---------------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3b93-173">**мсидбсервицеконтролевентунинсталлстарт**</span><span class="sxs-lookup"><span data-stu-id="c3b93-173">**msidbServiceControlEventUninstallStart**</span></span>  | <span data-ttu-id="c3b93-174">0x010</span><span class="sxs-lookup"><span data-stu-id="c3b93-174">0x010</span></span>       | <span data-ttu-id="c3b93-175">16</span><span class="sxs-lookup"><span data-stu-id="c3b93-175">16</span></span>      | <span data-ttu-id="c3b93-176">Запускает службу во время [действия стартсервицес](startservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="c3b93-176">Starts the service during the [StartServices action](startservices-action.md).</span></span>    |
| <span data-ttu-id="c3b93-177">**мсидбсервицеконтролевентунинсталлстоп**</span><span class="sxs-lookup"><span data-stu-id="c3b93-177">**msidbServiceControlEventUninstallStop**</span></span>   | <span data-ttu-id="c3b93-178">0x020</span><span class="sxs-lookup"><span data-stu-id="c3b93-178">0x020</span></span>       | <span data-ttu-id="c3b93-179">32</span><span class="sxs-lookup"><span data-stu-id="c3b93-179">32</span></span>      | <span data-ttu-id="c3b93-180">Останавливает службу во время [действия стопсервицес](stopservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="c3b93-180">Stops the service during the [StopServices action](stopservices-action.md).</span></span>       |
| <span data-ttu-id="c3b93-181">(нет)</span><span class="sxs-lookup"><span data-stu-id="c3b93-181">(none)</span></span>                                      | <span data-ttu-id="c3b93-182">0x040</span><span class="sxs-lookup"><span data-stu-id="c3b93-182">0x040</span></span>       | <span data-ttu-id="c3b93-183">64</span><span class="sxs-lookup"><span data-stu-id="c3b93-183">64</span></span>      | <reserved>                                                                   |
| <span data-ttu-id="c3b93-184">**мсидбсервицеконтролевентунинсталлделете**</span><span class="sxs-lookup"><span data-stu-id="c3b93-184">**msidbServiceControlEventUninstallDelete**</span></span> | <span data-ttu-id="c3b93-185">0x080</span><span class="sxs-lookup"><span data-stu-id="c3b93-185">0x080</span></span>       | <span data-ttu-id="c3b93-186">128</span><span class="sxs-lookup"><span data-stu-id="c3b93-186">128</span></span>     | <span data-ttu-id="c3b93-187">Удаляет службу во время [действия делетесервицес](deleteservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="c3b93-187">Deletes the service during the [DeleteServices action](deleteservices-action.md).</span></span> |



 

</dd> <dt>

<span data-ttu-id="c3b93-188"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Даваемых</span><span class="sxs-lookup"><span data-stu-id="c3b93-188"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span></span>
</dt> <dd>

<span data-ttu-id="c3b93-189">Список аргументов для запуска служб.</span><span class="sxs-lookup"><span data-stu-id="c3b93-189">A list of arguments for starting services.</span></span> <span data-ttu-id="c3b93-190">Аргументы разделяются символами NULL \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="c3b93-190">The arguments are separated by null characters \[~\].</span></span> <span data-ttu-id="c3b93-191">Например, список аргументов один, два и три перечислены как: один \[ ~ \] два \[ ~ \] три.</span><span class="sxs-lookup"><span data-stu-id="c3b93-191">For example, the list of arguments One, Two, and Three are listed as: One\[~\]Two\[~\]Three.</span></span>

</dd> <dt>

<span data-ttu-id="c3b93-192"><span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Ожидания</span><span class="sxs-lookup"><span data-stu-id="c3b93-192"><span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Wait</span></span>
</dt> <dd>

<span data-ttu-id="c3b93-193">Если это поле не задано или вводится значение 1, установщик ожидает завершения работы службы до 30 секунд, прежде чем продолжать работу.</span><span class="sxs-lookup"><span data-stu-id="c3b93-193">Leaving this field null or entering a value of 1 causes the installer to wait a maximum of 30 seconds for the service to complete before proceeding.</span></span> <span data-ttu-id="c3b93-194">Ожидание может быть использовано для того, чтобы дополнительное время для получения критического события возвращало ошибку сбоя.</span><span class="sxs-lookup"><span data-stu-id="c3b93-194">The wait can be used to allow additional time for a critical event to return a failure error.</span></span> <span data-ttu-id="c3b93-195">Значение 0 в этом поле означает ожидание до тех пор, пока диспетчер управления службами не сообщит о том, что эта служба находится в состоянии ожидания, прежде чем продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="c3b93-195">A value of 0 in this field means to wait only until the service control manager (SCM) reports that this service is in a pending state before continuing with the installation.</span></span>

</dd> <dt>

<span data-ttu-id="c3b93-196"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="c3b93-196"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="c3b93-197">Внешний ключ к столбцу одной из [таблиц Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="c3b93-197">External key to column one of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3b93-198">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3b93-198">Remarks</span></span>

<span data-ttu-id="c3b93-199">Действия [стартсервицес](startservices-action.md), [стопсервицес](stopservices-action.md)и [делетесервицес](deleteservices-action.md) в [*таблицах последовательностей*](s-gly.md) обрабатывают сведения, приведенные в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="c3b93-199">The [StartServices](startservices-action.md), [StopServices](stopservices-action.md), and [DeleteServices](deleteservices-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="c3b93-200">Дополнительные сведения об использовании *таблиц последовательности* см. [в разделе Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="c3b93-200">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="c3b93-201">Столбец имя используется для запуска, завершения или удаления служб, которые заменяются установкой или зависят от новой устанавливаемой службы.</span><span class="sxs-lookup"><span data-stu-id="c3b93-201">Use the Name column to start, stop, or delete services that are being replaced by the installation or that are dependent upon a new service that is being installed.</span></span> <span data-ttu-id="c3b93-202">Например, ввод MyService в столбец ServiceControl может связать эту службу с MyComponent в \_ столбце Component.</span><span class="sxs-lookup"><span data-stu-id="c3b93-202">For example, entering MyService into the ServiceControl column can tie this service to MyComponent in the Component\_ column.</span></span> <span data-ttu-id="c3b93-203">Если битовое поле в столбце событий задано для запуска во время установки, то установщик запускает MyService при установке MyComponent.</span><span class="sxs-lookup"><span data-stu-id="c3b93-203">If the bit field in the Event column is set for start while installing, then the installer starts MyService when installing MyComponent.</span></span>

## <a name="validation"></a><span data-ttu-id="c3b93-204">Проверка</span><span class="sxs-lookup"><span data-stu-id="c3b93-204">Validation</span></span>

<dl>

[<span data-ttu-id="c3b93-205">ICE03</span><span class="sxs-lookup"><span data-stu-id="c3b93-205">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c3b93-206">ICE06</span><span class="sxs-lookup"><span data-stu-id="c3b93-206">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c3b93-207">ICE32</span><span class="sxs-lookup"><span data-stu-id="c3b93-207">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="c3b93-208">ICE45</span><span class="sxs-lookup"><span data-stu-id="c3b93-208">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="c3b93-209">ICE46</span><span class="sxs-lookup"><span data-stu-id="c3b93-209">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="c3b93-210">ICE69</span><span class="sxs-lookup"><span data-stu-id="c3b93-210">ICE69</span></span>](ice69.md)  
</dl>

 

 



