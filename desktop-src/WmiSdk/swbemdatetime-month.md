---
description: Возвращает или задает значение, представляющее компонент месяца для значения DateTime.
ms.assetid: 05818f0a-7e15-4ddd-a6a7-9d16ae82cd3c
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. month (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Month
- ISWbemDateTime.Month
- ISWbemDateTime.get_Month
- ISWbemDateTime.put_Month
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 73769d73cffc5b9731cfd55785e2fa087182b33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703255"
---
# <a name="swbemdatetimemonth-property"></a><span data-ttu-id="c5bf8-103">SWbemDateTime. month, свойство</span><span class="sxs-lookup"><span data-stu-id="c5bf8-103">SWbemDateTime.Month property</span></span>

<span data-ttu-id="c5bf8-104">Свойство **Month** объекта [**SWbemDateTime**](swbemdatetime.md) Возвращает или задает значение, представляющее компонент месяца для значения DateTime.</span><span class="sxs-lookup"><span data-stu-id="c5bf8-104">The **Month** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the month component of the datetime value.</span></span> <span data-ttu-id="c5bf8-105">Число должно быть в диапазоне от 01 до 12 или возвращена ошибка **вбемвалуеаутофранже** .</span><span class="sxs-lookup"><span data-stu-id="c5bf8-105">The number must be in the range of 01 through 12 or the error **wbemValueOutOfRange** is returned.</span></span>

<span data-ttu-id="c5bf8-106">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c5bf8-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="c5bf8-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c5bf8-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5bf8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5bf8-108">Syntax</span></span>


```VB
SWbemDateTime.Month As Long
```



## <a name="property-value"></a><span data-ttu-id="c5bf8-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c5bf8-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="c5bf8-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="c5bf8-110">Examples</span></span>

<span data-ttu-id="c5bf8-111">Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="c5bf8-111">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="c5bf8-112">Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="c5bf8-112">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5bf8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c5bf8-113">Requirements</span></span>



| <span data-ttu-id="c5bf8-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c5bf8-114">Requirement</span></span> | <span data-ttu-id="c5bf8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c5bf8-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5bf8-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5bf8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c5bf8-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5bf8-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c5bf8-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5bf8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c5bf8-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5bf8-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c5bf8-120">Header</span><span class="sxs-lookup"><span data-stu-id="c5bf8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5bf8-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5bf8-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5bf8-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c5bf8-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="c5bf8-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c5bf8-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c5bf8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c5bf8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5bf8-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5bf8-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c5bf8-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="c5bf8-126">CLSID</span></span><br/>                    | <span data-ttu-id="c5bf8-127">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="c5bf8-127">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="c5bf8-128">IID</span><span class="sxs-lookup"><span data-stu-id="c5bf8-128">IID</span></span><br/>                      | <span data-ttu-id="c5bf8-129">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="c5bf8-129">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="c5bf8-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5bf8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5bf8-131">**SWbemDateTime. МонсспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="c5bf8-131">**SWbemDateTime.MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
</dt> <dt>

[<span data-ttu-id="c5bf8-132">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="c5bf8-132">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="c5bf8-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="c5bf8-133">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




