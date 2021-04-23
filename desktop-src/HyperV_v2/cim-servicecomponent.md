---
description: Представляет ассоциацию, в которой служба является компонентом родительской службы, которая вместе формирует службу более высокого уровня.
ms.assetid: c629d59d-d9d3-4019-a378-cd1d4d31a5d9
title: Класс CIM_ServiceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceComponent
- CIM_ServiceComponent.GroupComponent
- CIM_ServiceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2bfb9943685f8568674e696a76df94fda502fcb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263227"
---
# <a name="cim_servicecomponent-class"></a><span data-ttu-id="a5719-103">\_Класс CIM ServiceComponent</span><span class="sxs-lookup"><span data-stu-id="a5719-103">CIM\_ServiceComponent class</span></span>

<span data-ttu-id="a5719-104">Представляет ассоциацию, в которой служба является компонентом родительской службы, которая вместе формирует службу более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="a5719-104">Represents an association in which a service is a component of a parent service, which together, form a higher-level service.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5719-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5719-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceComponent : CIM_Component
{
  CIM_Service REF GroupComponent;
  CIM_Service REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="a5719-106">Члены</span><span class="sxs-lookup"><span data-stu-id="a5719-106">Members</span></span>

<span data-ttu-id="a5719-107">Класс **CIM \_ ServiceComponent** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a5719-107">The **CIM\_ServiceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="a5719-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="a5719-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5719-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="a5719-109">Properties</span></span>

<span data-ttu-id="a5719-110">Класс **CIM \_ ServiceComponent** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a5719-110">The **CIM\_ServiceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5719-111">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="a5719-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5719-112">Тип данных: **\_ Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="a5719-112">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="a5719-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5719-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5719-114">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="a5719-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="a5719-115">Родительская служба.</span><span class="sxs-lookup"><span data-stu-id="a5719-115">The parent service.</span></span>

</dd> <dt>

<span data-ttu-id="a5719-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a5719-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5719-117">Тип данных: **\_ Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="a5719-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="a5719-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5719-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5719-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="a5719-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="a5719-120">Служба компонентов.</span><span class="sxs-lookup"><span data-stu-id="a5719-120">The component service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5719-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a5719-121">Requirements</span></span>



| <span data-ttu-id="a5719-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a5719-122">Requirement</span></span> | <span data-ttu-id="a5719-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a5719-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5719-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5719-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a5719-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a5719-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a5719-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5719-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a5719-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a5719-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a5719-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a5719-128">Namespace</span></span><br/>                | <span data-ttu-id="a5719-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a5719-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a5719-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a5719-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5719-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5719-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5719-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a5719-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5719-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a5719-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a5719-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5719-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5719-135">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="a5719-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

