---
description: Содержит сведения о батарее.
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: Структура BATTERY_INFORMATION (Покласс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 1e892a14263822ddd009b162c6343975e1689683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663132"
---
# <a name="battery_information-structure"></a><span data-ttu-id="92038-103">\_Структура сведений о батарее</span><span class="sxs-lookup"><span data-stu-id="92038-103">BATTERY\_INFORMATION structure</span></span>

<span data-ttu-id="92038-104">Содержит сведения о батарее.</span><span class="sxs-lookup"><span data-stu-id="92038-104">Contains battery information.</span></span> <span data-ttu-id="92038-105">Эта структура возвращается с помощью кода [**управления \_ \_ \_ данными о запросе аккумулятора через батарею**](ioctl-battery-query-information.md) при запросе уровня информации баттеринформатион.</span><span class="sxs-lookup"><span data-stu-id="92038-105">This structure is returned by the [**IOCTL\_BATTERY\_QUERY\_INFORMATION**](ioctl-battery-query-information.md) control code when the BatteryInformation information level is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="92038-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92038-106">Syntax</span></span>


```C++
typedef struct _BATTERY_INFORMATION {
  ULONG Capabilities;
  UCHAR Technology;
  UCHAR Reserved[3];
  UCHAR Chemistry[4];
  ULONG DesignedCapacity;
  ULONG FullChargedCapacity;
  ULONG DefaultAlert1;
  ULONG DefaultAlert2;
  ULONG CriticalBias;
  ULONG CycleCount;
} BATTERY_INFORMATION, *PBATTERY_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="92038-107">Члены</span><span class="sxs-lookup"><span data-stu-id="92038-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="92038-108">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="92038-108">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="92038-109">Возможности аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="92038-109">The battery capabilities.</span></span> <span data-ttu-id="92038-110">Этот элемент может иметь одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="92038-110">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="92038-111">Значение</span><span class="sxs-lookup"><span data-stu-id="92038-111">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="92038-112">Значение</span><span class="sxs-lookup"><span data-stu-id="92038-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <span data-ttu-id="92038-113"><dt>**Батарея \_ \_Относительная емкость**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="92038-113"><dt>**BATTERY\_CAPACITY\_RELATIVE**</dt> <dt>0x40000000</dt></span></span> </dl>                    | <span data-ttu-id="92038-114">Указывает, что данные о емкости батареи и скорости относительны, а не в конкретных единицах.</span><span class="sxs-lookup"><span data-stu-id="92038-114">Indicates that the battery capacity and rate information are relative, and not in any specific units.</span></span> <span data-ttu-id="92038-115">Если этот бит не задан, то единицы отчетности — диаграмме милливаттах-hours (mWh) для емкости и МВт (mW) для ставки.</span><span class="sxs-lookup"><span data-stu-id="92038-115">If this bit is not set, the reporting units are milliwatt-hours (mWh) for capacity and milliwatts (mW) for rate.</span></span> <span data-ttu-id="92038-116">Если этот бит задан, все ссылки на модули в другой документации батареи можно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="92038-116">If this bit is set, all references to units in the other battery documentation can be ignored.</span></span> <span data-ttu-id="92038-117">Все сведения о частоте выводятся в единицах в час.</span><span class="sxs-lookup"><span data-stu-id="92038-117">All rate information is reported in units per hour.</span></span> <span data-ttu-id="92038-118">Например, если объем полностью заряженной емкости указывается как 100, то частота 200 указывает, что батарея будет использовать всю емкость в половину часа.</span><span class="sxs-lookup"><span data-stu-id="92038-118">For example, if the fully charged capacity is reported as 100, a rate of 200 indicates that the battery will use all of its capacity in half an hour.</span></span><br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <span data-ttu-id="92038-119"><dt>**Батарея \_ \_Краткосрочное \_**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="92038-119"><dt>**BATTERY\_IS\_SHORT\_TERM**</dt> <dt>0x20000000</dt></span></span> </dl>                               | <span data-ttu-id="92038-120">Указывает, что нормальная операция предназначена для резервной функции.</span><span class="sxs-lookup"><span data-stu-id="92038-120">Indicates that the normal operation is for a fail-safe function.</span></span> <span data-ttu-id="92038-121">Если этот бит не задан, предполагается, что батарея будет использоваться во время обычного использования системы.</span><span class="sxs-lookup"><span data-stu-id="92038-121">If this bit is not set the battery is expected to be used during normal system usage.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <span data-ttu-id="92038-122"><dt>**Батарея \_ НАБОР \_ \_ поддерживаемых задержек**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="92038-122"><dt>**BATTERY\_SET\_CHARGE\_SUPPORTED**</dt> <dt>0x00000001</dt></span></span> </dl>          | <span data-ttu-id="92038-123">Указывает, что данные о наборе запросов типа Баттеричарже поддерживаются этим устройством батареи.</span><span class="sxs-lookup"><span data-stu-id="92038-123">Indicates that set information requests of the type BatteryCharge are supported by this battery device.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <span data-ttu-id="92038-124"><dt>**Батарея \_ Установка \_ \_ поддерживаемого разряда**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="92038-124"><dt>**BATTERY\_SET\_DISCHARGE\_SUPPORTED**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="92038-125">Указывает, что данные о наборе запросов типа Баттеридисчарже поддерживаются этим устройством батареи.</span><span class="sxs-lookup"><span data-stu-id="92038-125">Indicates that set information requests of the type BatteryDischarge are supported by this battery device.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <span data-ttu-id="92038-126"><dt>**Батарея \_ СИСТЕМНЫЙ \_ аккумулятор**</dt> , <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="92038-126"><dt>**BATTERY\_SYSTEM\_BATTERY**</dt> <dt>0x80000000</dt></span></span> </dl>                             | <span data-ttu-id="92038-127">Указывает, что батарея может обеспечить общую мощность для работы системы.</span><span class="sxs-lookup"><span data-stu-id="92038-127">Indicates that the battery can provide general power to run the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="92038-128">**Технология**</span><span class="sxs-lookup"><span data-stu-id="92038-128">**Technology**</span></span>
</dt> <dd>

<span data-ttu-id="92038-129">Технология аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="92038-129">The battery technology.</span></span> <span data-ttu-id="92038-130">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="92038-130">This member can be one of the following values.</span></span>



| <span data-ttu-id="92038-131">Значение</span><span class="sxs-lookup"><span data-stu-id="92038-131">Value</span></span>                                                                        | <span data-ttu-id="92038-132">Значение</span><span class="sxs-lookup"><span data-stu-id="92038-132">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="92038-133"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="92038-133"><dt>0</dt></span></span> </dl> | <span data-ttu-id="92038-134">Несменный аккумулятор, например алкалине.</span><span class="sxs-lookup"><span data-stu-id="92038-134">Nonrechargeable battery, for example, alkaline.</span></span><br/> |
| <dl> <span data-ttu-id="92038-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="92038-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="92038-136">Аккумулятор, например, ведущий ACID.</span><span class="sxs-lookup"><span data-stu-id="92038-136">Rechargeable battery, for example, lead acid.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="92038-137">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="92038-137">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="92038-138">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="92038-138">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="92038-139">**Химия**</span><span class="sxs-lookup"><span data-stu-id="92038-139">**Chemistry**</span></span>
</dt> <dd>

<span data-ttu-id="92038-140">Сокращенная строка символов, указывающая химия батареи.</span><span class="sxs-lookup"><span data-stu-id="92038-140">An abbreviated character string that indicates the battery's chemistry.</span></span> <span data-ttu-id="92038-141">Эта строка не обязательно завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="92038-141">This string is not necessarily zero-terminated.</span></span> <span data-ttu-id="92038-142">Ниже приведен неполный список сокращений, которые могут быть возвращены, и связанный чемистриес.</span><span class="sxs-lookup"><span data-stu-id="92038-142">The following is a partial list of abbreviations that can be returned and the associated chemistries.</span></span>



| <span data-ttu-id="92038-143">Строка Юникода</span><span class="sxs-lookup"><span data-stu-id="92038-143">Unicode string</span></span>                                                                                                                                           | <span data-ttu-id="92038-144">Значение</span><span class="sxs-lookup"><span data-stu-id="92038-144">Meaning</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <span data-ttu-id="92038-145"><dt>**пбак**</dt></span><span class="sxs-lookup"><span data-stu-id="92038-145"><dt>**PbAc**</dt></span></span> </dl> | <span data-ttu-id="92038-146">ACID, ведущий</span><span class="sxs-lookup"><span data-stu-id="92038-146">Lead Acid</span></span><br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <span data-ttu-id="92038-147"><dt>**LION**</dt></span><span class="sxs-lookup"><span data-stu-id="92038-147"><dt>**LION**</dt></span></span> </dl>                        | <span data-ttu-id="92038-148">Литий — ионный</span><span class="sxs-lookup"><span data-stu-id="92038-148">Lithium Ion</span></span><br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <span data-ttu-id="92038-149"><dt>**Li-I**</dt></span><span class="sxs-lookup"><span data-stu-id="92038-149"><dt>**Li-I**</dt></span></span> </dl> | <span data-ttu-id="92038-150">Литий — ионный</span><span class="sxs-lookup"><span data-stu-id="92038-150">Lithium Ion</span></span><br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <span data-ttu-id="92038-151"><dt>**никд**</dt></span><span class="sxs-lookup"><span data-stu-id="92038-151"><dt>**NiCd**</dt></span></span> </dl> | <span data-ttu-id="92038-152">Никель кадмиум</span><span class="sxs-lookup"><span data-stu-id="92038-152">Nickel Cadmium</span></span><br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <span data-ttu-id="92038-153"><dt>**нимх**</dt></span><span class="sxs-lookup"><span data-stu-id="92038-153"><dt>**NiMH**</dt></span></span> </dl> | <span data-ttu-id="92038-154">Никель металла Хидриде</span><span class="sxs-lookup"><span data-stu-id="92038-154">Nickel Metal Hydride</span></span><br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <span data-ttu-id="92038-155"><dt>**низн**</dt></span><span class="sxs-lookup"><span data-stu-id="92038-155"><dt>**NiZn**</dt></span></span> </dl> | <span data-ttu-id="92038-156">Никель зинк</span><span class="sxs-lookup"><span data-stu-id="92038-156">Nickel Zinc</span></span><br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <span data-ttu-id="92038-157"><dt>**ОЗУ**</dt></span><span class="sxs-lookup"><span data-stu-id="92038-157"><dt>**RAM**</dt></span></span> </dl>                           | <span data-ttu-id="92038-158">Alkaline-Manganese</span><span class="sxs-lookup"><span data-stu-id="92038-158">Rechargeable Alkaline-Manganese</span></span><br/> |



 

<span data-ttu-id="92038-159">Другие чемистриес могут появиться в будущем, и ваш код должен уметь их обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="92038-159">Other chemistries may appear in the future and your code should be able to handle them.</span></span>

</dd> <dt>

<span data-ttu-id="92038-160">**десигнедкапаЦити**</span><span class="sxs-lookup"><span data-stu-id="92038-160">**DesignedCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="92038-161">Теоретическая емкость батареи при создании в mWh, если \_ \_ не задана относительная емкость батареи.</span><span class="sxs-lookup"><span data-stu-id="92038-161">The theoretical capacity of the battery when new, in mWh unless BATTERY\_CAPACITY\_RELATIVE is set.</span></span> <span data-ttu-id="92038-162">В этом случае единицы измерения не определены.</span><span class="sxs-lookup"><span data-stu-id="92038-162">In that case, the units are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="92038-163">**фуллчаржедкапаЦити**</span><span class="sxs-lookup"><span data-stu-id="92038-163">**FullChargedCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="92038-164">Текущая полностью заряженная емкость батареи в mWh (или относительное значение).</span><span class="sxs-lookup"><span data-stu-id="92038-164">The battery's current fully charged capacity in mWh (or relative).</span></span> <span data-ttu-id="92038-165">Сравните это значение с **десигнедкапаЦити** , чтобы оценить износ аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="92038-165">Compare this value to **DesignedCapacity** to estimate the battery's wear.</span></span>

</dd> <dt>

<span data-ttu-id="92038-166">**DefaultAlert1**</span><span class="sxs-lookup"><span data-stu-id="92038-166">**DefaultAlert1**</span></span>
</dt> <dd>

<span data-ttu-id="92038-167">Предлагаемая изготовителем мощность в mWh, на которой должно быть оповещено о низком уровне заряда аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="92038-167">The manufacturer's suggested capacity, in mWh, at which a low battery alert should occur.</span></span> <span data-ttu-id="92038-168">Определения Low отличаются от производителя к изготовителю.</span><span class="sxs-lookup"><span data-stu-id="92038-168">Definitions of low vary from manufacturer to manufacturer.</span></span> <span data-ttu-id="92038-169">Как правило, состояние предупреждения возникает до низкого состояния, но не следует рассчитывать, что он всегда будет.</span><span class="sxs-lookup"><span data-stu-id="92038-169">In general, a warning state will occur before a low state, but you should not assume that it always will.</span></span> <span data-ttu-id="92038-170">Чтобы снизить риск потери данных, это значение обычно используется в качестве значения по умолчанию для оповещения о критическом питании от аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="92038-170">To reduce risk of data loss, this value is usually used as the default setting for the critical battery alarm.</span></span>

</dd> <dt>

<span data-ttu-id="92038-171">**DefaultAlert2**</span><span class="sxs-lookup"><span data-stu-id="92038-171">**DefaultAlert2**</span></span>
</dt> <dd>

<span data-ttu-id="92038-172">Предлагаемая изготовителем мощность, в mWh, с которой должно появиться предупреждение о батарее.</span><span class="sxs-lookup"><span data-stu-id="92038-172">The manufacturer's suggested capacity, in mWh, at which a warning battery alert should occur.</span></span> <span data-ttu-id="92038-173">Определения предупреждений отличаются от производителя к изготовителю.</span><span class="sxs-lookup"><span data-stu-id="92038-173">Definitions of warning vary from manufacturer to manufacturer.</span></span> <span data-ttu-id="92038-174">Как правило, состояние предупреждения возникает до низкого состояния, но не следует рассчитывать, что он всегда будет.</span><span class="sxs-lookup"><span data-stu-id="92038-174">In general, a warning state will occur before a low state, but you should not assume that it always will.</span></span> <span data-ttu-id="92038-175">Чтобы снизить риск потери данных, это значение обычно используется в качестве значения по умолчанию для сигнала низкого заряда батареи.</span><span class="sxs-lookup"><span data-stu-id="92038-175">To reduce risk of data loss, this value is usually used as the default setting for the low battery alarm.</span></span>

</dd> <dt>

<span data-ttu-id="92038-176">**критикалбиас**</span><span class="sxs-lookup"><span data-stu-id="92038-176">**CriticalBias**</span></span>
</dt> <dd>

<span data-ttu-id="92038-177">Смещение от нуля в mWh, которое применяется к отчетам о батареях.</span><span class="sxs-lookup"><span data-stu-id="92038-177">A bias from zero, in mWh, which is applied to battery reporting.</span></span> <span data-ttu-id="92038-178">Некоторые батареи зарезервированы небольшие затраты, которые смещены от значений емкости аккумулятора, чтобы отобразить "0" как уровень критического аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="92038-178">Some batteries reserve a small charge that is biased out of the battery's capacity values to show "0" as the critical battery level.</span></span> <span data-ttu-id="92038-179">Критический сдвиг аналогичен настройке датчика горючего для отображения пустого значения, если осталось несколько литр горючего.</span><span class="sxs-lookup"><span data-stu-id="92038-179">Critical bias is analogous to setting a fuel gauge to show "empty" when there are several liters of fuel left.</span></span>

</dd> <dt>

<span data-ttu-id="92038-180">**циклекаунт**</span><span class="sxs-lookup"><span data-stu-id="92038-180">**CycleCount**</span></span>
</dt> <dd>

<span data-ttu-id="92038-181">Количество циклов зарядки аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="92038-181">The number of charge/discharge cycles the battery has experienced.</span></span> <span data-ttu-id="92038-182">Это дает возможность определить износ аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="92038-182">This provides a means to determine the battery's wear.</span></span> <span data-ttu-id="92038-183">Если батарея не поддерживает счетчик цикла, этот элемент равен нулю.</span><span class="sxs-lookup"><span data-stu-id="92038-183">If the battery does not support a cycle counter, this member is zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92038-184">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92038-184">Remarks</span></span>

<span data-ttu-id="92038-185">Как правило, состояние предупреждения возникает перед низким состоянием, но не следует рассчитывать на это.</span><span class="sxs-lookup"><span data-stu-id="92038-185">Generally, a warning state occurs before a low state, but you should not assume it will.</span></span> <span data-ttu-id="92038-186">Можно опросить батарею и обнаружить, что ни один из уровней оповещений не появлялся, и снова опросить батарею и найдет, что он будет отыскиваться в той степени, в которой были достигнуты оба уровня.</span><span class="sxs-lookup"><span data-stu-id="92038-186">It is possible to poll a battery and find that neither alert level has occurred, and poll the battery again and find it discharged to the extent that both levels have been achieved.</span></span> <span data-ttu-id="92038-187">Это может означать, что опросы недостаточно часто.</span><span class="sxs-lookup"><span data-stu-id="92038-187">This may indicate that you are not polling often enough.</span></span> <span data-ttu-id="92038-188">Это также может означать, что батарея не может удерживать плату за очень длинные и выплатить более быстро, чем ожидалось.</span><span class="sxs-lookup"><span data-stu-id="92038-188">It may also indicate that the battery is unable to hold a charge for very long and is discharging more rapidly than you expected.</span></span> <span data-ttu-id="92038-189">Возможно, батарея приближается к концу ее полезного времени или повреждена.</span><span class="sxs-lookup"><span data-stu-id="92038-189">Such a battery may be nearing the end of its useful life, or it may be damaged.</span></span>

## <a name="requirements"></a><span data-ttu-id="92038-190">Требования</span><span class="sxs-lookup"><span data-stu-id="92038-190">Requirements</span></span>



| <span data-ttu-id="92038-191">Требование</span><span class="sxs-lookup"><span data-stu-id="92038-191">Requirement</span></span> | <span data-ttu-id="92038-192">Значение</span><span class="sxs-lookup"><span data-stu-id="92038-192">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92038-193">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92038-193">Minimum supported client</span></span><br/> | <span data-ttu-id="92038-194">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="92038-194">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="92038-195">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92038-195">Minimum supported server</span></span><br/> | <span data-ttu-id="92038-196">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="92038-196">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="92038-197">Header</span><span class="sxs-lookup"><span data-stu-id="92038-197">Header</span></span><br/>                   | <dl> <span data-ttu-id="92038-198"><dt>Покласс. h; </dt> <dt>Баткласс. h в Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="92038-198"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92038-199">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92038-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92038-200">**\_ \_ сведения о запросе от аккумулятора ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="92038-200">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> </dl>

 

 




