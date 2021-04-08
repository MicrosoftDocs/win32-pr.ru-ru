---
description: Представляет секционированный GPU. Каждый GPU может быть разбит на несколько разделов GPU, которые могут быть назначены виртуальной машине в виде виртуального видеонабора.
ms.assetid: a32dfc03-6967-4fa3-ae32-bf074137740b
title: Класс Msvm_PartitionableGpu
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PartitionableGpu
- Msvm_PartitionableGpu.ValidPartitionCounts
- Msvm_PartitionableGpu.PartitionCount
- Msvm_PartitionableGpu.TotalVRAM
- Msvm_PartitionableGpu.AvailableVRAM
- Msvm_PartitionableGpu.MinPartitionVRAM
- Msvm_PartitionableGpu.MaxPartitionVRAM
- Msvm_PartitionableGpu.OptimalPartitionVRAM
- Msvm_PartitionableGpu.TotalEncode
- Msvm_PartitionableGpu.AvailableEncode
- Msvm_PartitionableGpu.MinPartitionEncode
- Msvm_PartitionableGpu.MaxPartitionEncode
- Msvm_PartitionableGpu.OptimalPartitionEncode
- Msvm_PartitionableGpu.TotalDecode
- Msvm_PartitionableGpu.AvailableDecode
- Msvm_PartitionableGpu.MinPartitionDecode
- Msvm_PartitionableGpu.MaxPartitionDecode
- Msvm_PartitionableGpu.OptimalPartitionDecode
- Msvm_PartitionableGpu.TotalCompute
- Msvm_PartitionableGpu.AvailableCompute
- Msvm_PartitionableGpu.MinPartitionCompute
- Msvm_PartitionableGpu.MaxPartitionCompute
- Msvm_PartitionableGpu.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f82904608a8e2ee4dfa13942066d57d35d511f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913112"
---
# <a name="msvm_partitionablegpu-class"></a><span data-ttu-id="f2ac9-104">\_Класс мсвм партитионаблегпу</span><span class="sxs-lookup"><span data-stu-id="f2ac9-104">Msvm\_PartitionableGpu class</span></span>

<span data-ttu-id="f2ac9-105">Представляет секционированный GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-105">Represents a partitionable GPU.</span></span> <span data-ttu-id="f2ac9-106">Каждый GPU может быть разбит на несколько разделов GPU, которые могут быть назначены виртуальной машине в виде виртуального видеонабора.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-106">Each GPU can be sliced into a number of GPU partitions, which can be assigned to a virtual machine as a vGPU.</span></span>

<span data-ttu-id="f2ac9-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2ac9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2ac9-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PartitionableGpu : CIM_ComputerSystem
{
  uint16 ValidPartitionCounts[];
  uint16 PartitionCount;
  uint64 TotalVRAM;
  uint64 AvailableVRAM;
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 TotalEncode;
  uint64 AvailableEncode;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 TotalDecode;
  uint64 AvailableDecode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 TotalCompute;
  uint64 AvailableCompute;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a><span data-ttu-id="f2ac9-109">Члены</span><span class="sxs-lookup"><span data-stu-id="f2ac9-109">Members</span></span>

<span data-ttu-id="f2ac9-110">Класс **мсвм \_ партитионаблегпу** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f2ac9-110">The **Msvm\_PartitionableGpu** class has these types of members:</span></span>

-   [<span data-ttu-id="f2ac9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2ac9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2ac9-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2ac9-112">Properties</span></span>

<span data-ttu-id="f2ac9-113">Класс **мсвм \_ партитионаблегпу** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-113">The **Msvm\_PartitionableGpu** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2ac9-114">**аваилаблекомпуте**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-114">**AvailableCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-115">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-115">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-117">Доступный объем модулей вычислений, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-117">The available amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-118">**аваилабледекоде**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-118">**AvailableDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-119">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-121">Доступный объем модулей декодирования, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-121">The available amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-122">**аваилаблинкоде**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-122">**AvailableEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-123">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-125">Доступный объем модулей кодирования, который будет отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-125">The available amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-126">**аваилаблеврам**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-126">**AvailableVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-127">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-127">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-129">Доступный объем видеопамяти, который будет отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-129">The available amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-130">**макспартитионкомпуте**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-130">**MaxPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-131">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-133">Максимальный объем модулей вычислений, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-133">The maximum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-134">**макспартитиондекоде**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-134">**MaxPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-135">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-137">Максимальный объем модулей декодирования, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-137">The maximum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-138">**макспартитионенкоде**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-138">**MaxPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-139">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-139">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-141">Максимальный объем модулей кодирования, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-141">The maximum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-142">**макспартитионврам**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-142">**MaxPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-143">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-145">Максимальный объем видеопамяти, который будет отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-145">The maximum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-146">**минпартитионкомпуте**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-146">**MinPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-147">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-149">Минимальное количество ядер, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-149">The minumum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-150">**минпартитиондекоде**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-150">**MinPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-151">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-151">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-153">Минимальный объем модулей декодирования, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-153">The minimum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-154">**минпартитионенкоде**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-154">**MinPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-155">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-157">Минимальноеный объем модулей кодирования, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-157">The minumum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-158">**минпартитионврам**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-158">**MinPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-159">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-161">Минимальный объем видеопамяти, который будет отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-161">The minimum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-162">**оптималпартитионкомпуте**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-162">**OptimalPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-163">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-163">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-165">Оптимальный объем модулей вычислений, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-165">The optimal amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-166">**оптималпартитиондекоде**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-166">**OptimalPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-167">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-167">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-169">Оптимальный объем модулей декодирования, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-169">The optimal amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-170">**оптималпартитионенкоде**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-170">**OptimalPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-171">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-173">Оптимальный объем модулей кодирования, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-173">The optimal amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-174">**оптималпартитионврам**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-174">**OptimalPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-175">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-177">Оптимальный объем видеопамяти, который будет отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-177">The optimal amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-178">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-178">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-179">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-180">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f2ac9-180">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-181">Объем разделов GPU, на которые разбит физический GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-181">The amount of GPU partitions the physical GPU is sliced into.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-182">**тоталкомпуте**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-182">**TotalCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-183">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-185">Общий объем модулей вычислений, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-185">The total amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-186">**тоталдекоде**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-186">**TotalDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-187">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-189">Общий объем модулей декодирования, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-189">The total amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-190">**тоталенкоде**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-190">**TotalEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-191">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-191">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-193">Общий объем модулей кодирования, которые будут отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-193">The total amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-194">**тоталврам**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-194">**TotalVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-195">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2ac9-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-197">Общий объем видеопамяти, который будет отображаться в разделе GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-197">The total amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="f2ac9-198">**валидпартитионкаунтс**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-198">**ValidPartitionCounts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2ac9-199">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="f2ac9-199">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f2ac9-200">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f2ac9-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f2ac9-201">Массив допустимых параметров раздела GPU, в который может быть разбит физический GPU.</span><span class="sxs-lookup"><span data-stu-id="f2ac9-201">An array of valid GPU partition options the physical GPU can be sliced into.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2ac9-202">Требования</span><span class="sxs-lookup"><span data-stu-id="f2ac9-202">Requirements</span></span>



| <span data-ttu-id="f2ac9-203">Требование</span><span class="sxs-lookup"><span data-stu-id="f2ac9-203">Requirement</span></span> | <span data-ttu-id="f2ac9-204">Значение</span><span class="sxs-lookup"><span data-stu-id="f2ac9-204">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ac9-205">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2ac9-205">Minimum supported client</span></span><br/> | <span data-ttu-id="f2ac9-206">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="f2ac9-206">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f2ac9-207">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2ac9-207">Minimum supported server</span></span><br/> | <span data-ttu-id="f2ac9-208">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f2ac9-208">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f2ac9-209">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f2ac9-209">Namespace</span></span><br/>                | <span data-ttu-id="f2ac9-210">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f2ac9-210">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f2ac9-211">MOF</span><span class="sxs-lookup"><span data-stu-id="f2ac9-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2ac9-212"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2ac9-212"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2ac9-213">DLL</span><span class="sxs-lookup"><span data-stu-id="f2ac9-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2ac9-214"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f2ac9-214"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f2ac9-215">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2ac9-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ac9-216">**CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="f2ac9-216">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

 




