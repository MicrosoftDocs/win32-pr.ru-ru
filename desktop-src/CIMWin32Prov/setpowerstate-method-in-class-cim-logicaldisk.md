---
description: Метод SetPowerState \_ класса CIM Logical устанавливает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.
ms.assetid: bb363434-2fb5-422e-aea7-5c7de1364b88
ms.tgt_platform: multiple
title: Метод SetPowerState класса CIM_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f97649a00f5e00e9fa098baeb2e6056080f41401
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142562"
---
# <a name="setpowerstate-method-of-the-cim_logicaldisk-class"></a><span data-ttu-id="d9bc4-103">Метод SetPowerState \_ класса CIM LogicalDisk</span><span class="sxs-lookup"><span data-stu-id="d9bc4-103">SetPowerState method of the CIM\_LogicalDisk class</span></span>

<span data-ttu-id="d9bc4-104">Метод **SetPowerState** \_ класса CIM Logical устанавливает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-104">The **SetPowerState** method of the CIM\_LogicalDisk class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="d9bc4-105">В подклассе набор возможных кодов возврата должен быть указан с помощью квалификатора **ValueMap** в методе.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="d9bc4-106">Строки, в которые преобразуются содержимое **ValueMap** , также должны быть указаны в подклассе как квалификатор массива **Values** .</span><span class="sxs-lookup"><span data-stu-id="d9bc4-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="d9bc4-107">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9bc4-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d9bc4-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d9bc4-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d9bc4-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9bc4-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="d9bc4-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9bc4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9bc4-112">*PowerState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9bc4-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9bc4-113">Значение **ValueMap** , указывающее требуемое состояние питания для этого логического устройства.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="d9bc4-114">1</span><span class="sxs-lookup"><span data-stu-id="d9bc4-114">1</span></span>
</dt> <dd>

<span data-ttu-id="d9bc4-115">Полная мощность.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="d9bc4-116">2</span><span class="sxs-lookup"><span data-stu-id="d9bc4-116">2</span></span>
</dt> <dd>

<span data-ttu-id="d9bc4-117">Режим энергосбережения с низким энергопотреблением.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="d9bc4-118">3</span><span class="sxs-lookup"><span data-stu-id="d9bc4-118">3</span></span>
</dt> <dd>

<span data-ttu-id="d9bc4-119">Энергосбережение в режиме ожидания.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="d9bc4-120">4</span><span class="sxs-lookup"><span data-stu-id="d9bc4-120">4</span></span>
</dt> <dd>

<span data-ttu-id="d9bc4-121">Энергосбережение.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="d9bc4-122">5</span><span class="sxs-lookup"><span data-stu-id="d9bc4-122">5</span></span>
</dt> <dd>

<span data-ttu-id="d9bc4-123">Цикл электропитания.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="d9bc4-124">6</span><span class="sxs-lookup"><span data-stu-id="d9bc4-124">6</span></span>
</dt> <dd>

<span data-ttu-id="d9bc4-125">Выключение питания.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d9bc4-126">*Время* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9bc4-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9bc4-127">Указывает, когда должно быть установлено состояние электропитания: как обычное значение даты-времени или как значение интервала (где интервал начинается при получении вызова метода).</span><span class="sxs-lookup"><span data-stu-id="d9bc4-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="d9bc4-128">Если параметр *PowerState* равен 5 ("цикл электропитания"), параметр *времени* указывает, когда устройство должно снова включить питание.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="d9bc4-129">Выключение осуществляется немедленно.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9bc4-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9bc4-130">Return value</span></span>

<span data-ttu-id="d9bc4-131">Возвращает 0 (нуль) в случае успеха, 1 (один), если *указанный запрос* о сбое и *время* не поддерживаются, и другое значение, если произошла какая-либо другая ошибка.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9bc4-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9bc4-132">Remarks</span></span>

<span data-ttu-id="d9bc4-133">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d9bc4-134">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d9bc4-135">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d9bc4-136">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d9bc4-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9bc4-137">Требования</span><span class="sxs-lookup"><span data-stu-id="d9bc4-137">Requirements</span></span>



| <span data-ttu-id="d9bc4-138">Требование</span><span class="sxs-lookup"><span data-stu-id="d9bc4-138">Requirement</span></span> | <span data-ttu-id="d9bc4-139">Значение</span><span class="sxs-lookup"><span data-stu-id="d9bc4-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9bc4-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9bc4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d9bc4-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9bc4-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d9bc4-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9bc4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d9bc4-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9bc4-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d9bc4-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d9bc4-144">Namespace</span></span><br/>                | <span data-ttu-id="d9bc4-145">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d9bc4-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d9bc4-146">MOF</span><span class="sxs-lookup"><span data-stu-id="d9bc4-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9bc4-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9bc4-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9bc4-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d9bc4-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9bc4-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9bc4-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9bc4-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9bc4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9bc4-151">Логический диск CIM \_</span><span class="sxs-lookup"><span data-stu-id="d9bc4-151">CIM\_LogicalDisk</span></span>](setpowerstate-method-in-class-cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="d9bc4-152">**Логический диск CIM \_**</span><span class="sxs-lookup"><span data-stu-id="d9bc4-152">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> </dl>

 

 




