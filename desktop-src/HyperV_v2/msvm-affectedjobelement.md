---
description: Представляет связь между заданием и управляемым элементом, на который может повлиять его выполнение.
ms.assetid: 125A4976-A4E3-4D7A-A43B-86045C3B00AE
title: Класс Msvm_AffectedJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedJobElement
- Msvm_AffectedJobElement.AffectedElement
- Msvm_AffectedJobElement.AffectingElement
- Msvm_AffectedJobElement.ElementEffects
- Msvm_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bef667872a7afa4c726ee1b2c77a36c29649114d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684026"
---
# <a name="msvm_affectedjobelement-class"></a><span data-ttu-id="322c9-103">\_Класс мсвм аффектеджобелемент</span><span class="sxs-lookup"><span data-stu-id="322c9-103">Msvm\_AffectedJobElement class</span></span>

<span data-ttu-id="322c9-104">Представляет связь между заданием и управляемым элементом, на который может повлиять его выполнение.</span><span class="sxs-lookup"><span data-stu-id="322c9-104">Represents an association between a job and the managed element that may be affected by its execution.</span></span>

<span data-ttu-id="322c9-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="322c9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="322c9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="322c9-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_ConcreteJob   REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="322c9-107">Члены</span><span class="sxs-lookup"><span data-stu-id="322c9-107">Members</span></span>

<span data-ttu-id="322c9-108">Класс **мсвм \_ аффектеджобелемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="322c9-108">The **Msvm\_AffectedJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="322c9-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="322c9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="322c9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="322c9-110">Properties</span></span>

<span data-ttu-id="322c9-111">Класс **мсвм \_ аффектеджобелемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="322c9-111">The **Msvm\_AffectedJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="322c9-112">**аффектеделемент**</span><span class="sxs-lookup"><span data-stu-id="322c9-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="322c9-113">Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="322c9-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="322c9-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="322c9-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="322c9-115">Управляемый элемент, затронутый выполнением задания.</span><span class="sxs-lookup"><span data-stu-id="322c9-115">The managed element affected by the execution of the job.</span></span> <span data-ttu-id="322c9-116">Это свойство наследуется от [**CIM \_ аффектеджобелемент**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="322c9-116">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="322c9-117">**аффектинжелемент**</span><span class="sxs-lookup"><span data-stu-id="322c9-117">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="322c9-118">Тип данных: **[ **мсвм \_ конкретежоб**](msvm-concretejob.md)**</span><span class="sxs-lookup"><span data-stu-id="322c9-118">Data type: **[**Msvm\_ConcreteJob**](msvm-concretejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="322c9-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="322c9-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="322c9-120">Задание, влияющее на управляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="322c9-120">The job that is affecting the managed element.</span></span> <span data-ttu-id="322c9-121">Это свойство наследуется от [**CIM \_ аффектеджобелемент**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="322c9-121">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="322c9-122">**елементеффектс**</span><span class="sxs-lookup"><span data-stu-id="322c9-122">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="322c9-123">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="322c9-123">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="322c9-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="322c9-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="322c9-125">Перечисление, описывающее воздействие на управляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="322c9-125">An enumeration that describes the effect on the managed element.</span></span> <span data-ttu-id="322c9-126">Это свойство наследуется от [**CIM \_ аффектеджобелемент**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="322c9-126">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="322c9-127">**осерелементеффектсдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="322c9-127">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="322c9-128">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="322c9-128">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="322c9-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="322c9-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="322c9-130">Предоставляет подробные сведения о результате действия в соответствующей позиции массива в **елементеффектс**.</span><span class="sxs-lookup"><span data-stu-id="322c9-130">Provides details for the effect at the corresponding array position in **ElementEffects**.</span></span> <span data-ttu-id="322c9-131">Это свойство наследуется от [**CIM \_ аффектеджобелемент**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="322c9-131">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="322c9-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="322c9-132">Remarks</span></span>

<span data-ttu-id="322c9-133">Доступ к классу **\_ аффектеджобелемент мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="322c9-133">Access to the **Msvm\_AffectedJobElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="322c9-134">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="322c9-134">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="322c9-135">Требования</span><span class="sxs-lookup"><span data-stu-id="322c9-135">Requirements</span></span>



| <span data-ttu-id="322c9-136">Требование</span><span class="sxs-lookup"><span data-stu-id="322c9-136">Requirement</span></span> | <span data-ttu-id="322c9-137">Значение</span><span class="sxs-lookup"><span data-stu-id="322c9-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="322c9-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="322c9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="322c9-139">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="322c9-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="322c9-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="322c9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="322c9-141">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="322c9-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="322c9-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="322c9-142">Namespace</span></span><br/>                | <span data-ttu-id="322c9-143">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="322c9-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="322c9-144">MOF</span><span class="sxs-lookup"><span data-stu-id="322c9-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="322c9-145"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="322c9-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="322c9-146">DLL</span><span class="sxs-lookup"><span data-stu-id="322c9-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="322c9-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="322c9-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="322c9-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="322c9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="322c9-149">**\_АФФЕКТЕДЖОБЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="322c9-149">**CIM\_AffectedJobElement**</span></span>](cim-affectedjobelement.md)
</dt> <dt>

<span data-ttu-id="322c9-150">[**\_АФФЕКТЕДЖОБЕЛЕМЕНТ CIM**](/previous-versions//cc150663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="322c9-150">[**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="322c9-151">Классы управления виртуальной системой</span><span class="sxs-lookup"><span data-stu-id="322c9-151">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

