---
description: Останавливает службу, представленную объектом, производным от Win32 \_ басесервице.
ms.assetid: 5d6427a6-d233-4db4-9235-c6187b36da5f
ms.tgt_platform: multiple
title: Метод «начало» класса Win32_BaseService (Сдоиас. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5b31b854255c6b20253875233bf2e5a44207a5a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655880"
---
# <a name="stopservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="4869a-103">Метод «начало» \_ класса Басесервице Win32</span><span class="sxs-lookup"><span data-stu-id="4869a-103">StopService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="4869a-104">Метод **"** неработающий [класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) " останавливает службу, представленную объектом, производным от [**Win32 \_ басесервице**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="4869a-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method stops the service represented by the object derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="4869a-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="4869a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4869a-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4869a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4869a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4869a-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="4869a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4869a-108">Parameters</span></span>

<span data-ttu-id="4869a-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4869a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4869a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4869a-110">Return value</span></span>

<span data-ttu-id="4869a-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="4869a-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="4869a-112">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="4869a-112">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-113">0</span><span class="sxs-lookup"><span data-stu-id="4869a-113">0</span></span>

<span data-ttu-id="4869a-114">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="4869a-114">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-115">**Не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="4869a-115">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-116">1</span><span class="sxs-lookup"><span data-stu-id="4869a-116">1</span></span>

<span data-ttu-id="4869a-117">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4869a-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-118">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="4869a-118">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-119">2</span><span class="sxs-lookup"><span data-stu-id="4869a-119">2</span></span>

<span data-ttu-id="4869a-120">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="4869a-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-121">**Работающие зависимые службы**</span><span class="sxs-lookup"><span data-stu-id="4869a-121">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-122">3</span><span class="sxs-lookup"><span data-stu-id="4869a-122">3</span></span>

<span data-ttu-id="4869a-123">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="4869a-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-124">**Недопустимый элемент управления службой**</span><span class="sxs-lookup"><span data-stu-id="4869a-124">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-125">4</span><span class="sxs-lookup"><span data-stu-id="4869a-125">4</span></span>

<span data-ttu-id="4869a-126">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="4869a-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-127">**Служба не может принять контроль**</span><span class="sxs-lookup"><span data-stu-id="4869a-127">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-128">5</span><span class="sxs-lookup"><span data-stu-id="4869a-128">5</span></span>

<span data-ttu-id="4869a-129">Запрошенный управляющий код не может быть отправлен в службу, так как состояние службы (свойство [**состояния**](win32-baseservice.md) [**Win32 \_ басесервице**](win32-baseservice.md)) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="4869a-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-130">**Служба неактивна**</span><span class="sxs-lookup"><span data-stu-id="4869a-130">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-131">6</span><span class="sxs-lookup"><span data-stu-id="4869a-131">6</span></span>

<span data-ttu-id="4869a-132">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="4869a-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-133">**Время ожидания запроса на обслуживание**</span><span class="sxs-lookup"><span data-stu-id="4869a-133">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-134">7</span><span class="sxs-lookup"><span data-stu-id="4869a-134">7</span></span>

<span data-ttu-id="4869a-135">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="4869a-135">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-136">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="4869a-136">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-137">8</span><span class="sxs-lookup"><span data-stu-id="4869a-137">8</span></span>

<span data-ttu-id="4869a-138">Интерактивный процесс.</span><span class="sxs-lookup"><span data-stu-id="4869a-138">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-139">**Путь не найден**</span><span class="sxs-lookup"><span data-stu-id="4869a-139">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-140">9</span><span class="sxs-lookup"><span data-stu-id="4869a-140">9</span></span>

<span data-ttu-id="4869a-141">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="4869a-141">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-142">**Служба уже запущена**</span><span class="sxs-lookup"><span data-stu-id="4869a-142">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-143">10</span><span class="sxs-lookup"><span data-stu-id="4869a-143">10</span></span>

<span data-ttu-id="4869a-144">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="4869a-144">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-145">**База данных службы заблокирована**</span><span class="sxs-lookup"><span data-stu-id="4869a-145">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-146">11</span><span class="sxs-lookup"><span data-stu-id="4869a-146">11</span></span>

<span data-ttu-id="4869a-147">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="4869a-147">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-148">**Зависимость службы удалена**</span><span class="sxs-lookup"><span data-stu-id="4869a-148">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-149">12</span><span class="sxs-lookup"><span data-stu-id="4869a-149">12</span></span>

<span data-ttu-id="4869a-150">Служба, от которой зависит эта служба, была удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="4869a-150">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-151">**Сбой зависимости службы**</span><span class="sxs-lookup"><span data-stu-id="4869a-151">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-152">13</span><span class="sxs-lookup"><span data-stu-id="4869a-152">13</span></span>

<span data-ttu-id="4869a-153">Службе не удалось найти службу, необходимую зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="4869a-153">The service failed to find the service required from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-154">**Служба отключена**</span><span class="sxs-lookup"><span data-stu-id="4869a-154">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-155">14</span><span class="sxs-lookup"><span data-stu-id="4869a-155">14</span></span>

<span data-ttu-id="4869a-156">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="4869a-156">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-157">**Сбой при входе в службу**</span><span class="sxs-lookup"><span data-stu-id="4869a-157">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-158">15</span><span class="sxs-lookup"><span data-stu-id="4869a-158">15</span></span>

<span data-ttu-id="4869a-159">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="4869a-159">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-160">**Служба помечена для удаления**</span><span class="sxs-lookup"><span data-stu-id="4869a-160">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-161">16</span><span class="sxs-lookup"><span data-stu-id="4869a-161">16</span></span>

<span data-ttu-id="4869a-162">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="4869a-162">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-163">**Служба без потока**</span><span class="sxs-lookup"><span data-stu-id="4869a-163">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-164">17</span><span class="sxs-lookup"><span data-stu-id="4869a-164">17</span></span>

<span data-ttu-id="4869a-165">Отсутствует поток исполнения для этой службы.</span><span class="sxs-lookup"><span data-stu-id="4869a-165">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-166">**Состояние "циклическая зависимость"**</span><span class="sxs-lookup"><span data-stu-id="4869a-166">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-167">18</span><span class="sxs-lookup"><span data-stu-id="4869a-167">18</span></span>

<span data-ttu-id="4869a-168">При запуске службы обнаружены циклические зависимости.</span><span class="sxs-lookup"><span data-stu-id="4869a-168">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-169">**Состояние "повторяющееся имя"**</span><span class="sxs-lookup"><span data-stu-id="4869a-169">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-170">19</span><span class="sxs-lookup"><span data-stu-id="4869a-170">19</span></span>

<span data-ttu-id="4869a-171">Служба с таким именем уже запущена.</span><span class="sxs-lookup"><span data-stu-id="4869a-171">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-172">**Состояние "Недопустимое имя"**</span><span class="sxs-lookup"><span data-stu-id="4869a-172">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-173">20</span><span class="sxs-lookup"><span data-stu-id="4869a-173">20</span></span>

<span data-ttu-id="4869a-174">В имени службы присутствуют недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="4869a-174">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-175">**Недопустимый параметр Status**</span><span class="sxs-lookup"><span data-stu-id="4869a-175">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-176">21</span><span class="sxs-lookup"><span data-stu-id="4869a-176">21</span></span>

<span data-ttu-id="4869a-177">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="4869a-177">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-178">**Недопустимое состояние учетной записи службы**</span><span class="sxs-lookup"><span data-stu-id="4869a-178">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-179">22</span><span class="sxs-lookup"><span data-stu-id="4869a-179">22</span></span>

<span data-ttu-id="4869a-180">Учетная запись, под которой будет запускаться эта служба, недопустима или не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="4869a-180">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-181">**Служба состояний существует**</span><span class="sxs-lookup"><span data-stu-id="4869a-181">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-182">23</span><span class="sxs-lookup"><span data-stu-id="4869a-182">23</span></span>

<span data-ttu-id="4869a-183">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="4869a-183">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-184">**Служба уже приостановлена**</span><span class="sxs-lookup"><span data-stu-id="4869a-184">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-185">24</span><span class="sxs-lookup"><span data-stu-id="4869a-185">24</span></span>

<span data-ttu-id="4869a-186">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="4869a-186">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="4869a-187">**Другое**</span><span class="sxs-lookup"><span data-stu-id="4869a-187">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="4869a-188">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="4869a-188">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4869a-189">Требования</span><span class="sxs-lookup"><span data-stu-id="4869a-189">Requirements</span></span>



| <span data-ttu-id="4869a-190">Требование</span><span class="sxs-lookup"><span data-stu-id="4869a-190">Requirement</span></span> | <span data-ttu-id="4869a-191">Значение</span><span class="sxs-lookup"><span data-stu-id="4869a-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4869a-192">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4869a-192">Minimum supported client</span></span><br/> | <span data-ttu-id="4869a-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4869a-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4869a-194">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4869a-194">Minimum supported server</span></span><br/> | <span data-ttu-id="4869a-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4869a-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4869a-196">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4869a-196">Namespace</span></span><br/>                | <span data-ttu-id="4869a-197">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4869a-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4869a-198">Header</span><span class="sxs-lookup"><span data-stu-id="4869a-198">Header</span></span><br/>                   | <dl> <span data-ttu-id="4869a-199"><dt>Сдоиас. h</dt></span><span class="sxs-lookup"><span data-stu-id="4869a-199"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="4869a-200">MOF</span><span class="sxs-lookup"><span data-stu-id="4869a-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4869a-201"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4869a-201"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4869a-202">DLL</span><span class="sxs-lookup"><span data-stu-id="4869a-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4869a-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4869a-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4869a-204">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4869a-204">See also</span></span>

<dl> <dt>

<span data-ttu-id="4869a-205">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4869a-205">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4869a-206">**\_Басесервице Win32**</span><span class="sxs-lookup"><span data-stu-id="4869a-206">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

