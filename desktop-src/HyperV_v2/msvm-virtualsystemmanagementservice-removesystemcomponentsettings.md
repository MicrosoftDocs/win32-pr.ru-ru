---
description: Удаляет параметры универсального компонента из конфигурации виртуальной системы.
ms.assetid: 54ddb960-65b7-409d-ad80-f3685562a1a1
title: Метод Ремовесистемкомпонентсеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93ef7b794b901212fad72a1fcdf6223d8344b8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682490"
---
# <a name="removesystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="b6124-103">Метод Ремовесистемкомпонентсеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="b6124-103">RemoveSystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="b6124-104">Удаляет параметры универсального компонента из конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="b6124-104">Removes generic component settings from a virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6124-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6124-105">Syntax</span></span>


```mof
uint32 RemoveSystemComponentSettings(
  [in]  Msvm_SystemComponentSettingData REF ComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b6124-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6124-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6124-107">*Компонентсеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b6124-107">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6124-108">Массив [**мсвм \_ системкомпонентсеттингдата**](msvm-systemcomponentsettingdata.md) , который ссылается на параметры компонента для удаления.</span><span class="sxs-lookup"><span data-stu-id="b6124-108">Array of [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that reference the component settings to remove.</span></span>

</dd> <dt>

<span data-ttu-id="b6124-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b6124-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6124-110">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b6124-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6124-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6124-111">Return value</span></span>

<span data-ttu-id="b6124-112">Возвращает 0 или 4096 при успешном выполнении; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="b6124-112">Returns 0 or 4096 on a success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b6124-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="b6124-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b6124-114">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="b6124-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b6124-115">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="b6124-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b6124-116">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="b6124-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b6124-117">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="b6124-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b6124-118">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="b6124-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b6124-119">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="b6124-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b6124-120">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="b6124-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b6124-121">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="b6124-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="b6124-122">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="b6124-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b6124-123">Требования</span><span class="sxs-lookup"><span data-stu-id="b6124-123">Requirements</span></span>



| <span data-ttu-id="b6124-124">Требование</span><span class="sxs-lookup"><span data-stu-id="b6124-124">Requirement</span></span> | <span data-ttu-id="b6124-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b6124-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6124-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6124-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b6124-127">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="b6124-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b6124-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6124-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b6124-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b6124-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b6124-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b6124-130">Namespace</span></span><br/>                | <span data-ttu-id="b6124-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="b6124-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b6124-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b6124-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6124-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6124-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6124-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b6124-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6124-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b6124-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b6124-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6124-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6124-137">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="b6124-137">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

