---
description: Имитирует последовательность ключей с помощью кодов сканирования.
ms.assetid: F67D2FBA-3CE0-4135-9043-FAB59381DE3C
title: Метод Типесканкодес класса Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeScancodes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 97479a1a0926894f72472b7459f77cd9325ac6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810420"
---
# <a name="typescancodes-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="f0771-103">Метод Типесканкодес \_ класса клавиатуры мсвм</span><span class="sxs-lookup"><span data-stu-id="f0771-103">TypeScancodes method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="f0771-104">Имитирует последовательность ключей с помощью кодов сканирования.</span><span class="sxs-lookup"><span data-stu-id="f0771-104">Simulates a key sequence using scan codes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0771-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0771-105">Syntax</span></span>


```mof
uint32 TypeScancodes(
  [in] uint8 Scancodes[]
);
```



## <a name="parameters"></a><span data-ttu-id="f0771-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0771-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0771-107">*Сканкодес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f0771-107">*Scancodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0771-108">Тип: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="f0771-108">Type: **uint8\[\]**</span></span>

<span data-ttu-id="f0771-109">Массив, содержащий коды проверки для ввода.</span><span class="sxs-lookup"><span data-stu-id="f0771-109">An array that contains the scan codes to type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0771-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0771-110">Return value</span></span>

<span data-ttu-id="f0771-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0771-111">Type: **uint32**</span></span>

<span data-ttu-id="f0771-112">Этот метод возвращает 0, если он завершается.</span><span class="sxs-lookup"><span data-stu-id="f0771-112">This method returns 0 if it succeeds.</span></span> <span data-ttu-id="f0771-113">Любое другое возвращаемое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="f0771-113">Any other return value indicates an error.</span></span> <span data-ttu-id="f0771-114">Возвращаемое значение может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f0771-114">The return value can be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f0771-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="f0771-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f0771-116">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="f0771-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f0771-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="f0771-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f0771-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="f0771-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f0771-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="f0771-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f0771-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="f0771-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f0771-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="f0771-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f0771-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="f0771-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f0771-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="f0771-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f0771-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="f0771-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f0771-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="f0771-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f0771-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="f0771-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f0771-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="f0771-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f0771-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f0771-128">Remarks</span></span>

<span data-ttu-id="f0771-129">Доступ к классу [**\_ клавиатуры мсвм**](msvm-keyboard.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="f0771-129">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f0771-130">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f0771-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0771-131">Требования</span><span class="sxs-lookup"><span data-stu-id="f0771-131">Requirements</span></span>



| <span data-ttu-id="f0771-132">Требование</span><span class="sxs-lookup"><span data-stu-id="f0771-132">Requirement</span></span> | <span data-ttu-id="f0771-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f0771-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0771-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0771-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f0771-135">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f0771-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f0771-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0771-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f0771-137">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f0771-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0771-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f0771-138">Namespace</span></span><br/>                | <span data-ttu-id="f0771-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f0771-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f0771-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f0771-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0771-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0771-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0771-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f0771-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0771-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f0771-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f0771-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0771-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0771-145">**Мсвм \_ клавиатура**</span><span class="sxs-lookup"><span data-stu-id="f0771-145">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

