---
description: Представляет значение метрики, определенное экземпляром \_ класса мсвм басеметрикдефинитион.
ms.assetid: bd872f21-ab71-4ab7-88d3-b26dd2fbdbe5
title: Класс Msvm_BaseMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricValue
- Msvm_BaseMetricValue.InstanceID
- Msvm_BaseMetricValue.Caption
- Msvm_BaseMetricValue.Description
- Msvm_BaseMetricValue.ElementName
- Msvm_BaseMetricValue.MetricDefinitionId
- Msvm_BaseMetricValue.MeasuredElementName
- Msvm_BaseMetricValue.TimeStamp
- Msvm_BaseMetricValue.Duration
- Msvm_BaseMetricValue.MetricValue
- Msvm_BaseMetricValue.BreakdownDimension
- Msvm_BaseMetricValue.BreakdownValue
- Msvm_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0e566de4822b271dcd4633c3dba35f7c88495bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912592"
---
# <a name="msvm_basemetricvalue-class"></a><span data-ttu-id="02525-103">\_Класс мсвм басеметриквалуе</span><span class="sxs-lookup"><span data-stu-id="02525-103">Msvm\_BaseMetricValue class</span></span>

<span data-ttu-id="02525-104">Представляет значение метрики, определенное экземпляром класса [**мсвм \_ басеметрикдефинитион**](msvm-basemetricdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="02525-104">Represents a metric value defined by an instance of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) class.</span></span>

<span data-ttu-id="02525-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="02525-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="02525-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02525-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricValue : CIM_BaseMetricValue
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
};
```

## <a name="members"></a><span data-ttu-id="02525-107">Члены</span><span class="sxs-lookup"><span data-stu-id="02525-107">Members</span></span>

<span data-ttu-id="02525-108">Класс **мсвм \_ басеметриквалуе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="02525-108">The **Msvm\_BaseMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="02525-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="02525-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02525-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="02525-110">Properties</span></span>

<span data-ttu-id="02525-111">Класс **мсвм \_ басеметриквалуе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="02525-111">The **Msvm\_BaseMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02525-112">**бреакдовндименсион**</span><span class="sxs-lookup"><span data-stu-id="02525-112">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02525-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02525-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02525-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02525-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02525-115">Указывает одно измерение декомпозиции из массива **бреакдовндименсионс** , определенного в связанном [**мсвм \_ басеметрикдефинитион**](msvm-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="02525-115">Specifies one breakdown dimension from the **BreakdownDimensions** array defined in the associated [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span> <span data-ttu-id="02525-116">Это измерение, в котором этот набор значений метрик разбит на части.</span><span class="sxs-lookup"><span data-stu-id="02525-116">This is the dimension along which this set of metric values is broken down.</span></span> <span data-ttu-id="02525-117">Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="02525-117">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="02525-118">**бреакдовнвалуе**</span><span class="sxs-lookup"><span data-stu-id="02525-118">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02525-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02525-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02525-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02525-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02525-121">Определяет значение свойства **бреакдовндименсион** , определенного для данного экземпляра значения метрики.</span><span class="sxs-lookup"><span data-stu-id="02525-121">Defines a value of the **BreakdownDimension** property defined for this metric value instance.</span></span> <span data-ttu-id="02525-122">Например, если **бреакдовндименсион** имеет значение "трансактионнаме", это свойство может наименовать фактическую транзакцию, к которой применяется это конкретное метрика.</span><span class="sxs-lookup"><span data-stu-id="02525-122">For example, if the **BreakdownDimension** is "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span> <span data-ttu-id="02525-123">Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="02525-123">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="02525-124">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="02525-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02525-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02525-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02525-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02525-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02525-127">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="02525-127">A short description of the object.</span></span> <span data-ttu-id="02525-128">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="02525-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="02525-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="02525-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02525-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02525-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02525-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02525-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02525-132">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="02525-132">A description of the object.</span></span> <span data-ttu-id="02525-133">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="02525-133">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="02525-134">**Длительность**</span><span class="sxs-lookup"><span data-stu-id="02525-134">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02525-135">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="02525-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="02525-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02525-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02525-137">Указывает период времени, в течение которого это значение метрики является допустимым.</span><span class="sxs-lookup"><span data-stu-id="02525-137">Specifies the time duration over which this metric value is valid.</span></span> <span data-ttu-id="02525-138">Это свойство не должно существовать для меток времени, которые применяются только к моменту времени, но должны быть указаны для значений, которые считаются допустимыми в течение определенного периода времени (например, выборка).</span><span class="sxs-lookup"><span data-stu-id="02525-138">This property should not exist for time stamps that apply only to a point in time, but should be specified for values that are considered valid for a certain time period (for example, sampling).</span></span> <span data-ttu-id="02525-139">Если свойство **Duration** существует и не равно **null**, свойство **timestamp** задает конец интервала.</span><span class="sxs-lookup"><span data-stu-id="02525-139">If the **Duration** property exists and is not **Null**, the **TimeStamp** property specifies the end of the interval.</span></span> <span data-ttu-id="02525-140">Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="02525-140">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="02525-141">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="02525-141">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02525-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02525-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02525-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02525-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02525-144">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="02525-144">A display name for the object.</span></span> <span data-ttu-id="02525-145">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="02525-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="02525-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="02525-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02525-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02525-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02525-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02525-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02525-149">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="02525-149">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="02525-150">Строка, уникально идентифицирующая экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="02525-150">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="02525-151">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="02525-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="02525-152">**меасуределементнаме**</span><span class="sxs-lookup"><span data-stu-id="02525-152">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02525-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02525-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02525-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02525-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02525-155">Описательное имя элемента, которому принадлежит значение метрики (измеряемый элемент).</span><span class="sxs-lookup"><span data-stu-id="02525-155">A descriptive name for the element to which the metric value belongs (the measured element).</span></span> <span data-ttu-id="02525-156">Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="02525-156">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="02525-157">**метрикдефинитионид**</span><span class="sxs-lookup"><span data-stu-id="02525-157">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02525-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02525-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02525-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02525-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02525-160">Ключ экземпляра [**\_ басеметрикдефинитион мсвм**](msvm-basemetricdefinition.md) для этого значения.</span><span class="sxs-lookup"><span data-stu-id="02525-160">The key of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance for this value.</span></span> <span data-ttu-id="02525-161">Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="02525-161">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="02525-162">**метриквалуе**</span><span class="sxs-lookup"><span data-stu-id="02525-162">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02525-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02525-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02525-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02525-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02525-165">Значение метрики, представленное в виде строки.</span><span class="sxs-lookup"><span data-stu-id="02525-165">The value of the metric that is represented as a string.</span></span> <span data-ttu-id="02525-166">Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="02525-166">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="02525-167">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="02525-167">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02525-168">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="02525-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="02525-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02525-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02525-170">Указывает время, когда значение метрики было перехвачено или вычислено.</span><span class="sxs-lookup"><span data-stu-id="02525-170">Specifies the time when the metric value was captured or computed.</span></span> <span data-ttu-id="02525-171">Имейте в виду, что это отличается от времени создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="02525-171">Be aware that this is different from the time when the instance was created.</span></span> <span data-ttu-id="02525-172">Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="02525-172">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="02525-173">**Независимо**</span><span class="sxs-lookup"><span data-stu-id="02525-173">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02525-174">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="02525-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02525-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02525-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02525-176">Значение **true** , если значение для следующего момента времени будет использовать один и тот же экземпляр класса и просто изменить значения свойств (например, **значение** или **метку времени**).</span><span class="sxs-lookup"><span data-stu-id="02525-176">**True** if the value for the next point in time will use the same class instance and just change the property values (such as the **Value** or **TimeStamp**).</span></span> <span data-ttu-id="02525-177">Если **значение — true**, экземпляр используется повторно.</span><span class="sxs-lookup"><span data-stu-id="02525-177">If **True**, the instance is reused.</span></span> <span data-ttu-id="02525-178">Если **значение равно false**, существующие экземпляры остаются неизменными и создается новый экземпляр для нового момента времени.</span><span class="sxs-lookup"><span data-stu-id="02525-178">If **False**, the existing instances remain unchanged and a new instance is created for the new point in time.</span></span> <span data-ttu-id="02525-179">Это свойство наследуется от [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="02525-179">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02525-180">Требования</span><span class="sxs-lookup"><span data-stu-id="02525-180">Requirements</span></span>



| <span data-ttu-id="02525-181">Требование</span><span class="sxs-lookup"><span data-stu-id="02525-181">Requirement</span></span> | <span data-ttu-id="02525-182">Значение</span><span class="sxs-lookup"><span data-stu-id="02525-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02525-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02525-183">Minimum supported client</span></span><br/> | <span data-ttu-id="02525-184">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="02525-184">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="02525-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02525-185">Minimum supported server</span></span><br/> | <span data-ttu-id="02525-186">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="02525-186">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="02525-187">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="02525-187">Namespace</span></span><br/>                | <span data-ttu-id="02525-188">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="02525-188">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="02525-189">MOF</span><span class="sxs-lookup"><span data-stu-id="02525-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02525-190"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02525-190"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="02525-191">DLL</span><span class="sxs-lookup"><span data-stu-id="02525-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02525-192"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="02525-192"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

