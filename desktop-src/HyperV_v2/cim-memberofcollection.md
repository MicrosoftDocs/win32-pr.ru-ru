---
description: Представляет связь, в которой управляемый элемент является членом и обрабатывается коллекцией.
ms.assetid: 324284fa-ece6-41df-9891-040a7561dce4
title: Класс CIM_MemberOfCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemberOfCollection
- CIM_MemberOfCollection.Collection
- CIM_MemberOfCollection.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9bcebfb08cbbc0cb18e00f1b0e5e2646ca086faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081079"
---
# <a name="cim_memberofcollection-class"></a><span data-ttu-id="859f7-103">\_Класс CIM мемберофколлектион</span><span class="sxs-lookup"><span data-stu-id="859f7-103">CIM\_MemberOfCollection class</span></span>

<span data-ttu-id="859f7-104">Представляет связь, в которой управляемый элемент является членом и обрабатывается коллекцией.</span><span class="sxs-lookup"><span data-stu-id="859f7-104">Represents a relationship in which a managed element is a member of and is aggregated by a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="859f7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="859f7-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_MemberOfCollection
{
  CIM_Collection     REF Collection;
  CIM_ManagedElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="859f7-106">Члены</span><span class="sxs-lookup"><span data-stu-id="859f7-106">Members</span></span>

<span data-ttu-id="859f7-107">Класс **CIM \_ мемберофколлектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="859f7-107">The **CIM\_MemberOfCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="859f7-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="859f7-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="859f7-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="859f7-109">Properties</span></span>

<span data-ttu-id="859f7-110">Класс **CIM \_ мемберофколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="859f7-110">The **CIM\_MemberOfCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="859f7-111">**Коллекция**</span><span class="sxs-lookup"><span data-stu-id="859f7-111">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="859f7-112">Тип данных: **\_ коллекция CIM**</span><span class="sxs-lookup"><span data-stu-id="859f7-112">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="859f7-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="859f7-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="859f7-114">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**агрегатная функция**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="859f7-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="859f7-115">Коллекция, которая выполняет статистическую обработку элементов.</span><span class="sxs-lookup"><span data-stu-id="859f7-115">The collection that aggregates members.</span></span>

</dd> <dt>

<span data-ttu-id="859f7-116">**Член**</span><span class="sxs-lookup"><span data-stu-id="859f7-116">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="859f7-117">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="859f7-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="859f7-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="859f7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="859f7-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="859f7-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="859f7-120">Элемент коллекции.</span><span class="sxs-lookup"><span data-stu-id="859f7-120">The member of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="859f7-121">Требования</span><span class="sxs-lookup"><span data-stu-id="859f7-121">Requirements</span></span>



| <span data-ttu-id="859f7-122">Требование</span><span class="sxs-lookup"><span data-stu-id="859f7-122">Requirement</span></span> | <span data-ttu-id="859f7-123">Значение</span><span class="sxs-lookup"><span data-stu-id="859f7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="859f7-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="859f7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="859f7-125">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="859f7-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="859f7-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="859f7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="859f7-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="859f7-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="859f7-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="859f7-128">Namespace</span></span><br/>                | <span data-ttu-id="859f7-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="859f7-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="859f7-130">MOF</span><span class="sxs-lookup"><span data-stu-id="859f7-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="859f7-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="859f7-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="859f7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="859f7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="859f7-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="859f7-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

