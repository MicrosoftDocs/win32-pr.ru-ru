---
description: Логическое значение, указывающее, содержит ли компонент универсального скоординированного времени (UTC) в значении DateTime CIM интервал или значение с подстановочным знаком.
ms.assetid: 9cb04351-294b-48ba-8d1c-2f28cb9ce463
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. УткспеЦифиед (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTCSpecified
- ISWbemDateTime.UTCSpecified
- ISWbemDateTime.get_UTCSpecified
- ISWbemDateTime.put_UTCSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2ada5bbbfa68e6cb63c0e060d6c3a12c0f771a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702554"
---
# <a name="swbemdatetimeutcspecified-property"></a><span data-ttu-id="049d9-103">SWbemDateTime. УткспеЦифиед, свойство</span><span class="sxs-lookup"><span data-stu-id="049d9-103">SWbemDateTime.UTCSpecified property</span></span>

<span data-ttu-id="049d9-104">Свойство **уткспеЦифиед** объекта [**SWbemDateTime**](swbemdatetime.md) является логическим значением, указывающим, содержит ли компонент универсального скоординированного времени (UTC) в значении DateTime CIM интервал или значение с подстановочным знаком.</span><span class="sxs-lookup"><span data-stu-id="049d9-104">The **UTCSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the Universal Coordinated Time (UTC) component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="049d9-105">Если **уткспеЦифиед** имеет значение true [**, а параметр**](swbemdatetime-isinterval.md) **IsTrue** имеет значение **false**, то [**SWbemDateTime. UTC**](swbemdatetime-utc.md) содержит значение [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="049d9-105">If **UTCSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.UTC**](swbemdatetime-utc.md) contains a [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="049d9-106">Значение **DateTime** , содержащее интервал, не может быть преобразовано в формат **\_ даты VT** или **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="049d9-106">A **DATETIME** value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="049d9-107">Если **уткспеЦифиед** имеет **значение false** **, а** параметр **IsTrue имеет значение true**, то **SWbemDateTime. UTC** содержит интервал.</span><span class="sxs-lookup"><span data-stu-id="049d9-107">If **UTCSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.UTC** contains an interval.</span></span>

<span data-ttu-id="049d9-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="049d9-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="049d9-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="049d9-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="049d9-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="049d9-110">Syntax</span></span>


```VB
SWbemDateTime.UTCSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="049d9-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="049d9-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="049d9-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="049d9-112">Examples</span></span>

<span data-ttu-id="049d9-113">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="049d9-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="049d9-114">Описание формата DateTime в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="049d9-114">For a description of the CIM datetime format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="049d9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="049d9-115">Requirements</span></span>



| <span data-ttu-id="049d9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="049d9-116">Requirement</span></span> | <span data-ttu-id="049d9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="049d9-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="049d9-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="049d9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="049d9-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="049d9-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="049d9-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="049d9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="049d9-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="049d9-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="049d9-122">Header</span><span class="sxs-lookup"><span data-stu-id="049d9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="049d9-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="049d9-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="049d9-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="049d9-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="049d9-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="049d9-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="049d9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="049d9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="049d9-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="049d9-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="049d9-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="049d9-128">CLSID</span></span><br/>                    | <span data-ttu-id="049d9-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="049d9-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="049d9-130">IID</span><span class="sxs-lookup"><span data-stu-id="049d9-130">IID</span></span><br/>                      | <span data-ttu-id="049d9-131">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="049d9-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="049d9-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="049d9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="049d9-133">**SWbemDateTime. UTC**</span><span class="sxs-lookup"><span data-stu-id="049d9-133">**SWbemDateTime.UTC**</span></span>](swbemdatetime-utc.md)
</dt> <dt>

[<span data-ttu-id="049d9-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="049d9-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="049d9-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="049d9-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




