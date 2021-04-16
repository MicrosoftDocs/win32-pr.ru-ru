---
description: Представляет связь между виртуальной системой и данными параметра моментального снимка, который был недавно применен к виртуальной системе.
ms.assetid: 9231b441-20c4-468b-905f-5baabc32a8cc
title: Класс Msvm_LastAppliedSnapshot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LastAppliedSnapshot
- Msvm_LastAppliedSnapshot.Antecedent
- Msvm_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 48854d7b5aaaa6f8026f8dec14745545b0c58806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663078"
---
# <a name="msvm_lastappliedsnapshot-class"></a><span data-ttu-id="43c3d-103">\_Класс мсвм ластапплиедснапшот</span><span class="sxs-lookup"><span data-stu-id="43c3d-103">Msvm\_LastAppliedSnapshot class</span></span>

<span data-ttu-id="43c3d-104">Представляет связь между виртуальной системой и данными параметра моментального снимка, который был недавно применен к виртуальной системе.</span><span class="sxs-lookup"><span data-stu-id="43c3d-104">Represents an association between a virtual system and the setting data of the snapshot that was most recently applied to the virtual system.</span></span>

<span data-ttu-id="43c3d-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="43c3d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="43c3d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43c3d-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LastAppliedSnapshot : CIM_LastAppliedSnapshot
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="43c3d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="43c3d-107">Members</span></span>

<span data-ttu-id="43c3d-108">Класс **мсвм \_ ластапплиедснапшот** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="43c3d-108">The **Msvm\_LastAppliedSnapshot** class has these types of members:</span></span>

-   [<span data-ttu-id="43c3d-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="43c3d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43c3d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="43c3d-110">Properties</span></span>

<span data-ttu-id="43c3d-111">Класс **мсвм \_ ластапплиедснапшот** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="43c3d-111">The **Msvm\_LastAppliedSnapshot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43c3d-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="43c3d-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43c3d-113">Тип данных: **CIM \_ виртуалсистемсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="43c3d-113">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="43c3d-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43c3d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43c3d-115">Квалификаторы: **override**, **min** (0), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="43c3d-115">Qualifiers: **Override**, **Min** ( 0 ), **Max** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="43c3d-116">Ссылка на экземпляр класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , представляющий моментальный снимок виртуальной системы, который был последний раз применен к виртуальной системе.</span><span class="sxs-lookup"><span data-stu-id="43c3d-116">Reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the virtual system snapshot that was last applied to the virtual system.</span></span> <span data-ttu-id="43c3d-117">Это свойство наследуется **от \_ зависимости CIM**.</span><span class="sxs-lookup"><span data-stu-id="43c3d-117">This property is inherited from **CIM\_Dependency**.</span></span>

</dd> <dt>

<span data-ttu-id="43c3d-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="43c3d-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43c3d-119">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="43c3d-119">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="43c3d-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43c3d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43c3d-121">Квалификаторы: **override**, **min** (0), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="43c3d-121">Qualifiers: **Override**, **Min** ( 0 ), **Max** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="43c3d-122">Ссылка на экземпляр класса [**\_ ComputerSystem мсвм**](msvm-computersystem.md) , представляющий виртуальную систему, на основе которой был недавно применен моментальный снимок виртуальной системы, представленный свойством **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="43c3d-122">Reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual system upon which the virtual system snapshot represented by the **Antecedent** property was most recently applied.</span></span> <span data-ttu-id="43c3d-123">Это свойство наследуется **от \_ зависимости CIM**.</span><span class="sxs-lookup"><span data-stu-id="43c3d-123">This property is inherited from **CIM\_Dependency**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43c3d-124">Требования</span><span class="sxs-lookup"><span data-stu-id="43c3d-124">Requirements</span></span>



| <span data-ttu-id="43c3d-125">Требование</span><span class="sxs-lookup"><span data-stu-id="43c3d-125">Requirement</span></span> | <span data-ttu-id="43c3d-126">Значение</span><span class="sxs-lookup"><span data-stu-id="43c3d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43c3d-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43c3d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="43c3d-128">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="43c3d-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="43c3d-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43c3d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="43c3d-130">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="43c3d-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43c3d-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="43c3d-131">Namespace</span></span><br/>                | <span data-ttu-id="43c3d-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="43c3d-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="43c3d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="43c3d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43c3d-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43c3d-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="43c3d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="43c3d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43c3d-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="43c3d-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




