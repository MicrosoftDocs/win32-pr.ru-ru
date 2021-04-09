---
description: Возвращает ошибку.
ms.assetid: 7c47acae-d398-4698-81db-e3c8a812f339
title: Метод method класса Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ea92bd08a2b65466d11e41bb459200610a89677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081406"
---
# <a name="geterror-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="f1085-103">Метод method \_ класса мсвм коллектионреференцепоинтекспортжоб</span><span class="sxs-lookup"><span data-stu-id="f1085-103">GetError method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="f1085-104">Возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f1085-104">Retrieves an error.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1085-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1085-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="f1085-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1085-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1085-107">*Ошибка при* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f1085-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1085-108">При успешном выполнении содержит описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="f1085-108">On success, contains a description of the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1085-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1085-109">Return value</span></span>

<span data-ttu-id="f1085-110">0 при успешном выполнении; в противном случае — ошибка.</span><span class="sxs-lookup"><span data-stu-id="f1085-110">0 on success; otherwise, an error.</span></span>

<dl> <dt>

<span data-ttu-id="f1085-111">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="f1085-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f1085-112">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="f1085-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f1085-113">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="f1085-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f1085-114">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="f1085-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f1085-115">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="f1085-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f1085-116">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="f1085-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f1085-117">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="f1085-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f1085-118">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="f1085-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f1085-119">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="f1085-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f1085-120">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="f1085-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f1085-121">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="f1085-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f1085-122">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="f1085-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f1085-123">Требования</span><span class="sxs-lookup"><span data-stu-id="f1085-123">Requirements</span></span>



| <span data-ttu-id="f1085-124">Требование</span><span class="sxs-lookup"><span data-stu-id="f1085-124">Requirement</span></span> | <span data-ttu-id="f1085-125">Значение</span><span class="sxs-lookup"><span data-stu-id="f1085-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1085-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1085-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f1085-127">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="f1085-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f1085-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1085-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f1085-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f1085-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f1085-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f1085-130">Namespace</span></span><br/>                | <span data-ttu-id="f1085-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f1085-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f1085-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f1085-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1085-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1085-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1085-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f1085-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1085-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1085-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f1085-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1085-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1085-137">**Мсвм \_ коллектионреференцепоинтекспортжоб**</span><span class="sxs-lookup"><span data-stu-id="f1085-137">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




