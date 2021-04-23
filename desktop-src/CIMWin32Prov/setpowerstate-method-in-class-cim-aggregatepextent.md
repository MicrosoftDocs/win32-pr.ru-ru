---
description: Метод SetPowerState задает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.
ms.assetid: 1a1a8d5e-d685-4b7e-99fb-61fa2e7bdafa
ms.tgt_platform: multiple
title: Метод SetPowerState класса CIM_AggregatePExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePExtent.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 47c97f30da1c8b6f2fe9a6032ef9be9ae87a7d6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990617"
---
# <a name="setpowerstate-method-of-the-cim_aggregatepextent-class"></a><span data-ttu-id="765fa-103">Метод SetPowerState \_ класса CIM аггрегатепекстент</span><span class="sxs-lookup"><span data-stu-id="765fa-103">SetPowerState method of the CIM\_AggregatePExtent class</span></span>

<span data-ttu-id="765fa-104">Метод **SetPowerState** задает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="765fa-104">The **SetPowerState** method sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="765fa-105">В подклассе набор возможных кодов возврата должен быть указан с помощью квалификатора **ValueMap** в методе.</span><span class="sxs-lookup"><span data-stu-id="765fa-105">In a subclass, the set of possible return codes should be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="765fa-106">Строки, в которые преобразуются содержимое **ValueMap** , также должны быть указаны в подклассе как квалификатор массива **Values** .</span><span class="sxs-lookup"><span data-stu-id="765fa-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="765fa-107">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="765fa-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="765fa-108">Дополнительные сведения об использовании этого метода с C/C++ см. в разделе [вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="765fa-108">For more information about using this method with C/C++, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="765fa-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="765fa-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="765fa-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="765fa-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="765fa-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="765fa-111">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="765fa-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="765fa-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="765fa-113">*PowerState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="765fa-113">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="765fa-114">Значение **ValueMap** , указывающее требуемое состояние электропитания для этого логического устройства.</span><span class="sxs-lookup"><span data-stu-id="765fa-114">The **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="765fa-115">1</span><span class="sxs-lookup"><span data-stu-id="765fa-115">1</span></span>
</dt> <dd>

<span data-ttu-id="765fa-116">Полная мощность</span><span class="sxs-lookup"><span data-stu-id="765fa-116">Full power</span></span>

</dd> <dt>

<span data-ttu-id="765fa-117">2</span><span class="sxs-lookup"><span data-stu-id="765fa-117">2</span></span>
</dt> <dd>

<span data-ttu-id="765fa-118">Режим энергосбережения с низким энергопотреблением</span><span class="sxs-lookup"><span data-stu-id="765fa-118">Power-save   low-power mode</span></span>

</dd> <dt>

<span data-ttu-id="765fa-119">3</span><span class="sxs-lookup"><span data-stu-id="765fa-119">3</span></span>
</dt> <dd>

<span data-ttu-id="765fa-120">Power-экономия в режиме ожидания</span><span class="sxs-lookup"><span data-stu-id="765fa-120">Power-save   standby</span></span>

</dd> <dt>

<span data-ttu-id="765fa-121">4</span><span class="sxs-lookup"><span data-stu-id="765fa-121">4</span></span>
</dt> <dd>

<span data-ttu-id="765fa-122">Power-сохранить другие</span><span class="sxs-lookup"><span data-stu-id="765fa-122">Power-save   other</span></span>

</dd> <dt>

<span data-ttu-id="765fa-123">5</span><span class="sxs-lookup"><span data-stu-id="765fa-123">5</span></span>
</dt> <dd>

<span data-ttu-id="765fa-124">Цикл электропитания</span><span class="sxs-lookup"><span data-stu-id="765fa-124">Power cycle</span></span>

</dd> <dt>

<span data-ttu-id="765fa-125">6</span><span class="sxs-lookup"><span data-stu-id="765fa-125">6</span></span>
</dt> <dd>

<span data-ttu-id="765fa-126">Выключение питания</span><span class="sxs-lookup"><span data-stu-id="765fa-126">Power off</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="765fa-127">*Время* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="765fa-127">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="765fa-128">Если необходимо задать состояние электропитания, как обычное значение даты-времени или как значение интервала (где интервал начинается при получении вызова метода).</span><span class="sxs-lookup"><span data-stu-id="765fa-128">When the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="765fa-129">Если параметр *PowerState* равен 5 (Power Cycle), параметр *time* указывает, когда устройство должно снова включить питание.</span><span class="sxs-lookup"><span data-stu-id="765fa-129">When the *PowerState* parameter is equal to 5 (power cycle), the *Time* parameter indicates when the device should power-on again.</span></span> <span data-ttu-id="765fa-130">Выключение осуществляется немедленно.</span><span class="sxs-lookup"><span data-stu-id="765fa-130">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="765fa-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="765fa-131">Return value</span></span>

<span data-ttu-id="765fa-132">Возвращает 0 (нуль) в случае успеха, 1 (один), если *указанный запрос* о сбое и *время* не поддерживаются, и другое значение, если произошла какая-либо другая ошибка.</span><span class="sxs-lookup"><span data-stu-id="765fa-132">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="765fa-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="765fa-133">Remarks</span></span>

<span data-ttu-id="765fa-134">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="765fa-134">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="765fa-135">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="765fa-135">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="765fa-136">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="765fa-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="765fa-137">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="765fa-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="765fa-138">Требования</span><span class="sxs-lookup"><span data-stu-id="765fa-138">Requirements</span></span>



| <span data-ttu-id="765fa-139">Требование</span><span class="sxs-lookup"><span data-stu-id="765fa-139">Requirement</span></span> | <span data-ttu-id="765fa-140">Значение</span><span class="sxs-lookup"><span data-stu-id="765fa-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="765fa-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="765fa-141">Minimum supported client</span></span><br/> | <span data-ttu-id="765fa-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="765fa-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="765fa-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="765fa-143">Minimum supported server</span></span><br/> | <span data-ttu-id="765fa-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="765fa-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="765fa-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="765fa-145">Namespace</span></span><br/>                | <span data-ttu-id="765fa-146">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="765fa-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="765fa-147">MOF</span><span class="sxs-lookup"><span data-stu-id="765fa-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="765fa-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="765fa-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="765fa-149">DLL</span><span class="sxs-lookup"><span data-stu-id="765fa-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="765fa-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="765fa-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="765fa-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="765fa-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="765fa-152">**\_АГГРЕГАТЕПЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="765fa-152">**CIM\_AggregatePExtent**</span></span>](setpowerstate-method-in-class-cim-aggregatepextent.md)
</dt> <dt>

[<span data-ttu-id="765fa-153">**\_АГГРЕГАТЕПЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="765fa-153">**CIM\_AggregatePExtent**</span></span>](cim-aggregatepextent.md)
</dt> </dl>

 

