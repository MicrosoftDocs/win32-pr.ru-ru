---
description: Свойство ХаурсспеЦифиед объекта SWbemDateTime является логическим значением, указывающим, содержит ли компонент hours в значении DateTime CIM интервал или значение с подстановочным знаком.
ms.assetid: 55211da6-cbd5-4e61-ab7d-ee20363e9d81
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. ХаурсспеЦифиед (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.HoursSpecified
- ISWbemDateTime.HoursSpecified
- ISWbemDateTime.get_HoursSpecified
- ISWbemDateTime.put_HoursSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e092747768035b7948ddef66f4c4d542bfa2c38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701982"
---
# <a name="swbemdatetimehoursspecified-property"></a><span data-ttu-id="6cf78-103">SWbemDateTime. ХаурсспеЦифиед, свойство</span><span class="sxs-lookup"><span data-stu-id="6cf78-103">SWbemDateTime.HoursSpecified property</span></span>

<span data-ttu-id="6cf78-104">Свойство **хаурсспеЦифиед** объекта [**SWbemDateTime**](swbemdatetime.md) является логическим значением, указывающим, содержит ли компонент hours в значении DateTime CIM интервал или значение с подстановочным знаком.</span><span class="sxs-lookup"><span data-stu-id="6cf78-104">The **HoursSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the hours component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="6cf78-105">Если **хаурсспеЦифиед** имеет значение true [**, а параметр**](swbemdatetime-isinterval.md) **IsTrue** имеет значение **false**, то [**SWbemDateTime. Hours**](swbemdatetime-hours.md) содержит значение DateTime.</span><span class="sxs-lookup"><span data-stu-id="6cf78-105">If **HoursSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Hours**](swbemdatetime-hours.md) contains a datetime value.</span></span> <span data-ttu-id="6cf78-106">Значение DateTime, содержащее интервал, не может быть преобразовано в формат **\_ даты VT** или **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="6cf78-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="6cf78-107">Если **хаурсспеЦифиед** имеет **значение false** **, а** параметр **IsTrue имеет значение true**, то **SWbemDateTime. Hours** содержит интервал.</span><span class="sxs-lookup"><span data-stu-id="6cf78-107">If **HoursSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Hours** contains an interval.</span></span>

<span data-ttu-id="6cf78-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6cf78-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="6cf78-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6cf78-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cf78-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6cf78-110">Syntax</span></span>


```VB
SWbemDateTime.HoursSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="6cf78-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6cf78-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="6cf78-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="6cf78-112">Examples</span></span>

<span data-ttu-id="6cf78-113">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="6cf78-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="6cf78-114">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="6cf78-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6cf78-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6cf78-115">Requirements</span></span>



| <span data-ttu-id="6cf78-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6cf78-116">Requirement</span></span> | <span data-ttu-id="6cf78-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6cf78-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf78-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6cf78-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6cf78-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6cf78-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6cf78-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6cf78-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6cf78-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6cf78-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6cf78-122">Header</span><span class="sxs-lookup"><span data-stu-id="6cf78-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cf78-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cf78-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6cf78-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6cf78-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="6cf78-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6cf78-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6cf78-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6cf78-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cf78-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cf78-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6cf78-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="6cf78-128">CLSID</span></span><br/>                    | <span data-ttu-id="6cf78-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="6cf78-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="6cf78-130">IID</span><span class="sxs-lookup"><span data-stu-id="6cf78-130">IID</span></span><br/>                      | <span data-ttu-id="6cf78-131">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="6cf78-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="6cf78-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cf78-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cf78-133">**SWbemDateTime. ч**</span><span class="sxs-lookup"><span data-stu-id="6cf78-133">**SWbemDateTime.Hours**</span></span>](swbemdatetime-hours.md)
</dt> <dt>

[<span data-ttu-id="6cf78-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="6cf78-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="6cf78-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="6cf78-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




