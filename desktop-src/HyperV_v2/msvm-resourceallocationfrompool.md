---
description: Связывает экземпляр выделения ресурсов с пулом ресурсов, из которого он выделяется.
ms.assetid: A2B3996D-7886-4B5F-BC89-EFDC1A48249B
title: Класс Msvm_ResourceAllocationFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationFromPool
- Msvm_ResourceAllocationFromPool.Antecedent
- Msvm_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5bb3db9bce86731b12730966a7a2f6d1c9dc8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683683"
---
# <a name="msvm_resourceallocationfrompool-class"></a><span data-ttu-id="70cbf-103">\_Класс мсвм ресаурцеаллокатионфромпул</span><span class="sxs-lookup"><span data-stu-id="70cbf-103">Msvm\_ResourceAllocationFromPool class</span></span>

<span data-ttu-id="70cbf-104">Связывает экземпляр выделения ресурсов с пулом ресурсов, из которого он выделяется.</span><span class="sxs-lookup"><span data-stu-id="70cbf-104">Associates an instance of a resource allocation with the resource pool from which it is allocated.</span></span>

<span data-ttu-id="70cbf-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="70cbf-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="70cbf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70cbf-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationFromPool : CIM_ResourceAllocationFromPool
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="70cbf-107">Члены</span><span class="sxs-lookup"><span data-stu-id="70cbf-107">Members</span></span>

<span data-ttu-id="70cbf-108">Класс **мсвм \_ ресаурцеаллокатионфромпул** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="70cbf-108">The **Msvm\_ResourceAllocationFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="70cbf-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="70cbf-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70cbf-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="70cbf-110">Properties</span></span>

<span data-ttu-id="70cbf-111">Класс **мсвм \_ ресаурцеаллокатионфромпул** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="70cbf-111">The **Msvm\_ResourceAllocationFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70cbf-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="70cbf-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70cbf-113">Тип данных: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="70cbf-113">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="70cbf-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70cbf-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70cbf-115">Квалификаторы: **override**, **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="70cbf-115">Qualifiers: **Override**, **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="70cbf-116">Пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="70cbf-116">The resource pool.</span></span> <span data-ttu-id="70cbf-117">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионфромпул**](/previous-versions//cc150673(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="70cbf-117">This property is inherited from [**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="70cbf-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="70cbf-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70cbf-119">Тип данных: **[ **CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="70cbf-119">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="70cbf-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70cbf-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70cbf-121">Выделение ресурсов.</span><span class="sxs-lookup"><span data-stu-id="70cbf-121">The resource allocation.</span></span> <span data-ttu-id="70cbf-122">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионфромпул**](/previous-versions//cc150673(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="70cbf-122">This property is inherited from [**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70cbf-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70cbf-123">Remarks</span></span>

<span data-ttu-id="70cbf-124">Доступ к классу **\_ ресаурцеаллокатионфромпул мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="70cbf-124">Access to the **Msvm\_ResourceAllocationFromPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="70cbf-125">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="70cbf-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="70cbf-126">Требования</span><span class="sxs-lookup"><span data-stu-id="70cbf-126">Requirements</span></span>



| <span data-ttu-id="70cbf-127">Требование</span><span class="sxs-lookup"><span data-stu-id="70cbf-127">Requirement</span></span> | <span data-ttu-id="70cbf-128">Значение</span><span class="sxs-lookup"><span data-stu-id="70cbf-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70cbf-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70cbf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="70cbf-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="70cbf-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="70cbf-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70cbf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="70cbf-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="70cbf-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70cbf-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="70cbf-133">Namespace</span></span><br/>                | <span data-ttu-id="70cbf-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="70cbf-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="70cbf-135">MOF</span><span class="sxs-lookup"><span data-stu-id="70cbf-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70cbf-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70cbf-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="70cbf-137">DLL</span><span class="sxs-lookup"><span data-stu-id="70cbf-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70cbf-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="70cbf-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="70cbf-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70cbf-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70cbf-140">**\_РЕСАУРЦЕАЛЛОКАТИОНФРОМПУЛ CIM**</span><span class="sxs-lookup"><span data-stu-id="70cbf-140">**CIM\_ResourceAllocationFromPool**</span></span>](cim-resourceallocationfrompool.md)
</dt> <dt>

<span data-ttu-id="70cbf-141">[**\_РЕСАУРЦЕАЛЛОКАТИОНФРОМПУЛ CIM**](/previous-versions//cc150673(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="70cbf-141">[**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="70cbf-142">**Мсвм \_ ресаурцеаллокатионфромпул (v1)**</span><span class="sxs-lookup"><span data-stu-id="70cbf-142">**Msvm\_ResourceAllocationFromPool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourceallocationfrompool)
</dt> <dt>

[<span data-ttu-id="70cbf-143">Классы управления ресурсами</span><span class="sxs-lookup"><span data-stu-id="70cbf-143">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

