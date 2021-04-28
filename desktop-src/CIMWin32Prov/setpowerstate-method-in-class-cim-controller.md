---
description: Метод SetPowerState класса CIM_Controller. Метод SetPowerState задает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.
ms.assetid: 442c6c2c-8e9a-476c-bb57-8b1a6439e97f
ms.tgt_platform: multiple
title: Метод SetPowerState класса CIM_Controller
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Controller.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7713d892643238233e9ac5469c942fdf16609512
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086232"
---
# <a name="setpowerstate-method-of-the-cim_controller-class"></a><span data-ttu-id="061f3-103">Метод SetPowerState \_ класса контроллера CIM</span><span class="sxs-lookup"><span data-stu-id="061f3-103">SetPowerState method of the CIM\_Controller class</span></span>

<span data-ttu-id="061f3-104">Метод **SetPowerState** задает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="061f3-104">The **SetPowerState** method sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="061f3-105">В подклассе набор возможных кодов возврата должен быть указан с помощью квалификатора **ValueMap** в методе.</span><span class="sxs-lookup"><span data-stu-id="061f3-105">In a subclass, the set of possible return codes should be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="061f3-106">Строки, в которые преобразуются содержимое **ValueMap** , также должны быть указаны в подклассе как квалификатор массива **Values** .</span><span class="sxs-lookup"><span data-stu-id="061f3-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="061f3-107">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="061f3-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="061f3-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="061f3-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="061f3-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="061f3-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="061f3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="061f3-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="061f3-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="061f3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="061f3-112">*PowerState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="061f3-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="061f3-113">Значение **ValueMap** , указывающее требуемое состояние электропитания для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="061f3-113">A **ValueMap** value that specifies the desired power state for the logical device.</span></span>

<dt>

<span data-ttu-id="061f3-114">1</span><span class="sxs-lookup"><span data-stu-id="061f3-114">1</span></span>
</dt> <dd>

<span data-ttu-id="061f3-115">Полная мощность.</span><span class="sxs-lookup"><span data-stu-id="061f3-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="061f3-116">2</span><span class="sxs-lookup"><span data-stu-id="061f3-116">2</span></span>
</dt> <dd>

<span data-ttu-id="061f3-117">Режим энергосбережения с низким энергопотреблением.</span><span class="sxs-lookup"><span data-stu-id="061f3-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="061f3-118">3</span><span class="sxs-lookup"><span data-stu-id="061f3-118">3</span></span>
</dt> <dd>

<span data-ttu-id="061f3-119">Энергосбережение в режиме ожидания.</span><span class="sxs-lookup"><span data-stu-id="061f3-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="061f3-120">4</span><span class="sxs-lookup"><span data-stu-id="061f3-120">4</span></span>
</dt> <dd>

<span data-ttu-id="061f3-121">Энергосбережение.</span><span class="sxs-lookup"><span data-stu-id="061f3-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="061f3-122">5</span><span class="sxs-lookup"><span data-stu-id="061f3-122">5</span></span>
</dt> <dd>

<span data-ttu-id="061f3-123">Цикл электропитания.</span><span class="sxs-lookup"><span data-stu-id="061f3-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="061f3-124">6</span><span class="sxs-lookup"><span data-stu-id="061f3-124">6</span></span>
</dt> <dd>

<span data-ttu-id="061f3-125">Выключение питания.</span><span class="sxs-lookup"><span data-stu-id="061f3-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="061f3-126">*Время* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="061f3-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="061f3-127">Указывает, когда должно быть установлено состояние электропитания: как обычное значение даты-времени или как значение интервала (где интервал начинается при получении вызова метода).</span><span class="sxs-lookup"><span data-stu-id="061f3-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="061f3-128">Если параметр *PowerState* равен 5 ("цикл электропитания"), параметр *времени* указывает, когда устройство должно снова включить питание.</span><span class="sxs-lookup"><span data-stu-id="061f3-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="061f3-129">Выключение осуществляется немедленно.</span><span class="sxs-lookup"><span data-stu-id="061f3-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="061f3-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="061f3-130">Return value</span></span>

<span data-ttu-id="061f3-131">Возвращает 0 (нуль) в случае успеха, 1 (один), если *указанный запрос* о сбое и *время* не поддерживаются, и другое значение, если произошла какая-либо другая ошибка.</span><span class="sxs-lookup"><span data-stu-id="061f3-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="061f3-132">Remarks</span><span class="sxs-lookup"><span data-stu-id="061f3-132">Remarks</span></span>

<span data-ttu-id="061f3-133">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="061f3-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="061f3-134">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="061f3-134">To use this method, you must implement it in your own provider.</span></span> <span data-ttu-id="061f3-135">Дополнительные сведения см. в разделе [Создание поставщиков WMI](/windows/desktop/WmiSdk/creating-wmi-providers).</span><span class="sxs-lookup"><span data-stu-id="061f3-135">For more information, see [Creating WMI Providers](/windows/desktop/WmiSdk/creating-wmi-providers).</span></span>

<span data-ttu-id="061f3-136">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="061f3-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="061f3-137">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="061f3-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="061f3-138">Требования</span><span class="sxs-lookup"><span data-stu-id="061f3-138">Requirements</span></span>



| <span data-ttu-id="061f3-139">Требование</span><span class="sxs-lookup"><span data-stu-id="061f3-139">Requirement</span></span> | <span data-ttu-id="061f3-140">Значение</span><span class="sxs-lookup"><span data-stu-id="061f3-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="061f3-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="061f3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="061f3-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="061f3-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="061f3-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="061f3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="061f3-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="061f3-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="061f3-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="061f3-145">Namespace</span></span><br/>                | <span data-ttu-id="061f3-146">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="061f3-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="061f3-147">MOF</span><span class="sxs-lookup"><span data-stu-id="061f3-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="061f3-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="061f3-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="061f3-149">DLL</span><span class="sxs-lookup"><span data-stu-id="061f3-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="061f3-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="061f3-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="061f3-151">См. также</span><span class="sxs-lookup"><span data-stu-id="061f3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="061f3-152">\_Контроллер CIM</span><span class="sxs-lookup"><span data-stu-id="061f3-152">CIM\_Controller</span></span>](setpowerstate-method-in-class-cim-controller.md)
</dt> <dt>

[<span data-ttu-id="061f3-153">**\_Контроллер CIM**</span><span class="sxs-lookup"><span data-stu-id="061f3-153">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

