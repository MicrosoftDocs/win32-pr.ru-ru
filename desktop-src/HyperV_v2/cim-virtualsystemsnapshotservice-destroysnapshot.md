---
description: Уничтожает существующий моментальный снимок виртуальной системы. Этот метод может оказаться побочным действием уничтожить другие моментальные снимки, зависящие от затронутого моментального снимка.
ms.assetid: 69f60d0e-50ef-4a38-ad4b-88534b7fb3f8
title: Метод Дестройснапшот класса CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80d618374d2da4a12f2ce31284d7b3fa36ba65ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542391"
---
# <a name="destroysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="ca7f1-104">Метод Дестройснапшот \_ класса CIM виртуалсистемснапшотсервице</span><span class="sxs-lookup"><span data-stu-id="ca7f1-104">DestroySnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="ca7f1-105">Уничтожает существующий моментальный снимок виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="ca7f1-105">Destroy an existing virtual system snapshot.</span></span> <span data-ttu-id="ca7f1-106">Этот метод может оказаться побочным действием уничтожить другие моментальные снимки, зависящие от затронутого моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ca7f1-106">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca7f1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca7f1-107">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ca7f1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca7f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca7f1-109">*Аффектедснапшот* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca7f1-109">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca7f1-110">Ссылка [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) на затронутый моментальный снимок виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="ca7f1-110">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the affected virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="ca7f1-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ca7f1-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca7f1-112">Если операция выполняется долго, может быть возвращена также [**\_ конкретежоб CIM**](cim-concretejob.md) , представляющая задание.</span><span class="sxs-lookup"><span data-stu-id="ca7f1-112">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

> [!Note]  
> <span data-ttu-id="ca7f1-113">Этот параметр был доступен для чтения и записи в Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="ca7f1-113">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca7f1-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca7f1-114">Return value</span></span>

<span data-ttu-id="ca7f1-115">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ca7f1-115">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="ca7f1-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="ca7f1-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ca7f1-117">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="ca7f1-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ca7f1-118">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="ca7f1-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ca7f1-119">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="ca7f1-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ca7f1-120">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="ca7f1-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ca7f1-121">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="ca7f1-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ca7f1-122">**Недопустимый тип** (6)</span><span class="sxs-lookup"><span data-stu-id="ca7f1-122">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ca7f1-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ca7f1-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ca7f1-124">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="ca7f1-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ca7f1-125">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="ca7f1-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="ca7f1-126">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="ca7f1-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ca7f1-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ca7f1-127">Requirements</span></span>



| <span data-ttu-id="ca7f1-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ca7f1-128">Requirement</span></span> | <span data-ttu-id="ca7f1-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ca7f1-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca7f1-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca7f1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ca7f1-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ca7f1-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ca7f1-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca7f1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ca7f1-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ca7f1-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ca7f1-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ca7f1-134">Namespace</span></span><br/>                | <span data-ttu-id="ca7f1-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ca7f1-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ca7f1-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ca7f1-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca7f1-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca7f1-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca7f1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ca7f1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca7f1-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ca7f1-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ca7f1-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca7f1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca7f1-141">**\_ВИРТУАЛСИСТЕМСНАПШОТСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ca7f1-141">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




