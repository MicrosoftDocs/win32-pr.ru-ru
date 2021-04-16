---
description: Регистрирует службу, которая предоставляет объекты, относящиеся к ресурсам виртуальной машины.
ms.assetid: 85782C4D-E0A3-4EED-9A26-7928862C559B
title: Класс Msvm_VirtualSystemResourceRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceRegistration
- Msvm_VirtualSystemResourceRegistration.ResourceType
- Msvm_VirtualSystemResourceRegistration.Component
- Msvm_VirtualSystemResourceRegistration.IsRootDevice
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7cef3699de973bd22985215a64100c594f223be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540274"
---
# <a name="msvm_virtualsystemresourceregistration-class"></a><span data-ttu-id="be72f-103">\_Класс мсвм виртуалсистемресаурцерегистратион</span><span class="sxs-lookup"><span data-stu-id="be72f-103">Msvm\_VirtualSystemResourceRegistration class</span></span>

<span data-ttu-id="be72f-104">Регистрирует службу, которая предоставляет объекты, относящиеся к ресурсам виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be72f-104">Registers a service that provides virtual machine-specific resource-related objects.</span></span>

<span data-ttu-id="be72f-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="be72f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="be72f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be72f-106">Syntax</span></span>

``` syntax
class Msvm_VirtualSystemResourceRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition         REF ResourceType;
  Msvm_VirtualSystemResourceComponent REF Component;
  boolean                                 IsRootDevice = False;
};
```

## <a name="members"></a><span data-ttu-id="be72f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="be72f-107">Members</span></span>

<span data-ttu-id="be72f-108">Класс **мсвм \_ виртуалсистемресаурцерегистратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="be72f-108">The **Msvm\_VirtualSystemResourceRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="be72f-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="be72f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be72f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="be72f-110">Properties</span></span>

<span data-ttu-id="be72f-111">Класс **мсвм \_ виртуалсистемресаурцерегистратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="be72f-111">The **Msvm\_VirtualSystemResourceRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be72f-112">**Компонент**</span><span class="sxs-lookup"><span data-stu-id="be72f-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be72f-113">Тип данных: **[ **мсвм \_ виртуалсистемресаурцекомпонент**](msvm-virtualsystemresourcecomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="be72f-113">Data type: **[**Msvm\_VirtualSystemResourceComponent**](msvm-virtualsystemresourcecomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="be72f-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be72f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be72f-115">Ссылка на экземпляр, описывающий COM-объект, реализующий этот класс.</span><span class="sxs-lookup"><span data-stu-id="be72f-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="be72f-116">**исрутдевице**</span><span class="sxs-lookup"><span data-stu-id="be72f-116">**IsRootDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be72f-117">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be72f-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be72f-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be72f-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be72f-119">**Значение true** , если эта регистрация указывает, является ли указанный тип ресурса корневым (или родительским) устройством для этой службы; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="be72f-119">**True** if this registration indicates whether the specified resource type is the root (or parent-less) device for this service; otherwise, **False**.</span></span> <span data-ttu-id="be72f-120">Если **исрутдевице** имеет значение **true**, может существовать только одна регистрация.</span><span class="sxs-lookup"><span data-stu-id="be72f-120">Only one registration can exist when **IsRootDevice** is set to **True**.</span></span> <span data-ttu-id="be72f-121">В противном случае эта регистрация представляет сопоставление с подсистемой устройства.</span><span class="sxs-lookup"><span data-stu-id="be72f-121">Otherwise, this registration represents a mapping to a sub-device.</span></span> <span data-ttu-id="be72f-122">Этому свойству всегда присвоено значение **false**.</span><span class="sxs-lookup"><span data-stu-id="be72f-122">This property is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="be72f-123">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="be72f-123">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be72f-124">Тип данных: **[ **мсвм \_ ресаурцетипедефинитион**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="be72f-124">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="be72f-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be72f-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be72f-126">Ссылка на экземпляр, описывающий тип ресурса, поддерживаемый службой.</span><span class="sxs-lookup"><span data-stu-id="be72f-126">A reference to an instance that describes a resource type supported by the service.</span></span> <span data-ttu-id="be72f-127">Это свойство наследуется от [**мсвм \_ виртуализатионкомпонентрегистратион**](msvm-virtualizationcomponentregistration.md).</span><span class="sxs-lookup"><span data-stu-id="be72f-127">This property is inherited from [**Msvm\_VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be72f-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be72f-128">Remarks</span></span>

<span data-ttu-id="be72f-129">Доступ к классу **\_ виртуалсистемресаурцерегистратион мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="be72f-129">Access to the **Msvm\_VirtualSystemResourceRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="be72f-130">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="be72f-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="be72f-131">Требования</span><span class="sxs-lookup"><span data-stu-id="be72f-131">Requirements</span></span>



| <span data-ttu-id="be72f-132">Требование</span><span class="sxs-lookup"><span data-stu-id="be72f-132">Requirement</span></span> | <span data-ttu-id="be72f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="be72f-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be72f-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be72f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="be72f-135">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="be72f-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="be72f-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be72f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="be72f-137">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="be72f-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="be72f-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="be72f-138">End of client support</span></span><br/>    | <span data-ttu-id="be72f-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="be72f-139">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="be72f-140">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="be72f-140">End of server support</span></span><br/>    | <span data-ttu-id="be72f-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="be72f-141">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="be72f-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="be72f-142">Namespace</span></span><br/>                | <span data-ttu-id="be72f-143">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="be72f-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="be72f-144">MOF</span><span class="sxs-lookup"><span data-stu-id="be72f-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be72f-145"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be72f-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="be72f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="be72f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be72f-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="be72f-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="be72f-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be72f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be72f-149">**Мсвм \_ виртуализатионкомпонентрегистратион**</span><span class="sxs-lookup"><span data-stu-id="be72f-149">**Msvm\_VirtualizationComponentRegistration**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[<span data-ttu-id="be72f-150">**Мсвм \_ виртуализатионкомпонентрегистратион**</span><span class="sxs-lookup"><span data-stu-id="be72f-150">**Msvm\_VirtualizationComponentRegistration**</span></span>](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

