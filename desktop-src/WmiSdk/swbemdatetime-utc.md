---
description: Возвращает или задает представление значения даты и времени в формате UTC.
ms.assetid: 43d9d0c8-5521-410f-825b-6b00c3dd0039
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. UTC (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTC
- ISWbemDateTime.UTC
- ISWbemDateTime.get_UTC
- ISWbemDateTime.put_UTC
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 80a4c32e47b94289f66999fdbf1f7daf5f9f03cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701975"
---
# <a name="swbemdatetimeutc-property"></a><span data-ttu-id="abfb4-103">SWbemDateTime. UTC, свойство</span><span class="sxs-lookup"><span data-stu-id="abfb4-103">SWbemDateTime.UTC property</span></span>

<span data-ttu-id="abfb4-104">Свойство **UTC** объекта [**SWbemDateTime**](swbemdatetime.md) Возвращает или задает представление значения **DateTime** в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="abfb4-104">The **UTC** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets the Coordinated Universal Times (UTC) representation of the **datetime** value.</span></span> <span data-ttu-id="abfb4-105">UTC — это время, заданное стандартом мирового времени.</span><span class="sxs-lookup"><span data-stu-id="abfb4-105">UTC is the time as set by the World Time Standard.</span></span> <span data-ttu-id="abfb4-106">Время в формате UTC заменяется средним временем по Гринвичу (GMT).</span><span class="sxs-lookup"><span data-stu-id="abfb4-106">UTC has replaced Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="abfb4-107">Значение UTC с нулевым смещением равно значению GMT с нулевым смещением.</span><span class="sxs-lookup"><span data-stu-id="abfb4-107">A UTC value with a zero offset is the same as GMT with a zero offset.</span></span> <span data-ttu-id="abfb4-108">Число со знаком должно быть в диапазоне от-720 до 720 или возвращена ошибка **вбемеррвалуеаутофранже** .</span><span class="sxs-lookup"><span data-stu-id="abfb4-108">The signed number must be in the range of -720 through 720 or the error **wbemErrValueOutOfRange** is returned.</span></span>

<span data-ttu-id="abfb4-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="abfb4-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="abfb4-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="abfb4-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="abfb4-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abfb4-111">Syntax</span></span>


```VB
SWbemDateTime.UTC As Long
```



## <a name="property-value"></a><span data-ttu-id="abfb4-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="abfb4-112">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="abfb4-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="abfb4-113">Error codes</span></span>

<span data-ttu-id="abfb4-114">После получения или задания свойства **UTC** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать приведенный ниже код ошибки.</span><span class="sxs-lookup"><span data-stu-id="abfb4-114">After you get or set the **UTC** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="abfb4-115">**вбемеррвалуеаутофранже** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="abfb4-115">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="abfb4-116">Значение не находится в диапазоне от-720 до 720.</span><span class="sxs-lookup"><span data-stu-id="abfb4-116">The value was not in the range of -720 through 720.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="abfb4-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="abfb4-117">Examples</span></span>

<span data-ttu-id="abfb4-118">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="abfb4-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="abfb4-119">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="abfb4-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="abfb4-120">Требования</span><span class="sxs-lookup"><span data-stu-id="abfb4-120">Requirements</span></span>



| <span data-ttu-id="abfb4-121">Требование</span><span class="sxs-lookup"><span data-stu-id="abfb4-121">Requirement</span></span> | <span data-ttu-id="abfb4-122">Значение</span><span class="sxs-lookup"><span data-stu-id="abfb4-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abfb4-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="abfb4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="abfb4-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abfb4-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="abfb4-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="abfb4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="abfb4-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abfb4-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="abfb4-127">Header</span><span class="sxs-lookup"><span data-stu-id="abfb4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="abfb4-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="abfb4-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="abfb4-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="abfb4-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="abfb4-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="abfb4-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="abfb4-131">DLL</span><span class="sxs-lookup"><span data-stu-id="abfb4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abfb4-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abfb4-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="abfb4-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="abfb4-133">CLSID</span></span><br/>                    | <span data-ttu-id="abfb4-134">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="abfb4-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="abfb4-135">IID</span><span class="sxs-lookup"><span data-stu-id="abfb4-135">IID</span></span><br/>                      | <span data-ttu-id="abfb4-136">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="abfb4-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="abfb4-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abfb4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abfb4-138">**SWbemDateTime. УткспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="abfb4-138">**SWbemDateTime.UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)
</dt> <dt>

[<span data-ttu-id="abfb4-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="abfb4-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="abfb4-140">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="abfb4-140">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

