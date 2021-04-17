---
description: Задает требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.
ms.assetid: 7b36a987-d4c9-4cdc-8703-cf3f713e0c4a
ms.tgt_platform: multiple
title: Метод SetPowerState класса Win32_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskPartition.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e42be975b7764039bec603928ef5a27bc38997b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655989"
---
# <a name="setpowerstate-method-of-the-win32_diskpartition-class"></a><span data-ttu-id="7b30c-103">Метод SetPowerState \_ класса Win32 дискпартитион</span><span class="sxs-lookup"><span data-stu-id="7b30c-103">SetPowerState method of the Win32\_DiskPartition class</span></span>

<span data-ttu-id="7b30c-104">Задает требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="7b30c-104">Sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="7b30c-105">В подклассе набор возможных кодов возврата должен быть указан с помощью квалификатора **ValueMap** в методе.</span><span class="sxs-lookup"><span data-stu-id="7b30c-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="7b30c-106">Строки, в которые преобразуются содержимое **ValueMap** , также должны быть указаны в подклассе как квалификатор массива **Values** .</span><span class="sxs-lookup"><span data-stu-id="7b30c-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b30c-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="7b30c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7b30c-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7b30c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7b30c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b30c-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="7b30c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b30c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b30c-111">*PowerState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b30c-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b30c-112">Значение **ValueMap** , указывающее требуемое состояние питания для этого логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7b30c-112">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="7b30c-113">1</span><span class="sxs-lookup"><span data-stu-id="7b30c-113">1</span></span>
</dt> <dd>

<span data-ttu-id="7b30c-114">Полная мощность.</span><span class="sxs-lookup"><span data-stu-id="7b30c-114">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="7b30c-115">2</span><span class="sxs-lookup"><span data-stu-id="7b30c-115">2</span></span>
</dt> <dd>

<span data-ttu-id="7b30c-116">Режим энергосбережения с низким энергопотреблением.</span><span class="sxs-lookup"><span data-stu-id="7b30c-116">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="7b30c-117">3</span><span class="sxs-lookup"><span data-stu-id="7b30c-117">3</span></span>
</dt> <dd>

<span data-ttu-id="7b30c-118">Энергосбережение в режиме ожидания.</span><span class="sxs-lookup"><span data-stu-id="7b30c-118">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="7b30c-119">4</span><span class="sxs-lookup"><span data-stu-id="7b30c-119">4</span></span>
</dt> <dd>

<span data-ttu-id="7b30c-120">Энергосбережение.</span><span class="sxs-lookup"><span data-stu-id="7b30c-120">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="7b30c-121">5</span><span class="sxs-lookup"><span data-stu-id="7b30c-121">5</span></span>
</dt> <dd>

<span data-ttu-id="7b30c-122">Цикл электропитания.</span><span class="sxs-lookup"><span data-stu-id="7b30c-122">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="7b30c-123">6</span><span class="sxs-lookup"><span data-stu-id="7b30c-123">6</span></span>
</dt> <dd>

<span data-ttu-id="7b30c-124">Выключение питания.</span><span class="sxs-lookup"><span data-stu-id="7b30c-124">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7b30c-125">*Время* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b30c-125">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b30c-126">Указывает, когда должно быть установлено состояние электропитания: как обычное значение даты-времени или как значение интервала (где интервал начинается при получении вызова метода).</span><span class="sxs-lookup"><span data-stu-id="7b30c-126">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="7b30c-127">Если параметр *PowerState* равен 5 ("цикл электропитания"), параметр *времени* указывает, когда устройство должно снова включить питание.</span><span class="sxs-lookup"><span data-stu-id="7b30c-127">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="7b30c-128">Выключение осуществляется немедленно.</span><span class="sxs-lookup"><span data-stu-id="7b30c-128">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b30c-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b30c-129">Return value</span></span>

<span data-ttu-id="7b30c-130">Возвращает 0 (нуль) в случае успеха, 1 (один), если *указанный запрос* о сбое и *время* не поддерживаются, и другое значение, если произошла какая-либо другая ошибка.</span><span class="sxs-lookup"><span data-stu-id="7b30c-130">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b30c-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b30c-131">Remarks</span></span>

<span data-ttu-id="7b30c-132">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="7b30c-132">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="7b30c-133">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="7b30c-133">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="7b30c-134">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="7b30c-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7b30c-135">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="7b30c-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b30c-136">Требования</span><span class="sxs-lookup"><span data-stu-id="7b30c-136">Requirements</span></span>



| <span data-ttu-id="7b30c-137">Требование</span><span class="sxs-lookup"><span data-stu-id="7b30c-137">Requirement</span></span> | <span data-ttu-id="7b30c-138">Значение</span><span class="sxs-lookup"><span data-stu-id="7b30c-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b30c-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b30c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7b30c-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b30c-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7b30c-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b30c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7b30c-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b30c-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7b30c-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7b30c-143">Namespace</span></span><br/>                | <span data-ttu-id="7b30c-144">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7b30c-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7b30c-145">MOF</span><span class="sxs-lookup"><span data-stu-id="7b30c-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b30c-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b30c-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b30c-147">DLL</span><span class="sxs-lookup"><span data-stu-id="7b30c-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b30c-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b30c-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b30c-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b30c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b30c-150">**\_ДИСКПАРТИТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="7b30c-150">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dt>

[<span data-ttu-id="7b30c-151">**\_Дискпартитион Win32**</span><span class="sxs-lookup"><span data-stu-id="7b30c-151">**Win32\_DiskPartition**</span></span>](win32-diskpartition.md)
</dt> </dl>

 

 




