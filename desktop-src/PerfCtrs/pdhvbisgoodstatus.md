---
description: Функция Пдхвбисгудстатус проверяет значение состояния, чтобы определить, является ли это кодом успешного или неудачи. Если значение Status является успешным, то возвращаемое значение будет ненулевым. Если это код состояния сбоя, возвращаемое значение будет равно нулю.
ms.assetid: bdca8f64-5dcd-4ecb-ba95-72f7a56c0439
title: Функция Пдхвбисгудстатус
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbIsGoodStatus
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: d21686be0398a84a57a303ad816b8a25f50aa611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663213"
---
# <a name="pdhvbisgoodstatus-function"></a><span data-ttu-id="21edd-105">Функция Пдхвбисгудстатус</span><span class="sxs-lookup"><span data-stu-id="21edd-105">PdhVbIsGoodStatus function</span></span>

<span data-ttu-id="21edd-106">Функция **пдхвбисгудстатус** проверяет значение состояния, чтобы определить, является ли это кодом успешного или неудачи.</span><span class="sxs-lookup"><span data-stu-id="21edd-106">The **PdhVbIsGoodStatus** function tests a status value to determine if it is a success or failure code.</span></span> <span data-ttu-id="21edd-107">Если значение Status является успешным, то возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="21edd-107">If the status value is a successful one, then the return value will be nonzero.</span></span> <span data-ttu-id="21edd-108">Если это код состояния сбоя, возвращаемое значение будет равно нулю.</span><span class="sxs-lookup"><span data-stu-id="21edd-108">If it is a failure status code, the return value will be zero.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="21edd-109">Функция, описанная в этом разделе, может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="21edd-109">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="21edd-110">Вместо этого корпорация Майкрософт рекомендует использовать функции, описанные в разделе [функции счетчиков производительности](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="21edd-110">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="21edd-111">Функция Пдхвбисгудстатус ( \_ ByVal Статусвалуе как long \_ )</span><span class="sxs-lookup"><span data-stu-id="21edd-111">Function PdhVbIsGoodStatus( \_ ByVal StatusValue As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="21edd-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="21edd-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21edd-113">*статусвалуе*</span><span class="sxs-lookup"><span data-stu-id="21edd-113">*StatusValue*</span></span> 
</dt> <dd>

<span data-ttu-id="21edd-114">Значение состояния, возвращаемое другой функцией PDH, которая должна быть протестирована.</span><span class="sxs-lookup"><span data-stu-id="21edd-114">Status value returned by another PDH function that is to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21edd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21edd-115">Return value</span></span>

<span data-ttu-id="21edd-116">Функция возвращает нуль, если код состояния является кодом состояния сбоя.</span><span class="sxs-lookup"><span data-stu-id="21edd-116">The function returns zero if the status code is a failure status code.</span></span> <span data-ttu-id="21edd-117">Он возвращает ненулевое значение, если код состояния является кодом состояния успеха.</span><span class="sxs-lookup"><span data-stu-id="21edd-117">It returns nonzero if the status code is a success status code.</span></span>

## <a name="requirements"></a><span data-ttu-id="21edd-118">Требования</span><span class="sxs-lookup"><span data-stu-id="21edd-118">Requirements</span></span>



| <span data-ttu-id="21edd-119">Требование</span><span class="sxs-lookup"><span data-stu-id="21edd-119">Requirement</span></span> | <span data-ttu-id="21edd-120">Значение</span><span class="sxs-lookup"><span data-stu-id="21edd-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="21edd-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="21edd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="21edd-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="21edd-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="21edd-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="21edd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="21edd-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="21edd-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="21edd-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="21edd-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="21edd-126"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21edd-126"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="21edd-127">DLL</span><span class="sxs-lookup"><span data-stu-id="21edd-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21edd-128"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21edd-128"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21edd-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21edd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21edd-130">**пдхвбжетдаублекаунтервалуе**</span><span class="sxs-lookup"><span data-stu-id="21edd-130">**PdhVbGetDoubleCounterValue**</span></span>](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




