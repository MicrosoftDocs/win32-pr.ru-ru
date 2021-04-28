---
description: Метод SetPowerState класса CIM_AlarmDevice. Метод SetPowerState задает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.
ms.assetid: 3194c363-4db7-4928-b47a-7e9c8a5339d7
ms.tgt_platform: multiple
title: Метод SetPowerState класса CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 45fcc3383e40fffa01b0c74971375d869c6eb038
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089522"
---
# <a name="setpowerstate-method-of-the-cim_alarmdevice-class"></a><span data-ttu-id="9f2fa-103">Метод SetPowerState \_ класса CIM алармдевице</span><span class="sxs-lookup"><span data-stu-id="9f2fa-103">SetPowerState method of the CIM\_AlarmDevice class</span></span>

<span data-ttu-id="9f2fa-104">Метод **SetPowerState** задает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-104">The **SetPowerState** method sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="9f2fa-105">В подклассе набор возможных кодов возврата должен быть указан с помощью квалификатора **ValueMap** в методе.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="9f2fa-106">Строки, в которые преобразуются содержимое **ValueMap** , также должны быть указаны в подклассе как квалификатор массива **Values** .</span><span class="sxs-lookup"><span data-stu-id="9f2fa-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="9f2fa-107">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f2fa-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9f2fa-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9f2fa-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9f2fa-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f2fa-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="9f2fa-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f2fa-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f2fa-112">*PowerState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f2fa-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2fa-113">Значение **ValueMap** , указывающее требуемое состояние электропитания для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-113">A **ValueMap** value that specifies the desired power state for the logical device.</span></span>

<dt>

<span data-ttu-id="9f2fa-114">1</span><span class="sxs-lookup"><span data-stu-id="9f2fa-114">1</span></span>
</dt> <dd>

<span data-ttu-id="9f2fa-115">Полная мощность.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="9f2fa-116">2</span><span class="sxs-lookup"><span data-stu-id="9f2fa-116">2</span></span>
</dt> <dd>

<span data-ttu-id="9f2fa-117">Режим энергосбережения с низким энергопотреблением.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="9f2fa-118">3</span><span class="sxs-lookup"><span data-stu-id="9f2fa-118">3</span></span>
</dt> <dd>

<span data-ttu-id="9f2fa-119">Энергосбережение в режиме ожидания.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="9f2fa-120">4</span><span class="sxs-lookup"><span data-stu-id="9f2fa-120">4</span></span>
</dt> <dd>

<span data-ttu-id="9f2fa-121">Энергосбережение.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="9f2fa-122">5</span><span class="sxs-lookup"><span data-stu-id="9f2fa-122">5</span></span>
</dt> <dd>

<span data-ttu-id="9f2fa-123">Цикл электропитания.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="9f2fa-124">6</span><span class="sxs-lookup"><span data-stu-id="9f2fa-124">6</span></span>
</dt> <dd>

<span data-ttu-id="9f2fa-125">Выключение питания.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9f2fa-126">*Время* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f2fa-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2fa-127">Указывает, когда должно быть установлено состояние электропитания: как обычное значение даты-времени или как значение интервала (где интервал начинается при получении вызова метода).</span><span class="sxs-lookup"><span data-stu-id="9f2fa-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="9f2fa-128">Если параметр *PowerState* равен 5 (Power Cycle), параметр *time* указывает, когда устройство должно снова включить питание.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-128">When the *PowerState* parameter is equal to 5 (power cycle), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="9f2fa-129">Выключение осуществляется немедленно.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-129">Power off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f2fa-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f2fa-130">Return value</span></span>

<span data-ttu-id="9f2fa-131">Возвращает 0 (нуль) в случае успеха, 1 (один), если *указанный запрос* о сбое и *время* не поддерживаются, и другое значение, если произошла какая-либо другая ошибка.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f2fa-132">Remarks</span><span class="sxs-lookup"><span data-stu-id="9f2fa-132">Remarks</span></span>

<span data-ttu-id="9f2fa-133">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="9f2fa-134">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="9f2fa-135">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9f2fa-136">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="9f2fa-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f2fa-137">Требования</span><span class="sxs-lookup"><span data-stu-id="9f2fa-137">Requirements</span></span>



| <span data-ttu-id="9f2fa-138">Требование</span><span class="sxs-lookup"><span data-stu-id="9f2fa-138">Requirement</span></span> | <span data-ttu-id="9f2fa-139">Значение</span><span class="sxs-lookup"><span data-stu-id="9f2fa-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f2fa-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f2fa-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9f2fa-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f2fa-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f2fa-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f2fa-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9f2fa-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f2fa-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f2fa-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9f2fa-144">Namespace</span></span><br/>                | <span data-ttu-id="9f2fa-145">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9f2fa-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9f2fa-146">MOF</span><span class="sxs-lookup"><span data-stu-id="9f2fa-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f2fa-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f2fa-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f2fa-148">DLL</span><span class="sxs-lookup"><span data-stu-id="9f2fa-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f2fa-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f2fa-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f2fa-150">См. также</span><span class="sxs-lookup"><span data-stu-id="9f2fa-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f2fa-151">\_АЛАРМДЕВИЦЕ CIM</span><span class="sxs-lookup"><span data-stu-id="9f2fa-151">CIM\_AlarmDevice</span></span>](setpowerstate-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[<span data-ttu-id="9f2fa-152">**\_АЛАРМДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="9f2fa-152">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> </dl>

 

 




