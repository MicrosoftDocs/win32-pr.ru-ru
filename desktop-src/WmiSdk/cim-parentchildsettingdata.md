---
description: Ассоциация между экземпляром CIM \_ виртуалсистемсеттингдата и \_ экземпляром CIM виртуалсистемсеттингдата, который представляет самый последний моментальный снимок, на основе которого основан этот объект.
ms.assetid: f6e93c22-077b-4604-8d0d-9584b1f4dce1
ms.tgt_platform: multiple
title: Класс CIM_ParentChildSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParentChildSettingData
- Root\CIMV2.CIM_ParentChildSettingData.Antecedent
- Root\CIMV2.CIM_ParentChildSettingData.Dependent
- Root\CIMV2.CIM_ParentChildSettingData.Parent
- Root\CIMV2.CIM_ParentChildSettingData.Child
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 9b2b866c3d5ae15d3f5a97c971e8efec75e9164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717973"
---
# <a name="cim_parentchildsettingdata-class"></a><span data-ttu-id="aabdd-103">\_Класс CIM парентчилдсеттингдата</span><span class="sxs-lookup"><span data-stu-id="aabdd-103">CIM\_ParentChildSettingData class</span></span>

<span data-ttu-id="aabdd-104">Ассоциация между экземпляром [**CIM \_ виртуалсистемсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) и экземпляром **CIM \_ виртуалсистемсеттингдата** , который представляет самый последний моментальный снимок, на основе которого основан этот объект.</span><span class="sxs-lookup"><span data-stu-id="aabdd-104">An association between an instance of [**CIM\_VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) and the **CIM\_VirtualSystemSettingData** instance which represents the most recent snapshot upon which this object is based.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aabdd-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="aabdd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aabdd-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="aabdd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aabdd-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="aabdd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aabdd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aabdd-108">Syntax</span></span>

``` syntax
class CIM_ParentChildSettingData : CIM_Dependency
{
  CIM_ManagedSystemElement     REF Antecedent;
  CIM_ManagedSystemElement     REF Dependent;
  CIM_VirtualSystemSettingData REF Parent;
  CIM_VirtualSystemSettingData REF Child;
};
```

## <a name="members"></a><span data-ttu-id="aabdd-109">Члены</span><span class="sxs-lookup"><span data-stu-id="aabdd-109">Members</span></span>

<span data-ttu-id="aabdd-110">Класс **CIM \_ парентчилдсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="aabdd-110">The **CIM\_ParentChildSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="aabdd-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="aabdd-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aabdd-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="aabdd-112">Properties</span></span>

<span data-ttu-id="aabdd-113">Класс **CIM \_ парентчилдсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="aabdd-113">The **CIM\_ParentChildSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aabdd-114">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="aabdd-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabdd-115">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="aabdd-115">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="aabdd-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aabdd-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabdd-117">Ссылка на независимый объект в этой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="aabdd-117">Reference to the independent object in this association.</span></span>

<span data-ttu-id="aabdd-118">Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="aabdd-118">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="aabdd-119">**Дочерний**</span><span class="sxs-lookup"><span data-stu-id="aabdd-119">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabdd-120">Тип данных: **CIM \_ виртуалсистемсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="aabdd-120">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="aabdd-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aabdd-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabdd-122">Данные параметра для виртуальной системы, представляющие дочерний элемент родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="aabdd-122">The setting data for the virtual system which represents the child of the Parent.</span></span>

</dd> <dt>

<span data-ttu-id="aabdd-123">**Него**</span><span class="sxs-lookup"><span data-stu-id="aabdd-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabdd-124">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="aabdd-124">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="aabdd-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aabdd-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabdd-126">Ссылка на объект, который зависит от свойства **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="aabdd-126">Reference to the object that is dependent on the **Antecedent** property.</span></span>

<span data-ttu-id="aabdd-127">Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="aabdd-127">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="aabdd-128">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="aabdd-128">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aabdd-129">Тип данных: **CIM \_ виртуалсистемсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="aabdd-129">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="aabdd-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aabdd-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aabdd-131">Данные параметра моментального снимка, на которых основаны данные дочернего параметра.</span><span class="sxs-lookup"><span data-stu-id="aabdd-131">The snapshot setting data upon which the Child setting data is based.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aabdd-132">Требования</span><span class="sxs-lookup"><span data-stu-id="aabdd-132">Requirements</span></span>



| <span data-ttu-id="aabdd-133">Требование</span><span class="sxs-lookup"><span data-stu-id="aabdd-133">Requirement</span></span> | <span data-ttu-id="aabdd-134">Значение</span><span class="sxs-lookup"><span data-stu-id="aabdd-134">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="aabdd-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="aabdd-135">Namespace</span></span><br/> | <span data-ttu-id="aabdd-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="aabdd-136">Root\\CIMV2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aabdd-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aabdd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aabdd-138">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="aabdd-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

