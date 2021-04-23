---
description: Представляет ассоциацию, когда \_ объект CIM сервицеакцесспоинт запрашивает службы протокола из \_ объекта протоколендпоинт CIM.
ms.assetid: d1ef774d-f0e0-43e7-8a9d-63c2fad5ca4a
title: Класс CIM_BindsTo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsTo
- CIM_BindsTo.Antecedent
- CIM_BindsTo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae32bd10d1e7d1944519fe8fb039453989c165fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663595"
---
# <a name="cim_bindsto-class"></a><span data-ttu-id="cd388-103">\_Класс CIM биндсто</span><span class="sxs-lookup"><span data-stu-id="cd388-103">CIM\_BindsTo class</span></span>

<span data-ttu-id="cd388-104">Представляет ассоциацию, когда объект [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md) запрашивает службы протокола из [**объекта \_ протоколендпоинт CIM**](cim-protocolendpoint.md) .</span><span class="sxs-lookup"><span data-stu-id="cd388-104">Represents an association where a [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) object requests protocol services from a [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd388-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd388-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_BindsTo : CIM_SAPSAPDependency
{
  CIM_ProtocolEndpoint   REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="cd388-106">Члены</span><span class="sxs-lookup"><span data-stu-id="cd388-106">Members</span></span>

<span data-ttu-id="cd388-107">Класс **CIM \_ биндсто** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cd388-107">The **CIM\_BindsTo** class has these types of members:</span></span>

-   [<span data-ttu-id="cd388-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="cd388-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd388-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="cd388-109">Properties</span></span>

<span data-ttu-id="cd388-110">Класс **CIM \_ биндсто** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cd388-110">The **CIM\_BindsTo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd388-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="cd388-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd388-112">Тип данных: **CIM \_ протоколендпоинт**</span><span class="sxs-lookup"><span data-stu-id="cd388-112">Data type: **CIM\_ProtocolEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="cd388-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd388-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd388-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="cd388-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="cd388-115">Конечная точка нижнего уровня, к которой обращается точка доступа службы.</span><span class="sxs-lookup"><span data-stu-id="cd388-115">The lower level endpoint that is accessed by the service access point.</span></span>

</dd> <dt>

<span data-ttu-id="cd388-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="cd388-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd388-117">Тип данных: **CIM \_ сервицеакцесспоинт**</span><span class="sxs-lookup"><span data-stu-id="cd388-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="cd388-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd388-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd388-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="cd388-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="cd388-120">Точка доступа или конечная точка протокола, зависящая от конечной точки нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="cd388-120">The access point or protocol endpoint that is dependent on the lower level endpoint.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd388-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cd388-121">Requirements</span></span>



| <span data-ttu-id="cd388-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cd388-122">Requirement</span></span> | <span data-ttu-id="cd388-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cd388-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd388-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd388-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cd388-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cd388-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="cd388-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd388-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cd388-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd388-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="cd388-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cd388-128">Namespace</span></span><br/>                | <span data-ttu-id="cd388-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="cd388-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cd388-130">MOF</span><span class="sxs-lookup"><span data-stu-id="cd388-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd388-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd388-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd388-132">DLL</span><span class="sxs-lookup"><span data-stu-id="cd388-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd388-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd388-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd388-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd388-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd388-135">**\_САПСАПДЕПЕНДЕНЦИ CIM**</span><span class="sxs-lookup"><span data-stu-id="cd388-135">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> </dl>

 

