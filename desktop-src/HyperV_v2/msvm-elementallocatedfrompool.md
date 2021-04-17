---
description: Связывает экземпляр выделенного ресурса с пулом ресурсов, из которого он был выделен.
ms.assetid: BA3168C7-E4F1-414B-827B-1A811069F223
title: Класс Msvm_ElementAllocatedFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromPool
- Msvm_ElementAllocatedFromPool.Antecedent
- Msvm_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4d798c31fbcd8429007c53f3b156fc7c5922e7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683856"
---
# <a name="msvm_elementallocatedfrompool-class"></a><span data-ttu-id="3067a-103">\_Класс мсвм елементаллокатедфромпул</span><span class="sxs-lookup"><span data-stu-id="3067a-103">Msvm\_ElementAllocatedFromPool class</span></span>

<span data-ttu-id="3067a-104">Связывает экземпляр выделенного ресурса с пулом ресурсов, из которого он был выделен.</span><span class="sxs-lookup"><span data-stu-id="3067a-104">Associates an instance of an allocated resource with the resource pool from which it was allocated.</span></span>

<span data-ttu-id="3067a-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="3067a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3067a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3067a-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromPool : CIM_ElementAllocatedFromPool
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3067a-107">Члены</span><span class="sxs-lookup"><span data-stu-id="3067a-107">Members</span></span>

<span data-ttu-id="3067a-108">Класс **мсвм \_ елементаллокатедфромпул** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3067a-108">The **Msvm\_ElementAllocatedFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="3067a-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="3067a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3067a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="3067a-110">Properties</span></span>

<span data-ttu-id="3067a-111">Класс **мсвм \_ елементаллокатедфромпул** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3067a-111">The **Msvm\_ElementAllocatedFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3067a-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="3067a-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3067a-113">Тип данных: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="3067a-113">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="3067a-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3067a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3067a-115">Квалификаторы: **override**, **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="3067a-115">Qualifiers: **Override**, **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="3067a-116">Пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3067a-116">The resource pool.</span></span> <span data-ttu-id="3067a-117">Это свойство наследуется от [**CIM \_ елементаллокатедфромпул**](/previous-versions//cc150668(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3067a-117">This property is inherited from [**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3067a-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="3067a-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3067a-119">Тип данных: **[ **CIM \_ логикалелемент**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span><span class="sxs-lookup"><span data-stu-id="3067a-119">Data type: **[**CIM\_LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span></span>
</dt> <dt>

<span data-ttu-id="3067a-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3067a-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3067a-121">Выделенный ресурс.</span><span class="sxs-lookup"><span data-stu-id="3067a-121">The allocated resource.</span></span> <span data-ttu-id="3067a-122">Это свойство наследуется от [**CIM \_ елементаллокатедфромпул**](/previous-versions//cc150668(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3067a-122">This property is inherited from [**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3067a-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3067a-123">Remarks</span></span>

<span data-ttu-id="3067a-124">Доступ к классу **\_ елементаллокатедфромпул мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="3067a-124">Access to the **Msvm\_ElementAllocatedFromPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3067a-125">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3067a-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3067a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3067a-126">Requirements</span></span>



| <span data-ttu-id="3067a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3067a-127">Requirement</span></span> | <span data-ttu-id="3067a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3067a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3067a-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3067a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3067a-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3067a-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3067a-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3067a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3067a-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3067a-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3067a-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3067a-133">Namespace</span></span><br/>                | <span data-ttu-id="3067a-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3067a-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3067a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="3067a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3067a-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3067a-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3067a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3067a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3067a-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3067a-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3067a-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3067a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3067a-140">**\_ЕЛЕМЕНТАЛЛОКАТЕДФРОМПУЛ CIM**</span><span class="sxs-lookup"><span data-stu-id="3067a-140">**CIM\_ElementAllocatedFromPool**</span></span>](cim-elementallocatedfrompool.md)
</dt> <dt>

<span data-ttu-id="3067a-141">[**\_ЕЛЕМЕНТАЛЛОКАТЕДФРОМПУЛ CIM**](/previous-versions//cc150668(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3067a-141">[**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3067a-142">**Мсвм \_ елементаллокатедфромпул (v1)**</span><span class="sxs-lookup"><span data-stu-id="3067a-142">**Msvm\_ElementAllocatedFromPool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-elementallocatedfrompool)
</dt> <dt>

[<span data-ttu-id="3067a-143">Классы управления ресурсами</span><span class="sxs-lookup"><span data-stu-id="3067a-143">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

