---
description: Имитирует сочетание клавиш Ctrl + Alt + Del.
ms.assetid: C24C9C42-844F-4560-B8C1-0054F5E913D6
title: Метод Типектрлалтдел класса Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeCtrlAltDel
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 64ebc4bddf8adccd7098cafed1df43d1cf1cb4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348172"
---
# <a name="typectrlaltdel-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="e94d7-103">Метод Типектрлалтдел \_ класса клавиатуры мсвм</span><span class="sxs-lookup"><span data-stu-id="e94d7-103">TypeCtrlAltDel method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="e94d7-104">Имитирует сочетание клавиш Ctrl + Alt + Del.</span><span class="sxs-lookup"><span data-stu-id="e94d7-104">Simulates a Ctrl+Alt+Del key sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="e94d7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e94d7-105">Syntax</span></span>


```mof
uint32 TypeCtrlAltDel();
```



## <a name="parameters"></a><span data-ttu-id="e94d7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e94d7-106">Parameters</span></span>

<span data-ttu-id="e94d7-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e94d7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e94d7-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e94d7-108">Return value</span></span>

<span data-ttu-id="e94d7-109">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e94d7-109">Type: **uint32**</span></span>

<span data-ttu-id="e94d7-110">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="e94d7-110">A return value of zero indicates success.</span></span> <span data-ttu-id="e94d7-111">Ненулевое значение указывает на ошибку отправки.</span><span class="sxs-lookup"><span data-stu-id="e94d7-111">A nonzero value indicates a failure to send.</span></span>

<dl> <dt>

<span data-ttu-id="e94d7-112">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="e94d7-112">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e94d7-113">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="e94d7-113">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e94d7-114">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="e94d7-114">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e94d7-115">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="e94d7-115">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e94d7-116">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="e94d7-116">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e94d7-117">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="e94d7-117">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e94d7-118">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="e94d7-118">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e94d7-119">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="e94d7-119">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e94d7-120">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="e94d7-120">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e94d7-121">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="e94d7-121">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e94d7-122">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="e94d7-122">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e94d7-123">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="e94d7-123">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e94d7-124">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="e94d7-124">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e94d7-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e94d7-125">Remarks</span></span>

<span data-ttu-id="e94d7-126">Доступ к классу [**\_ клавиатуры мсвм**](msvm-keyboard.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="e94d7-126">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e94d7-127">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e94d7-127">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e94d7-128">Требования</span><span class="sxs-lookup"><span data-stu-id="e94d7-128">Requirements</span></span>



| <span data-ttu-id="e94d7-129">Требование</span><span class="sxs-lookup"><span data-stu-id="e94d7-129">Requirement</span></span> | <span data-ttu-id="e94d7-130">Значение</span><span class="sxs-lookup"><span data-stu-id="e94d7-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e94d7-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e94d7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e94d7-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e94d7-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e94d7-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e94d7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e94d7-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e94d7-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e94d7-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e94d7-135">Namespace</span></span><br/>                | <span data-ttu-id="e94d7-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e94d7-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e94d7-137">MOF</span><span class="sxs-lookup"><span data-stu-id="e94d7-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e94d7-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e94d7-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e94d7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e94d7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e94d7-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e94d7-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e94d7-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e94d7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e94d7-142">**Мсвм \_ клавиатура**</span><span class="sxs-lookup"><span data-stu-id="e94d7-142">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

