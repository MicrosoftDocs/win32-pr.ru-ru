---
description: Представляет службу платформы Hyper-V Microsoft Windows.
ms.assetid: 309EFE4C-EEA4-454C-943D-CBF99D64FE15
title: Класс Msvm_VirtualizationComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponent
- Msvm_VirtualizationComponent.CLSID
- Msvm_VirtualizationComponent.Context
- Msvm_VirtualizationComponent.Enabled
- Msvm_VirtualizationComponent.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 19811b224a4e93e85420539248b7d010491335aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682507"
---
# <a name="msvm_virtualizationcomponent-class"></a><span data-ttu-id="44c0e-103">\_Класс мсвм виртуализатионкомпонент</span><span class="sxs-lookup"><span data-stu-id="44c0e-103">Msvm\_VirtualizationComponent class</span></span>

<span data-ttu-id="44c0e-104">Представляет службу платформы Hyper-V Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="44c0e-104">Represents a service of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="44c0e-105">Следующий синтаксис представляет собой упрощенный код MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="44c0e-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="44c0e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44c0e-106">Syntax</span></span>

``` syntax
[Abstract]
class Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="44c0e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="44c0e-107">Members</span></span>

<span data-ttu-id="44c0e-108">Класс **мсвм \_ виртуализатионкомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="44c0e-108">The **Msvm\_VirtualizationComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="44c0e-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="44c0e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44c0e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="44c0e-110">Properties</span></span>

<span data-ttu-id="44c0e-111">Класс **мсвм \_ виртуализатионкомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="44c0e-111">The **Msvm\_VirtualizationComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44c0e-112">**ЭТОМУ**</span><span class="sxs-lookup"><span data-stu-id="44c0e-112">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c0e-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="44c0e-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44c0e-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="44c0e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44c0e-115">Идентификатор **GUID** , представляющий идентификатор класса COM-объекта службы.</span><span class="sxs-lookup"><span data-stu-id="44c0e-115">A **GUID** that represents the class identifier of the service's COM object.</span></span>

</dd> <dt>

<span data-ttu-id="44c0e-116">**Контекст**</span><span class="sxs-lookup"><span data-stu-id="44c0e-116">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c0e-117">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44c0e-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44c0e-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="44c0e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c0e-119">Квалификаторы: **экспериментальные**</span><span class="sxs-lookup"><span data-stu-id="44c0e-119">Qualifiers: **Experimental**</span></span>
</dt> </dl>

<span data-ttu-id="44c0e-120">Контекст, в котором будет выполняться вновь созданный объект.</span><span class="sxs-lookup"><span data-stu-id="44c0e-120">The context in which the newly created object will run.</span></span> <span data-ttu-id="44c0e-121">Это значение передается в параметре *двклсконтекст* в [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="44c0e-121">This value is passed in the *dwClsContext* parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="44c0e-122">Это свойство всегда имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="44c0e-122">This property is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="44c0e-123">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="44c0e-123">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c0e-124">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="44c0e-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44c0e-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="44c0e-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44c0e-126">**Значение true** , если этот экземпляр включен и может использоваться для выполнения клиентских запросов; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="44c0e-126">**True** is this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="44c0e-127">Это свойство всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="44c0e-127">This property is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="44c0e-128">**Name**</span><span class="sxs-lookup"><span data-stu-id="44c0e-128">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44c0e-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="44c0e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44c0e-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="44c0e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44c0e-131">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="44c0e-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="44c0e-132">Строка, не зависящая от языка, которая уникально идентифицирует службу.</span><span class="sxs-lookup"><span data-stu-id="44c0e-132">A language-neutral string that uniquely identifies the service.</span></span> <span data-ttu-id="44c0e-133">Для предотвращения конфликтов именования предлагается следующий формат: " \| версия компонента поставщика \| ".</span><span class="sxs-lookup"><span data-stu-id="44c0e-133">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="44c0e-134">Например, это имя представляет версию 1,0 компонента сетевого порта эмуляции Microsoft: Microsoft \| емулатеднетворкпорткомпонент \| v 1.0.</span><span class="sxs-lookup"><span data-stu-id="44c0e-134">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44c0e-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44c0e-135">Remarks</span></span>

<span data-ttu-id="44c0e-136">Доступ к классу **\_ виртуализатионкомпонент мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="44c0e-136">Access to the **Msvm\_VirtualizationComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="44c0e-137">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="44c0e-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="44c0e-138">Требования</span><span class="sxs-lookup"><span data-stu-id="44c0e-138">Requirements</span></span>



| <span data-ttu-id="44c0e-139">Требование</span><span class="sxs-lookup"><span data-stu-id="44c0e-139">Requirement</span></span> | <span data-ttu-id="44c0e-140">Значение</span><span class="sxs-lookup"><span data-stu-id="44c0e-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44c0e-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44c0e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="44c0e-142">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="44c0e-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="44c0e-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44c0e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="44c0e-144">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="44c0e-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="44c0e-145">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="44c0e-145">End of client support</span></span><br/>    | <span data-ttu-id="44c0e-146">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="44c0e-146">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="44c0e-147">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="44c0e-147">End of server support</span></span><br/>    | <span data-ttu-id="44c0e-148">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="44c0e-148">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="44c0e-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="44c0e-149">Namespace</span></span><br/>                | <span data-ttu-id="44c0e-150">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="44c0e-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="44c0e-151">MOF</span><span class="sxs-lookup"><span data-stu-id="44c0e-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44c0e-152"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44c0e-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="44c0e-153">DLL</span><span class="sxs-lookup"><span data-stu-id="44c0e-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44c0e-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="44c0e-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

