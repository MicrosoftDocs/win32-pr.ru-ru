---
description: Извлекает дополнительные сведения об ошибке.
ms.assetid: 64a90f18-3ae7-4021-857f-64adf8c40430
title: Метод Жетеррорекс класса Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c056f7c8a05d8d06d136219fb55699ed5e146bc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664683"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="60759-103">Метод Жетеррорекс \_ класса Коллектионреференцепоинтекспортжоб мсвм</span><span class="sxs-lookup"><span data-stu-id="60759-103">GetErrorEx method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="60759-104">Извлекает дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="60759-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="60759-105">При выполнении или завершении задания без ошибок **жетеррорекс** не возвращает экземпляр [**\_ ошибки мсвм**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="60759-105">When the job is executing or has terminated without error, **GetErrorEx** returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="60759-106">Однако если задание завершилось сбоем из-за внутренней проблемы или из-за завершения задания клиентом, **жетеррорекс** возвращает один или несколько экземпляров **\_ ошибок мсвм** .</span><span class="sxs-lookup"><span data-stu-id="60759-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more **Msvm\_Error** instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="60759-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60759-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="60759-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="60759-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60759-109">*Ошибки* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="60759-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60759-110">Если оперативное состояние задания не равно "ОК", этот параметр возвращает массив экземпляров [**\_ ошибок мсвм**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="60759-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="60759-111">В противном случае, если задано "ОК", этот параметр содержит **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="60759-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60759-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60759-112">Return value</span></span>

<span data-ttu-id="60759-113">При успешном выполнении возвращает 0; в противном случае возвращает одно из следующих значений ошибки:</span><span class="sxs-lookup"><span data-stu-id="60759-113">On success, returns 0; otherwise, returns one of the following error values:</span></span>

<dl> <dt>

<span data-ttu-id="60759-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="60759-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="60759-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="60759-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="60759-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="60759-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="60759-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="60759-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="60759-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="60759-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="60759-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="60759-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="60759-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="60759-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="60759-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="60759-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="60759-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="60759-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="60759-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="60759-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="60759-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="60759-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="60759-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="60759-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="60759-126">Требования</span><span class="sxs-lookup"><span data-stu-id="60759-126">Requirements</span></span>



| <span data-ttu-id="60759-127">Требование</span><span class="sxs-lookup"><span data-stu-id="60759-127">Requirement</span></span> | <span data-ttu-id="60759-128">Значение</span><span class="sxs-lookup"><span data-stu-id="60759-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60759-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60759-129">Minimum supported client</span></span><br/> | <span data-ttu-id="60759-130">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="60759-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="60759-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60759-131">Minimum supported server</span></span><br/> | <span data-ttu-id="60759-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="60759-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="60759-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="60759-133">Namespace</span></span><br/>                | <span data-ttu-id="60759-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="60759-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="60759-135">MOF</span><span class="sxs-lookup"><span data-stu-id="60759-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60759-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60759-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="60759-137">DLL</span><span class="sxs-lookup"><span data-stu-id="60759-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60759-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60759-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="60759-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60759-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60759-140">**Мсвм \_ коллектионреференцепоинтекспортжоб**</span><span class="sxs-lookup"><span data-stu-id="60759-140">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




