---
description: Абстрактный класс для подклассов, представляющих коллекцию объектов CIM \_ манажедсистемелемент. Эти коллекции позволяют группировать управляемые системные элементы для целей идентификации и упростить сопоставление параметров и конфигураций.
ms.assetid: f47bf1d6-6d89-4d9f-82d1-99a7343481bc
title: Класс CIM_CollectionOfMSEs (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.CollectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e467e775c78364718f25cc732d6689d9fb2b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908740"
---
# <a name="cim_collectionofmses-class-hyper-v-management"></a><span data-ttu-id="6c9ae-104">Класс CIM_CollectionOfMSEs (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="6c9ae-104">CIM_CollectionOfMSEs class (Hyper-V management)</span></span>

<span data-ttu-id="6c9ae-105">Абстрактный класс для подклассов, представляющих коллекцию объектов [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="6c9ae-105">An abstract class for subclasses that represent a collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects.</span></span> <span data-ttu-id="6c9ae-106">Эти коллекции позволяют группировать управляемые системные элементы для целей идентификации и упростить сопоставление параметров и конфигураций.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-106">These collections allow managed system elements to be grouped for identification purposes and to simplify the association of settings and configurations.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c9ae-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c9ae-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectionOfMSEs : CIM_Collection
{
  string CollectionID;
};
```

## <a name="members"></a><span data-ttu-id="6c9ae-108">Члены</span><span class="sxs-lookup"><span data-stu-id="6c9ae-108">Members</span></span>

<span data-ttu-id="6c9ae-109">Класс **CIM \_ коллектионофмсес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6c9ae-109">The **CIM\_CollectionOfMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="6c9ae-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="6c9ae-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c9ae-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="6c9ae-111">Properties</span></span>

<span data-ttu-id="6c9ae-112">Класс **CIM \_ коллектионофмсес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-112">The **CIM\_CollectionOfMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c9ae-113">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="6c9ae-113">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c9ae-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6c9ae-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c9ae-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6c9ae-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c9ae-116">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6c9ae-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6c9ae-117">Идентификация объекта коллекции.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-117">The identification of the collection object.</span></span> <span data-ttu-id="6c9ae-118">При создании подкласса свойство **CollectionID** может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="6c9ae-118">When subclassed, the **CollectionID** property can be overridden as a key property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c9ae-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6c9ae-119">Requirements</span></span>



| <span data-ttu-id="6c9ae-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6c9ae-120">Requirement</span></span> | <span data-ttu-id="6c9ae-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6c9ae-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c9ae-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c9ae-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6c9ae-123">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6c9ae-123">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6c9ae-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c9ae-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6c9ae-125">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6c9ae-125">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6c9ae-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6c9ae-126">Namespace</span></span><br/>                | <span data-ttu-id="6c9ae-127">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6c9ae-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6c9ae-128">MOF</span><span class="sxs-lookup"><span data-stu-id="6c9ae-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c9ae-129"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c9ae-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c9ae-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6c9ae-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c9ae-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6c9ae-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6c9ae-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c9ae-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c9ae-133">**\_Коллекция CIM**</span><span class="sxs-lookup"><span data-stu-id="6c9ae-133">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

