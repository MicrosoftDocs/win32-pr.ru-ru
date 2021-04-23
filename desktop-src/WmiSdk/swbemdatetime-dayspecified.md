---
description: Логическое значение, указывающее, содержит ли компонент дня в значении DATETIME CIM интервал или значение с подстановочным знаком.
ms.assetid: a713378b-3953-49d8-9c6a-44aa9337eae2
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. ДайспеЦифиед (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.DaySpecified
- ISWbemDateTime.DaySpecified
- ISWbemDateTime.get_DaySpecified
- ISWbemDateTime.put_DaySpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f295d33940f36212fde4fe821af8d5df24d4f75f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711653"
---
# <a name="swbemdatetimedayspecified-property"></a><span data-ttu-id="11046-103">SWbemDateTime. ДайспеЦифиед, свойство</span><span class="sxs-lookup"><span data-stu-id="11046-103">SWbemDateTime.DaySpecified property</span></span>

<span data-ttu-id="11046-104">Свойство **дайспеЦифиед** объекта [**SWbemDateTime**](swbemdatetime.md) является логическим значением, указывающим, содержит ли компонент дня в значении [**DateTime**](datetime.md) CIM интервал или значение с подстановочным знаком.</span><span class="sxs-lookup"><span data-stu-id="11046-104">The **DaySpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the day component in the CIM [**DATETIME**](datetime.md) value contains an interval or a wildcard value.</span></span> <span data-ttu-id="11046-105">Если **дайспеЦифиед** имеет значение true [**, а параметр**](swbemdatetime-isinterval.md) **IsTrue** имеет значение **false**, то [**SWbemDateTime. Day**](swbemdatetime-day.md) содержит значение DateTime.</span><span class="sxs-lookup"><span data-stu-id="11046-105">If **DaySpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Day**](swbemdatetime-day.md) contains a datetime value.</span></span> <span data-ttu-id="11046-106">Значение [**DateTime**](datetime.md) , содержащее интервал, не может быть преобразовано в формат **\_ даты VT** или **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="11046-106">A [**DATETIME**](datetime.md) value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="11046-107">Если **дайспеЦифиед** имеет **значение false** **, а** параметр **IsTrue имеет значение true**, то **SWbemDateTime. Day** содержит интервал.</span><span class="sxs-lookup"><span data-stu-id="11046-107">If **DaySpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Day** contains an interval.</span></span>

<span data-ttu-id="11046-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="11046-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="11046-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="11046-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="11046-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11046-110">Syntax</span></span>


```VB
SWbemDateTime.DaySpecified As BOOLEAN
```



## <a name="property-value"></a><span data-ttu-id="11046-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="11046-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="11046-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="11046-112">Examples</span></span>

<span data-ttu-id="11046-113">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="11046-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="11046-114">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="11046-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11046-115">Требования</span><span class="sxs-lookup"><span data-stu-id="11046-115">Requirements</span></span>



| <span data-ttu-id="11046-116">Требование</span><span class="sxs-lookup"><span data-stu-id="11046-116">Requirement</span></span> | <span data-ttu-id="11046-117">Значение</span><span class="sxs-lookup"><span data-stu-id="11046-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11046-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11046-118">Minimum supported client</span></span><br/> | <span data-ttu-id="11046-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11046-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="11046-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11046-120">Minimum supported server</span></span><br/> | <span data-ttu-id="11046-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11046-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="11046-122">Header</span><span class="sxs-lookup"><span data-stu-id="11046-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="11046-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="11046-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="11046-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="11046-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="11046-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="11046-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="11046-126">DLL</span><span class="sxs-lookup"><span data-stu-id="11046-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11046-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11046-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="11046-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="11046-128">CLSID</span></span><br/>                    | <span data-ttu-id="11046-129">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="11046-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="11046-130">IID</span><span class="sxs-lookup"><span data-stu-id="11046-130">IID</span></span><br/>                      | <span data-ttu-id="11046-131">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="11046-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="11046-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11046-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11046-133">**SWbemDateTime. Day**</span><span class="sxs-lookup"><span data-stu-id="11046-133">**SWbemDateTime.Day**</span></span>](swbemdatetime-day.md)
</dt> <dt>

[<span data-ttu-id="11046-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="11046-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="11046-135">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="11046-135">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

 




