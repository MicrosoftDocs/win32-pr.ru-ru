---
description: Представляет ассоциацию объектов значений метрик с их определениями метрик.
ms.assetid: 98ad9390-78b4-4c18-b068-d05efa2f1866
title: Класс Msvm_MetricInstance
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricInstance
- Msvm_MetricInstance.Antecedent
- Msvm_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab17dce339e866fb22654a0bd75c6f3945d320a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683384"
---
# <a name="msvm_metricinstance-class"></a><span data-ttu-id="c38f2-103">\_Класс мсвм метриЦинстанце</span><span class="sxs-lookup"><span data-stu-id="c38f2-103">Msvm\_MetricInstance class</span></span>

<span data-ttu-id="c38f2-104">Представляет ассоциацию объектов значений метрик с их определениями метрик.</span><span class="sxs-lookup"><span data-stu-id="c38f2-104">Represents an association of metric value objects with their metrics definitions.</span></span> <span data-ttu-id="c38f2-105">Эта Ассоциация связывает экземпляр [**мсвм \_ басеметриквалуе**](msvm-basemetricvalue.md) с его [**мсвм \_ басеметрикдефинитион**](msvm-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="c38f2-105">This association ties an instance of [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) to its [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span>

<span data-ttu-id="c38f2-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c38f2-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c38f2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c38f2-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricInstance : CIM_MetricInstance
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c38f2-108">Члены</span><span class="sxs-lookup"><span data-stu-id="c38f2-108">Members</span></span>

<span data-ttu-id="c38f2-109">Класс **мсвм \_ метриЦинстанце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c38f2-109">The **Msvm\_MetricInstance** class has these types of members:</span></span>

-   [<span data-ttu-id="c38f2-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c38f2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c38f2-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="c38f2-111">Properties</span></span>

<span data-ttu-id="c38f2-112">Класс **мсвм \_ метриЦинстанце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c38f2-112">The **Msvm\_MetricInstance** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c38f2-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="c38f2-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38f2-114">Тип данных: \* \* \* \* CIM \_ манажеделемент \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="c38f2-114">Data type: \*\*\*\*CIM\_ManagedElement\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="c38f2-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38f2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38f2-116">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="c38f2-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c38f2-117">Ссылка на экземпляр класса [**мсвм \_ басеметрикдефинитион**](msvm-basemetricdefinition.md) , представляющий определения метрик.</span><span class="sxs-lookup"><span data-stu-id="c38f2-117">A reference to an instance of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) class that represents the metrics definitions.</span></span>

</dd> <dt>

<span data-ttu-id="c38f2-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="c38f2-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38f2-119">Тип данных: \* \* \* \* CIM \_ манажеделемент \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="c38f2-119">Data type: \*\*\*\*CIM\_ManagedElement\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="c38f2-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38f2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38f2-121">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="c38f2-121">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c38f2-122">Ссылка на экземпляр класса [**мсвм \_ басеметриквалуе**](msvm-basemetricvalue.md) , представляющий метрики, зависящие от **предшествующей задачи**.</span><span class="sxs-lookup"><span data-stu-id="c38f2-122">A reference to an instance of the [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) class that represents the metrics that are dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c38f2-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c38f2-123">Requirements</span></span>



| <span data-ttu-id="c38f2-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c38f2-124">Requirement</span></span> | <span data-ttu-id="c38f2-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c38f2-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c38f2-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c38f2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c38f2-127">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c38f2-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c38f2-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c38f2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c38f2-129">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c38f2-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c38f2-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c38f2-130">Namespace</span></span><br/>                | <span data-ttu-id="c38f2-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c38f2-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c38f2-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c38f2-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c38f2-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c38f2-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c38f2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c38f2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c38f2-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c38f2-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




