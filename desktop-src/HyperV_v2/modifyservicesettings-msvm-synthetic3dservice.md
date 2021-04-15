---
description: Изменяет данные параметра для искусственной трехмерной службы.
ms.assetid: 951ba829-2821-4621-800f-4e1a967b41f5
title: Метод Модифисервицесеттингс класса Msvm_Synthetic3DService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 76f6fe18dea67231c9d722352df516bf97c35ac0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497919"
---
# <a name="modifyservicesettings-method-of-the-msvm_synthetic3dservice-class"></a><span data-ttu-id="e2ca3-103">Метод Модифисервицесеттингс \_ класса Synthetic3DService мсвм</span><span class="sxs-lookup"><span data-stu-id="e2ca3-103">ModifyServiceSettings method of the Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="e2ca3-104">Изменяет данные параметра для искусственной трехмерной службы.</span><span class="sxs-lookup"><span data-stu-id="e2ca3-104">Modifies the setting data for the synthetic 3-D service.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2ca3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2ca3-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e2ca3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2ca3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2ca3-107">*SettingData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2ca3-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ca3-108">Строковое представление класса [**мсвм \_ Synthetic3DServiceSettingData**](msvm-synthetic3dservicesettingdata.md) , содержащего измененные данные настройки для службы.</span><span class="sxs-lookup"><span data-stu-id="e2ca3-108">A string representation of the [**Msvm\_Synthetic3DServiceSettingData**](msvm-synthetic3dservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="e2ca3-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e2ca3-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ca3-110">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2ca3-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2ca3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2ca3-111">Return value</span></span>

<span data-ttu-id="e2ca3-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e2ca3-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e2ca3-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="e2ca3-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e2ca3-114">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="e2ca3-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e2ca3-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="e2ca3-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e2ca3-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="e2ca3-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e2ca3-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="e2ca3-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e2ca3-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="e2ca3-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e2ca3-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="e2ca3-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e2ca3-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="e2ca3-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e2ca3-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="e2ca3-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e2ca3-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="e2ca3-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e2ca3-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="e2ca3-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e2ca3-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="e2ca3-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e2ca3-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="e2ca3-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e2ca3-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e2ca3-126">Requirements</span></span>



| <span data-ttu-id="e2ca3-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e2ca3-127">Requirement</span></span> | <span data-ttu-id="e2ca3-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e2ca3-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2ca3-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2ca3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e2ca3-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e2ca3-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e2ca3-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2ca3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e2ca3-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e2ca3-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e2ca3-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e2ca3-133">Namespace</span></span><br/>                | <span data-ttu-id="e2ca3-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e2ca3-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e2ca3-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e2ca3-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2ca3-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2ca3-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2ca3-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e2ca3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2ca3-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e2ca3-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e2ca3-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2ca3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2ca3-140">**Мсвм \_ Synthetic3DService**</span><span class="sxs-lookup"><span data-stu-id="e2ca3-140">**Msvm\_Synthetic3DService**</span></span>](msvm-synthetic3dservice.md)
</dt> </dl>

 

