---
description: Имитирует нажатие кнопки указанного устройства.
ms.assetid: 77CFA2E9-E422-464C-B124-6F7D3D56BA4C
title: Метод Кликкбуттон класса Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.ClickButton
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ffaded2a5e9a8e4e37a158e3aa91b27520dff2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683242"
---
# <a name="clickbutton-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="c729d-103">Метод Кликкбуттон \_ класса Ps2Mouse мсвм</span><span class="sxs-lookup"><span data-stu-id="c729d-103">ClickButton method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="c729d-104">Имитирует нажатие кнопки указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="c729d-104">Simulates a click of the specified device button.</span></span> <span data-ttu-id="c729d-105">Это эквивалентно вызову [**сетбуттонстате**](setbuttonstate-msvm-syntheticmouse.md) дважды, сначала нажмите кнопку и снова, чтобы освободить ее.</span><span class="sxs-lookup"><span data-stu-id="c729d-105">This is equivalent to calling [**SetButtonState**](setbuttonstate-msvm-syntheticmouse.md) twice, first to press the button, and again to release it.</span></span>

## <a name="syntax"></a><span data-ttu-id="c729d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c729d-106">Syntax</span></span>


```mof
uint32 ClickButton(
  [in] uint32 buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="c729d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c729d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c729d-108">*буттониндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c729d-108">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c729d-109">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c729d-109">Type: **uint32**</span></span>

<span data-ttu-id="c729d-110">Отсчитываемый от 1 индекс кнопки.</span><span class="sxs-lookup"><span data-stu-id="c729d-110">The 1-based index of the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c729d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c729d-111">Return value</span></span>

<span data-ttu-id="c729d-112">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c729d-112">Type: **uint32**</span></span>

<span data-ttu-id="c729d-113">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="c729d-113">A return value of zero indicates success.</span></span> <span data-ttu-id="c729d-114">Ненулевое значение указывает на ошибку при изменении состояния кнопки.</span><span class="sxs-lookup"><span data-stu-id="c729d-114">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="c729d-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="c729d-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c729d-116">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="c729d-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c729d-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="c729d-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c729d-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="c729d-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c729d-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="c729d-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c729d-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="c729d-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c729d-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="c729d-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c729d-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="c729d-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c729d-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="c729d-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c729d-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="c729d-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c729d-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="c729d-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c729d-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="c729d-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c729d-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="c729d-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="c729d-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c729d-128">Remarks</span></span>

<span data-ttu-id="c729d-129">Доступ к классу [**\_ Ps2Mouse мсвм**](msvm-ps2mouse.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="c729d-129">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c729d-130">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c729d-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c729d-131">Требования</span><span class="sxs-lookup"><span data-stu-id="c729d-131">Requirements</span></span>



| <span data-ttu-id="c729d-132">Требование</span><span class="sxs-lookup"><span data-stu-id="c729d-132">Requirement</span></span> | <span data-ttu-id="c729d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="c729d-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c729d-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c729d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c729d-135">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c729d-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c729d-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c729d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c729d-137">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c729d-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c729d-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c729d-138">Namespace</span></span><br/>                | <span data-ttu-id="c729d-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c729d-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c729d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c729d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c729d-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c729d-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c729d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c729d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c729d-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c729d-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c729d-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c729d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c729d-145">**Мсвм \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="c729d-145">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

