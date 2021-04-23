---
description: Применяет моментальный снимок виртуальной машины к виртуальной машине, из которой он был создан.
ms.assetid: 45f1ec8f-aa96-4060-8f8c-0471d0ad4a21
title: Метод Апплиснапшот класса Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 735e827935689a0f0ede7fbac1d582ea40772ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909840"
---
# <a name="applysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="cf348-103">Метод Апплиснапшот \_ класса Виртуалсистемснапшотсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="cf348-103">ApplySnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="cf348-104">Применяет моментальный снимок виртуальной машины к виртуальной машине, из которой он был создан.</span><span class="sxs-lookup"><span data-stu-id="cf348-104">Applies a virtual machine snapshot to the virtual machine that it was created from.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf348-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf348-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="cf348-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf348-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf348-107">*Моментальный снимок* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf348-107">*Snapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf348-108">Ссылка на класс, производный от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)) , который представляет моментальный снимок виртуальной машины, который необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="cf348-108">A reference to a class derived from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) that represents the virtual machine snapshot to be applied.</span></span>

</dd> <dt>

<span data-ttu-id="cf348-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cf348-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf348-110">Эта операция всегда выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="cf348-110">This operation is always performed asynchronously.</span></span> <span data-ttu-id="cf348-111">Этот метод возвращает 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cf348-111">This method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf348-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf348-112">Return value</span></span>

<span data-ttu-id="cf348-113">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="cf348-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="cf348-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="cf348-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cf348-115">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="cf348-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cf348-116">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="cf348-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cf348-117">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="cf348-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cf348-118">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="cf348-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cf348-119">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="cf348-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="cf348-120">**Недопустимый тип** (6)</span><span class="sxs-lookup"><span data-stu-id="cf348-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="cf348-121">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="cf348-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cf348-122">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="cf348-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cf348-123">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="cf348-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cf348-124">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="cf348-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cf348-125">**Недопустимое состояние** (32775)</span><span class="sxs-lookup"><span data-stu-id="cf348-125">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cf348-126">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="cf348-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="cf348-127">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="cf348-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cf348-128">Требования</span><span class="sxs-lookup"><span data-stu-id="cf348-128">Requirements</span></span>



| <span data-ttu-id="cf348-129">Требование</span><span class="sxs-lookup"><span data-stu-id="cf348-129">Requirement</span></span> | <span data-ttu-id="cf348-130">Значение</span><span class="sxs-lookup"><span data-stu-id="cf348-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf348-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf348-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cf348-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cf348-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cf348-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf348-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cf348-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cf348-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cf348-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cf348-135">Namespace</span></span><br/>                | <span data-ttu-id="cf348-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="cf348-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cf348-137">MOF</span><span class="sxs-lookup"><span data-stu-id="cf348-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf348-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf348-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf348-139">DLL</span><span class="sxs-lookup"><span data-stu-id="cf348-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf348-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cf348-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cf348-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf348-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf348-142">**Мсвм \_ виртуалсистемснапшотсервице**</span><span class="sxs-lookup"><span data-stu-id="cf348-142">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="cf348-143">**Аппливиртуалсистемснапшот (v1)**</span><span class="sxs-lookup"><span data-stu-id="cf348-143">**ApplyVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/applyvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="cf348-144">**Аппливиртуалсистемснапшотекс (v1)**</span><span class="sxs-lookup"><span data-stu-id="cf348-144">**ApplyVirtualSystemSnapshotEx (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-virtualsystemmanagementservice-applyvirtualsystemsnapshotex)
</dt> </dl>

 

