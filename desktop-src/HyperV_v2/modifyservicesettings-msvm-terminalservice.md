---
description: Метод Модифисервицесеттингс класса Msvm_TerminalService — изменяет данные настройки для службы.
ms.assetid: 76669180-fa95-4d6e-b89a-53e45da664c4
title: Метод Модифисервицесеттингс класса Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 930b29c5c07c755b493a0aabad88ae776c0803e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119332"
---
# <a name="modifyservicesettings-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="4a8f4-103">Метод Модифисервицесеттингс \_ класса Терминалсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="4a8f4-103">ModifyServiceSettings method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="4a8f4-104">Изменяет данные настройки для службы.</span><span class="sxs-lookup"><span data-stu-id="4a8f4-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a8f4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a8f4-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              ServiceSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4a8f4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a8f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a8f4-107">*Сервицесеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4a8f4-107">*ServiceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a8f4-108">Строковое представление класса [**мсвм \_ терминалсервицесеттингдата**](msvm-terminalservicesettingdata.md) , содержащего измененные данные настройки для службы.</span><span class="sxs-lookup"><span data-stu-id="4a8f4-108">A string representation of the [**Msvm\_TerminalServiceSettingData**](msvm-terminalservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="4a8f4-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4a8f4-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a8f4-110">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4a8f4-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a8f4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a8f4-111">Return value</span></span>

<span data-ttu-id="4a8f4-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4a8f4-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4a8f4-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="4a8f4-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4a8f4-114">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="4a8f4-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4a8f4-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="4a8f4-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4a8f4-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="4a8f4-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4a8f4-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="4a8f4-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4a8f4-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="4a8f4-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4a8f4-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="4a8f4-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4a8f4-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="4a8f4-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4a8f4-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="4a8f4-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4a8f4-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="4a8f4-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4a8f4-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="4a8f4-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4a8f4-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="4a8f4-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4a8f4-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="4a8f4-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4a8f4-126">Требования</span><span class="sxs-lookup"><span data-stu-id="4a8f4-126">Requirements</span></span>



| <span data-ttu-id="4a8f4-127">Требование</span><span class="sxs-lookup"><span data-stu-id="4a8f4-127">Requirement</span></span> | <span data-ttu-id="4a8f4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="4a8f4-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a8f4-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a8f4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4a8f4-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4a8f4-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4a8f4-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a8f4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4a8f4-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4a8f4-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4a8f4-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4a8f4-133">Namespace</span></span><br/>                | <span data-ttu-id="4a8f4-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4a8f4-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4a8f4-135">MOF</span><span class="sxs-lookup"><span data-stu-id="4a8f4-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a8f4-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a8f4-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a8f4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4a8f4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a8f4-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4a8f4-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4a8f4-139">См. также</span><span class="sxs-lookup"><span data-stu-id="4a8f4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a8f4-140">**Мсвм \_ терминалсервице**</span><span class="sxs-lookup"><span data-stu-id="4a8f4-140">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

