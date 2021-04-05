---
description: Задает горизонтальное и вертикальное расположение курсора мыши.
ms.assetid: 7845E10A-7F61-4134-BF81-AED5483F36AD
title: Метод Сетабсолутепоситион класса Msvm_SyntheticMouse (Дбдао. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetAbsolutePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b8ffb3a4d415f76dedf30acba5869b4cc585eb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909507"
---
# <a name="setabsoluteposition-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="dd3da-103">Метод Сетабсолутепоситион \_ класса Синсетикмаусе мсвм</span><span class="sxs-lookup"><span data-stu-id="dd3da-103">SetAbsolutePosition method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="dd3da-104">Задает горизонтальное и вертикальное расположение курсора мыши.</span><span class="sxs-lookup"><span data-stu-id="dd3da-104">Sets the horizontal and vertical position of the mouse cursor.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd3da-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd3da-105">Syntax</span></span>


```mof
uint32 SetAbsolutePosition(
  [in] sint32 horizontalPosition,
  [in] sint32 verticalPosition
);
```



## <a name="parameters"></a><span data-ttu-id="dd3da-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd3da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd3da-107">*хоризонталпоситион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd3da-107">*horizontalPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd3da-108">Тип: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="dd3da-108">Type: **sint32**</span></span>

<span data-ttu-id="dd3da-109">Новое горизонтальное расположение курсора мыши в пикселях.</span><span class="sxs-lookup"><span data-stu-id="dd3da-109">The new horizontal position of the mouse cursor, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="dd3da-110">*вертикалпоситион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd3da-110">*verticalPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd3da-111">Тип: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="dd3da-111">Type: **sint32**</span></span>

<span data-ttu-id="dd3da-112">Новое вертикальное расположение курсора мыши в пикселях.</span><span class="sxs-lookup"><span data-stu-id="dd3da-112">The new vertical position of the mouse cursor, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd3da-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd3da-113">Return value</span></span>

<span data-ttu-id="dd3da-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd3da-114">Type: **uint32**</span></span>

<span data-ttu-id="dd3da-115">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="dd3da-115">A return value of zero indicates success.</span></span> <span data-ttu-id="dd3da-116">Ненулевое значение указывает на ошибку изменения расположения прокрутки.</span><span class="sxs-lookup"><span data-stu-id="dd3da-116">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="dd3da-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="dd3da-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dd3da-118">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="dd3da-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="dd3da-119">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="dd3da-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="dd3da-120">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="dd3da-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="dd3da-121">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="dd3da-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="dd3da-122">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="dd3da-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="dd3da-123">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="dd3da-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="dd3da-124">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="dd3da-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="dd3da-125">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="dd3da-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="dd3da-126">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="dd3da-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="dd3da-127">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="dd3da-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="dd3da-128">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="dd3da-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="dd3da-129">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="dd3da-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="dd3da-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd3da-130">Remarks</span></span>

<span data-ttu-id="dd3da-131">Доступ к классу [**\_ синсетикмаусе мсвм**](msvm-syntheticmouse.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="dd3da-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dd3da-132">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="dd3da-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd3da-133">Требования</span><span class="sxs-lookup"><span data-stu-id="dd3da-133">Requirements</span></span>



| <span data-ttu-id="dd3da-134">Требование</span><span class="sxs-lookup"><span data-stu-id="dd3da-134">Requirement</span></span> | <span data-ttu-id="dd3da-135">Значение</span><span class="sxs-lookup"><span data-stu-id="dd3da-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd3da-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd3da-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dd3da-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dd3da-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dd3da-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd3da-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dd3da-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dd3da-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd3da-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dd3da-140">Namespace</span></span><br/>                | <span data-ttu-id="dd3da-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="dd3da-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dd3da-142">Header</span><span class="sxs-lookup"><span data-stu-id="dd3da-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd3da-143"><dt>Дбдао. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd3da-143"><dt>Dbdao.h</dt></span></span> </dl>                      |
| <span data-ttu-id="dd3da-144">MOF</span><span class="sxs-lookup"><span data-stu-id="dd3da-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd3da-145"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd3da-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd3da-146">DLL</span><span class="sxs-lookup"><span data-stu-id="dd3da-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd3da-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd3da-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dd3da-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd3da-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd3da-149">**Мсвм \_ синсетикмаусе**</span><span class="sxs-lookup"><span data-stu-id="dd3da-149">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

