---
description: Связь между точкой доступа к службе (SAP) и ее реализацией.
ms.assetid: 36108521-A699-4498-A962-DC0801D9EE81
title: Класс Msvm_DeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DeviceSAPImplementation
- Msvm_DeviceSAPImplementation.Antecedent
- Msvm_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9551d4409edfdfca18b66e3a3b86d6adcb28b19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663727"
---
# <a name="msvm_devicesapimplementation-class"></a><span data-ttu-id="7a50f-103">\_Класс мсвм девицесапимплементатион</span><span class="sxs-lookup"><span data-stu-id="7a50f-103">Msvm\_DeviceSAPImplementation class</span></span>

<span data-ttu-id="7a50f-104">Связь между точкой доступа к службе (SAP) и ее реализацией.</span><span class="sxs-lookup"><span data-stu-id="7a50f-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="7a50f-105">Кратность этой ассоциации — «многие ко многим».</span><span class="sxs-lookup"><span data-stu-id="7a50f-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="7a50f-106">SAP может предоставляться более чем одним логическим устройством, работающим совместно.</span><span class="sxs-lookup"><span data-stu-id="7a50f-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="7a50f-107">Любое устройство может предоставлять более одного SAP.</span><span class="sxs-lookup"><span data-stu-id="7a50f-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="7a50f-108">Если несколько логических устройств связаны с одним SAP, предполагается, что эти элементы работают совместно, чтобы предоставить точку доступа.</span><span class="sxs-lookup"><span data-stu-id="7a50f-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="7a50f-109">При наличии различных реализаций SAP каждая из этих реализаций будет создавать отдельные экземпляры объекта SAP.</span><span class="sxs-lookup"><span data-stu-id="7a50f-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="7a50f-110">Эти отдельные экземпляры будут иметь связи с уникальными реализациями.</span><span class="sxs-lookup"><span data-stu-id="7a50f-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="7a50f-111">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7a50f-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a50f-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a50f-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="7a50f-113">Члены</span><span class="sxs-lookup"><span data-stu-id="7a50f-113">Members</span></span>

<span data-ttu-id="7a50f-114">Класс **мсвм \_ девицесапимплементатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7a50f-114">The **Msvm\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="7a50f-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="7a50f-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a50f-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="7a50f-116">Properties</span></span>

<span data-ttu-id="7a50f-117">Класс **мсвм \_ девицесапимплементатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7a50f-117">The **Msvm\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a50f-118">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="7a50f-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a50f-119">Тип данных: CIM с типом " **[ **модель \_** "](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="7a50f-119">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="7a50f-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a50f-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a50f-121">Логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="7a50f-121">The logical device.</span></span> <span data-ttu-id="7a50f-122">Это свойство наследуется от [**CIM \_ девицесапимплементатион**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span><span class="sxs-lookup"><span data-stu-id="7a50f-122">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> <dt>

<span data-ttu-id="7a50f-123">**Него**</span><span class="sxs-lookup"><span data-stu-id="7a50f-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a50f-124">Тип данных: **[ **CIM \_ сервицеакцесспоинт**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span><span class="sxs-lookup"><span data-stu-id="7a50f-124">Data type: **[**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span></span>
</dt> <dt>

<span data-ttu-id="7a50f-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a50f-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a50f-126">Точка доступа к службе, реализованная с помощью логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7a50f-126">The service access point implemented using the logical device.</span></span> <span data-ttu-id="7a50f-127">Это свойство наследуется от [**CIM \_ девицесапимплементатион**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span><span class="sxs-lookup"><span data-stu-id="7a50f-127">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a50f-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a50f-128">Remarks</span></span>

<span data-ttu-id="7a50f-129">Доступ к классу **\_ девицесапимплементатион мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="7a50f-129">Access to the **Msvm\_DeviceSAPImplementation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7a50f-130">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7a50f-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="7a50f-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="7a50f-131">Examples</span></span>

<span data-ttu-id="7a50f-132">См. раздел [запросы к сетевым объектам](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7a50f-132">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a50f-133">Требования</span><span class="sxs-lookup"><span data-stu-id="7a50f-133">Requirements</span></span>



| <span data-ttu-id="7a50f-134">Требование</span><span class="sxs-lookup"><span data-stu-id="7a50f-134">Requirement</span></span> | <span data-ttu-id="7a50f-135">Значение</span><span class="sxs-lookup"><span data-stu-id="7a50f-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a50f-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a50f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7a50f-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7a50f-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7a50f-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a50f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7a50f-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7a50f-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a50f-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7a50f-140">Namespace</span></span><br/>                | <span data-ttu-id="7a50f-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7a50f-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7a50f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="7a50f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a50f-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a50f-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a50f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7a50f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a50f-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7a50f-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7a50f-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a50f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a50f-147">**\_ДЕВИЦЕСАПИМПЛЕМЕНТАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="7a50f-147">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dt>

[<span data-ttu-id="7a50f-148">**\_ДЕВИЦЕСАПИМПЛЕМЕНТАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="7a50f-148">**CIM\_DeviceSAPImplementation**</span></span>](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 

