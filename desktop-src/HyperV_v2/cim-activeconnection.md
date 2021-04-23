---
description: Определяет подключение, которое в настоящее время включено и настроено для обеспечения взаимодействия между двумя \_ объектами CIM сервицеакцесспоинт.
ms.assetid: 03f8e43f-a77b-46e2-bb7d-c29758c65aee
title: Класс CIM_ActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActiveConnection
- CIM_ActiveConnection.Antecedent
- CIM_ActiveConnection.Dependent
- CIM_ActiveConnection.TrafficType
- CIM_ActiveConnection.OtherTrafficDescription
- CIM_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 644e8aaae1368e4164ceca7f7db29e343116c93c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683046"
---
# <a name="cim_activeconnection-class"></a><span data-ttu-id="a2dd9-103">\_Класс CIM ActiveConnection</span><span class="sxs-lookup"><span data-stu-id="a2dd9-103">CIM\_ActiveConnection class</span></span>

<span data-ttu-id="a2dd9-104">Определяет подключение, которое в настоящее время включено и настроено для обеспечения взаимодействия между двумя объектами **CIM \_ сервицеакцесспоинт** .</span><span class="sxs-lookup"><span data-stu-id="a2dd9-104">Defines a connection that is currently turned on and configured to provide communication between two **CIM\_ServiceAccessPoint** objects.</span></span> <span data-ttu-id="a2dd9-105">**Модель CIM \_ ActiveConnection** используется, если соединение не рассматривается как объект **CIM \_ манажеделемент** .</span><span class="sxs-lookup"><span data-stu-id="a2dd9-105">**CIM\_ActiveConnection** is used when the connection is not treated as a **CIM\_ManagedElement** object.</span></span> <span data-ttu-id="a2dd9-106">Точки доступа к службам, подключенные активным подключением, обычно находятся на одном уровне сети или приложения.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-106">Service access points that are connected by an active connection are typically at the same networking or application layer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2dd9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2dd9-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ActiveConnection : CIM_SAPSAPDependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     TrafficType;
  string                     OtherTrafficDescription;
  boolean                    IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="a2dd9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="a2dd9-108">Members</span></span>

<span data-ttu-id="a2dd9-109">Класс **CIM \_ ActiveConnection** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a2dd9-109">The **CIM\_ActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="a2dd9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a2dd9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2dd9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a2dd9-111">Properties</span></span>

<span data-ttu-id="a2dd9-112">Класс **CIM \_ ActiveConnection** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-112">The **CIM\_ActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2dd9-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="a2dd9-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dd9-114">Тип данных: **CIM \_ сервицеакцесспоинт**</span><span class="sxs-lookup"><span data-stu-id="a2dd9-114">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="a2dd9-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dd9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dd9-116">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="a2dd9-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a2dd9-117">Точка доступа к службе, которая подключена к другой точке доступа к службе через активное соединение.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-117">The service access point that is connected to the other service access point through the active connection.</span></span> <span data-ttu-id="a2dd9-118">**Модель CIM \_ Объект Сервицеакцесспоинт** .</span><span class="sxs-lookup"><span data-stu-id="a2dd9-118">**CIM\_ServiceAccessPoint** object.</span></span> <span data-ttu-id="a2dd9-119">В однонаправленном соединении это точка доступа, которая передает данные.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-119">In a unidirectional connection, this access point is the one that is transmitting data.</span></span>

</dd> <dt>

<span data-ttu-id="a2dd9-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="a2dd9-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dd9-121">Тип данных: **CIM \_ сервицеакцесспоинт**</span><span class="sxs-lookup"><span data-stu-id="a2dd9-121">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="a2dd9-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dd9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dd9-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="a2dd9-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a2dd9-124">Точка доступа к службе, настроенная для обмена данными или активно взаимодействующая с точкой доступа к службе, указанной в свойстве **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="a2dd9-124">The service access point that is configured to communicate or is actively communicating with the service access point specified in the **Antecedent** property.</span></span> <span data-ttu-id="a2dd9-125">В однонаправленном соединении это точка доступа, которая получает данные.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-125">In a unidirectional connection, this access point is the one that is receiving data.</span></span>

</dd> <dt>

<span data-ttu-id="a2dd9-126">**По поднаправлению**</span><span class="sxs-lookup"><span data-stu-id="a2dd9-126">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dd9-127">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a2dd9-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2dd9-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dd9-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2dd9-129">Значение true, если соединение является однонаправленным; значение false, если соединение является двунаправленным.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-129">True if the connection is unidirectional; false if the connection is bidirectional.</span></span> <span data-ttu-id="a2dd9-130">Если соединение является однонаправленным, свойство **Antecedent** указывает точку доступа, которая передает данные.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-130">When the connection is unidirectional, the **Antecedent** property specifies the access point that is transmitting data.</span></span> <span data-ttu-id="a2dd9-131">В двунаправленном соединении **Antecedent** может указывать любую точку доступа, назначенную соединению.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-131">In a bidirectional connection, **Antecedent** can specify either access point assigned to the connection.</span></span>

</dd> <dt>

<span data-ttu-id="a2dd9-132">**осертраффикдескриптион**</span><span class="sxs-lookup"><span data-stu-id="a2dd9-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dd9-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dd9-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dd9-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dd9-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dd9-135">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**Траффиктипе**")</span><span class="sxs-lookup"><span data-stu-id="a2dd9-135">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ActiveConnection**.**TrafficType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="a2dd9-136">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-136">This property is deprecated.</span></span> <span data-ttu-id="a2dd9-137">Вместо этого рекомендуется указывать эти сведения в параметрах адресации, протокола и базовой функциональности конечных точек.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-137">Instead, we recommend that you specify this information in the addressing, protocol, and basic functionality of the endpoints.</span></span>

 

<span data-ttu-id="a2dd9-138">Описание типа трафика, указанного, если свойство **траффиктипе** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="a2dd9-138">A description of the traffic type that is specified when the **TrafficType** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="a2dd9-139">**ТипТрафика**</span><span class="sxs-lookup"><span data-stu-id="a2dd9-139">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dd9-140">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2dd9-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2dd9-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dd9-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dd9-142">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**Осертраффикдескриптион**")</span><span class="sxs-lookup"><span data-stu-id="a2dd9-142">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ActiveConnection**.**OtherTrafficDescription**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="a2dd9-143">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-143">This property is deprecated.</span></span> <span data-ttu-id="a2dd9-144">Вместо этого рекомендуется указывать эти сведения в параметрах адресации, протокола и базовой функциональности конечных точек.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-144">Instead, we recommend that you specify this information in the addressing, protocol, and basic functionality of the endpoints.</span></span>

 

<span data-ttu-id="a2dd9-145">Тип трафика, передаваемого через это соединение.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-145">The type of traffic that is transmitted over this connection.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a2dd9-146">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a2dd9-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a2dd9-147">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="a2dd9-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicast"></span><span id="unicast"></span><span id="UNICAST"></span>

<span data-ttu-id="a2dd9-148">**Одноадресная рассылка** (2)</span><span class="sxs-lookup"><span data-stu-id="a2dd9-148">**Unicast** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast"></span><span id="broadcast"></span><span id="BROADCAST"></span>

<span data-ttu-id="a2dd9-149">**Вещание** (3)</span><span class="sxs-lookup"><span data-stu-id="a2dd9-149">**Broadcast** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Multicast"></span><span id="multicast"></span><span id="MULTICAST"></span>

<span data-ttu-id="a2dd9-150">**Многоадресная рассылка** (4)</span><span class="sxs-lookup"><span data-stu-id="a2dd9-150">**Multicast** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Anycast"></span><span id="anycast"></span><span id="ANYCAST"></span>

<span data-ttu-id="a2dd9-151">**Рассылки** (5)</span><span class="sxs-lookup"><span data-stu-id="a2dd9-151">**Anycast** (5)</span></span>


<span data-ttu-id="a2dd9-152"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a2dd9-152"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a2dd9-153">Требования</span><span class="sxs-lookup"><span data-stu-id="a2dd9-153">Requirements</span></span>



| <span data-ttu-id="a2dd9-154">Требование</span><span class="sxs-lookup"><span data-stu-id="a2dd9-154">Requirement</span></span> | <span data-ttu-id="a2dd9-155">Значение</span><span class="sxs-lookup"><span data-stu-id="a2dd9-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2dd9-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2dd9-156">Minimum supported client</span></span><br/> | <span data-ttu-id="a2dd9-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a2dd9-157">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a2dd9-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2dd9-158">Minimum supported server</span></span><br/> | <span data-ttu-id="a2dd9-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2dd9-159">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a2dd9-160">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a2dd9-160">Namespace</span></span><br/>                | <span data-ttu-id="a2dd9-161">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a2dd9-161">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a2dd9-162">MOF</span><span class="sxs-lookup"><span data-stu-id="a2dd9-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2dd9-163"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2dd9-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2dd9-164">DLL</span><span class="sxs-lookup"><span data-stu-id="a2dd9-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2dd9-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a2dd9-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a2dd9-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2dd9-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2dd9-167">**\_САПСАПДЕПЕНДЕНЦИ CIM**</span><span class="sxs-lookup"><span data-stu-id="a2dd9-167">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> </dl>

 

