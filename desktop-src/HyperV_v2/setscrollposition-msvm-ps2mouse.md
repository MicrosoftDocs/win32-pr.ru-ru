---
description: Настраивает z-координату элемента управления "колесо" для указывающего устройства.
ms.assetid: FF1929EE-4A2D-4761-8919-488369FAEE1F
title: Метод Сетскроллпоситион класса Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetScrollPosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ffec8e05acf2210c55038edde5def8373e900ed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911000"
---
# <a name="setscrollposition-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="ba489-103">Метод Сетскроллпоситион \_ класса Ps2Mouse мсвм</span><span class="sxs-lookup"><span data-stu-id="ba489-103">SetScrollPosition method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="ba489-104">Настраивает z-координату элемента управления "колесо" для указывающего устройства.</span><span class="sxs-lookup"><span data-stu-id="ba489-104">Adjusts the z-coordinate of the wheel control of the pointing device.</span></span> <span data-ttu-id="ba489-105">Значения, записанные в это свойство, всегда являются относительными смещениями координат.</span><span class="sxs-lookup"><span data-stu-id="ba489-105">Values written to this property are always relative coordinate offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba489-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba489-106">Syntax</span></span>


```mof
uint32 SetScrollPosition(
  [in] sint8 scrollPositionDelta
);
```



## <a name="parameters"></a><span data-ttu-id="ba489-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba489-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba489-108">*скроллпоситионделта* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ba489-108">*scrollPositionDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba489-109">Тип: **sint8**</span><span class="sxs-lookup"><span data-stu-id="ba489-109">Type: **sint8**</span></span>

<span data-ttu-id="ba489-110">Разность в положении прокрутки.</span><span class="sxs-lookup"><span data-stu-id="ba489-110">The delta of the scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba489-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba489-111">Return value</span></span>

<span data-ttu-id="ba489-112">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba489-112">Type: **uint32**</span></span>

<span data-ttu-id="ba489-113">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="ba489-113">A return value of zero indicates success.</span></span> <span data-ttu-id="ba489-114">Ненулевое значение указывает на ошибку изменения расположения прокрутки.</span><span class="sxs-lookup"><span data-stu-id="ba489-114">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="ba489-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="ba489-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ba489-116">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="ba489-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ba489-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="ba489-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ba489-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="ba489-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ba489-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="ba489-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ba489-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="ba489-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ba489-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="ba489-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ba489-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="ba489-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ba489-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="ba489-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ba489-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="ba489-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ba489-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="ba489-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ba489-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="ba489-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ba489-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="ba489-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ba489-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba489-128">Remarks</span></span>

<span data-ttu-id="ba489-129">Доступ к классу [**\_ Ps2Mouse мсвм**](msvm-ps2mouse.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="ba489-129">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ba489-130">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ba489-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba489-131">Требования</span><span class="sxs-lookup"><span data-stu-id="ba489-131">Requirements</span></span>



| <span data-ttu-id="ba489-132">Требование</span><span class="sxs-lookup"><span data-stu-id="ba489-132">Requirement</span></span> | <span data-ttu-id="ba489-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ba489-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba489-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba489-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ba489-135">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ba489-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ba489-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba489-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ba489-137">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ba489-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ba489-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ba489-138">Namespace</span></span><br/>                | <span data-ttu-id="ba489-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ba489-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ba489-140">MOF</span><span class="sxs-lookup"><span data-stu-id="ba489-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba489-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba489-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba489-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ba489-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba489-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ba489-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ba489-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba489-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba489-145">**Мсвм \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="ba489-145">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

