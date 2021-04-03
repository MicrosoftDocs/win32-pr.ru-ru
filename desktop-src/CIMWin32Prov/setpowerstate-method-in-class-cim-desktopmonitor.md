---
description: Метод SetPowerState задает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.
ms.assetid: 9a8be1bb-f5ca-4b82-bea1-30090c7e2569
ms.tgt_platform: multiple
title: Метод SetPowerState класса CIM_DesktopMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DesktopMonitor.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 107a4a8df69cb5e5e9e4cf781f52d88ff37e3fba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896097"
---
# <a name="setpowerstate-method-of-the-cim_desktopmonitor-class"></a><span data-ttu-id="02c38-103">Метод SetPowerState \_ класса CIM десктопмонитор</span><span class="sxs-lookup"><span data-stu-id="02c38-103">SetPowerState method of the CIM\_DesktopMonitor class</span></span>

<span data-ttu-id="02c38-104">Метод **SetPowerState** задает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="02c38-104">The **SetPowerState** method sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="02c38-105">В подклассе набор возможных кодов возврата должен быть указан с помощью квалификатора **ValueMap** в методе.</span><span class="sxs-lookup"><span data-stu-id="02c38-105">In a subclass, the set of possible return codes should be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="02c38-106">Строки, в которые преобразуются содержимое **ValueMap** , также должны быть указаны в подклассе как квалификатор массива **Values** .</span><span class="sxs-lookup"><span data-stu-id="02c38-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="02c38-107">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="02c38-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02c38-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="02c38-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="02c38-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="02c38-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="02c38-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02c38-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="02c38-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="02c38-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02c38-112">*PowerState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="02c38-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02c38-113">Значение **ValueMap** , указывающее требуемое состояние питания для этого логического устройства.</span><span class="sxs-lookup"><span data-stu-id="02c38-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="02c38-114">1</span><span class="sxs-lookup"><span data-stu-id="02c38-114">1</span></span>
</dt> <dd>

<span data-ttu-id="02c38-115">Полная мощность.</span><span class="sxs-lookup"><span data-stu-id="02c38-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="02c38-116">2</span><span class="sxs-lookup"><span data-stu-id="02c38-116">2</span></span>
</dt> <dd>

<span data-ttu-id="02c38-117">Режим энергосбережения с низким энергопотреблением.</span><span class="sxs-lookup"><span data-stu-id="02c38-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="02c38-118">3</span><span class="sxs-lookup"><span data-stu-id="02c38-118">3</span></span>
</dt> <dd>

<span data-ttu-id="02c38-119">Энергосбережение в режиме ожидания.</span><span class="sxs-lookup"><span data-stu-id="02c38-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="02c38-120">4</span><span class="sxs-lookup"><span data-stu-id="02c38-120">4</span></span>
</dt> <dd>

<span data-ttu-id="02c38-121">Энергосбережение.</span><span class="sxs-lookup"><span data-stu-id="02c38-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="02c38-122">5</span><span class="sxs-lookup"><span data-stu-id="02c38-122">5</span></span>
</dt> <dd>

<span data-ttu-id="02c38-123">Цикл электропитания.</span><span class="sxs-lookup"><span data-stu-id="02c38-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="02c38-124">6</span><span class="sxs-lookup"><span data-stu-id="02c38-124">6</span></span>
</dt> <dd>

<span data-ttu-id="02c38-125">Выключение питания.</span><span class="sxs-lookup"><span data-stu-id="02c38-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="02c38-126">*Время* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="02c38-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02c38-127">Указывает, когда должно быть установлено состояние электропитания: как обычное значение даты-времени или как значение интервала (где интервал начинается при получении вызова метода).</span><span class="sxs-lookup"><span data-stu-id="02c38-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="02c38-128">Если параметр *PowerState* равен 5 ("цикл электропитания"), параметр *времени* указывает, когда устройство должно снова включить питание.</span><span class="sxs-lookup"><span data-stu-id="02c38-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power-on again.</span></span> <span data-ttu-id="02c38-129">Выключение осуществляется немедленно.</span><span class="sxs-lookup"><span data-stu-id="02c38-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02c38-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02c38-130">Return value</span></span>

<span data-ttu-id="02c38-131">Возвращает 0 (нуль) в случае успеха, 1 (один), если *указанный запрос* о сбое и *время* не поддерживаются, и другое значение, если произошла какая-либо другая ошибка.</span><span class="sxs-lookup"><span data-stu-id="02c38-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="02c38-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02c38-132">Remarks</span></span>

<span data-ttu-id="02c38-133">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="02c38-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="02c38-134">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="02c38-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="02c38-135">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="02c38-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="02c38-136">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="02c38-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="02c38-137">Требования</span><span class="sxs-lookup"><span data-stu-id="02c38-137">Requirements</span></span>



| <span data-ttu-id="02c38-138">Требование</span><span class="sxs-lookup"><span data-stu-id="02c38-138">Requirement</span></span> | <span data-ttu-id="02c38-139">Значение</span><span class="sxs-lookup"><span data-stu-id="02c38-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02c38-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02c38-140">Minimum supported client</span></span><br/> | <span data-ttu-id="02c38-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02c38-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02c38-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02c38-142">Minimum supported server</span></span><br/> | <span data-ttu-id="02c38-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02c38-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02c38-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="02c38-144">Namespace</span></span><br/>                | <span data-ttu-id="02c38-145">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="02c38-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="02c38-146">MOF</span><span class="sxs-lookup"><span data-stu-id="02c38-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02c38-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02c38-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="02c38-148">DLL</span><span class="sxs-lookup"><span data-stu-id="02c38-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02c38-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02c38-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02c38-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02c38-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02c38-151">\_ДЕСКТОПМОНИТОР CIM</span><span class="sxs-lookup"><span data-stu-id="02c38-151">CIM\_DesktopMonitor</span></span>](setpowerstate-method-in-class-cim-desktopmonitor.md)
</dt> <dt>

[<span data-ttu-id="02c38-152">**\_ДЕСКТОПМОНИТОР CIM**</span><span class="sxs-lookup"><span data-stu-id="02c38-152">**CIM\_DesktopMonitor**</span></span>](cim-desktopmonitor.md)
</dt> </dl>

 

 




