---
description: Задает текущее состояние указанной кнопки устройства.
ms.assetid: 942DB31C-09A2-43B6-A666-267AF6A84E0E
title: Метод Сетбуттонстате класса Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c99915fa8ede9cbb405f4483ac10ca9ff8efaf71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264403"
---
# <a name="setbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="4ce10-103">Метод Сетбуттонстате \_ класса Синсетикмаусе мсвм</span><span class="sxs-lookup"><span data-stu-id="4ce10-103">SetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="4ce10-104">Задает текущее состояние указанной кнопки устройства.</span><span class="sxs-lookup"><span data-stu-id="4ce10-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ce10-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ce10-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="4ce10-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ce10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ce10-107">*буттониндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ce10-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce10-108">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ce10-108">Type: **uint32**</span></span>

<span data-ttu-id="4ce10-109">Отсчитываемый от 1 индекс изменяемой кнопки.</span><span class="sxs-lookup"><span data-stu-id="4ce10-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="4ce10-110">*раскрывающийся список* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ce10-110">*isDown* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce10-111">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4ce10-111">Type: **boolean**</span></span>

<span data-ttu-id="4ce10-112">Новое состояние кнопки "отключено".</span><span class="sxs-lookup"><span data-stu-id="4ce10-112">The new down state of the button.</span></span> <span data-ttu-id="4ce10-113">Значение **true** означает, что кнопка не работает.</span><span class="sxs-lookup"><span data-stu-id="4ce10-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ce10-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ce10-114">Return value</span></span>

<span data-ttu-id="4ce10-115">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ce10-115">Type: **uint32**</span></span>

<span data-ttu-id="4ce10-116">Ненулевые значения указывают на ошибку при изменении состояния кнопки.</span><span class="sxs-lookup"><span data-stu-id="4ce10-116">Non zero values indicate a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="4ce10-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="4ce10-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4ce10-118">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="4ce10-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4ce10-119">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="4ce10-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4ce10-120">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="4ce10-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4ce10-121">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="4ce10-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4ce10-122">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="4ce10-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4ce10-123">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="4ce10-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4ce10-124">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="4ce10-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4ce10-125">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="4ce10-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4ce10-126">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="4ce10-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4ce10-127">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="4ce10-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4ce10-128">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="4ce10-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4ce10-129">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="4ce10-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="4ce10-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ce10-130">Remarks</span></span>

<span data-ttu-id="4ce10-131">Доступ к классу [**\_ синсетикмаусе мсвм**](msvm-syntheticmouse.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="4ce10-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4ce10-132">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4ce10-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ce10-133">Требования</span><span class="sxs-lookup"><span data-stu-id="4ce10-133">Requirements</span></span>



| <span data-ttu-id="4ce10-134">Требование</span><span class="sxs-lookup"><span data-stu-id="4ce10-134">Requirement</span></span> | <span data-ttu-id="4ce10-135">Значение</span><span class="sxs-lookup"><span data-stu-id="4ce10-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce10-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4ce10-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4ce10-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4ce10-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4ce10-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4ce10-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4ce10-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4ce10-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4ce10-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4ce10-140">Namespace</span></span><br/>                | <span data-ttu-id="4ce10-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4ce10-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4ce10-142">MOF</span><span class="sxs-lookup"><span data-stu-id="4ce10-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ce10-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ce10-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ce10-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4ce10-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ce10-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4ce10-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4ce10-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ce10-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ce10-147">**Мсвм \_ синсетикмаусе**</span><span class="sxs-lookup"><span data-stu-id="4ce10-147">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

