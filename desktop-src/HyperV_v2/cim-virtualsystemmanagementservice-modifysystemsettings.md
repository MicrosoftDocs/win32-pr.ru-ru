---
description: Изменяет параметры виртуальной системы.
ms.assetid: 9c3d28f8-9806-411a-866f-d062c6d31818
title: Метод Модифисистемсеттингс класса CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da610d03e683b06ad743d1b6d4fe413dc5b31d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991591"
---
# <a name="modifysystemsettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="c9aad-103">Метод Модифисистемсеттингс \_ класса CIM виртуалсистемманажементсервице</span><span class="sxs-lookup"><span data-stu-id="c9aad-103">ModifySystemSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="c9aad-104">Изменяет параметры виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="c9aad-104">Modifies virtual system settings.</span></span>

<span data-ttu-id="c9aad-105">При применении к параметрам системы "Текущая" Конфигурация виртуальной системы в качестве побочного результата можно изменить экземпляр виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="c9aad-105">When applied to the system settings of a "current" virtual system configuration, as a side effect the virtual system instance may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9aad-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9aad-106">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c9aad-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9aad-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9aad-108">*SystemSettings* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c9aad-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9aad-109">Строка, содержащая экземпляр класса [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) , который используется для изменения параметров виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="c9aad-109">String containing an instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that is used to modify the settings of the virtual system.</span></span> <span data-ttu-id="c9aad-110">Для указания изменяемого параметра виртуальной системы экземпляр должен иметь допустимый идентификатор **InstanceId** .</span><span class="sxs-lookup"><span data-stu-id="c9aad-110">The instance must have a valid **InstanceID** in order to identify the virtual system setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="c9aad-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c9aad-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9aad-112">Если операция выполняется долго, может быть возвращена также [**\_ конкретежоб CIM**](cim-concretejob.md) , представляющая задание.</span><span class="sxs-lookup"><span data-stu-id="c9aad-112">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9aad-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9aad-113">Return value</span></span>

<span data-ttu-id="c9aad-114">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c9aad-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="c9aad-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="c9aad-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c9aad-116">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="c9aad-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c9aad-117">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="c9aad-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c9aad-118">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="c9aad-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c9aad-119">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="c9aad-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c9aad-120">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="c9aad-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c9aad-121">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="c9aad-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c9aad-122">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="c9aad-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c9aad-123">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="c9aad-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c9aad-124">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="c9aad-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="c9aad-125">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="c9aad-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c9aad-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c9aad-126">Requirements</span></span>



| <span data-ttu-id="c9aad-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c9aad-127">Requirement</span></span> | <span data-ttu-id="c9aad-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c9aad-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9aad-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9aad-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c9aad-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c9aad-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c9aad-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9aad-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c9aad-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c9aad-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c9aad-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c9aad-133">Namespace</span></span><br/>                | <span data-ttu-id="c9aad-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c9aad-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c9aad-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c9aad-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9aad-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9aad-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9aad-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c9aad-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9aad-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c9aad-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c9aad-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9aad-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9aad-140">**\_ВИРТУАЛСИСТЕММАНАЖЕМЕНТСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="c9aad-140">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




