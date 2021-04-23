---
description: Логическое значение, указывающее, содержит ли компонент year в значении DateTime CIM интервал или значение с подстановочным знаком.
ms.assetid: afac0a08-7bd0-42f1-b5a7-8664f9db8615
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. ЕарспеЦифиед (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.YearSpecified
- ISWbemDateTime.YearSpecified
- ISWbemDateTime.get_YearSpecified
- ISWbemDateTime.put_YearSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3ad6ae5b120c2b38d7b6170951ef30b3b19f5295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701973"
---
# <a name="swbemdatetimeyearspecified-property"></a><span data-ttu-id="94df6-103">SWbemDateTime. ЕарспеЦифиед, свойство</span><span class="sxs-lookup"><span data-stu-id="94df6-103">SWbemDateTime.YearSpecified property</span></span>

<span data-ttu-id="94df6-104">Свойство **еарспеЦифиед** объекта [**SWbemDateTime**](swbemdatetime.md) является логическим значением, указывающим, содержит ли компонент year в значении DateTime CIM интервал или значение с подстановочным знаком.</span><span class="sxs-lookup"><span data-stu-id="94df6-104">The **YearSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the year component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="94df6-105">Если **еарспеЦифиед** имеет значение true [**, а параметр**](swbemdatetime-isinterval.md) **IsTrue** имеет значение **false**, то [**SWbemDateTime. Year**](swbemdatetime-year.md) содержит значение DateTime.</span><span class="sxs-lookup"><span data-stu-id="94df6-105">If **YearSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Year**](swbemdatetime-year.md) contains a datetime value.</span></span> <span data-ttu-id="94df6-106">Значение DateTime, содержащее интервал, не может быть преобразовано в формат **\_ даты VT** или **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="94df6-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="94df6-107">Если **еарспеЦифиед** имеет **значение false** **, а** параметр **IsTrue имеет значение true**, то **SWbemDateTime. Year** содержит интервал.</span><span class="sxs-lookup"><span data-stu-id="94df6-107">If **YearSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Year** contains an interval.</span></span>

<span data-ttu-id="94df6-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="94df6-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="94df6-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="94df6-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="94df6-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94df6-110">Syntax</span></span>


```VB
SWbemDateTime.YearSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="94df6-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="94df6-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="94df6-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="94df6-112">Examples</span></span>

<span data-ttu-id="94df6-113">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="94df6-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="94df6-114">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="94df6-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94df6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="94df6-115">Requirements</span></span>



| <span data-ttu-id="94df6-116">Требование</span><span class="sxs-lookup"><span data-stu-id="94df6-116">Requirement</span></span> | <span data-ttu-id="94df6-117">Значение</span><span class="sxs-lookup"><span data-stu-id="94df6-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94df6-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94df6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="94df6-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94df6-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94df6-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94df6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="94df6-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94df6-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94df6-122">Header</span><span class="sxs-lookup"><span data-stu-id="94df6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="94df6-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="94df6-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="94df6-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="94df6-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="94df6-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="94df6-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="94df6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="94df6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94df6-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94df6-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="94df6-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="94df6-128">CLSID</span></span><br/>                    | <span data-ttu-id="94df6-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="94df6-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="94df6-130">IID</span><span class="sxs-lookup"><span data-stu-id="94df6-130">IID</span></span><br/>                      | <span data-ttu-id="94df6-131">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="94df6-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="94df6-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94df6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94df6-133">**SWbemDateTime. год**</span><span class="sxs-lookup"><span data-stu-id="94df6-133">**SWbemDateTime.Year**</span></span>](swbemdatetime-year.md)
</dt> <dt>

[<span data-ttu-id="94df6-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="94df6-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="94df6-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="94df6-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




