---
description: Имитирует основной выпуск.
ms.assetid: EAE84BD5-ECEA-44E7-A7AB-CD18299DF2FE
title: Метод Релеасекэй класса Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.ReleaseKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2193a4b78128ff3f65e98b4425528a51f6cf5916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546826"
---
# <a name="releasekey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="4f7d6-103">Метод Релеасекэй \_ класса клавиатуры мсвм</span><span class="sxs-lookup"><span data-stu-id="4f7d6-103">ReleaseKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="4f7d6-104">Имитирует основной выпуск.</span><span class="sxs-lookup"><span data-stu-id="4f7d6-104">Simulates a key release.</span></span> <span data-ttu-id="4f7d6-105">При успешном выполнении ключ будет находиться в состоянии up.</span><span class="sxs-lookup"><span data-stu-id="4f7d6-105">When successful, the key will be in the up state.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f7d6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f7d6-106">Syntax</span></span>


```mof
uint32 ReleaseKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="4f7d6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f7d6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f7d6-108">*keyCode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4f7d6-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f7d6-109">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f7d6-109">Type: **uint32**</span></span>

<span data-ttu-id="4f7d6-110">Виртуальный код ключа для выпуска.</span><span class="sxs-lookup"><span data-stu-id="4f7d6-110">The virtual key code of the key to release.</span></span> <span data-ttu-id="4f7d6-111">Список кодов виртуальных клавиш см. в разделе [**коды виртуальных**](../inputdev/virtual-key-codes.md)клавиш.</span><span class="sxs-lookup"><span data-stu-id="4f7d6-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f7d6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f7d6-112">Return value</span></span>

<span data-ttu-id="4f7d6-113">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f7d6-113">Type: **uint32**</span></span>

<span data-ttu-id="4f7d6-114">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="4f7d6-114">A return value of zero indicates success.</span></span> <span data-ttu-id="4f7d6-115">Ненулевое значение указывает на ошибку при изменении состояния ключа.</span><span class="sxs-lookup"><span data-stu-id="4f7d6-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="4f7d6-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="4f7d6-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4f7d6-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="4f7d6-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4f7d6-118">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="4f7d6-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4f7d6-119">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="4f7d6-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4f7d6-120">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="4f7d6-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4f7d6-121">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="4f7d6-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4f7d6-122">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="4f7d6-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4f7d6-123">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="4f7d6-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4f7d6-124">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="4f7d6-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4f7d6-125">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="4f7d6-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4f7d6-126">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="4f7d6-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4f7d6-127">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="4f7d6-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4f7d6-128">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="4f7d6-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="4f7d6-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f7d6-129">Remarks</span></span>

<span data-ttu-id="4f7d6-130">Метод **релеасекэй** сопоставляет ссылки на **\_ меню VK** (18), **VK \_ Control** (17) и **VK \_ SHIFT** (16) с **VK \_ лмену** (164), **VK \_ Лконтрол** (162) и **VK \_ лшифт** (160), соответственно, так как **\_ меню VK**, **VK \_ Control** и **VK \_ SHIFT** , не являются реальными ключами на клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="4f7d6-130">The **ReleaseKey** method maps references to the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, because the **VK\_MENU**, **VK\_CONTROL**, and **VK\_SHIFT** virtual key codes do not represent real keys on a keyboard.</span></span>

<span data-ttu-id="4f7d6-131">Доступ к классу [**\_ клавиатуры мсвм**](msvm-keyboard.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="4f7d6-131">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4f7d6-132">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4f7d6-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f7d6-133">Требования</span><span class="sxs-lookup"><span data-stu-id="4f7d6-133">Requirements</span></span>



| <span data-ttu-id="4f7d6-134">Требование</span><span class="sxs-lookup"><span data-stu-id="4f7d6-134">Requirement</span></span> | <span data-ttu-id="4f7d6-135">Значение</span><span class="sxs-lookup"><span data-stu-id="4f7d6-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f7d6-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f7d6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4f7d6-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4f7d6-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4f7d6-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f7d6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4f7d6-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4f7d6-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f7d6-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4f7d6-140">Namespace</span></span><br/>                | <span data-ttu-id="4f7d6-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4f7d6-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4f7d6-142">MOF</span><span class="sxs-lookup"><span data-stu-id="4f7d6-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f7d6-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f7d6-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f7d6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4f7d6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f7d6-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4f7d6-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4f7d6-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f7d6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f7d6-147">**Мсвм \_ клавиатура**</span><span class="sxs-lookup"><span data-stu-id="4f7d6-147">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="4f7d6-148">**Коды виртуальных клавиш**</span><span class="sxs-lookup"><span data-stu-id="4f7d6-148">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

