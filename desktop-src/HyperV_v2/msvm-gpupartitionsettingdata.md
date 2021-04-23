---
description: Представляет настроенное состояние для устройства раздела GPU.
ms.assetid: 33ec4ea2-4e79-4c84-8abe-da8308ad6702
title: Класс Msvm_GpuPartitionSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartitionSettingData
- Msvm_GpuPartitionSettingData.MinPartitionVRAM
- Msvm_GpuPartitionSettingData.MaxPartitionVRAM
- Msvm_GpuPartitionSettingData.OptimalPartitionVRAM
- Msvm_GpuPartitionSettingData.MinPartitionEncode
- Msvm_GpuPartitionSettingData.MaxPartitionEncode
- Msvm_GpuPartitionSettingData.OptimalPartitionEncode
- Msvm_GpuPartitionSettingData.MinPartitionDecode
- Msvm_GpuPartitionSettingData.MaxPartitionDecode
- Msvm_GpuPartitionSettingData.OptimalPartitionDecode
- Msvm_GpuPartitionSettingData.MinPartitionCompute
- Msvm_GpuPartitionSettingData.MaxPartitionCompute
- Msvm_GpuPartitionSettingData.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7d8c9809b3a062654eaf0fb7a73b75b0188f7284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991227"
---
# <a name="msvm_gpupartitionsettingdata-class"></a><span data-ttu-id="a00c2-103">\_Класс мсвм гпупартитионсеттингдата</span><span class="sxs-lookup"><span data-stu-id="a00c2-103">Msvm\_GpuPartitionSettingData class</span></span>

<span data-ttu-id="a00c2-104">Представляет настроенное состояние для устройства раздела GPU.</span><span class="sxs-lookup"><span data-stu-id="a00c2-104">Represents the configured state of a GPU partition device.</span></span>

<span data-ttu-id="a00c2-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a00c2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a00c2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a00c2-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartitionSettingData : CIM_ResourceAllocationSettingData
{
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a><span data-ttu-id="a00c2-107">Члены</span><span class="sxs-lookup"><span data-stu-id="a00c2-107">Members</span></span>

<span data-ttu-id="a00c2-108">Класс **мсвм \_ гпупартитионсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a00c2-108">The **Msvm\_GpuPartitionSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a00c2-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="a00c2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a00c2-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a00c2-110">Properties</span></span>

<span data-ttu-id="a00c2-111">Класс **мсвм \_ гпупартитионсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a00c2-111">The **Msvm\_GpuPartitionSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a00c2-112">**макспартитионкомпуте**</span><span class="sxs-lookup"><span data-stu-id="a00c2-112">**MaxPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a00c2-113">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a00c2-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a00c2-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a00c2-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a00c2-115">Максимальный объем модулей вычислений, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="a00c2-115">The maximum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a00c2-116">**макспартитиондекоде**</span><span class="sxs-lookup"><span data-stu-id="a00c2-116">**MaxPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a00c2-117">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a00c2-117">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a00c2-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a00c2-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a00c2-119">Максимальный объем модулей декодирования, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="a00c2-119">The maximum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a00c2-120">**макспартитионенкоде**</span><span class="sxs-lookup"><span data-stu-id="a00c2-120">**MaxPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a00c2-121">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a00c2-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a00c2-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a00c2-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a00c2-123">Максимальный объем модулей кодирования, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="a00c2-123">The maximum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a00c2-124">**макспартитионврам**</span><span class="sxs-lookup"><span data-stu-id="a00c2-124">**MaxPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a00c2-125">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a00c2-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a00c2-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a00c2-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a00c2-127">Максимальный объем видеопамяти, который будет отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="a00c2-127">The maximum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a00c2-128">**минпартитионкомпуте**</span><span class="sxs-lookup"><span data-stu-id="a00c2-128">**MinPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a00c2-129">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a00c2-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a00c2-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a00c2-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a00c2-131">Минимальное количество ядер, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="a00c2-131">The minumum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a00c2-132">**минпартитиондекоде**</span><span class="sxs-lookup"><span data-stu-id="a00c2-132">**MinPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a00c2-133">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a00c2-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a00c2-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a00c2-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a00c2-135">Минимальный объем модулей декодирования, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="a00c2-135">The minimum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a00c2-136">**минпартитионенкоде**</span><span class="sxs-lookup"><span data-stu-id="a00c2-136">**MinPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a00c2-137">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a00c2-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a00c2-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a00c2-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a00c2-139">Минимальный объем модулей кодирования, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="a00c2-139">The minimum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a00c2-140">**минпартитионврам**</span><span class="sxs-lookup"><span data-stu-id="a00c2-140">**MinPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a00c2-141">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a00c2-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a00c2-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a00c2-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a00c2-143">Минимальный объем видеопамяти, который будет отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="a00c2-143">The minimum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a00c2-144">**оптималпартитионкомпуте**</span><span class="sxs-lookup"><span data-stu-id="a00c2-144">**OptimalPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a00c2-145">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a00c2-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a00c2-146">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a00c2-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a00c2-147">Оптимальный объем модулей вычислений, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="a00c2-147">The optimal amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a00c2-148">**оптималпартитиондекоде**</span><span class="sxs-lookup"><span data-stu-id="a00c2-148">**OptimalPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a00c2-149">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a00c2-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a00c2-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a00c2-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a00c2-151">Оптимальный объем модулей декодирования, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="a00c2-151">The optimal amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a00c2-152">**оптималпартитионенкоде**</span><span class="sxs-lookup"><span data-stu-id="a00c2-152">**OptimalPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a00c2-153">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a00c2-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a00c2-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a00c2-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a00c2-155">Оптимальный объем модулей кодирования, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="a00c2-155">The optimal amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="a00c2-156">**оптималпартитионврам**</span><span class="sxs-lookup"><span data-stu-id="a00c2-156">**OptimalPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a00c2-157">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a00c2-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a00c2-158">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a00c2-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a00c2-159">Оптимальный объем видеопамяти, который будет отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="a00c2-159">The optimal amount of VRAM which will appear in the GPU partition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a00c2-160">Требования</span><span class="sxs-lookup"><span data-stu-id="a00c2-160">Requirements</span></span>



| <span data-ttu-id="a00c2-161">Требование</span><span class="sxs-lookup"><span data-stu-id="a00c2-161">Requirement</span></span> | <span data-ttu-id="a00c2-162">Значение</span><span class="sxs-lookup"><span data-stu-id="a00c2-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a00c2-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a00c2-163">Minimum supported client</span></span><br/> | <span data-ttu-id="a00c2-164">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="a00c2-164">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a00c2-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a00c2-165">Minimum supported server</span></span><br/> | <span data-ttu-id="a00c2-166">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a00c2-166">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a00c2-167">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a00c2-167">Namespace</span></span><br/>                | <span data-ttu-id="a00c2-168">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a00c2-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a00c2-169">MOF</span><span class="sxs-lookup"><span data-stu-id="a00c2-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a00c2-170"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a00c2-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a00c2-171">DLL</span><span class="sxs-lookup"><span data-stu-id="a00c2-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a00c2-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a00c2-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a00c2-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a00c2-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a00c2-174">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="a00c2-174">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




