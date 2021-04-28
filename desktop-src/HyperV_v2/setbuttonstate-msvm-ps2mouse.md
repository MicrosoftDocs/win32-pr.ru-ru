---
description: Метод Сетбуттонстате класса Msvm_Ps2Mouse — задает текущее состояние указанной кнопки устройства.
ms.assetid: 312A2B8B-D518-4797-9B50-F12493598CD6
title: Метод Сетбуттонстате класса Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ea6a984b84c7ee17436a7fb4738433edce6d68d8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118532"
---
# <a name="setbuttonstate-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="fef7a-103">Метод Сетбуттонстате \_ класса Ps2Mouse мсвм</span><span class="sxs-lookup"><span data-stu-id="fef7a-103">SetButtonState method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="fef7a-104">Задает текущее состояние указанной кнопки устройства.</span><span class="sxs-lookup"><span data-stu-id="fef7a-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="fef7a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fef7a-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean buttonState
);
```



## <a name="parameters"></a><span data-ttu-id="fef7a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fef7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fef7a-107">*буттониндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fef7a-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fef7a-108">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fef7a-108">Type: **uint32**</span></span>

<span data-ttu-id="fef7a-109">Отсчитываемый от 1 индекс изменяемой кнопки.</span><span class="sxs-lookup"><span data-stu-id="fef7a-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="fef7a-110">*буттонстате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fef7a-110">*buttonState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fef7a-111">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fef7a-111">Type: **boolean**</span></span>

<span data-ttu-id="fef7a-112">Новое состояние кнопки "отключено".</span><span class="sxs-lookup"><span data-stu-id="fef7a-112">The new down state of the button.</span></span> <span data-ttu-id="fef7a-113">Значение **true** означает, что кнопка не работает.</span><span class="sxs-lookup"><span data-stu-id="fef7a-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fef7a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fef7a-114">Return value</span></span>

<span data-ttu-id="fef7a-115">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fef7a-115">Type: **uint32**</span></span>

<span data-ttu-id="fef7a-116">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="fef7a-116">A return value of zero indicates success.</span></span> <span data-ttu-id="fef7a-117">Ненулевое значение указывает на ошибку при изменении состояния кнопки.</span><span class="sxs-lookup"><span data-stu-id="fef7a-117">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="fef7a-118">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="fef7a-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fef7a-119">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="fef7a-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fef7a-120">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="fef7a-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fef7a-121">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="fef7a-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fef7a-122">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="fef7a-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fef7a-123">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="fef7a-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fef7a-124">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="fef7a-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fef7a-125">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="fef7a-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fef7a-126">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="fef7a-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fef7a-127">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="fef7a-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fef7a-128">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="fef7a-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fef7a-129">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="fef7a-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fef7a-130">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="fef7a-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="fef7a-131">Remarks</span><span class="sxs-lookup"><span data-stu-id="fef7a-131">Remarks</span></span>

<span data-ttu-id="fef7a-132">Доступ к классу [**\_ Ps2Mouse мсвм**](msvm-ps2mouse.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="fef7a-132">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="fef7a-133">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="fef7a-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="fef7a-134">Требования</span><span class="sxs-lookup"><span data-stu-id="fef7a-134">Requirements</span></span>



| <span data-ttu-id="fef7a-135">Требование</span><span class="sxs-lookup"><span data-stu-id="fef7a-135">Requirement</span></span> | <span data-ttu-id="fef7a-136">Значение</span><span class="sxs-lookup"><span data-stu-id="fef7a-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fef7a-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fef7a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fef7a-138">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fef7a-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fef7a-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fef7a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fef7a-140">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fef7a-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fef7a-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fef7a-141">Namespace</span></span><br/>                | <span data-ttu-id="fef7a-142">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="fef7a-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fef7a-143">MOF</span><span class="sxs-lookup"><span data-stu-id="fef7a-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fef7a-144"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fef7a-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fef7a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="fef7a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fef7a-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fef7a-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fef7a-147">См. также</span><span class="sxs-lookup"><span data-stu-id="fef7a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fef7a-148">**Мсвм \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="fef7a-148">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

