---
description: Сдвигает указатель мыши на заданную горизонтальную и вертикальную разности.
ms.assetid: C74E4BEA-C7E1-44C7-B4FC-8926F23DF1FE
title: Метод Сетрелативепоситион класса Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetRelativePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b7f4d10f48bce4b33cd4965f08633b85b5a738bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663723"
---
# <a name="setrelativeposition-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="473c1-103">Метод Сетрелативепоситион \_ класса Ps2Mouse мсвм</span><span class="sxs-lookup"><span data-stu-id="473c1-103">SetRelativePosition method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="473c1-104">Сдвигает указатель мыши на заданную горизонтальную и вертикальную разности.</span><span class="sxs-lookup"><span data-stu-id="473c1-104">Offsets the position of the mouse pointer by the specified horizontal and vertical deltas.</span></span>

## <a name="syntax"></a><span data-ttu-id="473c1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="473c1-105">Syntax</span></span>


```mof
uint32 SetRelativePosition(
  [in] sint8 horizontalDelta,
  [in] sint8 verticalDelta
);
```



## <a name="parameters"></a><span data-ttu-id="473c1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="473c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="473c1-107">*хоризонталделта* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="473c1-107">*horizontalDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="473c1-108">Тип: **sint8**</span><span class="sxs-lookup"><span data-stu-id="473c1-108">Type: **sint8**</span></span>

<span data-ttu-id="473c1-109">Горизонтальное изменение расположения мыши в пикселях.</span><span class="sxs-lookup"><span data-stu-id="473c1-109">The horizontal change for the mouse position, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="473c1-110">*вертикалделта* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="473c1-110">*verticalDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="473c1-111">Тип: **sint8**</span><span class="sxs-lookup"><span data-stu-id="473c1-111">Type: **sint8**</span></span>

<span data-ttu-id="473c1-112">Вертикальное изменение расположения мыши в пикселях.</span><span class="sxs-lookup"><span data-stu-id="473c1-112">The vertical change for the mouse position, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="473c1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="473c1-113">Return value</span></span>

<span data-ttu-id="473c1-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="473c1-114">Type: **uint32**</span></span>

<span data-ttu-id="473c1-115">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="473c1-115">A return value of zero indicates success.</span></span> <span data-ttu-id="473c1-116">Ненулевое значение указывает на ошибку изменения расположения мыши.</span><span class="sxs-lookup"><span data-stu-id="473c1-116">A nonzero value indicates a failure to alter the mouse position.</span></span>

<dl> <dt>

<span data-ttu-id="473c1-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="473c1-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="473c1-118">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="473c1-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="473c1-119">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="473c1-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="473c1-120">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="473c1-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="473c1-121">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="473c1-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="473c1-122">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="473c1-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="473c1-123">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="473c1-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="473c1-124">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="473c1-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="473c1-125">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="473c1-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="473c1-126">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="473c1-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="473c1-127">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="473c1-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="473c1-128">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="473c1-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="473c1-129">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="473c1-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="473c1-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="473c1-130">Remarks</span></span>

<span data-ttu-id="473c1-131">Доступ к классу [**\_ Ps2Mouse мсвм**](msvm-ps2mouse.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="473c1-131">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="473c1-132">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="473c1-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="473c1-133">Требования</span><span class="sxs-lookup"><span data-stu-id="473c1-133">Requirements</span></span>



| <span data-ttu-id="473c1-134">Требование</span><span class="sxs-lookup"><span data-stu-id="473c1-134">Requirement</span></span> | <span data-ttu-id="473c1-135">Значение</span><span class="sxs-lookup"><span data-stu-id="473c1-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="473c1-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="473c1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="473c1-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="473c1-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="473c1-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="473c1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="473c1-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="473c1-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="473c1-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="473c1-140">Namespace</span></span><br/>                | <span data-ttu-id="473c1-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="473c1-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="473c1-142">MOF</span><span class="sxs-lookup"><span data-stu-id="473c1-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="473c1-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="473c1-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="473c1-144">DLL</span><span class="sxs-lookup"><span data-stu-id="473c1-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="473c1-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="473c1-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="473c1-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="473c1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="473c1-147">**Мсвм \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="473c1-147">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

