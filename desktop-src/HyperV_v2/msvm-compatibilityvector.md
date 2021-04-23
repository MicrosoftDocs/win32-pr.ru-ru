---
description: Ссылается на сведения о совместимости для виртуальной машины (ВМ) (при запуске на компьютере виртуальной машины) или на узле (при запуске в системе главного компьютера).
ms.assetid: A3DB75BF-91C8-444E-B273-25DF8A5BFA7B
title: Класс Msvm_CompatibilityVector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CompatibilityVector
- Msvm_CompatibilityVector.VectorId
- Msvm_CompatibilityVector.CompareOperation
- Msvm_CompatibilityVector.CompatibilityInfo
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66eba92daf420fb4bd332d3f7d537b7936618ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911031"
---
# <a name="msvm_compatibilityvector-class"></a><span data-ttu-id="c3e3f-103">\_Класс мсвм компатибилитивектор</span><span class="sxs-lookup"><span data-stu-id="c3e3f-103">Msvm\_CompatibilityVector class</span></span>

<span data-ttu-id="c3e3f-104">Ссылается на сведения о совместимости для виртуальной машины (ВМ) (при запуске на компьютере виртуальной машины) или на узле (при запуске в системе главного компьютера).</span><span class="sxs-lookup"><span data-stu-id="c3e3f-104">References the compatibility info for a virtual machine (VM) (when run on a VM computer system) or a host (when run on a host computer system).</span></span>

<span data-ttu-id="c3e3f-105">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3e3f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3e3f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CompatibilityVector
{
  uint32 VectorId;
  uint32 CompareOperation;
  uint64 CompatibilityInfo;
};
```

## <a name="members"></a><span data-ttu-id="c3e3f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c3e3f-107">Members</span></span>

<span data-ttu-id="c3e3f-108">Класс **мсвм \_ компатибилитивектор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c3e3f-108">The **Msvm\_CompatibilityVector** class has these types of members:</span></span>

-   [<span data-ttu-id="c3e3f-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c3e3f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c3e3f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c3e3f-110">Properties</span></span>

<span data-ttu-id="c3e3f-111">Класс **мсвм \_ компатибилитивектор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-111">The **Msvm\_CompatibilityVector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3e3f-112">**компареоператион**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-112">**CompareOperation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3e3f-113">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3e3f-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3e3f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3e3f-115">Определяет операцию сравнения, которая будет возвращать значение true только в случае, если два вектора совместимы.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-115">Identifies the comparison operation that will return true if and only if two vectors are compatible.</span></span> <span data-ttu-id="c3e3f-116">Данные виртуальной машины находятся в левой части сравнения, а данные узла — в правой части.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-116">The VM's data is on the left hand side of the comparison, and the host's data is on the right hand side.</span></span>

<dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>

<span data-ttu-id="c3e3f-117">**Равно** (0)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-117">**Equal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Superset"></span><span id="superset"></span><span id="SUPERSET"></span>

<span data-ttu-id="c3e3f-118">**Супермножество** (1)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-118">**Superset** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Subset"></span><span id="subset"></span><span id="SUBSET"></span>

<span data-ttu-id="c3e3f-119">**Подмножество** (2)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-119">**Subset** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disjoint"></span><span id="disjoint"></span><span id="DISJOINT"></span>

<span data-ttu-id="c3e3f-120">Несвязанная **(3** )</span><span class="sxs-lookup"><span data-stu-id="c3e3f-120">**Disjoint** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="GreaterThan"></span><span id="greaterthan"></span><span id="GREATERTHAN"></span>

<span data-ttu-id="c3e3f-121">**GreaterThan** (4)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-121">**GreaterThan** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="GreaterThanOrEqual"></span><span id="greaterthanorequal"></span><span id="GREATERTHANOREQUAL"></span>

<span data-ttu-id="c3e3f-122">**GreaterThanOrEqual** (5)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-122">**GreaterThanOrEqual** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="LessThan"></span><span id="lessthan"></span><span id="LESSTHAN"></span>

<span data-ttu-id="c3e3f-123">**LessThan** (6)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-123">**LessThan** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="LessThanOrEqual"></span><span id="lessthanorequal"></span><span id="LESSTHANOREQUAL"></span>

<span data-ttu-id="c3e3f-124">**LessThanOrEqual** (7)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-124">**LessThanOrEqual** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiple"></span><span id="multiple"></span><span id="MULTIPLE"></span>

<span data-ttu-id="c3e3f-125">**Несколько** (8)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-125">**Multiple** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Divisible"></span><span id="divisible"></span><span id="DIVISIBLE"></span>

<span data-ttu-id="c3e3f-126">**Кратные** (9)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-126">**Divisible** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c3e3f-127">**компатибилитинфо**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-127">**CompatibilityInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3e3f-128">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3e3f-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3e3f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3e3f-130">Фактические данные атрибута совместимости, используемые для сравнения.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-130">The actual compatibility attribute data that is used for comparison.</span></span>

</dd> <dt>

<span data-ttu-id="c3e3f-131">**векторид**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-131">**VectorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3e3f-132">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3e3f-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3e3f-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3e3f-134">Определяет вектор совместимости, представляющий конкретный атрибут.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-134">Identifies a compatibility vector that represents a specific attribute.</span></span> <span data-ttu-id="c3e3f-135">Это свойство используется для сопоставления соответствующих векторов между узлом и виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-135">This property is used to match corresponding vectors between a host and a VM.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3e3f-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3e3f-136">Remarks</span></span>

<span data-ttu-id="c3e3f-137">Метод [**жетсистемкомпатибилитивекторс**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) класса [**мсвм \_ Виртуалсистеммигратионсервице**](msvm-virtualsystemmigrationservice.md) возвращает массив экземпляров **мсвм \_ компатибилитивектор** для узла (если выполняется на узле) или виртуальной машины (если она выполняется на виртуальной машине).</span><span class="sxs-lookup"><span data-stu-id="c3e3f-137">The [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class returns an array of **Msvm\_CompatibilityVector** instances for the host (if run on the host) or a VM (if run on the VM).</span></span> <span data-ttu-id="c3e3f-138">Каждая запись **мсвм \_ компатибилитивектор** в списке описывает вектор атрибута совместимости.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-138">Each **Msvm\_CompatibilityVector** entry in the list describes a compatibility attribute vector.</span></span> <span data-ttu-id="c3e3f-139">Чтобы виртуальная машина была совместима с узлом, все его атрибуты совместимости должны быть совместимы с атрибутами узла s.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-139">For a VM to be compatible with a host, all of its compatibility attributes must be compatible with the host s attributes.</span></span>

<span data-ttu-id="c3e3f-140">Каждая **запись \_ компатибилитивектор мсвм** имеет следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="c3e3f-140">Each **Msvm\_CompatibilityVector** entry has these properties:</span></span>

<dl> <dt>

<span data-ttu-id="c3e3f-141">**векторид**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-141">**VectorId**</span></span>
</dt> <dd>

<span data-ttu-id="c3e3f-142">Однозначно определяет вектор совместимости.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-142">Uniquely identifies the compatibility vector.</span></span> <span data-ttu-id="c3e3f-143">Используется для сопоставления векторов для сравнения между узлом и виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-143">This is used to match the vectors to compare between a host and a VM.</span></span>

</dd> <dt>

<span data-ttu-id="c3e3f-144">**компареоператион**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-144">**CompareOperation**</span></span>
</dt> <dd>

<span data-ttu-id="c3e3f-145">Определяет операцию сравнения, которая определяет, совместимы ли векторы.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-145">Identifies the comparison operation that determines whether the vectors are compatible.</span></span>

</dd> <dt>

<span data-ttu-id="c3e3f-146">**компатибилитинфо**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-146">**CompatibilityInfo**</span></span>
</dt> <dd>

<span data-ttu-id="c3e3f-147">Содержит атрибут фактической совместимости; Это фактически полезная нагрузка атрибута (например, маска характеристик процессора, размер буфера записи кэша и т. д.).</span><span class="sxs-lookup"><span data-stu-id="c3e3f-147">Contains the actual compatibility attribute; This is effectively the attribute payload (e.g. processor feature mask, cache line flush size, etc.)</span></span>

</dd> </dl>

<span data-ttu-id="c3e3f-148">Набор операций, определенных для **компареоператион** , просто подразумевает базовое сравнение целых чисел и побитовую логику.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-148">The set of operations defined for **CompareOperation** just involve basic integer comparison and bitwise logic.</span></span> <span data-ttu-id="c3e3f-149">Это позволяет действительное содержимое **компатибилитинфо** оставаться непрозрачным.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-149">This enables the actual contents of **CompatibilityInfo** to remain opaque.</span></span> <span data-ttu-id="c3e3f-150">Набор операций включает:</span><span class="sxs-lookup"><span data-stu-id="c3e3f-150">The set of operations include:</span></span>



| <span data-ttu-id="c3e3f-151">компареоператион</span><span class="sxs-lookup"><span data-stu-id="c3e3f-151">CompareOperation</span></span> | <span data-ttu-id="c3e3f-152">Описание</span><span class="sxs-lookup"><span data-stu-id="c3e3f-152">Description</span></span>                                      | <span data-ttu-id="c3e3f-153">Сравнение псевдокода</span><span class="sxs-lookup"><span data-stu-id="c3e3f-153">Pseudocode Comparison</span></span>                |
|------------------|--------------------------------------------------|--------------------------------------|
| <span data-ttu-id="c3e3f-154">вмкцекуал</span><span class="sxs-lookup"><span data-stu-id="c3e3f-154">VmCcEqual</span></span>        | <span data-ttu-id="c3e3f-155">Вматтр должен равняться Хостаттр</span><span class="sxs-lookup"><span data-stu-id="c3e3f-155">VmAttr must equal HostAttr</span></span>                       | <span data-ttu-id="c3e3f-156">If (Вматтр = = Хостаттр)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-156">If (VmAttr == HostAttr)</span></span>              |
| <span data-ttu-id="c3e3f-157">вмкксуперсет</span><span class="sxs-lookup"><span data-stu-id="c3e3f-157">VmCcSuperSet</span></span>     | <span data-ttu-id="c3e3f-158">Вматтр должен быть надмножеством Хостаттр</span><span class="sxs-lookup"><span data-stu-id="c3e3f-158">VmAttr must be a superset of HostAttr</span></span>            | <span data-ttu-id="c3e3f-159">If ((Вматтр & Хостаттр) = = Хостаттр)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-159">If ((VmAttr & HostAttr) == HostAttr)</span></span> |
| <span data-ttu-id="c3e3f-160">вмкксубсет</span><span class="sxs-lookup"><span data-stu-id="c3e3f-160">VmCcSubSet</span></span>       | <span data-ttu-id="c3e3f-161">Вматтр должен быть подмножеством Хостаттр</span><span class="sxs-lookup"><span data-stu-id="c3e3f-161">VmAttr must be a subset of HostAttr</span></span>              | <span data-ttu-id="c3e3f-162">If ((Вматтр & Хостаттр) = = Вматтр)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-162">If ((VmAttr & HostAttr) == VmAttr)</span></span>   |
| <span data-ttu-id="c3e3f-163">вмккдисжоинтсет</span><span class="sxs-lookup"><span data-stu-id="c3e3f-163">VmCcDisjointSet</span></span>  | <span data-ttu-id="c3e3f-164">Вматтр должен быть несвязанным набором из Хостаттр</span><span class="sxs-lookup"><span data-stu-id="c3e3f-164">VmAttr must be a disjoint set from HostAttr</span></span>      | <span data-ttu-id="c3e3f-165">If ((Вматтр & Хостаттр) = = 0)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-165">If ((VmAttr & HostAttr) == 0)</span></span>        |
| <span data-ttu-id="c3e3f-166">вмккгреатер</span><span class="sxs-lookup"><span data-stu-id="c3e3f-166">VmCcGreater</span></span>      | <span data-ttu-id="c3e3f-167">Вматтр должен быть больше Хостаттр</span><span class="sxs-lookup"><span data-stu-id="c3e3f-167">VmAttr must be greater than HostAttr</span></span>             | <span data-ttu-id="c3e3f-168">If (Вматтр > Хостаттр)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-168">If (VmAttr > HostAttr)</span></span>            |
| <span data-ttu-id="c3e3f-169">вмккгреатерекуал</span><span class="sxs-lookup"><span data-stu-id="c3e3f-169">VmCcGreaterEqual</span></span> | <span data-ttu-id="c3e3f-170">Вматтр должно быть больше или равно Хостаттр</span><span class="sxs-lookup"><span data-stu-id="c3e3f-170">VmAttr must be greater than or equal to HostAttr</span></span> | <span data-ttu-id="c3e3f-171">If (Вматтр >= Хостаттр)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-171">If (VmAttr >= HostAttr)</span></span>           |
| <span data-ttu-id="c3e3f-172">вмкклесс</span><span class="sxs-lookup"><span data-stu-id="c3e3f-172">VmCcLess</span></span>         | <span data-ttu-id="c3e3f-173">Вматтр должно быть меньше Хостаттр</span><span class="sxs-lookup"><span data-stu-id="c3e3f-173">VmAttr must be less than HostAttr</span></span>                | <span data-ttu-id="c3e3f-174">If (Вматтр < Хостаттр)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-174">If (VmAttr < HostAttr)</span></span>            |
| <span data-ttu-id="c3e3f-175">вмкклессекуал</span><span class="sxs-lookup"><span data-stu-id="c3e3f-175">VmCcLessEqual</span></span>    | <span data-ttu-id="c3e3f-176">Вматтр должно быть меньше или равно Хостаттр</span><span class="sxs-lookup"><span data-stu-id="c3e3f-176">VmAttr must be less than or equal to HostAttr</span></span>    | <span data-ttu-id="c3e3f-177">If (Вматтр <= Хостаттр)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-177">If (VmAttr <= HostAttr)</span></span>           |
| <span data-ttu-id="c3e3f-178">вмккмултипле</span><span class="sxs-lookup"><span data-stu-id="c3e3f-178">VmCcMultiple</span></span>     | <span data-ttu-id="c3e3f-179">Вматтр должен быть кратен Хостаттр</span><span class="sxs-lookup"><span data-stu-id="c3e3f-179">VmAttr must be a multiple of HostAttr</span></span>            | <span data-ttu-id="c3e3f-180">If ((Вматтр% Хостаттр) = = 0)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-180">If ((VmAttr % HostAttr) == 0)</span></span>        |
| <span data-ttu-id="c3e3f-181">вмккдивисор</span><span class="sxs-lookup"><span data-stu-id="c3e3f-181">VmCcDivisor</span></span>      | <span data-ttu-id="c3e3f-182">Вматтр должен быть делителем Хостаттр</span><span class="sxs-lookup"><span data-stu-id="c3e3f-182">VmAttr must be a divisor of HostAttr</span></span>             | <span data-ttu-id="c3e3f-183">If ((Хостаттр% Вматтр) = = 0)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-183">If ((HostAttr % VmAttr) == 0)</span></span>        |



 

<span data-ttu-id="c3e3f-184">SCVMM необходимо выполнить эти действия, чтобы определить, совместима ли виртуальная машина с узлом.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-184">SCVMM needs to do these steps to determine whether a VM is compatible with a host.</span></span>

<span data-ttu-id="c3e3f-185">**Определение, совместима ли виртуальная машина с узлом**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-185">**To determine whether a VM is compatible with a host**</span></span>

1.  <span data-ttu-id="c3e3f-186">Выполните итерацию всех элементов **мсвм \_ компатибилитивектор** для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-186">Iterate through all of the **Msvm\_CompatibilityVector** elements for the VM.</span></span>
2.  <span data-ttu-id="c3e3f-187">Для каждого **элемента \_ компатибилитивектор мсвм** используйте операцию совместимости, указанную в **компареоператион** , чтобы сравнить вектор совместимости оборудования VM s с соответствующим вектором совместимости для узла.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-187">For each **Msvm\_CompatibilityVector** element, use the compatibility operation specified in **CompareOperation** to compare the VM s hardware compatibility vector with the corresponding compatibility vector for the host.</span></span>
3.  <span data-ttu-id="c3e3f-188">Если все элементы **мсвм \_ компатибилитивектор** из виртуальной машины считаются совместимыми, то виртуальная машина совместима с узлом (с точки зрения функциональности процессора).</span><span class="sxs-lookup"><span data-stu-id="c3e3f-188">If the all of the **Msvm\_CompatibilityVector** elements from the VM are deemed compatible, the VM is compatible with the host (from a processor feature perspective).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3e3f-189">Требования</span><span class="sxs-lookup"><span data-stu-id="c3e3f-189">Requirements</span></span>



| <span data-ttu-id="c3e3f-190">Требование</span><span class="sxs-lookup"><span data-stu-id="c3e3f-190">Requirement</span></span> | <span data-ttu-id="c3e3f-191">Значение</span><span class="sxs-lookup"><span data-stu-id="c3e3f-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3e3f-192">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3e3f-192">Minimum supported client</span></span><br/> | <span data-ttu-id="c3e3f-193">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c3e3f-193">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c3e3f-194">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3e3f-194">Minimum supported server</span></span><br/> | <span data-ttu-id="c3e3f-195">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c3e3f-195">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c3e3f-196">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c3e3f-196">Namespace</span></span><br/>                | <span data-ttu-id="c3e3f-197">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c3e3f-197">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c3e3f-198">MOF</span><span class="sxs-lookup"><span data-stu-id="c3e3f-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3e3f-199"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3e3f-199"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3e3f-200">DLL</span><span class="sxs-lookup"><span data-stu-id="c3e3f-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3e3f-201"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c3e3f-201"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c3e3f-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3e3f-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3e3f-203">**жетсистемкомпатибилитивекторс**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-203">**GetSystemCompatibilityVectors**</span></span>](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="c3e3f-204">**Мсвм \_ виртуалсистеммигратионсервице**</span><span class="sxs-lookup"><span data-stu-id="c3e3f-204">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




