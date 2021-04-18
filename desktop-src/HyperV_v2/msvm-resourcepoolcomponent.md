---
description: Представляет элемент пула ресурсов платформы Microsoft Windows Hyper-V.
ms.assetid: DF48E8A6-240F-44E9-9DA3-1E6694396F10
title: Класс Msvm_ResourcePoolComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolComponent
- Msvm_ResourcePoolComponent.CLSID
- Msvm_ResourcePoolComponent.Context
- Msvm_ResourcePoolComponent.Enabled
- Msvm_ResourcePoolComponent.Name
- Msvm_ResourcePoolComponent.AllocationCapabilitiesClassName
- Msvm_ResourcePoolComponent.ResourcePoolClassName
- Msvm_ResourcePoolComponent.ResourcePoolSettingDataClassName
- Msvm_ResourcePoolComponent.PhysicalDeviceClassName
- Msvm_ResourcePoolComponent.WmiFactoryCLSID
- Msvm_ResourcePoolComponent.MaxParentPools
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a0cf64a9e01d904aa4e6c6ec263fdeec92eb7c94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650912"
---
# <a name="msvm_resourcepoolcomponent-class"></a><span data-ttu-id="fac61-103">\_Класс мсвм ресаурцепулкомпонент</span><span class="sxs-lookup"><span data-stu-id="fac61-103">Msvm\_ResourcePoolComponent class</span></span>

<span data-ttu-id="fac61-104">Представляет элемент пула ресурсов платформы Microsoft Windows Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="fac61-104">Represents a resource pool element of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="fac61-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="fac61-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac61-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fac61-106">Syntax</span></span>

``` syntax
class Msvm_ResourcePoolComponent : Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
  string  AllocationCapabilitiesClassName;
  string  ResourcePoolClassName;
  string  ResourcePoolSettingDataClassName = "Msvm_ResourcePoolSettingData";
  string  PhysicalDeviceClassName;
  string  WmiFactoryCLSID;
  uint8   MaxParentPools = 0;
};
```

## <a name="members"></a><span data-ttu-id="fac61-107">Члены</span><span class="sxs-lookup"><span data-stu-id="fac61-107">Members</span></span>

<span data-ttu-id="fac61-108">Класс **мсвм \_ ресаурцепулкомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fac61-108">The **Msvm\_ResourcePoolComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="fac61-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="fac61-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fac61-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="fac61-110">Properties</span></span>

<span data-ttu-id="fac61-111">Класс **мсвм \_ ресаурцепулкомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fac61-111">The **Msvm\_ResourcePoolComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fac61-112">**аллокатионкапабилитиескласснаме**</span><span class="sxs-lookup"><span data-stu-id="fac61-112">**AllocationCapabilitiesClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fac61-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fac61-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fac61-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fac61-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fac61-115">Имя класса, производного от [**CIM \_ аллокатионкапабилитиес**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) , которое описывает возможности выделения ресурсов в этом пуле.</span><span class="sxs-lookup"><span data-stu-id="fac61-115">The name of the class derived from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) that describes the allocation capabilities of this resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="fac61-116">**ЭТОМУ**</span><span class="sxs-lookup"><span data-stu-id="fac61-116">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fac61-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fac61-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fac61-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fac61-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fac61-119">Идентификатор **GUID** , представляющий идентификатор класса COM-объекта службы.</span><span class="sxs-lookup"><span data-stu-id="fac61-119">A **GUID** that represents the class identifier of the service's COM object.</span></span> <span data-ttu-id="fac61-120">Это свойство наследуется от [**мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="fac61-120">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="fac61-121">**Контекст**</span><span class="sxs-lookup"><span data-stu-id="fac61-121">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fac61-122">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fac61-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fac61-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fac61-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fac61-124">Контекст, в котором будет выполняться вновь созданный объект.</span><span class="sxs-lookup"><span data-stu-id="fac61-124">The context in which the newly created object will run.</span></span> <span data-ttu-id="fac61-125">Это значение передается в параметре *двклсконтекст* в **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="fac61-125">This value is passed in the *dwClsContext* parameter to **CoCreateInstance**.</span></span> <span data-ttu-id="fac61-126">Это свойство наследуется от [**мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md)и всегда имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="fac61-126">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="fac61-127">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="fac61-127">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fac61-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="fac61-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fac61-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fac61-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fac61-130">**Значение true** , если этот экземпляр включен и может использоваться для выполнения клиентских запросов; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="fac61-130">**True** if this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="fac61-131">Это свойство наследуется от [**мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md)и всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="fac61-131">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="fac61-132">**макспарентпулс**</span><span class="sxs-lookup"><span data-stu-id="fac61-132">**MaxParentPools**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fac61-133">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fac61-133">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fac61-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fac61-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fac61-135">Максимальное число родительских пулов ресурсов, поддерживаемых дочерним пулом.</span><span class="sxs-lookup"><span data-stu-id="fac61-135">The maximum number of parent resource pools that a child pool supports.</span></span>

</dd> <dt>

<span data-ttu-id="fac61-136">**Name**</span><span class="sxs-lookup"><span data-stu-id="fac61-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fac61-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fac61-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fac61-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fac61-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fac61-139">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="fac61-139">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fac61-140">Строка, не зависящая от языка, которая уникальным образом идентифицирует элемент.</span><span class="sxs-lookup"><span data-stu-id="fac61-140">A language-neutral string that uniquely identifies the element.</span></span> <span data-ttu-id="fac61-141">Для предотвращения конфликтов именования предлагается следующий формат: " \| версия компонента поставщика \| ".</span><span class="sxs-lookup"><span data-stu-id="fac61-141">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="fac61-142">Например, это имя представляет версию 1,0 компонента сетевого порта эмуляции Microsoft: Microsoft \| емулатеднетворкпорткомпонент \| v 1.0.</span><span class="sxs-lookup"><span data-stu-id="fac61-142">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span> <span data-ttu-id="fac61-143">Это свойство наследуется от [**мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="fac61-143">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="fac61-144">**фисикалдевицекласснаме**</span><span class="sxs-lookup"><span data-stu-id="fac61-144">**PhysicalDeviceClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fac61-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fac61-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fac61-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fac61-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fac61-147">Имя класса, производного от [**CIM source \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , который реализует физическое устройство, из которого этот пул выделяет ресурсы.</span><span class="sxs-lookup"><span data-stu-id="fac61-147">The name of the class derived from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) that implements the physical device from which this pool allocates resources.</span></span> <span data-ttu-id="fac61-148">Это свойство может иметь **значение NULL** , если класс виртуального устройства, выделенный из этого пула, совпадает с классом физического устройства.</span><span class="sxs-lookup"><span data-stu-id="fac61-148">This property can be **Null** if the virtual device class allocated from this pool is the same as the physical device class.</span></span>

</dd> <dt>

<span data-ttu-id="fac61-149">**ресаурцепулкласснаме**</span><span class="sxs-lookup"><span data-stu-id="fac61-149">**ResourcePoolClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fac61-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fac61-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fac61-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fac61-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fac61-152">Имя класса, производного от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)) , который реализует пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fac61-152">The name of the class derived from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)) that implements the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="fac61-153">**ресаурцепулсеттингдатакласснаме**</span><span class="sxs-lookup"><span data-stu-id="fac61-153">**ResourcePoolSettingDataClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fac61-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fac61-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fac61-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fac61-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fac61-156">Имя класса, производного от значения [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)) , которое описывает параметры пула ресурсов, не связанные с выделением.</span><span class="sxs-lookup"><span data-stu-id="fac61-156">The name of the class derived from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) that describes the non-allocation related settings of the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="fac61-157">**вмифакториклсид**</span><span class="sxs-lookup"><span data-stu-id="fac61-157">**WmiFactoryCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fac61-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fac61-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fac61-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fac61-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fac61-160">Идентификатор **GUID** , представляющий идентификатор класса фабрики объектов WMI компонента.</span><span class="sxs-lookup"><span data-stu-id="fac61-160">A **GUID** that represents the class identifier of the component's WMI object factory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fac61-161">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fac61-161">Remarks</span></span>

<span data-ttu-id="fac61-162">Доступ к классу **\_ ресаурцепулкомпонент мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="fac61-162">Access to the **Msvm\_ResourcePoolComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="fac61-163">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="fac61-163">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="fac61-164">Требования</span><span class="sxs-lookup"><span data-stu-id="fac61-164">Requirements</span></span>



| <span data-ttu-id="fac61-165">Требование</span><span class="sxs-lookup"><span data-stu-id="fac61-165">Requirement</span></span> | <span data-ttu-id="fac61-166">Значение</span><span class="sxs-lookup"><span data-stu-id="fac61-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fac61-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fac61-167">Minimum supported client</span></span><br/> | <span data-ttu-id="fac61-168">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fac61-168">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fac61-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fac61-169">Minimum supported server</span></span><br/> | <span data-ttu-id="fac61-170">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fac61-170">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fac61-171">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fac61-171">End of client support</span></span><br/>    | <span data-ttu-id="fac61-172">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fac61-172">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="fac61-173">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="fac61-173">End of server support</span></span><br/>    | <span data-ttu-id="fac61-174">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fac61-174">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="fac61-175">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fac61-175">Namespace</span></span><br/>                | <span data-ttu-id="fac61-176">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="fac61-176">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fac61-177">MOF</span><span class="sxs-lookup"><span data-stu-id="fac61-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fac61-178"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fac61-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fac61-179">DLL</span><span class="sxs-lookup"><span data-stu-id="fac61-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fac61-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fac61-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fac61-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fac61-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac61-182">**Мсвм \_ виртуализатионкомпонент**</span><span class="sxs-lookup"><span data-stu-id="fac61-182">**Msvm\_VirtualizationComponent**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[<span data-ttu-id="fac61-183">**Мсвм \_ виртуализатионкомпонент**</span><span class="sxs-lookup"><span data-stu-id="fac61-183">**Msvm\_VirtualizationComponent**</span></span>](msvm-virtualizationcomponent.md)
</dt> </dl>

 

