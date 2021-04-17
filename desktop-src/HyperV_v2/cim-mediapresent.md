---
description: Представляет связь, в которой доступ к экстенту хранения должен осуществляться через устройство доступа к носителю.
ms.assetid: 436a7e2d-2c14-4058-aca0-669373b8004a
title: Класс CIM_MediaPresent (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Antecedent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0e26c36231edaf3ca4b8accf844a3c58b3d70bc7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105664797"
---
# <a name="cim_mediapresent-class-hyper-v-management"></a><span data-ttu-id="53d27-103">Класс CIM_MediaPresent (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="53d27-103">CIM_MediaPresent class (Hyper-V management)</span></span>

<span data-ttu-id="53d27-104">Представляет связь, в которой доступ к экстенту хранения должен осуществляться через устройство доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="53d27-104">Represents a relationship in which a storage extent must be accessed through a media access device.</span></span>

## <a name="syntax"></a><span data-ttu-id="53d27-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53d27-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageExtents"), MappingStrings("MIF.DMTF|Storage Devices|001.8"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a><span data-ttu-id="53d27-106">Члены</span><span class="sxs-lookup"><span data-stu-id="53d27-106">Members</span></span>

<span data-ttu-id="53d27-107">Класс **CIM \_ медиапресент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="53d27-107">The **CIM\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="53d27-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="53d27-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53d27-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="53d27-109">Properties</span></span>

<span data-ttu-id="53d27-110">Класс **CIM \_ медиапресент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="53d27-110">The **CIM\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53d27-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="53d27-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d27-112">Тип данных: **CIM \_ медиаакцессдевице**</span><span class="sxs-lookup"><span data-stu-id="53d27-112">Data type: **CIM\_MediaAccessDevice**</span></span>
</dt> <dt>

<span data-ttu-id="53d27-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53d27-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d27-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="53d27-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="53d27-115">Устройство доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="53d27-115">The media access device.</span></span>

</dd> <dt>

<span data-ttu-id="53d27-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="53d27-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d27-117">Тип данных: **CIM \_ сторажеекстент**</span><span class="sxs-lookup"><span data-stu-id="53d27-117">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="53d27-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53d27-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d27-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="53d27-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="53d27-120">Область хранения, доступ к которой осуществляется при использовании устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="53d27-120">The storage extent that is accessed when using the media access device.</span></span>

</dd> <dt>

<span data-ttu-id="53d27-121">**фикседмедиа**</span><span class="sxs-lookup"><span data-stu-id="53d27-121">**FixedMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d27-122">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="53d27-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="53d27-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53d27-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53d27-124">**значение true** , если экстент хранения зафиксирован на устройстве доступа к носителю и не может быть извлечен. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="53d27-124">**true** if the storage extent is fixed in the media access device and can not be ejected; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53d27-125">Требования</span><span class="sxs-lookup"><span data-stu-id="53d27-125">Requirements</span></span>



| <span data-ttu-id="53d27-126">Требование</span><span class="sxs-lookup"><span data-stu-id="53d27-126">Requirement</span></span> | <span data-ttu-id="53d27-127">Значение</span><span class="sxs-lookup"><span data-stu-id="53d27-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53d27-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53d27-128">Minimum supported client</span></span><br/> | <span data-ttu-id="53d27-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="53d27-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="53d27-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53d27-130">Minimum supported server</span></span><br/> | <span data-ttu-id="53d27-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53d27-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="53d27-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="53d27-132">Namespace</span></span><br/>                | <span data-ttu-id="53d27-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="53d27-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="53d27-134">MOF</span><span class="sxs-lookup"><span data-stu-id="53d27-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53d27-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53d27-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="53d27-136">DLL</span><span class="sxs-lookup"><span data-stu-id="53d27-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53d27-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53d27-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="53d27-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53d27-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53d27-139">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="53d27-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

