---
description: Предоставляет сведения о состоянии для существующего образа виртуального жесткого диска.
ms.assetid: b0177906-71dc-4be8-b351-97d7ef427acd
title: Класс Msvm_VirtualHardDiskState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskState
- Msvm_VirtualHardDiskState.FileSize
- Msvm_VirtualHardDiskState.InUse
- Msvm_VirtualHardDiskState.MinInternalSize
- Msvm_VirtualHardDiskState.PhysicalSectorSize
- Msvm_VirtualHardDiskState.Alignment
- Msvm_VirtualHardDiskState.FragmentationPercentage
- Msvm_VirtualHardDiskState.Timestamp
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 15d0a8b150e83c17946a6d1b66c7086383f08466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497019"
---
# <a name="msvm_virtualharddiskstate-class"></a><span data-ttu-id="c61bd-103">\_Класс мсвм виртуалхарддискстате</span><span class="sxs-lookup"><span data-stu-id="c61bd-103">Msvm\_VirtualHardDiskState class</span></span>

<span data-ttu-id="c61bd-104">Предоставляет сведения о состоянии для существующего образа виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="c61bd-104">Provides state information for an existing virtual hard disk image.</span></span>

<span data-ttu-id="c61bd-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c61bd-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c61bd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c61bd-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskState
{
  uint64   FileSize;
  boolean  InUse;
  uint64   MinInternalSize;
  uint32   PhysicalSectorSize;
  uint32   Alignment;
  uint32   FragmentationPercentage;
  DATETIME Timestamp;
};
```

## <a name="members"></a><span data-ttu-id="c61bd-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c61bd-107">Members</span></span>

<span data-ttu-id="c61bd-108">Класс **мсвм \_ виртуалхарддискстате** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c61bd-108">The **Msvm\_VirtualHardDiskState** class has these types of members:</span></span>

-   [<span data-ttu-id="c61bd-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c61bd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c61bd-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c61bd-110">Properties</span></span>

<span data-ttu-id="c61bd-111">Класс **мсвм \_ виртуалхарддискстате** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c61bd-111">The **Msvm\_VirtualHardDiskState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c61bd-112">**Выравнивание**</span><span class="sxs-lookup"><span data-stu-id="c61bd-112">**Alignment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c61bd-113">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c61bd-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c61bd-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c61bd-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c61bd-115">Задает тип выравнивания виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="c61bd-115">Specifies the type of alignment of the virtual hard disk.</span></span> <span data-ttu-id="c61bd-116">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c61bd-116">This will be one of the following values.</span></span>



| <span data-ttu-id="c61bd-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c61bd-117">Value</span></span>                                                                        | <span data-ttu-id="c61bd-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c61bd-118">Meaning</span></span>                        |
|------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="c61bd-119"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c61bd-119"><dt>0</dt></span></span> </dl> | <span data-ttu-id="c61bd-120">512. выравнивание по байтам.</span><span class="sxs-lookup"><span data-stu-id="c61bd-120">512 byte alignment.</span></span><br/> |
| <dl> <span data-ttu-id="c61bd-121"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c61bd-121"><dt>1</dt></span></span> </dl> | <span data-ttu-id="c61bd-122">Выравнивание по 4 КБ.</span><span class="sxs-lookup"><span data-stu-id="c61bd-122">4 KB alignment.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="c61bd-123">**Размер файла**</span><span class="sxs-lookup"><span data-stu-id="c61bd-123">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c61bd-124">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c61bd-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c61bd-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c61bd-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c61bd-126">Размер файла виртуального жесткого диска (фактического объема хранилища, используемого файлом) в байтах.</span><span class="sxs-lookup"><span data-stu-id="c61bd-126">The size of the virtual hard disk file (the actual amount of storage being consumed by the file), in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c61bd-127">**фрагментатионперцентаже**</span><span class="sxs-lookup"><span data-stu-id="c61bd-127">**FragmentationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c61bd-128">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c61bd-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c61bd-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c61bd-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c61bd-130">Приблизительное число блоков виртуальных дисков, фрагментированных в файле виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="c61bd-130">An approximation of the percentage of virtual disk blocks that are fragmented in the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="c61bd-131">**Используемых**</span><span class="sxs-lookup"><span data-stu-id="c61bd-131">**InUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c61bd-132">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c61bd-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c61bd-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c61bd-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c61bd-134">Это свойство зарезервировано для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="c61bd-134">This property is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="c61bd-135">**мининтерналсизе**</span><span class="sxs-lookup"><span data-stu-id="c61bd-135">**MinInternalSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c61bd-136">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c61bd-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c61bd-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c61bd-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c61bd-138">Минимальный размер, до которого может быть сжат виртуальный жесткий диск, в байтах.</span><span class="sxs-lookup"><span data-stu-id="c61bd-138">The minimum size that the virtual hard disk can be shrunk to, in bytes.</span></span> <span data-ttu-id="c61bd-139">Этот размер округляется до следующего большего числа, кратного размеру сектора.</span><span class="sxs-lookup"><span data-stu-id="c61bd-139">This size is rounded up to the next largest multiple of the sector size.</span></span>

</dd> <dt>

<span data-ttu-id="c61bd-140">**фисикалсекторсизе**</span><span class="sxs-lookup"><span data-stu-id="c61bd-140">**PhysicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c61bd-141">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c61bd-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c61bd-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c61bd-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c61bd-143">Физический размер сектора, используемый базовым физическим диском в байтах.</span><span class="sxs-lookup"><span data-stu-id="c61bd-143">The physical sector size used by the underlying physical disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c61bd-144">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="c61bd-144">**Timestamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c61bd-145">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c61bd-145">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="c61bd-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c61bd-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c61bd-147">Метка времени виртуального жесткого диска</span><span class="sxs-lookup"><span data-stu-id="c61bd-147">The timestamp of the virtual hard disk</span></span>

> [!Note]  
> <span data-ttu-id="c61bd-148">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="c61bd-148">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c61bd-149">Требования</span><span class="sxs-lookup"><span data-stu-id="c61bd-149">Requirements</span></span>



| <span data-ttu-id="c61bd-150">Требование</span><span class="sxs-lookup"><span data-stu-id="c61bd-150">Requirement</span></span> | <span data-ttu-id="c61bd-151">Значение</span><span class="sxs-lookup"><span data-stu-id="c61bd-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c61bd-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c61bd-152">Minimum supported client</span></span><br/> | <span data-ttu-id="c61bd-153">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c61bd-153">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c61bd-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c61bd-154">Minimum supported server</span></span><br/> | <span data-ttu-id="c61bd-155">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c61bd-155">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c61bd-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c61bd-156">Namespace</span></span><br/>                | <span data-ttu-id="c61bd-157">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c61bd-157">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c61bd-158">MOF</span><span class="sxs-lookup"><span data-stu-id="c61bd-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c61bd-159"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c61bd-159"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c61bd-160">DLL</span><span class="sxs-lookup"><span data-stu-id="c61bd-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c61bd-161"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c61bd-161"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c61bd-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c61bd-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c61bd-163">**жетвиртуалхарддискстате**</span><span class="sxs-lookup"><span data-stu-id="c61bd-163">**GetVirtualHardDiskState**</span></span>](getvirtualharddiskstate-msvm-imagemanagementservice.md)
</dt> </dl>

 

 




