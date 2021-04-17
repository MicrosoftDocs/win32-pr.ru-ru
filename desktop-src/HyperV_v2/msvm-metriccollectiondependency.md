---
description: Представляет связь между двумя определениями метрик или двумя значениями метрик.
ms.assetid: 78fb926d-8981-443a-a82d-ebac34d38e13
title: Класс Msvm_MetricCollectionDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricCollectionDependency
- Msvm_MetricCollectionDependency.Antecedent
- Msvm_MetricCollectionDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dc24cf72975f9d4e47e414425ac4cfbfe5d11847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684474"
---
# <a name="msvm_metriccollectiondependency-class"></a><span data-ttu-id="3e298-103">\_Класс мсвм метрикколлектиондепенденци</span><span class="sxs-lookup"><span data-stu-id="3e298-103">Msvm\_MetricCollectionDependency class</span></span>

<span data-ttu-id="3e298-104">Представляет связь между двумя определениями метрик или двумя значениями метрик.</span><span class="sxs-lookup"><span data-stu-id="3e298-104">Represents the association between two metric definitions or two metric values.</span></span>

<span data-ttu-id="3e298-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="3e298-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e298-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e298-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricCollectionDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3e298-107">Члены</span><span class="sxs-lookup"><span data-stu-id="3e298-107">Members</span></span>

<span data-ttu-id="3e298-108">Класс **мсвм \_ метрикколлектиондепенденци** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3e298-108">The **Msvm\_MetricCollectionDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="3e298-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="3e298-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e298-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="3e298-110">Properties</span></span>

<span data-ttu-id="3e298-111">Класс **мсвм \_ метрикколлектиондепенденци** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3e298-111">The **Msvm\_MetricCollectionDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e298-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="3e298-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e298-113">Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="3e298-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="3e298-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e298-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e298-115">Ссылка на экземпляр класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , представляющий независимое определение метрики или значение метрики.</span><span class="sxs-lookup"><span data-stu-id="3e298-115">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the independent metric definition or metric value.</span></span> <span data-ttu-id="3e298-116">Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="3e298-116">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="3e298-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="3e298-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e298-118">Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="3e298-118">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="3e298-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e298-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e298-120">Ссылка на экземпляр класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , представляющий определение метрики или значение метрики, зависящие от **предшествующей задачи**.</span><span class="sxs-lookup"><span data-stu-id="3e298-120">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the metric definition or metric value that is dependent on the **Antecedent**.</span></span> <span data-ttu-id="3e298-121">Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="3e298-121">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e298-122">Требования</span><span class="sxs-lookup"><span data-stu-id="3e298-122">Requirements</span></span>



| <span data-ttu-id="3e298-123">Требование</span><span class="sxs-lookup"><span data-stu-id="3e298-123">Requirement</span></span> | <span data-ttu-id="3e298-124">Значение</span><span class="sxs-lookup"><span data-stu-id="3e298-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e298-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e298-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3e298-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3e298-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3e298-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e298-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3e298-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3e298-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e298-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3e298-129">Namespace</span></span><br/>                | <span data-ttu-id="3e298-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3e298-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3e298-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3e298-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e298-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e298-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e298-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3e298-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e298-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3e298-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

