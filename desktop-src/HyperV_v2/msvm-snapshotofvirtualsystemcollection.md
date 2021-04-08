---
description: Связывает снапшотколлектион Мсвм \_ с соответствующими \_ объектами мсвм виртуалсистемколлектион.
ms.assetid: 4dbfe21f-e700-4266-aedb-236c57c424f6
title: Класс Msvm_SnapshotOfVirtualSystemCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystemCollection
- Msvm_SnapshotOfVirtualSystemCollection.Antecedent
- Msvm_SnapshotOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae3c9c146cea8a8af98f4d3071ee7339d53eb6b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898329"
---
# <a name="msvm_snapshotofvirtualsystemcollection-class"></a><span data-ttu-id="c986c-103">\_Класс мсвм снапшотофвиртуалсистемколлектион</span><span class="sxs-lookup"><span data-stu-id="c986c-103">Msvm\_SnapshotOfVirtualSystemCollection class</span></span>

<span data-ttu-id="c986c-104">Связывает [**\_ снапшотколлектион мсвм**](msvm-snapshotcollection.md) с соответствующими объектами [**мсвм \_ виртуалсистемколлектион**](msvm-virtualsystemcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="c986c-104">Associates the [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) to the corresponding [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) objects.</span></span>

<span data-ttu-id="c986c-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c986c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c986c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c986c-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c986c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c986c-107">Members</span></span>

<span data-ttu-id="c986c-108">Класс **мсвм \_ снапшотофвиртуалсистемколлектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c986c-108">The **Msvm\_SnapshotOfVirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="c986c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c986c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c986c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c986c-110">Properties</span></span>

<span data-ttu-id="c986c-111">Класс **мсвм \_ снапшотофвиртуалсистемколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c986c-111">The **Msvm\_SnapshotOfVirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c986c-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="c986c-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c986c-113">Тип данных: **CIM \_ коллектионофмсес**</span><span class="sxs-lookup"><span data-stu-id="c986c-113">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="c986c-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c986c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c986c-115">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="c986c-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c986c-116">[**\_ Коллектионофмсес CIM**](cim-collectionofmses.md) , представляющий независимый объект в этой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="c986c-116">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="c986c-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="c986c-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c986c-118">Тип данных: **\_ коллекция CIM**</span><span class="sxs-lookup"><span data-stu-id="c986c-118">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="c986c-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c986c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c986c-120">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="c986c-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c986c-121">[**\_ Коллекция CIM**](cim-collection.md) , представляющая объект, который зависит от **предшествующей задачи.**</span><span class="sxs-lookup"><span data-stu-id="c986c-121">A [**CIM\_Collection**](cim-collection.md) that represents the object that is dependent on the **Antecedent.**</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c986c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c986c-122">Requirements</span></span>



| <span data-ttu-id="c986c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c986c-123">Requirement</span></span> | <span data-ttu-id="c986c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c986c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c986c-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c986c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c986c-126">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c986c-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c986c-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c986c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c986c-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c986c-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c986c-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c986c-129">Namespace</span></span><br/>                | <span data-ttu-id="c986c-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c986c-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c986c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c986c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c986c-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c986c-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c986c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c986c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c986c-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c986c-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c986c-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c986c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c986c-136">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="c986c-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

