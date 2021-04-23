---
description: Пытается перевести службу в состояние возобновления.
ms.assetid: df582402-d932-4132-a1ad-257b2993bbf6
ms.tgt_platform: multiple
title: Метод ResumeService класса Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bba09180121d5649542f70a01adf2cb3acd7b142
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655749"
---
# <a name="resumeservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="cf882-103">Метод ResumeService \_ класса Win32 басесервице</span><span class="sxs-lookup"><span data-stu-id="cf882-103">ResumeService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="cf882-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) ResumeService пытается перевести службу в состояние возобновления.</span><span class="sxs-lookup"><span data-stu-id="cf882-104">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the resumed state.</span></span>

<span data-ttu-id="cf882-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="cf882-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cf882-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cf882-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cf882-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf882-107">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="cf882-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf882-108">Parameters</span></span>

<span data-ttu-id="cf882-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cf882-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf882-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf882-110">Return value</span></span>

<span data-ttu-id="cf882-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="cf882-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="cf882-112">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="cf882-112">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-113">0</span><span class="sxs-lookup"><span data-stu-id="cf882-113">0</span></span>

<span data-ttu-id="cf882-114">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="cf882-114">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-115">**Не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="cf882-115">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-116">1</span><span class="sxs-lookup"><span data-stu-id="cf882-116">1</span></span>

<span data-ttu-id="cf882-117">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cf882-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-118">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="cf882-118">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-119">2</span><span class="sxs-lookup"><span data-stu-id="cf882-119">2</span></span>

<span data-ttu-id="cf882-120">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="cf882-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-121">**Работающие зависимые службы**</span><span class="sxs-lookup"><span data-stu-id="cf882-121">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-122">3</span><span class="sxs-lookup"><span data-stu-id="cf882-122">3</span></span>

<span data-ttu-id="cf882-123">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="cf882-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-124">**Недопустимый элемент управления службой**</span><span class="sxs-lookup"><span data-stu-id="cf882-124">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-125">4</span><span class="sxs-lookup"><span data-stu-id="cf882-125">4</span></span>

<span data-ttu-id="cf882-126">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="cf882-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-127">**Служба не может принять контроль**</span><span class="sxs-lookup"><span data-stu-id="cf882-127">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-128">5</span><span class="sxs-lookup"><span data-stu-id="cf882-128">5</span></span>

<span data-ttu-id="cf882-129">Запрошенный управляющий код не может быть отправлен в службу, так как состояние службы (свойство [**состояния**](win32-baseservice.md) [**Win32 \_ басесервице**](win32-baseservice.md)) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="cf882-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-130">**Служба неактивна**</span><span class="sxs-lookup"><span data-stu-id="cf882-130">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-131">6</span><span class="sxs-lookup"><span data-stu-id="cf882-131">6</span></span>

<span data-ttu-id="cf882-132">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="cf882-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-133">**Время ожидания запроса на обслуживание**</span><span class="sxs-lookup"><span data-stu-id="cf882-133">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-134">7</span><span class="sxs-lookup"><span data-stu-id="cf882-134">7</span></span>

<span data-ttu-id="cf882-135">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="cf882-135">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-136">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="cf882-136">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-137">8</span><span class="sxs-lookup"><span data-stu-id="cf882-137">8</span></span>

<span data-ttu-id="cf882-138">Интерактивный процесс.</span><span class="sxs-lookup"><span data-stu-id="cf882-138">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-139">**Путь не найден**</span><span class="sxs-lookup"><span data-stu-id="cf882-139">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-140">9</span><span class="sxs-lookup"><span data-stu-id="cf882-140">9</span></span>

<span data-ttu-id="cf882-141">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="cf882-141">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-142">**Служба уже запущена**</span><span class="sxs-lookup"><span data-stu-id="cf882-142">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-143">10</span><span class="sxs-lookup"><span data-stu-id="cf882-143">10</span></span>

<span data-ttu-id="cf882-144">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="cf882-144">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-145">**База данных службы заблокирована**</span><span class="sxs-lookup"><span data-stu-id="cf882-145">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-146">11</span><span class="sxs-lookup"><span data-stu-id="cf882-146">11</span></span>

<span data-ttu-id="cf882-147">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="cf882-147">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-148">**Зависимость службы удалена**</span><span class="sxs-lookup"><span data-stu-id="cf882-148">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-149">12</span><span class="sxs-lookup"><span data-stu-id="cf882-149">12</span></span>

<span data-ttu-id="cf882-150">Служба, от которой зависит эта служба, была удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="cf882-150">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-151">**Сбой зависимости службы**</span><span class="sxs-lookup"><span data-stu-id="cf882-151">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-152">13</span><span class="sxs-lookup"><span data-stu-id="cf882-152">13</span></span>

<span data-ttu-id="cf882-153">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="cf882-153">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-154">**Служба отключена**</span><span class="sxs-lookup"><span data-stu-id="cf882-154">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-155">14</span><span class="sxs-lookup"><span data-stu-id="cf882-155">14</span></span>

<span data-ttu-id="cf882-156">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="cf882-156">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-157">**Сбой при входе в службу**</span><span class="sxs-lookup"><span data-stu-id="cf882-157">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-158">15</span><span class="sxs-lookup"><span data-stu-id="cf882-158">15</span></span>

<span data-ttu-id="cf882-159">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="cf882-159">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-160">**Служба помечена для удаления**</span><span class="sxs-lookup"><span data-stu-id="cf882-160">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-161">16</span><span class="sxs-lookup"><span data-stu-id="cf882-161">16</span></span>

<span data-ttu-id="cf882-162">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="cf882-162">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-163">**Служба без потока**</span><span class="sxs-lookup"><span data-stu-id="cf882-163">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-164">17</span><span class="sxs-lookup"><span data-stu-id="cf882-164">17</span></span>

<span data-ttu-id="cf882-165">Отсутствует поток исполнения для этой службы.</span><span class="sxs-lookup"><span data-stu-id="cf882-165">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-166">**Состояние "циклическая зависимость"**</span><span class="sxs-lookup"><span data-stu-id="cf882-166">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-167">18</span><span class="sxs-lookup"><span data-stu-id="cf882-167">18</span></span>

<span data-ttu-id="cf882-168">При запуске службы обнаружены циклические зависимости.</span><span class="sxs-lookup"><span data-stu-id="cf882-168">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-169">**Состояние "повторяющееся имя"**</span><span class="sxs-lookup"><span data-stu-id="cf882-169">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-170">19</span><span class="sxs-lookup"><span data-stu-id="cf882-170">19</span></span>

<span data-ttu-id="cf882-171">Служба с таким именем уже запущена.</span><span class="sxs-lookup"><span data-stu-id="cf882-171">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-172">**Состояние "Недопустимое имя"**</span><span class="sxs-lookup"><span data-stu-id="cf882-172">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-173">20</span><span class="sxs-lookup"><span data-stu-id="cf882-173">20</span></span>

<span data-ttu-id="cf882-174">В имени службы присутствуют недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="cf882-174">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-175">**Недопустимый параметр Status**</span><span class="sxs-lookup"><span data-stu-id="cf882-175">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-176">21</span><span class="sxs-lookup"><span data-stu-id="cf882-176">21</span></span>

<span data-ttu-id="cf882-177">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="cf882-177">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-178">**Недопустимое состояние учетной записи службы**</span><span class="sxs-lookup"><span data-stu-id="cf882-178">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-179">22</span><span class="sxs-lookup"><span data-stu-id="cf882-179">22</span></span>

<span data-ttu-id="cf882-180">Учетная запись, под которой будет запускаться эта служба, недопустима или не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="cf882-180">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-181">**Служба состояний существует**</span><span class="sxs-lookup"><span data-stu-id="cf882-181">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-182">23</span><span class="sxs-lookup"><span data-stu-id="cf882-182">23</span></span>

<span data-ttu-id="cf882-183">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="cf882-183">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-184">**Служба уже приостановлена**</span><span class="sxs-lookup"><span data-stu-id="cf882-184">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-185">24</span><span class="sxs-lookup"><span data-stu-id="cf882-185">24</span></span>

<span data-ttu-id="cf882-186">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="cf882-186">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="cf882-187">**Другое**</span><span class="sxs-lookup"><span data-stu-id="cf882-187">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="cf882-188">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="cf882-188">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf882-189">Требования</span><span class="sxs-lookup"><span data-stu-id="cf882-189">Requirements</span></span>



| <span data-ttu-id="cf882-190">Требование</span><span class="sxs-lookup"><span data-stu-id="cf882-190">Requirement</span></span> | <span data-ttu-id="cf882-191">Значение</span><span class="sxs-lookup"><span data-stu-id="cf882-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf882-192">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf882-192">Minimum supported client</span></span><br/> | <span data-ttu-id="cf882-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf882-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cf882-194">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf882-194">Minimum supported server</span></span><br/> | <span data-ttu-id="cf882-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf882-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cf882-196">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cf882-196">Namespace</span></span><br/>                | <span data-ttu-id="cf882-197">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cf882-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cf882-198">MOF</span><span class="sxs-lookup"><span data-stu-id="cf882-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf882-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf882-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf882-200">DLL</span><span class="sxs-lookup"><span data-stu-id="cf882-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf882-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf882-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf882-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf882-202">See also</span></span>

<dl> <dt>

<span data-ttu-id="cf882-203">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cf882-203">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cf882-204">**\_Басесервице Win32**</span><span class="sxs-lookup"><span data-stu-id="cf882-204">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

