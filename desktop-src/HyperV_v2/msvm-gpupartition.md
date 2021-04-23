---
description: Представляет состояние раздела GPU.
ms.assetid: 319b37d5-b5f0-4251-9482-316347a9015b
title: Класс Msvm_GpuPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartition
- Msvm_GpuPartition.DeviceInstancePath
- Msvm_GpuPartition.PartitionId
- Msvm_GpuPartition.PartitionVfLuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc0975644609832c692f5522cc756240f7a5bff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682861"
---
# <a name="msvm_gpupartition-class"></a><span data-ttu-id="d6f2b-103">\_Класс мсвм гпупартитион</span><span class="sxs-lookup"><span data-stu-id="d6f2b-103">Msvm\_GpuPartition class</span></span>

<span data-ttu-id="d6f2b-104">Представляет состояние раздела GPU.</span><span class="sxs-lookup"><span data-stu-id="d6f2b-104">Represents the state of the GPU partition.</span></span>

<span data-ttu-id="d6f2b-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d6f2b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6f2b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6f2b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartition : CIM_LogicalDevice
{
  string DeviceInstancePath;
  uint16 PartitionId;
  string PartitionVfLuid;
};
```

## <a name="members"></a><span data-ttu-id="d6f2b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d6f2b-107">Members</span></span>

<span data-ttu-id="d6f2b-108">Класс **мсвм \_ гпупартитион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d6f2b-108">The **Msvm\_GpuPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="d6f2b-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="d6f2b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d6f2b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d6f2b-110">Properties</span></span>

<span data-ttu-id="d6f2b-111">Класс **мсвм \_ гпупартитион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d6f2b-111">The **Msvm\_GpuPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d6f2b-112">**девицеинстанцепас**</span><span class="sxs-lookup"><span data-stu-id="d6f2b-112">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f2b-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d6f2b-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6f2b-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d6f2b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6f2b-115">Строка, содержащая путь к экземпляру устройства, который определяет устройство раздела GPU.</span><span class="sxs-lookup"><span data-stu-id="d6f2b-115">A string containing the device instance path that identifies the GPU partition device.</span></span>

</dd> <dt>

<span data-ttu-id="d6f2b-116">**PartitionId**</span><span class="sxs-lookup"><span data-stu-id="d6f2b-116">**PartitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f2b-117">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d6f2b-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6f2b-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d6f2b-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6f2b-119">Идентификатор секции устройства раздела GPU.</span><span class="sxs-lookup"><span data-stu-id="d6f2b-119">The partition ID of the GPU partition device.</span></span>

</dd> <dt>

<span data-ttu-id="d6f2b-120">**партитионвфлуид**</span><span class="sxs-lookup"><span data-stu-id="d6f2b-120">**PartitionVfLuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f2b-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d6f2b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6f2b-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d6f2b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6f2b-123">Виртуальный LUID функции, представляющий раздел GPU.</span><span class="sxs-lookup"><span data-stu-id="d6f2b-123">The virtual function LUID, which represents a GPU partition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6f2b-124">Требования</span><span class="sxs-lookup"><span data-stu-id="d6f2b-124">Requirements</span></span>



| <span data-ttu-id="d6f2b-125">Требование</span><span class="sxs-lookup"><span data-stu-id="d6f2b-125">Requirement</span></span> | <span data-ttu-id="d6f2b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d6f2b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f2b-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6f2b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d6f2b-128">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="d6f2b-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d6f2b-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6f2b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d6f2b-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d6f2b-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d6f2b-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d6f2b-131">Namespace</span></span><br/>                | <span data-ttu-id="d6f2b-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d6f2b-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d6f2b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="d6f2b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6f2b-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6f2b-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6f2b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d6f2b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6f2b-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d6f2b-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d6f2b-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6f2b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f2b-138">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="d6f2b-138">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




