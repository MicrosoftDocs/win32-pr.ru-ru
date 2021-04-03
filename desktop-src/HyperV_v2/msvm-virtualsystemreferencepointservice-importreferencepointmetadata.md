---
description: Импортирует метаданные опорной точки виртуальной системы.
ms.assetid: 8e32fded-cd84-4586-83c4-c23200d4698e
title: Метод Импортреференцепоинтметадата класса Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ImportReferencePointMetadata
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c66a374247d324f5df192114d0b66adc3a17c5b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999962"
---
# <a name="importreferencepointmetadata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="f132a-103">Метод Импортреференцепоинтметадата \_ класса Виртуалсистемреференцепоинтсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="f132a-103">ImportReferencePointMetadata method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="f132a-104">Импортирует метаданные опорной точки виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="f132a-104">Imports reference point metadata of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f132a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f132a-105">Syntax</span></span>


```mof
uint32 ImportReferencePointMetadata(
  [in]  Msvm_ComputerSystem REF AffectedSystem,
  [in]  string                  ConfigFilePath,
  [in]  string                  RuntimeStateFilePath,
  [out] CIM_ConcreteJob     REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f132a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f132a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f132a-107">*Аффектедсистем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f132a-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f132a-108">Ссылка на объект [**\_ ComputerSystem мсвм**](msvm-computersystem.md) , описывающий затронутую систему.</span><span class="sxs-lookup"><span data-stu-id="f132a-108">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) describing the affected system.</span></span>

</dd> <dt>

<span data-ttu-id="f132a-109">*Конфигфилепас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f132a-109">*ConfigFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f132a-110">Полный путь к файлу конфигурации, из которого будут импортированы метаданные точки ссылки.</span><span class="sxs-lookup"><span data-stu-id="f132a-110">The fully-qualified path of the config file from where the reference point metadata will be imported.</span></span>

</dd> <dt>

<span data-ttu-id="f132a-111">*Рунтиместатефилепас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f132a-111">*RuntimeStateFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f132a-112">Полный путь к файлу состояния среды выполнения, из которого будут импортированы метаданные точки ссылки.</span><span class="sxs-lookup"><span data-stu-id="f132a-112">The fully-qualified path of the runtime state file from where the reference point metadata will be imported.</span></span>

</dd> <dt>

<span data-ttu-id="f132a-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f132a-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f132a-114">Необязательный параметр для отслеживания хода выполнения операции, который используется, если метод не может быть выполнен синхронно.</span><span class="sxs-lookup"><span data-stu-id="f132a-114">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="f132a-115">Если операция выполняется асинхронно, возвращается значение 4096.</span><span class="sxs-lookup"><span data-stu-id="f132a-115">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f132a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f132a-116">Return value</span></span>

<span data-ttu-id="f132a-117">Возвращает значение 0 (нет ошибки) или одно из следующих сообщений об ошибке:</span><span class="sxs-lookup"><span data-stu-id="f132a-117">Returns either 0 (no error) or one of the following error messages:</span></span>

<dl> <dt>

<span data-ttu-id="f132a-118">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="f132a-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f132a-119">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="f132a-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f132a-120">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="f132a-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f132a-121">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="f132a-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f132a-122">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="f132a-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f132a-123">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="f132a-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f132a-124">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="f132a-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f132a-125">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="f132a-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f132a-126">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="f132a-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f132a-127">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="f132a-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f132a-128">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="f132a-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f132a-129">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="f132a-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f132a-130">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="f132a-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f132a-131">Требования</span><span class="sxs-lookup"><span data-stu-id="f132a-131">Requirements</span></span>



| <span data-ttu-id="f132a-132">Требование</span><span class="sxs-lookup"><span data-stu-id="f132a-132">Requirement</span></span> | <span data-ttu-id="f132a-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f132a-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f132a-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f132a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f132a-135">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="f132a-135">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f132a-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f132a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f132a-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f132a-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f132a-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f132a-138">Namespace</span></span><br/>                | <span data-ttu-id="f132a-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f132a-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f132a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f132a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f132a-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f132a-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f132a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f132a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f132a-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f132a-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f132a-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f132a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f132a-145">**Мсвм \_ виртуалсистемреференцепоинтсервице**</span><span class="sxs-lookup"><span data-stu-id="f132a-145">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




