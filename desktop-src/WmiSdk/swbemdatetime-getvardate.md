---
description: Преобразует значение даты и времени в формате DATETIME CIM в \_ Формат даты VT.
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: SWbemDateTime. GetVarDate, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d0c71e4748774eacab4b234092178179a4a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711652"
---
# <a name="swbemdatetimegetvardate-method"></a><span data-ttu-id="f7c5a-103">SWbemDateTime. GetVarDate, метод</span><span class="sxs-lookup"><span data-stu-id="f7c5a-103">SWbemDateTime.GetVarDate method</span></span>

<span data-ttu-id="f7c5a-104">Метод **GetVarDate** объекта [**SWbemDateTime**](swbemdatetime.md) преобразует значение даты и времени в формате [**DateTime**](datetime.md) CIM в формат **\_ даты VT** .</span><span class="sxs-lookup"><span data-stu-id="f7c5a-104">The **GetVarDate** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date and time value in the CIM [**DATETIME**](datetime.md) format to the **VT\_DATE** format.</span></span>

<span data-ttu-id="f7c5a-105">Формат **\_ даты VT** — это значение даты и [**времени**](datetime.md) автоматизации типа Variant, которое Visual Basic и использование ActiveX.</span><span class="sxs-lookup"><span data-stu-id="f7c5a-105">The **VT\_DATE** format is an automation variant [**DATETIME**](datetime.md) value that Visual Basic and ActiveX use.</span></span>

<span data-ttu-id="f7c5a-106">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f7c5a-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f7c5a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7c5a-107">Syntax</span></span>


```VB
vdate = .GetVarDate( _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f7c5a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7c5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7c5a-109">*бислокал* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f7c5a-109">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7c5a-110">Указывает, интерпретируется ли возвращаемое значение как местное время.</span><span class="sxs-lookup"><span data-stu-id="f7c5a-110">Indicates whether the returned value is interpreted as local time.</span></span> <span data-ttu-id="f7c5a-111">Свойство времени в формате UTC содержит местное время, преобразованное в правильное смещение в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="f7c5a-111">The Coordinated Universal Time (UTC) property contains the local time converted to the correct UTC offset.</span></span> <span data-ttu-id="f7c5a-112">Если значение равно **false**, то значение интерпретируется как время в формате UTC с нулевым смещением (0).</span><span class="sxs-lookup"><span data-stu-id="f7c5a-112">If the value is **FALSE**, then the value is interpreted as UTC with a zero (0) offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7c5a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7c5a-113">Return value</span></span>

<span data-ttu-id="f7c5a-114">Значение даты и времени в формате **\_ даты VT** .</span><span class="sxs-lookup"><span data-stu-id="f7c5a-114">The date and time value in the **VT\_DATE** format.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7c5a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7c5a-115">Remarks</span></span>

<span data-ttu-id="f7c5a-116">**VT \_ Значения DATE** и **fileTime** не могут содержать подстановочные поля.</span><span class="sxs-lookup"><span data-stu-id="f7c5a-116">**VT\_DATE** and **FILETIME** values cannot contain wildcard fields.</span></span>

<span data-ttu-id="f7c5a-117">Метод **GetVarDate** завершается ошибкой (**вбемеррфаилед**), если любое из следующих свойств имеет **значение false**:</span><span class="sxs-lookup"><span data-stu-id="f7c5a-117">The **GetVarDate** method fails (**wbemErrFailed**) if any of the following properties are **FALSE**:</span></span>

-   [<span data-ttu-id="f7c5a-118">**еарспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="f7c5a-118">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
-   [<span data-ttu-id="f7c5a-119">**монсспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="f7c5a-119">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
-   [<span data-ttu-id="f7c5a-120">**дайспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="f7c5a-120">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
-   [<span data-ttu-id="f7c5a-121">**хаурсспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="f7c5a-121">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
-   [<span data-ttu-id="f7c5a-122">**минутесспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="f7c5a-122">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
-   [<span data-ttu-id="f7c5a-123">**секондсспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="f7c5a-123">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
-   [<span data-ttu-id="f7c5a-124">**микросекондсспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="f7c5a-124">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
-   [<span data-ttu-id="f7c5a-125">**уткспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="f7c5a-125">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)

<span data-ttu-id="f7c5a-126">При успешном возврате из [**сетвардате**](swbemdatetime-setvardate.md)всем этим свойствам присваивается **значение true**.</span><span class="sxs-lookup"><span data-stu-id="f7c5a-126">On successful return from [**SetVarDate**](swbemdatetime-setvardate.md), all of these properties are set to **TRUE**.</span></span>

<span data-ttu-id="f7c5a-127">После успешного вызова [**сетвардате**](swbemdatetime-setvardate.md)значение [**DateTime**](datetime.md) всегда интерпретируется как абсолютное значение **DateTime** вместо интервала, а для параметра IsFalse [**устанавливается значение**](swbemdatetime-isinterval.md) **false**.</span><span class="sxs-lookup"><span data-stu-id="f7c5a-127">After a successful call to [**SetVarDate**](swbemdatetime-setvardate.md), the [**DATETIME**](datetime.md) value is always interpreted as an absolute **DATETIME** value instead of an interval, and the [**IsInterval**](swbemdatetime-isinterval.md) is set to **FALSE**.</span></span>

<span data-ttu-id="f7c5a-128">Если параметру IsTrue [**присвоено**](swbemdatetime-isinterval.md) значение **true**, вызов **GetVarDate** приводит к ошибке **вбемеррфаилед** .</span><span class="sxs-lookup"><span data-stu-id="f7c5a-128">If [**IsInterval**](swbemdatetime-isinterval.md) is set to **TRUE**, then a call to **GetVarDate** results in the **wbemErrFailed** error.</span></span>

<span data-ttu-id="f7c5a-129">При вызове **GetVarDate** происходит некоторое снижение точности, поскольку значения [DateTime](datetime.md) имеют одно разрешение в микросекундах, а значения **\_ даты VT** имеют разрешение 500 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="f7c5a-129">Some loss of precision occurs when you call **GetVarDate**, because [datetime](datetime.md) values have a one microsecond ( s) resolution, and **VT\_DATE** values have a 500 millisecond resolution.</span></span>

## <a name="examples"></a><span data-ttu-id="f7c5a-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="f7c5a-130">Examples</span></span>

<span data-ttu-id="f7c5a-131">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в и из параметра **fileTime** или формата **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="f7c5a-131">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="f7c5a-132">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="f7c5a-132">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7c5a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="f7c5a-133">Requirements</span></span>



| <span data-ttu-id="f7c5a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="f7c5a-134">Requirement</span></span> | <span data-ttu-id="f7c5a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="f7c5a-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7c5a-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7c5a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f7c5a-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7c5a-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f7c5a-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7c5a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f7c5a-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7c5a-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f7c5a-140">Header</span><span class="sxs-lookup"><span data-stu-id="f7c5a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7c5a-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7c5a-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7c5a-142">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f7c5a-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="f7c5a-143"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f7c5a-143"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f7c5a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f7c5a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7c5a-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7c5a-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f7c5a-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="f7c5a-146">CLSID</span></span><br/>                    | <span data-ttu-id="f7c5a-147">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="f7c5a-147">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="f7c5a-148">IID</span><span class="sxs-lookup"><span data-stu-id="f7c5a-148">IID</span></span><br/>                      | <span data-ttu-id="f7c5a-149">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="f7c5a-149">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="f7c5a-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7c5a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7c5a-151">**SWbemDateTime. функции getFileTime**</span><span class="sxs-lookup"><span data-stu-id="f7c5a-151">**SWbemDateTime.GetFileTime**</span></span>](swbemdatetime-getfiletime.md)
</dt> <dt>

[<span data-ttu-id="f7c5a-152">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="f7c5a-152">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="f7c5a-153">DATETIME</span><span class="sxs-lookup"><span data-stu-id="f7c5a-153">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




