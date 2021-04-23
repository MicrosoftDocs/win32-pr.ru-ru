---
description: Представляет связь между объектом CIM сторажеекстент более высокого уровня \_ и объектом CIM сторажеекстент более низкого уровня \_ . Например, объект CIM \_ протектедспацеекстент является частью \_ объекта фисикалекстент CIM.
ms.assetid: 40a88927-981b-4fc4-af5f-be91d9933284
title: Класс CIM_BasedOn (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Antecedent
- CIM_BasedOn.Dependent
- CIM_BasedOn.StartingAddress
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47d2e44d1106eba57f4c46c0957662c348c9ca1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897233"
---
# <a name="cim_basedon-class-hyper-v-management"></a><span data-ttu-id="9c09f-104">Класс CIM_BasedOn (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="9c09f-104">CIM_BasedOn class (Hyper-V management)</span></span>

<span data-ttu-id="9c09f-105">Представляет связь между объектом **CIM \_ сторажеекстент** более высокого уровня и объектом **CIM \_ сторажеекстент** более низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="9c09f-105">Represents an association between a higher level **CIM\_StorageExtent** object and a lower level **CIM\_StorageExtent** object.</span></span> <span data-ttu-id="9c09f-106">Например, объект [**CIM \_ протектедспацеекстент**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) является частью объекта [**\_ фисикалекстент CIM**](/windows/desktop/CIMWin32Prov/cim-physicalextent) .</span><span class="sxs-lookup"><span data-stu-id="9c09f-106">For example a [**CIM\_ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) object is a part of a [**CIM\_PhysicalExtent**](/windows/desktop/CIMWin32Prov/cim-physicalextent) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c09f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c09f-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a><span data-ttu-id="9c09f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9c09f-108">Members</span></span>

<span data-ttu-id="9c09f-109">Класс **CIM \_ BasedOn** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9c09f-109">The **CIM\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="9c09f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c09f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c09f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c09f-111">Properties</span></span>

<span data-ttu-id="9c09f-112">Класс **CIM \_ BasedOn** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9c09f-112">The **CIM\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c09f-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="9c09f-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c09f-114">Тип данных: **CIM \_ сторажеекстент**</span><span class="sxs-lookup"><span data-stu-id="9c09f-114">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="9c09f-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c09f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c09f-116">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="9c09f-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="9c09f-117">Объект **CIM \_ сторажеекстент** нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="9c09f-117">The lower level **CIM\_StorageExtent** object.</span></span>

</dd> <dt>

<span data-ttu-id="9c09f-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="9c09f-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c09f-119">Тип данных: **CIM \_ сторажеекстент**</span><span class="sxs-lookup"><span data-stu-id="9c09f-119">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="9c09f-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c09f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c09f-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="9c09f-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9c09f-122">Объект **CIM \_ сторажеекстент** более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="9c09f-122">The higher level **CIM\_StorageExtent** object.</span></span>

</dd> <dt>

<span data-ttu-id="9c09f-123">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="9c09f-123">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c09f-124">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c09f-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c09f-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c09f-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c09f-126">Адрес, указывающий, где в хранилище нижнего уровня заканчивается объект **CIM \_ сторажеекстент** более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="9c09f-126">The address that indicates where in lower level storage, the higher level **CIM\_StorageExtent** object ends.</span></span> <span data-ttu-id="9c09f-127">Это свойство полезно при сопоставлении несмежных объектов **CIM \_ сторажеекстент** с группировкой более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="9c09f-127">This property is useful when mapping non-contiguous **CIM\_StorageExtent** objects into a higher level grouping.</span></span>

</dd> <dt>

<span data-ttu-id="9c09f-128">**ордериндекс**</span><span class="sxs-lookup"><span data-stu-id="9c09f-128">**OrderIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c09f-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c09f-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c09f-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c09f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c09f-131">Индекс, который используется для указания порядка сопоставлений **CIM \_ BasedOn** в коллекции; в противном случае — значение 0 указывает на отсутствие порядка.</span><span class="sxs-lookup"><span data-stu-id="9c09f-131">An index that is used to specify the order of **CIM\_BasedOn** associations in a collection; otherwise "0" indicates no order.</span></span> <span data-ttu-id="9c09f-132">**Модель CIM \_ Экземпляры BasedOn** с одинаковым зависимым значением должны располагать уникальными значениями в свойстве **ордериндекс** .</span><span class="sxs-lookup"><span data-stu-id="9c09f-132">**CIM\_BasedOn** instances with the same dependent value should place unique values in the **OrderIndex** property.</span></span> <span data-ttu-id="9c09f-133">Наименьшее значение **ордериндекс** указывает первый элемент коллекции.</span><span class="sxs-lookup"><span data-stu-id="9c09f-133">The lowest **OrderIndex** value specifies the first member of the collection.</span></span>

<span data-ttu-id="9c09f-134">Примером использования этого свойства является определение чередующегося массива RAID-0 из 3 дисков.</span><span class="sxs-lookup"><span data-stu-id="9c09f-134">An example of the use of this property is to define a RAID-0 striped array of 3 disks.</span></span> <span data-ttu-id="9c09f-135">Результирующий массив RAID — это область хранения, которая зависит от экстентов хранения, описывающих каждый из трех дисков.</span><span class="sxs-lookup"><span data-stu-id="9c09f-135">The resultant RAID array is a storage extent that is dependent on the storage extents that describe each of the 3 disks.</span></span> <span data-ttu-id="9c09f-136">Значение **ордериндекс** каждой ассоциации **CIM \_ BasedOn** из ЭКСТЕНТов диска в массив RAID можно указать как 1, 2 и 3, чтобы указать порядок, в котором экстенты дисков используются для доступа к данным RAID.</span><span class="sxs-lookup"><span data-stu-id="9c09f-136">The **OrderIndex** value of each **CIM\_BasedOn** association from the disk extents to the RAID array could be specified as 1, 2, and 3 to indicate the order in which the disk extents are used to access the RAID data.</span></span>

</dd> <dt>

<span data-ttu-id="9c09f-137">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="9c09f-137">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c09f-138">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c09f-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c09f-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c09f-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c09f-140">Адрес, который указывает, где в хранилище нижнего уровня начинается объект **CIM \_ сторажеекстент** высшего уровня.</span><span class="sxs-lookup"><span data-stu-id="9c09f-140">The address that indicates where in lower level storage, the higher level **CIM\_StorageExtent** object begins.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c09f-141">Требования</span><span class="sxs-lookup"><span data-stu-id="9c09f-141">Requirements</span></span>



| <span data-ttu-id="9c09f-142">Требование</span><span class="sxs-lookup"><span data-stu-id="9c09f-142">Requirement</span></span> | <span data-ttu-id="9c09f-143">Значение</span><span class="sxs-lookup"><span data-stu-id="9c09f-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c09f-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c09f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9c09f-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9c09f-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9c09f-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c09f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9c09f-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c09f-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9c09f-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9c09f-148">Namespace</span></span><br/>                | <span data-ttu-id="9c09f-149">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9c09f-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9c09f-150">MOF</span><span class="sxs-lookup"><span data-stu-id="9c09f-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c09f-151"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c09f-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c09f-152">DLL</span><span class="sxs-lookup"><span data-stu-id="9c09f-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c09f-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9c09f-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9c09f-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c09f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c09f-155">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="9c09f-155">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

