---
description: Связывает референцепоинтколлектион Мсвм \_ с содержащимися в \_ них объектами мсвм виртуалсистемреференцепоинт.
ms.assetid: 826125c3-0a89-4573-ac28-88588eac248d
title: Класс Msvm_CollectedReferencePoints
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedReferencePoints
- Msvm_CollectedReferencePoints.Collection
- Msvm_CollectedReferencePoints.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4891d4ec4c613c92c3b5d5a090f2683bfc77dc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810918"
---
# <a name="msvm_collectedreferencepoints-class"></a><span data-ttu-id="93f52-103">\_Класс мсвм коллектедреференцепоинтс</span><span class="sxs-lookup"><span data-stu-id="93f52-103">Msvm\_CollectedReferencePoints class</span></span>

<span data-ttu-id="93f52-104">Связывает [**\_ референцепоинтколлектион мсвм**](msvm-referencepointcollection.md) с содержащимися в них объектами [**мсвм \_ виртуалсистемреференцепоинт**](msvm-virtualsystemreferencepoint.md) .</span><span class="sxs-lookup"><span data-stu-id="93f52-104">Associates the [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) to the contained [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) objects.</span></span>

<span data-ttu-id="93f52-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="93f52-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="93f52-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93f52-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedReferencePoints : CIM_CollectedMSEs
{
  Msvm_ReferencePointCollection    REF Collection;
  Msvm_VirtualSystemReferencePoint REF Member;
};
```

## <a name="members"></a><span data-ttu-id="93f52-107">Члены</span><span class="sxs-lookup"><span data-stu-id="93f52-107">Members</span></span>

<span data-ttu-id="93f52-108">Класс **мсвм \_ коллектедреференцепоинтс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="93f52-108">The **Msvm\_CollectedReferencePoints** class has these types of members:</span></span>

-   [<span data-ttu-id="93f52-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="93f52-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93f52-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="93f52-110">Properties</span></span>

<span data-ttu-id="93f52-111">Класс **мсвм \_ коллектедреференцепоинтс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="93f52-111">The **Msvm\_CollectedReferencePoints** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93f52-112">**Коллекция**</span><span class="sxs-lookup"><span data-stu-id="93f52-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f52-113">Тип данных: **мсвм \_ референцепоинтколлектион**</span><span class="sxs-lookup"><span data-stu-id="93f52-113">Data type: **Msvm\_ReferencePointCollection**</span></span>
</dt> <dt>

<span data-ttu-id="93f52-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93f52-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93f52-115">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="93f52-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="93f52-116">Объект [**мсвм \_ референцепоинтколлектион**](msvm-referencepointcollection.md) GROUPING или "сумка", представляющий коллекцию.</span><span class="sxs-lookup"><span data-stu-id="93f52-116">An [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="93f52-117">**Член**</span><span class="sxs-lookup"><span data-stu-id="93f52-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f52-118">Тип данных: **мсвм \_ виртуалсистемреференцепоинт**</span><span class="sxs-lookup"><span data-stu-id="93f52-118">Data type: **Msvm\_VirtualSystemReferencePoint**</span></span>
</dt> <dt>

<span data-ttu-id="93f52-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93f52-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93f52-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("член")</span><span class="sxs-lookup"><span data-stu-id="93f52-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="93f52-121">Объект [**\_ виртуалсистемреференцепоинт мсвм**](msvm-virtualsystemreferencepoint.md) , содержащий элементы коллекции.</span><span class="sxs-lookup"><span data-stu-id="93f52-121">An [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93f52-122">Требования</span><span class="sxs-lookup"><span data-stu-id="93f52-122">Requirements</span></span>



| <span data-ttu-id="93f52-123">Требование</span><span class="sxs-lookup"><span data-stu-id="93f52-123">Requirement</span></span> | <span data-ttu-id="93f52-124">Значение</span><span class="sxs-lookup"><span data-stu-id="93f52-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93f52-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93f52-125">Minimum supported client</span></span><br/> | <span data-ttu-id="93f52-126">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="93f52-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="93f52-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93f52-127">Minimum supported server</span></span><br/> | <span data-ttu-id="93f52-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="93f52-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="93f52-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="93f52-129">Namespace</span></span><br/>                | <span data-ttu-id="93f52-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="93f52-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="93f52-131">MOF</span><span class="sxs-lookup"><span data-stu-id="93f52-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93f52-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93f52-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93f52-133">DLL</span><span class="sxs-lookup"><span data-stu-id="93f52-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93f52-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93f52-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="93f52-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93f52-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93f52-136">**\_КОЛЛЕКТЕДМСЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="93f52-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

