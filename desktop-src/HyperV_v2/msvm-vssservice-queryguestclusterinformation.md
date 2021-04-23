---
description: Запрос сведений о кластере от узла Hyper-V к гостевой системе.
ms.assetid: 28983984-a2af-4eab-8b1f-2f7d6a3d70ea
title: Метод Куеригуестклустеринформатион класса Msvm_VssService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService.QueryGuestClusterInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 36f88441729cc1e6e36bcad9ca84b46049bce2a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540263"
---
# <a name="queryguestclusterinformation-method-of-the-msvm_vssservice-class"></a><span data-ttu-id="12da7-103">Метод Куеригуестклустеринформатион \_ класса Всссервице мсвм</span><span class="sxs-lookup"><span data-stu-id="12da7-103">QueryGuestClusterInformation method of the Msvm\_VssService class</span></span>

<span data-ttu-id="12da7-104">Запрос сведений о кластере от узла Hyper-V к гостевой системе.</span><span class="sxs-lookup"><span data-stu-id="12da7-104">Querying cluster information from the Hyper-V host to the guest.</span></span>

## <a name="syntax"></a><span data-ttu-id="12da7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12da7-105">Syntax</span></span>


```mof
uint32 QueryGuestClusterInformation(
  [out] Msvm_GuestClusterInformation GuestClusterInformation
);
```



## <a name="parameters"></a><span data-ttu-id="12da7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="12da7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12da7-107">*Гуестклустеринформатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="12da7-107">*GuestClusterInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12da7-108">При успешном выполнении содержит [**мсвм \_ гуестклустеринформатион**](msvm-guestclusterinformation.md) , описывающий гостевой кластер.</span><span class="sxs-lookup"><span data-stu-id="12da7-108">On success, contains an [**Msvm\_GuestClusterInformation**](msvm-guestclusterinformation.md) that describes the guest cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12da7-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12da7-109">Return value</span></span>

<span data-ttu-id="12da7-110">При успешном выполнении возвращает значение 0 (завершено без ошибок) или 4096 (задание запущено); в противном случае возвратите ошибку.</span><span class="sxs-lookup"><span data-stu-id="12da7-110">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="12da7-111">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="12da7-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="12da7-112">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="12da7-112">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="12da7-113">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="12da7-113">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="12da7-114">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="12da7-114">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="12da7-115">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="12da7-115">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="12da7-116">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="12da7-116">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="12da7-117">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="12da7-117">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="12da7-118">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="12da7-118">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="12da7-119">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="12da7-119">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="12da7-120">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="12da7-120">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="12da7-121">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="12da7-121">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="12da7-122">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="12da7-122">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="12da7-123">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="12da7-123">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="12da7-124">Требования</span><span class="sxs-lookup"><span data-stu-id="12da7-124">Requirements</span></span>



| <span data-ttu-id="12da7-125">Требование</span><span class="sxs-lookup"><span data-stu-id="12da7-125">Requirement</span></span> | <span data-ttu-id="12da7-126">Значение</span><span class="sxs-lookup"><span data-stu-id="12da7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12da7-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12da7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="12da7-128">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="12da7-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="12da7-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12da7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="12da7-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="12da7-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="12da7-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="12da7-131">Namespace</span></span><br/>                | <span data-ttu-id="12da7-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="12da7-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="12da7-133">MOF</span><span class="sxs-lookup"><span data-stu-id="12da7-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12da7-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12da7-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="12da7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="12da7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12da7-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="12da7-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="12da7-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12da7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12da7-138">**Мсвм \_ всссервице**</span><span class="sxs-lookup"><span data-stu-id="12da7-138">**Msvm\_VssService**</span></span>](msvm-vssservice.md)
</dt> </dl>

 

 




