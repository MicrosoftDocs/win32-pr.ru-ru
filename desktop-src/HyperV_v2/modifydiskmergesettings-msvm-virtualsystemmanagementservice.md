---
description: Изменяет данные параметров слияния диска.
ms.assetid: 91775dc5-105a-4e38-a334-fb34dd4e59f8
title: Метод Модифидискмержесеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyDiskMergeSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe737c084b4c1c76a411ce1d2eba513554b40f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683691"
---
# <a name="modifydiskmergesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="887f8-103">Метод Модифидискмержесеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="887f8-103">ModifyDiskMergeSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="887f8-104">Изменяет данные параметров слияния диска.</span><span class="sxs-lookup"><span data-stu-id="887f8-104">Modifies the disk merge setting data.</span></span>

## <a name="syntax"></a><span data-ttu-id="887f8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="887f8-105">Syntax</span></span>


```mof
uint32 ModifyDiskMergeSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="887f8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="887f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="887f8-107">*SettingData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="887f8-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="887f8-108">Встроенный экземпляр класса [**мсвм \_ дискмержесеттингдата**](msvm-diskmergesettingdata.md) , который содержит измененные данные параметров для функции слияния диска.</span><span class="sxs-lookup"><span data-stu-id="887f8-108">An embedded instance of the [**Msvm\_DiskMergeSettingData**](msvm-diskmergesettingdata.md) class that contains modified setting data for the disk merge function.</span></span>

</dd> <dt>

<span data-ttu-id="887f8-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="887f8-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="887f8-110">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="887f8-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="887f8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="887f8-111">Return value</span></span>

<span data-ttu-id="887f8-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="887f8-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="887f8-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="887f8-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="887f8-114">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="887f8-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="887f8-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="887f8-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="887f8-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="887f8-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="887f8-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="887f8-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="887f8-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="887f8-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="887f8-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="887f8-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="887f8-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="887f8-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="887f8-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="887f8-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="887f8-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="887f8-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="887f8-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="887f8-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="887f8-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="887f8-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="887f8-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="887f8-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="887f8-126">Требования</span><span class="sxs-lookup"><span data-stu-id="887f8-126">Requirements</span></span>



| <span data-ttu-id="887f8-127">Требование</span><span class="sxs-lookup"><span data-stu-id="887f8-127">Requirement</span></span> | <span data-ttu-id="887f8-128">Значение</span><span class="sxs-lookup"><span data-stu-id="887f8-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="887f8-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="887f8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="887f8-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="887f8-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="887f8-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="887f8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="887f8-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="887f8-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="887f8-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="887f8-133">Namespace</span></span><br/>                | <span data-ttu-id="887f8-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="887f8-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="887f8-135">MOF</span><span class="sxs-lookup"><span data-stu-id="887f8-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="887f8-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="887f8-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="887f8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="887f8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="887f8-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="887f8-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="887f8-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="887f8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="887f8-140">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="887f8-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

