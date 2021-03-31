---
description: Связывает экземпляр виртуальной машины со службой управления, которая управляет ее состоянием.
ms.assetid: 12EB3951-74D4-477F-8B55-69FAA3B14631
title: Класс Msvm_ServiceAffectsElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceAffectsElement
- Msvm_ServiceAffectsElement.AffectedElement
- Msvm_ServiceAffectsElement.AffectingElement
- Msvm_ServiceAffectsElement.ElementEffects
- Msvm_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eadb9f33015091999776b73c83d792ccd29396b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154846"
---
# <a name="msvm_serviceaffectselement-class"></a><span data-ttu-id="ca4c4-103">\_Класс мсвм сервицеаффектселемент</span><span class="sxs-lookup"><span data-stu-id="ca4c4-103">Msvm\_ServiceAffectsElement class</span></span>

<span data-ttu-id="ca4c4-104">Связывает экземпляр виртуальной машины со службой управления, которая управляет ее состоянием.</span><span class="sxs-lookup"><span data-stu-id="ca4c4-104">Associates a virtual machine instance with the management service that controls its state.</span></span>

<span data-ttu-id="ca4c4-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ca4c4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca4c4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca4c4-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceAffectsElement : CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[] = 5;
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="ca4c4-107">Члены</span><span class="sxs-lookup"><span data-stu-id="ca4c4-107">Members</span></span>

<span data-ttu-id="ca4c4-108">Класс **мсвм \_ сервицеаффектселемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ca4c4-108">The **Msvm\_ServiceAffectsElement** class has these types of members:</span></span>

-   [<span data-ttu-id="ca4c4-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ca4c4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca4c4-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ca4c4-110">Properties</span></span>

<span data-ttu-id="ca4c4-111">Класс **мсвм \_ сервицеаффектселемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ca4c4-111">The **Msvm\_ServiceAffectsElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca4c4-112">**аффектеделемент**</span><span class="sxs-lookup"><span data-stu-id="ca4c4-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca4c4-113">Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="ca4c4-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="ca4c4-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca4c4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca4c4-115">Ссылка на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ca4c4-115">A reference to the virtual machine.</span></span> <span data-ttu-id="ca4c4-116">Это свойство наследуется от [**CIM \_ сервицеаффектселемент**](/previous-versions//cc136907(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ca4c4-116">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ca4c4-117">**аффектинжелемент**</span><span class="sxs-lookup"><span data-stu-id="ca4c4-117">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca4c4-118">Тип данных: **[ **\_ Служба CIM**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="ca4c4-118">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="ca4c4-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca4c4-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca4c4-120">Ссылка на службу, которая управляет виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="ca4c4-120">A reference to the service that controls the virtual machine.</span></span> <span data-ttu-id="ca4c4-121">Это свойство наследуется от [**CIM \_ сервицеаффектселемент**](/previous-versions//cc136907(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ca4c4-121">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ca4c4-122">**елементеффектс**</span><span class="sxs-lookup"><span data-stu-id="ca4c4-122">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca4c4-123">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ca4c4-123">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ca4c4-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca4c4-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca4c4-125">Указывает тип элемента управления, который представляет Ассоциация.</span><span class="sxs-lookup"><span data-stu-id="ca4c4-125">Specifies the type of control that the association represents.</span></span> <span data-ttu-id="ca4c4-126">Это свойство наследуется от [**CIM \_ сервицеаффектселемент**](/previous-versions//cc136907(v=vs.85)), и для него всегда устанавливается следующее значение.</span><span class="sxs-lookup"><span data-stu-id="ca4c4-126">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)), and it is always set to the following value.</span></span>



| <span data-ttu-id="ca4c4-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ca4c4-127">Value</span></span>                                                                        | <span data-ttu-id="ca4c4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ca4c4-128">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="ca4c4-129"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ca4c4-129"><dt>5</dt></span></span> </dl> | <span data-ttu-id="ca4c4-130">Управление</span><span class="sxs-lookup"><span data-stu-id="ca4c4-130">Manages</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ca4c4-131">**осерелементеффектсдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="ca4c4-131">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca4c4-132">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ca4c4-132">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ca4c4-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca4c4-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca4c4-134">Сведения о типе ассоциации в соответствующей позиции массива в массиве свойств **елементаффектс** .</span><span class="sxs-lookup"><span data-stu-id="ca4c4-134">The details for the type of association at the corresponding array position in the **ElementAffects** property array.</span></span> <span data-ttu-id="ca4c4-135">Эта информация необходима, если для **елементаффектс** задано значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="ca4c4-135">This information is required if **ElementAffects** is set to 1 (Other).</span></span> <span data-ttu-id="ca4c4-136">Это свойство наследуется от [**CIM \_ сервицеаффектселемент**](/previous-versions//cc136907(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ca4c4-136">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca4c4-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca4c4-137">Remarks</span></span>

<span data-ttu-id="ca4c4-138">Доступ к классу **\_ сервицеаффектселемент мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="ca4c4-138">Access to the **Msvm\_ServiceAffectsElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ca4c4-139">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ca4c4-139">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca4c4-140">Требования</span><span class="sxs-lookup"><span data-stu-id="ca4c4-140">Requirements</span></span>



| <span data-ttu-id="ca4c4-141">Требование</span><span class="sxs-lookup"><span data-stu-id="ca4c4-141">Requirement</span></span> | <span data-ttu-id="ca4c4-142">Значение</span><span class="sxs-lookup"><span data-stu-id="ca4c4-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca4c4-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca4c4-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ca4c4-144">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ca4c4-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ca4c4-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca4c4-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ca4c4-146">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ca4c4-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca4c4-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ca4c4-147">Namespace</span></span><br/>                | <span data-ttu-id="ca4c4-148">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ca4c4-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ca4c4-149">MOF</span><span class="sxs-lookup"><span data-stu-id="ca4c4-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca4c4-150"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca4c4-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca4c4-151">DLL</span><span class="sxs-lookup"><span data-stu-id="ca4c4-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca4c4-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ca4c4-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ca4c4-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca4c4-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca4c4-154">**\_СЕРВИЦЕАФФЕКТСЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ca4c4-154">**CIM\_ServiceAffectsElement**</span></span>](cim-serviceaffectselement.md)
</dt> <dt>

<span data-ttu-id="ca4c4-155">[**\_СЕРВИЦЕАФФЕКТСЕЛЕМЕНТ CIM**](/previous-versions//cc136907(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca4c4-155">[**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))</span></span>
</dt> </dl>

 

