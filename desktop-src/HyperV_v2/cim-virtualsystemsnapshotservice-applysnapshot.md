---
description: Применяет моментальный снимок виртуальной системы к виртуальной системе, из которой он был создан.
ms.assetid: acd90ce0-7f82-48d9-9d23-903ba6815779
title: Метод Апплиснапшот класса CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 252f7d7d9a57b439ac00fa663fa0a0e816ebada0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683982"
---
# <a name="applysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="2963d-103">Метод Апплиснапшот \_ класса CIM виртуалсистемснапшотсервице</span><span class="sxs-lookup"><span data-stu-id="2963d-103">ApplySnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="2963d-104">Применяет моментальный снимок виртуальной системы к виртуальной системе, из которой он был создан.</span><span class="sxs-lookup"><span data-stu-id="2963d-104">Applies a virtual system snapshot to the virtual system that it was created from.</span></span>

## <a name="syntax"></a><span data-ttu-id="2963d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2963d-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2963d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2963d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2963d-107">*Моментальный снимок* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2963d-107">*Snapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2963d-108">Ссылка [**на \_ виртуалсистемсеттингдата CIM**](cim-virtualsystemsettingdata.md) для моментального снимка виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="2963d-108">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="2963d-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2963d-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2963d-110">Если операция выполняется долго, может быть возвращена также [**\_ конкретежоб CIM**](cim-concretejob.md) , представляющая задание.</span><span class="sxs-lookup"><span data-stu-id="2963d-110">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

> [!Note]  
> <span data-ttu-id="2963d-111">Этот параметр был доступен для чтения и записи в Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="2963d-111">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2963d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2963d-112">Return value</span></span>

<span data-ttu-id="2963d-113">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="2963d-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="2963d-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="2963d-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2963d-115">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="2963d-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2963d-116">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="2963d-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2963d-117">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="2963d-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2963d-118">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="2963d-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2963d-119">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="2963d-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2963d-120">**Недопустимый тип** (6)</span><span class="sxs-lookup"><span data-stu-id="2963d-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2963d-121">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="2963d-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2963d-122">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="2963d-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2963d-123">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="2963d-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2963d-124">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="2963d-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2963d-125">Требования</span><span class="sxs-lookup"><span data-stu-id="2963d-125">Requirements</span></span>



| <span data-ttu-id="2963d-126">Требование</span><span class="sxs-lookup"><span data-stu-id="2963d-126">Requirement</span></span> | <span data-ttu-id="2963d-127">Значение</span><span class="sxs-lookup"><span data-stu-id="2963d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2963d-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2963d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2963d-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2963d-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2963d-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2963d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2963d-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2963d-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2963d-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2963d-132">Namespace</span></span><br/>                | <span data-ttu-id="2963d-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2963d-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2963d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="2963d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2963d-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2963d-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2963d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2963d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2963d-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2963d-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2963d-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2963d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2963d-139">**\_ВИРТУАЛСИСТЕМСНАПШОТСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="2963d-139">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




