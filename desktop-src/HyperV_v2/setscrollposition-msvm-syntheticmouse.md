---
description: Задает z-координату элемента управления "колесо" для указывающего устройства.
ms.assetid: 02349957-6BAA-42E7-B3D4-F39E748615E6
title: Метод Сетскроллпоситион класса Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetScrollPosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6d82ad2cd75b41ca914d0db49d5de4709790ea6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156723"
---
# <a name="setscrollposition-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="efc04-103">Метод Сетскроллпоситион \_ класса Синсетикмаусе мсвм</span><span class="sxs-lookup"><span data-stu-id="efc04-103">SetScrollPosition method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="efc04-104">Задает z-координату элемента управления "колесо" для указывающего устройства.</span><span class="sxs-lookup"><span data-stu-id="efc04-104">Sets the z-coordinate of the wheel control of the pointing device.</span></span> <span data-ttu-id="efc04-105">Значения, записанные в это свойство, всегда являются относительными смещениями координат.</span><span class="sxs-lookup"><span data-stu-id="efc04-105">Values written to this property are always relative coordinate offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="efc04-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efc04-106">Syntax</span></span>


```mof
uint32 SetScrollPosition(
  [in] sint32 scrollPositionDelta
);
```



## <a name="parameters"></a><span data-ttu-id="efc04-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="efc04-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efc04-108">*скроллпоситионделта* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="efc04-108">*scrollPositionDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efc04-109">Тип: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="efc04-109">Type: **sint32**</span></span>

<span data-ttu-id="efc04-110">Разность в положении прокрутки.</span><span class="sxs-lookup"><span data-stu-id="efc04-110">The delta of the scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efc04-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efc04-111">Return value</span></span>

<span data-ttu-id="efc04-112">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efc04-112">Type: **uint32**</span></span>

<span data-ttu-id="efc04-113">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="efc04-113">A return value of zero indicates success.</span></span> <span data-ttu-id="efc04-114">Ненулевое значение указывает на ошибку изменения расположения прокрутки.</span><span class="sxs-lookup"><span data-stu-id="efc04-114">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="efc04-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="efc04-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="efc04-116">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="efc04-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="efc04-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="efc04-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="efc04-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="efc04-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="efc04-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="efc04-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="efc04-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="efc04-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="efc04-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="efc04-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="efc04-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="efc04-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="efc04-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="efc04-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="efc04-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="efc04-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="efc04-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="efc04-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="efc04-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="efc04-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="efc04-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="efc04-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="efc04-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="efc04-128">Remarks</span></span>

<span data-ttu-id="efc04-129">Доступ к классу [**\_ синсетикмаусе мсвм**](msvm-syntheticmouse.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="efc04-129">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="efc04-130">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="efc04-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="efc04-131">Требования</span><span class="sxs-lookup"><span data-stu-id="efc04-131">Requirements</span></span>



| <span data-ttu-id="efc04-132">Требование</span><span class="sxs-lookup"><span data-stu-id="efc04-132">Requirement</span></span> | <span data-ttu-id="efc04-133">Значение</span><span class="sxs-lookup"><span data-stu-id="efc04-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efc04-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="efc04-134">Minimum supported client</span></span><br/> | <span data-ttu-id="efc04-135">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="efc04-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="efc04-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="efc04-136">Minimum supported server</span></span><br/> | <span data-ttu-id="efc04-137">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="efc04-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="efc04-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="efc04-138">Namespace</span></span><br/>                | <span data-ttu-id="efc04-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="efc04-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="efc04-140">MOF</span><span class="sxs-lookup"><span data-stu-id="efc04-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efc04-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="efc04-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="efc04-142">DLL</span><span class="sxs-lookup"><span data-stu-id="efc04-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efc04-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="efc04-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="efc04-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efc04-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efc04-145">**Мсвм \_ синсетикмаусе**</span><span class="sxs-lookup"><span data-stu-id="efc04-145">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

