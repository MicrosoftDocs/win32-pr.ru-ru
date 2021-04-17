---
description: Уничтожает виртуальную систему.
ms.assetid: 8d2504dc-ce23-4257-9dfd-6a35dfd84b2d
title: Метод Дестройсистем класса CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 41355970bb70063b8e90deb8f49b5e6f4b439017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683245"
---
# <a name="destroysystem-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="0e21c-103">Метод Дестройсистем \_ класса CIM виртуалсистемманажементсервице</span><span class="sxs-lookup"><span data-stu-id="0e21c-103">DestroySystem method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="0e21c-104">Уничтожает виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="0e21c-104">Destroys a virtual system.</span></span>

<span data-ttu-id="0e21c-105">Виртуальная система, на которую указывает ссылка, уничтожается, включая все элементы, ограниченные ею.</span><span class="sxs-lookup"><span data-stu-id="0e21c-105">The referenced virtual system is destroyed, including any elements scoped by it.</span></span> <span data-ttu-id="0e21c-106">Виртуальные ресурсы возвращаются в пулы ресурсов, что может привести к уничтожению этих ресурсов (зависит от реализации).</span><span class="sxs-lookup"><span data-stu-id="0e21c-106">Virtual resources are returned to their resource pools, which may imply the destruction of those resources (implementation dependent).</span></span> <span data-ttu-id="0e21c-107">Если виртуальная система активна при вызове операции, она сначала деактивируется, а затем уничтожается.</span><span class="sxs-lookup"><span data-stu-id="0e21c-107">If the virtual system is active when the operation is invoked, it is first deactivated and then destroyed.</span></span> <span data-ttu-id="0e21c-108">Если моментальные снимки были созданы из виртуальной системы, они также уничтожаются.</span><span class="sxs-lookup"><span data-stu-id="0e21c-108">If snapshots were created from the virtual system, these are destroyed as well.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e21c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e21c-109">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0e21c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e21c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e21c-111">*Аффектедсистем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0e21c-111">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e21c-112">Ссылка на экземпляр класса CIM, [**представляющий \_**](cim-computersystem.md) виртуальную систему компьютера, которую необходимо уничтожить.</span><span class="sxs-lookup"><span data-stu-id="0e21c-112">Reference to an instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) representing the virtual computer system that is to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="0e21c-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0e21c-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e21c-114">Если операция выполняется долго, может быть возвращена также [**\_ конкретежоб CIM**](cim-concretejob.md) , представляющая задание.</span><span class="sxs-lookup"><span data-stu-id="0e21c-114">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e21c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e21c-115">Return value</span></span>

<span data-ttu-id="0e21c-116">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0e21c-116">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="0e21c-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="0e21c-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0e21c-118">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="0e21c-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0e21c-119">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="0e21c-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0e21c-120">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="0e21c-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0e21c-121">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="0e21c-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0e21c-122">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="0e21c-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0e21c-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="0e21c-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0e21c-124">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="0e21c-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0e21c-125">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="0e21c-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0e21c-126">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="0e21c-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0e21c-127">Требования</span><span class="sxs-lookup"><span data-stu-id="0e21c-127">Requirements</span></span>



| <span data-ttu-id="0e21c-128">Требование</span><span class="sxs-lookup"><span data-stu-id="0e21c-128">Requirement</span></span> | <span data-ttu-id="0e21c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="0e21c-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e21c-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e21c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0e21c-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0e21c-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0e21c-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e21c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0e21c-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0e21c-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0e21c-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0e21c-134">Namespace</span></span><br/>                | <span data-ttu-id="0e21c-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0e21c-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0e21c-136">MOF</span><span class="sxs-lookup"><span data-stu-id="0e21c-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e21c-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e21c-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e21c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0e21c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e21c-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e21c-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0e21c-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e21c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e21c-141">**\_ВИРТУАЛСИСТЕММАНАЖЕМЕНТСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="0e21c-141">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




