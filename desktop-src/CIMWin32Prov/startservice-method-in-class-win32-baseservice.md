---
description: Пытается перевести службу в состояние запуска.
ms.assetid: 3bafa228-a84b-4f14-a9e5-dfad09b83610
ms.tgt_platform: multiple
title: Метод StartService класса Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9fbfad47899193a25be08292aff97f9d8e211ba7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895958"
---
# <a name="startservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="c7256-103">Метод StartService \_ класса Win32 басесервице</span><span class="sxs-lookup"><span data-stu-id="c7256-103">StartService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="c7256-104">Метод **StartService** пытается перевести службу в состояние запуска.</span><span class="sxs-lookup"><span data-stu-id="c7256-104">The **StartService** method attempts to place the service into its startup state.</span></span>

<span data-ttu-id="c7256-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="c7256-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c7256-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c7256-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7256-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7256-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="c7256-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7256-108">Parameters</span></span>

<span data-ttu-id="c7256-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c7256-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7256-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7256-110">Return value</span></span>

<span data-ttu-id="c7256-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="c7256-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c7256-112">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="c7256-112">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-113">0</span><span class="sxs-lookup"><span data-stu-id="c7256-113">0</span></span>

<span data-ttu-id="c7256-114">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="c7256-114">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-115">**Не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="c7256-115">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-116">1</span><span class="sxs-lookup"><span data-stu-id="c7256-116">1</span></span>

<span data-ttu-id="c7256-117">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c7256-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-118">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="c7256-118">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-119">2</span><span class="sxs-lookup"><span data-stu-id="c7256-119">2</span></span>

<span data-ttu-id="c7256-120">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="c7256-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-121">**Работающие зависимые службы**</span><span class="sxs-lookup"><span data-stu-id="c7256-121">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-122">3</span><span class="sxs-lookup"><span data-stu-id="c7256-122">3</span></span>

<span data-ttu-id="c7256-123">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="c7256-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-124">**Недопустимый элемент управления службой**</span><span class="sxs-lookup"><span data-stu-id="c7256-124">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-125">4</span><span class="sxs-lookup"><span data-stu-id="c7256-125">4</span></span>

<span data-ttu-id="c7256-126">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="c7256-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-127">**Служба не может принять контроль**</span><span class="sxs-lookup"><span data-stu-id="c7256-127">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-128">5</span><span class="sxs-lookup"><span data-stu-id="c7256-128">5</span></span>

<span data-ttu-id="c7256-129">Запрошенный управляющий код не может быть отправлен в службу, так как состояние службы (свойство [**состояния**](win32-baseservice.md) [**Win32 \_ басесервице**](win32-baseservice.md)) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="c7256-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-130">**Служба неактивна**</span><span class="sxs-lookup"><span data-stu-id="c7256-130">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-131">6</span><span class="sxs-lookup"><span data-stu-id="c7256-131">6</span></span>

<span data-ttu-id="c7256-132">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="c7256-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-133">**Время ожидания запроса на обслуживание**</span><span class="sxs-lookup"><span data-stu-id="c7256-133">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-134">7</span><span class="sxs-lookup"><span data-stu-id="c7256-134">7</span></span>

<span data-ttu-id="c7256-135">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="c7256-135">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-136">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="c7256-136">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-137">8</span><span class="sxs-lookup"><span data-stu-id="c7256-137">8</span></span>

<span data-ttu-id="c7256-138">Интерактивный процесс.</span><span class="sxs-lookup"><span data-stu-id="c7256-138">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-139">**Путь не найден**</span><span class="sxs-lookup"><span data-stu-id="c7256-139">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-140">9</span><span class="sxs-lookup"><span data-stu-id="c7256-140">9</span></span>

<span data-ttu-id="c7256-141">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="c7256-141">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-142">**Служба уже запущена**</span><span class="sxs-lookup"><span data-stu-id="c7256-142">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-143">10</span><span class="sxs-lookup"><span data-stu-id="c7256-143">10</span></span>

<span data-ttu-id="c7256-144">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="c7256-144">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-145">**База данных службы заблокирована**</span><span class="sxs-lookup"><span data-stu-id="c7256-145">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-146">11</span><span class="sxs-lookup"><span data-stu-id="c7256-146">11</span></span>

<span data-ttu-id="c7256-147">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="c7256-147">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-148">**Зависимость службы удалена**</span><span class="sxs-lookup"><span data-stu-id="c7256-148">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-149">12</span><span class="sxs-lookup"><span data-stu-id="c7256-149">12</span></span>

<span data-ttu-id="c7256-150">Служба, от которой зависит эта служба, была удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="c7256-150">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-151">**Сбой зависимости службы**</span><span class="sxs-lookup"><span data-stu-id="c7256-151">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-152">13</span><span class="sxs-lookup"><span data-stu-id="c7256-152">13</span></span>

<span data-ttu-id="c7256-153">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="c7256-153">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-154">**Служба отключена**</span><span class="sxs-lookup"><span data-stu-id="c7256-154">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-155">14</span><span class="sxs-lookup"><span data-stu-id="c7256-155">14</span></span>

<span data-ttu-id="c7256-156">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="c7256-156">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-157">**Сбой при входе в службу**</span><span class="sxs-lookup"><span data-stu-id="c7256-157">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-158">15</span><span class="sxs-lookup"><span data-stu-id="c7256-158">15</span></span>

<span data-ttu-id="c7256-159">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="c7256-159">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-160">**Служба помечена для удаления**</span><span class="sxs-lookup"><span data-stu-id="c7256-160">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-161">16</span><span class="sxs-lookup"><span data-stu-id="c7256-161">16</span></span>

<span data-ttu-id="c7256-162">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="c7256-162">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-163">**Служба без потока**</span><span class="sxs-lookup"><span data-stu-id="c7256-163">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-164">17</span><span class="sxs-lookup"><span data-stu-id="c7256-164">17</span></span>

<span data-ttu-id="c7256-165">Отсутствует поток исполнения для этой службы.</span><span class="sxs-lookup"><span data-stu-id="c7256-165">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-166">**Состояние "циклическая зависимость"**</span><span class="sxs-lookup"><span data-stu-id="c7256-166">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-167">18</span><span class="sxs-lookup"><span data-stu-id="c7256-167">18</span></span>

<span data-ttu-id="c7256-168">При запуске службы обнаружены циклические зависимости.</span><span class="sxs-lookup"><span data-stu-id="c7256-168">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-169">**Состояние "повторяющееся имя"**</span><span class="sxs-lookup"><span data-stu-id="c7256-169">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-170">19</span><span class="sxs-lookup"><span data-stu-id="c7256-170">19</span></span>

<span data-ttu-id="c7256-171">Служба с таким именем уже запущена.</span><span class="sxs-lookup"><span data-stu-id="c7256-171">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-172">**Состояние "Недопустимое имя"**</span><span class="sxs-lookup"><span data-stu-id="c7256-172">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-173">20</span><span class="sxs-lookup"><span data-stu-id="c7256-173">20</span></span>

<span data-ttu-id="c7256-174">В имени службы присутствуют недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="c7256-174">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-175">**Недопустимый параметр Status**</span><span class="sxs-lookup"><span data-stu-id="c7256-175">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-176">21</span><span class="sxs-lookup"><span data-stu-id="c7256-176">21</span></span>

<span data-ttu-id="c7256-177">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="c7256-177">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-178">**Недопустимое состояние учетной записи службы**</span><span class="sxs-lookup"><span data-stu-id="c7256-178">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-179">22</span><span class="sxs-lookup"><span data-stu-id="c7256-179">22</span></span>

<span data-ttu-id="c7256-180">Учетная запись, под которой будет запускаться эта служба, недопустима или не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="c7256-180">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-181">**Служба состояний существует**</span><span class="sxs-lookup"><span data-stu-id="c7256-181">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-182">23</span><span class="sxs-lookup"><span data-stu-id="c7256-182">23</span></span>

<span data-ttu-id="c7256-183">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="c7256-183">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-184">**Служба уже приостановлена**</span><span class="sxs-lookup"><span data-stu-id="c7256-184">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-185">24</span><span class="sxs-lookup"><span data-stu-id="c7256-185">24</span></span>

<span data-ttu-id="c7256-186">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="c7256-186">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="c7256-187">**Другое**</span><span class="sxs-lookup"><span data-stu-id="c7256-187">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="c7256-188">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="c7256-188">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7256-189">Требования</span><span class="sxs-lookup"><span data-stu-id="c7256-189">Requirements</span></span>



| <span data-ttu-id="c7256-190">Требование</span><span class="sxs-lookup"><span data-stu-id="c7256-190">Requirement</span></span> | <span data-ttu-id="c7256-191">Значение</span><span class="sxs-lookup"><span data-stu-id="c7256-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7256-192">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7256-192">Minimum supported client</span></span><br/> | <span data-ttu-id="c7256-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7256-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c7256-194">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7256-194">Minimum supported server</span></span><br/> | <span data-ttu-id="c7256-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7256-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7256-196">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c7256-196">Namespace</span></span><br/>                | <span data-ttu-id="c7256-197">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c7256-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c7256-198">MOF</span><span class="sxs-lookup"><span data-stu-id="c7256-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7256-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7256-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7256-200">DLL</span><span class="sxs-lookup"><span data-stu-id="c7256-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7256-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7256-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7256-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7256-202">See also</span></span>

<dl> <dt>

<span data-ttu-id="c7256-203">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c7256-203">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c7256-204">**\_Басесервице Win32**</span><span class="sxs-lookup"><span data-stu-id="c7256-204">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

