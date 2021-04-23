---
description: Изменяет режим запуска \_ службы Win32 SystemDriver.
ms.assetid: 34f4e0ac-d8a0-4be7-8c84-0252e50db441
ms.tgt_platform: multiple
title: Метод Чанжестартмоде класса Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: edb6dfc9d745f5e408871246b581e6fab7eb72d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538774"
---
# <a name="changestartmode-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="17daf-103">Метод Чанжестартмоде \_ класса Win32 SystemDriver</span><span class="sxs-lookup"><span data-stu-id="17daf-103">ChangeStartMode method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="17daf-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) чанжестартмоде изменяет режим запуска службы [**\_ SystemDriver Win32**](win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="17daf-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_SystemDriver**](win32-systemdriver.md) service.</span></span>

<span data-ttu-id="17daf-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="17daf-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="17daf-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="17daf-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="17daf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17daf-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="17daf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="17daf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17daf-109">*StartMode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17daf-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17daf-110">Режим запуска базовой службы Windows.</span><span class="sxs-lookup"><span data-stu-id="17daf-110">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="17daf-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Запуск загрузки** ("Boot")</span><span class="sxs-lookup"><span data-stu-id="17daf-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="17daf-112">Драйвер устройства запущен загрузчиком операционной системы.</span><span class="sxs-lookup"><span data-stu-id="17daf-112">Device driver started by the operating system loader.</span></span> <span data-ttu-id="17daf-113">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="17daf-113">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="17daf-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Система** ("System")</span><span class="sxs-lookup"><span data-stu-id="17daf-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="17daf-115">Драйвер устройства запущен процессом инициализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="17daf-115">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="17daf-116">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="17daf-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="17daf-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Автоматический запуск** (автоматический)</span><span class="sxs-lookup"><span data-stu-id="17daf-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="17daf-118">Служба запускается автоматически диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="17daf-118">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="17daf-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Запуск по требованию** (вручную)</span><span class="sxs-lookup"><span data-stu-id="17daf-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="17daf-120">Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="17daf-120">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="17daf-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** ("отключено")</span><span class="sxs-lookup"><span data-stu-id="17daf-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="17daf-122">Служба, которая больше не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="17daf-122">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17daf-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17daf-123">Return value</span></span>

<span data-ttu-id="17daf-124">Возвращает значение 0 (нуль), если служба была успешно изменена, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="17daf-124">Returns a value of 0 (zero) if the service was successfully modified, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="17daf-125">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="17daf-125">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-126">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="17daf-126">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-127">**Отказано в доступе** (2)</span><span class="sxs-lookup"><span data-stu-id="17daf-127">**Access Denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-128">**Запуск зависимых служб** (3)</span><span class="sxs-lookup"><span data-stu-id="17daf-128">**Dependent Services Running** (3)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-129">**Недопустимый элемент управления службой** (4)</span><span class="sxs-lookup"><span data-stu-id="17daf-129">**Invalid Service Control** (4)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-130">**Служба не может принять управление** (5)</span><span class="sxs-lookup"><span data-stu-id="17daf-130">**Service Cannot Accept Control** (5)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-131">**Служба неактивна** (6)</span><span class="sxs-lookup"><span data-stu-id="17daf-131">**Service Not Active** (6)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-132">**Время ожидания запроса на обслуживание** (7)</span><span class="sxs-lookup"><span data-stu-id="17daf-132">**Service Request Timeout** (7)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-133">**Неизвестный сбой** (8)</span><span class="sxs-lookup"><span data-stu-id="17daf-133">**Unknown Failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-134">**Путь не найден** (9)</span><span class="sxs-lookup"><span data-stu-id="17daf-134">**Path Not Found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-135">**Служба уже запущена** (10)</span><span class="sxs-lookup"><span data-stu-id="17daf-135">**Service Already Running** (10)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-136">**База данных службы заблокирована** (11)</span><span class="sxs-lookup"><span data-stu-id="17daf-136">**Service Database Locked** (11)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-137">**Удалена зависимость службы** (12)</span><span class="sxs-lookup"><span data-stu-id="17daf-137">**Service Dependency Deleted** (12)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-138">**Сбой зависимости службы** (13)</span><span class="sxs-lookup"><span data-stu-id="17daf-138">**Service Dependency Failure** (13)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-139">**Служба отключена** (14)</span><span class="sxs-lookup"><span data-stu-id="17daf-139">**Service Disabled** (14)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-140">**Сбой входа службы** (15)</span><span class="sxs-lookup"><span data-stu-id="17daf-140">**Service Logon Failed** (15)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-141">**Служба помечена для удаления** (16)</span><span class="sxs-lookup"><span data-stu-id="17daf-141">**Service Marked For Deletion** (16)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-142">**Служба без потока** (17)</span><span class="sxs-lookup"><span data-stu-id="17daf-142">**Service No Thread** (17)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-143">**Состояние "циклическая зависимость** " (18)</span><span class="sxs-lookup"><span data-stu-id="17daf-143">**Status Circular Dependency** (18)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-144">**Состояние "повторяющееся имя** " (19)</span><span class="sxs-lookup"><span data-stu-id="17daf-144">**Status Duplicate Name** (19)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-145">**Состояние недопустимое имя** (20)</span><span class="sxs-lookup"><span data-stu-id="17daf-145">**Status Invalid Name** (20)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-146">**Недопустимый параметр Status** (21)</span><span class="sxs-lookup"><span data-stu-id="17daf-146">**Status Invalid Parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-147">**Недопустимое состояние учетной записи службы** (22)</span><span class="sxs-lookup"><span data-stu-id="17daf-147">**Status Invalid Service Account** (22)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-148">**Служба состояния существует** (23)</span><span class="sxs-lookup"><span data-stu-id="17daf-148">**Status Service Exists** (23)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-149">**Служба уже приостановлена** (24)</span><span class="sxs-lookup"><span data-stu-id="17daf-149">**Service Already Paused** (24)</span></span>
</dt> <dt>

<span data-ttu-id="17daf-150">**Другие** (25 4294967295)</span><span class="sxs-lookup"><span data-stu-id="17daf-150">**Other** (25 4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="17daf-151">Требования</span><span class="sxs-lookup"><span data-stu-id="17daf-151">Requirements</span></span>



| <span data-ttu-id="17daf-152">Требование</span><span class="sxs-lookup"><span data-stu-id="17daf-152">Requirement</span></span> | <span data-ttu-id="17daf-153">Значение</span><span class="sxs-lookup"><span data-stu-id="17daf-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17daf-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17daf-154">Minimum supported client</span></span><br/> | <span data-ttu-id="17daf-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17daf-155">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17daf-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17daf-156">Minimum supported server</span></span><br/> | <span data-ttu-id="17daf-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17daf-157">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17daf-158">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="17daf-158">Namespace</span></span><br/>                | <span data-ttu-id="17daf-159">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="17daf-159">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17daf-160">MOF</span><span class="sxs-lookup"><span data-stu-id="17daf-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17daf-161"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17daf-161"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17daf-162">DLL</span><span class="sxs-lookup"><span data-stu-id="17daf-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17daf-163"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17daf-163"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17daf-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17daf-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="17daf-165">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17daf-165">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="17daf-166">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="17daf-166">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

