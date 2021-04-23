---
description: Преобразует дату в формате VT в \_ Формат даты и времени CIM.
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: SWbemDateTime. Сетвардате, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetVarDate
- ISWbemDateTime.SetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8641bad2c59f100b689c74e23faf727bc80d2f49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348885"
---
# <a name="swbemdatetimesetvardate-method"></a><span data-ttu-id="dd495-103">SWbemDateTime. Сетвардате, метод</span><span class="sxs-lookup"><span data-stu-id="dd495-103">SWbemDateTime.SetVarDate method</span></span>

<span data-ttu-id="dd495-104">Метод **сетвардате** объекта [**SWbemDateTime**](swbemdatetime.md) преобразует дату в формате VT в формат **\_ даты** [и времени CIM](date-and-time-format.md) .</span><span class="sxs-lookup"><span data-stu-id="dd495-104">The **SetVarDate** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date in the **VT\_DATE** format to the [CIM datetime](date-and-time-format.md) format.</span></span>

<span data-ttu-id="dd495-105">Значение **\_ даты VT** — это значение типа datetime, которое Visual Basic и использование ActiveX.</span><span class="sxs-lookup"><span data-stu-id="dd495-105">A **VT\_DATE** value is a variant datetime value that Visual Basic and ActiveX use.</span></span>

<span data-ttu-id="dd495-106">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="dd495-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd495-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd495-107">Syntax</span></span>


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="dd495-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd495-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd495-109">*вдате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd495-109">*vdate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd495-110">Значение варианта даты для задания объекта.</span><span class="sxs-lookup"><span data-stu-id="dd495-110">The variant date value to set the object.</span></span> <span data-ttu-id="dd495-111">Этот параметр должен быть в формате **\_ даты VT** .</span><span class="sxs-lookup"><span data-stu-id="dd495-111">This parameter must be in the **VT\_DATE** format.</span></span>

</dd> <dt>

<span data-ttu-id="dd495-112">*бислокал* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="dd495-112">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dd495-113">Если **значение равно true**, *вдате* интерпретируется как местное время, а свойство координированного скоординированного времени (UTC) содержит местное время, которое преобразуется в правильное смещение в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="dd495-113">If **TRUE**, *vdate* is interpreted as a local time, and the Coordinated Universal Time (UTC) property contains the local time that is converted to the correct UTC offset.</span></span> <span data-ttu-id="dd495-114">Если *бислокал* имеет **значение false**, то *вдате* преобразуется непосредственно в значение времени в формате UTC с нулевым смещением (0).</span><span class="sxs-lookup"><span data-stu-id="dd495-114">When *bIsLocal* is **FALSE**, then *vdate* is converted directly into a UTC value with an offset of zero (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd495-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd495-115">Return value</span></span>

<span data-ttu-id="dd495-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dd495-116">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dd495-117">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="dd495-117">Error codes</span></span>

<span data-ttu-id="dd495-118">После завершения метода **сетвардате** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать код ошибки из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="dd495-118">After completing the **SetVarDate** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="dd495-119">**вбемерринвалидсинтакс** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="dd495-119">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="dd495-120">Недопустимый формат *вдате* .</span><span class="sxs-lookup"><span data-stu-id="dd495-120">The format of *vdate* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd495-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd495-121">Remarks</span></span>

<span data-ttu-id="dd495-122">После успешного вызова **сетвардате** значение [**DateTime**](datetime.md) интерпретируется как абсолютное значение DateTime, а не как интервал, а свойство " [**интервал**](swbemdatetime-isinterval.md) " — в значение **false**.</span><span class="sxs-lookup"><span data-stu-id="dd495-122">After a successful call to **SetVarDate**, the [**DATETIME**](datetime.md) value is interpreted as an absolute datetime value instead of an interval, and the [**IsInterval**](swbemdatetime-isinterval.md) property is set to **FALSE**.</span></span>

<span data-ttu-id="dd495-123">Встроенная функция [CDate](/previous-versions//2dt118h2(v=vs.85)) Visual Basic или VBScript предоставляет значение [**DateTime**](datetime.md) в формате **\_ даты VT** для входных данных в **сетвардате**.</span><span class="sxs-lookup"><span data-stu-id="dd495-123">The intrinsic Visual Basic or VBScript function [CDate](/previous-versions//2dt118h2(v=vs.85)) provides a [**datetime**](datetime.md) value in the **VT\_DATE** format for input to **SetVarDate**.</span></span>

## <a name="examples"></a><span data-ttu-id="dd495-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="dd495-124">Examples</span></span>

<span data-ttu-id="dd495-125">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="dd495-125">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="dd495-126">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="dd495-126">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

<span data-ttu-id="dd495-127">Пример кода VBScript [Date to WMI Date-Time Format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) в коллекции TechNet использует сетвардате для преобразования регулярного значения даты и времени в формат даты и времени в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="dd495-127">The [Convert Date to WMI Date-Time Format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript code sample in the TechNet Gallery uses SetVarDate to convert a regular date-time value into the UTC date-time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd495-128">Требования</span><span class="sxs-lookup"><span data-stu-id="dd495-128">Requirements</span></span>



| <span data-ttu-id="dd495-129">Требование</span><span class="sxs-lookup"><span data-stu-id="dd495-129">Requirement</span></span> | <span data-ttu-id="dd495-130">Значение</span><span class="sxs-lookup"><span data-stu-id="dd495-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd495-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd495-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dd495-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd495-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd495-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd495-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dd495-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd495-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd495-135">Header</span><span class="sxs-lookup"><span data-stu-id="dd495-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd495-136"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd495-136"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd495-137">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="dd495-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="dd495-138"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dd495-138"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dd495-139">DLL</span><span class="sxs-lookup"><span data-stu-id="dd495-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd495-140"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd495-140"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dd495-141">CLSID</span><span class="sxs-lookup"><span data-stu-id="dd495-141">CLSID</span></span><br/>                    | <span data-ttu-id="dd495-142">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="dd495-142">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="dd495-143">IID</span><span class="sxs-lookup"><span data-stu-id="dd495-143">IID</span></span><br/>                      | <span data-ttu-id="dd495-144">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="dd495-144">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="dd495-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd495-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd495-146">**SWbemDateTime. Сетфилетиме**</span><span class="sxs-lookup"><span data-stu-id="dd495-146">**SWbemDateTime.SetFileTime**</span></span>](swbemdatetime-setfiletime.md)
</dt> <dt>

[<span data-ttu-id="dd495-147">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="dd495-147">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="dd495-148">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="dd495-148">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

