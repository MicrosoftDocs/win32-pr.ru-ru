---
description: Метод Жетеррорекс класса Msvm_VirtualSystemReferencePointExportJob — получение дополнительных сведений об ошибке.
ms.assetid: 63ce4762-e5ce-405f-b5fc-74e505b0eaf1
title: Метод Жетеррорекс класса Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80e0850018b20497dbc42bbdbb802ffe4317489b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118612"
---
# <a name="geterrorex-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="f7f51-103">Метод Жетеррорекс \_ класса Виртуалсистемреференцепоинтекспортжоб мсвм</span><span class="sxs-lookup"><span data-stu-id="f7f51-103">GetErrorEx method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="f7f51-104">Извлекает дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="f7f51-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="f7f51-105">При выполнении или завершении задания без ошибок **жетеррорекс** не возвращает экземпляр **жетеррорекс** .</span><span class="sxs-lookup"><span data-stu-id="f7f51-105">When the job is executing or has terminated without error, **GetErrorEx** returns no **GetErrorEx** instance.</span></span> <span data-ttu-id="f7f51-106">Однако если задание завершилось сбоем из-за внутренней проблемы или из-за завершения задания клиентом, **жетеррорекс** возвращает один или несколько экземпляров [**\_ ошибок мсвм**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="f7f51-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more [**Msvm\_Error**](msvm-error.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7f51-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7f51-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="f7f51-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7f51-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7f51-109">*Ошибки* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f7f51-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7f51-110">Если оперативное состояние задания не равно "ОК", этот параметр возвращает массив экземпляров [**\_ ошибок мсвм**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="f7f51-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="f7f51-111">В противном случае, если задано "ОК", этот параметр содержит **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f7f51-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7f51-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7f51-112">Return value</span></span>

<span data-ttu-id="f7f51-113">При успешном выполнении возвращает 0; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f7f51-113">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f7f51-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="f7f51-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f7f51-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="f7f51-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f7f51-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="f7f51-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f7f51-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="f7f51-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f7f51-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="f7f51-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f7f51-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="f7f51-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f7f51-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="f7f51-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f7f51-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="f7f51-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f7f51-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="f7f51-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f7f51-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="f7f51-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f7f51-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="f7f51-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f7f51-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="f7f51-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f7f51-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f7f51-126">Requirements</span></span>



| <span data-ttu-id="f7f51-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f7f51-127">Requirement</span></span> | <span data-ttu-id="f7f51-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f7f51-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f51-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7f51-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f7f51-130">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="f7f51-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f7f51-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7f51-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f7f51-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f7f51-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f7f51-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f7f51-133">Namespace</span></span><br/>                | <span data-ttu-id="f7f51-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f7f51-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f7f51-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f7f51-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7f51-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7f51-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7f51-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f7f51-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7f51-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f7f51-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f7f51-139">См. также</span><span class="sxs-lookup"><span data-stu-id="f7f51-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7f51-140">**Мсвм \_ виртуалсистемреференцепоинтекспортжоб**</span><span class="sxs-lookup"><span data-stu-id="f7f51-140">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




