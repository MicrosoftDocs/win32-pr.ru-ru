---
description: В таблице Мсисервицеконфиг настраивается служба, установленная или устанавливаемая текущим пакетом.
ms.assetid: 0d9fd005-9326-4a18-8496-35b5d1927f47
title: Таблица Мсисервицеконфиг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357b6787e56d52a893dd1a118a3e2fcbc13379e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664176"
---
# <a name="msiserviceconfig-table"></a><span data-ttu-id="ce82e-103">Таблица Мсисервицеконфиг</span><span class="sxs-lookup"><span data-stu-id="ce82e-103">MsiServiceConfig Table</span></span>

<span data-ttu-id="ce82e-104">В таблице Мсисервицеконфиг настраивается служба, установленная или устанавливаемая текущим пакетом.</span><span class="sxs-lookup"><span data-stu-id="ce82e-104">The MsiServiceConfig table configures a service that is installed or being installed by the current package.</span></span>

<span data-ttu-id="ce82e-105">**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ce82e-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="ce82e-106">Эта таблица доступна начиная с установщик Windows 5,0.</span><span class="sxs-lookup"><span data-stu-id="ce82e-106">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="ce82e-107">Таблица Мсисервицеконфиг содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="ce82e-107">The MsiServiceConfig table has the following columns.</span></span>



| <span data-ttu-id="ce82e-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="ce82e-108">Column</span></span>           | <span data-ttu-id="ce82e-109">Type</span><span class="sxs-lookup"><span data-stu-id="ce82e-109">Type</span></span>                         | <span data-ttu-id="ce82e-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="ce82e-110">Key</span></span> | <span data-ttu-id="ce82e-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="ce82e-111">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="ce82e-112">мсисервицеконфиг</span><span class="sxs-lookup"><span data-stu-id="ce82e-112">MsiServiceConfig</span></span> | [<span data-ttu-id="ce82e-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="ce82e-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="ce82e-114">Да</span><span class="sxs-lookup"><span data-stu-id="ce82e-114">Y</span></span>   | <span data-ttu-id="ce82e-115">Нет</span><span class="sxs-lookup"><span data-stu-id="ce82e-115">N</span></span>        |
| <span data-ttu-id="ce82e-116">Имя</span><span class="sxs-lookup"><span data-stu-id="ce82e-116">Name</span></span>             | [<span data-ttu-id="ce82e-117">Формате</span><span class="sxs-lookup"><span data-stu-id="ce82e-117">Formatted</span></span>](formatted.md)   | <span data-ttu-id="ce82e-118">Нет</span><span class="sxs-lookup"><span data-stu-id="ce82e-118">N</span></span>   | <span data-ttu-id="ce82e-119">Нет</span><span class="sxs-lookup"><span data-stu-id="ce82e-119">N</span></span>        |
| <span data-ttu-id="ce82e-120">Событие</span><span class="sxs-lookup"><span data-stu-id="ce82e-120">Event</span></span>            | [<span data-ttu-id="ce82e-121">Integer</span><span class="sxs-lookup"><span data-stu-id="ce82e-121">Integer</span></span>](integer.md)       | <span data-ttu-id="ce82e-122">Нет</span><span class="sxs-lookup"><span data-stu-id="ce82e-122">N</span></span>   | <span data-ttu-id="ce82e-123">Нет</span><span class="sxs-lookup"><span data-stu-id="ce82e-123">N</span></span>        |
| <span data-ttu-id="ce82e-124">ConfigType</span><span class="sxs-lookup"><span data-stu-id="ce82e-124">ConfigType</span></span>       | [<span data-ttu-id="ce82e-125">Integer</span><span class="sxs-lookup"><span data-stu-id="ce82e-125">Integer</span></span>](integer.md)       | <span data-ttu-id="ce82e-126">Нет</span><span class="sxs-lookup"><span data-stu-id="ce82e-126">N</span></span>   | <span data-ttu-id="ce82e-127">Нет</span><span class="sxs-lookup"><span data-stu-id="ce82e-127">N</span></span>        |
| <span data-ttu-id="ce82e-128">Аргумент</span><span class="sxs-lookup"><span data-stu-id="ce82e-128">Argument</span></span>         | [<span data-ttu-id="ce82e-129">Формате</span><span class="sxs-lookup"><span data-stu-id="ce82e-129">Formatted</span></span>](formatted.md)   | <span data-ttu-id="ce82e-130">Нет</span><span class="sxs-lookup"><span data-stu-id="ce82e-130">N</span></span>   | <span data-ttu-id="ce82e-131">Да</span><span class="sxs-lookup"><span data-stu-id="ce82e-131">Y</span></span>        |
| <span data-ttu-id="ce82e-132">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="ce82e-132">Component\_</span></span>      | [<span data-ttu-id="ce82e-133">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="ce82e-133">Identifier</span></span>](identifier.md) | <span data-ttu-id="ce82e-134">Нет</span><span class="sxs-lookup"><span data-stu-id="ce82e-134">N</span></span>   | <span data-ttu-id="ce82e-135">Нет</span><span class="sxs-lookup"><span data-stu-id="ce82e-135">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ce82e-136">Столбцы</span><span class="sxs-lookup"><span data-stu-id="ce82e-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ce82e-137"><span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>мсисервицеконфиг</span><span class="sxs-lookup"><span data-stu-id="ce82e-137"><span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig</span></span>
</dt> <dd>

<span data-ttu-id="ce82e-138">Это первичный ключ этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="ce82e-138">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="ce82e-139"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян</span><span class="sxs-lookup"><span data-stu-id="ce82e-139"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="ce82e-140">Этот столбец содержит имя службы, которая является частью этого пакета или уже установлена.</span><span class="sxs-lookup"><span data-stu-id="ce82e-140">This column contains the name of a service that is a part of this package or that is already is installed.</span></span>

</dd> <dt>

<span data-ttu-id="ce82e-141"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Журнале</span><span class="sxs-lookup"><span data-stu-id="ce82e-141"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="ce82e-142">В этом столбце указывается, когда следует изменять конфигурацию службы.</span><span class="sxs-lookup"><span data-stu-id="ce82e-142">This column specifies when to change the service configuration.</span></span> <span data-ttu-id="ce82e-143">Следующие значения можно комбинировать для представления нескольких операций.</span><span class="sxs-lookup"><span data-stu-id="ce82e-143">The following values can be combined to represent multiple operations.</span></span> <span data-ttu-id="ce82e-144">Любые значения, кроме указанных, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="ce82e-144">Any values included other than these are ignored.</span></span>



| <span data-ttu-id="ce82e-145">Константа</span><span class="sxs-lookup"><span data-stu-id="ce82e-145">Constant</span></span>                                         | <span data-ttu-id="ce82e-146">Описание</span><span class="sxs-lookup"><span data-stu-id="ce82e-146">Description</span></span>                                              |
|--------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="ce82e-147">**мсидбсервицеконфижевентинсталл** 1</span><span class="sxs-lookup"><span data-stu-id="ce82e-147">**msidbServiceConfigEventInstall** 1</span></span><br/>   | <span data-ttu-id="ce82e-148">Выполняет действие во время установки компонента.</span><span class="sxs-lookup"><span data-stu-id="ce82e-148">Takes the action during installation of the component.</span></span>   |
| <span data-ttu-id="ce82e-149">**мсидбсервицеконфижевентунинсталл** 2</span><span class="sxs-lookup"><span data-stu-id="ce82e-149">**msidbServiceConfigEventUninstall** 2</span></span><br/> | <span data-ttu-id="ce82e-150">Выполняет действие во время удаления компонента.</span><span class="sxs-lookup"><span data-stu-id="ce82e-150">Takes the action during uninstallation of the component.</span></span> |
| <span data-ttu-id="ce82e-151">**мсидбсервицеконфижевентреинсталл** 4</span><span class="sxs-lookup"><span data-stu-id="ce82e-151">**msidbServiceConfigEventReinstall** 4</span></span><br/> | <span data-ttu-id="ce82e-152">Выполняет действие во время повторной установки компонента.</span><span class="sxs-lookup"><span data-stu-id="ce82e-152">Takes the action during reinstallation of the component.</span></span> |



 

</dd> <dt>

<span data-ttu-id="ce82e-153"><span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType</span><span class="sxs-lookup"><span data-stu-id="ce82e-153"><span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType</span></span>
</dt> <dd>

<span data-ttu-id="ce82e-154">Значение в этом поле в сочетании со значением в поле Arguments (аргументы) указывает, какое изменение следует внести в конфигурацию службы.</span><span class="sxs-lookup"><span data-stu-id="ce82e-154">The value in this field, combined with the value in the Arguments field, specify what change to make to the service configuration.</span></span> <span data-ttu-id="ce82e-155">Указанное изменение вступает в силу при следующем запуске системы.</span><span class="sxs-lookup"><span data-stu-id="ce82e-155">The specified change takes effect the next time the system is started.</span></span>



| <span data-ttu-id="ce82e-156">Config</span><span class="sxs-lookup"><span data-stu-id="ce82e-156">Config</span></span>                                                      | <span data-ttu-id="ce82e-157">Описание</span><span class="sxs-lookup"><span data-stu-id="ce82e-157">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce82e-158">**Служба \_ \_Отложенная \_ Автоматическая \_ Загрузка конфигурации** 3</span><span class="sxs-lookup"><span data-stu-id="ce82e-158">**SERVICE\_CONFIG\_DELAYED\_AUTO\_START** 3</span></span><br/>       | <span data-ttu-id="ce82e-159">Настройка временной задержки [службы автоматического запуска](../services/automatically-starting-services.md).</span><span class="sxs-lookup"><span data-stu-id="ce82e-159">Configure the time delay of an [auto-start service](../services/automatically-starting-services.md).</span></span> <br/> <span data-ttu-id="ce82e-160">В поле argument (аргумент) введите 1, чтобы запустить службу после других служб с автозапуском и с задержкой.</span><span class="sxs-lookup"><span data-stu-id="ce82e-160">Enter 1 in the Argument field to start the service after other auto-start services plus a time delay.</span></span> <br/> <span data-ttu-id="ce82e-161">Введите 0 в поле Argument, чтобы отключить автоматическую задержку службы.</span><span class="sxs-lookup"><span data-stu-id="ce82e-161">Enter 0 in the Argument field to turn off the auto-start service delay.</span></span><br/> <span data-ttu-id="ce82e-162">Применяется только к установленным автозапуску служб или службам, установленным этим пакетом, с **\_ \_ автозапуском службы** в поле старттипе [таблицы сервицеинсталл](serviceinstall-table.md).</span><span class="sxs-lookup"><span data-stu-id="ce82e-162">Applies only to installed auto-start services or services installed by this package with **SERVICE\_AUTO\_START** in the StartType field of the [ServiceInstall table](serviceinstall-table.md).</span></span><br/>                                                                         |
| <span data-ttu-id="ce82e-163">**Служба \_ \_ \_ \_ Сведения о необходимых привилегиях конфигурации** 6</span><span class="sxs-lookup"><span data-stu-id="ce82e-163">**SERVICE\_CONFIG\_REQUIRED\_PRIVILEGES\_INFO** 6</span></span><br/> | <span data-ttu-id="ce82e-164">Измените список привилегий, необходимых для службы.</span><span class="sxs-lookup"><span data-stu-id="ce82e-164">Change the list of privileges required by the service.</span></span><br/> <span data-ttu-id="ce82e-165">Введите список запрошенных привилегий в поле Argument.</span><span class="sxs-lookup"><span data-stu-id="ce82e-165">Enter a list of requested privileges in the Argument field.</span></span> <span data-ttu-id="ce82e-166">[Форматированное](formatted.md) строковое значение в поле Argument перечисляет [**константы прав доступа**](../secauthz/privilege-constants.md) для запрошенных привилегий.</span><span class="sxs-lookup"><span data-stu-id="ce82e-166">The [Formatted](formatted.md) string value in the Argument field lists the [**Privilege Constants**](../secauthz/privilege-constants.md) for the requested privileges.</span></span> <span data-ttu-id="ce82e-167">\[ ~ \] Для вставки символа NULL можно использовать синтаксис [форматированной](formatted.md) строки.</span><span class="sxs-lookup"><span data-stu-id="ce82e-167">You can use the \[~\] syntax of the [Formatted](formatted.md) string to insert a null character.</span></span> <span data-ttu-id="ce82e-168">Разделите константы прав доступа в списке на \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="ce82e-168">Separate the privilege constants in the list by \[~\].</span></span><br/>                                                                                                                              |
| <span data-ttu-id="ce82e-169">**Служба \_ \_ \_ \_ Сведения о SID службы конфигурации** 5</span><span class="sxs-lookup"><span data-stu-id="ce82e-169">**SERVICE\_CONFIG\_SERVICE\_SID\_INFO** 5</span></span><br/>         | <span data-ttu-id="ce82e-170">Добавьте тип идентификатора безопасности службы в токен процесса, содержащий эту службу.</span><span class="sxs-lookup"><span data-stu-id="ce82e-170">Add a service SID type to the process token containing this service.</span></span><br/> <span data-ttu-id="ce82e-171">Введите в поле аргумента допустимый тип идентификатора безопасности службы для [**структуры \_ \_ сведений идентификатора безопасности**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) службы **: \_ тип идентификатора безопасности службы \_ \_** (0x00) **, \_ \_ тип идентификатора \_ безопасности службы** (0x03) или **\_ тип идентификатора безопасности службы без \_ \_ ограничений** (0x01).</span><span class="sxs-lookup"><span data-stu-id="ce82e-171">Enter in the Argument field a valid service SID type for the [**SERVICE\_SID\_INFO**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) structure: **SERVICE\_SID\_TYPE\_NONE** (0x00), **SERVICE\_SID\_TYPE\_RESTRICTED** (0x03), or **SERVICE\_SID\_TYPE\_UNRESTRICTED** (0x01).</span></span> <br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="ce82e-172">**Служба \_ \_ \_ Сведения о предзакрытии конфигурации** 7</span><span class="sxs-lookup"><span data-stu-id="ce82e-172">**SERVICE\_CONFIG\_PRESHUTDOWN\_INFO** 7</span></span><br/>          | <span data-ttu-id="ce82e-173">Настройте время ожидания [диспетчером управления службами](../services/service-control-manager.md) (SCM) перед продолжением других операций завершения работы.</span><span class="sxs-lookup"><span data-stu-id="ce82e-173">Configure the length of the time the [Service Control Manager](../services/service-control-manager.md) (SCM) waits before proceeding with other shutdown operations.</span></span> <span data-ttu-id="ce82e-174">SCM ожидает в течение этого периода времени после отправки уведомления о **\_ \_ завершении работы службы управления службой** .</span><span class="sxs-lookup"><span data-stu-id="ce82e-174">The SCM waits for this period of time after sending the **SERVICE\_CONTROL\_PRESHUTDOWN** notification to the service.</span></span> <br/> <span data-ttu-id="ce82e-175">Введите длину временной задержки в миллисекундах в поле Argument.</span><span class="sxs-lookup"><span data-stu-id="ce82e-175">Enter the time delay length, in milliseconds, in the Argument field.</span></span> <span data-ttu-id="ce82e-176">Оставьте поле Argument пустым, чтобы сбросить время задержки до значения по умолчанию (3 минуты).</span><span class="sxs-lookup"><span data-stu-id="ce82e-176">Leave the Argument field empty to reset the time delay to the default of 3 minutes.</span></span> <br/>                                                                                                                               |
| <span data-ttu-id="ce82e-177">**Служба \_ \_ \_ \_ Флаг действий при сбое конфигурации** 4</span><span class="sxs-lookup"><span data-stu-id="ce82e-177">**SERVICE\_CONFIG\_FAILURE\_ACTIONS\_FLAG** 4</span></span><br/>     | <span data-ttu-id="ce82e-178">Укажите, когда следует запускать действия при сбое для этой службы.</span><span class="sxs-lookup"><span data-stu-id="ce82e-178">Configure when to run the failure actions for this service.</span></span> <span data-ttu-id="ce82e-179">Этот параметр пропускается, если служба не имеет настроенных действий по ошибке.</span><span class="sxs-lookup"><span data-stu-id="ce82e-179">This setting is ignored if the service has no configured failure actions.</span></span><br/> <span data-ttu-id="ce82e-180">Введите 0, чтобы выполнить действия только в том случае, если служба завершает работу без **\_ остановки службы** отчетов.</span><span class="sxs-lookup"><span data-stu-id="ce82e-180">Enter 0 to run the actions only if the service terminates without reporting **SERVICE\_STOPPED**.</span></span><br/> <span data-ttu-id="ce82e-181">Введите 1, чтобы выполнить действия, если служба прекращает работу **службы отчетов \_** , а член **dwWin32ExitCode** структуры [**\_ состояния службы**](/windows/win32/api/winsvc/ns-winsvc-service_status) не **\_ прошел ошибку**.</span><span class="sxs-lookup"><span data-stu-id="ce82e-181">Enter 1 to run the actions if the service terminates reporting **SERVICE\_STOPPED** and the **dwWin32ExitCode** member of [**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) structure is not **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="ce82e-182">Настроенные действия при сбое также выполняются, если служба завершается без **\_ остановки службы** отчетов.</span><span class="sxs-lookup"><span data-stu-id="ce82e-182">Configured failure actions are also run if the service terminates without reporting **SERVICE\_STOPPED**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ce82e-183"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Параметр</span><span class="sxs-lookup"><span data-stu-id="ce82e-183"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="ce82e-184">Значение в этом поле в сочетании со значением в поле ConfigType укажите, какие изменения следует внести в конфигурацию службы.</span><span class="sxs-lookup"><span data-stu-id="ce82e-184">The value in this field, combined with the value in the ConfigType field, specify what change to make to the service configuration.</span></span> <span data-ttu-id="ce82e-185">Указанное изменение вступает в силу при следующем запуске системы.</span><span class="sxs-lookup"><span data-stu-id="ce82e-185">The specified change takes effect the next time the system is started.</span></span>

</dd> <dt>

<span data-ttu-id="ce82e-186"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="ce82e-186"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="ce82e-187">Внешний ключ к столбцу Component [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="ce82e-187">External key to the Component column of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="ce82e-188">Проверка</span><span class="sxs-lookup"><span data-stu-id="ce82e-188">Validation</span></span>

<dl>

[<span data-ttu-id="ce82e-189">ICE102</span><span class="sxs-lookup"><span data-stu-id="ce82e-189">ICE102</span></span>](ice-102.md)  
[<span data-ttu-id="ce82e-190">ICE03</span><span class="sxs-lookup"><span data-stu-id="ce82e-190">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ce82e-191">ICE06</span><span class="sxs-lookup"><span data-stu-id="ce82e-191">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ce82e-192">ICE32</span><span class="sxs-lookup"><span data-stu-id="ce82e-192">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="ce82e-193">ICE45</span><span class="sxs-lookup"><span data-stu-id="ce82e-193">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="ce82e-194">ICE46</span><span class="sxs-lookup"><span data-stu-id="ce82e-194">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="ce82e-195">ICE69</span><span class="sxs-lookup"><span data-stu-id="ce82e-195">ICE69</span></span>](ice69.md)  
</dl>

 

 
