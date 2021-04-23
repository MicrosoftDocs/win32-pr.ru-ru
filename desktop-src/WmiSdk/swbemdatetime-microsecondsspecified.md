---
description: Логическое значение, указывающее, содержит ли компонент микросекунды в значении DateTime CIM интервал или значение с подстановочным знаком.
ms.assetid: 65244ece-2326-4edc-b982-57e2046ec33e
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. МикросекондсспеЦифиед (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MicrosecondsSpecified
- ISWbemDateTime.MicrosecondsSpecified
- ISWbemDateTime.get_MicrosecondsSpecified
- ISWbemDateTime.put_MicrosecondsSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d4fa9d99cf323e19ccd298786896f789bbb08be6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701979"
---
# <a name="swbemdatetimemicrosecondsspecified-property"></a><span data-ttu-id="3b54a-103">SWbemDateTime. МикросекондсспеЦифиед, свойство</span><span class="sxs-lookup"><span data-stu-id="3b54a-103">SWbemDateTime.MicrosecondsSpecified property</span></span>

<span data-ttu-id="3b54a-104">Свойство **микросекондсспеЦифиед** объекта [**SWbemDateTime**](swbemdatetime.md) является логическим значением, указывающим, содержит ли компонент микросекунды в значении типа данных CIM интервал или значение с подстановочным знаком.</span><span class="sxs-lookup"><span data-stu-id="3b54a-104">The **MicrosecondsSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the microseconds component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="3b54a-105">Если **микросекондсспеЦифиед** имеет значение true [**, а параметр**](swbemdatetime-isinterval.md) **IsTrue** имеет значение **false**, то [**SWbemDateTime. в микросекундах**](swbemdatetime-microseconds.md) содержит значение DateTime.</span><span class="sxs-lookup"><span data-stu-id="3b54a-105">If **MicrosecondsSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Microseconds**](swbemdatetime-microseconds.md) contains a datetime value.</span></span> <span data-ttu-id="3b54a-106">Значение DateTime, содержащее интервал, не может быть преобразовано в формат **\_ даты VT** или **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="3b54a-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="3b54a-107">Если [**хаурсспеЦифиед**](swbemdatetime-hoursspecified.md) имеет **значение false** **, а** параметр **IsTrue имеет значение true**, то **SWbemDateTime. МКС** содержит интервал.</span><span class="sxs-lookup"><span data-stu-id="3b54a-107">If [**HoursSpecified**](swbemdatetime-hoursspecified.md) is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Microseconds** contains an interval.</span></span>

<span data-ttu-id="3b54a-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3b54a-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="3b54a-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3b54a-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b54a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b54a-110">Syntax</span></span>


```VB
SWbemDateTime.MicrosecondsSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="3b54a-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3b54a-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="3b54a-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="3b54a-112">Examples</span></span>

<span data-ttu-id="3b54a-113">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="3b54a-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="3b54a-114">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="3b54a-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b54a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3b54a-115">Requirements</span></span>



| <span data-ttu-id="3b54a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3b54a-116">Requirement</span></span> | <span data-ttu-id="3b54a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3b54a-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b54a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b54a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3b54a-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b54a-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b54a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b54a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3b54a-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b54a-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b54a-122">Header</span><span class="sxs-lookup"><span data-stu-id="3b54a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b54a-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b54a-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b54a-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3b54a-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="3b54a-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3b54a-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3b54a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3b54a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b54a-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b54a-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3b54a-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="3b54a-128">CLSID</span></span><br/>                    | <span data-ttu-id="3b54a-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="3b54a-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="3b54a-130">IID</span><span class="sxs-lookup"><span data-stu-id="3b54a-130">IID</span></span><br/>                      | <span data-ttu-id="3b54a-131">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="3b54a-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="3b54a-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b54a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b54a-133">**SWbemDateTime. микросекунды**</span><span class="sxs-lookup"><span data-stu-id="3b54a-133">**SWbemDateTime.Microseconds**</span></span>](swbemdatetime-microseconds.md)
</dt> <dt>

[<span data-ttu-id="3b54a-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="3b54a-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="3b54a-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="3b54a-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




