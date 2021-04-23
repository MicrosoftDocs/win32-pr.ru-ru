---
description: Возвращает или задает значение, представляющее компонент минут для значения DateTime.
ms.assetid: a52a66c2-f7ab-48d0-bdee-a07984ed3bc2
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. Minutes (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Minutes
- ISWbemDateTime.Minutes
- ISWbemDateTime.get_Minutes
- ISWbemDateTime.put_Minutes
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cce55d731916d0e8180de1bde495566d4ed22c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703256"
---
# <a name="swbemdatetimeminutes-property"></a><span data-ttu-id="519ae-103">SWbemDateTime. minutes, свойство</span><span class="sxs-lookup"><span data-stu-id="519ae-103">SWbemDateTime.Minutes property</span></span>

<span data-ttu-id="519ae-104">Свойство **minutes** объекта [**SWbemDateTime**](swbemdatetime.md) Возвращает или задает значение, представляющее компонент минут для значения DateTime.</span><span class="sxs-lookup"><span data-stu-id="519ae-104">The **Minutes** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the minutes component of the datetime value.</span></span>

<span data-ttu-id="519ae-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="519ae-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="519ae-106">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="519ae-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="519ae-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="519ae-107">Syntax</span></span>


```VB
SWbemDateTime.Minutes As Long
```



## <a name="property-value"></a><span data-ttu-id="519ae-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="519ae-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="519ae-109">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="519ae-109">Error codes</span></span>

<span data-ttu-id="519ae-110">После получения или задания свойства **minutes** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать приведенный ниже код ошибки.</span><span class="sxs-lookup"><span data-stu-id="519ae-110">After you get or set the **Minutes** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="519ae-111">**вбемеррвалуеаутофранже** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="519ae-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="519ae-112">Значение не находится в диапазоне от 0 до 59.</span><span class="sxs-lookup"><span data-stu-id="519ae-112">The value was not in the range of 0 through 59.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="519ae-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="519ae-113">Remarks</span></span>

<span data-ttu-id="519ae-114">Если свойство **SWbemDateTime. minutes** имеет значение 1, то свойство [**SWbemDateTime. Seconds**](swbemdatetime-seconds.md) содержит значение, которое смещается на одну секунду. ошибка округления, возникающая при преобразовании значения **DateTime** CIM в значение **\_ даты VT** .</span><span class="sxs-lookup"><span data-stu-id="519ae-114">If the **SWbemDateTime.Minutes** property is set to 1, then the [**SWbemDateTime.Seconds**](swbemdatetime-seconds.md) property contains a value that is offset by one second a rounding error that occurs when a CIM **datetime** value is translated to a **VT\_DATE** value.</span></span> <span data-ttu-id="519ae-115">Если вместо этого для свойства **minutes** задано значение 0, то свойство **Seconds** будет возвращать правильную величину.</span><span class="sxs-lookup"><span data-stu-id="519ae-115">If the **Minutes** property is set to 0 instead, then the **Seconds** property returns the correct value.</span></span>

## <a name="examples"></a><span data-ttu-id="519ae-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="519ae-116">Examples</span></span>

<span data-ttu-id="519ae-117">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="519ae-117">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="519ae-118">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="519ae-118">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="519ae-119">Требования</span><span class="sxs-lookup"><span data-stu-id="519ae-119">Requirements</span></span>



| <span data-ttu-id="519ae-120">Требование</span><span class="sxs-lookup"><span data-stu-id="519ae-120">Requirement</span></span> | <span data-ttu-id="519ae-121">Значение</span><span class="sxs-lookup"><span data-stu-id="519ae-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="519ae-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="519ae-122">Minimum supported client</span></span><br/> | <span data-ttu-id="519ae-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="519ae-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="519ae-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="519ae-124">Minimum supported server</span></span><br/> | <span data-ttu-id="519ae-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="519ae-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="519ae-126">Header</span><span class="sxs-lookup"><span data-stu-id="519ae-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="519ae-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="519ae-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="519ae-128">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="519ae-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="519ae-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="519ae-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="519ae-130">DLL</span><span class="sxs-lookup"><span data-stu-id="519ae-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="519ae-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="519ae-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="519ae-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="519ae-132">CLSID</span></span><br/>                    | <span data-ttu-id="519ae-133">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="519ae-133">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="519ae-134">IID</span><span class="sxs-lookup"><span data-stu-id="519ae-134">IID</span></span><br/>                      | <span data-ttu-id="519ae-135">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="519ae-135">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="519ae-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="519ae-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="519ae-137">**SWbemDateTime. МинутесспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="519ae-137">**SWbemDateTime.MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
</dt> <dt>

[<span data-ttu-id="519ae-138">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="519ae-138">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="519ae-139">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="519ae-139">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

