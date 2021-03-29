---
description: Извлекает текущий список управления доступом на уровне пользователей (DACL), который управляет доступом к интерактивному сеансу виртуальной машины.
ms.assetid: 9b81f6d5-20fa-4277-b943-756d85359fd2
title: Метод Жетинтерактивесессионакл класса Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GetInteractiveSessionACL
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f08c8514a2f65a08b4b9350b38988da8e49b4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810325"
---
# <a name="getinteractivesessionacl-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="61a53-103">Метод Жетинтерактивесессионакл \_ класса Терминалсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="61a53-103">GetInteractiveSessionACL method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="61a53-104">Извлекает текущий *список управления доступом на уровне пользователей* (DACL), который управляет доступом к интерактивному сеансу виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="61a53-104">Retrieves the current *discretionary access control list* (DACL) that controls access to the interactive session of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="61a53-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61a53-105">Syntax</span></span>


```mof
uint32 GetInteractiveSessionACL(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 AccessControlList[]
);
```



## <a name="parameters"></a><span data-ttu-id="61a53-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="61a53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61a53-107">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="61a53-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61a53-108">Ссылка на экземпляр класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , представляющий виртуальную машину, для которой будет извлечен список DACL.</span><span class="sxs-lookup"><span data-stu-id="61a53-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine whose DACL will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="61a53-109">*Акцессконтроллист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="61a53-109">*AccessControlList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61a53-110">Массив строк, каждый из которых содержит встроенный экземпляр класса [**мсвм \_ интерактивесессионаце**](msvm-interactivesessionace.md) , представляющий *запись управления доступом* (ACE) в списке DACL интерактивного сеанса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="61a53-110">An array of strings, each containing an embedded instance of the [**Msvm\_InteractiveSessionACE**](msvm-interactivesessionace.md) class that represents an *access control entry* (ACE) in the virtual machine interactive session DACL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61a53-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="61a53-111">Return value</span></span>

<span data-ttu-id="61a53-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="61a53-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="61a53-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="61a53-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="61a53-114">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="61a53-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="61a53-115">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="61a53-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="61a53-116">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="61a53-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="61a53-117">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="61a53-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="61a53-118">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="61a53-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="61a53-119">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="61a53-119">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="61a53-120">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="61a53-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="61a53-121">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="61a53-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="61a53-122">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="61a53-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="61a53-123">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="61a53-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="61a53-124">Требования</span><span class="sxs-lookup"><span data-stu-id="61a53-124">Requirements</span></span>



| <span data-ttu-id="61a53-125">Требование</span><span class="sxs-lookup"><span data-stu-id="61a53-125">Requirement</span></span> | <span data-ttu-id="61a53-126">Значение</span><span class="sxs-lookup"><span data-stu-id="61a53-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61a53-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61a53-127">Minimum supported client</span></span><br/> | <span data-ttu-id="61a53-128">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="61a53-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="61a53-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61a53-129">Minimum supported server</span></span><br/> | <span data-ttu-id="61a53-130">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="61a53-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61a53-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="61a53-131">Namespace</span></span><br/>                | <span data-ttu-id="61a53-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="61a53-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="61a53-133">MOF</span><span class="sxs-lookup"><span data-stu-id="61a53-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61a53-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61a53-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61a53-135">DLL</span><span class="sxs-lookup"><span data-stu-id="61a53-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61a53-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61a53-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61a53-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61a53-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61a53-138">**Мсвм \_ терминалсервице**</span><span class="sxs-lookup"><span data-stu-id="61a53-138">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

 




