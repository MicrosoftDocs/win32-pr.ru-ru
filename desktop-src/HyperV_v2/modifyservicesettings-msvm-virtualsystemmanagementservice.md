---
description: Изменяет данные настройки для службы.
ms.assetid: 1CA49922-894D-4AA1-B741-6A0DC9F5654E
title: Метод Модифисервицесеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e93d86c454de4f214c72a6ed95a414d184419c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911676"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="e4d76-103">Метод Модифисервицесеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="e4d76-103">ModifyServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="e4d76-104">Изменяет данные настройки для службы.</span><span class="sxs-lookup"><span data-stu-id="e4d76-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4d76-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4d76-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e4d76-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4d76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4d76-107">*SettingData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e4d76-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d76-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="e4d76-108">Type: **string**</span></span>

<span data-ttu-id="e4d76-109">Встроенный экземпляр класса [**мсвм \_ виртуалсистемманажементсервицесеттингдата**](msvm-virtualsystemmanagementservicesettingdata.md) , который содержит измененные аспекты существующей службы.</span><span class="sxs-lookup"><span data-stu-id="e4d76-109">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the modified aspects of the existing service.</span></span>

</dd> <dt>

<span data-ttu-id="e4d76-110">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e4d76-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d76-111">Тип: **[ **CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="e4d76-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="e4d76-112">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4d76-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4d76-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4d76-113">Return value</span></span>

<span data-ttu-id="e4d76-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4d76-114">Type: **uint32**</span></span>

<span data-ttu-id="e4d76-115">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e4d76-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e4d76-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="e4d76-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e4d76-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="e4d76-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e4d76-118">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="e4d76-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e4d76-119">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="e4d76-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e4d76-120">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="e4d76-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e4d76-121">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="e4d76-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e4d76-122">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="e4d76-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e4d76-123">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="e4d76-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e4d76-124">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="e4d76-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e4d76-125">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="e4d76-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e4d76-126">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="e4d76-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e4d76-127">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="e4d76-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e4d76-128">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="e4d76-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e4d76-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4d76-129">Remarks</span></span>

<span data-ttu-id="e4d76-130">Доступ к классу [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="e4d76-130">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e4d76-131">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e4d76-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4d76-132">Требования</span><span class="sxs-lookup"><span data-stu-id="e4d76-132">Requirements</span></span>



| <span data-ttu-id="e4d76-133">Требование</span><span class="sxs-lookup"><span data-stu-id="e4d76-133">Requirement</span></span> | <span data-ttu-id="e4d76-134">Значение</span><span class="sxs-lookup"><span data-stu-id="e4d76-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4d76-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4d76-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e4d76-136">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e4d76-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e4d76-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4d76-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e4d76-138">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e4d76-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e4d76-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e4d76-139">Namespace</span></span><br/>                | <span data-ttu-id="e4d76-140">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e4d76-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e4d76-141">MOF</span><span class="sxs-lookup"><span data-stu-id="e4d76-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4d76-142"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4d76-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4d76-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e4d76-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4d76-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e4d76-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e4d76-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4d76-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4d76-146">**Модифисервицесеттингс (v1)**</span><span class="sxs-lookup"><span data-stu-id="e4d76-146">**ModifyServiceSettings (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyservicesettings-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="e4d76-147">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="e4d76-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="e4d76-148">[**\_КОНКРЕТЕЖОБ CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e4d76-148">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> </dl>

 

