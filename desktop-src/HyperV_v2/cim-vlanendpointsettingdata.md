---
description: Представляет данные конфигурации для конечной точки виртуальной ЛС.
ms.assetid: 5ef3cc55-cf27-40b4-9e94-2e2b42ca41c5
title: Класс CIM_VLANEndpointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpointSettingData
- CIM_VLANEndpointSettingData.PruneEligibleVLANList
- CIM_VLANEndpointSettingData.NativeVLAN
- CIM_VLANEndpointSettingData.DefaultVLAN
- CIM_VLANEndpointSettingData.TrunkedVLANList
- CIM_VLANEndpointSettingData.AccessVLAN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a510c4195c538ab9735e7544acec2c88beeaa1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913899"
---
# <a name="cim_vlanendpointsettingdata-class"></a><span data-ttu-id="3d126-103">\_Класс CIM вланендпоинтсеттингдата</span><span class="sxs-lookup"><span data-stu-id="3d126-103">CIM\_VLANEndpointSettingData class</span></span>

<span data-ttu-id="3d126-104">Представляет данные конфигурации для конечной точки виртуальной ЛС.</span><span class="sxs-lookup"><span data-stu-id="3d126-104">Represents configuration data for a VLAN endpoint.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d126-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d126-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.11.0"), UMLPackagePath("CIM::Network::VLAN")]
class CIM_VLANEndpointSettingData : CIM_SettingData
{
  uint16 PruneEligibleVLANList[];
  uint16 NativeVLAN;
  uint16 DefaultVLAN;
  uint16 TrunkedVLANList[];
  uint16 AccessVLAN;
};
```

## <a name="members"></a><span data-ttu-id="3d126-106">Члены</span><span class="sxs-lookup"><span data-stu-id="3d126-106">Members</span></span>

<span data-ttu-id="3d126-107">Класс **CIM \_ вланендпоинтсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3d126-107">The **CIM\_VLANEndpointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3d126-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="3d126-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3d126-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="3d126-109">Properties</span></span>

<span data-ttu-id="3d126-110">Класс **CIM \_ вланендпоинтсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3d126-110">The **CIM\_VLANEndpointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d126-111">**акцессвлан**</span><span class="sxs-lookup"><span data-stu-id="3d126-111">**AccessVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d126-112">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3d126-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3d126-113">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3d126-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3d126-114">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ вланендпоинт**](cim-vlanendpoint.md).**Оператионалендпоинтмоде**")</span><span class="sxs-lookup"><span data-stu-id="3d126-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="3d126-115">VLAN для доступа к конечной точке.</span><span class="sxs-lookup"><span data-stu-id="3d126-115">The access VLAN for the endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="3d126-116">**дефаултвлан**</span><span class="sxs-lookup"><span data-stu-id="3d126-116">**DefaultVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d126-117">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3d126-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3d126-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d126-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d126-119">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ вланендпоинт**](cim-vlanendpoint.md).**Оператионалендпоинтмоде**")</span><span class="sxs-lookup"><span data-stu-id="3d126-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="3d126-120">Значение по умолчанию для собственной виртуальной ЛС в конечной точке магистрали.</span><span class="sxs-lookup"><span data-stu-id="3d126-120">The default value for the native VLAN on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="3d126-121">Это свойство используется, только если конечная точка VLAN работает в режиме магистрали, который указан в свойстве **оператионалендпоинтмоде** .</span><span class="sxs-lookup"><span data-stu-id="3d126-121">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="3d126-122">**нативевлан**</span><span class="sxs-lookup"><span data-stu-id="3d126-122">**NativeVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d126-123">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3d126-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3d126-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3d126-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3d126-125">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ вланендпоинт**](cim-vlanendpoint.md).**Оператионалендпоинтмоде**")</span><span class="sxs-lookup"><span data-stu-id="3d126-125">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="3d126-126">ИДЕНТИФИКАТОР виртуальной ЛС, который используется для обозначения трафика без тегов, полученного в конечной точке магистрали.</span><span class="sxs-lookup"><span data-stu-id="3d126-126">The VLAN ID that is used to tag untagged traffic received on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="3d126-127">Это свойство используется, только если конечная точка VLAN работает в режиме магистрали, который указан в свойстве **свитчендпоинтмоде** .</span><span class="sxs-lookup"><span data-stu-id="3d126-127">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **SwitchEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="3d126-128">**прунилигиблевланлист**</span><span class="sxs-lookup"><span data-stu-id="3d126-128">**PruneEligibleVLANList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d126-129">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3d126-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3d126-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3d126-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3d126-131">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ вланендпоинт**](cim-vlanendpoint.md).**Оператионалендпоинтмоде**")</span><span class="sxs-lookup"><span data-stu-id="3d126-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="3d126-132">Массив, содержащий идентификаторы виртуальных ЛС, которые система может удалить из конечной точки магистрали.</span><span class="sxs-lookup"><span data-stu-id="3d126-132">An array that contains IDs of VLANs that the system may remove from the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="3d126-133">Это свойство используется, только если конечная точка VLAN работает в режиме магистрали, который указан в свойстве **оператионалендпоинтмоде** .</span><span class="sxs-lookup"><span data-stu-id="3d126-133">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="3d126-134">**трункедвланлист**</span><span class="sxs-lookup"><span data-stu-id="3d126-134">**TrunkedVLANList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d126-135">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3d126-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3d126-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3d126-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3d126-137">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ вланендпоинт**](cim-vlanendpoint.md).**Оператионалендпоинтмоде**")</span><span class="sxs-lookup"><span data-stu-id="3d126-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="3d126-138">Массив, содержащий идентификаторы конечных точек VLAN с включенной магистральной службой.</span><span class="sxs-lookup"><span data-stu-id="3d126-138">An array that contains IDs of VLAN endpoints with trunking enabled.</span></span>

> [!Note]  
> <span data-ttu-id="3d126-139">Это свойство используется, только если конечная точка VLAN работает в режиме магистрали, который указан в свойстве **оператионалендпоинтмоде** .</span><span class="sxs-lookup"><span data-stu-id="3d126-139">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d126-140">Требования</span><span class="sxs-lookup"><span data-stu-id="3d126-140">Requirements</span></span>



| <span data-ttu-id="3d126-141">Требование</span><span class="sxs-lookup"><span data-stu-id="3d126-141">Requirement</span></span> | <span data-ttu-id="3d126-142">Значение</span><span class="sxs-lookup"><span data-stu-id="3d126-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d126-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d126-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3d126-144">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3d126-144">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3d126-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d126-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3d126-146">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3d126-146">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3d126-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3d126-147">Namespace</span></span><br/>                | <span data-ttu-id="3d126-148">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3d126-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3d126-149">MOF</span><span class="sxs-lookup"><span data-stu-id="3d126-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d126-150"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d126-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d126-151">DLL</span><span class="sxs-lookup"><span data-stu-id="3d126-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d126-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3d126-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3d126-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d126-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d126-154">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="3d126-154">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

