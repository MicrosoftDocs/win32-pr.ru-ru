---
description: Содержит сведения о физическом графическом процессоре RemoteFX.
ms.assetid: 86B47AAE-DBFF-43EF-88C6-44836D6C3AFA
title: Класс Msvm_PhysicalGPUInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PhysicalGPUInfo
- Msvm_PhysicalGPUInfo.InstanceID
- Msvm_PhysicalGPUInfo.Caption
- Msvm_PhysicalGPUInfo.Description
- Msvm_PhysicalGPUInfo.ElementName
- Msvm_PhysicalGPUInfo.Name
- Msvm_PhysicalGPUInfo.ID
- Msvm_PhysicalGPUInfo.TotalVideoMemory
- Msvm_PhysicalGPUInfo.AvailableVideoMemory
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cd4ccf65b364620e84063ea6398c59dd0e467f67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664501"
---
# <a name="msvm_physicalgpuinfo-class"></a><span data-ttu-id="93566-103">\_Класс мсвм фисикалгпуинфо</span><span class="sxs-lookup"><span data-stu-id="93566-103">Msvm\_PhysicalGPUInfo class</span></span>

<span data-ttu-id="93566-104">Содержит сведения о физическом графическом процессоре RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="93566-104">Contains information about a RemoteFX physical graphics processing unit (GPU).</span></span>

<span data-ttu-id="93566-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="93566-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="93566-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93566-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PhysicalGPUInfo : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  string ID;
  uint64 TotalVideoMemory;
  uint64 AvailableVideoMemory;
};
```

## <a name="members"></a><span data-ttu-id="93566-107">Члены</span><span class="sxs-lookup"><span data-stu-id="93566-107">Members</span></span>

<span data-ttu-id="93566-108">Класс **мсвм \_ фисикалгпуинфо** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="93566-108">The **Msvm\_PhysicalGPUInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="93566-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="93566-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93566-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="93566-110">Properties</span></span>

<span data-ttu-id="93566-111">Класс **мсвм \_ фисикалгпуинфо** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="93566-111">The **Msvm\_PhysicalGPUInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93566-112">**аваилаблевидеомемори**</span><span class="sxs-lookup"><span data-stu-id="93566-112">**AvailableVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93566-113">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93566-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93566-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93566-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93566-115">Объем неиспользуемой видеопамяти (в байтах) на физическом GPU, который может использоваться RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="93566-115">The amount of unused video memory, in bytes, on the physical GPU that can be used by RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="93566-116">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="93566-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93566-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93566-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93566-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93566-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93566-119">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="93566-119">A short description of the object.</span></span> <span data-ttu-id="93566-120">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93566-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93566-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="93566-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93566-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93566-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93566-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93566-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93566-124">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="93566-124">A description of the object.</span></span> <span data-ttu-id="93566-125">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93566-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93566-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="93566-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93566-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93566-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93566-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93566-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93566-129">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="93566-129">A display name for the object.</span></span> <span data-ttu-id="93566-130">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93566-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93566-131">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="93566-131">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93566-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93566-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93566-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93566-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93566-134">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="93566-134">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="93566-135">Уникальный идентификатор физического GPU.</span><span class="sxs-lookup"><span data-stu-id="93566-135">The unique identifier of the physical GPU.</span></span>

</dd> <dt>

<span data-ttu-id="93566-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="93566-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93566-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93566-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93566-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93566-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93566-139">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="93566-139">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="93566-140">Строка, уникально идентифицирующая экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="93566-140">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="93566-141">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93566-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93566-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="93566-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93566-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93566-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93566-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93566-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93566-145">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="93566-145">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="93566-146">Отображаемое имя физического GPU.</span><span class="sxs-lookup"><span data-stu-id="93566-146">The display name of the physical GPU.</span></span>

</dd> <dt>

<span data-ttu-id="93566-147">**тоталвидеомемори**</span><span class="sxs-lookup"><span data-stu-id="93566-147">**TotalVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93566-148">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93566-148">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93566-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93566-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93566-150">Общий объем видеопамяти в байтах на физическом GPU, который может использоваться RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="93566-150">The total amount of video memory, in bytes, on the physical GPU that can be used by RemoteFX.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93566-151">Требования</span><span class="sxs-lookup"><span data-stu-id="93566-151">Requirements</span></span>



| <span data-ttu-id="93566-152">Требование</span><span class="sxs-lookup"><span data-stu-id="93566-152">Requirement</span></span> | <span data-ttu-id="93566-153">Значение</span><span class="sxs-lookup"><span data-stu-id="93566-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93566-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93566-154">Minimum supported client</span></span><br/> | <span data-ttu-id="93566-155">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="93566-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="93566-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93566-156">Minimum supported server</span></span><br/> | <span data-ttu-id="93566-157">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="93566-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93566-158">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="93566-158">Namespace</span></span><br/>                | <span data-ttu-id="93566-159">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="93566-159">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="93566-160">MOF</span><span class="sxs-lookup"><span data-stu-id="93566-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93566-161"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93566-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93566-162">DLL</span><span class="sxs-lookup"><span data-stu-id="93566-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93566-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93566-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="93566-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93566-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93566-165">**\_МАНАЖЕДЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="93566-165">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

