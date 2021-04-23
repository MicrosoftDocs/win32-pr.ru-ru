---
description: Преобразует дату в строковом формате FILETIME в формат даты и времени CIM.
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: SWbemDateTime. Сетфилетиме, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ca3e36a284e3700e166e86f6786218bada8f369e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155839"
---
# <a name="swbemdatetimesetfiletime-method"></a><span data-ttu-id="d4399-103">SWbemDateTime. Сетфилетиме, метод</span><span class="sxs-lookup"><span data-stu-id="d4399-103">SWbemDateTime.SetFileTime method</span></span>

<span data-ttu-id="d4399-104">Метод **сетфилетиме** объекта [**SWbemDateTime**](swbemdatetime.md) преобразует дату в строковом формате **fileTime** в формат [даты и времени CIM](date-and-time-format.md) .</span><span class="sxs-lookup"><span data-stu-id="d4399-104">The **SetFileTime** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date in the string **FILETIME** format to the [CIM datetime](date-and-time-format.md) format.</span></span>

<span data-ttu-id="d4399-105">Формат **fileTime** — это 64-разрядная структура DateTime, представляющая число единиц с 100 до 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="d4399-105">The **FILETIME** format is a 64-bit datetime structure that represents the number of 100-nanosecond units since the beginning of January 1, 1601.</span></span> <span data-ttu-id="d4399-106">Инструментарий управления Windows (WMI) (WMI) рассматривает значения **fileTime** как строковые представления беззнаковых 64-разрядных чисел.</span><span class="sxs-lookup"><span data-stu-id="d4399-106">Windows Management Instrumentation (WMI) treats **FILETIME** values as string representations of unsigned 64-bit numbers.</span></span>

<span data-ttu-id="d4399-107">Описание синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d4399-107">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d4399-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4399-108">Syntax</span></span>


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d4399-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4399-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4399-110">*стрфилетиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4399-110">*strFileTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4399-111">Значение **fileTime** , используемое для задания объекта.</span><span class="sxs-lookup"><span data-stu-id="d4399-111">**FILETIME** value used to set the object.</span></span>

</dd> <dt>

<span data-ttu-id="d4399-112">*бислокал* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d4399-112">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4399-113">Если **значение равно true**, *стрфилетиме* интерпретируется как местное время.</span><span class="sxs-lookup"><span data-stu-id="d4399-113">If **TRUE**, *strFileTime* is interpreted as a local time.</span></span> <span data-ttu-id="d4399-114">Свойство времени в формате UTC содержит местное время, преобразованное в правильное смещение в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="d4399-114">The Coordinated Universal Time (UTC) property contains the local time converted to the correct UTC offset.</span></span> <span data-ttu-id="d4399-115">Если *бислокал* имеет **значение false**, то *стрфилетиме* преобразуется непосредственно в значение UTC со смещением 0 (нулем).</span><span class="sxs-lookup"><span data-stu-id="d4399-115">When *bIsLocal* is **FALSE**, then *strFileTime* is converted directly into a UTC value with an offset of 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4399-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4399-116">Return value</span></span>

<span data-ttu-id="d4399-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d4399-117">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d4399-118">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d4399-118">Error codes</span></span>

<span data-ttu-id="d4399-119">После завершения метода **сетфилетиме** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать код ошибки из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="d4399-119">After completing the **SetFileTime** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d4399-120">**вбемерринвалидсинтакс** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="d4399-120">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="d4399-121">Недопустимый формат *стрфилетиме* .</span><span class="sxs-lookup"><span data-stu-id="d4399-121">The format of *strFileTime* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4399-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4399-122">Remarks</span></span>

<span data-ttu-id="d4399-123">После успешного вызова **сетфилетиме** значение [**DateTime**](datetime.md) всегда интерпретируется как абсолютное значение (**DateTime**) [**, а**](swbemdatetime-isinterval.md) параметру IsFalse — значение **false**.</span><span class="sxs-lookup"><span data-stu-id="d4399-123">After a successful call to **SetFileTime**, the [**datetime**](datetime.md) value is always interpreted as an absolute (**datetime**) value, and [**IsInterval**](swbemdatetime-isinterval.md) is set to **FALSE**.</span></span>

## <a name="examples"></a><span data-ttu-id="d4399-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="d4399-124">Examples</span></span>

<span data-ttu-id="d4399-125">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="d4399-125">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="d4399-126">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="d4399-126">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4399-127">Требования</span><span class="sxs-lookup"><span data-stu-id="d4399-127">Requirements</span></span>



| <span data-ttu-id="d4399-128">Требование</span><span class="sxs-lookup"><span data-stu-id="d4399-128">Requirement</span></span> | <span data-ttu-id="d4399-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d4399-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4399-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4399-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d4399-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4399-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d4399-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4399-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d4399-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4399-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d4399-134">Header</span><span class="sxs-lookup"><span data-stu-id="d4399-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4399-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4399-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4399-136">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d4399-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="d4399-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d4399-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d4399-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d4399-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4399-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4399-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d4399-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="d4399-140">CLSID</span></span><br/>                    | <span data-ttu-id="d4399-141">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="d4399-141">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="d4399-142">IID</span><span class="sxs-lookup"><span data-stu-id="d4399-142">IID</span></span><br/>                      | <span data-ttu-id="d4399-143">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="d4399-143">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d4399-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4399-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4399-145">**SWbemDateTime. Сетвардате**</span><span class="sxs-lookup"><span data-stu-id="d4399-145">**SWbemDateTime.SetVarDate**</span></span>](swbemdatetime-setvardate.md)
</dt> <dt>

[<span data-ttu-id="d4399-146">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="d4399-146">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="d4399-147">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="d4399-147">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

