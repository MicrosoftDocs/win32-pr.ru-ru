---
description: Универсальная ассоциация, используемая для установления части отношений между управляемыми элементами.
ms.assetid: 4D237D68-0A63-4A19-B6AD-E3C781090994
title: Класс Msvm_ConcreteComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteComponent
- Msvm_ConcreteComponent.GroupComponent
- Msvm_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2ef9e286f4c7ca296ee6b3638ffb9511ccea4115
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663733"
---
# <a name="msvm_concretecomponent-class"></a><span data-ttu-id="d184f-103">\_Класс мсвм конкретекомпонент</span><span class="sxs-lookup"><span data-stu-id="d184f-103">Msvm\_ConcreteComponent class</span></span>

<span data-ttu-id="d184f-104">Универсальная ассоциация, используемая для установления отношений "часть" между управляемыми элементами.</span><span class="sxs-lookup"><span data-stu-id="d184f-104">A generic association used to establish 'part of' relationships between managed elements.</span></span> <span data-ttu-id="d184f-105">[**Модель CIM \_ Конкретекомпонент**](/previous-versions//cc150665(v=vs.85)) определяется как конкретный подкласс абстрактного класса [**\_ компонента CIM**](/windows/desktop/CIMWin32Prov/cim-component) , который используется вместо множества конкретных подклассов компонента, которые не добавляют семантику (то есть подклассы, которые не уточняют тип композиции, обновляют кратность или добавляют или удаляют квалификаторы).</span><span class="sxs-lookup"><span data-stu-id="d184f-105">[**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) is defined as a concrete subclass of the abstract [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component) class, to be used in place of many specific subclasses of component that add no semantics (that is subclasses that do not clarify the type of composition, update cardinalities, or add or remove qualifiers.)</span></span>

<span data-ttu-id="d184f-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d184f-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d184f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d184f-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteComponent : CIM_ConcreteComponent
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="d184f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d184f-108">Members</span></span>

<span data-ttu-id="d184f-109">Класс **мсвм \_ конкретекомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d184f-109">The **Msvm\_ConcreteComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="d184f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d184f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d184f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="d184f-111">Properties</span></span>

<span data-ttu-id="d184f-112">Класс **мсвм \_ конкретекомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d184f-112">The **Msvm\_ConcreteComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d184f-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="d184f-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d184f-114">Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="d184f-114">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="d184f-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d184f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d184f-116">Родительский элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="d184f-116">The parent element in the association.</span></span> <span data-ttu-id="d184f-117">Это свойство наследуется от [**CIM \_ конкретекомпонент**](/previous-versions//cc150665(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d184f-117">This property is inherited from [**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d184f-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d184f-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d184f-119">Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="d184f-119">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="d184f-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d184f-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d184f-121">Дочерний элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="d184f-121">The child element in the association.</span></span> <span data-ttu-id="d184f-122">Это свойство наследуется от [**CIM \_ конкретекомпонент**](/previous-versions//cc150665(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d184f-122">This property is inherited from [**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d184f-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d184f-123">Remarks</span></span>

<span data-ttu-id="d184f-124">Доступ к классу **\_ конкретекомпонент мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="d184f-124">Access to the **Msvm\_ConcreteComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d184f-125">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d184f-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d184f-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d184f-126">Requirements</span></span>



| <span data-ttu-id="d184f-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d184f-127">Requirement</span></span> | <span data-ttu-id="d184f-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d184f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d184f-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d184f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d184f-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d184f-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d184f-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d184f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d184f-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d184f-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d184f-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d184f-133">Namespace</span></span><br/>                | <span data-ttu-id="d184f-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d184f-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d184f-135">MOF</span><span class="sxs-lookup"><span data-stu-id="d184f-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d184f-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d184f-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d184f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d184f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d184f-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d184f-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d184f-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d184f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d184f-140">**\_КОНКРЕТЕКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="d184f-140">**CIM\_ConcreteComponent**</span></span>](cim-concretecomponent.md)
</dt> <dt>

<span data-ttu-id="d184f-141">[**\_КОНКРЕТЕКОМПОНЕНТ CIM**](/previous-versions//cc150665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d184f-141">[**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d184f-142">Классы виртуальных систем</span><span class="sxs-lookup"><span data-stu-id="d184f-142">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

