---
description: Извлекает ошибку.
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
ms.openlocfilehash: a7d8ff9c2c01bb21343b4859e2db2dbed7ad643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911015"
---
# <a name="geterror-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="acf19-103">Метод method \_ класса мсвм сторажежоб</span><span class="sxs-lookup"><span data-stu-id="acf19-103">GetError method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="acf19-104">Извлекает ошибку.</span><span class="sxs-lookup"><span data-stu-id="acf19-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="acf19-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acf19-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="acf19-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="acf19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acf19-107">*Ошибка при* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="acf19-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acf19-108">Полученная ошибка.</span><span class="sxs-lookup"><span data-stu-id="acf19-108">The retrieved error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acf19-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="acf19-109">Return value</span></span>

<span data-ttu-id="acf19-110">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="acf19-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="acf19-111">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="acf19-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="acf19-112">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="acf19-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="acf19-113">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="acf19-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="acf19-114">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="acf19-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="acf19-115">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="acf19-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="acf19-116">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="acf19-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="acf19-117">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="acf19-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="acf19-118">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="acf19-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="acf19-119">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="acf19-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="acf19-120">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="acf19-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="acf19-121">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="acf19-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="acf19-122">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="acf19-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="acf19-123">Требования</span><span class="sxs-lookup"><span data-stu-id="acf19-123">Requirements</span></span>



| <span data-ttu-id="acf19-124">Требование</span><span class="sxs-lookup"><span data-stu-id="acf19-124">Requirement</span></span> | <span data-ttu-id="acf19-125">Значение</span><span class="sxs-lookup"><span data-stu-id="acf19-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acf19-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="acf19-126">Minimum supported client</span></span><br/> | <span data-ttu-id="acf19-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="acf19-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="acf19-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="acf19-128">Minimum supported server</span></span><br/> | <span data-ttu-id="acf19-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="acf19-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="acf19-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="acf19-130">Namespace</span></span><br/>                | <span data-ttu-id="acf19-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="acf19-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="acf19-132">MOF</span><span class="sxs-lookup"><span data-stu-id="acf19-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="acf19-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="acf19-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="acf19-134">DLL</span><span class="sxs-lookup"><span data-stu-id="acf19-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acf19-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="acf19-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="acf19-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="acf19-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acf19-137">**Мсвм \_ сторажежоб**</span><span class="sxs-lookup"><span data-stu-id="acf19-137">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

 




