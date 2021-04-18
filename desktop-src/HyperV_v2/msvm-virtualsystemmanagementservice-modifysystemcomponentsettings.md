---
description: Изменяет общие параметры системных компонентов.
ms.assetid: e745be32-c26a-4343-99c8-950788243adf
title: Метод Модифисистемкомпонентсеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9495256d1b7610bebdac1fb2cc8b70960a63304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682496"
---
# <a name="modifysystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="9218a-103">Метод Модифисистемкомпонентсеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="9218a-103">ModifySystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="9218a-104">Изменяет общие параметры системных компонентов.</span><span class="sxs-lookup"><span data-stu-id="9218a-104">Modifies generic system component settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="9218a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9218a-105">Syntax</span></span>


```mof
uint32 ModifySystemComponentSettings(
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9218a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9218a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9218a-107">*Компонентсеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9218a-107">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9218a-108">Массив параметров компонента для обновления.</span><span class="sxs-lookup"><span data-stu-id="9218a-108">An array of component settings to update.</span></span>

</dd> <dt>

<span data-ttu-id="9218a-109">*Ресултингкомпонентсеттингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9218a-109">*ResultingComponentSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9218a-110">При успешном выполнении возвращает массив [**мсвм \_ системкомпонентсеттингдата**](msvm-systemcomponentsettingdata.md) , ссылающийся на результирующие параметры компонента.</span><span class="sxs-lookup"><span data-stu-id="9218a-110">On success, returns an array of [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that reference the resulting component settings.</span></span>

</dd> <dt>

<span data-ttu-id="9218a-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9218a-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9218a-112">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9218a-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9218a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9218a-113">Return value</span></span>

<span data-ttu-id="9218a-114">При успешном выполнении возвращает 0 или 4096; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="9218a-114">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="9218a-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="9218a-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9218a-116">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="9218a-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9218a-117">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="9218a-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9218a-118">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="9218a-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9218a-119">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="9218a-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9218a-120">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="9218a-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9218a-121">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="9218a-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9218a-122">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="9218a-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9218a-123">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="9218a-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9218a-124">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="9218a-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="9218a-125">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="9218a-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9218a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="9218a-126">Requirements</span></span>



| <span data-ttu-id="9218a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="9218a-127">Requirement</span></span> | <span data-ttu-id="9218a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="9218a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9218a-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9218a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9218a-130">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="9218a-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9218a-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9218a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9218a-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9218a-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9218a-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9218a-133">Namespace</span></span><br/>                | <span data-ttu-id="9218a-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9218a-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9218a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="9218a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9218a-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9218a-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9218a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9218a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9218a-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9218a-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9218a-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9218a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9218a-140">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="9218a-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

