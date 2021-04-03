---
description: Метод Ресеткаунтер сбрасывает счетчики ошибок и предупреждений.
ms.assetid: 5bc6c939-cd97-40ca-a16c-5227e7f27c76
ms.tgt_platform: multiple
title: Метод Ресеткаунтер класса CIM_DeviceErrorCounts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts.ResetCounter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 386547362f5a7aa52bddfbf9df3af01949aecbdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895474"
---
# <a name="resetcounter-method-of-the-cim_deviceerrorcounts-class"></a><span data-ttu-id="60d83-103">Метод Ресеткаунтер \_ класса CIM девицеерроркаунтс</span><span class="sxs-lookup"><span data-stu-id="60d83-103">ResetCounter method of the CIM\_DeviceErrorCounts class</span></span>

<span data-ttu-id="60d83-104">Метод **ресеткаунтер** сбрасывает счетчики ошибок и предупреждений.</span><span class="sxs-lookup"><span data-stu-id="60d83-104">The **ResetCounter** method resets the error and warning counters.</span></span> <span data-ttu-id="60d83-105">Метод используется таким образом, чтобы инструментирование логического устройства, которое будет выводить ошибки и предупреждения в виде табуляции, также мог сбросить свою внутреннюю обработку и счетчики.</span><span class="sxs-lookup"><span data-stu-id="60d83-105">A method is used so that the logical device's instrumentation, which tabulates the errors and warnings, can also reset its internal processing and counters.</span></span> <span data-ttu-id="60d83-106">В подклассе набор возможных кодов возврата можно указать с помощью квалификатора **ValueMap** в методе.</span><span class="sxs-lookup"><span data-stu-id="60d83-106">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="60d83-107">Строки, в которые транслируются содержимое **ValueMap** , также можно указать в подклассе как квалификатор массива **значений** .</span><span class="sxs-lookup"><span data-stu-id="60d83-107">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60d83-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="60d83-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="60d83-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="60d83-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="60d83-110">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="60d83-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="60d83-111">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="60d83-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="60d83-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60d83-112">Syntax</span></span>


```mof
uint32 ResetCounter(
  [in] uint16 SelectedCounter
);
```



## <a name="parameters"></a><span data-ttu-id="60d83-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="60d83-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60d83-114">*Селектедкаунтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60d83-114">*SelectedCounter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60d83-115">Счетчик ошибок для сброса.</span><span class="sxs-lookup"><span data-stu-id="60d83-115">Error counter to reset.</span></span>

<dt>

<span id="All"></span><span id="all"></span><span id="ALL"></span>

<span data-ttu-id="60d83-116">**Все** (0)</span><span class="sxs-lookup"><span data-stu-id="60d83-116">**All** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Indeterminate_Error_Counter"></span><span id="indeterminate_error_counter"></span><span id="INDETERMINATE_ERROR_COUNTER"></span>

<span data-ttu-id="60d83-117">**Счетчик неопределенных ошибок** (1)</span><span class="sxs-lookup"><span data-stu-id="60d83-117">**Indeterminate Error Counter** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical_Error_Counter"></span><span id="critical_error_counter"></span><span id="CRITICAL_ERROR_COUNTER"></span>

<span data-ttu-id="60d83-118">**Счетчик критических ошибок** (2)</span><span class="sxs-lookup"><span data-stu-id="60d83-118">**Critical Error Counter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Major_Error_Counter"></span><span id="major_error_counter"></span><span id="MAJOR_ERROR_COUNTER"></span>

<span data-ttu-id="60d83-119">**Счетчик основных ошибок** (3)</span><span class="sxs-lookup"><span data-stu-id="60d83-119">**Major Error Counter** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Minor_Error_Counter"></span><span id="minor_error_counter"></span><span id="MINOR_ERROR_COUNTER"></span>

<span data-ttu-id="60d83-120">**Счетчик незначительных ошибок** (4)</span><span class="sxs-lookup"><span data-stu-id="60d83-120">**Minor Error Counter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning_Counter"></span><span id="warning_counter"></span><span id="WARNING_COUNTER"></span>

<span data-ttu-id="60d83-121">**Счетчик предупреждений** (5)</span><span class="sxs-lookup"><span data-stu-id="60d83-121">**Warning Counter** (5)</span></span>


<span data-ttu-id="60d83-122"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="60d83-122"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="60d83-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60d83-123">Return value</span></span>

<span data-ttu-id="60d83-124">Возвращает 0 (нуль) в случае успеха, 1 (один), если не поддерживается, и любое другое значение, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="60d83-124">Returns 0 (zero) if successful, 1 (one) if not supported, and any other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="60d83-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60d83-125">Remarks</span></span>

<span data-ttu-id="60d83-126">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="60d83-126">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="60d83-127">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="60d83-127">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="60d83-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="60d83-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="60d83-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="60d83-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="60d83-130">Требования</span><span class="sxs-lookup"><span data-stu-id="60d83-130">Requirements</span></span>



| <span data-ttu-id="60d83-131">Требование</span><span class="sxs-lookup"><span data-stu-id="60d83-131">Requirement</span></span> | <span data-ttu-id="60d83-132">Значение</span><span class="sxs-lookup"><span data-stu-id="60d83-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60d83-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60d83-133">Minimum supported client</span></span><br/> | <span data-ttu-id="60d83-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60d83-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60d83-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60d83-135">Minimum supported server</span></span><br/> | <span data-ttu-id="60d83-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60d83-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60d83-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="60d83-137">Namespace</span></span><br/>                | <span data-ttu-id="60d83-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="60d83-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="60d83-139">MOF</span><span class="sxs-lookup"><span data-stu-id="60d83-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60d83-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60d83-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="60d83-141">DLL</span><span class="sxs-lookup"><span data-stu-id="60d83-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60d83-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60d83-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60d83-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60d83-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60d83-144">\_ДЕВИЦЕЕРРОРКАУНТС CIM</span><span class="sxs-lookup"><span data-stu-id="60d83-144">CIM\_DeviceErrorCounts</span></span>](resetcounter-method-in-class-cim-deviceerrorcounts.md)
</dt> <dt>

[<span data-ttu-id="60d83-145">**\_ДЕВИЦЕЕРРОРКАУНТС CIM**</span><span class="sxs-lookup"><span data-stu-id="60d83-145">**CIM\_DeviceErrorCounts**</span></span>](cim-deviceerrorcounts.md)
</dt> </dl>

 

