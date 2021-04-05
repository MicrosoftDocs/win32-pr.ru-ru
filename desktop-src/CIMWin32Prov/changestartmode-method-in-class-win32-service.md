---
description: Изменяет режим запуска \_ службы Win32.
ms.assetid: 4fd6a1eb-d2e0-4172-843d-24ae89c5bfcf
ms.tgt_platform: multiple
title: Метод Чанжестартмоде класса Win32_Service (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06a4692996354614a685471f98b0243fc1091433
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072433"
---
# <a name="changestartmode-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="cf9ab-103">Метод Чанжестартмоде класса Win32_Service (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="cf9ab-103">ChangeStartMode method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="cf9ab-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) чанжестартмоде изменяет режим запуска [**\_ службы Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="cf9ab-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_Service**](win32-service.md).</span></span>

<span data-ttu-id="cf9ab-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="cf9ab-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cf9ab-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cf9ab-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cf9ab-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf9ab-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="cf9ab-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf9ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf9ab-109">*StartMode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf9ab-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-110">Режим запуска базовой службы Windows.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-110">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="cf9ab-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Запуск загрузки** ("Boot")</span><span class="sxs-lookup"><span data-stu-id="cf9ab-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="cf9ab-112">Драйвер устройства запущен загрузчиком операционной системы.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-112">Device driver started by the operating system loader.</span></span> <span data-ttu-id="cf9ab-113">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-113">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="cf9ab-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Система** ("System")</span><span class="sxs-lookup"><span data-stu-id="cf9ab-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="cf9ab-115">Драйвер устройства запущен процессом инициализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-115">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="cf9ab-116">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="cf9ab-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Автоматический запуск** (автоматический)</span><span class="sxs-lookup"><span data-stu-id="cf9ab-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="cf9ab-118">Служба запускается автоматически диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-118">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="cf9ab-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Запуск по требованию** (вручную)</span><span class="sxs-lookup"><span data-stu-id="cf9ab-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="cf9ab-120">Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="cf9ab-120">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cf9ab-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** ("отключено")</span><span class="sxs-lookup"><span data-stu-id="cf9ab-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="cf9ab-122">Служба, которая больше не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-122">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf9ab-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf9ab-123">Return value</span></span>

<span data-ttu-id="cf9ab-124">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-124">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="cf9ab-125">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="cf9ab-125">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="cf9ab-126">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="cf9ab-126">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="cf9ab-127">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-127">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-128">0</span><span class="sxs-lookup"><span data-stu-id="cf9ab-128">0</span></span>

<span data-ttu-id="cf9ab-129">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-129">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-130">**Не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-130">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-131">1</span><span class="sxs-lookup"><span data-stu-id="cf9ab-131">1</span></span>

<span data-ttu-id="cf9ab-132">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-132">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-133">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-133">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-134">2</span><span class="sxs-lookup"><span data-stu-id="cf9ab-134">2</span></span>

<span data-ttu-id="cf9ab-135">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-135">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-136">**Работающие зависимые службы**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-136">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-137">3</span><span class="sxs-lookup"><span data-stu-id="cf9ab-137">3</span></span>

<span data-ttu-id="cf9ab-138">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-138">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-139">**Недопустимый элемент управления службой**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-139">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-140">4</span><span class="sxs-lookup"><span data-stu-id="cf9ab-140">4</span></span>

<span data-ttu-id="cf9ab-141">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-141">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-142">**Служба не может принять контроль**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-142">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-143">5</span><span class="sxs-lookup"><span data-stu-id="cf9ab-143">5</span></span>

<span data-ttu-id="cf9ab-144">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-144">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-145">**Служба неактивна**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-145">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-146">6</span><span class="sxs-lookup"><span data-stu-id="cf9ab-146">6</span></span>

<span data-ttu-id="cf9ab-147">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-147">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-148">**Время ожидания запроса на обслуживание**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-148">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-149">7</span><span class="sxs-lookup"><span data-stu-id="cf9ab-149">7</span></span>

<span data-ttu-id="cf9ab-150">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-150">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-151">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-151">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-152">8</span><span class="sxs-lookup"><span data-stu-id="cf9ab-152">8</span></span>

<span data-ttu-id="cf9ab-153">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-153">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-154">**Путь не найден**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-154">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-155">9</span><span class="sxs-lookup"><span data-stu-id="cf9ab-155">9</span></span>

<span data-ttu-id="cf9ab-156">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-156">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-157">**Служба уже запущена**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-157">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-158">10</span><span class="sxs-lookup"><span data-stu-id="cf9ab-158">10</span></span>

<span data-ttu-id="cf9ab-159">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-159">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-160">**База данных службы заблокирована**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-160">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-161">11</span><span class="sxs-lookup"><span data-stu-id="cf9ab-161">11</span></span>

<span data-ttu-id="cf9ab-162">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-162">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-163">**Зависимость службы удалена**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-163">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-164">12</span><span class="sxs-lookup"><span data-stu-id="cf9ab-164">12</span></span>

<span data-ttu-id="cf9ab-165">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-165">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-166">**Сбой зависимости службы**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-166">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-167">13</span><span class="sxs-lookup"><span data-stu-id="cf9ab-167">13</span></span>

<span data-ttu-id="cf9ab-168">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-168">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-169">**Служба отключена**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-169">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-170">14</span><span class="sxs-lookup"><span data-stu-id="cf9ab-170">14</span></span>

<span data-ttu-id="cf9ab-171">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-171">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-172">**Сбой при входе в службу**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-172">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-173">15</span><span class="sxs-lookup"><span data-stu-id="cf9ab-173">15</span></span>

<span data-ttu-id="cf9ab-174">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-174">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-175">**Служба помечена для удаления**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-175">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-176">16</span><span class="sxs-lookup"><span data-stu-id="cf9ab-176">16</span></span>

<span data-ttu-id="cf9ab-177">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-177">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-178">**Служба без потока**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-178">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-179">17</span><span class="sxs-lookup"><span data-stu-id="cf9ab-179">17</span></span>

<span data-ttu-id="cf9ab-180">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-180">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-181">**Состояние "циклическая зависимость"**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-181">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-182">18</span><span class="sxs-lookup"><span data-stu-id="cf9ab-182">18</span></span>

<span data-ttu-id="cf9ab-183">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-183">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-184">**Состояние "повторяющееся имя"**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-184">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-185">19</span><span class="sxs-lookup"><span data-stu-id="cf9ab-185">19</span></span>

<span data-ttu-id="cf9ab-186">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-186">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-187">**Состояние "Недопустимое имя"**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-187">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-188">20</span><span class="sxs-lookup"><span data-stu-id="cf9ab-188">20</span></span>

<span data-ttu-id="cf9ab-189">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-189">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-190">**Недопустимый параметр Status**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-190">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-191">21</span><span class="sxs-lookup"><span data-stu-id="cf9ab-191">21</span></span>

<span data-ttu-id="cf9ab-192">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-192">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-193">**Недопустимое состояние учетной записи службы**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-193">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-194">22</span><span class="sxs-lookup"><span data-stu-id="cf9ab-194">22</span></span>

<span data-ttu-id="cf9ab-195">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-195">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-196">**Служба состояний существует**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-196">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-197">23</span><span class="sxs-lookup"><span data-stu-id="cf9ab-197">23</span></span>

<span data-ttu-id="cf9ab-198">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-198">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-199">**Служба уже приостановлена**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-199">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-200">24</span><span class="sxs-lookup"><span data-stu-id="cf9ab-200">24</span></span>

<span data-ttu-id="cf9ab-201">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-201">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="cf9ab-202">**Другое**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-202">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="cf9ab-203">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="cf9ab-203">25 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="cf9ab-204">Примеры</span><span class="sxs-lookup"><span data-stu-id="cf9ab-204">Examples</span></span>

<span data-ttu-id="cf9ab-205">Следующее [изменение StartMode примера службы](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell, извлеченного из коллекции TechNet, изменяет режим запуска службы.</span><span class="sxs-lookup"><span data-stu-id="cf9ab-205">The following [Change StartMode of a Service](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell sample, pulled from TechNet Gallery, changes the start mode of a service.</span></span>


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
```



## <a name="requirements"></a><span data-ttu-id="cf9ab-206">Требования</span><span class="sxs-lookup"><span data-stu-id="cf9ab-206">Requirements</span></span>



| <span data-ttu-id="cf9ab-207">Требование</span><span class="sxs-lookup"><span data-stu-id="cf9ab-207">Requirement</span></span> | <span data-ttu-id="cf9ab-208">Значение</span><span class="sxs-lookup"><span data-stu-id="cf9ab-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf9ab-209">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf9ab-209">Minimum supported client</span></span><br/> | <span data-ttu-id="cf9ab-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf9ab-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cf9ab-211">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf9ab-211">Minimum supported server</span></span><br/> | <span data-ttu-id="cf9ab-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf9ab-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cf9ab-213">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cf9ab-213">Namespace</span></span><br/>                | <span data-ttu-id="cf9ab-214">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cf9ab-214">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cf9ab-215">MOF</span><span class="sxs-lookup"><span data-stu-id="cf9ab-215">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf9ab-216"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf9ab-216"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf9ab-217">DLL</span><span class="sxs-lookup"><span data-stu-id="cf9ab-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf9ab-218"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf9ab-218"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf9ab-219">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf9ab-219">See also</span></span>

<dl> <dt>

<span data-ttu-id="cf9ab-220">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cf9ab-220">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cf9ab-221">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="cf9ab-221">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="cf9ab-222">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="cf9ab-222">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

