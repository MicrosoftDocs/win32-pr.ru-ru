---
description: Экспортирует опорную точку виртуальной системы.
ms.assetid: e4d80404-6b1b-4153-9ab2-aebab18c331a
title: Метод Експортреференцепоинт класса Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bedd051123e4f75d7438b2e3831a84204ff4aec3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105664814"
---
# <a name="exportreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="0f6b9-103">Метод Експортреференцепоинт \_ класса Виртуалсистемреференцепоинтсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="0f6b9-103">ExportReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="0f6b9-104">Экспортирует опорную точку виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="0f6b9-104">Exports the reference point of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f6b9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f6b9-105">Syntax</span></span>


```mof
uint32 ExportReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF ReferencePoint,
  [in]  string                               ExportDirectory,
  [in]  string                               ExportSettingData,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0f6b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f6b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f6b9-107">*Референцепоинт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f6b9-107">*ReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f6b9-108">Ссылка на экземпляр [**\_ виртуалсистемреференцепоинт мсвм**](msvm-virtualsystemreferencepoint.md) , представляющий эталонную точку для экспорта.</span><span class="sxs-lookup"><span data-stu-id="0f6b9-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="0f6b9-109">*Експортдиректори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f6b9-109">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f6b9-110">Полный путь к каталогу, в который должна быть экспортирована эталонная точка.</span><span class="sxs-lookup"><span data-stu-id="0f6b9-110">The fully-qualified path of the directory to which the reference point is to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="0f6b9-111">*Експортсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f6b9-111">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f6b9-112">Экземпляр [**мсвм \_ виртуалсистемреференцепоинтекспортсеттингдата**](msvm-virtualsystemreferencepointexportsettingdata.md) , представляющий параметры для операции экспорта.</span><span class="sxs-lookup"><span data-stu-id="0f6b9-112">An instance of [**Msvm\_VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="0f6b9-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0f6b9-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f6b9-114">Необязательный параметр для отслеживания хода выполнения операции, который используется, если метод не может быть выполнен синхронно.</span><span class="sxs-lookup"><span data-stu-id="0f6b9-114">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="0f6b9-115">Если операция выполняется асинхронно, возвращается значение 4096.</span><span class="sxs-lookup"><span data-stu-id="0f6b9-115">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f6b9-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f6b9-116">Return value</span></span>

<span data-ttu-id="0f6b9-117">При успешном выполнении возвращает значение 0 (завершено без ошибок) или 4096 (задание запущено); в противном случае возвратите ошибку.</span><span class="sxs-lookup"><span data-stu-id="0f6b9-117">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="0f6b9-118">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="0f6b9-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0f6b9-119">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="0f6b9-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0f6b9-120">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="0f6b9-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0f6b9-121">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="0f6b9-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0f6b9-122">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="0f6b9-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0f6b9-123">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="0f6b9-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0f6b9-124">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="0f6b9-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0f6b9-125">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="0f6b9-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0f6b9-126">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="0f6b9-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0f6b9-127">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="0f6b9-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0f6b9-128">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="0f6b9-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0f6b9-129">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="0f6b9-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0f6b9-130">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="0f6b9-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0f6b9-131">Требования</span><span class="sxs-lookup"><span data-stu-id="0f6b9-131">Requirements</span></span>



| <span data-ttu-id="0f6b9-132">Требование</span><span class="sxs-lookup"><span data-stu-id="0f6b9-132">Requirement</span></span> | <span data-ttu-id="0f6b9-133">Значение</span><span class="sxs-lookup"><span data-stu-id="0f6b9-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f6b9-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f6b9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0f6b9-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0f6b9-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0f6b9-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f6b9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0f6b9-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0f6b9-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0f6b9-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0f6b9-138">Namespace</span></span><br/>                | <span data-ttu-id="0f6b9-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0f6b9-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0f6b9-140">MOF</span><span class="sxs-lookup"><span data-stu-id="0f6b9-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f6b9-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f6b9-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f6b9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0f6b9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f6b9-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f6b9-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0f6b9-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f6b9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f6b9-145">**Мсвм \_ виртуалсистемреференцепоинтсервице**</span><span class="sxs-lookup"><span data-stu-id="0f6b9-145">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




