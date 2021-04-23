---
description: Представляет службу виртуального устройства платформы Microsoft Windows Hyper-V.
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Класс Msvm_VirtualSystemResourceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceComponent
- Msvm_VirtualSystemResourceComponent.Name
- Msvm_VirtualSystemResourceComponent.CLSID
- Msvm_VirtualSystemResourceComponent.Context
- Msvm_VirtualSystemResourceComponent.Enabled
- Msvm_VirtualSystemResourceComponent.AdditionalClassNames
- Msvm_VirtualSystemResourceComponent.Type
- Msvm_VirtualSystemResourceComponent.HotAdd
- Msvm_VirtualSystemResourceComponent.HotRemove
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 81c2d31a6497325ac77003ded266333518de890a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662231"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a><span data-ttu-id="f4219-103">\_Класс мсвм виртуалсистемресаурцекомпонент</span><span class="sxs-lookup"><span data-stu-id="f4219-103">Msvm\_VirtualSystemResourceComponent class</span></span>

<span data-ttu-id="f4219-104">Представляет службу виртуального устройства платформы Microsoft Windows Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="f4219-104">Represents a virtual device service of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="f4219-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f4219-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4219-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4219-106">Syntax</span></span>

``` syntax
class Msvm_VirtualSystemResourceComponent : Msvm_VirtualizationComponent
{
  string  Name;
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  AdditionalClassNames[];
  uint16  Type = 1;
  boolean HotAdd = False;
  boolean HotRemove = False;
};
```

## <a name="members"></a><span data-ttu-id="f4219-107">Члены</span><span class="sxs-lookup"><span data-stu-id="f4219-107">Members</span></span>

<span data-ttu-id="f4219-108">Класс **мсвм \_ виртуалсистемресаурцекомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f4219-108">The **Msvm\_VirtualSystemResourceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="f4219-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="f4219-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f4219-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f4219-110">Properties</span></span>

<span data-ttu-id="f4219-111">Класс **мсвм \_ виртуалсистемресаурцекомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f4219-111">The **Msvm\_VirtualSystemResourceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4219-112">**аддитионалкласснамес**</span><span class="sxs-lookup"><span data-stu-id="f4219-112">**AdditionalClassNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4219-113">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="f4219-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f4219-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4219-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4219-115">Массив строк, содержащий дополнительные классы, не связанные с взаимоассоциациями, на которые ссылается этот экземпляр **\_ виртуалсистемресаурцекомпонент мсвм** .</span><span class="sxs-lookup"><span data-stu-id="f4219-115">An array of strings containing additional non-association classes surfaced by this **Msvm\_VirtualSystemResourceComponent** instance.</span></span> <span data-ttu-id="f4219-116">Эти классы должны быть производными от [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) или [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="f4219-116">These classes must derive from neither [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) nor [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="f4219-117">**ЭТОМУ**</span><span class="sxs-lookup"><span data-stu-id="f4219-117">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4219-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4219-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4219-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4219-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4219-120">Идентификатор GUID, представляющий идентификатор класса COM-объекта службы.</span><span class="sxs-lookup"><span data-stu-id="f4219-120">A GUID that represents the class identifier of the service's COM object.</span></span> <span data-ttu-id="f4219-121">Это свойство наследуется от [**мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="f4219-121">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4219-122">**Контекст**</span><span class="sxs-lookup"><span data-stu-id="f4219-122">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4219-123">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4219-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4219-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4219-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4219-125">Контекст, в котором будет выполняться вновь созданный объект.</span><span class="sxs-lookup"><span data-stu-id="f4219-125">The context in which the newly created object will run.</span></span> <span data-ttu-id="f4219-126">Это значение передается в параметре *двклсконтекст* в [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="f4219-126">This value is passed in the *dwClsContext* parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="f4219-127">Это свойство наследуется от [**мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md)и всегда имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="f4219-127">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="f4219-128">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="f4219-128">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4219-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f4219-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f4219-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4219-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4219-131">**Значение true** , если этот экземпляр включен и может использоваться для выполнения клиентских запросов; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f4219-131">**True** if this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="f4219-132">Это свойство наследуется от [**мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md)и всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="f4219-132">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="f4219-133">**хотадд**</span><span class="sxs-lookup"><span data-stu-id="f4219-133">**HotAdd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4219-134">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f4219-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f4219-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4219-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4219-136">**Значение true** , если этот экземпляр можно добавить в виртуальную машину с помощью горячего подключения; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f4219-136">**True** if this instance can be hot-added to a virtual machine; otherwise, **False**.</span></span> <span data-ttu-id="f4219-137">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="f4219-137">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="f4219-138">**хотремове**</span><span class="sxs-lookup"><span data-stu-id="f4219-138">**HotRemove**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4219-139">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f4219-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f4219-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4219-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4219-141">**Значение true** , если этот экземпляр можно удалить с виртуальной машины. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f4219-141">**True** if this instance can be hot-removed from a virtual machine; otherwise, **False**.</span></span> <span data-ttu-id="f4219-142">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="f4219-142">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="f4219-143">**Name**</span><span class="sxs-lookup"><span data-stu-id="f4219-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4219-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4219-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4219-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4219-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4219-146">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="f4219-146">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f4219-147">Строка, не зависящая от языка, которая уникально идентифицирует службу.</span><span class="sxs-lookup"><span data-stu-id="f4219-147">A language-neutral string that uniquely identifies the service.</span></span> <span data-ttu-id="f4219-148">Для предотвращения конфликтов именования предлагается следующий формат: " \| версия компонента поставщика \| ".</span><span class="sxs-lookup"><span data-stu-id="f4219-148">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="f4219-149">Например, это имя представляет версию 1,0 компонента сетевого порта эмуляции Microsoft: Microsoft \| емулатеднетворкпорткомпонент \| v 1.0.</span><span class="sxs-lookup"><span data-stu-id="f4219-149">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span> <span data-ttu-id="f4219-150">Это свойство наследуется от [**мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="f4219-150">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4219-151">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f4219-151">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4219-152">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4219-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4219-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4219-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4219-154">Отношение объекта WMI, описываемого здесь к виртуальному устройству.</span><span class="sxs-lookup"><span data-stu-id="f4219-154">The relationship of the WMI object that is described here with the virtual device.</span></span>



| <span data-ttu-id="f4219-155">Значение</span><span class="sxs-lookup"><span data-stu-id="f4219-155">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="f4219-156">Значение</span><span class="sxs-lookup"><span data-stu-id="f4219-156">Meaning</span></span>                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <span data-ttu-id="f4219-157"><dt>**"Не изменять"**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f4219-157"><dt>**"Not Changeable"**</dt> <dt>0</dt></span></span> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <span data-ttu-id="f4219-158"><dt>**"Singleton"**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f4219-158"><dt>**"Singleton"**</dt> <dt>1</dt></span></span> </dl>                     | <span data-ttu-id="f4219-159">Singleton — это объект WMI верхнего уровня, который связан с виртуальным устройством 1:1 и может существовать только один раз для каждой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f4219-159">Singleton is a top level WMI object that is tied 1:1 with a Virtual Device and can only exist once per virtual machine.</span></span> <span data-ttu-id="f4219-160">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4219-160">This is the default value.</span></span><br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <span data-ttu-id="f4219-161"><dt>**"Многоэкземплярный"**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f4219-161"><dt>**"MultiInstance"**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="f4219-162">Многоэкземпляр — это объект WMI верхнего уровня, который может существовать несколько раз для каждой виртуальной машины и связан с виртуальным устройством 1:1.</span><span class="sxs-lookup"><span data-stu-id="f4219-162">MultiInstance is a top level WMI object that can exist multiple times per virtual machine and is tied 1:1 with a Virtual Device.</span></span><br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <span data-ttu-id="f4219-163"><dt>**"Подустройство"**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f4219-163"><dt>**"Subdevice"**</dt> <dt>3</dt></span></span> </dl>                     | <span data-ttu-id="f4219-164">Подустройство — это объект WMI, который не имеет родительской ссылки, но управляется только одним виртуальным устройством, которое может существовать только один раз для каждой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f4219-164">Subdevice is a WMI object that has not parent reference but is controlled by only one Virtual Device that can exist only once per virtual machine.</span></span> <span data-ttu-id="f4219-165">Однако объект WMI может существовать несколько раз.</span><span class="sxs-lookup"><span data-stu-id="f4219-165">The WMI object though can exist multiples times.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4219-166">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4219-166">Remarks</span></span>

<span data-ttu-id="f4219-167">Доступ к классу **\_ виртуалсистемресаурцекомпонент мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="f4219-167">Access to the **Msvm\_VirtualSystemResourceComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f4219-168">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f4219-168">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4219-169">Требования</span><span class="sxs-lookup"><span data-stu-id="f4219-169">Requirements</span></span>



| <span data-ttu-id="f4219-170">Требование</span><span class="sxs-lookup"><span data-stu-id="f4219-170">Requirement</span></span> | <span data-ttu-id="f4219-171">Значение</span><span class="sxs-lookup"><span data-stu-id="f4219-171">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4219-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f4219-172">Minimum supported client</span></span><br/> | <span data-ttu-id="f4219-173">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f4219-173">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f4219-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f4219-174">Minimum supported server</span></span><br/> | <span data-ttu-id="f4219-175">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f4219-175">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f4219-176">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f4219-176">End of client support</span></span><br/>    | <span data-ttu-id="f4219-177">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f4219-177">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f4219-178">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f4219-178">End of server support</span></span><br/>    | <span data-ttu-id="f4219-179">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f4219-179">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f4219-180">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f4219-180">Namespace</span></span><br/>                | <span data-ttu-id="f4219-181">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f4219-181">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f4219-182">MOF</span><span class="sxs-lookup"><span data-stu-id="f4219-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4219-183"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4219-183"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4219-184">DLL</span><span class="sxs-lookup"><span data-stu-id="f4219-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4219-185"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f4219-185"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f4219-186">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4219-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4219-187">**Мсвм \_ виртуализатионкомпонент**</span><span class="sxs-lookup"><span data-stu-id="f4219-187">**Msvm\_VirtualizationComponent**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[<span data-ttu-id="f4219-188">**Мсвм \_ виртуализатионкомпонент**</span><span class="sxs-lookup"><span data-stu-id="f4219-188">**Msvm\_VirtualizationComponent**</span></span>](msvm-virtualizationcomponent.md)
</dt> </dl>

 

