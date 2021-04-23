---
description: Возвращает или задает значение, представляющее компонент секунд значения DateTime.
ms.assetid: 194d4309-6abf-4c5f-99f8-60d2c835af6c
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. Seconds (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Seconds
- ISWbemDateTime.Seconds
- ISWbemDateTime.get_Seconds
- ISWbemDateTime.put_Seconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0ef4ef15f13bf3d8dfc9272b2a3b734c3678f8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711649"
---
# <a name="swbemdatetimeseconds-property"></a><span data-ttu-id="46adf-103">SWbemDateTime. Seconds, свойство</span><span class="sxs-lookup"><span data-stu-id="46adf-103">SWbemDateTime.Seconds property</span></span>

<span data-ttu-id="46adf-104">Свойство **Seconds** объекта [**SWbemDateTime**](swbemdatetime.md) Возвращает или задает значение, представляющее компонент секунд значения DateTime.</span><span class="sxs-lookup"><span data-stu-id="46adf-104">The **Seconds** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the seconds component of the datetime value.</span></span>

<span data-ttu-id="46adf-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="46adf-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="46adf-106">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="46adf-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="46adf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46adf-107">Syntax</span></span>


```VB
SWbemDateTime.Seconds As Long
```



## <a name="property-value"></a><span data-ttu-id="46adf-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="46adf-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="46adf-109">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="46adf-109">Error codes</span></span>

<span data-ttu-id="46adf-110">После получения или задания свойства **Seconds** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать приведенный ниже код ошибки.</span><span class="sxs-lookup"><span data-stu-id="46adf-110">After you get or set the **Seconds** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="46adf-111">**вбемеррвалуеаутофранже** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="46adf-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="46adf-112">Значение не находится в диапазоне от 0 до 59.</span><span class="sxs-lookup"><span data-stu-id="46adf-112">The value was not in the range of 0 through 59.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46adf-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46adf-113">Remarks</span></span>

<span data-ttu-id="46adf-114">Свойство **SWbemDateTime. Seconds** может содержать неверное значение, если свойство [**SWbemDateTime. minutes**](swbemdatetime-minutes.md) установлено в значение 1.</span><span class="sxs-lookup"><span data-stu-id="46adf-114">The **SWbemDateTime.Seconds** property may contain an incorrect value if the [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) property has been set to 1.</span></span> <span data-ttu-id="46adf-115">Он содержит значение, которое смещается на одну секунду из-за ошибки округления, возникающей при преобразовании значения [**DateTime**](datetime.md) CIM в значение **\_ даты VT** .</span><span class="sxs-lookup"><span data-stu-id="46adf-115">It contains a value that is offset by one second because of a rounding error that occurs when a CIM [**DATETIME**](datetime.md) value is translated to a **VT\_DATE** value.</span></span> <span data-ttu-id="46adf-116">Если вместо значения свойства **minutes** задано значение 0 (ноль), то свойство **Seconds** будет возвращать правильную величину.</span><span class="sxs-lookup"><span data-stu-id="46adf-116">If the **Minutes** property is set to 0 (zero) instead, then the **Seconds** property returns the correct value.</span></span>

## <a name="examples"></a><span data-ttu-id="46adf-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="46adf-117">Examples</span></span>

<span data-ttu-id="46adf-118">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="46adf-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="46adf-119">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="46adf-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46adf-120">Требования</span><span class="sxs-lookup"><span data-stu-id="46adf-120">Requirements</span></span>



| <span data-ttu-id="46adf-121">Требование</span><span class="sxs-lookup"><span data-stu-id="46adf-121">Requirement</span></span> | <span data-ttu-id="46adf-122">Значение</span><span class="sxs-lookup"><span data-stu-id="46adf-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46adf-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46adf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="46adf-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46adf-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46adf-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46adf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="46adf-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46adf-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46adf-127">Header</span><span class="sxs-lookup"><span data-stu-id="46adf-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="46adf-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="46adf-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="46adf-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="46adf-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="46adf-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="46adf-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="46adf-131">DLL</span><span class="sxs-lookup"><span data-stu-id="46adf-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46adf-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46adf-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="46adf-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="46adf-133">CLSID</span></span><br/>                    | <span data-ttu-id="46adf-134">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="46adf-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="46adf-135">IID</span><span class="sxs-lookup"><span data-stu-id="46adf-135">IID</span></span><br/>                      | <span data-ttu-id="46adf-136">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="46adf-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="46adf-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46adf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46adf-138">**SWbemDateTime. СекондсспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="46adf-138">**SWbemDateTime.SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
</dt> <dt>

[<span data-ttu-id="46adf-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="46adf-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="46adf-140">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="46adf-140">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

