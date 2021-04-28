---
description: Метод Жетбуттонстате класса Msvm_SyntheticMouse — извлекает текущее состояние указанной кнопки устройства.
ms.assetid: 66363AF1-E360-478D-8E62-513DE66EF130
title: Метод Жетбуттонстате класса Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26839292cf2fb3099e740629b28c7de0fbe3f60f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119392"
---
# <a name="getbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="8f54c-103">Метод Жетбуттонстате \_ класса Синсетикмаусе мсвм</span><span class="sxs-lookup"><span data-stu-id="8f54c-103">GetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="8f54c-104">Извлекает текущее состояние указанной кнопки устройства.</span><span class="sxs-lookup"><span data-stu-id="8f54c-104">Retrieves the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f54c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f54c-105">Syntax</span></span>


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="8f54c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f54c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f54c-107">*буттониндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8f54c-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f54c-108">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f54c-108">Type: **uint32**</span></span>

<span data-ttu-id="8f54c-109">Отсчитываемый от 1 индекс кнопки для запроса.</span><span class="sxs-lookup"><span data-stu-id="8f54c-109">The 1-based index of the button to query.</span></span>

</dd> <dt>

<span data-ttu-id="8f54c-110">*раскрывающийся список* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8f54c-110">*isDown* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f54c-111">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8f54c-111">Type: **boolean**</span></span>

<span data-ttu-id="8f54c-112">Текущее состояние кнопки.</span><span class="sxs-lookup"><span data-stu-id="8f54c-112">The current down state of the button.</span></span> <span data-ttu-id="8f54c-113">Значение **true** означает, что кнопка не работает.</span><span class="sxs-lookup"><span data-stu-id="8f54c-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f54c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f54c-114">Return value</span></span>

<span data-ttu-id="8f54c-115">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f54c-115">Type: **uint32**</span></span>

<span data-ttu-id="8f54c-116">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="8f54c-116">A return value of zero indicates success.</span></span> <span data-ttu-id="8f54c-117">Ненулевое значение указывает на ошибку запроса.</span><span class="sxs-lookup"><span data-stu-id="8f54c-117">A nonzero value indicates a query failure.</span></span>

<dl> <dt>

<span data-ttu-id="8f54c-118">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="8f54c-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8f54c-119">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="8f54c-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8f54c-120">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="8f54c-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8f54c-121">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="8f54c-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8f54c-122">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="8f54c-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8f54c-123">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="8f54c-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8f54c-124">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="8f54c-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8f54c-125">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="8f54c-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8f54c-126">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="8f54c-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8f54c-127">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="8f54c-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="8f54c-128">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="8f54c-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="8f54c-129">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="8f54c-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="8f54c-130">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="8f54c-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="8f54c-131">Remarks</span><span class="sxs-lookup"><span data-stu-id="8f54c-131">Remarks</span></span>

<span data-ttu-id="8f54c-132">Доступ к классу [**\_ синсетикмаусе мсвм**](msvm-syntheticmouse.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="8f54c-132">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8f54c-133">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8f54c-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f54c-134">Требования</span><span class="sxs-lookup"><span data-stu-id="8f54c-134">Requirements</span></span>



| <span data-ttu-id="8f54c-135">Требование</span><span class="sxs-lookup"><span data-stu-id="8f54c-135">Requirement</span></span> | <span data-ttu-id="8f54c-136">Значение</span><span class="sxs-lookup"><span data-stu-id="8f54c-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f54c-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8f54c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8f54c-138">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8f54c-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8f54c-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8f54c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8f54c-140">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8f54c-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8f54c-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8f54c-141">Namespace</span></span><br/>                | <span data-ttu-id="8f54c-142">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="8f54c-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8f54c-143">MOF</span><span class="sxs-lookup"><span data-stu-id="8f54c-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f54c-144"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f54c-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f54c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8f54c-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f54c-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8f54c-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8f54c-147">См. также</span><span class="sxs-lookup"><span data-stu-id="8f54c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f54c-148">**Мсвм \_ синсетикмаусе**</span><span class="sxs-lookup"><span data-stu-id="8f54c-148">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

