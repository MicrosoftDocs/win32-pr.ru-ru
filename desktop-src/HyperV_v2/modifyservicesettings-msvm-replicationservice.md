---
description: Изменяет параметры службы реплики Hyper-V.
ms.assetid: e203f9f5-da4b-4ba7-8637-add7169990d3
title: Метод Модифисервицесеттингс класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe20f8e6f113dce05961eb11fbafdc7841f39e38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810312"
---
# <a name="modifyservicesettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="ef7bd-103">Метод Модифисервицесеттингс \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="ef7bd-103">ModifyServiceSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="ef7bd-104">Изменяет параметры службы реплики Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-104">Modifies the settings for the Hyper-V Replica service.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef7bd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef7bd-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ef7bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef7bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef7bd-107">*SettingData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef7bd-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef7bd-108">Строковое представление класса [**мсвм \_ репликатионсервицесеттингдата**](msvm-replicationservicesettingdata.md) , содержащего измененные данные настройки для службы.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-108">A string representation of the [**Msvm\_ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="ef7bd-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ef7bd-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef7bd-110">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ef7bd-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef7bd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef7bd-111">Return value</span></span>

<span data-ttu-id="ef7bd-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ef7bd-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ef7bd-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="ef7bd-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ef7bd-114">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="ef7bd-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ef7bd-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="ef7bd-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ef7bd-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="ef7bd-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ef7bd-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="ef7bd-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ef7bd-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="ef7bd-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ef7bd-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="ef7bd-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ef7bd-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="ef7bd-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ef7bd-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="ef7bd-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ef7bd-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="ef7bd-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ef7bd-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="ef7bd-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ef7bd-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="ef7bd-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ef7bd-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="ef7bd-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ef7bd-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ef7bd-126">Requirements</span></span>



| <span data-ttu-id="ef7bd-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ef7bd-127">Requirement</span></span> | <span data-ttu-id="ef7bd-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ef7bd-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef7bd-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef7bd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ef7bd-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ef7bd-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ef7bd-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef7bd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ef7bd-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ef7bd-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ef7bd-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ef7bd-133">Namespace</span></span><br/>                | <span data-ttu-id="ef7bd-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ef7bd-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ef7bd-135">MOF</span><span class="sxs-lookup"><span data-stu-id="ef7bd-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef7bd-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef7bd-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef7bd-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ef7bd-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef7bd-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef7bd-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ef7bd-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef7bd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef7bd-140">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="ef7bd-140">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

