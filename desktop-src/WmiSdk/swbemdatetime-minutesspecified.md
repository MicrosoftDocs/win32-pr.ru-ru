---
description: Указывает, содержит ли компонент минут в значении DateTime CIM интервал или значение с подстановочным знаком.
ms.assetid: de15f87e-0092-467e-b0d7-42ef447fa00a
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. МинутесспеЦифиед (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MinutesSpecified
- ISWbemDateTime.MinutesSpecified
- ISWbemDateTime.get_MinutesSpecified
- ISWbemDateTime.put_MinutesSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 62f64ad749ee020093008a308a3244e045f9995d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155842"
---
# <a name="swbemdatetimeminutesspecified-property"></a><span data-ttu-id="51f67-103">SWbemDateTime. МинутесспеЦифиед, свойство</span><span class="sxs-lookup"><span data-stu-id="51f67-103">SWbemDateTime.MinutesSpecified property</span></span>

<span data-ttu-id="51f67-104">Свойство **минутесспеЦифиед** объекта [**SWbemDateTime**](swbemdatetime.md) является логическим значением, указывающим, содержит ли компонент минут в значении DateTime CIM интервал или значение с подстановочным знаком.</span><span class="sxs-lookup"><span data-stu-id="51f67-104">The **MinutesSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the minutes component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="51f67-105">Если **минутесспеЦифиед** имеет **значение true** [**, а параметр**](swbemdatetime-isinterval.md) ISDATE имеет значение **false** (что означает, что значение DateTime в CIM не содержит подстановочных знаков), то [**SWbemDateTime. minutes**](swbemdatetime-minutes.md) содержит значение даты.</span><span class="sxs-lookup"><span data-stu-id="51f67-105">If **MinutesSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE** (indicating that the CIM datetime value has no wildcards), then [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) contains a date value.</span></span> <span data-ttu-id="51f67-106">Значение DateTime, содержащее интервал, не может быть преобразовано в формат **\_ даты VT** или **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="51f67-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="51f67-107">Если [**хаурсспеЦифиед**](swbemdatetime-hoursspecified.md) имеет **значение false** **, а** параметр **IsTrue имеет значение true**, то **SWbemDateTime. minutes** содержит интервал.</span><span class="sxs-lookup"><span data-stu-id="51f67-107">If [**HoursSpecified**](swbemdatetime-hoursspecified.md) is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Minutes** contains an interval.</span></span>

<span data-ttu-id="51f67-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="51f67-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="51f67-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="51f67-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="51f67-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51f67-110">Syntax</span></span>


```VB
SWbemDateTime.MinutesSpecified As boolean
```



## <a name="property-value"></a><span data-ttu-id="51f67-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="51f67-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="51f67-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="51f67-112">Examples</span></span>

<span data-ttu-id="51f67-113">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="51f67-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="51f67-114">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="51f67-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51f67-115">Требования</span><span class="sxs-lookup"><span data-stu-id="51f67-115">Requirements</span></span>



| <span data-ttu-id="51f67-116">Требование</span><span class="sxs-lookup"><span data-stu-id="51f67-116">Requirement</span></span> | <span data-ttu-id="51f67-117">Значение</span><span class="sxs-lookup"><span data-stu-id="51f67-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51f67-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51f67-118">Minimum supported client</span></span><br/> | <span data-ttu-id="51f67-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51f67-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="51f67-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51f67-120">Minimum supported server</span></span><br/> | <span data-ttu-id="51f67-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51f67-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="51f67-122">Header</span><span class="sxs-lookup"><span data-stu-id="51f67-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="51f67-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="51f67-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="51f67-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="51f67-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="51f67-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="51f67-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="51f67-126">DLL</span><span class="sxs-lookup"><span data-stu-id="51f67-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51f67-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51f67-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="51f67-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="51f67-128">CLSID</span></span><br/>                    | <span data-ttu-id="51f67-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="51f67-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="51f67-130">IID</span><span class="sxs-lookup"><span data-stu-id="51f67-130">IID</span></span><br/>                      | <span data-ttu-id="51f67-131">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="51f67-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="51f67-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51f67-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51f67-133">**SWbemDateTime. минут**</span><span class="sxs-lookup"><span data-stu-id="51f67-133">**SWbemDateTime.Minutes**</span></span>](swbemdatetime-minutes.md)
</dt> <dt>

[<span data-ttu-id="51f67-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="51f67-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="51f67-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="51f67-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




