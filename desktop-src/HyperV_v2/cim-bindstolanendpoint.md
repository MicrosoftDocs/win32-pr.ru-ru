---
description: Представляет ассоциацию, в которой \_ объект CIM сервицеакцесспоинт или CIM \_ протоколендпоинт зависит от базового \_ объекта CIM ланендпоинт в той же системе.
ms.assetid: 3c015fbd-0611-41e8-a79a-01c980eedfd3
title: Класс CIM_BindsToLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsToLANEndpoint
- CIM_BindsToLANEndpoint.Antecedent
- CIM_BindsToLANEndpoint.Dependent
- CIM_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dff1cf243b54739509343d6d8958aa2a54f464b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664042"
---
# <a name="cim_bindstolanendpoint-class"></a><span data-ttu-id="916ab-103">\_Класс CIM биндстоланендпоинт</span><span class="sxs-lookup"><span data-stu-id="916ab-103">CIM\_BindsToLANEndpoint class</span></span>

<span data-ttu-id="916ab-104">Представляет ассоциацию, в которой объект [**CIM \_ Сервицеакцесспоинт**](cim-serviceaccesspoint.md) или [**CIM \_ Протоколендпоинт**](cim-protocolendpoint.md) зависит от базового объекта [**CIM \_ ланендпоинт**](cim-lanendpoint.md) в той же системе.</span><span class="sxs-lookup"><span data-stu-id="916ab-104">Represents an association where a [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) or [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object depends on an underlying [**CIM\_LANEndpoint**](cim-lanendpoint.md) object on the same system.</span></span>

## <a name="syntax"></a><span data-ttu-id="916ab-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="916ab-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_BindsToLANEndpoint : CIM_BindsTo
{
  CIM_LANEndpoint        REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     FrameType;
};
```

## <a name="members"></a><span data-ttu-id="916ab-106">Члены</span><span class="sxs-lookup"><span data-stu-id="916ab-106">Members</span></span>

<span data-ttu-id="916ab-107">Класс **CIM \_ биндстоланендпоинт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="916ab-107">The **CIM\_BindsToLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="916ab-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="916ab-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="916ab-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="916ab-109">Properties</span></span>

<span data-ttu-id="916ab-110">Класс **CIM \_ биндстоланендпоинт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="916ab-110">The **CIM\_BindsToLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="916ab-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="916ab-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="916ab-112">Тип данных: **CIM \_ ланендпоинт**</span><span class="sxs-lookup"><span data-stu-id="916ab-112">Data type: **CIM\_LANEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="916ab-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="916ab-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="916ab-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="916ab-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="916ab-115">Базовый объект [**CIM \_ ланендпоинт**](cim-lanendpoint.md) .</span><span class="sxs-lookup"><span data-stu-id="916ab-115">The underlying [**CIM\_LANEndpoint**](cim-lanendpoint.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="916ab-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="916ab-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="916ab-117">Тип данных: **CIM \_ сервицеакцесспоинт**</span><span class="sxs-lookup"><span data-stu-id="916ab-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="916ab-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="916ab-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="916ab-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="916ab-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="916ab-120">Объект [**CIM \_ Сервицеакцесспоинт**](cim-serviceaccesspoint.md) или [**CIM \_ Протоколендпоинт**](cim-protocolendpoint.md) , который зависит от [**CIM \_ ланендпоинт**](cim-lanendpoint.md).</span><span class="sxs-lookup"><span data-stu-id="916ab-120">The [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) or [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object that is dependent on the [**CIM\_LANEndpoint**](cim-lanendpoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="916ab-121">**фраметипе**</span><span class="sxs-lookup"><span data-stu-id="916ab-121">**FrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="916ab-122">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="916ab-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="916ab-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="916ab-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="916ab-124">Метод кадрирования для точки доступа к службе верхнего уровня или конечной точки протокола.</span><span class="sxs-lookup"><span data-stu-id="916ab-124">The framing method for the upper layer service access point or protocol endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="916ab-125">Для протокола IPX известно только использование RAW 802.3.</span><span class="sxs-lookup"><span data-stu-id="916ab-125">Raw802.3 is only known to be used with the IPX protocol.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="916ab-126">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="916ab-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="916ab-127">**Ethernet** (1)</span><span class="sxs-lookup"><span data-stu-id="916ab-127">**Ethernet** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.2"></span>

<span data-ttu-id="916ab-128">**802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="916ab-128">**802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SNAP"></span><span id="snap"></span>

<span data-ttu-id="916ab-129">**Привязать** (3)</span><span class="sxs-lookup"><span data-stu-id="916ab-129">**SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Raw802.3"></span><span id="raw802.3"></span><span id="RAW802.3"></span>

<span data-ttu-id="916ab-130">**RAW 802.3** (4)</span><span class="sxs-lookup"><span data-stu-id="916ab-130">**Raw802.3** (4)</span></span>


<span data-ttu-id="916ab-131"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="916ab-131"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="916ab-132">Требования</span><span class="sxs-lookup"><span data-stu-id="916ab-132">Requirements</span></span>



| <span data-ttu-id="916ab-133">Требование</span><span class="sxs-lookup"><span data-stu-id="916ab-133">Requirement</span></span> | <span data-ttu-id="916ab-134">Значение</span><span class="sxs-lookup"><span data-stu-id="916ab-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="916ab-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="916ab-135">Minimum supported client</span></span><br/> | <span data-ttu-id="916ab-136">Windows 8</span><span class="sxs-lookup"><span data-stu-id="916ab-136">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="916ab-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="916ab-137">Minimum supported server</span></span><br/> | <span data-ttu-id="916ab-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="916ab-138">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="916ab-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="916ab-139">Namespace</span></span><br/>                | <span data-ttu-id="916ab-140">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="916ab-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="916ab-141">MOF</span><span class="sxs-lookup"><span data-stu-id="916ab-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="916ab-142"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="916ab-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="916ab-143">DLL</span><span class="sxs-lookup"><span data-stu-id="916ab-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="916ab-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="916ab-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="916ab-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="916ab-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="916ab-146">**\_БИНДСТО CIM**</span><span class="sxs-lookup"><span data-stu-id="916ab-146">**CIM\_BindsTo**</span></span>](cim-bindsto.md)
</dt> </dl>

 

