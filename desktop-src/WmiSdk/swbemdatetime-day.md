---
description: Возвращает или задает значение, представляющее компонент дня значения DateTime.
ms.assetid: 60da99bc-560c-45bc-b787-f4bef8e5a509
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. Day (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Day
- ISWbemDateTime.Day
- ISWbemDateTime.get_Day
- ISWbemDateTime.put_Day
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1de77a8e5d616284c3dc13a19bce2526db371c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999371"
---
# <a name="swbemdatetimeday-property"></a><span data-ttu-id="1473b-103">SWbemDateTime. Day, свойство</span><span class="sxs-lookup"><span data-stu-id="1473b-103">SWbemDateTime.Day property</span></span>

<span data-ttu-id="1473b-104">Свойство **Day** объекта [**SWbemDateTime**](swbemdatetime.md) Возвращает или задает значение, представляющее компонент дня значения DateTime.</span><span class="sxs-lookup"><span data-stu-id="1473b-104">The **Day** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the day component of the datetime value.</span></span> <span data-ttu-id="1473b-105">Значение должно находиться в диапазоне от 1 до 31 [**, если**](swbemdatetime-isinterval.md) параметру IsFalse задано **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1473b-105">The value must be in the range of 1 through 31 if [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**.</span></span> <span data-ttu-id="1473b-106">Однако проверка ошибок не зависит от значения месяца.</span><span class="sxs-lookup"><span data-stu-id="1473b-106">However, error checking is not sensitive to the month value.</span></span> <span data-ttu-id="1473b-107">Таким словами, значение 31 в диапазоне не будет возвращать ошибку в случаях, когда значение [**SWbemDateTime. month**](swbemdatetime-month.md) составляет месяц менее 31 дня (Февраль, Апрель, Июнь, Сентябрь ноября).</span><span class="sxs-lookup"><span data-stu-id="1473b-107">Thus, the in-range value of 31 will not return an error in the cases where the [**SWbemDateTime.Month**](swbemdatetime-month.md) value is for a month of fewer than 31 days (February, April, June, September, November).</span></span>

<span data-ttu-id="1473b-108">Значение **дня** по умолчанию — 01.</span><span class="sxs-lookup"><span data-stu-id="1473b-108">The default value for **Day** is 01.</span></span>

<span data-ttu-id="1473b-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="1473b-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="1473b-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1473b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1473b-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1473b-111">Syntax</span></span>


```VB
SWbemDateTime.Day As Long
```



## <a name="property-value"></a><span data-ttu-id="1473b-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1473b-112">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="1473b-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="1473b-113">Error codes</span></span>

<span data-ttu-id="1473b-114">После получения или задания свойства **Day** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать приведенный ниже код ошибки.</span><span class="sxs-lookup"><span data-stu-id="1473b-114">After you get or set the **Day** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="1473b-115">**вбемеррвалуеаутофранже** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="1473b-115">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="1473b-116">Если [**параметр**](swbemdatetime-isinterval.md) IsTrue имеет **значение true** , а диапазон правильных значений превышает 0 – 99999999.</span><span class="sxs-lookup"><span data-stu-id="1473b-116">If [**IsInterval**](swbemdatetime-isinterval.md) is **TRUE** and the range of correct values exceeds 0 through 99999999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="1473b-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="1473b-117">Examples</span></span>

<span data-ttu-id="1473b-118">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="1473b-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="1473b-119">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="1473b-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1473b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="1473b-120">Requirements</span></span>



| <span data-ttu-id="1473b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="1473b-121">Requirement</span></span> | <span data-ttu-id="1473b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1473b-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1473b-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1473b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1473b-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1473b-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1473b-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1473b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1473b-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1473b-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1473b-127">Header</span><span class="sxs-lookup"><span data-stu-id="1473b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1473b-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1473b-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1473b-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1473b-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="1473b-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1473b-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1473b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1473b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1473b-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1473b-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1473b-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="1473b-133">CLSID</span></span><br/>                    | <span data-ttu-id="1473b-134">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="1473b-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="1473b-135">IID</span><span class="sxs-lookup"><span data-stu-id="1473b-135">IID</span></span><br/>                      | <span data-ttu-id="1473b-136">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="1473b-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="1473b-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1473b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1473b-138">**SWbemDateTime. ДайспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="1473b-138">**SWbemDateTime.DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
</dt> <dt>

[<span data-ttu-id="1473b-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="1473b-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="1473b-140">DATETIME</span><span class="sxs-lookup"><span data-stu-id="1473b-140">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

