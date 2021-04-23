---
description: Представляет ассоциацию между управляемыми элементами и их возможностями.
ms.assetid: F083E6D2-CC74-4DAD-8FF7-3FE3CA4EEFFF
title: Класс Msvm_ElementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementCapabilities
- Msvm_ElementCapabilities.ManagedElement
- Msvm_ElementCapabilities.Capabilities
- Msvm_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7602de569a51aec73130a4b5f4d3ba339cb29c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683751"
---
# <a name="msvm_elementcapabilities-class"></a><span data-ttu-id="0208c-103">\_Класс мсвм елементкапабилитиес</span><span class="sxs-lookup"><span data-stu-id="0208c-103">Msvm\_ElementCapabilities class</span></span>

<span data-ttu-id="0208c-104">Представляет ассоциацию между управляемыми элементами и их возможностями.</span><span class="sxs-lookup"><span data-stu-id="0208c-104">Represents the association between managed elements and their capabilities.</span></span>

<span data-ttu-id="0208c-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="0208c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0208c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0208c-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementCapabilities : CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="0208c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="0208c-107">Members</span></span>

<span data-ttu-id="0208c-108">Класс **мсвм \_ елементкапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0208c-108">The **Msvm\_ElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="0208c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="0208c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0208c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0208c-110">Properties</span></span>

<span data-ttu-id="0208c-111">Класс **мсвм \_ елементкапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0208c-111">The **Msvm\_ElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0208c-112">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="0208c-112">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0208c-113">Тип данных: **[ **\_ возможности CIM**](/previous-versions//cc136806(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="0208c-113">Data type: **[**CIM\_Capabilities**](/previous-versions//cc136806(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="0208c-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0208c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0208c-115">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="0208c-115">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0208c-116">Объект capabilities, связанный с элементом.</span><span class="sxs-lookup"><span data-stu-id="0208c-116">The capabilities object associated with the element.</span></span> <span data-ttu-id="0208c-117">Это свойство наследуется от [**CIM \_ елементкапабилитиес**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="0208c-117">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="0208c-118">**Характеристики**</span><span class="sxs-lookup"><span data-stu-id="0208c-118">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0208c-119">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="0208c-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0208c-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0208c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0208c-121">Содержит описательные сведения о возможностях.</span><span class="sxs-lookup"><span data-stu-id="0208c-121">Provides descriptive information about the capabilities.</span></span> <span data-ttu-id="0208c-122">Это свойство наследуется от [**CIM \_ елементкапабилитиес**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="0208c-122">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>



| <span data-ttu-id="0208c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0208c-123">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="0208c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0208c-124">Meaning</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="0208c-125"><dt>**По умолчанию**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0208c-125"><dt>**Default**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="0208c-126">Связанные возможности представляют возможности управляемого элемента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0208c-126">The associated capabilities represent the default capabilities of the managed element.</span></span><br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <span data-ttu-id="0208c-127"><dt>**Текущие**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0208c-127"><dt>**Current**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="0208c-128">Связанные возможности представляют текущие возможности управляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="0208c-128">The associated capabilities represent the current capabilities of the managed element.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0208c-129">**манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="0208c-129">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0208c-130">Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="0208c-130">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="0208c-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0208c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0208c-132">Квалификаторы: **Key**, **min** (1)</span><span class="sxs-lookup"><span data-stu-id="0208c-132">Qualifiers: **Key**, **Min** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="0208c-133">Управляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="0208c-133">The managed element.</span></span> <span data-ttu-id="0208c-134">Это свойство наследуется от [**CIM \_ елементкапабилитиес**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="0208c-134">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0208c-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0208c-135">Remarks</span></span>

<span data-ttu-id="0208c-136">Доступ к классу **\_ елементкапабилитиес мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="0208c-136">Access to the **Msvm\_ElementCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0208c-137">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0208c-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0208c-138">Требования</span><span class="sxs-lookup"><span data-stu-id="0208c-138">Requirements</span></span>



| <span data-ttu-id="0208c-139">Требование</span><span class="sxs-lookup"><span data-stu-id="0208c-139">Requirement</span></span> | <span data-ttu-id="0208c-140">Значение</span><span class="sxs-lookup"><span data-stu-id="0208c-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0208c-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0208c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0208c-142">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0208c-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0208c-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0208c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0208c-144">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0208c-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0208c-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0208c-145">Namespace</span></span><br/>                | <span data-ttu-id="0208c-146">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0208c-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0208c-147">MOF</span><span class="sxs-lookup"><span data-stu-id="0208c-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0208c-148"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0208c-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0208c-149">DLL</span><span class="sxs-lookup"><span data-stu-id="0208c-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0208c-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0208c-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0208c-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0208c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0208c-152">**\_ЕЛЕМЕНТКАПАБИЛИТИЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="0208c-152">**CIM\_ElementCapabilities**</span></span>](cim-elementcapabilities.md)
</dt> <dt>

[<span data-ttu-id="0208c-153">**\_ЕЛЕМЕНТКАПАБИЛИТИЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="0208c-153">**CIM\_ElementCapabilities**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)
</dt> <dt>

[<span data-ttu-id="0208c-154">**Мсвм \_ елементкапабилитиес (v1)**</span><span class="sxs-lookup"><span data-stu-id="0208c-154">**Msvm\_ElementCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-elementcapabilities)
</dt> </dl>

 

