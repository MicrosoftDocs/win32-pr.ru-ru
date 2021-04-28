---
description: Метод-Error класса Msvm_VirtualSystemReferencePointExportJob — извлекает ошибку.
ms.assetid: a30cb74a-4e41-4981-b355-6f46b4b75ce6
title: Метод method класса Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1311e4e56b6396266ece72277e8ddadcdb9d835
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109342"
---
# <a name="geterror-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="45505-103">Метод method \_ класса мсвм виртуалсистемреференцепоинтекспортжоб</span><span class="sxs-lookup"><span data-stu-id="45505-103">GetError method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="45505-104">Извлекает ошибку.</span><span class="sxs-lookup"><span data-stu-id="45505-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="45505-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45505-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="45505-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="45505-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45505-107">*Ошибка при* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="45505-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45505-108">Полученная ошибка.</span><span class="sxs-lookup"><span data-stu-id="45505-108">The error retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45505-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45505-109">Return value</span></span>

<span data-ttu-id="45505-110">При успешном выполнении возвращает 0; в противном случае содержит ошибку.</span><span class="sxs-lookup"><span data-stu-id="45505-110">On success, returns a 0; otherwise, contains an error.</span></span>

<dl> <dt>

<span data-ttu-id="45505-111">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="45505-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45505-112">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="45505-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="45505-113">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="45505-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="45505-114">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="45505-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="45505-115">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="45505-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="45505-116">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="45505-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="45505-117">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="45505-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="45505-118">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="45505-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="45505-119">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="45505-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="45505-120">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="45505-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="45505-121">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="45505-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="45505-122">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="45505-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="45505-123">Требования</span><span class="sxs-lookup"><span data-stu-id="45505-123">Requirements</span></span>



| <span data-ttu-id="45505-124">Требование</span><span class="sxs-lookup"><span data-stu-id="45505-124">Requirement</span></span> | <span data-ttu-id="45505-125">Значение</span><span class="sxs-lookup"><span data-stu-id="45505-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45505-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45505-126">Minimum supported client</span></span><br/> | <span data-ttu-id="45505-127">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="45505-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="45505-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45505-128">Minimum supported server</span></span><br/> | <span data-ttu-id="45505-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="45505-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="45505-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="45505-130">Namespace</span></span><br/>                | <span data-ttu-id="45505-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="45505-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="45505-132">MOF</span><span class="sxs-lookup"><span data-stu-id="45505-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45505-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45505-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="45505-134">DLL</span><span class="sxs-lookup"><span data-stu-id="45505-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45505-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="45505-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="45505-136">См. также</span><span class="sxs-lookup"><span data-stu-id="45505-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45505-137">**Мсвм \_ виртуалсистемреференцепоинтекспортжоб**</span><span class="sxs-lookup"><span data-stu-id="45505-137">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




