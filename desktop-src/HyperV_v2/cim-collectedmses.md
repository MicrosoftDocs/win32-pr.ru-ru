---
description: Представляет универсальную связь между коллекцией управляемых системных элементов и элементами коллекции.
ms.assetid: c9e2bbca-67be-41f2-a94c-cf4eaf5f4694
title: Класс CIM_CollectedMSEs (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdf5c5d682f1b6e1b47b64100b3e00f5f79cebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663998"
---
# <a name="cim_collectedmses-class-hyper-v-management"></a><span data-ttu-id="ab056-103">Класс CIM_CollectedMSEs (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="ab056-103">CIM_CollectedMSEs class (Hyper-V management)</span></span>

<span data-ttu-id="ab056-104">Представляет универсальную связь между коллекцией управляемых системных элементов и элементами коллекции.</span><span class="sxs-lookup"><span data-stu-id="ab056-104">Represents a generic association between a collection of managed system elements and the members of the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab056-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab056-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectedMSEs : CIM_MemberOfCollection
{
  CIM_CollectionOfMSEs     REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="ab056-106">Члены</span><span class="sxs-lookup"><span data-stu-id="ab056-106">Members</span></span>

<span data-ttu-id="ab056-107">Класс **CIM \_ коллектедмсес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ab056-107">The **CIM\_CollectedMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="ab056-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="ab056-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab056-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ab056-109">Properties</span></span>

<span data-ttu-id="ab056-110">Класс **CIM \_ коллектедмсес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ab056-110">The **CIM\_CollectedMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab056-111">**Коллекция**</span><span class="sxs-lookup"><span data-stu-id="ab056-111">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab056-112">Тип данных: **CIM \_ коллектионофмсес**</span><span class="sxs-lookup"><span data-stu-id="ab056-112">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="ab056-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab056-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab056-114">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="ab056-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="ab056-115">Коллекция.</span><span class="sxs-lookup"><span data-stu-id="ab056-115">The collection.</span></span>

</dd> <dt>

<span data-ttu-id="ab056-116">**Член**</span><span class="sxs-lookup"><span data-stu-id="ab056-116">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab056-117">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="ab056-117">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="ab056-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab056-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab056-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("член")</span><span class="sxs-lookup"><span data-stu-id="ab056-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="ab056-120">Элементы коллекции.</span><span class="sxs-lookup"><span data-stu-id="ab056-120">The members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab056-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ab056-121">Requirements</span></span>



| <span data-ttu-id="ab056-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ab056-122">Requirement</span></span> | <span data-ttu-id="ab056-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ab056-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab056-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab056-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ab056-125">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ab056-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ab056-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab056-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ab056-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ab056-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ab056-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ab056-128">Namespace</span></span><br/>                | <span data-ttu-id="ab056-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ab056-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ab056-130">MOF</span><span class="sxs-lookup"><span data-stu-id="ab056-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab056-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab056-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab056-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ab056-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab056-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ab056-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ab056-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab056-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab056-135">**\_МЕМБЕРОФКОЛЛЕКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ab056-135">**CIM\_MemberOfCollection**</span></span>](cim-memberofcollection.md)
</dt> </dl>

 

