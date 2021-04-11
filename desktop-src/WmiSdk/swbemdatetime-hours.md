---
description: Возвращает или задает значение, представляющее компонент часов значения DateTime.
ms.assetid: 83f084fa-57a5-4467-acea-7e19de82a91f
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. Hours (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Hours
- ISWbemDateTime.Hours
- ISWbemDateTime.get_Hours
- ISWbemDateTime.put_Hours
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 27edb3c209e2e95ae7aff20930d260f8f6d44427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272215"
---
# <a name="swbemdatetimehours-property"></a><span data-ttu-id="4b4fa-103">SWbemDateTime. hours, свойство</span><span class="sxs-lookup"><span data-stu-id="4b4fa-103">SWbemDateTime.Hours property</span></span>

<span data-ttu-id="4b4fa-104">Свойство **hours** объекта [**SWbemDateTime**](swbemdatetime.md) Возвращает или задает значение, представляющее компонент часов для значения DateTime.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-104">The **Hours** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the hours component of the datetime value.</span></span>

<span data-ttu-id="4b4fa-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4b4fa-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="4b4fa-106">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b4fa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b4fa-107">Syntax</span></span>


```VB
SWbemDateTime.Hours As Long
```



## <a name="property-value"></a><span data-ttu-id="4b4fa-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4b4fa-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="4b4fa-109">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4b4fa-109">Error codes</span></span>

<span data-ttu-id="4b4fa-110">После получения или задания свойства **hours** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать приведенный ниже код ошибки.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-110">After you get or set the **Hours** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="4b4fa-111">**вбемеррвалуеаутофранже** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="4b4fa-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="4b4fa-112">Значение не находится в диапазоне от 0 до 23.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-112">The value was not in the range of 0 through 23.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="4b4fa-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="4b4fa-113">Examples</span></span>

<span data-ttu-id="4b4fa-114">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="4b4fa-114">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="4b4fa-115">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="4b4fa-115">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b4fa-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4b4fa-116">Requirements</span></span>



| <span data-ttu-id="4b4fa-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4b4fa-117">Requirement</span></span> | <span data-ttu-id="4b4fa-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4b4fa-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b4fa-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b4fa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4b4fa-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b4fa-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4b4fa-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b4fa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4b4fa-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b4fa-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4b4fa-123">Header</span><span class="sxs-lookup"><span data-stu-id="4b4fa-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b4fa-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b4fa-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4b4fa-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4b4fa-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="4b4fa-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4b4fa-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4b4fa-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4b4fa-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b4fa-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b4fa-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4b4fa-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="4b4fa-129">CLSID</span></span><br/>                    | <span data-ttu-id="4b4fa-130">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="4b4fa-130">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="4b4fa-131">IID</span><span class="sxs-lookup"><span data-stu-id="4b4fa-131">IID</span></span><br/>                      | <span data-ttu-id="4b4fa-132">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="4b4fa-132">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="4b4fa-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b4fa-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b4fa-134">**SWbemDateTime. ХаурсспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="4b4fa-134">**SWbemDateTime.HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
</dt> <dt>

[<span data-ttu-id="4b4fa-135">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="4b4fa-135">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="4b4fa-136">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="4b4fa-136">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

