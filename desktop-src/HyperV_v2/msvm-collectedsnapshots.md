---
description: Связывает снапшотколлектион Мсвм \_ с содержащимися в \_ них объектами мсвм виртуалсистемсеттингдата.
ms.assetid: 21005e8a-0bc6-4ea7-8f6f-d79803b43bc0
title: Класс Msvm_CollectedSnapshots
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedSnapshots
- Msvm_CollectedSnapshots.Collection
- Msvm_CollectedSnapshots.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9c89e7c7390cc1f2cc0c3217fca93e3f2d2d01ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662663"
---
# <a name="msvm_collectedsnapshots-class"></a><span data-ttu-id="f8c84-103">\_Класс мсвм коллектедснапшотс</span><span class="sxs-lookup"><span data-stu-id="f8c84-103">Msvm\_CollectedSnapshots class</span></span>

<span data-ttu-id="f8c84-104">Связывает [**\_ снапшотколлектион мсвм**](msvm-snapshotcollection.md) с содержащимися в них объектами [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="f8c84-104">Associates the [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) to the contained [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) objects.</span></span>

<span data-ttu-id="f8c84-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f8c84-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8c84-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8c84-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedSnapshots : CIM_CollectedMSEs
{
  Msvm_SnapshotCollection       REF Collection;
  Msvm_VirtualSystemSettingData REF Member;
};
```

## <a name="members"></a><span data-ttu-id="f8c84-107">Члены</span><span class="sxs-lookup"><span data-stu-id="f8c84-107">Members</span></span>

<span data-ttu-id="f8c84-108">Класс **мсвм \_ коллектедснапшотс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f8c84-108">The **Msvm\_CollectedSnapshots** class has these types of members:</span></span>

-   [<span data-ttu-id="f8c84-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8c84-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8c84-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8c84-110">Properties</span></span>

<span data-ttu-id="f8c84-111">Класс **мсвм \_ коллектедснапшотс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f8c84-111">The **Msvm\_CollectedSnapshots** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8c84-112">**Коллекция**</span><span class="sxs-lookup"><span data-stu-id="f8c84-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8c84-113">Тип данных: **мсвм \_ снапшотколлектион**</span><span class="sxs-lookup"><span data-stu-id="f8c84-113">Data type: **Msvm\_SnapshotCollection**</span></span>
</dt> <dt>

<span data-ttu-id="f8c84-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8c84-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8c84-115">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="f8c84-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="f8c84-116">Объект [**мсвм \_ снапшотколлектион**](msvm-snapshotcollection.md) GROUPING или "сумка", представляющий коллекцию.</span><span class="sxs-lookup"><span data-stu-id="f8c84-116">An [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="f8c84-117">**Член**</span><span class="sxs-lookup"><span data-stu-id="f8c84-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8c84-118">Тип данных: **мсвм \_ виртуалсистемсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="f8c84-118">Data type: **Msvm\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="f8c84-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8c84-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8c84-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("член")</span><span class="sxs-lookup"><span data-stu-id="f8c84-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="f8c84-121">Объект [**\_ виртуалсистемсеттингдата мсвм**](msvm-virtualsystemsettingdata.md) , содержащий элементы коллекции.</span><span class="sxs-lookup"><span data-stu-id="f8c84-121">An [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8c84-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f8c84-122">Requirements</span></span>



| <span data-ttu-id="f8c84-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f8c84-123">Requirement</span></span> | <span data-ttu-id="f8c84-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f8c84-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c84-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8c84-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f8c84-126">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f8c84-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f8c84-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8c84-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f8c84-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f8c84-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f8c84-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f8c84-129">Namespace</span></span><br/>                | <span data-ttu-id="f8c84-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f8c84-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f8c84-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f8c84-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8c84-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8c84-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8c84-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f8c84-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8c84-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f8c84-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f8c84-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8c84-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8c84-136">**\_КОЛЛЕКТЕДМСЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="f8c84-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

