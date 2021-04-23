---
description: Используется в методе Куеригуестклустеринформатион \_ класса мсвм всссервице для получения сведений о гостевом кластере, частью которого является виртуальная машина.
ms.assetid: c484b38d-9137-44da-a368-a2a673b94ef8
title: Класс Msvm_GuestClusterInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestClusterInformation
- Msvm_GuestClusterInformation.ClusterId
- Msvm_GuestClusterInformation.ClusterSize
- Msvm_GuestClusterInformation.SharedVirtualHardDisks
- Msvm_GuestClusterInformation.SharedVirtualHardDiskPaths
- Msvm_GuestClusterInformation.IsClustered
- Msvm_GuestClusterInformation.IsOnline
- Msvm_GuestClusterInformation.IsOwned
- Msvm_GuestClusterInformation.IsActiveActive
- Msvm_GuestClusterInformation.LastResourceMoveTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee7fa33f142e47b9493e53aa5bc4779623d6ef40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682859"
---
# <a name="msvm_guestclusterinformation-class"></a><span data-ttu-id="84324-103">\_Класс мсвм гуестклустеринформатион</span><span class="sxs-lookup"><span data-stu-id="84324-103">Msvm\_GuestClusterInformation class</span></span>

<span data-ttu-id="84324-104">Используется в методе [**куеригуестклустеринформатион**](msvm-vssservice-queryguestclusterinformation.md) класса [**мсвм \_ всссервице**](msvm-vssservice.md) для получения сведений о гостевом кластере, частью которого является виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="84324-104">Used in the [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) method in the [**Msvm\_VssService**](msvm-vssservice.md) class to retrieve information about the guest cluster the VM is part of.</span></span>

<span data-ttu-id="84324-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="84324-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="84324-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84324-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestClusterInformation
{
  string  ClusterId;
  uint16  ClusterSize;
  string  SharedVirtualHardDisks[];
  string  SharedVirtualHardDiskPaths[];
  boolean IsClustered[];
  boolean IsOnline[];
  boolean IsOwned[];
  boolean IsActiveActive[];
  uint64  LastResourceMoveTime;
};
```

## <a name="members"></a><span data-ttu-id="84324-107">Члены</span><span class="sxs-lookup"><span data-stu-id="84324-107">Members</span></span>

<span data-ttu-id="84324-108">Класс **мсвм \_ гуестклустеринформатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="84324-108">The **Msvm\_GuestClusterInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="84324-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="84324-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84324-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="84324-110">Properties</span></span>

<span data-ttu-id="84324-111">Класс **мсвм \_ гуестклустеринформатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="84324-111">The **Msvm\_GuestClusterInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84324-112">**ClusterId**</span><span class="sxs-lookup"><span data-stu-id="84324-112">**ClusterId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84324-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="84324-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84324-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84324-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84324-115">Идентификатор отказоустойчивого кластера, частью которого является гостевая операционная система виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="84324-115">The identifier of the failover cluster the VM's guest Operating System is a part of.</span></span>

</dd> <dt>

<span data-ttu-id="84324-116">**ClusterSize**</span><span class="sxs-lookup"><span data-stu-id="84324-116">**ClusterSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84324-117">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84324-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84324-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84324-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84324-119">Количество узлов в кластере, частью которого является гостевая операционная система виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="84324-119">Number of nodes in the cluster the VM's guest Operating System is a part of.</span></span>

</dd> <dt>

<span data-ttu-id="84324-120">**исактивеактиве**</span><span class="sxs-lookup"><span data-stu-id="84324-120">**IsActiveActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84324-121">Тип данных: **логический** массив</span><span class="sxs-lookup"><span data-stu-id="84324-121">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="84324-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84324-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84324-123">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="84324-123">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="84324-124">Массив логических значений, соответствующий каждому общему виртуальному жесткому диску, который указывает, является ли соответствующий дисковый ресурс в гостевом кластере общим для виртуальных машин в активном и активном режиме.</span><span class="sxs-lookup"><span data-stu-id="84324-124">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is shared between VMs in active/active mode.</span></span>

</dd> <dt>

<span data-ttu-id="84324-125">**IsClustered**</span><span class="sxs-lookup"><span data-stu-id="84324-125">**IsClustered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84324-126">Тип данных: **логический** массив</span><span class="sxs-lookup"><span data-stu-id="84324-126">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="84324-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84324-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84324-128">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="84324-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="84324-129">Массив логических значений, соответствующий каждому общему виртуальному жесткому диску, указывающему, является ли соответствующий диск ресурсом кластера в гостевом кластере.</span><span class="sxs-lookup"><span data-stu-id="84324-129">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk is a cluster resource in the guest cluster.</span></span>

</dd> <dt>

<span data-ttu-id="84324-130">**Подключение к Интернету**</span><span class="sxs-lookup"><span data-stu-id="84324-130">**IsOnline**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84324-131">Тип данных: **логический** массив</span><span class="sxs-lookup"><span data-stu-id="84324-131">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="84324-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84324-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84324-133">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="84324-133">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="84324-134">Массив логических значений, соответствующий каждому общему виртуальному жесткому диску, указывающему, находится ли соответствующий дисковый ресурс в гостевом кластере в сети.</span><span class="sxs-lookup"><span data-stu-id="84324-134">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is online.</span></span>

</dd> <dt>

<span data-ttu-id="84324-135">**Владелец**</span><span class="sxs-lookup"><span data-stu-id="84324-135">**IsOwned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84324-136">Тип данных: **логический** массив</span><span class="sxs-lookup"><span data-stu-id="84324-136">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="84324-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84324-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84324-138">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="84324-138">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="84324-139">Массив логических значений, соответствующий каждому общему виртуальному жесткому диску, указывающему, является ли соответствующий дисковый ресурс в гостевом кластере курренли владельцем этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="84324-139">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is currenly owned by this VM.</span></span>

</dd> <dt>

<span data-ttu-id="84324-140">**ластресаурцемоветиме**</span><span class="sxs-lookup"><span data-stu-id="84324-140">**LastResourceMoveTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84324-141">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="84324-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="84324-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84324-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84324-143">Число тактов часов при последнем перемещении одного из ресурсов общего диска.</span><span class="sxs-lookup"><span data-stu-id="84324-143">The clock tick count when one of the shared disk resources last moved.</span></span>

> [!Note]  
> <span data-ttu-id="84324-144">Это свойство было добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="84324-144">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="84324-145">**шаредвиртуалхарддискпасс**</span><span class="sxs-lookup"><span data-stu-id="84324-145">**SharedVirtualHardDiskPaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84324-146">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="84324-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="84324-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84324-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84324-148">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="84324-148">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="84324-149">Массив путей к общим виртуальным жестким дискам, подключенных к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="84324-149">An array of shared virtual hard disk paths connected to the VM.</span></span>

</dd> <dt>

<span data-ttu-id="84324-150">**шаредвиртуалхарддискс**</span><span class="sxs-lookup"><span data-stu-id="84324-150">**SharedVirtualHardDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84324-151">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="84324-151">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="84324-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84324-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84324-153">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="84324-153">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="84324-154">Массив данных параметров выделения ресурсов (РАСД), представляющих общие виртуальные жесткие диски, подключенные к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="84324-154">An array of Resource Allocation Setting Data (RASD) representing the shared virtual hard disks connected to the VM.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84324-155">Требования</span><span class="sxs-lookup"><span data-stu-id="84324-155">Requirements</span></span>



| <span data-ttu-id="84324-156">Требование</span><span class="sxs-lookup"><span data-stu-id="84324-156">Requirement</span></span> | <span data-ttu-id="84324-157">Значение</span><span class="sxs-lookup"><span data-stu-id="84324-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84324-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84324-158">Minimum supported client</span></span><br/> | <span data-ttu-id="84324-159">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="84324-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="84324-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84324-160">Minimum supported server</span></span><br/> | <span data-ttu-id="84324-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="84324-161">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="84324-162">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="84324-162">Namespace</span></span><br/>                | <span data-ttu-id="84324-163">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="84324-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="84324-164">MOF</span><span class="sxs-lookup"><span data-stu-id="84324-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84324-165"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84324-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84324-166">DLL</span><span class="sxs-lookup"><span data-stu-id="84324-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84324-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84324-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

