---
description: Представляет связь между расширением родительского коммутатора Ethernet и расширением дочернего коммутатора Ethernet.
ms.assetid: a0a60214-d85d-4c64-b720-1c34abc25287
title: Класс Msvm_ParentEthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentEthernetSwitchExtension
- Msvm_ParentEthernetSwitchExtension.Antecedent
- Msvm_ParentEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8e215a01c9de98baa545dbb32b8279db4555f9cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684463"
---
# <a name="msvm_parentethernetswitchextension-class"></a><span data-ttu-id="59e7a-103">\_Класс мсвм парентесернетсвитчекстенсион</span><span class="sxs-lookup"><span data-stu-id="59e7a-103">Msvm\_ParentEthernetSwitchExtension class</span></span>

<span data-ttu-id="59e7a-104">Представляет связь между расширением родительского коммутатора Ethernet и расширением дочернего коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="59e7a-104">Represents the association between a parent Ethernet switch extension and a child Ethernet switch extension.</span></span>

<span data-ttu-id="59e7a-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="59e7a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="59e7a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59e7a-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentEthernetSwitchExtension : CIM_Dependency
{
  Msvm_EthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="59e7a-107">Члены</span><span class="sxs-lookup"><span data-stu-id="59e7a-107">Members</span></span>

<span data-ttu-id="59e7a-108">Класс **мсвм \_ парентесернетсвитчекстенсион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="59e7a-108">The **Msvm\_ParentEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="59e7a-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="59e7a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59e7a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="59e7a-110">Properties</span></span>

<span data-ttu-id="59e7a-111">Класс **мсвм \_ парентесернетсвитчекстенсион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="59e7a-111">The **Msvm\_ParentEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59e7a-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="59e7a-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59e7a-113">Тип данных: **[ **мсвм \_ есернетсвитчекстенсион**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="59e7a-113">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="59e7a-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="59e7a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59e7a-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="59e7a-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="59e7a-116">Ссылка на экземпляр класса [**мсвм \_ есернетсвитчекстенсион**](msvm-ethernetswitchextension.md) , представляющий расширение родительского коммутатора.</span><span class="sxs-lookup"><span data-stu-id="59e7a-116">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the parent switch extension.</span></span>

</dd> <dt>

<span data-ttu-id="59e7a-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="59e7a-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59e7a-118">Тип данных: **[ **мсвм \_ есернетсвитчекстенсион**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="59e7a-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="59e7a-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="59e7a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59e7a-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="59e7a-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="59e7a-121">Ссылка на экземпляр класса [**мсвм \_ есернетсвитчекстенсион**](msvm-ethernetswitchextension.md) , представляющий расширение дочернего коммутатора.</span><span class="sxs-lookup"><span data-stu-id="59e7a-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the child switch extension.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59e7a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="59e7a-122">Requirements</span></span>



| <span data-ttu-id="59e7a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="59e7a-123">Requirement</span></span> | <span data-ttu-id="59e7a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="59e7a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59e7a-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59e7a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="59e7a-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="59e7a-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="59e7a-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59e7a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="59e7a-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="59e7a-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59e7a-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="59e7a-129">Namespace</span></span><br/>                | <span data-ttu-id="59e7a-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="59e7a-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="59e7a-131">MOF</span><span class="sxs-lookup"><span data-stu-id="59e7a-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59e7a-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59e7a-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="59e7a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="59e7a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59e7a-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="59e7a-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

