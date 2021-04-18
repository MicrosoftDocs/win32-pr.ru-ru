---
description: Восстанавливается до последнего работоспособного предохранителя ключа.
ms.assetid: 0d1ea5d8-d25e-400c-be65-afe1bd65b1f0
title: Метод Рестореласткновнгудкэйпротектор класса Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.RestoreLastKnownGoodKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e82fb3b40f4b85e74f92ed2690a411932af2eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684691"
---
# <a name="restorelastknowngoodkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="d8847-103">Метод Рестореласткновнгудкэйпротектор \_ класса SecurityService мсвм</span><span class="sxs-lookup"><span data-stu-id="d8847-103">RestoreLastKnownGoodKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="d8847-104">Восстанавливается до последнего работоспособного предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="d8847-104">Restores back to the last known good key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8847-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8847-105">Syntax</span></span>


```mof
uint32 RestoreLastKnownGoodKeyProtector(
  [in]  string              SecuritySettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d8847-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8847-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8847-107">*Секуритисеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8847-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8847-108">Строка содержит встроенный экземпляр класса [**мсвм \_ секуритисеттингдата**](msvm-securitysettingdata.md) , представляющий параметры безопасности виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="d8847-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="d8847-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d8847-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8847-110">Необязательный параметр для отслеживания хода выполнения операции, который используется, если метод не может быть выполнен синхронно.</span><span class="sxs-lookup"><span data-stu-id="d8847-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="d8847-111">Если операция выполняется асинхронно, возвращается значение 4096.</span><span class="sxs-lookup"><span data-stu-id="d8847-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8847-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8847-112">Return value</span></span>

<span data-ttu-id="d8847-113">При успешном выполнении возвращает 0 или 4096; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d8847-113">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="d8847-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="d8847-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d8847-115">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="d8847-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d8847-116">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="d8847-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d8847-117">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="d8847-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d8847-118">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="d8847-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d8847-119">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="d8847-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d8847-120">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="d8847-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d8847-121">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="d8847-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d8847-122">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="d8847-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d8847-123">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="d8847-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d8847-124">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="d8847-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d8847-125">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="d8847-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d8847-126">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="d8847-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d8847-127">Требования</span><span class="sxs-lookup"><span data-stu-id="d8847-127">Requirements</span></span>



| <span data-ttu-id="d8847-128">Требование</span><span class="sxs-lookup"><span data-stu-id="d8847-128">Requirement</span></span> | <span data-ttu-id="d8847-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d8847-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8847-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8847-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d8847-131">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="d8847-131">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d8847-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8847-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d8847-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d8847-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d8847-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d8847-134">Namespace</span></span><br/>                | <span data-ttu-id="d8847-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d8847-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d8847-136">MOF</span><span class="sxs-lookup"><span data-stu-id="d8847-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8847-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8847-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8847-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d8847-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8847-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d8847-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d8847-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8847-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8847-141">**Мсвм \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="d8847-141">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




