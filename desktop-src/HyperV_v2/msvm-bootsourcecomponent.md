---
description: Связывает бутсаурцесеттингдата Мсвм \_ с общей мсвм \_ виртуалсистемсеттингдата.
ms.assetid: DB2E66F1-CC2C-49FC-96CE-D9DE441AA809
title: Класс Msvm_BootSourceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceComponent
- Msvm_BootSourceComponent.GroupComponent
- Msvm_BootSourceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44dfe86fa7882b1b20e5b5abbbdaa9d4f37f231f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662597"
---
# <a name="msvm_bootsourcecomponent-class"></a><span data-ttu-id="4dfa3-103">\_Класс мсвм бутсаурцекомпонент</span><span class="sxs-lookup"><span data-stu-id="4dfa3-103">Msvm\_BootSourceComponent class</span></span>

<span data-ttu-id="4dfa3-104">Связывает [**\_ бутсаурцесеттингдата мсвм**](msvm-bootsourcesettingdata.md) с общей [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="4dfa3-104">Associates the [**Msvm\_BootSourceSettingData**](msvm-bootsourcesettingdata.md) to the overall [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).</span></span> <span data-ttu-id="4dfa3-105">Этот класс является производным [**от \_ компонента CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="4dfa3-105">This class derives from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

<span data-ttu-id="4dfa3-106">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4dfa3-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dfa3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4dfa3-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceComponent : CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="4dfa3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="4dfa3-108">Members</span></span>

<span data-ttu-id="4dfa3-109">Класс **мсвм \_ бутсаурцекомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4dfa3-109">The **Msvm\_BootSourceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="4dfa3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="4dfa3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4dfa3-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="4dfa3-111">Properties</span></span>

<span data-ttu-id="4dfa3-112">Класс **мсвм \_ бутсаурцекомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4dfa3-112">The **Msvm\_BootSourceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4dfa3-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="4dfa3-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfa3-114">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="4dfa3-114">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="4dfa3-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4dfa3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfa3-116">Ссылка на родительский элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="4dfa3-116">Reference to the parent element in the association.</span></span> <span data-ttu-id="4dfa3-117">Это свойство наследуется [**от \_ компонента CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="4dfa3-117">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> <dt>

<span data-ttu-id="4dfa3-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4dfa3-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dfa3-119">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="4dfa3-119">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="4dfa3-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4dfa3-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dfa3-121">Ссылка на дочерний элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="4dfa3-121">Reference to the child element in the association.</span></span> <span data-ttu-id="4dfa3-122">Это свойство наследуется [**от \_ компонента CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="4dfa3-122">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4dfa3-123">Требования</span><span class="sxs-lookup"><span data-stu-id="4dfa3-123">Requirements</span></span>



| <span data-ttu-id="4dfa3-124">Требование</span><span class="sxs-lookup"><span data-stu-id="4dfa3-124">Requirement</span></span> | <span data-ttu-id="4dfa3-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4dfa3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dfa3-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4dfa3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4dfa3-127">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4dfa3-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4dfa3-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4dfa3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4dfa3-129">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4dfa3-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4dfa3-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4dfa3-130">Namespace</span></span><br/>                | <span data-ttu-id="4dfa3-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4dfa3-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4dfa3-132">MOF</span><span class="sxs-lookup"><span data-stu-id="4dfa3-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4dfa3-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4dfa3-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4dfa3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4dfa3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dfa3-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4dfa3-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4dfa3-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4dfa3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dfa3-137">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="4dfa3-137">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="4dfa3-138">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="4dfa3-138">**CIM\_Component**</span></span>](/windows/desktop/CIMWin32Prov/cim-component)
</dt> <dt>

[<span data-ttu-id="4dfa3-139">**Мсвм \_ бутсаурцесеттингдата**</span><span class="sxs-lookup"><span data-stu-id="4dfa3-139">**Msvm\_BootSourceSettingData**</span></span>](msvm-bootsourcesettingdata.md)
</dt> <dt>

[<span data-ttu-id="4dfa3-140">**Мсвм \_ виртуалсистемсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="4dfa3-140">**Msvm\_VirtualSystemSettingData**</span></span>](msvm-virtualsystemsettingdata.md)
</dt> </dl>

 

