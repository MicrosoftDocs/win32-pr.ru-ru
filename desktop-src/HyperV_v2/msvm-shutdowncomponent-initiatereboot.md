---
description: Инициирует операцию перезагрузки операционной системы для связанной дочерней виртуальной машины.
ms.assetid: 9f3ebbaf-ee0f-4c01-8f73-1f37c08a0feb
title: Метод Инитиатеребут класса Msvm_ShutdownComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateReboot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 527569e8a5d6c2bb0a54294637ae19c13f5e3af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650584"
---
# <a name="initiatereboot-method-of-the-msvm_shutdowncomponent-class"></a><span data-ttu-id="9bfa7-103">Метод Инитиатеребут \_ класса Шутдовнкомпонент мсвм</span><span class="sxs-lookup"><span data-stu-id="9bfa7-103">InitiateReboot method of the Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="9bfa7-104">Инициирует операцию перезагрузки операционной системы для связанной дочерней виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-104">Initiates an operating system reboot operation on the associated child virtual machine.</span></span>

<span data-ttu-id="9bfa7-105">Если возвращается ноль (0), перезагрузка была успешно инициирована.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-105">If zero (0) is returned, then the reboot was initiated successfully.</span></span> <span data-ttu-id="9bfa7-106">Любой другой код возврата указывает на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-106">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bfa7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bfa7-107">Syntax</span></span>


```mof
uint32 InitiateReboot(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a><span data-ttu-id="9bfa7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bfa7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bfa7-109">*Force* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9bfa7-109">*Force* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bfa7-110">Флаг, который при значении TRUE принудительно закрывает приложения, несмотря на наличие несохраненных данных.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-110">A flag which, if TRUE, forces applications to be closed despite having unsaved data.</span></span>

</dd> <dt>

<span data-ttu-id="9bfa7-111">*Причина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9bfa7-111">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bfa7-112">Причина операции перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-112">The reason for the reboot operation.</span></span> <span data-ttu-id="9bfa7-113">Это определяемая пользователем строка.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-113">This is a user-defined string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bfa7-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9bfa7-114">Return value</span></span>

<span data-ttu-id="9bfa7-115">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="9bfa7-115">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="9bfa7-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9bfa7-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9bfa7-118">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9bfa7-119">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9bfa7-120">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9bfa7-121">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9bfa7-122">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9bfa7-123">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9bfa7-124">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9bfa7-125">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9bfa7-126">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9bfa7-127">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9bfa7-128">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="9bfa7-129">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="9bfa7-130">**Система не готова** (32780)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-130">**The system is not ready** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="9bfa7-131">**Компьютер заблокирован и не может завершить работу без параметра Force** (32781)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-131">**The machine is locked and cannot be shut down without the force option** (32781)</span></span>
</dt> <dt>

<span data-ttu-id="9bfa7-132">Выполняется **Завершение работы системы** (32782)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-132">**A system shutdown is in progress** (32782)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9bfa7-133">Требования</span><span class="sxs-lookup"><span data-stu-id="9bfa7-133">Requirements</span></span>



| <span data-ttu-id="9bfa7-134">Требование</span><span class="sxs-lookup"><span data-stu-id="9bfa7-134">Requirement</span></span> | <span data-ttu-id="9bfa7-135">Значение</span><span class="sxs-lookup"><span data-stu-id="9bfa7-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bfa7-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9bfa7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9bfa7-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9bfa7-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9bfa7-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9bfa7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9bfa7-139">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9bfa7-139">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9bfa7-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9bfa7-140">Namespace</span></span><br/>                | <span data-ttu-id="9bfa7-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9bfa7-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9bfa7-142">MOF</span><span class="sxs-lookup"><span data-stu-id="9bfa7-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9bfa7-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9bfa7-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9bfa7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9bfa7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bfa7-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9bfa7-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9bfa7-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9bfa7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bfa7-147">**Мсвм \_ шутдовнкомпонент**</span><span class="sxs-lookup"><span data-stu-id="9bfa7-147">**Msvm\_ShutdownComponent**</span></span>](msvm-shutdowncomponent.md)
</dt> </dl>

 

 




