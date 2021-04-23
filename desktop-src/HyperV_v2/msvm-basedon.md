---
description: Ассоциация, которая описывает, как можно собрать экстенты хранилища из экстентов нижнего уровня.
ms.assetid: 8be9bb2c-ef46-454b-bfc3-0398c64d17b7
title: Класс Msvm_BasedOn
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BasedOn
- Msvm_BasedOn.Antecedent
- Msvm_BasedOn.Dependent
- Msvm_BasedOn.StartingAddress
- Msvm_BasedOn.EndingAddress
- Msvm_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8262ae5e510574bf02630410b584d9df10d64ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664336"
---
# <a name="msvm_basedon-class"></a><span data-ttu-id="f8adc-103">\_Класс мсвм BasedOn</span><span class="sxs-lookup"><span data-stu-id="f8adc-103">Msvm\_BasedOn class</span></span>

<span data-ttu-id="f8adc-104">Ассоциация, которая описывает, как можно собрать экстенты хранилища из экстентов нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="f8adc-104">An association that describes how storage extents can be assembled from lower level extents.</span></span> <span data-ttu-id="f8adc-105">Например, Протектедспацеекстентс являются частями Фисикалекстентс, а Волумесетс собраны из одного или нескольких физических или Протектедспацеекстентс.</span><span class="sxs-lookup"><span data-stu-id="f8adc-105">For example, ProtectedSpaceExtents are parts of PhysicalExtents, while VolumeSets are assembled from one or more Physical or ProtectedSpaceExtents.</span></span> <span data-ttu-id="f8adc-106">Другой пример: Качемемори может быть определен независимо и реализован в Фисикалелемент или может быть основан на volatile или Нонволатилесторажеекстентс.</span><span class="sxs-lookup"><span data-stu-id="f8adc-106">As another example, CacheMemory can be defined independently and realized in a PhysicalElement or can be based on Volatile or NonVolatileStorageExtents.</span></span>

<span data-ttu-id="f8adc-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f8adc-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8adc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8adc-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BasedOn : CIM_BasedOn
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a><span data-ttu-id="f8adc-109">Члены</span><span class="sxs-lookup"><span data-stu-id="f8adc-109">Members</span></span>

<span data-ttu-id="f8adc-110">Класс **мсвм \_ BasedOn** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f8adc-110">The **Msvm\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="f8adc-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8adc-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8adc-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8adc-112">Properties</span></span>

<span data-ttu-id="f8adc-113">Класс **мсвм \_ BasedOn** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f8adc-113">The **Msvm\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8adc-114">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="f8adc-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8adc-115">Тип данных: **[ **CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="f8adc-115">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="f8adc-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8adc-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8adc-117">Экстент хранения нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="f8adc-117">The lower level storage extent.</span></span> <span data-ttu-id="f8adc-118">Это свойство наследуется от [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="f8adc-118">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="f8adc-119">**Него**</span><span class="sxs-lookup"><span data-stu-id="f8adc-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8adc-120">Тип данных: **[ **CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="f8adc-120">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="f8adc-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8adc-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8adc-122">Область хранения более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="f8adc-122">The higher level storage extent.</span></span> <span data-ttu-id="f8adc-123">Это свойство наследуется от [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="f8adc-123">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="f8adc-124">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="f8adc-124">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8adc-125">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8adc-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8adc-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8adc-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8adc-127">Конечный адрес, на котором заканчивается экстент более высокого уровня, в хранилище более низких уровней.</span><span class="sxs-lookup"><span data-stu-id="f8adc-127">The ending address where, in lower level storage, the higher level extent ends.</span></span> <span data-ttu-id="f8adc-128">Это свойство полезно при сопоставлении несмежных экстентов с группировкой более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="f8adc-128">This property is useful when mapping non-contiguous extents into a higher level grouping.</span></span> <span data-ttu-id="f8adc-129">Это свойство наследуется от [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="f8adc-129">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="f8adc-130">**ордериндекс**</span><span class="sxs-lookup"><span data-stu-id="f8adc-130">**OrderIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8adc-131">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8adc-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8adc-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8adc-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8adc-133">Если существует заказ на основе ассоциаций, описывающих, как собирается экстент хранения более высокого уровня, свойство **ордериндекс** указывает это.</span><span class="sxs-lookup"><span data-stu-id="f8adc-133">If there is an order to the based on associations that describe how a higher level storage extent is assembled, the **OrderIndex** property indicates this.</span></span> <span data-ttu-id="f8adc-134">Если заказ существует, экземпляры с одинаковым **зависимым** значением (в том же экстенте более высокого уровня) должны располагать уникальными значениями в свойстве **ордериндекс** .</span><span class="sxs-lookup"><span data-stu-id="f8adc-134">When an order exists, the instances with the same **Dependent** value (the same higher level extent) should place unique values in the **OrderIndex** property.</span></span> <span data-ttu-id="f8adc-135">Наименьшее значение подразумевает первый элемент коллекции экстентов нижнего уровня, а увеличение значений подразумевают последовательные члены коллекции.</span><span class="sxs-lookup"><span data-stu-id="f8adc-135">The lowest value implies the first member of the collection of lower level extents, and increasing values imply successive members of the collection.</span></span> <span data-ttu-id="f8adc-136">Если упорядоченная связь отсутствует, следует указать нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f8adc-136">If there is no ordered relationship, a value of zero should be specified.</span></span> <span data-ttu-id="f8adc-137">Примером использования этого свойства является определение чередующегося массива RAID-0 из трех дисков.</span><span class="sxs-lookup"><span data-stu-id="f8adc-137">An example of the use of this property is to define a RAID-0 striped array of three disks.</span></span> <span data-ttu-id="f8adc-138">Результирующий массив RAID — это область хранения, которая зависит от экстентов хранения, описывающих каждый из трех дисков.</span><span class="sxs-lookup"><span data-stu-id="f8adc-138">The resultant RAID array is a storage extent that is dependent on the storage extents that describe each of the three disks.</span></span> <span data-ttu-id="f8adc-139">**Ордериндекс** каждой ассоциации из экстентов диска в массив RAID можно указать как 1, 2 и 3, чтобы указать порядок, в котором экстенты дисков используются для доступа к данным RAID.</span><span class="sxs-lookup"><span data-stu-id="f8adc-139">The **OrderIndex** of each association from the disk extents to the RAID array could be specified as 1, 2, and 3 to indicate the order in which the disk extents are used to access the RAID data.</span></span> <span data-ttu-id="f8adc-140">Это свойство наследуется от [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="f8adc-140">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="f8adc-141">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="f8adc-141">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8adc-142">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8adc-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8adc-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8adc-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8adc-144">Начальный адрес, на котором начинается экстент более высокого уровня, в хранилище нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="f8adc-144">The starting address where, in lower level storage, the higher level extent begins.</span></span> <span data-ttu-id="f8adc-145">Это свойство наследуется от [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="f8adc-145">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8adc-146">Требования</span><span class="sxs-lookup"><span data-stu-id="f8adc-146">Requirements</span></span>



| <span data-ttu-id="f8adc-147">Требование</span><span class="sxs-lookup"><span data-stu-id="f8adc-147">Requirement</span></span> | <span data-ttu-id="f8adc-148">Значение</span><span class="sxs-lookup"><span data-stu-id="f8adc-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8adc-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8adc-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f8adc-150">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f8adc-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f8adc-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8adc-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f8adc-152">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f8adc-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f8adc-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f8adc-153">Namespace</span></span><br/>                | <span data-ttu-id="f8adc-154">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f8adc-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f8adc-155">MOF</span><span class="sxs-lookup"><span data-stu-id="f8adc-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8adc-156"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8adc-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8adc-157">DLL</span><span class="sxs-lookup"><span data-stu-id="f8adc-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8adc-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f8adc-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

