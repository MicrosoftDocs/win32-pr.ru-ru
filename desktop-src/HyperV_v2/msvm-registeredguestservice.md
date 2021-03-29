---
description: Представляет связь между экземпляром Мсвм \_ гуестсервицеинтерфацекомпонент и экземпляром мсвм \_ гуестсервице, который представляет службу, работающую в гостевой системе.
ms.assetid: 246CFAC1-7D83-4DE7-B9D3-96326511E08B
title: Класс Msvm_RegisteredGuestService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredGuestService
- Msvm_RegisteredGuestService.Antecedent
- Msvm_RegisteredGuestService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 850d7f081b070fd34ef11bc56e8cd1f914e498b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814216"
---
# <a name="msvm_registeredguestservice-class"></a><span data-ttu-id="f6c7e-103">\_Класс мсвм регистередгуестсервице</span><span class="sxs-lookup"><span data-stu-id="f6c7e-103">Msvm\_RegisteredGuestService class</span></span>

<span data-ttu-id="f6c7e-104">Представляет связь между экземпляром [**мсвм \_ гуестсервицеинтерфацекомпонент**](msvm-guestserviceinterfacecomponent.md) и экземпляром [**мсвм \_ гуестсервице**](msvm-guestservice.md), который представляет службу, работающую в гостевой системе.</span><span class="sxs-lookup"><span data-stu-id="f6c7e-104">Represents an association between an instance of [**Msvm\_GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) and an instance of [**Msvm\_GuestService**](msvm-guestservice.md), which represents a service running in the guest.</span></span> <span data-ttu-id="f6c7e-105">Этот класс является производным от [**класса \_ зависимостей CIM**](/windows/desktop/CIMWin32Prov/cim-dependency) .</span><span class="sxs-lookup"><span data-stu-id="f6c7e-105">This class derives from the [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency) class.</span></span>

<span data-ttu-id="f6c7e-106">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f6c7e-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6c7e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6c7e-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RegisteredGuestService : CIM_Dependency
{
  Msvm_GuestServiceInterfaceComponent REF Antecedent;
  Msvm_GuestService                   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f6c7e-108">Члены</span><span class="sxs-lookup"><span data-stu-id="f6c7e-108">Members</span></span>

<span data-ttu-id="f6c7e-109">Класс **мсвм \_ регистередгуестсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f6c7e-109">The **Msvm\_RegisteredGuestService** class has these types of members:</span></span>

-   [<span data-ttu-id="f6c7e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f6c7e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6c7e-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f6c7e-111">Properties</span></span>

<span data-ttu-id="f6c7e-112">Класс **мсвм \_ регистередгуестсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f6c7e-112">The **Msvm\_RegisteredGuestService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6c7e-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="f6c7e-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6c7e-114">Тип данных: **[ **мсвм \_ гуестсервицеинтерфацекомпонент**](msvm-guestserviceinterfacecomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="f6c7e-114">Data type: **[**Msvm\_GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f6c7e-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6c7e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6c7e-116">Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="f6c7e-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f6c7e-117">Ссылка на компонент интерфейса гостевой службы в этой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="f6c7e-117">Reference to the guest service interface component in this association.</span></span>

</dd> <dt>

<span data-ttu-id="f6c7e-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="f6c7e-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6c7e-119">Тип данных: **[ **мсвм \_ гуестсервице**](msvm-guestservice.md)**</span><span class="sxs-lookup"><span data-stu-id="f6c7e-119">Data type: **[**Msvm\_GuestService**](msvm-guestservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f6c7e-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6c7e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6c7e-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ зависимость CIM. Dependent")</span><span class="sxs-lookup"><span data-stu-id="f6c7e-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f6c7e-122">Ссылка на зарегистрированную гостевую службу, которая зависит от свойства **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="f6c7e-122">Reference to the registered guest service that is dependent on the **Antecedent** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6c7e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="f6c7e-123">Requirements</span></span>



| <span data-ttu-id="f6c7e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="f6c7e-124">Requirement</span></span> | <span data-ttu-id="f6c7e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="f6c7e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c7e-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6c7e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f6c7e-127">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f6c7e-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f6c7e-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6c7e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f6c7e-129">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6c7e-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f6c7e-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f6c7e-130">Namespace</span></span><br/>                | <span data-ttu-id="f6c7e-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f6c7e-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f6c7e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f6c7e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6c7e-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6c7e-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6c7e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f6c7e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6c7e-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6c7e-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f6c7e-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6c7e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6c7e-137">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="f6c7e-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="f6c7e-138">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="f6c7e-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

