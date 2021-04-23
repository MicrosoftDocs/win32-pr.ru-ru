---
description: Получает состояние ключа для ключа.
ms.assetid: 4AEB732D-274E-42BB-AA97-9E4D30B81338
title: Метод с нажатием клавиши класса Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.IsKeyPressed
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 44af7a3dc82c0d4d20a2e4c6aff21f7a47837490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263610"
---
# <a name="iskeypressed-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="fa222-103">Метод с нажатием клавиши для \_ класса мсвм Keyboard</span><span class="sxs-lookup"><span data-stu-id="fa222-103">IsKeyPressed method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="fa222-104">Получает состояние ключа для ключа.</span><span class="sxs-lookup"><span data-stu-id="fa222-104">Retrieves the key state of a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa222-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa222-105">Syntax</span></span>


```mof
uint32 IsKeyPressed(
  [in]  uint32  keyCode,
  [out] boolean keyState
);
```



## <a name="parameters"></a><span data-ttu-id="fa222-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa222-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa222-107">*keyCode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa222-107">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa222-108">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fa222-108">Type: **uint32**</span></span>

<span data-ttu-id="fa222-109">Виртуальный код ключа для запроса.</span><span class="sxs-lookup"><span data-stu-id="fa222-109">The virtual key code of the key to query.</span></span> <span data-ttu-id="fa222-110">Список кодов виртуальных клавиш см. в разделе [**коды виртуальных**](../inputdev/virtual-key-codes.md)клавиш.</span><span class="sxs-lookup"><span data-stu-id="fa222-110">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa222-111">*кэйстате* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fa222-111">*keyState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa222-112">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fa222-112">Type: **boolean**</span></span>

<span data-ttu-id="fa222-113">Текущее состояние нажатия клавиши.</span><span class="sxs-lookup"><span data-stu-id="fa222-113">The current down state of the key.</span></span> <span data-ttu-id="fa222-114">Значение **true** означает, что ключ не работает.</span><span class="sxs-lookup"><span data-stu-id="fa222-114">A **True** value means the key is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa222-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa222-115">Return value</span></span>

<span data-ttu-id="fa222-116">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fa222-116">Type: **uint32**</span></span>

<span data-ttu-id="fa222-117">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="fa222-117">A return value of zero indicates success.</span></span> <span data-ttu-id="fa222-118">Ненулевое значение указывает на ошибку при запросе состояния ключа.</span><span class="sxs-lookup"><span data-stu-id="fa222-118">A nonzero value indicates a failure to query the key state.</span></span>

<dl> <dt>

<span data-ttu-id="fa222-119">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="fa222-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fa222-120">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="fa222-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fa222-121">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="fa222-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fa222-122">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="fa222-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fa222-123">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="fa222-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fa222-124">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="fa222-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fa222-125">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="fa222-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fa222-126">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="fa222-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fa222-127">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="fa222-127">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fa222-128">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="fa222-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fa222-129">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="fa222-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fa222-130">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="fa222-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fa222-131">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="fa222-131">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="fa222-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa222-132">Remarks</span></span>

<span data-ttu-id="fa222-133">Метод с **нажатием клавиши** всегда будет возвращать **значение false** для **\_ меню VK** (18), **VK \_ Control** (17) и **VK \_ SHIFT** (16), так как они не являются реальными клавишами на клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="fa222-133">The **IsKeyPressed** method will always return **False** for the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) because these are not real keys on a keyboard.</span></span> <span data-ttu-id="fa222-134">Эти виртуальные коды ключей всегда сопоставлены **с VK \_ лмену** (164), **VK \_ Лконтрол** (162) и **VK \_ лшифт** (160) соответственно методам [**пресскэй**](presskey-msvm-keyboard.md) и [**релеасекэй**](releasekey-msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="fa222-134">These virtual key codes are always mapped to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, by the [**PressKey**](presskey-msvm-keyboard.md) and [**ReleaseKey**](releasekey-msvm-keyboard.md) methods.</span></span>

<span data-ttu-id="fa222-135">Доступ к классу [**\_ клавиатуры мсвм**](msvm-keyboard.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="fa222-135">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="fa222-136">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="fa222-136">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa222-137">Требования</span><span class="sxs-lookup"><span data-stu-id="fa222-137">Requirements</span></span>



| <span data-ttu-id="fa222-138">Требование</span><span class="sxs-lookup"><span data-stu-id="fa222-138">Requirement</span></span> | <span data-ttu-id="fa222-139">Значение</span><span class="sxs-lookup"><span data-stu-id="fa222-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa222-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa222-140">Minimum supported client</span></span><br/> | <span data-ttu-id="fa222-141">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fa222-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fa222-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa222-142">Minimum supported server</span></span><br/> | <span data-ttu-id="fa222-143">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fa222-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fa222-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fa222-144">Namespace</span></span><br/>                | <span data-ttu-id="fa222-145">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="fa222-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fa222-146">MOF</span><span class="sxs-lookup"><span data-stu-id="fa222-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa222-147"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa222-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa222-148">DLL</span><span class="sxs-lookup"><span data-stu-id="fa222-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa222-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fa222-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fa222-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa222-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa222-151">**Мсвм \_ клавиатура**</span><span class="sxs-lookup"><span data-stu-id="fa222-151">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="fa222-152">**Коды виртуальных клавиш**</span><span class="sxs-lookup"><span data-stu-id="fa222-152">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

