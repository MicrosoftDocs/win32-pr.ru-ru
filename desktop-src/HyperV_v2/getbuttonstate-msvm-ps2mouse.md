---
description: Метод Жетбуттонстате класса Msvm_Ps2Mouse — извлекает текущее состояние указанной кнопки устройства.
ms.assetid: 7772A3AC-1677-44A7-9E5E-D31E90988705
title: Метод Жетбуттонстате класса Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 160134a2ae48bb23dc525eeded70b483484e0b71
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112202"
---
# <a name="getbuttonstate-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="9b6cd-103">Метод Жетбуттонстате \_ класса Ps2Mouse мсвм</span><span class="sxs-lookup"><span data-stu-id="9b6cd-103">GetButtonState method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="9b6cd-104">Извлекает текущее состояние указанной кнопки устройства.</span><span class="sxs-lookup"><span data-stu-id="9b6cd-104">Retrieves the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b6cd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b6cd-105">Syntax</span></span>


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean buttonState
);
```



## <a name="parameters"></a><span data-ttu-id="9b6cd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b6cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b6cd-107">*буттониндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b6cd-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6cd-108">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b6cd-108">Type: **uint32**</span></span>

<span data-ttu-id="9b6cd-109">Отсчитываемый от 1 индекс кнопки для запроса.</span><span class="sxs-lookup"><span data-stu-id="9b6cd-109">The 1-based index of the button to query.</span></span>

</dd> <dt>

<span data-ttu-id="9b6cd-110">*буттонстате* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9b6cd-110">*buttonState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6cd-111">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9b6cd-111">Type: **boolean**</span></span>

<span data-ttu-id="9b6cd-112">Текущее состояние кнопки.</span><span class="sxs-lookup"><span data-stu-id="9b6cd-112">The current down state of the button.</span></span> <span data-ttu-id="9b6cd-113">Значение **true** означает, что кнопка не работает.</span><span class="sxs-lookup"><span data-stu-id="9b6cd-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b6cd-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b6cd-114">Return value</span></span>

<span data-ttu-id="9b6cd-115">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b6cd-115">Type: **uint32**</span></span>

<span data-ttu-id="9b6cd-116">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="9b6cd-116">A return value of zero indicates success.</span></span> <span data-ttu-id="9b6cd-117">Ненулевое значение указывает на ошибку запроса.</span><span class="sxs-lookup"><span data-stu-id="9b6cd-117">A nonzero value indicates a query failure.</span></span>

<dl> <dt>

<span data-ttu-id="9b6cd-118">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="9b6cd-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9b6cd-119">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="9b6cd-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9b6cd-120">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="9b6cd-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9b6cd-121">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="9b6cd-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9b6cd-122">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="9b6cd-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9b6cd-123">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="9b6cd-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9b6cd-124">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="9b6cd-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9b6cd-125">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="9b6cd-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9b6cd-126">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="9b6cd-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9b6cd-127">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="9b6cd-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9b6cd-128">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="9b6cd-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9b6cd-129">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="9b6cd-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9b6cd-130">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="9b6cd-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="9b6cd-131">Remarks</span><span class="sxs-lookup"><span data-stu-id="9b6cd-131">Remarks</span></span>

<span data-ttu-id="9b6cd-132">Доступ к классу [**\_ Ps2Mouse мсвм**](msvm-ps2mouse.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="9b6cd-132">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9b6cd-133">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9b6cd-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b6cd-134">Требования</span><span class="sxs-lookup"><span data-stu-id="9b6cd-134">Requirements</span></span>



| <span data-ttu-id="9b6cd-135">Требование</span><span class="sxs-lookup"><span data-stu-id="9b6cd-135">Requirement</span></span> | <span data-ttu-id="9b6cd-136">Значение</span><span class="sxs-lookup"><span data-stu-id="9b6cd-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b6cd-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b6cd-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9b6cd-138">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9b6cd-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9b6cd-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b6cd-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9b6cd-140">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9b6cd-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9b6cd-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9b6cd-141">Namespace</span></span><br/>                | <span data-ttu-id="9b6cd-142">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9b6cd-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9b6cd-143">MOF</span><span class="sxs-lookup"><span data-stu-id="9b6cd-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b6cd-144"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b6cd-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b6cd-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9b6cd-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b6cd-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9b6cd-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9b6cd-147">См. также</span><span class="sxs-lookup"><span data-stu-id="9b6cd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b6cd-148">**Мсвм \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="9b6cd-148">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

