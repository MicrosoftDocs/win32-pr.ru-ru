---
description: Представляет точку доступа к службе (SAP), которая может использовать или вызывать службу. SAPs указывает, что служба доступна для использования другими сущностями.
ms.assetid: 09349c95-3f7e-46c5-bea1-c3d14ee16a2a
title: Класс CIM_ServiceAccessPoint (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e3e27fc667c55cd101b06a34f9140cb9eed8923f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682806"
---
# <a name="cim_serviceaccesspoint-class-hyper-v-management"></a><span data-ttu-id="b14a3-104">Класс CIM_ServiceAccessPoint (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="b14a3-104">CIM_ServiceAccessPoint class (Hyper-V management)</span></span>

<span data-ttu-id="b14a3-105">Представляет точку доступа к службе (SAP), которая может использовать или вызывать службу.</span><span class="sxs-lookup"><span data-stu-id="b14a3-105">Represents a service access point (SAP), which is able to utilize or invoke a service.</span></span> <span data-ttu-id="b14a3-106">SAPs указывает, что служба доступна для использования другими сущностями.</span><span class="sxs-lookup"><span data-stu-id="b14a3-106">SAPs indicate that a service is available for other entities to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="b14a3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b14a3-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAccessPoint : CIM_EnabledLogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="b14a3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b14a3-108">Members</span></span>

<span data-ttu-id="b14a3-109">Класс **CIM \_ сервицеакцесспоинт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b14a3-109">The **CIM\_ServiceAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="b14a3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="b14a3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b14a3-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b14a3-111">Properties</span></span>

<span data-ttu-id="b14a3-112">Класс **CIM \_ сервицеакцесспоинт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b14a3-112">The **CIM\_ServiceAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b14a3-113">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b14a3-113">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b14a3-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b14a3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b14a3-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b14a3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b14a3-116">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b14a3-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b14a3-117">Имя класса, используемое для создания экземпляра этого класса.</span><span class="sxs-lookup"><span data-stu-id="b14a3-117">The class name used to create an instance of this class.</span></span> <span data-ttu-id="b14a3-118">**Свойство CreationClassName** объединяется с другими ключевыми свойствами этого класса, чтобы уникальным образом идентифицировать экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="b14a3-118">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="b14a3-119">**Name**</span><span class="sxs-lookup"><span data-stu-id="b14a3-119">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b14a3-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b14a3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b14a3-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b14a3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b14a3-122">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b14a3-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b14a3-123">Уникальное имя SAP, которое указывает возможности, поддерживаемые SAP.</span><span class="sxs-lookup"><span data-stu-id="b14a3-123">The unique name of the SAP that indicates the features supported by the SAP.</span></span>

</dd> <dt>

<span data-ttu-id="b14a3-124">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="b14a3-124">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b14a3-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b14a3-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b14a3-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b14a3-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b14a3-127">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="b14a3-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="b14a3-128">Имя класса, используемое для создания экземпляра системы, содержащей SAP.</span><span class="sxs-lookup"><span data-stu-id="b14a3-128">The class name used to create an instance of the system that contains the SAP.</span></span> <span data-ttu-id="b14a3-129">**Системкреатионкласснаме** сочетается с другими ключевыми свойствами этого класса, чтобы уникальным образом идентифицировать экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="b14a3-129">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="b14a3-130">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b14a3-130">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b14a3-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b14a3-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b14a3-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b14a3-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b14a3-133">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="b14a3-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="b14a3-134">Имя системы, содержащей SAP.</span><span class="sxs-lookup"><span data-stu-id="b14a3-134">The name of the system that contains the SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b14a3-135">Требования</span><span class="sxs-lookup"><span data-stu-id="b14a3-135">Requirements</span></span>



| <span data-ttu-id="b14a3-136">Требование</span><span class="sxs-lookup"><span data-stu-id="b14a3-136">Requirement</span></span> | <span data-ttu-id="b14a3-137">Значение</span><span class="sxs-lookup"><span data-stu-id="b14a3-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b14a3-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b14a3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b14a3-139">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b14a3-139">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b14a3-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b14a3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b14a3-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b14a3-141">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b14a3-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b14a3-142">Namespace</span></span><br/>                | <span data-ttu-id="b14a3-143">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="b14a3-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b14a3-144">MOF</span><span class="sxs-lookup"><span data-stu-id="b14a3-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b14a3-145"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b14a3-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b14a3-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b14a3-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b14a3-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b14a3-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b14a3-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b14a3-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b14a3-149">**\_ЕНАБЛЕДЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="b14a3-149">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

