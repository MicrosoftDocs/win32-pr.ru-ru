---
description: Метод SetPowerState \_ класса CIM унитарикомпутерсистем устанавливает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.
ms.assetid: a02991d5-3c93-4579-b1f5-f70ad7c7052b
ms.tgt_platform: multiple
title: Метод SetPowerState класса CIM_UnitaryComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UnitaryComputerSystem.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4d9b69306c7bb362dceaee254be5dae8f5d37a52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990334"
---
# <a name="setpowerstate-method-of-the-cim_unitarycomputersystem-class"></a><span data-ttu-id="ac3fc-103">Метод SetPowerState \_ класса CIM унитарикомпутерсистем</span><span class="sxs-lookup"><span data-stu-id="ac3fc-103">SetPowerState method of the CIM\_UnitaryComputerSystem class</span></span>

<span data-ttu-id="ac3fc-104">Метод **SetPowerState** \_ класса CIM унитарикомпутерсистем устанавливает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-104">The **SetPowerState** method of the CIM\_UnitaryComputerSystem class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="ac3fc-105">В подклассе набор возможных кодов возврата должен быть указан с помощью квалификатора **ValueMap** в методе.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="ac3fc-106">Строки, в которые преобразуются содержимое **ValueMap** , также должны быть указаны в подклассе как квалификатор массива **Values** .</span><span class="sxs-lookup"><span data-stu-id="ac3fc-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="ac3fc-107">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ac3fc-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ac3fc-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ac3fc-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ac3fc-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac3fc-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="ac3fc-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac3fc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac3fc-112">*PowerState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac3fc-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac3fc-113">Значение **ValueMap** , указывающее требуемое состояние питания для этого логического устройства.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="ac3fc-114"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Полная мощность** (1)</span><span class="sxs-lookup"><span data-stu-id="ac3fc-114"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ac3fc-115">Полная мощность.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-115">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ac3fc-116"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (2)</span><span class="sxs-lookup"><span data-stu-id="ac3fc-116"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ac3fc-117">Режим энергосбережения с низким энергопотреблением.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ac3fc-118"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (3)</span><span class="sxs-lookup"><span data-stu-id="ac3fc-118"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ac3fc-119">Энергосбережение в режиме ожидания.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-119">Power save   standby.</span></span>

</dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="ac3fc-120"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Энергосбережение — другие** (4)</span><span class="sxs-lookup"><span data-stu-id="ac3fc-120"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Power Save - Other** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ac3fc-121">Энергосбережение.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-121">Power save   other.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ac3fc-122"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (5)</span><span class="sxs-lookup"><span data-stu-id="ac3fc-122"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ac3fc-123">Цикл электропитания.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-123">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ac3fc-124"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (6)</span><span class="sxs-lookup"><span data-stu-id="ac3fc-124"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ac3fc-125">Выключение питания.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-125">Power off.</span></span>

</dd> <dt>

<span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>

<span data-ttu-id="ac3fc-126"><span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>**Режим гибернации** (7)</span><span class="sxs-lookup"><span data-stu-id="ac3fc-126"><span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>**Hibernate** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ac3fc-127">Режим гибернации.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-127">Hibernate.</span></span>

</dd> <dt>

<span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>

<span data-ttu-id="ac3fc-128"><span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>**Мягкое отключение** (8)</span><span class="sxs-lookup"><span data-stu-id="ac3fc-128"><span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>**Soft Off** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ac3fc-129">Мягкое отключение.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-129">Soft off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ac3fc-130">*Время* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac3fc-130">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac3fc-131">Указывает, когда должно быть установлено состояние электропитания: как обычное значение даты-времени или как значение интервала (где интервал начинается при получении вызова метода).</span><span class="sxs-lookup"><span data-stu-id="ac3fc-131">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="ac3fc-132">Если параметр *PowerState* равен 5 ("цикл электропитания"), параметр *времени* указывает, когда устройство должно снова включить питание.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-132">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="ac3fc-133">Выключение осуществляется немедленно.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-133">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac3fc-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac3fc-134">Return value</span></span>

<span data-ttu-id="ac3fc-135">Возвращает 0 (нуль) в случае успеха, 1 (один), если *указанный запрос* о сбое и *время* не поддерживаются, и другое значение, если произошла какая-либо другая ошибка.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-135">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac3fc-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac3fc-136">Remarks</span></span>

<span data-ttu-id="ac3fc-137">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-137">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="ac3fc-138">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-138">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="ac3fc-139">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-139">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ac3fc-140">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ac3fc-140">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac3fc-141">Требования</span><span class="sxs-lookup"><span data-stu-id="ac3fc-141">Requirements</span></span>



| <span data-ttu-id="ac3fc-142">Требование</span><span class="sxs-lookup"><span data-stu-id="ac3fc-142">Requirement</span></span> | <span data-ttu-id="ac3fc-143">Значение</span><span class="sxs-lookup"><span data-stu-id="ac3fc-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3fc-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac3fc-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ac3fc-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ac3fc-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ac3fc-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac3fc-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ac3fc-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac3fc-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ac3fc-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ac3fc-148">Namespace</span></span><br/>                | <span data-ttu-id="ac3fc-149">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ac3fc-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ac3fc-150">MOF</span><span class="sxs-lookup"><span data-stu-id="ac3fc-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac3fc-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac3fc-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac3fc-152">DLL</span><span class="sxs-lookup"><span data-stu-id="ac3fc-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac3fc-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac3fc-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac3fc-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac3fc-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac3fc-155">\_УНИТАРИКОМПУТЕРСИСТЕМ CIM</span><span class="sxs-lookup"><span data-stu-id="ac3fc-155">CIM\_UnitaryComputerSystem</span></span>](setpowerstate-method-in-class-cim-unitarycomputersystem.md)
</dt> <dt>

[<span data-ttu-id="ac3fc-156">**\_УНИТАРИКОМПУТЕРСИСТЕМ CIM**</span><span class="sxs-lookup"><span data-stu-id="ac3fc-156">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> </dl>

 

 




