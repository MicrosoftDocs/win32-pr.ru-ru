---
description: Метод-Error класса Msvm_StorageJob — извлекает ошибку.
ms.assetid: 785b83c4-06f4-46b5-81f7-35c6fce16c92
title: Метод method класса Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 00434ef529b7f26755f52833ff6f37310c7dc210
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109602"
---
# <a name="geterror-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="6664d-103">Метод method \_ класса мсвм сторажежоб</span><span class="sxs-lookup"><span data-stu-id="6664d-103">GetError method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="6664d-104">Извлекает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6664d-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="6664d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6664d-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="6664d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6664d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6664d-107">*Ошибка при* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6664d-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6664d-108">Полученная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6664d-108">The retrieved error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6664d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6664d-109">Return value</span></span>

<span data-ttu-id="6664d-110">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="6664d-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="6664d-111">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="6664d-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6664d-112">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="6664d-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6664d-113">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="6664d-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6664d-114">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="6664d-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6664d-115">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="6664d-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6664d-116">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="6664d-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6664d-117">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="6664d-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6664d-118">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="6664d-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6664d-119">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="6664d-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6664d-120">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="6664d-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6664d-121">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="6664d-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6664d-122">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="6664d-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6664d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="6664d-123">Requirements</span></span>



| <span data-ttu-id="6664d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="6664d-124">Requirement</span></span> | <span data-ttu-id="6664d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6664d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6664d-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6664d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6664d-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6664d-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6664d-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6664d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6664d-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6664d-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6664d-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6664d-130">Namespace</span></span><br/>                | <span data-ttu-id="6664d-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6664d-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6664d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="6664d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6664d-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6664d-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6664d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6664d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6664d-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6664d-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6664d-136">См. также</span><span class="sxs-lookup"><span data-stu-id="6664d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6664d-137">**Мсвм \_ сторажежоб**</span><span class="sxs-lookup"><span data-stu-id="6664d-137">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

 




