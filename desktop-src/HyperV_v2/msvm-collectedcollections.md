---
description: Msvm_CollectedCollections класс — связывает виртуалсистемколлектион Мсвм \_ с содержащимися в \_ них объектами мсвм ComputerSystem.
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
ms.openlocfilehash: 83719d364fac22923d68206c8cfe7d37adad5edb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112132"
---
# <a name="msvm_collectedcollections-class"></a><span data-ttu-id="15155-103">\_Класс мсвм коллектедколлектионс</span><span class="sxs-lookup"><span data-stu-id="15155-103">Msvm\_CollectedCollections class</span></span>

<span data-ttu-id="15155-104">Связывает [**\_ виртуалсистемколлектион мсвм**](msvm-virtualsystemcollection.md) с содержащимися в них объектами [**мсвм \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="15155-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="15155-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="15155-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="15155-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15155-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedCollections : CIM_CollectedMSEs
{
  Msvm_ManagementCollection REF Collection;
  CIM_CollectionOfMSEs      REF Member;
};
```

## <a name="members"></a><span data-ttu-id="15155-107">Члены</span><span class="sxs-lookup"><span data-stu-id="15155-107">Members</span></span>

<span data-ttu-id="15155-108">Класс **мсвм \_ коллектедколлектионс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="15155-108">The **Msvm\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="15155-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="15155-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15155-110">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="15155-110">Properties</span></span>

<span data-ttu-id="15155-111">Класс **мсвм \_ коллектедколлектионс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="15155-111">The **Msvm\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15155-112">**Коллекция**</span><span class="sxs-lookup"><span data-stu-id="15155-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15155-113">Тип данных: **мсвм \_ манажементколлектион**</span><span class="sxs-lookup"><span data-stu-id="15155-113">Data type: **Msvm\_ManagementCollection**</span></span>
</dt> <dt>

<span data-ttu-id="15155-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15155-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15155-115">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="15155-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="15155-116">Объект [**мсвм \_ манажементколлектион**](msvm-managementcollection.md) GROUPING или "сумка", представляющий коллекцию.</span><span class="sxs-lookup"><span data-stu-id="15155-116">An [**Msvm\_ManagementCollection**](msvm-managementcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="15155-117">**Член**</span><span class="sxs-lookup"><span data-stu-id="15155-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15155-118">Тип данных: **CIM \_ коллектионофмсес**</span><span class="sxs-lookup"><span data-stu-id="15155-118">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="15155-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15155-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15155-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("член")</span><span class="sxs-lookup"><span data-stu-id="15155-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="15155-121">[**\_ Коллектионофмсес CIM**](cim-collectionofmses.md) , содержащий элементы коллекции.</span><span class="sxs-lookup"><span data-stu-id="15155-121">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15155-122">Требования</span><span class="sxs-lookup"><span data-stu-id="15155-122">Requirements</span></span>



| <span data-ttu-id="15155-123">Требование</span><span class="sxs-lookup"><span data-stu-id="15155-123">Requirement</span></span> | <span data-ttu-id="15155-124">Значение</span><span class="sxs-lookup"><span data-stu-id="15155-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15155-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15155-125">Minimum supported client</span></span><br/> | <span data-ttu-id="15155-126">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="15155-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="15155-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15155-127">Minimum supported server</span></span><br/> | <span data-ttu-id="15155-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="15155-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="15155-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="15155-129">Namespace</span></span><br/>                | <span data-ttu-id="15155-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="15155-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="15155-131">MOF</span><span class="sxs-lookup"><span data-stu-id="15155-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15155-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15155-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15155-133">DLL</span><span class="sxs-lookup"><span data-stu-id="15155-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15155-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15155-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="15155-135">См. также</span><span class="sxs-lookup"><span data-stu-id="15155-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15155-136">**\_КОЛЛЕКТЕДМСЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="15155-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

