---
description: Метод SetPowerState класса CIM- \_ класс задает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.
ms.assetid: 0d9678e0-a956-45d3-ac41-5c1604478fd7
ms.tgt_platform: multiple
title: Метод SetPowerState класса CIM_LogicalDevice (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd258a4372c16a7f98f2fe3ea8b84bbfef44f69e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655889"
---
# <a name="setpowerstate-method-of-the-cim_logicaldevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="afff5-103">Метод SetPowerState класса CIM_LogicalDevice (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="afff5-103">SetPowerState method of the CIM_LogicalDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="afff5-104">Метод **SetPowerState** класса CIM- \_ класс задает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="afff5-104">The **SetPowerState** method of the CIM\_LogicalDevice class sets the desired power state for a logical device and when a device should be put into that state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="afff5-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="afff5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="afff5-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="afff5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="afff5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afff5-107">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="afff5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="afff5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afff5-109">*PowerState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="afff5-109">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afff5-110">Значение **ValueMap** , указывающее требуемое состояние питания для этого логического устройства.</span><span class="sxs-lookup"><span data-stu-id="afff5-110">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="afff5-111"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Полная мощность** (1)</span><span class="sxs-lookup"><span data-stu-id="afff5-111"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="afff5-112">Полная мощность.</span><span class="sxs-lookup"><span data-stu-id="afff5-112">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="afff5-113"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (2)</span><span class="sxs-lookup"><span data-stu-id="afff5-113"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="afff5-114">Режим энергосбережения с низким энергопотреблением.</span><span class="sxs-lookup"><span data-stu-id="afff5-114">Power save   low-power mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="afff5-115"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (3)</span><span class="sxs-lookup"><span data-stu-id="afff5-115"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="afff5-116">Энергосбережение в режиме ожидания.</span><span class="sxs-lookup"><span data-stu-id="afff5-116">Power save   standby.</span></span>

</dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="afff5-117"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Энергосбережение — другие** (4)</span><span class="sxs-lookup"><span data-stu-id="afff5-117"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Power Save - Other** (4)</span></span>


</dt> <dd>

<span data-ttu-id="afff5-118">Энергосбережение.</span><span class="sxs-lookup"><span data-stu-id="afff5-118">Power save   other.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="afff5-119"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (5)</span><span class="sxs-lookup"><span data-stu-id="afff5-119"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="afff5-120">Цикл электропитания.</span><span class="sxs-lookup"><span data-stu-id="afff5-120">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="afff5-121"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (6)</span><span class="sxs-lookup"><span data-stu-id="afff5-121"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="afff5-122">Выключение питания.</span><span class="sxs-lookup"><span data-stu-id="afff5-122">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="afff5-123">*Время* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="afff5-123">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afff5-124">Указывает, когда должно быть установлено состояние электропитания: как обычное значение даты-времени или как значение интервала (где интервал начинается при получении вызова метода).</span><span class="sxs-lookup"><span data-stu-id="afff5-124">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="afff5-125">Если параметр *PowerState* равен 5 ("цикл электропитания"), параметр *времени* указывает, когда устройство должно снова включить питание.</span><span class="sxs-lookup"><span data-stu-id="afff5-125">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="afff5-126">Выключение осуществляется немедленно.</span><span class="sxs-lookup"><span data-stu-id="afff5-126">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afff5-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="afff5-127">Return value</span></span>

<span data-ttu-id="afff5-128">Возвращает 0 (нуль) в случае успеха, 1 (один), если *указанный запрос* о сбое и *время* не поддерживаются, и другое значение, если произошла какая-либо другая ошибка.</span><span class="sxs-lookup"><span data-stu-id="afff5-128">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="afff5-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="afff5-129">Remarks</span></span>

<span data-ttu-id="afff5-130">В подклассе набор возможных кодов возврата должен быть указан с помощью квалификатора **ValueMap** в методе.</span><span class="sxs-lookup"><span data-stu-id="afff5-130">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="afff5-131">Строки, в которые преобразуются содержимое **ValueMap** , также должны быть указаны в подклассе как квалификатор массива **Values** .</span><span class="sxs-lookup"><span data-stu-id="afff5-131">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="afff5-132">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="afff5-132">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="afff5-133">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="afff5-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="afff5-134">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="afff5-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="afff5-135">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="afff5-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="afff5-136">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="afff5-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="afff5-137">Требования</span><span class="sxs-lookup"><span data-stu-id="afff5-137">Requirements</span></span>



| <span data-ttu-id="afff5-138">Требование</span><span class="sxs-lookup"><span data-stu-id="afff5-138">Requirement</span></span> | <span data-ttu-id="afff5-139">Значение</span><span class="sxs-lookup"><span data-stu-id="afff5-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afff5-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="afff5-140">Minimum supported client</span></span><br/> | <span data-ttu-id="afff5-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="afff5-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="afff5-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="afff5-142">Minimum supported server</span></span><br/> | <span data-ttu-id="afff5-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afff5-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="afff5-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="afff5-144">Namespace</span></span><br/>                | <span data-ttu-id="afff5-145">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="afff5-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="afff5-146">MOF</span><span class="sxs-lookup"><span data-stu-id="afff5-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afff5-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="afff5-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="afff5-148">DLL</span><span class="sxs-lookup"><span data-stu-id="afff5-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afff5-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afff5-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afff5-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="afff5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afff5-151">Модель \_ CIM</span><span class="sxs-lookup"><span data-stu-id="afff5-151">CIM\_LogicalDevice</span></span>](setpowerstate-method-in-class-cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="afff5-152">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="afff5-152">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




