---
description: В таблице Мсисервицеконфигфаилуреактионс перечисляются операции, выполняемые после сбоя службы. Операции, указанные в этой таблице, запускаются при следующей загрузке системы.
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: Таблица Мсисервицеконфигфаилуреактионс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae55d095e227611271de35d673289fc9eb5b174e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664175"
---
# <a name="msiserviceconfigfailureactions-table"></a><span data-ttu-id="f1d00-104">Таблица Мсисервицеконфигфаилуреактионс</span><span class="sxs-lookup"><span data-stu-id="f1d00-104">MsiServiceConfigFailureActions Table</span></span>

<span data-ttu-id="f1d00-105">В таблице Мсисервицеконфигфаилуреактионс перечисляются операции, выполняемые после сбоя службы.</span><span class="sxs-lookup"><span data-stu-id="f1d00-105">The MsiServiceConfigFailureActions table lists operations to be run after a service fails.</span></span> <span data-ttu-id="f1d00-106">Операции, указанные в этой таблице, запускаются при следующей загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="f1d00-106">The operations specified in this table run the next time the system is started.</span></span>

<span data-ttu-id="f1d00-107">**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f1d00-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="f1d00-108">Эта таблица доступна начиная с установщик Windows 5,0.</span><span class="sxs-lookup"><span data-stu-id="f1d00-108">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="f1d00-109">Таблица Мсисервицеконфигфаилуреактионс содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="f1d00-109">The MsiServiceConfigFailureActions table has the following columns.</span></span>



| <span data-ttu-id="f1d00-110">Столбец</span><span class="sxs-lookup"><span data-stu-id="f1d00-110">Column</span></span>                         | <span data-ttu-id="f1d00-111">Type</span><span class="sxs-lookup"><span data-stu-id="f1d00-111">Type</span></span>                         | <span data-ttu-id="f1d00-112">Ключ</span><span class="sxs-lookup"><span data-stu-id="f1d00-112">Key</span></span> | <span data-ttu-id="f1d00-113">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="f1d00-113">Nullable</span></span> |
|--------------------------------|------------------------------|-----|----------|
| <span data-ttu-id="f1d00-114">мсисервицеконфигфаилуреактионс</span><span class="sxs-lookup"><span data-stu-id="f1d00-114">MsiServiceConfigFailureActions</span></span> | [<span data-ttu-id="f1d00-115">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="f1d00-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="f1d00-116">Да</span><span class="sxs-lookup"><span data-stu-id="f1d00-116">Y</span></span>   | <span data-ttu-id="f1d00-117">Нет</span><span class="sxs-lookup"><span data-stu-id="f1d00-117">N</span></span>        |
| <span data-ttu-id="f1d00-118">Имя</span><span class="sxs-lookup"><span data-stu-id="f1d00-118">Name</span></span>                           | [<span data-ttu-id="f1d00-119">Формате</span><span class="sxs-lookup"><span data-stu-id="f1d00-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="f1d00-120">Нет</span><span class="sxs-lookup"><span data-stu-id="f1d00-120">N</span></span>   | <span data-ttu-id="f1d00-121">Нет</span><span class="sxs-lookup"><span data-stu-id="f1d00-121">N</span></span>        |
| <span data-ttu-id="f1d00-122">Событие</span><span class="sxs-lookup"><span data-stu-id="f1d00-122">Event</span></span>                          | [<span data-ttu-id="f1d00-123">Integer</span><span class="sxs-lookup"><span data-stu-id="f1d00-123">Integer</span></span>](integer.md)       | <span data-ttu-id="f1d00-124">Нет</span><span class="sxs-lookup"><span data-stu-id="f1d00-124">N</span></span>   | <span data-ttu-id="f1d00-125">Нет</span><span class="sxs-lookup"><span data-stu-id="f1d00-125">N</span></span>        |
| <span data-ttu-id="f1d00-126">ресетпериод</span><span class="sxs-lookup"><span data-stu-id="f1d00-126">ResetPeriod</span></span>                    | [<span data-ttu-id="f1d00-127">Integer</span><span class="sxs-lookup"><span data-stu-id="f1d00-127">Integer</span></span>](integer.md)       | <span data-ttu-id="f1d00-128">Нет</span><span class="sxs-lookup"><span data-stu-id="f1d00-128">N</span></span>   | <span data-ttu-id="f1d00-129">Да</span><span class="sxs-lookup"><span data-stu-id="f1d00-129">Y</span></span>        |
| <span data-ttu-id="f1d00-130">ребутмессаже</span><span class="sxs-lookup"><span data-stu-id="f1d00-130">RebootMessage</span></span>                  | [<span data-ttu-id="f1d00-131">Формате</span><span class="sxs-lookup"><span data-stu-id="f1d00-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="f1d00-132">Нет</span><span class="sxs-lookup"><span data-stu-id="f1d00-132">N</span></span>   | <span data-ttu-id="f1d00-133">Да</span><span class="sxs-lookup"><span data-stu-id="f1d00-133">Y</span></span>        |
| <span data-ttu-id="f1d00-134">Get-Help</span><span class="sxs-lookup"><span data-stu-id="f1d00-134">Command</span></span>                        | [<span data-ttu-id="f1d00-135">Формате</span><span class="sxs-lookup"><span data-stu-id="f1d00-135">Formatted</span></span>](formatted.md)   | <span data-ttu-id="f1d00-136">Нет</span><span class="sxs-lookup"><span data-stu-id="f1d00-136">N</span></span>   | <span data-ttu-id="f1d00-137">Да</span><span class="sxs-lookup"><span data-stu-id="f1d00-137">Y</span></span>        |
| <span data-ttu-id="f1d00-138">Действия</span><span class="sxs-lookup"><span data-stu-id="f1d00-138">Actions</span></span>                        | [<span data-ttu-id="f1d00-139">Text</span><span class="sxs-lookup"><span data-stu-id="f1d00-139">Text</span></span>](text.md)             | <span data-ttu-id="f1d00-140">Нет</span><span class="sxs-lookup"><span data-stu-id="f1d00-140">N</span></span>   | <span data-ttu-id="f1d00-141">Да</span><span class="sxs-lookup"><span data-stu-id="f1d00-141">Y</span></span>        |
| <span data-ttu-id="f1d00-142">делайактионс</span><span class="sxs-lookup"><span data-stu-id="f1d00-142">DelayActions</span></span>                   | [<span data-ttu-id="f1d00-143">Text</span><span class="sxs-lookup"><span data-stu-id="f1d00-143">Text</span></span>](text.md)             | <span data-ttu-id="f1d00-144">Нет</span><span class="sxs-lookup"><span data-stu-id="f1d00-144">N</span></span>   | <span data-ttu-id="f1d00-145">Да</span><span class="sxs-lookup"><span data-stu-id="f1d00-145">Y</span></span>        |
| <span data-ttu-id="f1d00-146">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="f1d00-146">Component\_</span></span>                    | [<span data-ttu-id="f1d00-147">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="f1d00-147">Identifier</span></span>](identifier.md) | <span data-ttu-id="f1d00-148">Нет</span><span class="sxs-lookup"><span data-stu-id="f1d00-148">N</span></span>   | <span data-ttu-id="f1d00-149">Нет</span><span class="sxs-lookup"><span data-stu-id="f1d00-149">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f1d00-150">Столбцы</span><span class="sxs-lookup"><span data-stu-id="f1d00-150">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f1d00-151"><span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>мсисервицеконфигфаилуреактионс</span><span class="sxs-lookup"><span data-stu-id="f1d00-151"><span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions</span></span>
</dt> <dd>

<span data-ttu-id="f1d00-152">Это первичный ключ этой таблицы, который определяет действие при сбое.</span><span class="sxs-lookup"><span data-stu-id="f1d00-152">This is the primary key of this table that identifies a failure action.</span></span>

</dd> <dt>

<span data-ttu-id="f1d00-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян</span><span class="sxs-lookup"><span data-stu-id="f1d00-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="f1d00-154">Этот столбец содержит имя службы, которая является частью этого пакета или уже установлена.</span><span class="sxs-lookup"><span data-stu-id="f1d00-154">This column contains the name of a service that is a part of this package or that is already is installed.</span></span>

</dd> <dt>

<span data-ttu-id="f1d00-155"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Журнале</span><span class="sxs-lookup"><span data-stu-id="f1d00-155"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="f1d00-156">В этом столбце указывается, когда следует изменять конфигурацию службы.</span><span class="sxs-lookup"><span data-stu-id="f1d00-156">This column specifies when to change the service's configuration.</span></span> <span data-ttu-id="f1d00-157">Следующие значения являются битовыми полями, которые можно комбинировать для представления нескольких операций.</span><span class="sxs-lookup"><span data-stu-id="f1d00-157">The following values are bit fields that can be combined to represent multiple operations.</span></span> <span data-ttu-id="f1d00-158">Любые другие значения битовых полей игнорируются.</span><span class="sxs-lookup"><span data-stu-id="f1d00-158">Any other bit field values are ignored.</span></span>



| <span data-ttu-id="f1d00-159">Константа</span><span class="sxs-lookup"><span data-stu-id="f1d00-159">Constant</span></span>                                         | <span data-ttu-id="f1d00-160">Описание</span><span class="sxs-lookup"><span data-stu-id="f1d00-160">Description</span></span>                                     |
|--------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="f1d00-161">**мсидбсервицеконфижевентинсталл** 1</span><span class="sxs-lookup"><span data-stu-id="f1d00-161">**msidbServiceConfigEventInstall** 1</span></span><br/>   | <span data-ttu-id="f1d00-162">Изменение во время установки компонента.</span><span class="sxs-lookup"><span data-stu-id="f1d00-162">Change during installation of the component.</span></span>    |
| <span data-ttu-id="f1d00-163">**мсидбсервицеконфижевентунинсталл** 2</span><span class="sxs-lookup"><span data-stu-id="f1d00-163">**msidbServiceConfigEventUninstall** 2</span></span><br/> | <span data-ttu-id="f1d00-164">Изменение во время удаления компонента.</span><span class="sxs-lookup"><span data-stu-id="f1d00-164">Change during uninstallation of the component.</span></span>  |
| <span data-ttu-id="f1d00-165">**мсидбсервицеконфижевентреинсталл** 4</span><span class="sxs-lookup"><span data-stu-id="f1d00-165">**msidbServiceConfigEventReinstall** 4</span></span><br/> | <span data-ttu-id="f1d00-166">Изменение во время повторной установки компонента.</span><span class="sxs-lookup"><span data-stu-id="f1d00-166">Change during re-installation of the component.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f1d00-167"><span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ресетпериод</span><span class="sxs-lookup"><span data-stu-id="f1d00-167"><span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod</span></span>
</dt> <dd>

<span data-ttu-id="f1d00-168">Период сброса числа сбоев службы (в секундах).</span><span class="sxs-lookup"><span data-stu-id="f1d00-168">The reset period in seconds of service's failure count.</span></span> <span data-ttu-id="f1d00-169">[Диспетчер управления службами](../services/service-control-manager.md) (SCM) подсчитывает количество сбоев каждой службы с момента последнего перезапуска системы.</span><span class="sxs-lookup"><span data-stu-id="f1d00-169">The [Service Control Manager](../services/service-control-manager.md) (SCM) counts the number of times each service has failed since the system was last restarted.</span></span> <span data-ttu-id="f1d00-170">Счетчик сбрасывается в нуль, если служба не завершается сбоем в течение периода сброса.</span><span class="sxs-lookup"><span data-stu-id="f1d00-170">The count is reset to zero if the service does not fail for the reset period.</span></span> <span data-ttu-id="f1d00-171">Когда служба завершается со сбоем в течение n часов, система выполняет действие, указанное в элементе \[ N-1 \] массива, указанного в поле действия.</span><span class="sxs-lookup"><span data-stu-id="f1d00-171">When the service fails for the Nth time, the system performs the action specified in the element \[N-1\] of the array specified in the Actions field.</span></span>

<span data-ttu-id="f1d00-172">Оставьте поле Ресетпериод пустым, чтобы указать, что счетчик сбоев никогда не должен сбрасываться.</span><span class="sxs-lookup"><span data-stu-id="f1d00-172">Leave ResetPeriod field empty to indicate that failure count should never be reset.</span></span>

</dd> <dt>

<span data-ttu-id="f1d00-173"><span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>ребутмессаже</span><span class="sxs-lookup"><span data-stu-id="f1d00-173"><span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage</span></span>
</dt> <dd>

<span data-ttu-id="f1d00-174">Сообщение, отправляемое пользователям перед перезагрузкой компьютера в ответ на действие SC, заданное в столбце действия. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="f1d00-174">The message sent to users before restarting the computer in response to a **SC\_ACTION\_REBOOT** action specified in the Actions column.</span></span> <span data-ttu-id="f1d00-175">Чтобы отправить текущее сообщение без изменений, можно использовать пустую строку "".</span><span class="sxs-lookup"><span data-stu-id="f1d00-175">You can use an empty string, "", to send the current message unchanged.</span></span> <span data-ttu-id="f1d00-176">Можно использовать \[ ~ \] синтаксис [форматированного](formatted.md) типа данных для удаления текущего сообщения и отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="f1d00-176">You can use \[~\] syntax of the [Formatted](formatted.md) data type to delete the current message and send no message.</span></span>

</dd> <dt>

<span data-ttu-id="f1d00-177"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Кнопки</span><span class="sxs-lookup"><span data-stu-id="f1d00-177"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command</span></span>
</dt> <dd>

<span data-ttu-id="f1d00-178">Командная строка, выполняемая процессом, созданной функцией [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) в ответ на действие **\_ \_ \_ команды SC Action Run** , указанное в столбце Actions.</span><span class="sxs-lookup"><span data-stu-id="f1d00-178">The command line run by the process created by the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function in response to a **SC\_ACTION\_RUN\_COMMAND** action specified in the Actions column.</span></span> <span data-ttu-id="f1d00-179">Новый процесс выполняется под той же учетной записью, что и служба, и только в том случае, если поле Action — **\_ \_ выполнить \_ команду SC Action**.</span><span class="sxs-lookup"><span data-stu-id="f1d00-179">The new process runs under the same account as the service and only if the Action field is **SC\_ACTION\_RUN\_COMMAND**.</span></span> <span data-ttu-id="f1d00-180">Чтобы использовать текущую командную строку без изменений, можно использовать пустую строку "".</span><span class="sxs-lookup"><span data-stu-id="f1d00-180">You can use an empty string, "", to use the current command line unchanged.</span></span> <span data-ttu-id="f1d00-181">Можно использовать \[ ~ \] синтаксис [форматированного](formatted.md) типа данных, чтобы удалить текущую командную строку и не выполнять никаких операций при сбое службы.</span><span class="sxs-lookup"><span data-stu-id="f1d00-181">You can use \[~\] syntax of the [Formatted](formatted.md) data type to delete the current command line and run no operation when the service fails.</span></span>

</dd> <dt>

<span data-ttu-id="f1d00-182"><span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Действия</span><span class="sxs-lookup"><span data-stu-id="f1d00-182"><span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Actions</span></span>
</dt> <dd>

<span data-ttu-id="f1d00-183">Это поле содержит массив целочисленных значений, указывающих действия, выполняемые SCM в случае сбоя службы.</span><span class="sxs-lookup"><span data-stu-id="f1d00-183">This field contains an array of integer values that specify the actions taken by the SCM if the service fails.</span></span> <span data-ttu-id="f1d00-184">Разделите значения в массиве на \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="f1d00-184">Separate the values in the array by \[~\].</span></span> <span data-ttu-id="f1d00-185">Целочисленное значение в n элементе массива указывает действие, выполняемое при сбое службы в течение n часов.</span><span class="sxs-lookup"><span data-stu-id="f1d00-185">The integer value in the Nth element of the array specifies the action performed when the service fails for the Nth time.</span></span> <span data-ttu-id="f1d00-186">Каждый член массива является одним из следующих целочисленных значений.</span><span class="sxs-lookup"><span data-stu-id="f1d00-186">Each member of the array is one of following integer values.</span></span>



| <span data-ttu-id="f1d00-187">Константа</span><span class="sxs-lookup"><span data-stu-id="f1d00-187">Constant</span></span>                                 | <span data-ttu-id="f1d00-188">Описание</span><span class="sxs-lookup"><span data-stu-id="f1d00-188">Description</span></span>           |
|------------------------------------------|-----------------------|
| <span data-ttu-id="f1d00-189">**SC \_ ДЕЙСТВИЕ \_ нет** 0</span><span class="sxs-lookup"><span data-stu-id="f1d00-189">**SC\_ACTION\_NONE** 0</span></span><br/>         | <span data-ttu-id="f1d00-190">Никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="f1d00-190">No action.</span></span>            |
| <span data-ttu-id="f1d00-191">**SC \_ ДЕЙСТВИЕ 2 при \_ перезагрузке**</span><span class="sxs-lookup"><span data-stu-id="f1d00-191">**SC\_ACTION\_REBOOT** 2</span></span><br/>       | <span data-ttu-id="f1d00-192">Перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="f1d00-192">Restart the computer.</span></span> |
| <span data-ttu-id="f1d00-193">**SC \_ ДЕЙСТВИЕ при \_ перезапуске** 1</span><span class="sxs-lookup"><span data-stu-id="f1d00-193">**SC\_ACTION\_RESTART** 1</span></span><br/>      | <span data-ttu-id="f1d00-194">Перезапустите службу.</span><span class="sxs-lookup"><span data-stu-id="f1d00-194">Restart the service.</span></span>  |
| <span data-ttu-id="f1d00-195">**SC \_ ДЕЙСТВИЕ \_ выполнения, \_ команда** 3</span><span class="sxs-lookup"><span data-stu-id="f1d00-195">**SC\_ACTION\_RUN\_COMMAND** 3</span></span><br/> | <span data-ttu-id="f1d00-196">Выполните команду.</span><span class="sxs-lookup"><span data-stu-id="f1d00-196">Run a command.</span></span>        |



 

</dd> <dt>

<span data-ttu-id="f1d00-197"><span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>делайактионс</span><span class="sxs-lookup"><span data-stu-id="f1d00-197"><span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions</span></span>
</dt> <dd>

<span data-ttu-id="f1d00-198">Это поле содержит массив целочисленных значений, которые указывают время ожидания в миллисекундах перед выполнением действия, указанного в столбце Action.</span><span class="sxs-lookup"><span data-stu-id="f1d00-198">This field contains an array of integer values that specify the time in milliseconds to wait before performing the action specified in the Action column.</span></span> <span data-ttu-id="f1d00-199">Разделите значения в массиве на \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="f1d00-199">Separate the values in the array by \[~\].</span></span> <span data-ttu-id="f1d00-200">Число элементов в массиве Делайактионс должно быть равно числу элементов в массиве actions.</span><span class="sxs-lookup"><span data-stu-id="f1d00-200">The number of elements in the DelayActions array must be equal to the number of elements in the Actions array.</span></span> <span data-ttu-id="f1d00-201">Элемент n массива Делайактионс задает временную задержку для элемента n массива Actions.</span><span class="sxs-lookup"><span data-stu-id="f1d00-201">The Nth element of the DelayActions array specifies the time delay for the nth element of the Actions array.</span></span>

</dd> <dt>

<span data-ttu-id="f1d00-202"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="f1d00-202"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="f1d00-203">Внешний ключ к столбцу одной из [таблиц Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f1d00-203">External key to column one of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="f1d00-204">Проверка</span><span class="sxs-lookup"><span data-stu-id="f1d00-204">Validation</span></span>

<dl>

[<span data-ttu-id="f1d00-205">ICE102</span><span class="sxs-lookup"><span data-stu-id="f1d00-205">ICE102</span></span>](ice-102.md)  
[<span data-ttu-id="f1d00-206">ICE03</span><span class="sxs-lookup"><span data-stu-id="f1d00-206">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f1d00-207">ICE06</span><span class="sxs-lookup"><span data-stu-id="f1d00-207">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f1d00-208">ICE32</span><span class="sxs-lookup"><span data-stu-id="f1d00-208">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="f1d00-209">ICE45</span><span class="sxs-lookup"><span data-stu-id="f1d00-209">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="f1d00-210">ICE46</span><span class="sxs-lookup"><span data-stu-id="f1d00-210">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="f1d00-211">ICE69</span><span class="sxs-lookup"><span data-stu-id="f1d00-211">ICE69</span></span>](ice69.md)  
</dl>

 

 
