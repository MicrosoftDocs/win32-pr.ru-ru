---
description: Метод РемовеассоЦиатеддата класса Msvm_VirtualSystemReferencePointService — удаляет журнал данных, связанный с точкой ссылки.
ms.assetid: b6206bda-c195-4c6f-9b80-508c20b53ce5
title: Метод РемовеассоЦиатеддата класса Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b5291e4e018edc89909ccde36ce0e420698af8e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118622"
---
# <a name="removeassociateddata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="3002c-103">Метод РемовеассоЦиатеддата \_ класса Виртуалсистемреференцепоинтсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="3002c-103">RemoveAssociatedData method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="3002c-104">Удаляет журнал данных, связанный с точкой ссылки.</span><span class="sxs-lookup"><span data-stu-id="3002c-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="3002c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3002c-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3002c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3002c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3002c-107">*Аффектедреференцепоинт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3002c-107">*AffectedReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3002c-108">Ссылка на экземпляр [**\_ виртуалсистемреференцепоинт мсвм**](msvm-virtualsystemreferencepoint.md) , представляющий удаляемую точку ссылки.</span><span class="sxs-lookup"><span data-stu-id="3002c-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="3002c-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3002c-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3002c-110">Необязательный параметр для отслеживания хода выполнения операции, который используется, если метод не может быть выполнен синхронно.</span><span class="sxs-lookup"><span data-stu-id="3002c-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="3002c-111">Если операция выполняется асинхронно, возвращается значение 4096.</span><span class="sxs-lookup"><span data-stu-id="3002c-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3002c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3002c-112">Return value</span></span>

<span data-ttu-id="3002c-113">При успешном выполнении возвращает значение 0 (завершено без ошибок) или 4096 (задание запущено); в противном случае возвратите ошибку.</span><span class="sxs-lookup"><span data-stu-id="3002c-113">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="3002c-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="3002c-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3002c-115">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="3002c-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3002c-116">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="3002c-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3002c-117">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="3002c-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3002c-118">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="3002c-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3002c-119">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="3002c-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3002c-120">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="3002c-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3002c-121">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="3002c-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3002c-122">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="3002c-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3002c-123">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="3002c-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3002c-124">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="3002c-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3002c-125">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="3002c-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3002c-126">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="3002c-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3002c-127">Требования</span><span class="sxs-lookup"><span data-stu-id="3002c-127">Requirements</span></span>



| <span data-ttu-id="3002c-128">Требование</span><span class="sxs-lookup"><span data-stu-id="3002c-128">Requirement</span></span> | <span data-ttu-id="3002c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="3002c-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3002c-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3002c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3002c-131">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3002c-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3002c-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3002c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3002c-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3002c-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3002c-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3002c-134">Namespace</span></span><br/>                | <span data-ttu-id="3002c-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3002c-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3002c-136">MOF</span><span class="sxs-lookup"><span data-stu-id="3002c-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3002c-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3002c-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3002c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3002c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3002c-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3002c-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3002c-140">См. также</span><span class="sxs-lookup"><span data-stu-id="3002c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3002c-141">**Мсвм \_ виртуалсистемреференцепоинтсервице**</span><span class="sxs-lookup"><span data-stu-id="3002c-141">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




