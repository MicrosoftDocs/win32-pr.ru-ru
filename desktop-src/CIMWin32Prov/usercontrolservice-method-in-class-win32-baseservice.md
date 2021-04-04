---
description: Пытается отправить в службу определенный пользователем управляющий код.
ms.assetid: d181dbf8-e1ad-47b2-9e64-4aabc77e64bd
ms.tgt_platform: multiple
title: Метод Усерконтролсервице класса Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55647524c8ba561716441976fe6654b933e1900b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896366"
---
# <a name="usercontrolservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="6e36f-103">Метод Усерконтролсервице \_ класса Win32 басесервице</span><span class="sxs-lookup"><span data-stu-id="6e36f-103">UserControlService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="6e36f-104">Метод [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) пытается отправить в службу определенный пользователем код элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6e36f-104">The [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to a service.</span></span>

<span data-ttu-id="6e36f-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="6e36f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6e36f-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6e36f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6e36f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e36f-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="6e36f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e36f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e36f-109">*Контролкоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e36f-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-110">Значение, указывающее команду элемента управления для службы.</span><span class="sxs-lookup"><span data-stu-id="6e36f-110">Value that specifies a control command to a service.</span></span> <span data-ttu-id="6e36f-111">Например, команда управления является командой "Pause" или "Continue".</span><span class="sxs-lookup"><span data-stu-id="6e36f-111">For example a control command is a "pause" or "continue" command.</span></span> <span data-ttu-id="6e36f-112">Значением может быть предопределенный код, а также значение и действие, определяемое службой.</span><span class="sxs-lookup"><span data-stu-id="6e36f-112">The value can be a predefined code, or a value and action that the service defines.</span></span> <span data-ttu-id="6e36f-113">Ниже перечислены стандартные управляющие коды.</span><span class="sxs-lookup"><span data-stu-id="6e36f-113">The following are the predefined control codes:</span></span>

<dt>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>

<span data-ttu-id="6e36f-114"><span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**\_продолжение управления \_ службой**</span><span class="sxs-lookup"><span data-stu-id="6e36f-114"><span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**SERVICE\_CONTROL\_CONTINUE**</span></span>


</dt> <dd>

<span data-ttu-id="6e36f-115">Уведомляет приостановленную службу о возобновлении.</span><span class="sxs-lookup"><span data-stu-id="6e36f-115">Notifies a paused service to resume.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>

<span data-ttu-id="6e36f-116"><span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**\_контроль службы \_ опроса**</span><span class="sxs-lookup"><span data-stu-id="6e36f-116"><span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**SERVICE\_CONTROL\_INTERROGATE**</span></span>


</dt> <dd>

<span data-ttu-id="6e36f-117">Уведомляет службу о текущих сведениях о состоянии диспетчеру управления службами.</span><span class="sxs-lookup"><span data-stu-id="6e36f-117">Notifies a service to report the current status information to the service control manager.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>

<span data-ttu-id="6e36f-118"><span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**\_нетбиндадд управления \_ службами**</span><span class="sxs-lookup"><span data-stu-id="6e36f-118"><span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**SERVICE\_CONTROL\_NETBINDADD**</span></span>


</dt> <dd>

<span data-ttu-id="6e36f-119">Уведомляет сетевую службу о том, что для привязки существует новый компонент.</span><span class="sxs-lookup"><span data-stu-id="6e36f-119">Notifies a network service that there is a new component for binding.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>

<span data-ttu-id="6e36f-120"><span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**\_нетбинддисабле управления \_ службами**</span><span class="sxs-lookup"><span data-stu-id="6e36f-120"><span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**SERVICE\_CONTROL\_NETBINDDISABLE**</span></span>


</dt> <dd>

<span data-ttu-id="6e36f-121">Уведомляет сетевую службу, что одна из ее привязок отключена.</span><span class="sxs-lookup"><span data-stu-id="6e36f-121">Notifies a network service that one of its bindings is disabled.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>

<span data-ttu-id="6e36f-122"><span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**\_нетбинденабле управления \_ службами**</span><span class="sxs-lookup"><span data-stu-id="6e36f-122"><span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**SERVICE\_CONTROL\_NETBINDENABLE**</span></span>


</dt> <dd>

<span data-ttu-id="6e36f-123">Уведомляет сетевую службу, что включена отключенная привязка.</span><span class="sxs-lookup"><span data-stu-id="6e36f-123">Notifies a network service that a disabled binding is enabled.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>

<span data-ttu-id="6e36f-124"><span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**\_нетбиндремове управления \_ службами**</span><span class="sxs-lookup"><span data-stu-id="6e36f-124"><span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**SERVICE\_CONTROL\_NETBINDREMOVE**</span></span>


</dt> <dd>

<span data-ttu-id="6e36f-125">Уведомляет сетевую службу о том, что компонент для привязки был удален.</span><span class="sxs-lookup"><span data-stu-id="6e36f-125">Notifies a network service that a component for binding has been removed.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>

<span data-ttu-id="6e36f-126"><span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**\_парамчанже управления \_ службами**</span><span class="sxs-lookup"><span data-stu-id="6e36f-126"><span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**SERVICE\_CONTROL\_PARAMCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="6e36f-127">Уведомляет службу о том, что параметры запуска были изменены.</span><span class="sxs-lookup"><span data-stu-id="6e36f-127">Notifies a service that its startup parameters are changed.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>

<span data-ttu-id="6e36f-128"><span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**\_приостановка управления службой \_**</span><span class="sxs-lookup"><span data-stu-id="6e36f-128"><span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**SERVICE\_CONTROL\_PAUSE**</span></span>


</dt> <dd>

<span data-ttu-id="6e36f-129">Сообщает службе о необходимости приостановки.</span><span class="sxs-lookup"><span data-stu-id="6e36f-129">Notifies a service to pause.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>

<span data-ttu-id="6e36f-130"><span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**\_Завершение управления \_ службой**</span><span class="sxs-lookup"><span data-stu-id="6e36f-130"><span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**SERVICE\_CONTROL\_STOP**</span></span>


</dt> <dd>

<span data-ttu-id="6e36f-131">Уведомляет службу о необходимости ее завершения.</span><span class="sxs-lookup"><span data-stu-id="6e36f-131">Notifies a service to stop.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e36f-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e36f-132">Return value</span></span>

<span data-ttu-id="6e36f-133">Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="6e36f-133">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="6e36f-134">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="6e36f-134">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-135">0</span><span class="sxs-lookup"><span data-stu-id="6e36f-135">0</span></span>

<span data-ttu-id="6e36f-136">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="6e36f-136">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-137">**Не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="6e36f-137">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-138">1</span><span class="sxs-lookup"><span data-stu-id="6e36f-138">1</span></span>

<span data-ttu-id="6e36f-139">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6e36f-139">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-140">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="6e36f-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-141">2</span><span class="sxs-lookup"><span data-stu-id="6e36f-141">2</span></span>

<span data-ttu-id="6e36f-142">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="6e36f-142">The user does not have the necessary access rights.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-143">**Работающие зависимые службы**</span><span class="sxs-lookup"><span data-stu-id="6e36f-143">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-144">3</span><span class="sxs-lookup"><span data-stu-id="6e36f-144">3</span></span>

<span data-ttu-id="6e36f-145">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="6e36f-145">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-146">**Недопустимый элемент управления службой**</span><span class="sxs-lookup"><span data-stu-id="6e36f-146">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-147">4</span><span class="sxs-lookup"><span data-stu-id="6e36f-147">4</span></span>

<span data-ttu-id="6e36f-148">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="6e36f-148">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-149">**Служба не может принять контроль**</span><span class="sxs-lookup"><span data-stu-id="6e36f-149">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-150">5</span><span class="sxs-lookup"><span data-stu-id="6e36f-150">5</span></span>

<span data-ttu-id="6e36f-151">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="6e36f-151">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-152">**Служба неактивна**</span><span class="sxs-lookup"><span data-stu-id="6e36f-152">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-153">6</span><span class="sxs-lookup"><span data-stu-id="6e36f-153">6</span></span>

<span data-ttu-id="6e36f-154">Служба не запустилась.</span><span class="sxs-lookup"><span data-stu-id="6e36f-154">The service has not started.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-155">**Время ожидания запроса на обслуживание**</span><span class="sxs-lookup"><span data-stu-id="6e36f-155">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-156">7</span><span class="sxs-lookup"><span data-stu-id="6e36f-156">7</span></span>

<span data-ttu-id="6e36f-157">Служба не реагирует на запрос на запуск быстро.</span><span class="sxs-lookup"><span data-stu-id="6e36f-157">The service does not respond to the start request quickly.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-158">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="6e36f-158">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-159">8</span><span class="sxs-lookup"><span data-stu-id="6e36f-159">8</span></span>

<span data-ttu-id="6e36f-160">Интерактивный процесс.</span><span class="sxs-lookup"><span data-stu-id="6e36f-160">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-161">**Путь не найден**</span><span class="sxs-lookup"><span data-stu-id="6e36f-161">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-162">9</span><span class="sxs-lookup"><span data-stu-id="6e36f-162">9</span></span>

<span data-ttu-id="6e36f-163">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="6e36f-163">The directory path to the service executable file is not found.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-164">**Служба уже запущена**</span><span class="sxs-lookup"><span data-stu-id="6e36f-164">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-165">10</span><span class="sxs-lookup"><span data-stu-id="6e36f-165">10</span></span>

<span data-ttu-id="6e36f-166">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="6e36f-166">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-167">**База данных службы заблокирована**</span><span class="sxs-lookup"><span data-stu-id="6e36f-167">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-168">11</span><span class="sxs-lookup"><span data-stu-id="6e36f-168">11</span></span>

<span data-ttu-id="6e36f-169">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="6e36f-169">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-170">**Зависимость службы удалена**</span><span class="sxs-lookup"><span data-stu-id="6e36f-170">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-171">12</span><span class="sxs-lookup"><span data-stu-id="6e36f-171">12</span></span>

<span data-ttu-id="6e36f-172">Зависимость, от которой зависит эта служба, удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="6e36f-172">A dependency that this service relies on is removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-173">**Сбой зависимости службы**</span><span class="sxs-lookup"><span data-stu-id="6e36f-173">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-174">13</span><span class="sxs-lookup"><span data-stu-id="6e36f-174">13</span></span>

<span data-ttu-id="6e36f-175">Служба не находит службу, необходимую зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="6e36f-175">The service does not find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-176">**Служба отключена**</span><span class="sxs-lookup"><span data-stu-id="6e36f-176">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-177">14</span><span class="sxs-lookup"><span data-stu-id="6e36f-177">14</span></span>

<span data-ttu-id="6e36f-178">Служба отключена от системы.</span><span class="sxs-lookup"><span data-stu-id="6e36f-178">The service is disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-179">**Сбой при входе в службу**</span><span class="sxs-lookup"><span data-stu-id="6e36f-179">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-180">15</span><span class="sxs-lookup"><span data-stu-id="6e36f-180">15</span></span>

<span data-ttu-id="6e36f-181">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="6e36f-181">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-182">**Служба помечена для удаления**</span><span class="sxs-lookup"><span data-stu-id="6e36f-182">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-183">16</span><span class="sxs-lookup"><span data-stu-id="6e36f-183">16</span></span>

<span data-ttu-id="6e36f-184">Служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="6e36f-184">The service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-185">**Служба без потока**</span><span class="sxs-lookup"><span data-stu-id="6e36f-185">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-186">17</span><span class="sxs-lookup"><span data-stu-id="6e36f-186">17</span></span>

<span data-ttu-id="6e36f-187">Отсутствует поток исполнения для этой службы.</span><span class="sxs-lookup"><span data-stu-id="6e36f-187">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-188">**Состояние "циклическая зависимость"**</span><span class="sxs-lookup"><span data-stu-id="6e36f-188">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-189">18</span><span class="sxs-lookup"><span data-stu-id="6e36f-189">18</span></span>

<span data-ttu-id="6e36f-190">При запуске службы обнаружены циклические зависимости.</span><span class="sxs-lookup"><span data-stu-id="6e36f-190">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-191">**Состояние "повторяющееся имя"**</span><span class="sxs-lookup"><span data-stu-id="6e36f-191">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-192">19</span><span class="sxs-lookup"><span data-stu-id="6e36f-192">19</span></span>

<span data-ttu-id="6e36f-193">Служба с таким именем уже запущена.</span><span class="sxs-lookup"><span data-stu-id="6e36f-193">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-194">**Состояние "Недопустимое имя"**</span><span class="sxs-lookup"><span data-stu-id="6e36f-194">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-195">20</span><span class="sxs-lookup"><span data-stu-id="6e36f-195">20</span></span>

<span data-ttu-id="6e36f-196">В имени службы присутствуют недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="6e36f-196">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-197">**Недопустимый параметр Status**</span><span class="sxs-lookup"><span data-stu-id="6e36f-197">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-198">21</span><span class="sxs-lookup"><span data-stu-id="6e36f-198">21</span></span>

<span data-ttu-id="6e36f-199">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="6e36f-199">Invalid parameters have passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-200">**Недопустимое состояние учетной записи службы**</span><span class="sxs-lookup"><span data-stu-id="6e36f-200">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-201">22</span><span class="sxs-lookup"><span data-stu-id="6e36f-201">22</span></span>

<span data-ttu-id="6e36f-202">Учетная запись, под которой выполняется эта служба, недопустима или не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="6e36f-202">The account that this service runs under is not valid or does not have the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-203">**Служба состояний существует**</span><span class="sxs-lookup"><span data-stu-id="6e36f-203">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-204">23</span><span class="sxs-lookup"><span data-stu-id="6e36f-204">23</span></span>

<span data-ttu-id="6e36f-205">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="6e36f-205">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-206">**Служба уже приостановлена**</span><span class="sxs-lookup"><span data-stu-id="6e36f-206">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-207">24</span><span class="sxs-lookup"><span data-stu-id="6e36f-207">24</span></span>

<span data-ttu-id="6e36f-208">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="6e36f-208">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="6e36f-209">**Другое**</span><span class="sxs-lookup"><span data-stu-id="6e36f-209">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="6e36f-210">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="6e36f-210">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e36f-211">Требования</span><span class="sxs-lookup"><span data-stu-id="6e36f-211">Requirements</span></span>



| <span data-ttu-id="6e36f-212">Требование</span><span class="sxs-lookup"><span data-stu-id="6e36f-212">Requirement</span></span> | <span data-ttu-id="6e36f-213">Значение</span><span class="sxs-lookup"><span data-stu-id="6e36f-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e36f-214">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e36f-214">Minimum supported client</span></span><br/> | <span data-ttu-id="6e36f-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e36f-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6e36f-216">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e36f-216">Minimum supported server</span></span><br/> | <span data-ttu-id="6e36f-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e36f-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6e36f-218">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6e36f-218">Namespace</span></span><br/>                | <span data-ttu-id="6e36f-219">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6e36f-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6e36f-220">MOF</span><span class="sxs-lookup"><span data-stu-id="6e36f-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e36f-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e36f-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e36f-222">DLL</span><span class="sxs-lookup"><span data-stu-id="6e36f-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e36f-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e36f-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e36f-224">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e36f-224">See also</span></span>

<dl> <dt>

<span data-ttu-id="6e36f-225">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e36f-225">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6e36f-226">**\_Басесервице Win32**</span><span class="sxs-lookup"><span data-stu-id="6e36f-226">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

