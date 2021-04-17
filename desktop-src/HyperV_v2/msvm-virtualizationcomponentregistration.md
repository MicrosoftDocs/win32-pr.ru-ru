---
description: Представляет регистрацию службы на Microsoft Hyper-Vной платформе.
ms.assetid: 706557C2-49D6-453F-9DC0-2C655888EEBE
title: Класс Msvm_VirtualizationComponentRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponentRegistration
- Msvm_VirtualizationComponentRegistration.Component
- Msvm_VirtualizationComponentRegistration.ResourceType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e9704dcade0474a10ca60383280941ec2e3591b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682505"
---
# <a name="msvm_virtualizationcomponentregistration-class"></a><span data-ttu-id="c7401-103">\_Класс мсвм виртуализатионкомпонентрегистратион</span><span class="sxs-lookup"><span data-stu-id="c7401-103">Msvm\_VirtualizationComponentRegistration class</span></span>

<span data-ttu-id="c7401-104">Представляет регистрацию службы на Microsoft Hyper-Vной платформе.</span><span class="sxs-lookup"><span data-stu-id="c7401-104">Represents the registration of a service in the Microsoft Hyper-V platform.</span></span>

<span data-ttu-id="c7401-105">Следующий синтаксис представляет собой упрощенный код MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="c7401-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7401-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7401-106">Syntax</span></span>

``` syntax
class Msvm_VirtualizationComponentRegistration
{
  Msvm_VirtualizationComponent REF Component;
  Msvm_ResourceTypeDefinition  REF ResourceType;
};
```

## <a name="members"></a><span data-ttu-id="c7401-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c7401-107">Members</span></span>

<span data-ttu-id="c7401-108">Класс **мсвм \_ виртуализатионкомпонентрегистратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c7401-108">The **Msvm\_VirtualizationComponentRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="c7401-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c7401-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7401-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c7401-110">Properties</span></span>

<span data-ttu-id="c7401-111">Класс **мсвм \_ виртуализатионкомпонентрегистратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c7401-111">The **Msvm\_VirtualizationComponentRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7401-112">**Компонент**</span><span class="sxs-lookup"><span data-stu-id="c7401-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7401-113">Тип данных: **[ **мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="c7401-113">Data type: **[**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c7401-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7401-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7401-115">Ссылка на экземпляр, описывающий COM-объект, реализующий этот класс.</span><span class="sxs-lookup"><span data-stu-id="c7401-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="c7401-116">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="c7401-116">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7401-117">Тип данных: **[ **мсвм \_ ресаурцетипедефинитион**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="c7401-117">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c7401-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7401-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7401-119">Ссылка на экземпляр, описывающий тип ресурса, поддерживаемый службой.</span><span class="sxs-lookup"><span data-stu-id="c7401-119">A reference to an instance that describes a resource type supported by the service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7401-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7401-120">Remarks</span></span>

<span data-ttu-id="c7401-121">Доступ к классу **\_ виртуализатионкомпонентрегистратион мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="c7401-121">Access to the **Msvm\_VirtualizationComponentRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c7401-122">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c7401-122">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7401-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c7401-123">Requirements</span></span>



| <span data-ttu-id="c7401-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c7401-124">Requirement</span></span> | <span data-ttu-id="c7401-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c7401-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7401-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7401-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c7401-127">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c7401-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c7401-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7401-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c7401-129">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c7401-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7401-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c7401-130">End of client support</span></span><br/>    | <span data-ttu-id="c7401-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c7401-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c7401-132">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="c7401-132">End of server support</span></span><br/>    | <span data-ttu-id="c7401-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c7401-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c7401-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c7401-134">Namespace</span></span><br/>                | <span data-ttu-id="c7401-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c7401-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c7401-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c7401-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7401-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7401-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7401-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c7401-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7401-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7401-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

