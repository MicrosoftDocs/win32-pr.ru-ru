---
description: Преобразует значение даты и времени в формате DATETIME CIM в формат FILETIME.
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: SWbemDateTime. функции getFileTime, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3f8a8c85cb4c78be578187b1f55afce078fe7bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498051"
---
# <a name="swbemdatetimegetfiletime-method"></a><span data-ttu-id="2a7c8-103">SWbemDateTime. функции getFileTime, метод</span><span class="sxs-lookup"><span data-stu-id="2a7c8-103">SWbemDateTime.GetFileTime method</span></span>

<span data-ttu-id="2a7c8-104">Метод **функции getFileTime** объекта [**SWbemDateTime**](swbemdatetime.md) преобразует значение даты и времени в формате [DateTime](datetime.md) CIM в формат FILETIME.</span><span class="sxs-lookup"><span data-stu-id="2a7c8-104">The **GetFileTime** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date and time value in the CIM [DATETIME](datetime.md) format to the FILETIME format.</span></span>

<span data-ttu-id="2a7c8-105">Если для параметра задано значение **true**, то возвращаемое значение представляет местное время клиента.</span><span class="sxs-lookup"><span data-stu-id="2a7c8-105">If the parameter is set to **TRUE**, then the return value represents a local time for the client.</span></span> <span data-ttu-id="2a7c8-106">В противном случае возвращаемое значение — это время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="2a7c8-106">Otherwise, the return value is a Coordinated Universal Time (UTC) time.</span></span> <span data-ttu-id="2a7c8-107">Структура  [даты и времени](datetime.md) FILETIME — это 64-разрядное значение, представляющее число единиц в 100-наносекундных с начала 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="2a7c8-107">A **FILETIME** [DATETIME](datetime.md) structure is a 64-bit value that represents the number of 100-nanosecond units since the beginning of January 1, 1601.</span></span> <span data-ttu-id="2a7c8-108">Инструментарий управления Windows (WMI) (WMI) рассматривает значения **fileTime** как строковые представления беззнаковых 64-разрядных чисел.</span><span class="sxs-lookup"><span data-stu-id="2a7c8-108">Windows Management Instrumentation (WMI) treats **FILETIME** values as string representations of unsigned 64-bit numbers.</span></span>

<span data-ttu-id="2a7c8-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2a7c8-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2a7c8-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a7c8-110">Syntax</span></span>


```VB
vDate = .GetFileTime( _
  [ ByVal bIsLocaL ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2a7c8-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a7c8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a7c8-112">*бислокал* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="2a7c8-112">*bIsLocaL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a7c8-113">Указывает, интерпретируется ли возвращаемое значение как местное время.</span><span class="sxs-lookup"><span data-stu-id="2a7c8-113">Indicates whether the returned value is interpreted as local time.</span></span> <span data-ttu-id="2a7c8-114">Свойство UTC содержит местное время, преобразованное в правильное смещение в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="2a7c8-114">The UTC property then contains the local time converted to the correct Coordinated Universal Times (UTC) offset.</span></span> <span data-ttu-id="2a7c8-115">Если значение равно **false**, то значение интерпретируется как время в формате UTC с нулевым смещением (0).</span><span class="sxs-lookup"><span data-stu-id="2a7c8-115">If the value is **FALSE**, then the value is interpreted as UTC with a zero (0) offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a7c8-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a7c8-116">Return value</span></span>

<span data-ttu-id="2a7c8-117">Дата и время в формате **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="2a7c8-117">The date and time in the **FILETIME** format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2a7c8-118">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="2a7c8-118">Error codes</span></span>

<span data-ttu-id="2a7c8-119">После завершения метода **функции getFileTime** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать код ошибки из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="2a7c8-119">After completing the **GetFileTime** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="2a7c8-120">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="2a7c8-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2a7c8-121">Вызов не выполнен.</span><span class="sxs-lookup"><span data-stu-id="2a7c8-121">The call failed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a7c8-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a7c8-122">Remarks</span></span>

<span data-ttu-id="2a7c8-123">**VT \_ Значения DATE** и **fileTime** не могут содержать подстановочные поля.</span><span class="sxs-lookup"><span data-stu-id="2a7c8-123">**VT\_DATE** and **FILETIME** values cannot contain wildcard fields.</span></span>

<span data-ttu-id="2a7c8-124">Метод **функции getFileTime** завершается ошибкой (вбемеррфаилед), если любое из следующих свойств имеет **значение false**:</span><span class="sxs-lookup"><span data-stu-id="2a7c8-124">The **GetFileTime** method fails (wbemErrFailed) if any of the following properties are **FALSE**:</span></span>

-   [<span data-ttu-id="2a7c8-125">**еарспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="2a7c8-125">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
-   [<span data-ttu-id="2a7c8-126">**монсспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="2a7c8-126">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
-   [<span data-ttu-id="2a7c8-127">**дайспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="2a7c8-127">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
-   [<span data-ttu-id="2a7c8-128">**хаурсспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="2a7c8-128">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
-   [<span data-ttu-id="2a7c8-129">**минутесспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="2a7c8-129">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
-   [<span data-ttu-id="2a7c8-130">**секондсспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="2a7c8-130">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
-   [<span data-ttu-id="2a7c8-131">**микросекондсспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="2a7c8-131">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
-   [<span data-ttu-id="2a7c8-132">**уткспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="2a7c8-132">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)

<span data-ttu-id="2a7c8-133">При успешном возврате из [**сетфилетиме**](swbemdatetime-setfiletime.md)всем этим свойствам присваивается **значение true**.</span><span class="sxs-lookup"><span data-stu-id="2a7c8-133">On a successful return from [**SetFileTime**](swbemdatetime-setfiletime.md), all of these properties are set to **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="2a7c8-134">Примеры</span><span class="sxs-lookup"><span data-stu-id="2a7c8-134">Examples</span></span>

<span data-ttu-id="2a7c8-135">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="2a7c8-135">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="2a7c8-136">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="2a7c8-136">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a7c8-137">Требования</span><span class="sxs-lookup"><span data-stu-id="2a7c8-137">Requirements</span></span>



| <span data-ttu-id="2a7c8-138">Требование</span><span class="sxs-lookup"><span data-stu-id="2a7c8-138">Requirement</span></span> | <span data-ttu-id="2a7c8-139">Значение</span><span class="sxs-lookup"><span data-stu-id="2a7c8-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a7c8-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a7c8-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2a7c8-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a7c8-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2a7c8-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a7c8-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2a7c8-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a7c8-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2a7c8-144">Header</span><span class="sxs-lookup"><span data-stu-id="2a7c8-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a7c8-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a7c8-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a7c8-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="2a7c8-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="2a7c8-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2a7c8-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2a7c8-148">DLL</span><span class="sxs-lookup"><span data-stu-id="2a7c8-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a7c8-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a7c8-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2a7c8-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="2a7c8-150">CLSID</span></span><br/>                    | <span data-ttu-id="2a7c8-151">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="2a7c8-151">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="2a7c8-152">IID</span><span class="sxs-lookup"><span data-stu-id="2a7c8-152">IID</span></span><br/>                      | <span data-ttu-id="2a7c8-153">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="2a7c8-153">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="2a7c8-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a7c8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a7c8-155">**SWbemDateTime. GetVarDate**</span><span class="sxs-lookup"><span data-stu-id="2a7c8-155">**SWbemDateTime.GetVarDate**</span></span>](swbemdatetime-getvardate.md)
</dt> <dt>

[<span data-ttu-id="2a7c8-156">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="2a7c8-156">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="2a7c8-157">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="2a7c8-157">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

