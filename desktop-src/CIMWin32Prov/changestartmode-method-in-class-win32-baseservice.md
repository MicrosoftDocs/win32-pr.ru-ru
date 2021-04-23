---
description: Изменяет режим запуска объекта службы, производного от Win32 \_ басесервице.
ms.assetid: 33040632-6c04-4084-af09-8e1b8bc29090
ms.tgt_platform: multiple
title: Метод Чанжестартмоде класса Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9877300a2135b7082677193696cd2d11811ab3dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141443"
---
# <a name="changestartmode-method-of-the-win32_baseservice-class"></a><span data-ttu-id="e90e7-103">Метод Чанжестартмоде \_ класса Win32 басесервице</span><span class="sxs-lookup"><span data-stu-id="e90e7-103">ChangeStartMode method of the Win32\_BaseService class</span></span>

<span data-ttu-id="e90e7-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) чанжестартмоде изменяет режим запуска объекта службы, производного от [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="e90e7-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a service object derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="e90e7-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="e90e7-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e90e7-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e90e7-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e90e7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e90e7-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="e90e7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e90e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e90e7-109">*StartMode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e90e7-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-110">Режим запуска базовой службы Windows.</span><span class="sxs-lookup"><span data-stu-id="e90e7-110">Start mode of the Windows base service.</span></span> <span data-ttu-id="e90e7-111">Значение по умолчанию — "Automatic".</span><span class="sxs-lookup"><span data-stu-id="e90e7-111">The default is "Automatic".</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="e90e7-112"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Запуск загрузки** ("Boot")</span><span class="sxs-lookup"><span data-stu-id="e90e7-112"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="e90e7-113">Драйвер устройства запущен загрузчиком операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e90e7-113">Device driver started by the operating system loader.</span></span> <span data-ttu-id="e90e7-114">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="e90e7-114">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="e90e7-115"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Системный запуск** ("System")</span><span class="sxs-lookup"><span data-stu-id="e90e7-115"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="e90e7-116">Драйвер устройства запущен процессом инициализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e90e7-116">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="e90e7-117">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="e90e7-117">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="e90e7-118"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Автоматический запуск** (автоматический)</span><span class="sxs-lookup"><span data-stu-id="e90e7-118"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="e90e7-119">Служба запускается автоматически диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="e90e7-119">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="e90e7-120"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Запуск по требованию** (вручную)</span><span class="sxs-lookup"><span data-stu-id="e90e7-120"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="e90e7-121">Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-baseservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e90e7-121">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e90e7-122"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** ("отключено")</span><span class="sxs-lookup"><span data-stu-id="e90e7-122"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="e90e7-123">Служба отключена.</span><span class="sxs-lookup"><span data-stu-id="e90e7-123">Service is disabled.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e90e7-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e90e7-124">Return value</span></span>

<span data-ttu-id="e90e7-125">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="e90e7-125">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="e90e7-126">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="e90e7-126">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-127">0</span><span class="sxs-lookup"><span data-stu-id="e90e7-127">0</span></span>

<span data-ttu-id="e90e7-128">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="e90e7-128">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-129">**Не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="e90e7-129">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-130">1</span><span class="sxs-lookup"><span data-stu-id="e90e7-130">1</span></span>

<span data-ttu-id="e90e7-131">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e90e7-131">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-132">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="e90e7-132">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-133">2</span><span class="sxs-lookup"><span data-stu-id="e90e7-133">2</span></span>

<span data-ttu-id="e90e7-134">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="e90e7-134">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-135">**Работающие зависимые службы**</span><span class="sxs-lookup"><span data-stu-id="e90e7-135">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-136">3</span><span class="sxs-lookup"><span data-stu-id="e90e7-136">3</span></span>

<span data-ttu-id="e90e7-137">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="e90e7-137">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-138">**Недопустимый элемент управления службой**</span><span class="sxs-lookup"><span data-stu-id="e90e7-138">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-139">4</span><span class="sxs-lookup"><span data-stu-id="e90e7-139">4</span></span>

<span data-ttu-id="e90e7-140">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="e90e7-140">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-141">**Служба не может принять контроль**</span><span class="sxs-lookup"><span data-stu-id="e90e7-141">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-142">5</span><span class="sxs-lookup"><span data-stu-id="e90e7-142">5</span></span>

<span data-ttu-id="e90e7-143">Запрошенный управляющий код не может быть отправлен в службу, так как состояние службы (свойство [**состояния**](win32-baseservice.md) [**Win32 \_ басесервице**](win32-baseservice.md)) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="e90e7-143">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-144">**Служба неактивна**</span><span class="sxs-lookup"><span data-stu-id="e90e7-144">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-145">6</span><span class="sxs-lookup"><span data-stu-id="e90e7-145">6</span></span>

<span data-ttu-id="e90e7-146">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="e90e7-146">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-147">**Время ожидания запроса на обслуживание**</span><span class="sxs-lookup"><span data-stu-id="e90e7-147">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-148">7</span><span class="sxs-lookup"><span data-stu-id="e90e7-148">7</span></span>

<span data-ttu-id="e90e7-149">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="e90e7-149">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-150">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="e90e7-150">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-151">8</span><span class="sxs-lookup"><span data-stu-id="e90e7-151">8</span></span>

<span data-ttu-id="e90e7-152">Интерактивный процесс.</span><span class="sxs-lookup"><span data-stu-id="e90e7-152">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-153">**Путь не найден**</span><span class="sxs-lookup"><span data-stu-id="e90e7-153">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-154">9</span><span class="sxs-lookup"><span data-stu-id="e90e7-154">9</span></span>

<span data-ttu-id="e90e7-155">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="e90e7-155">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-156">**Служба уже запущена**</span><span class="sxs-lookup"><span data-stu-id="e90e7-156">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-157">10</span><span class="sxs-lookup"><span data-stu-id="e90e7-157">10</span></span>

<span data-ttu-id="e90e7-158">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="e90e7-158">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-159">**База данных службы заблокирована**</span><span class="sxs-lookup"><span data-stu-id="e90e7-159">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-160">11</span><span class="sxs-lookup"><span data-stu-id="e90e7-160">11</span></span>

<span data-ttu-id="e90e7-161">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="e90e7-161">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-162">**Зависимость службы удалена**</span><span class="sxs-lookup"><span data-stu-id="e90e7-162">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-163">12</span><span class="sxs-lookup"><span data-stu-id="e90e7-163">12</span></span>

<span data-ttu-id="e90e7-164">Служба, от которой зависит эта служба, была удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="e90e7-164">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-165">**Сбой зависимости службы**</span><span class="sxs-lookup"><span data-stu-id="e90e7-165">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-166">13</span><span class="sxs-lookup"><span data-stu-id="e90e7-166">13</span></span>

<span data-ttu-id="e90e7-167">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="e90e7-167">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-168">**Служба отключена**</span><span class="sxs-lookup"><span data-stu-id="e90e7-168">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-169">14</span><span class="sxs-lookup"><span data-stu-id="e90e7-169">14</span></span>

<span data-ttu-id="e90e7-170">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="e90e7-170">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-171">**Сбой при входе в службу**</span><span class="sxs-lookup"><span data-stu-id="e90e7-171">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-172">15</span><span class="sxs-lookup"><span data-stu-id="e90e7-172">15</span></span>

<span data-ttu-id="e90e7-173">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="e90e7-173">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-174">**Служба помечена для удаления**</span><span class="sxs-lookup"><span data-stu-id="e90e7-174">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-175">16</span><span class="sxs-lookup"><span data-stu-id="e90e7-175">16</span></span>

<span data-ttu-id="e90e7-176">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="e90e7-176">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-177">**Служба без потока**</span><span class="sxs-lookup"><span data-stu-id="e90e7-177">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-178">17</span><span class="sxs-lookup"><span data-stu-id="e90e7-178">17</span></span>

<span data-ttu-id="e90e7-179">Отсутствует поток исполнения для этой службы.</span><span class="sxs-lookup"><span data-stu-id="e90e7-179">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-180">**Состояние "циклическая зависимость"**</span><span class="sxs-lookup"><span data-stu-id="e90e7-180">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-181">18</span><span class="sxs-lookup"><span data-stu-id="e90e7-181">18</span></span>

<span data-ttu-id="e90e7-182">При запуске службы обнаружены циклические зависимости.</span><span class="sxs-lookup"><span data-stu-id="e90e7-182">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-183">**Состояние "повторяющееся имя"**</span><span class="sxs-lookup"><span data-stu-id="e90e7-183">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-184">19</span><span class="sxs-lookup"><span data-stu-id="e90e7-184">19</span></span>

<span data-ttu-id="e90e7-185">Служба с таким именем уже запущена.</span><span class="sxs-lookup"><span data-stu-id="e90e7-185">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-186">**Состояние "Недопустимое имя"**</span><span class="sxs-lookup"><span data-stu-id="e90e7-186">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-187">20</span><span class="sxs-lookup"><span data-stu-id="e90e7-187">20</span></span>

<span data-ttu-id="e90e7-188">В имени службы присутствуют недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="e90e7-188">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-189">**Недопустимый параметр Status**</span><span class="sxs-lookup"><span data-stu-id="e90e7-189">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-190">21</span><span class="sxs-lookup"><span data-stu-id="e90e7-190">21</span></span>

<span data-ttu-id="e90e7-191">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="e90e7-191">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-192">**Недопустимое состояние учетной записи службы**</span><span class="sxs-lookup"><span data-stu-id="e90e7-192">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-193">22</span><span class="sxs-lookup"><span data-stu-id="e90e7-193">22</span></span>

<span data-ttu-id="e90e7-194">Учетная запись, под которой будет запускаться эта служба, недопустима или не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="e90e7-194">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-195">**Служба состояний существует**</span><span class="sxs-lookup"><span data-stu-id="e90e7-195">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-196">23</span><span class="sxs-lookup"><span data-stu-id="e90e7-196">23</span></span>

<span data-ttu-id="e90e7-197">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="e90e7-197">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-198">**Служба уже приостановлена**</span><span class="sxs-lookup"><span data-stu-id="e90e7-198">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-199">24</span><span class="sxs-lookup"><span data-stu-id="e90e7-199">24</span></span>

<span data-ttu-id="e90e7-200">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="e90e7-200">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="e90e7-201">**Другое**</span><span class="sxs-lookup"><span data-stu-id="e90e7-201">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="e90e7-202">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="e90e7-202">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e90e7-203">Требования</span><span class="sxs-lookup"><span data-stu-id="e90e7-203">Requirements</span></span>



| <span data-ttu-id="e90e7-204">Требование</span><span class="sxs-lookup"><span data-stu-id="e90e7-204">Requirement</span></span> | <span data-ttu-id="e90e7-205">Значение</span><span class="sxs-lookup"><span data-stu-id="e90e7-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e90e7-206">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e90e7-206">Minimum supported client</span></span><br/> | <span data-ttu-id="e90e7-207">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e90e7-207">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e90e7-208">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e90e7-208">Minimum supported server</span></span><br/> | <span data-ttu-id="e90e7-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e90e7-209">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e90e7-210">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e90e7-210">Namespace</span></span><br/>                | <span data-ttu-id="e90e7-211">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e90e7-211">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e90e7-212">MOF</span><span class="sxs-lookup"><span data-stu-id="e90e7-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e90e7-213"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e90e7-213"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e90e7-214">DLL</span><span class="sxs-lookup"><span data-stu-id="e90e7-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e90e7-215"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e90e7-215"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e90e7-216">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e90e7-216">See also</span></span>

<dl> <dt>

<span data-ttu-id="e90e7-217">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e90e7-217">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e90e7-218">**\_Басесервице Win32**</span><span class="sxs-lookup"><span data-stu-id="e90e7-218">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

