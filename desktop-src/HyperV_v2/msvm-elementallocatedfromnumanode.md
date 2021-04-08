---
description: Связывает экземпляр выделенного ресурса с физическим узлом NUMA, из которого он был выделен.
ms.assetid: 811ed19f-9084-4e30-8604-860d2bf722c7
title: Класс Msvm_ElementAllocatedFromNumaNode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromNumaNode
- Msvm_ElementAllocatedFromNumaNode.Antecedent
- Msvm_ElementAllocatedFromNumaNode.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98940306f25d46c6af1be31133ee336765f8f1a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911024"
---
# <a name="msvm_elementallocatedfromnumanode-class"></a><span data-ttu-id="09d8b-103">\_Класс мсвм елементаллокатедфромнуманоде</span><span class="sxs-lookup"><span data-stu-id="09d8b-103">Msvm\_ElementAllocatedFromNumaNode class</span></span>

<span data-ttu-id="09d8b-104">Связывает экземпляр выделенного ресурса с физическим узлом NUMA, из которого он был выделен.</span><span class="sxs-lookup"><span data-stu-id="09d8b-104">Associates an instance of an allocated resource with the physical NUMA node from which it was allocated.</span></span>

<span data-ttu-id="09d8b-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="09d8b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="09d8b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09d8b-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromNumaNode : CIM_Dependency
{
  Msvm_NumaNode      REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="09d8b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="09d8b-107">Members</span></span>

<span data-ttu-id="09d8b-108">Класс **мсвм \_ елементаллокатедфромнуманоде** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="09d8b-108">The **Msvm\_ElementAllocatedFromNumaNode** class has these types of members:</span></span>

-   [<span data-ttu-id="09d8b-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="09d8b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09d8b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="09d8b-110">Properties</span></span>

<span data-ttu-id="09d8b-111">Класс **мсвм \_ елементаллокатедфромнуманоде** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="09d8b-111">The **Msvm\_ElementAllocatedFromNumaNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09d8b-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="09d8b-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09d8b-113">Тип данных: **[ **мсвм \_ NumaNode**](msvm-numanode.md)**</span><span class="sxs-lookup"><span data-stu-id="09d8b-113">Data type: **[**Msvm\_NumaNode**](msvm-numanode.md)**</span></span>
</dt> <dt>

<span data-ttu-id="09d8b-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09d8b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09d8b-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="09d8b-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="09d8b-116">Физический узел NUMA.</span><span class="sxs-lookup"><span data-stu-id="09d8b-116">The physical NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="09d8b-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="09d8b-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09d8b-118">Тип данных: **[ **CIM \_ логикалелемент**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span><span class="sxs-lookup"><span data-stu-id="09d8b-118">Data type: **[**CIM\_LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span></span>
</dt> <dt>

<span data-ttu-id="09d8b-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09d8b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09d8b-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="09d8b-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="09d8b-121">Выделенный ресурс.</span><span class="sxs-lookup"><span data-stu-id="09d8b-121">The allocated resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09d8b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="09d8b-122">Requirements</span></span>



| <span data-ttu-id="09d8b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="09d8b-123">Requirement</span></span> | <span data-ttu-id="09d8b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="09d8b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09d8b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="09d8b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="09d8b-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="09d8b-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="09d8b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="09d8b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="09d8b-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="09d8b-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="09d8b-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="09d8b-129">Namespace</span></span><br/>                | <span data-ttu-id="09d8b-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="09d8b-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="09d8b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="09d8b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09d8b-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09d8b-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="09d8b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="09d8b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09d8b-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="09d8b-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

