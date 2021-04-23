---
description: Метод Сетурженци задает требуемый уровень срочности сигнала.
ms.assetid: ac2e7fda-1317-440a-adbd-1ef0844d124c
ms.tgt_platform: multiple
title: Метод Сетурженци класса CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.SetUrgency
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35918677e210ac2fe7ac4798a04db9dc628f5fa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990571"
---
# <a name="seturgency-method-of-the-cim_alarmdevice-class"></a><span data-ttu-id="39e57-103">Метод Сетурженци \_ класса CIM алармдевице</span><span class="sxs-lookup"><span data-stu-id="39e57-103">SetUrgency method of the CIM\_AlarmDevice class</span></span>

<span data-ttu-id="39e57-104">Метод **сетурженци** задает требуемый уровень срочности сигнала.</span><span class="sxs-lookup"><span data-stu-id="39e57-104">The **SetUrgency** method sets the desired urgency level for an alarm.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39e57-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="39e57-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="39e57-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="39e57-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="39e57-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="39e57-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="39e57-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="39e57-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="39e57-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39e57-109">Syntax</span></span>


```mof
uint32 SetUrgency(
  [in] uint16 RequestedUrgency
);
```



## <a name="parameters"></a><span data-ttu-id="39e57-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="39e57-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39e57-111">*Рекуестедурженци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39e57-111">*RequestedUrgency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e57-112">Относительная частота, с которой будильник мигает, вибратес или выдает звуковые сигналы.</span><span class="sxs-lookup"><span data-stu-id="39e57-112">Relative frequency at which the alarm flashes, vibrates, or emits audible tones.</span></span> <span data-ttu-id="39e57-113">Следующие значения относятся к свойству **срочности** в [**CIM \_ алармдевице**](cim-alarmdevice.md).</span><span class="sxs-lookup"><span data-stu-id="39e57-113">The following values are from the **Urgency** property in [**CIM\_AlarmDevice**](cim-alarmdevice.md).</span></span>

<dt>

<span data-ttu-id="39e57-114">0</span><span class="sxs-lookup"><span data-stu-id="39e57-114">0</span></span>
</dt> <dd>

<span data-ttu-id="39e57-115">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="39e57-115">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="39e57-116">1</span><span class="sxs-lookup"><span data-stu-id="39e57-116">1</span></span>
</dt> <dd>

<span data-ttu-id="39e57-117">Другое</span><span class="sxs-lookup"><span data-stu-id="39e57-117">Other.</span></span>

</dd> <dt>

<span data-ttu-id="39e57-118">2</span><span class="sxs-lookup"><span data-stu-id="39e57-118">2</span></span>
</dt> <dd>

<span data-ttu-id="39e57-119">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="39e57-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="39e57-120">3</span><span class="sxs-lookup"><span data-stu-id="39e57-120">3</span></span>
</dt> <dd>

<span data-ttu-id="39e57-121">Извещен.</span><span class="sxs-lookup"><span data-stu-id="39e57-121">Informational.</span></span>

</dd> <dt>

<span data-ttu-id="39e57-122">4</span><span class="sxs-lookup"><span data-stu-id="39e57-122">4</span></span>
</dt> <dd>

<span data-ttu-id="39e57-123">Не является критическим.</span><span class="sxs-lookup"><span data-stu-id="39e57-123">Non-critical.</span></span>

</dd> <dt>

<span data-ttu-id="39e57-124">5</span><span class="sxs-lookup"><span data-stu-id="39e57-124">5</span></span>
</dt> <dd>

<span data-ttu-id="39e57-125">Критическое —</span><span class="sxs-lookup"><span data-stu-id="39e57-125">Critical.</span></span>

</dd> <dt>

<span data-ttu-id="39e57-126">6</span><span class="sxs-lookup"><span data-stu-id="39e57-126">6</span></span>
</dt> <dd>

<span data-ttu-id="39e57-127">Неустранимая.</span><span class="sxs-lookup"><span data-stu-id="39e57-127">Unrecoverable.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39e57-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39e57-128">Return value</span></span>

<span data-ttu-id="39e57-129">Возвращает значение 0 (нуль) при успешном выполнении, 1 (один), если запрошенный уровень срочности не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="39e57-129">Returns a value of 0 (zero) on success, 1 (one) if the requested urgency level is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="39e57-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39e57-130">Remarks</span></span>

<span data-ttu-id="39e57-131">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="39e57-131">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="39e57-132">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="39e57-132">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="39e57-133">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="39e57-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="39e57-134">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="39e57-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="39e57-135">Требования</span><span class="sxs-lookup"><span data-stu-id="39e57-135">Requirements</span></span>



| <span data-ttu-id="39e57-136">Требование</span><span class="sxs-lookup"><span data-stu-id="39e57-136">Requirement</span></span> | <span data-ttu-id="39e57-137">Значение</span><span class="sxs-lookup"><span data-stu-id="39e57-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39e57-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39e57-138">Minimum supported client</span></span><br/> | <span data-ttu-id="39e57-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39e57-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39e57-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39e57-140">Minimum supported server</span></span><br/> | <span data-ttu-id="39e57-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39e57-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39e57-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="39e57-142">Namespace</span></span><br/>                | <span data-ttu-id="39e57-143">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="39e57-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="39e57-144">MOF</span><span class="sxs-lookup"><span data-stu-id="39e57-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39e57-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39e57-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="39e57-146">DLL</span><span class="sxs-lookup"><span data-stu-id="39e57-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39e57-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39e57-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39e57-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39e57-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39e57-149">\_АЛАРМДЕВИЦЕ CIM</span><span class="sxs-lookup"><span data-stu-id="39e57-149">CIM\_AlarmDevice</span></span>](seturgency-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[<span data-ttu-id="39e57-150">**\_АЛАРМДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="39e57-150">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> </dl>

 

