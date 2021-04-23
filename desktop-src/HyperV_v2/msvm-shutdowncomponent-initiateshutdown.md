---
description: Инициирует операцию завершения работы операционной системы на связанной дочерней виртуальной машине. Если возвращается ноль (0), то завершение работы было инициировано успешно. Любой другой код возврата указывает на состояние ошибки.
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: Метод Инитиатешутдовн класса Msvm_ShutdownComponent (winreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateShutdown
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 266ab64bb058325ac165a2e12c2a91d442a90269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265242"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a><span data-ttu-id="950d0-105">Метод Инитиатешутдовн \_ класса Шутдовнкомпонент мсвм</span><span class="sxs-lookup"><span data-stu-id="950d0-105">InitiateShutdown method of the Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="950d0-106">Инициирует операцию завершения работы операционной системы на связанной дочерней виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="950d0-106">Initiates an operating system shutdown operation on the associated child virtual machine.</span></span> <span data-ttu-id="950d0-107">Если возвращается ноль (0), то завершение работы было инициировано успешно.</span><span class="sxs-lookup"><span data-stu-id="950d0-107">If zero (0) is returned, then the shutdown was initiated successfully.</span></span> <span data-ttu-id="950d0-108">Любой другой код возврата указывает на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="950d0-108">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="950d0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="950d0-109">Syntax</span></span>


```mof
uint32 InitiateShutdown(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a><span data-ttu-id="950d0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="950d0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="950d0-111">*Force* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="950d0-111">*Force* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="950d0-112">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="950d0-112">Type: **boolean**</span></span>

<span data-ttu-id="950d0-113">Флаг, который при **значении true** принудительно закрывает приложения, несмотря на наличие несохраненных данных.</span><span class="sxs-lookup"><span data-stu-id="950d0-113">A flag which, if **True**, forces applications to be closed despite having unsaved data.</span></span>

</dd> <dt>

<span data-ttu-id="950d0-114">*Причина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="950d0-114">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="950d0-115">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="950d0-115">Type: **string**</span></span>

<span data-ttu-id="950d0-116">Причина операции завершения работы.</span><span class="sxs-lookup"><span data-stu-id="950d0-116">The reason for the shutdown operation.</span></span> <span data-ttu-id="950d0-117">Это определяемая пользователем строка.</span><span class="sxs-lookup"><span data-stu-id="950d0-117">This is a user-defined string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="950d0-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="950d0-118">Return value</span></span>

<span data-ttu-id="950d0-119">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="950d0-119">Type: **uint32**</span></span>

<dl> <dt>

<span data-ttu-id="950d0-120">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="950d0-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="950d0-121">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="950d0-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="950d0-122">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="950d0-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="950d0-123">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="950d0-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="950d0-124">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="950d0-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="950d0-125">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="950d0-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="950d0-126">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="950d0-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="950d0-127">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="950d0-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="950d0-128">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="950d0-128">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="950d0-129">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="950d0-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="950d0-130">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="950d0-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="950d0-131">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="950d0-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="950d0-132">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="950d0-132">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="950d0-133">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="950d0-133">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="950d0-134">**Система не готова** (32780)</span><span class="sxs-lookup"><span data-stu-id="950d0-134">**The system is not ready** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="950d0-135">**Компьютер заблокирован и не может завершить работу без параметра Force** (32781)</span><span class="sxs-lookup"><span data-stu-id="950d0-135">**The machine is locked and cannot be shut down without the force option** (32781)</span></span>
</dt> <dt>

<span data-ttu-id="950d0-136">Выполняется **Завершение работы системы** (32782)</span><span class="sxs-lookup"><span data-stu-id="950d0-136">**A system shutdown is in progress** (32782)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="950d0-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="950d0-137">Remarks</span></span>

<span data-ttu-id="950d0-138">Доступ к классу [**\_ шутдовнкомпонент мсвм**](msvm-shutdowncomponent.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="950d0-138">Access to the [**Msvm\_ShutdownComponent**](msvm-shutdowncomponent.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="950d0-139">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="950d0-139">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="950d0-140">Требования</span><span class="sxs-lookup"><span data-stu-id="950d0-140">Requirements</span></span>



| <span data-ttu-id="950d0-141">Требование</span><span class="sxs-lookup"><span data-stu-id="950d0-141">Requirement</span></span> | <span data-ttu-id="950d0-142">Значение</span><span class="sxs-lookup"><span data-stu-id="950d0-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="950d0-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="950d0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="950d0-144">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="950d0-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="950d0-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="950d0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="950d0-146">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="950d0-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="950d0-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="950d0-147">Namespace</span></span><br/>                | <span data-ttu-id="950d0-148">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="950d0-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="950d0-149">Header</span><span class="sxs-lookup"><span data-stu-id="950d0-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="950d0-150"><dt>Winreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="950d0-150"><dt>Winreg.h</dt></span></span> </dl>                     |
| <span data-ttu-id="950d0-151">MOF</span><span class="sxs-lookup"><span data-stu-id="950d0-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="950d0-152"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="950d0-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="950d0-153">DLL</span><span class="sxs-lookup"><span data-stu-id="950d0-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="950d0-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="950d0-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="950d0-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="950d0-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="950d0-156">**Мсвм \_ шутдовнкомпонент**</span><span class="sxs-lookup"><span data-stu-id="950d0-156">**Msvm\_ShutdownComponent**</span></span>](msvm-shutdowncomponent.md)
</dt> </dl>

 

