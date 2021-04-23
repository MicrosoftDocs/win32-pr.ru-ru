---
description: Возвращает или задает значение, представляющее компонент года значения DATETIME.
ms.assetid: eab3738a-c92a-4602-b1ee-e2547da88308
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. Year (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Year
- ISWbemDateTime.Year
- ISWbemDateTime.get_Year
- ISWbemDateTime.put_Year
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5fe8988b3772f0f5d976c38eb5e9cc44fb9c4ede
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702746"
---
# <a name="swbemdatetimeyear-property"></a><span data-ttu-id="5f9e6-103">SWbemDateTime. year, свойство</span><span class="sxs-lookup"><span data-stu-id="5f9e6-103">SWbemDateTime.Year property</span></span>

<span data-ttu-id="5f9e6-104">Свойство **year** объекта [**SWbemDateTime**](swbemdatetime.md) Возвращает или задает значение, представляющее компонент года для значения [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="5f9e6-104">The **Year** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the year component of the [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="5f9e6-105">Значение должно быть в диапазоне от 0000-9999 или возвращена ошибка Вбемеррвалуеаутофранже.</span><span class="sxs-lookup"><span data-stu-id="5f9e6-105">The value must be in the range of 0000 - 9999 or the error wbemErrValueOutOfRange is returned.</span></span>

<span data-ttu-id="5f9e6-106">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5f9e6-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="5f9e6-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5f9e6-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f9e6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f9e6-108">Syntax</span></span>


```VB
SWbemDateTime.Year As Long
```



## <a name="property-value"></a><span data-ttu-id="5f9e6-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5f9e6-109">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="5f9e6-110">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="5f9e6-110">Error codes</span></span>

<span data-ttu-id="5f9e6-111">После получения или задания свойства **year** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать приведенный ниже код ошибки.</span><span class="sxs-lookup"><span data-stu-id="5f9e6-111">After you get or set the **Year** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="5f9e6-112">**вбемеррвалуеаутофранже** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="5f9e6-112">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="5f9e6-113">Значение не находится в диапазоне от 0000 до 9999.</span><span class="sxs-lookup"><span data-stu-id="5f9e6-113">The value was not in the range of 0000 through 9999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="5f9e6-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="5f9e6-114">Examples</span></span>

<span data-ttu-id="5f9e6-115">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="5f9e6-115">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="5f9e6-116">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="5f9e6-116">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f9e6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5f9e6-117">Requirements</span></span>



| <span data-ttu-id="5f9e6-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5f9e6-118">Requirement</span></span> | <span data-ttu-id="5f9e6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5f9e6-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f9e6-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5f9e6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5f9e6-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f9e6-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5f9e6-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5f9e6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5f9e6-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f9e6-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5f9e6-124">Header</span><span class="sxs-lookup"><span data-stu-id="5f9e6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f9e6-125"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f9e6-125"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f9e6-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5f9e6-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="5f9e6-127"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5f9e6-127"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5f9e6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5f9e6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f9e6-129"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f9e6-129"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5f9e6-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="5f9e6-130">CLSID</span></span><br/>                    | <span data-ttu-id="5f9e6-131">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="5f9e6-131">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="5f9e6-132">IID</span><span class="sxs-lookup"><span data-stu-id="5f9e6-132">IID</span></span><br/>                      | <span data-ttu-id="5f9e6-133">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="5f9e6-133">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="5f9e6-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f9e6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f9e6-135">**SWbemDateTime. ЕарспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="5f9e6-135">**SWbemDateTime.YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
</dt> <dt>

[<span data-ttu-id="5f9e6-136">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="5f9e6-136">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="5f9e6-137">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="5f9e6-137">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

