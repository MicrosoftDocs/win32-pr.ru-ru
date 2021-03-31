---
description: Логическое значение, указывающее, содержит ли компонент секунд в значении DATETIME CIM интервал или значение с подстановочным знаком.
ms.assetid: 9f9b75c3-ae08-49a6-b747-294831601a62
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. СекондсспеЦифиед (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SecondsSpecified
- ISWbemDateTime.SecondsSpecified
- ISWbemDateTime.get_SecondsSpecified
- ISWbemDateTime.put_SecondsSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e0cf97eff544d6e244890014108506f39b1934b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913007"
---
# <a name="swbemdatetimesecondsspecified-property"></a><span data-ttu-id="4187a-103">SWbemDateTime. СекондсспеЦифиед, свойство</span><span class="sxs-lookup"><span data-stu-id="4187a-103">SWbemDateTime.SecondsSpecified property</span></span>

<span data-ttu-id="4187a-104">Свойство **секондсспеЦифиед** объекта [**SWbemDateTime**](swbemdatetime.md) является логическим значением, указывающим, содержит ли компонент секунд в значении [**DateTime**](datetime.md) CIM интервал или значение с подстановочным знаком.</span><span class="sxs-lookup"><span data-stu-id="4187a-104">The **SecondsSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the seconds component in the CIM [**DATETIME**](datetime.md) value contains an interval or a wildcard value.</span></span> <span data-ttu-id="4187a-105">Если **секондсспеЦифиед** имеет  значение true [**, а параметр**](swbemdatetime-isinterval.md) ISDATE имеет значение **false**, то [**SWbemDateTime. Seconds**](swbemdatetime-seconds.md) содержит значение даты.</span><span class="sxs-lookup"><span data-stu-id="4187a-105">If **SecondsSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Seconds**](swbemdatetime-seconds.md) contains a date value.</span></span> <span data-ttu-id="4187a-106">Значение DateTime, содержащее интервал, не может быть преобразовано в формат **\_ даты VT** или **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="4187a-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="4187a-107">Если **секондсспеЦифиед** имеет **значение false** **, а** параметр **IsTrue имеет значение true**, то **SWbemDateTime. Seconds** содержит интервал.</span><span class="sxs-lookup"><span data-stu-id="4187a-107">If **SecondsSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Seconds** contains an interval.</span></span>

<span data-ttu-id="4187a-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4187a-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="4187a-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4187a-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4187a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4187a-110">Syntax</span></span>


```VB
SWbemDateTime.SecondsSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="4187a-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4187a-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="4187a-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="4187a-112">Examples</span></span>

<span data-ttu-id="4187a-113">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="4187a-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="4187a-114">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="4187a-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4187a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4187a-115">Requirements</span></span>



| <span data-ttu-id="4187a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4187a-116">Requirement</span></span> | <span data-ttu-id="4187a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4187a-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4187a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4187a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4187a-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4187a-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4187a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4187a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4187a-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4187a-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4187a-122">Header</span><span class="sxs-lookup"><span data-stu-id="4187a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4187a-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4187a-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4187a-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4187a-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="4187a-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4187a-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4187a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4187a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4187a-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4187a-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4187a-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="4187a-128">CLSID</span></span><br/>                    | <span data-ttu-id="4187a-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="4187a-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="4187a-130">IID</span><span class="sxs-lookup"><span data-stu-id="4187a-130">IID</span></span><br/>                      | <span data-ttu-id="4187a-131">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="4187a-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="4187a-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4187a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4187a-133">**SWbemDateTime. сек.**</span><span class="sxs-lookup"><span data-stu-id="4187a-133">**SWbemDateTime.Seconds**</span></span>](swbemdatetime-seconds.md)
</dt> <dt>

[<span data-ttu-id="4187a-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="4187a-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="4187a-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="4187a-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




