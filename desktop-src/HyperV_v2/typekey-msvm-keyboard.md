---
description: Имитирует последовательность клавиш для пресс-релизов.
ms.assetid: 4166BA71-315D-41BD-857C-48AFB702911E
title: Метод Типекэй класса Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1b978da48600cc52472ab8bdec011ddbaa5ff624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999332"
---
# <a name="typekey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="d82af-103">Метод Типекэй \_ класса клавиатуры мсвм</span><span class="sxs-lookup"><span data-stu-id="d82af-103">TypeKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="d82af-104">Имитирует последовательность клавиш для пресс-релизов.</span><span class="sxs-lookup"><span data-stu-id="d82af-104">Simulates a press-release key sequence.</span></span> <span data-ttu-id="d82af-105">Это эквивалентно вызову [**пресскэй**](presskey-msvm-keyboard.md) , за которым следует [**релеасекэй**](releasekey-msvm-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="d82af-105">This is equivalent to calling [**PressKey**](presskey-msvm-keyboard.md) followed by [**ReleaseKey**](releasekey-msvm-keyboard.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d82af-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d82af-106">Syntax</span></span>


```mof
uint32 TypeKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="d82af-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d82af-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d82af-108">*keyCode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d82af-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d82af-109">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d82af-109">Type: **uint32**</span></span>

<span data-ttu-id="d82af-110">Код виртуального ключа для нажатия клавиши.</span><span class="sxs-lookup"><span data-stu-id="d82af-110">The virtual key code of the key to press.</span></span> <span data-ttu-id="d82af-111">Список кодов виртуальных клавиш см. в разделе [**коды виртуальных**](../inputdev/virtual-key-codes.md)клавиш.</span><span class="sxs-lookup"><span data-stu-id="d82af-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d82af-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d82af-112">Return value</span></span>

<span data-ttu-id="d82af-113">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d82af-113">Type: **uint32**</span></span>

<span data-ttu-id="d82af-114">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="d82af-114">A return value of zero indicates success.</span></span> <span data-ttu-id="d82af-115">Ненулевое значение указывает на ошибку при изменении состояния ключа.</span><span class="sxs-lookup"><span data-stu-id="d82af-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="d82af-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="d82af-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d82af-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="d82af-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d82af-118">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="d82af-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d82af-119">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="d82af-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d82af-120">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="d82af-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d82af-121">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="d82af-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d82af-122">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="d82af-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d82af-123">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="d82af-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d82af-124">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="d82af-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d82af-125">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="d82af-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d82af-126">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="d82af-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d82af-127">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="d82af-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d82af-128">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="d82af-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d82af-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d82af-129">Remarks</span></span>

<span data-ttu-id="d82af-130">Доступ к классу [**\_ клавиатуры мсвм**](msvm-keyboard.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="d82af-130">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d82af-131">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d82af-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d82af-132">Требования</span><span class="sxs-lookup"><span data-stu-id="d82af-132">Requirements</span></span>



| <span data-ttu-id="d82af-133">Требование</span><span class="sxs-lookup"><span data-stu-id="d82af-133">Requirement</span></span> | <span data-ttu-id="d82af-134">Значение</span><span class="sxs-lookup"><span data-stu-id="d82af-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d82af-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d82af-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d82af-136">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d82af-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d82af-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d82af-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d82af-138">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d82af-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d82af-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d82af-139">Namespace</span></span><br/>                | <span data-ttu-id="d82af-140">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d82af-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d82af-141">MOF</span><span class="sxs-lookup"><span data-stu-id="d82af-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d82af-142"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d82af-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d82af-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d82af-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d82af-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d82af-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d82af-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d82af-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d82af-146">**Мсвм \_ клавиатура**</span><span class="sxs-lookup"><span data-stu-id="d82af-146">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="d82af-147">**Коды виртуальных клавиш**</span><span class="sxs-lookup"><span data-stu-id="d82af-147">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

