---
description: Представляет связь между заданием и управляемыми элементами, на которые может повлиять его выполнение.
ms.assetid: 81849DE4-9039-426F-B7B1-45BB31A9132C
title: Класс Msvm_AffectedStorageJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedStorageJobElement
- Msvm_AffectedStorageJobElement.AffectedElement
- Msvm_AffectedStorageJobElement.AffectingElement
- Msvm_AffectedStorageJobElement.ElementEffects
- Msvm_AffectedStorageJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d900f42e5022301a08ebeee0036400be3a2f1bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662138"
---
# <a name="msvm_affectedstoragejobelement-class"></a><span data-ttu-id="a5ced-103">\_Класс мсвм аффектедсторажежобелемент</span><span class="sxs-lookup"><span data-stu-id="a5ced-103">Msvm\_AffectedStorageJobElement class</span></span>

<span data-ttu-id="a5ced-104">Представляет связь между заданием и управляемыми элементами, на которые может повлиять его выполнение.</span><span class="sxs-lookup"><span data-stu-id="a5ced-104">Represents the association between a job and the managed elements that may be affected by its execution.</span></span>

<span data-ttu-id="a5ced-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a5ced-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5ced-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5ced-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedStorageJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_StorageJob    REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="a5ced-107">Члены</span><span class="sxs-lookup"><span data-stu-id="a5ced-107">Members</span></span>

<span data-ttu-id="a5ced-108">Класс **мсвм \_ аффектедсторажежобелемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a5ced-108">The **Msvm\_AffectedStorageJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="a5ced-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="a5ced-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5ced-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a5ced-110">Properties</span></span>

<span data-ttu-id="a5ced-111">Класс **мсвм \_ аффектедсторажежобелемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a5ced-111">The **Msvm\_AffectedStorageJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5ced-112">**аффектеделемент**</span><span class="sxs-lookup"><span data-stu-id="a5ced-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5ced-113">Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="a5ced-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="a5ced-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5ced-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5ced-115">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="a5ced-115">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a5ced-116">Управляемый элемент, затронутый выполнением задания.</span><span class="sxs-lookup"><span data-stu-id="a5ced-116">The managed element affected by the execution of the job.</span></span> <span data-ttu-id="a5ced-117">Это свойство наследуется от [**CIM \_ аффектеджобелемент**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5ced-117">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a5ced-118">**аффектинжелемент**</span><span class="sxs-lookup"><span data-stu-id="a5ced-118">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5ced-119">Тип данных: **[ **мсвм \_ сторажежоб**](msvm-storagejob.md)**</span><span class="sxs-lookup"><span data-stu-id="a5ced-119">Data type: **[**Msvm\_StorageJob**](msvm-storagejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a5ced-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5ced-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5ced-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ аффектеджобелемент. аффектинжелемент")</span><span class="sxs-lookup"><span data-stu-id="a5ced-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_AffectedJobElement.AffectingElement")</span></span>
</dt> </dl>

<span data-ttu-id="a5ced-122">Задание, влияющее на затронутый элемент.</span><span class="sxs-lookup"><span data-stu-id="a5ced-122">The job that is affecting the affected element.</span></span> <span data-ttu-id="a5ced-123">Это свойство наследуется от [**CIM \_ аффектеджобелемент**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5ced-123">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a5ced-124">**елементеффектс**</span><span class="sxs-lookup"><span data-stu-id="a5ced-124">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5ced-125">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="a5ced-125">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a5ced-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5ced-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5ced-127">Перечисление, описывающее воздействие на управляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="a5ced-127">An enumeration that describes the effect on the managed element.</span></span> <span data-ttu-id="a5ced-128">Этот массив соответствует массиву свойств **осерелементеффектсдескриптионс** , где второй предоставляет подробные сведения, относящиеся к эффектам высокого уровня, перечисленным этим свойством.</span><span class="sxs-lookup"><span data-stu-id="a5ced-128">This array corresponds to the **OtherElementEffectsDescriptions** property array, where the latter provides details related to the high-level effects enumerated by this property.</span></span> <span data-ttu-id="a5ced-129">Дополнительные сведения требуются, если массив свойств **елементеффектс** содержит значение 1, (другое).</span><span class="sxs-lookup"><span data-stu-id="a5ced-129">Additional detail is required if the **ElementEffects** property array contains the value 1, (Other).</span></span> <span data-ttu-id="a5ced-130">Это свойство наследуется от [**CIM \_ аффектеджобелемент**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5ced-130">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="a5ced-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a5ced-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a5ced-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="a5ced-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a5ced-133"><span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Эксклюзивное использование** (2)</span><span class="sxs-lookup"><span data-stu-id="a5ced-133"><span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Exclusive Use** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a5ced-134"><span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Влияние на производительность** (3)</span><span class="sxs-lookup"><span data-stu-id="a5ced-134"><span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Performance Impact** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a5ced-135"><span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Целостность элементов** (4)</span><span class="sxs-lookup"><span data-stu-id="a5ced-135"><span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Element Integrity** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a5ced-136">**осерелементеффектсдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="a5ced-136">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5ced-137">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="a5ced-137">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a5ced-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5ced-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5ced-139">Предоставляет подробные сведения о результате действия на соответствующей позиции массива в массиве свойств **елементеффектс** .</span><span class="sxs-lookup"><span data-stu-id="a5ced-139">Provides details for the effect at the corresponding array position in the **ElementEffects** property array.</span></span> <span data-ttu-id="a5ced-140">Эта информация необходима, когда соответствующий элемент в массиве свойств **елементеффектс** содержит значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="a5ced-140">This information is required whenever the corresponding element in the **ElementEffects** property array contains the value 1 (Other).</span></span> <span data-ttu-id="a5ced-141">Это свойство наследуется от [**CIM \_ аффектеджобелемент**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5ced-141">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5ced-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5ced-142">Remarks</span></span>

<span data-ttu-id="a5ced-143">Доступ к классу **\_ аффектедсторажежобелемент мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="a5ced-143">Access to the **Msvm\_AffectedStorageJobElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a5ced-144">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a5ced-144">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5ced-145">Требования</span><span class="sxs-lookup"><span data-stu-id="a5ced-145">Requirements</span></span>



| <span data-ttu-id="a5ced-146">Требование</span><span class="sxs-lookup"><span data-stu-id="a5ced-146">Requirement</span></span> | <span data-ttu-id="a5ced-147">Значение</span><span class="sxs-lookup"><span data-stu-id="a5ced-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5ced-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5ced-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a5ced-149">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a5ced-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a5ced-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5ced-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a5ced-151">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a5ced-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a5ced-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a5ced-152">Namespace</span></span><br/>                | <span data-ttu-id="a5ced-153">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a5ced-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a5ced-154">MOF</span><span class="sxs-lookup"><span data-stu-id="a5ced-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5ced-155"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5ced-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5ced-156">DLL</span><span class="sxs-lookup"><span data-stu-id="a5ced-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5ced-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a5ced-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a5ced-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5ced-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5ced-159">**\_АФФЕКТЕДЖОБЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="a5ced-159">**CIM\_AffectedJobElement**</span></span>](cim-affectedjobelement.md)
</dt> <dt>

<span data-ttu-id="a5ced-160">[**\_АФФЕКТЕДЖОБЕЛЕМЕНТ CIM**](/previous-versions//cc150663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5ced-160">[**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a5ced-161">Классы хранения</span><span class="sxs-lookup"><span data-stu-id="a5ced-161">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

