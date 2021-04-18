---
description: Ассоциация между экземпляром Мсвм \_ виртуалсистемсеттингдата и \_ экземпляром мсвм виртуалсистемсеттингдата, который представляет самый последний моментальный снимок, на основе которого основан этот объект.
ms.assetid: F779775B-9AB3-4495-B6FF-9985FCDF63E4
title: Класс Msvm_ParentChildSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentChildSettingData
- Msvm_ParentChildSettingData.Antecedent
- Msvm_ParentChildSettingData.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 083de5f5d162f32fc9499a67b2ec991c6d3b398a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664503"
---
# <a name="msvm_parentchildsettingdata-class"></a><span data-ttu-id="c00e3-103">\_Класс мсвм парентчилдсеттингдата</span><span class="sxs-lookup"><span data-stu-id="c00e3-103">Msvm\_ParentChildSettingData class</span></span>

<span data-ttu-id="c00e3-104">Ассоциация между экземпляром [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) и экземпляром **мсвм \_ виртуалсистемсеттингдата** , который представляет самый последний моментальный снимок, на основе которого основан этот объект.</span><span class="sxs-lookup"><span data-stu-id="c00e3-104">An association between an instance of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) and the **Msvm\_VirtualSystemSettingData** instance that represents the most recent snapshot upon which this object is based.</span></span>

<span data-ttu-id="c00e3-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c00e3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c00e3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c00e3-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentChildSettingData : CIM_Dependency
{
  Msvm_VirtualSystemSettingData REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c00e3-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c00e3-107">Members</span></span>

<span data-ttu-id="c00e3-108">Класс **мсвм \_ парентчилдсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c00e3-108">The **Msvm\_ParentChildSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c00e3-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c00e3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c00e3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c00e3-110">Properties</span></span>

<span data-ttu-id="c00e3-111">Класс **мсвм \_ парентчилдсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c00e3-111">The **Msvm\_ParentChildSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c00e3-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="c00e3-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00e3-113">Тип данных: **[ **мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="c00e3-113">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c00e3-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c00e3-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00e3-115">Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="c00e3-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c00e3-116">Данные параметра моментального снимка, на которых основаны данные дочернего параметра.</span><span class="sxs-lookup"><span data-stu-id="c00e3-116">The snapshot setting data upon which the child setting data is based.</span></span>

</dd> <dt>

<span data-ttu-id="c00e3-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="c00e3-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00e3-118">Тип данных: **[ **мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="c00e3-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c00e3-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c00e3-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00e3-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ зависимость CIM. Dependent")</span><span class="sxs-lookup"><span data-stu-id="c00e3-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c00e3-121">Данные параметра для виртуальной машины, представляющие дочерний элемент родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="c00e3-121">The setting data for the virtual machine that represents the child of the parent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c00e3-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c00e3-122">Remarks</span></span>

<span data-ttu-id="c00e3-123">Доступ к классу **\_ парентчилдсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="c00e3-123">Access to the **Msvm\_ParentChildSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c00e3-124">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c00e3-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c00e3-125">Требования</span><span class="sxs-lookup"><span data-stu-id="c00e3-125">Requirements</span></span>



| <span data-ttu-id="c00e3-126">Требование</span><span class="sxs-lookup"><span data-stu-id="c00e3-126">Requirement</span></span> | <span data-ttu-id="c00e3-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c00e3-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c00e3-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c00e3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c00e3-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c00e3-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c00e3-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c00e3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c00e3-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c00e3-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c00e3-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c00e3-132">Namespace</span></span><br/>                | <span data-ttu-id="c00e3-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c00e3-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c00e3-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c00e3-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c00e3-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c00e3-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c00e3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c00e3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c00e3-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c00e3-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c00e3-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c00e3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c00e3-139">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="c00e3-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="c00e3-140">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="c00e3-140">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> <dt>

[<span data-ttu-id="c00e3-141">Классы виртуальных систем</span><span class="sxs-lookup"><span data-stu-id="c00e3-141">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

