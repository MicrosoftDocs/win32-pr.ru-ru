---
description: Определяет зарегистрированные профили, к которым соответствует указанная система.
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Класс Msvm_ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementConformsToProfile
- Msvm_ElementConformsToProfile.ConformantStandard
- Msvm_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b0afdc7dd9d55a036de0695f9a88a95d2b01308
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683854"
---
# <a name="msvm_elementconformstoprofile-class"></a><span data-ttu-id="31923-103">\_Класс мсвм елементконформстопрофиле</span><span class="sxs-lookup"><span data-stu-id="31923-103">Msvm\_ElementConformsToProfile class</span></span>

<span data-ttu-id="31923-104">Определяет зарегистрированные профили, к которым соответствует указанная система.</span><span class="sxs-lookup"><span data-stu-id="31923-104">Defines the registered profiles to which the referenced system conforms.</span></span> <span data-ttu-id="31923-105">Эта ассоциация может применяться к любому управляемому элементу.</span><span class="sxs-lookup"><span data-stu-id="31923-105">This association may apply to any managed element.</span></span> <span data-ttu-id="31923-106">При обычном использовании он применяется к экземпляру более высокого уровня, например к системе, пространству имен или службе.</span><span class="sxs-lookup"><span data-stu-id="31923-106">Typical usage will apply it to a higher level instance, such as a System, Namespace, or Service.</span></span> <span data-ttu-id="31923-107">При применении к экземпляру более высокого уровня все составные части должны вести себя соответствующим образом для поддержки согласованности управляемого элемента с именованным зарегистрированным профилем.</span><span class="sxs-lookup"><span data-stu-id="31923-107">When applied to a higher level instance, all constituent parts must behave appropriately in support of the managed element's conformance to the named registered profile.</span></span>

<span data-ttu-id="31923-108">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="31923-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="31923-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31923-109">Syntax</span></span>

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="31923-110">Члены</span><span class="sxs-lookup"><span data-stu-id="31923-110">Members</span></span>

<span data-ttu-id="31923-111">Класс **мсвм \_ елементконформстопрофиле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="31923-111">The **Msvm\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="31923-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="31923-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31923-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="31923-113">Properties</span></span>

<span data-ttu-id="31923-114">Класс **мсвм \_ елементконформстопрофиле** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="31923-114">The **Msvm\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31923-115">**конформантстандард**</span><span class="sxs-lookup"><span data-stu-id="31923-115">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31923-116">Тип данных: **[ **мсвм \_ регистередпрофиле**](msvm-registeredprofile.md)**</span><span class="sxs-lookup"><span data-stu-id="31923-116">Data type: **[**Msvm\_RegisteredProfile**](msvm-registeredprofile.md)**</span></span>
</dt> <dt>

<span data-ttu-id="31923-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="31923-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31923-118">Квалификаторы: [ **Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="31923-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="31923-119">Ссылка на экземпляр класса [**мсвм \_ регистередпрофиле**](msvm-registeredprofile.md) , представляющий зарегистрированный профиль, которому соответствует система.</span><span class="sxs-lookup"><span data-stu-id="31923-119">A reference to an instance of the [**Msvm\_RegisteredProfile**](msvm-registeredprofile.md) class that represents the registered profile to which the system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="31923-120">**манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="31923-120">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31923-121">Тип данных: **[ **мсвм \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="31923-121">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="31923-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="31923-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31923-123">Квалификаторы: [ **Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="31923-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="31923-124">Ссылка на экземпляр класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , представляющий систему, которая соответствует зарегистрированному профилю.</span><span class="sxs-lookup"><span data-stu-id="31923-124">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31923-125">Требования</span><span class="sxs-lookup"><span data-stu-id="31923-125">Requirements</span></span>



| <span data-ttu-id="31923-126">Требование</span><span class="sxs-lookup"><span data-stu-id="31923-126">Requirement</span></span> | <span data-ttu-id="31923-127">Значение</span><span class="sxs-lookup"><span data-stu-id="31923-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31923-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31923-128">Minimum supported client</span></span><br/> | <span data-ttu-id="31923-129">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="31923-129">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="31923-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31923-130">Minimum supported server</span></span><br/> | <span data-ttu-id="31923-131">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="31923-131">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="31923-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="31923-132">Namespace</span></span><br/>                | <span data-ttu-id="31923-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="31923-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="31923-134">MOF</span><span class="sxs-lookup"><span data-stu-id="31923-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31923-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31923-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="31923-136">DLL</span><span class="sxs-lookup"><span data-stu-id="31923-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31923-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="31923-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

