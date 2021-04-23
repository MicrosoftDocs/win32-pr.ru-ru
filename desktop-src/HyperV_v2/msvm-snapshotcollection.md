---
description: Представляет коллекцию моментальных снимков виртуальных систем.
ms.assetid: c9b64421-232c-4f32-a088-6b98602ca3f4
title: Класс Msvm_SnapshotCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotCollection
- Msvm_SnapshotCollection.CollectionID
- Msvm_SnapshotCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e24566f1f5c5500258f14f88cbe2b7c4fa29e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155539"
---
# <a name="msvm_snapshotcollection-class"></a><span data-ttu-id="816b1-103">\_Класс мсвм снапшотколлектион</span><span class="sxs-lookup"><span data-stu-id="816b1-103">Msvm\_SnapshotCollection class</span></span>

<span data-ttu-id="816b1-104">Представляет коллекцию моментальных снимков виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="816b1-104">Represents a collection of virtual system snapshots.</span></span>

<span data-ttu-id="816b1-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="816b1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="816b1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="816b1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotCollection : CIM_Collection
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="816b1-107">Члены</span><span class="sxs-lookup"><span data-stu-id="816b1-107">Members</span></span>

<span data-ttu-id="816b1-108">Класс **мсвм \_ снапшотколлектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="816b1-108">The **Msvm\_SnapshotCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="816b1-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="816b1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="816b1-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="816b1-110">Properties</span></span>

<span data-ttu-id="816b1-111">Класс **мсвм \_ снапшотколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="816b1-111">The **Msvm\_SnapshotCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="816b1-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="816b1-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="816b1-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="816b1-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="816b1-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="816b1-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="816b1-115">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="816b1-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="816b1-116">Уникальная идентификация объекта коллекции.</span><span class="sxs-lookup"><span data-stu-id="816b1-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="816b1-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="816b1-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="816b1-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="816b1-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="816b1-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="816b1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="816b1-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="816b1-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="816b1-121">Определяемое пользователем имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="816b1-121">An user-defined name for the collection.</span></span> <span data-ttu-id="816b1-122">Обратите внимание, что это не обязательно должно быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="816b1-122">Note this is not guaranteed to be unique.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="816b1-123">Требования</span><span class="sxs-lookup"><span data-stu-id="816b1-123">Requirements</span></span>



| <span data-ttu-id="816b1-124">Требование</span><span class="sxs-lookup"><span data-stu-id="816b1-124">Requirement</span></span> | <span data-ttu-id="816b1-125">Значение</span><span class="sxs-lookup"><span data-stu-id="816b1-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="816b1-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="816b1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="816b1-127">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="816b1-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="816b1-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="816b1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="816b1-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="816b1-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="816b1-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="816b1-130">Namespace</span></span><br/>                | <span data-ttu-id="816b1-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="816b1-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="816b1-132">MOF</span><span class="sxs-lookup"><span data-stu-id="816b1-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="816b1-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="816b1-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="816b1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="816b1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="816b1-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="816b1-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="816b1-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="816b1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="816b1-137">**\_Коллекция CIM**</span><span class="sxs-lookup"><span data-stu-id="816b1-137">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

