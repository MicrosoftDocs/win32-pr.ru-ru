---
description: Метод SetPowerState \_ класса CIM TapeDrive устанавливает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.
ms.assetid: 73f98d08-49da-4b21-91c4-cbe420c648e4
ms.tgt_platform: multiple
title: Метод SetPowerState класса CIM_TapeDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a6efcfe08dfddca3477081f65fac35780f713005
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539266"
---
# <a name="setpowerstate-method-of-the-cim_tapedrive-class"></a><span data-ttu-id="01cd2-103">Метод SetPowerState \_ класса CIM TapeDrive</span><span class="sxs-lookup"><span data-stu-id="01cd2-103">SetPowerState method of the CIM\_TapeDrive class</span></span>

<span data-ttu-id="01cd2-104">Метод **SetPowerState** \_ класса CIM TapeDrive устанавливает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="01cd2-104">The **SetPowerState** method of the CIM\_TapeDrive class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="01cd2-105">В подклассе набор возможных кодов возврата должен быть указан с помощью квалификатора **ValueMap** в методе.</span><span class="sxs-lookup"><span data-stu-id="01cd2-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="01cd2-106">Строки, в которые преобразуются содержимое **ValueMap** , также должны быть указаны в подклассе как квалификатор массива **Values** .</span><span class="sxs-lookup"><span data-stu-id="01cd2-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="01cd2-107">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="01cd2-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="01cd2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01cd2-108">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="01cd2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="01cd2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01cd2-110">*PowerState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01cd2-110">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01cd2-111">Значение **ValueMap** , указывающее требуемое состояние питания для этого логического устройства.</span><span class="sxs-lookup"><span data-stu-id="01cd2-111">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="01cd2-112">1</span><span class="sxs-lookup"><span data-stu-id="01cd2-112">1</span></span>
</dt> <dd>

<span data-ttu-id="01cd2-113">Полная мощность.</span><span class="sxs-lookup"><span data-stu-id="01cd2-113">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="01cd2-114">2</span><span class="sxs-lookup"><span data-stu-id="01cd2-114">2</span></span>
</dt> <dd>

<span data-ttu-id="01cd2-115">Режим энергосбережения с низким энергопотреблением.</span><span class="sxs-lookup"><span data-stu-id="01cd2-115">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="01cd2-116">3</span><span class="sxs-lookup"><span data-stu-id="01cd2-116">3</span></span>
</dt> <dd>

<span data-ttu-id="01cd2-117">Энергосбережение в режиме ожидания.</span><span class="sxs-lookup"><span data-stu-id="01cd2-117">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="01cd2-118">4</span><span class="sxs-lookup"><span data-stu-id="01cd2-118">4</span></span>
</dt> <dd>

<span data-ttu-id="01cd2-119">Энергосбережение.</span><span class="sxs-lookup"><span data-stu-id="01cd2-119">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="01cd2-120">5</span><span class="sxs-lookup"><span data-stu-id="01cd2-120">5</span></span>
</dt> <dd>

<span data-ttu-id="01cd2-121">Цикл электропитания.</span><span class="sxs-lookup"><span data-stu-id="01cd2-121">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="01cd2-122">6</span><span class="sxs-lookup"><span data-stu-id="01cd2-122">6</span></span>
</dt> <dd>

<span data-ttu-id="01cd2-123">Выключение питания.</span><span class="sxs-lookup"><span data-stu-id="01cd2-123">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="01cd2-124">*Время* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01cd2-124">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01cd2-125">Указывает, когда должно быть установлено состояние электропитания: как обычное значение даты-времени или как значение интервала (где интервал начинается при получении вызова метода).</span><span class="sxs-lookup"><span data-stu-id="01cd2-125">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="01cd2-126">Если параметр *PowerState* равен 5 ("цикл электропитания"), параметр *времени* указывает, когда устройство должно снова включить питание.</span><span class="sxs-lookup"><span data-stu-id="01cd2-126">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="01cd2-127">Выключение осуществляется немедленно.</span><span class="sxs-lookup"><span data-stu-id="01cd2-127">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01cd2-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01cd2-128">Return value</span></span>

<span data-ttu-id="01cd2-129">Возвращает 0 (нуль) в случае успеха, 1 (один), если *указанный запрос* о сбое и *время* не поддерживаются, и другое значение, если произошла какая-либо другая ошибка.</span><span class="sxs-lookup"><span data-stu-id="01cd2-129">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="01cd2-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01cd2-130">Remarks</span></span>

<span data-ttu-id="01cd2-131">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="01cd2-131">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="01cd2-132">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="01cd2-132">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="01cd2-133">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="01cd2-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="01cd2-134">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="01cd2-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="01cd2-135">Требования</span><span class="sxs-lookup"><span data-stu-id="01cd2-135">Requirements</span></span>



| <span data-ttu-id="01cd2-136">Требование</span><span class="sxs-lookup"><span data-stu-id="01cd2-136">Requirement</span></span> | <span data-ttu-id="01cd2-137">Значение</span><span class="sxs-lookup"><span data-stu-id="01cd2-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01cd2-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01cd2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="01cd2-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01cd2-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01cd2-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01cd2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="01cd2-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01cd2-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01cd2-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="01cd2-142">Namespace</span></span><br/>                | <span data-ttu-id="01cd2-143">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="01cd2-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01cd2-144">MOF</span><span class="sxs-lookup"><span data-stu-id="01cd2-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01cd2-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01cd2-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01cd2-146">DLL</span><span class="sxs-lookup"><span data-stu-id="01cd2-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01cd2-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01cd2-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01cd2-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01cd2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01cd2-149">\_TAPEDRIVE CIM</span><span class="sxs-lookup"><span data-stu-id="01cd2-149">CIM\_TapeDrive</span></span>](setpowerstate-method-in-class-cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="01cd2-150">**\_TAPEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="01cd2-150">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> </dl>

 

 




