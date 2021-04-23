---
description: Эта Ассоциация связывает управляемый элемент с поддерживаемыми значениями метрик.
ms.assetid: 89b43736-90ae-49e0-a0ed-7918ddec8558
title: Класс Msvm_MetricForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricForME
- Msvm_MetricForME.Antecedent
- Msvm_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 554f77390737b336b8660d09f737049be193b448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684473"
---
# <a name="msvm_metricforme-class"></a><span data-ttu-id="236fb-103">\_Класс мсвм метрикформе</span><span class="sxs-lookup"><span data-stu-id="236fb-103">Msvm\_MetricForME class</span></span>

<span data-ttu-id="236fb-104">Эта Ассоциация связывает управляемый элемент с поддерживаемыми значениями метрик.</span><span class="sxs-lookup"><span data-stu-id="236fb-104">This association links a managed element to the metric values being maintained for it.</span></span>

<span data-ttu-id="236fb-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="236fb-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="236fb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="236fb-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricForME : CIM_MetricForME
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="236fb-107">Члены</span><span class="sxs-lookup"><span data-stu-id="236fb-107">Members</span></span>

<span data-ttu-id="236fb-108">Класс **мсвм \_ метрикформе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="236fb-108">The **Msvm\_MetricForME** class has these types of members:</span></span>

-   [<span data-ttu-id="236fb-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="236fb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="236fb-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="236fb-110">Properties</span></span>

<span data-ttu-id="236fb-111">Класс **мсвм \_ метрикформе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="236fb-111">The **Msvm\_MetricForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="236fb-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="236fb-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="236fb-113">Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="236fb-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="236fb-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="236fb-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="236fb-115">Ссылка на экземпляр класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , представляющий управляемый элемент, имеющий метрики, определенные с помощью **зависимости** .</span><span class="sxs-lookup"><span data-stu-id="236fb-115">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the managed element that has metrics defined by **Dependent** maintained for it.</span></span> <span data-ttu-id="236fb-116">Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="236fb-116">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="236fb-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="236fb-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="236fb-118">Тип данных: \* \* \* \* CIM \_ басеметриквалуе \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="236fb-118">Data type: \*\*\*\*CIM\_BaseMetricValue\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="236fb-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="236fb-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="236fb-120">Ссылка на экземпляр класса **CIM \_ басеметриквалуе** , представляющий метрику, для которой собрана **предшествующая задача** .</span><span class="sxs-lookup"><span data-stu-id="236fb-120">A reference to an instance of the **CIM\_BaseMetricValue** class that represents the metric that the **Antecedent** has collected for it.</span></span> <span data-ttu-id="236fb-121">Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="236fb-121">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="236fb-122">Требования</span><span class="sxs-lookup"><span data-stu-id="236fb-122">Requirements</span></span>



| <span data-ttu-id="236fb-123">Требование</span><span class="sxs-lookup"><span data-stu-id="236fb-123">Requirement</span></span> | <span data-ttu-id="236fb-124">Значение</span><span class="sxs-lookup"><span data-stu-id="236fb-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="236fb-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="236fb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="236fb-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="236fb-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="236fb-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="236fb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="236fb-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="236fb-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="236fb-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="236fb-129">Namespace</span></span><br/>                | <span data-ttu-id="236fb-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="236fb-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="236fb-131">MOF</span><span class="sxs-lookup"><span data-stu-id="236fb-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="236fb-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="236fb-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="236fb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="236fb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="236fb-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="236fb-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

