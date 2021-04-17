---
description: Представляет коллекцию других коллекций.
ms.assetid: 1f7f5517-55d9-44a3-b0ca-444a9d7d5941
title: Класс Msvm_ManagementCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ManagementCollection
- Msvm_ManagementCollection.CollectionID
- Msvm_ManagementCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2d3499bb161495152b6de4b8aebd7c64d041d069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684475"
---
# <a name="msvm_managementcollection-class"></a><span data-ttu-id="e7644-103">\_Класс мсвм манажементколлектион</span><span class="sxs-lookup"><span data-stu-id="e7644-103">Msvm\_ManagementCollection class</span></span>

<span data-ttu-id="e7644-104">Представляет коллекцию других коллекций.</span><span class="sxs-lookup"><span data-stu-id="e7644-104">Represents a collection of other collections.</span></span>

<span data-ttu-id="e7644-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e7644-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7644-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7644-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ManagementCollection : CIM_CollectionOfMSEs
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="e7644-107">Члены</span><span class="sxs-lookup"><span data-stu-id="e7644-107">Members</span></span>

<span data-ttu-id="e7644-108">Класс **мсвм \_ манажементколлектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e7644-108">The **Msvm\_ManagementCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="e7644-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="e7644-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7644-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e7644-110">Properties</span></span>

<span data-ttu-id="e7644-111">Класс **мсвм \_ манажементколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e7644-111">The **Msvm\_ManagementCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7644-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="e7644-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7644-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e7644-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7644-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e7644-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7644-115">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e7644-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e7644-116">Уникальная идентификация объекта коллекции.</span><span class="sxs-lookup"><span data-stu-id="e7644-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="e7644-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e7644-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7644-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e7644-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7644-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e7644-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7644-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="e7644-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="e7644-121">Определяемое пользователем имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="e7644-121">An user-defined name for the collection.</span></span> <span data-ttu-id="e7644-122">Обратите внимание, что это не обязательно должно быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="e7644-122">Note this is not guaranteed to be unique.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7644-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e7644-123">Requirements</span></span>



| <span data-ttu-id="e7644-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e7644-124">Requirement</span></span> | <span data-ttu-id="e7644-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e7644-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7644-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7644-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e7644-127">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e7644-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e7644-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7644-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e7644-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e7644-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e7644-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e7644-130">Namespace</span></span><br/>                | <span data-ttu-id="e7644-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e7644-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e7644-132">MOF</span><span class="sxs-lookup"><span data-stu-id="e7644-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7644-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7644-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7644-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e7644-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7644-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e7644-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e7644-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7644-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7644-137">**\_КОЛЛЕКТИОНОФМСЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="e7644-137">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> </dl>

 

