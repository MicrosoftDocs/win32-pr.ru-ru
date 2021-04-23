---
description: Связывает диск хранилища с носителем, вставленным в диск.
ms.assetid: C0B2D604-0B55-4EA0-A46E-2450D89A5B22
title: Класс Msvm_MediaPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MediaPresent
- Msvm_MediaPresent.Antecedent
- Msvm_MediaPresent.Dependent
- Msvm_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57d46fb711ab8d4abcf27966e6ec92ed2287bc3e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914211"
---
# <a name="msvm_mediapresent-class"></a><span data-ttu-id="e7e1c-103">\_Класс мсвм медиапресент</span><span class="sxs-lookup"><span data-stu-id="e7e1c-103">Msvm\_MediaPresent class</span></span>

<span data-ttu-id="e7e1c-104">Связывает диск хранилища с носителем, вставленным в диск.</span><span class="sxs-lookup"><span data-stu-id="e7e1c-104">Associates a storage drive with the media inserted into the drive.</span></span> <span data-ttu-id="e7e1c-105">Эта ассоциация используется для всех объектов дисков хранилища.</span><span class="sxs-lookup"><span data-stu-id="e7e1c-105">This association is used for all storage drive objects.</span></span>

<span data-ttu-id="e7e1c-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e7e1c-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7e1c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7e1c-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MediaPresent : CIM_MediaPresent
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a><span data-ttu-id="e7e1c-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e7e1c-108">Members</span></span>

<span data-ttu-id="e7e1c-109">Класс **мсвм \_ медиапресент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e7e1c-109">The **Msvm\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="e7e1c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e7e1c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7e1c-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e7e1c-111">Properties</span></span>

<span data-ttu-id="e7e1c-112">Класс **мсвм \_ медиапресент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e7e1c-112">The **Msvm\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7e1c-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="e7e1c-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7e1c-114">Тип данных: **[ **CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**</span><span class="sxs-lookup"><span data-stu-id="e7e1c-114">Data type: **[**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**</span></span>
</dt> <dt>

<span data-ttu-id="e7e1c-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e7e1c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7e1c-116">Ссылка на устройство доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="e7e1c-116">The reference to the media access device.</span></span> <span data-ttu-id="e7e1c-117">Это свойство наследуется от [**CIM \_ медиапресент**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span><span class="sxs-lookup"><span data-stu-id="e7e1c-117">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> <dt>

<span data-ttu-id="e7e1c-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="e7e1c-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7e1c-119">Тип данных: **[ **CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="e7e1c-119">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="e7e1c-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e7e1c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7e1c-121">Ссылка на экстент хранилища, к которому осуществляется доступ с помощью устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="e7e1c-121">The reference to the storage extent accessed with the media access device.</span></span> <span data-ttu-id="e7e1c-122">Это свойство наследуется от [**CIM \_ медиапресент**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span><span class="sxs-lookup"><span data-stu-id="e7e1c-122">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> <dt>

<span data-ttu-id="e7e1c-123">**фикседмедиа**</span><span class="sxs-lookup"><span data-stu-id="e7e1c-123">**FixedMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7e1c-124">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e7e1c-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e7e1c-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e7e1c-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7e1c-126">Указывает, является ли доступная область хранилища фиксированной и не может быть извлечена.</span><span class="sxs-lookup"><span data-stu-id="e7e1c-126">Indicates whether the accessed storage extent is fixed and cannot be ejected.</span></span> <span data-ttu-id="e7e1c-127">Значение **true** для жестких дисков и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e7e1c-127">The value is **True** for hard disks and **False** otherwise.</span></span> <span data-ttu-id="e7e1c-128">Это свойство наследуется от [**CIM \_ медиапресент**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span><span class="sxs-lookup"><span data-stu-id="e7e1c-128">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7e1c-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7e1c-129">Remarks</span></span>

<span data-ttu-id="e7e1c-130">Доступ к классу **\_ медиапресент мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="e7e1c-130">Access to the **Msvm\_MediaPresent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e7e1c-131">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e7e1c-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7e1c-132">Требования</span><span class="sxs-lookup"><span data-stu-id="e7e1c-132">Requirements</span></span>



| <span data-ttu-id="e7e1c-133">Требование</span><span class="sxs-lookup"><span data-stu-id="e7e1c-133">Requirement</span></span> | <span data-ttu-id="e7e1c-134">Значение</span><span class="sxs-lookup"><span data-stu-id="e7e1c-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e1c-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7e1c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e7e1c-136">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e7e1c-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e7e1c-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7e1c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e7e1c-138">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e7e1c-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e7e1c-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e7e1c-139">Namespace</span></span><br/>                | <span data-ttu-id="e7e1c-140">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e7e1c-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e7e1c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="e7e1c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7e1c-142"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7e1c-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7e1c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e7e1c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7e1c-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e7e1c-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e7e1c-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7e1c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7e1c-146">**\_МЕДИАПРЕСЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="e7e1c-146">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dt>

[<span data-ttu-id="e7e1c-147">**\_МЕДИАПРЕСЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="e7e1c-147">**CIM\_MediaPresent**</span></span>](/windows/desktop/CIMWin32Prov/cim-mediapresent)
</dt> <dt>

[<span data-ttu-id="e7e1c-148">Классы хранения</span><span class="sxs-lookup"><span data-stu-id="e7e1c-148">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

