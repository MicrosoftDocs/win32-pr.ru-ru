---
description: Связывает виртуальный коммутатор Ethernet с расширениями, привязанными к нему в данный момент.
ms.assetid: d8c87fa2-6859-49ed-abd5-32a836b00e5a
title: Класс Msvm_HostedEthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedEthernetSwitchExtension
- Msvm_HostedEthernetSwitchExtension.Antecedent
- Msvm_HostedEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cb952d42864fb6130ad6cbec09ef5eb68439f6a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810438"
---
# <a name="msvm_hostedethernetswitchextension-class"></a><span data-ttu-id="2cbeb-103">\_Класс мсвм хостедесернетсвитчекстенсион</span><span class="sxs-lookup"><span data-stu-id="2cbeb-103">Msvm\_HostedEthernetSwitchExtension class</span></span>

<span data-ttu-id="2cbeb-104">Связывает виртуальный коммутатор Ethernet с расширениями, привязанными к нему в данный момент.</span><span class="sxs-lookup"><span data-stu-id="2cbeb-104">Associates a virtual Ethernet switch to the extensions currently bound to it.</span></span>

<span data-ttu-id="2cbeb-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="2cbeb-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cbeb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cbeb-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedEthernetSwitchExtension : CIM_HostedDependency
{
  Msvm_VirtualEthernetSwitch   REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2cbeb-107">Члены</span><span class="sxs-lookup"><span data-stu-id="2cbeb-107">Members</span></span>

<span data-ttu-id="2cbeb-108">Класс **мсвм \_ хостедесернетсвитчекстенсион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2cbeb-108">The **Msvm\_HostedEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="2cbeb-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="2cbeb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2cbeb-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2cbeb-110">Properties</span></span>

<span data-ttu-id="2cbeb-111">Класс **мсвм \_ хостедесернетсвитчекстенсион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2cbeb-111">The **Msvm\_HostedEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2cbeb-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="2cbeb-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cbeb-113">Тип данных: **[ **мсвм \_ виртуалесернетсвитч**](msvm-virtualethernetswitch.md)**</span><span class="sxs-lookup"><span data-stu-id="2cbeb-113">Data type: **[**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span></span>
</dt> <dt>

<span data-ttu-id="2cbeb-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2cbeb-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cbeb-115">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="2cbeb-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="2cbeb-116">Ссылка на экземпляр класса [**мсвм \_ виртуалесернетсвитч**](msvm-virtualethernetswitch.md) , представляющий виртуальный коммутатор.</span><span class="sxs-lookup"><span data-stu-id="2cbeb-116">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="2cbeb-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="2cbeb-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cbeb-118">Тип данных: **[ **мсвм \_ есернетсвитчекстенсион**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="2cbeb-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="2cbeb-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2cbeb-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cbeb-120">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2cbeb-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2cbeb-121">Ссылка на экземпляр класса [**мсвм \_ есернетсвитчекстенсион**](msvm-ethernetswitchextension.md) , представляющий экземпляр расширения коммутатора, привязанный к виртуальному коммутатору.</span><span class="sxs-lookup"><span data-stu-id="2cbeb-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the switch extension instance bound to the virtual switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2cbeb-122">Требования</span><span class="sxs-lookup"><span data-stu-id="2cbeb-122">Requirements</span></span>



| <span data-ttu-id="2cbeb-123">Требование</span><span class="sxs-lookup"><span data-stu-id="2cbeb-123">Requirement</span></span> | <span data-ttu-id="2cbeb-124">Значение</span><span class="sxs-lookup"><span data-stu-id="2cbeb-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbeb-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2cbeb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2cbeb-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2cbeb-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2cbeb-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2cbeb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2cbeb-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2cbeb-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2cbeb-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2cbeb-129">Namespace</span></span><br/>                | <span data-ttu-id="2cbeb-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2cbeb-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2cbeb-131">MOF</span><span class="sxs-lookup"><span data-stu-id="2cbeb-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2cbeb-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2cbeb-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2cbeb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2cbeb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cbeb-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2cbeb-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

