---
description: Определяет связь между установленным расширением коммутатора Ethernet и расширением коммутатора Ethernet.
ms.assetid: 306658ed-03a4-49fa-8704-f4b83a4bdd4f
title: Класс Msvm_ConcreteDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteDependency
- Msvm_ConcreteDependency.Antecedent
- Msvm_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c74a8431b03389a106cd127933a2c78b842385f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263854"
---
# <a name="msvm_concretedependency-class"></a><span data-ttu-id="4bb27-103">\_Класс мсвм конкретедепенденци</span><span class="sxs-lookup"><span data-stu-id="4bb27-103">Msvm\_ConcreteDependency class</span></span>

<span data-ttu-id="4bb27-104">Определяет связь между установленным расширением коммутатора Ethernet и расширением коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="4bb27-104">Defines the association between an installed Ethernet switch extension and an Ethernet switch extension.</span></span>

<span data-ttu-id="4bb27-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="4bb27-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bb27-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4bb27-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteDependency : CIM_ConcreteDependency
{
  Msvm_InstalledEthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension          REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4bb27-107">Члены</span><span class="sxs-lookup"><span data-stu-id="4bb27-107">Members</span></span>

<span data-ttu-id="4bb27-108">Класс **мсвм \_ конкретедепенденци** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4bb27-108">The **Msvm\_ConcreteDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="4bb27-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="4bb27-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4bb27-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="4bb27-110">Properties</span></span>

<span data-ttu-id="4bb27-111">Класс **мсвм \_ конкретедепенденци** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4bb27-111">The **Msvm\_ConcreteDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4bb27-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="4bb27-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bb27-113">Тип данных: **[ **мсвм \_ инсталледесернетсвитчекстенсион**](msvm-installedethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="4bb27-113">Data type: **[**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4bb27-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4bb27-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4bb27-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="4bb27-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4bb27-116">Ссылка на экземпляр класса [**мсвм \_ инсталледесернетсвитчекстенсион**](msvm-installedethernetswitchextension.md) , представляющий компонент расширения виртуального коммутатора Ethernet, установленный в системе.</span><span class="sxs-lookup"><span data-stu-id="4bb27-116">A reference to an instance of the [**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) class that represents a virtual Ethernet switch extension component installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="4bb27-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="4bb27-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bb27-118">Тип данных: **[ **мсвм \_ есернетсвитчекстенсион**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="4bb27-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4bb27-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4bb27-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4bb27-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="4bb27-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4bb27-121">Ссылка на экземпляр класса [**мсвм \_ есернетсвитчекстенсион**](msvm-ethernetswitchextension.md) , представляющий вхождение **предшествующей задачи** , привязанной к определенному виртуальному коммутатору Ethernet.</span><span class="sxs-lookup"><span data-stu-id="4bb27-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the occurrence of the **Antecedent** bound to a specific virtual Ethernet switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4bb27-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4bb27-122">Requirements</span></span>



| <span data-ttu-id="4bb27-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4bb27-123">Requirement</span></span> | <span data-ttu-id="4bb27-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4bb27-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bb27-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4bb27-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4bb27-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4bb27-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4bb27-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4bb27-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4bb27-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4bb27-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4bb27-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4bb27-129">Namespace</span></span><br/>                | <span data-ttu-id="4bb27-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4bb27-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4bb27-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4bb27-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bb27-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4bb27-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4bb27-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4bb27-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bb27-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4bb27-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

