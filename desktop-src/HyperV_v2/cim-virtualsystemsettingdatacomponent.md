---
description: Представляет часть связи между \_ экземпляром CIM виртуалсистемсеттингдата и набором \_ экземпляров ресаурцеаллокатионсеттингдата CIM.
ms.assetid: 4f167517-079e-4b5f-885a-741ac1d1dc71
title: Класс CIM_VirtualSystemSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingDataComponent
- CIM_VirtualSystemSettingDataComponent.GroupComponent
- CIM_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afbd7ab192c65e99f4479e5380e57dc78c8a0a9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156846"
---
# <a name="cim_virtualsystemsettingdatacomponent-class"></a><span data-ttu-id="53d3b-103">\_Класс CIM виртуалсистемсеттингдатакомпонент</span><span class="sxs-lookup"><span data-stu-id="53d3b-103">CIM\_VirtualSystemSettingDataComponent class</span></span>

<span data-ttu-id="53d3b-104">Представляет часть связи между экземпляром [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) и набором экземпляров [**\_ ресаурцеаллокатионсеттингдата CIM**](cim-resourceallocationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="53d3b-104">Represents a portion of a relationship between a [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) instance and a set of [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="53d3b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53d3b-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingDataComponent : CIM_Component
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="53d3b-106">Члены</span><span class="sxs-lookup"><span data-stu-id="53d3b-106">Members</span></span>

<span data-ttu-id="53d3b-107">Класс **CIM \_ виртуалсистемсеттингдатакомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="53d3b-107">The **CIM\_VirtualSystemSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="53d3b-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="53d3b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53d3b-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="53d3b-109">Properties</span></span>

<span data-ttu-id="53d3b-110">Класс **CIM \_ виртуалсистемсеттингдатакомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="53d3b-110">The **CIM\_VirtualSystemSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53d3b-111">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="53d3b-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d3b-112">Тип данных: **CIM \_ виртуалсистемсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="53d3b-112">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="53d3b-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53d3b-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d3b-114">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="53d3b-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="53d3b-115">Ссылка на объект CIM верхнего уровня [**\_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="53d3b-115">A reference to the top-level [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) object of the virtual system configuration.</span></span>

</dd> <dt>

<span data-ttu-id="53d3b-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="53d3b-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d3b-117">Тип данных: **CIM \_ ресаурцеаллокатионсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="53d3b-117">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="53d3b-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53d3b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d3b-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="53d3b-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="53d3b-120">Ссылка на объект [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , представляющий часть конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="53d3b-120">A reference the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) object that represents a part of the virtual system configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53d3b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="53d3b-121">Requirements</span></span>



| <span data-ttu-id="53d3b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="53d3b-122">Requirement</span></span> | <span data-ttu-id="53d3b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="53d3b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53d3b-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53d3b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="53d3b-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="53d3b-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="53d3b-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53d3b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="53d3b-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53d3b-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="53d3b-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="53d3b-128">Namespace</span></span><br/>                | <span data-ttu-id="53d3b-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="53d3b-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="53d3b-130">MOF</span><span class="sxs-lookup"><span data-stu-id="53d3b-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53d3b-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53d3b-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="53d3b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="53d3b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53d3b-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53d3b-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="53d3b-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53d3b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53d3b-135">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="53d3b-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

