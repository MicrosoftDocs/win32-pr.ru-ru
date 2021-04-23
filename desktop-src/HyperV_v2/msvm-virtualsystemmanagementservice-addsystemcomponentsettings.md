---
description: Добавляет универсальные параметры в конфигурацию виртуальной системы.
ms.assetid: ae04be39-0401-43e9-b19b-3539ca1786ec
title: Метод Аддсистемкомпонентсеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56ca8bed752bab52f6a82e18975dd5df72dbe12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682498"
---
# <a name="addsystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="7d735-103">Метод Аддсистемкомпонентсеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="7d735-103">AddSystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="7d735-104">Добавляет универсальные параметры в конфигурацию виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="7d735-104">Adds generic settings to a virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d735-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d735-105">Syntax</span></span>


```mof
uint32 AddSystemComponentSettings(
  [in]  Msvm_VirtualSystemSettingData   REF AffectedConfiguration,
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7d735-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d735-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d735-107">*Аффектедконфигуратион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7d735-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7d735-108">*Компонентсеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7d735-108">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d735-109">Добавляемые параметры компонента.</span><span class="sxs-lookup"><span data-stu-id="7d735-109">The component settings to add.</span></span>

</dd> <dt>

<span data-ttu-id="7d735-110">*Ресултингкомпонентсеттингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7d735-110">*ResultingComponentSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d735-111">В случае успеха ссылается на [**мсвм \_ системкомпонентсеттингдата**](msvm-systemcomponentsettingdata.md) , содержащий результирующие параметры компонента.</span><span class="sxs-lookup"><span data-stu-id="7d735-111">On success, references a [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that contains the resulting component settings.</span></span>

</dd> <dt>

<span data-ttu-id="7d735-112">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7d735-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d735-113">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7d735-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d735-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d735-114">Return value</span></span>

<span data-ttu-id="7d735-115">При успешном выполнении возвращает 0 или 4096; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="7d735-115">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="7d735-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="7d735-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7d735-117">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="7d735-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7d735-118">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="7d735-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7d735-119">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="7d735-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7d735-120">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="7d735-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7d735-121">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="7d735-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7d735-122">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="7d735-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7d735-123">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7d735-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7d735-124">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="7d735-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7d735-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7d735-125">Requirements</span></span>



| <span data-ttu-id="7d735-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7d735-126">Requirement</span></span> | <span data-ttu-id="7d735-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7d735-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d735-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d735-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7d735-129">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="7d735-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7d735-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d735-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7d735-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7d735-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7d735-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7d735-132">Namespace</span></span><br/>                | <span data-ttu-id="7d735-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7d735-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7d735-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7d735-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d735-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d735-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d735-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7d735-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d735-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7d735-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7d735-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d735-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d735-139">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="7d735-139">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

