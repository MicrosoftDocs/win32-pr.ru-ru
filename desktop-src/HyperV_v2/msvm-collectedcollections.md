---
description: Связывает виртуалсистемколлектион Мсвм \_ с содержащимися в \_ них объектами мсвм ComputerSystem.
ms.assetid: bbf7713a-b331-4b40-bcb4-3545c26c6f3a
title: Класс Msvm_CollectedCollections
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedCollections
- Msvm_CollectedCollections.Collection
- Msvm_CollectedCollections.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16ec6ad77c44e0a4e9001a0cb77d227573635ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664684"
---
# <a name="msvm_collectedcollections-class"></a><span data-ttu-id="d9d4f-103">\_Класс мсвм коллектедколлектионс</span><span class="sxs-lookup"><span data-stu-id="d9d4f-103">Msvm\_CollectedCollections class</span></span>

<span data-ttu-id="d9d4f-104">Связывает [**\_ виртуалсистемколлектион мсвм**](msvm-virtualsystemcollection.md) с содержащимися в них объектами [**мсвм \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="d9d4f-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="d9d4f-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d9d4f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9d4f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9d4f-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedCollections : CIM_CollectedMSEs
{
  Msvm_ManagementCollection REF Collection;
  CIM_CollectionOfMSEs      REF Member;
};
```

## <a name="members"></a><span data-ttu-id="d9d4f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d9d4f-107">Members</span></span>

<span data-ttu-id="d9d4f-108">Класс **мсвм \_ коллектедколлектионс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d9d4f-108">The **Msvm\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="d9d4f-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="d9d4f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d9d4f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d9d4f-110">Properties</span></span>

<span data-ttu-id="d9d4f-111">Класс **мсвм \_ коллектедколлектионс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d9d4f-111">The **Msvm\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d9d4f-112">**Коллекция**</span><span class="sxs-lookup"><span data-stu-id="d9d4f-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9d4f-113">Тип данных: **мсвм \_ манажементколлектион**</span><span class="sxs-lookup"><span data-stu-id="d9d4f-113">Data type: **Msvm\_ManagementCollection**</span></span>
</dt> <dt>

<span data-ttu-id="d9d4f-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9d4f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9d4f-115">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="d9d4f-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="d9d4f-116">Объект [**мсвм \_ манажементколлектион**](msvm-managementcollection.md) GROUPING или "сумка", представляющий коллекцию.</span><span class="sxs-lookup"><span data-stu-id="d9d4f-116">An [**Msvm\_ManagementCollection**](msvm-managementcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="d9d4f-117">**Член**</span><span class="sxs-lookup"><span data-stu-id="d9d4f-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9d4f-118">Тип данных: **CIM \_ коллектионофмсес**</span><span class="sxs-lookup"><span data-stu-id="d9d4f-118">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="d9d4f-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9d4f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9d4f-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("член")</span><span class="sxs-lookup"><span data-stu-id="d9d4f-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="d9d4f-121">[**\_ Коллектионофмсес CIM**](cim-collectionofmses.md) , содержащий элементы коллекции.</span><span class="sxs-lookup"><span data-stu-id="d9d4f-121">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9d4f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d9d4f-122">Requirements</span></span>



| <span data-ttu-id="d9d4f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d9d4f-123">Requirement</span></span> | <span data-ttu-id="d9d4f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d9d4f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9d4f-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9d4f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d9d4f-126">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d9d4f-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d9d4f-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9d4f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d9d4f-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d9d4f-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d9d4f-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d9d4f-129">Namespace</span></span><br/>                | <span data-ttu-id="d9d4f-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d9d4f-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d9d4f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d9d4f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9d4f-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9d4f-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9d4f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d9d4f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9d4f-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d9d4f-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d9d4f-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9d4f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9d4f-136">**\_КОЛЛЕКТЕДМСЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="d9d4f-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

