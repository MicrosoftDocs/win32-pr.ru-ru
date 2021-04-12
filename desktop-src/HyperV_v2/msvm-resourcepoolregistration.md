---
description: Регистрирует службу, которая предоставляет объекты, связанные с пулом глобальных ресурсов.
ms.assetid: B602F6E1-2889-43CF-AAF1-40F339231DB4
title: Класс Msvm_ResourcePoolRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolRegistration
- Msvm_ResourcePoolRegistration.ResourceType
- Msvm_ResourcePoolRegistration.Component
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6eecfefc8c542eeb3a06c509533060f8036d447e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156686"
---
# <a name="msvm_resourcepoolregistration-class"></a><span data-ttu-id="f040d-103">\_Класс мсвм ресаурцепулрегистратион</span><span class="sxs-lookup"><span data-stu-id="f040d-103">Msvm\_ResourcePoolRegistration class</span></span>

<span data-ttu-id="f040d-104">Регистрирует службу, которая предоставляет объекты, связанные с пулом глобальных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f040d-104">Registers a service that provides global resource pool-related objects.</span></span>

<span data-ttu-id="f040d-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f040d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f040d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f040d-106">Syntax</span></span>

``` syntax
class Msvm_ResourcePoolRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition REF ResourceType;
  Msvm_ResourcePoolComponent  REF Component;
};
```

## <a name="members"></a><span data-ttu-id="f040d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="f040d-107">Members</span></span>

<span data-ttu-id="f040d-108">Класс **мсвм \_ ресаурцепулрегистратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f040d-108">The **Msvm\_ResourcePoolRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="f040d-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="f040d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f040d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f040d-110">Properties</span></span>

<span data-ttu-id="f040d-111">Класс **мсвм \_ ресаурцепулрегистратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f040d-111">The **Msvm\_ResourcePoolRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f040d-112">**Компонент**</span><span class="sxs-lookup"><span data-stu-id="f040d-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f040d-113">Тип данных: **[ **мсвм \_ ресаурцепулкомпонент**](msvm-resourcepoolcomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="f040d-113">Data type: **[**Msvm\_ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f040d-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f040d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f040d-115">Ссылка на экземпляр, описывающий COM-объект, реализующий этот класс.</span><span class="sxs-lookup"><span data-stu-id="f040d-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="f040d-116">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="f040d-116">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f040d-117">Тип данных: **[ **мсвм \_ ресаурцетипедефинитион**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="f040d-117">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f040d-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f040d-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f040d-119">Ссылка на экземпляр, описывающий тип ресурса, поддерживаемый службой.</span><span class="sxs-lookup"><span data-stu-id="f040d-119">A reference to an instance that describes a resource type supported by the service.</span></span> <span data-ttu-id="f040d-120">Это свойство наследуется от [**мсвм \_ виртуализатионкомпонентрегистратион**](msvm-virtualizationcomponentregistration.md).</span><span class="sxs-lookup"><span data-stu-id="f040d-120">This property is inherited from [**Msvm\_VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f040d-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f040d-121">Remarks</span></span>

<span data-ttu-id="f040d-122">Доступ к классу **\_ ресаурцепулрегистратион мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="f040d-122">Access to the **Msvm\_ResourcePoolRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f040d-123">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f040d-123">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f040d-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f040d-124">Requirements</span></span>



| <span data-ttu-id="f040d-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f040d-125">Requirement</span></span> | <span data-ttu-id="f040d-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f040d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f040d-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f040d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f040d-128">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f040d-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f040d-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f040d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f040d-130">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f040d-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f040d-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f040d-131">End of client support</span></span><br/>    | <span data-ttu-id="f040d-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f040d-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f040d-133">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f040d-133">End of server support</span></span><br/>    | <span data-ttu-id="f040d-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f040d-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f040d-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f040d-135">Namespace</span></span><br/>                | <span data-ttu-id="f040d-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f040d-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f040d-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f040d-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f040d-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f040d-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f040d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f040d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f040d-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f040d-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f040d-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f040d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f040d-142">**Мсвм \_ виртуализатионкомпонентрегистратион**</span><span class="sxs-lookup"><span data-stu-id="f040d-142">**Msvm\_VirtualizationComponentRegistration**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[<span data-ttu-id="f040d-143">**Мсвм \_ виртуализатионкомпонентрегистратион**</span><span class="sxs-lookup"><span data-stu-id="f040d-143">**Msvm\_VirtualizationComponentRegistration**</span></span>](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

