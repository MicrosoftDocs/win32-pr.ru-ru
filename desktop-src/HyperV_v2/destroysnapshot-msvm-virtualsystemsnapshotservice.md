---
description: Уничтожает существующий моментальный снимок виртуальной машины.
ms.assetid: 84752bb3-cae1-4a93-89bc-e735c058feda
title: Метод Дестройснапшот класса Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 91c2e59baa8bb22f5ea9f128130d7dc440e28ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912848"
---
# <a name="destroysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="7ed4e-103">Метод Дестройснапшот \_ класса Виртуалсистемснапшотсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="7ed4e-103">DestroySnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="7ed4e-104">Уничтожает существующий моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7ed4e-104">Destroys an existing virtual machine snapshot.</span></span> <span data-ttu-id="7ed4e-105">Этот метод может в качестве побочного результата уничтожить другие моментальные снимки, зависящие от затронутого моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="7ed4e-105">This method may, as a side effect, destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ed4e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ed4e-106">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7ed4e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ed4e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ed4e-108">*Аффектедснапшот* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ed4e-108">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ed4e-109">Ссылка на [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)) , представляющая моментальный снимок виртуальной машины для уничтожения.</span><span class="sxs-lookup"><span data-stu-id="7ed4e-109">A [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) reference that represents the virtual machine snapshot to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="7ed4e-110">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7ed4e-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ed4e-111">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7ed4e-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ed4e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ed4e-112">Return value</span></span>

<span data-ttu-id="7ed4e-113">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7ed4e-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7ed4e-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="7ed4e-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7ed4e-115">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="7ed4e-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7ed4e-116">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="7ed4e-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7ed4e-117">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="7ed4e-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7ed4e-118">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="7ed4e-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7ed4e-119">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="7ed4e-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7ed4e-120">**Недопустимый тип** (6)</span><span class="sxs-lookup"><span data-stu-id="7ed4e-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7ed4e-121">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="7ed4e-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7ed4e-122">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="7ed4e-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7ed4e-123">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7ed4e-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7ed4e-124">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="7ed4e-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7ed4e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7ed4e-125">Requirements</span></span>



| <span data-ttu-id="7ed4e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7ed4e-126">Requirement</span></span> | <span data-ttu-id="7ed4e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7ed4e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed4e-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ed4e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7ed4e-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7ed4e-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7ed4e-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ed4e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7ed4e-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7ed4e-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7ed4e-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7ed4e-132">Namespace</span></span><br/>                | <span data-ttu-id="7ed4e-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7ed4e-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7ed4e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7ed4e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ed4e-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ed4e-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ed4e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7ed4e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ed4e-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7ed4e-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7ed4e-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ed4e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ed4e-139">**Мсвм \_ виртуалсистемснапшотсервице**</span><span class="sxs-lookup"><span data-stu-id="7ed4e-139">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="7ed4e-140">**Ремовевиртуалсистемснапшот (v1)**</span><span class="sxs-lookup"><span data-stu-id="7ed4e-140">**RemoveVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

