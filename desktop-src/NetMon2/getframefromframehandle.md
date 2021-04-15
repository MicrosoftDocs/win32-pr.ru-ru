---
description: Функция Жетфрамефромфрамехандле возвращает указатель на кадр из маркера кадра.
ms.assetid: 790fe5fe-a857-4947-a471-d0538c0f0d61
title: Функция Жетфрамефромфрамехандле (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameFromFrameHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ce8151b2f4c81c61dea5969ff52e9ddf2d6615a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662188"
---
# <a name="getframefromframehandle-function"></a><span data-ttu-id="0916a-103">Функция Жетфрамефромфрамехандле</span><span class="sxs-lookup"><span data-stu-id="0916a-103">GetFrameFromFrameHandle function</span></span>

<span data-ttu-id="0916a-104">Функция **жетфрамефромфрамехандле** возвращает указатель на кадр из маркера кадра.</span><span class="sxs-lookup"><span data-stu-id="0916a-104">The **GetFrameFromFrameHandle** function returns a pointer to a frame from a frame handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="0916a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0916a-105">Syntax</span></span>


```C++
ULPFRAME WINAPI GetFrameFromFrameHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="0916a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0916a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0916a-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0916a-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0916a-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="0916a-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0916a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0916a-109">Return value</span></span>

<span data-ttu-id="0916a-110">Если функция выполнена успешно, возвращаемое значение является указателем на кадр.</span><span class="sxs-lookup"><span data-stu-id="0916a-110">If the function is successful, the return value is a pointer to the frame.</span></span>

<span data-ttu-id="0916a-111">Если функция завершается неудачно, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="0916a-111">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="0916a-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0916a-112">Remarks</span></span>

<span data-ttu-id="0916a-113">Функция **жетфрамефромфрамехандле** извлекает данные, которые не могут быть извлечены другими вспомогательными функциями, предоставляемыми сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="0916a-113">The **GetFrameFromFrameHandle** function retrieves data that cannot be retrieved by the other helper functions that Network Monitor provides.</span></span> <span data-ttu-id="0916a-114">При возможности используйте следующие функции.</span><span class="sxs-lookup"><span data-stu-id="0916a-114">Use the following functions whenever possible.</span></span>

<dl>

[<span data-ttu-id="0916a-115">**жетфрамедстаддрессоффсет**</span><span class="sxs-lookup"><span data-stu-id="0916a-115">**GetFrameDstAddressOffset**</span></span>](getframedstaddressoffset.md)  
[<span data-ttu-id="0916a-116">**жетфрамесркаддрессоффсет**</span><span class="sxs-lookup"><span data-stu-id="0916a-116">**GetFrameSrcAddressOffset**</span></span>](getframesrcaddressoffset.md)  
[<span data-ttu-id="0916a-117">**жетфрамекаптурехандле**</span><span class="sxs-lookup"><span data-stu-id="0916a-117">**GetFrameCaptureHandle**</span></span>](getframecapturehandle.md)  
[<span data-ttu-id="0916a-118">**жетфрамедестаддресс**</span><span class="sxs-lookup"><span data-stu-id="0916a-118">**GetFrameDestAddress**</span></span>](getframedestaddress.md)  
[<span data-ttu-id="0916a-119">**жетфрамесаурцеаддресс**</span><span class="sxs-lookup"><span data-stu-id="0916a-119">**GetFrameSourceAddress**</span></span>](getframesourceaddress.md)  
[<span data-ttu-id="0916a-120">**жетфрамемачеадерленгс**</span><span class="sxs-lookup"><span data-stu-id="0916a-120">**GetFrameMacHeaderLength**</span></span>](getframemacheaderlength.md)  
[<span data-ttu-id="0916a-121">**жетфрамеленгс**</span><span class="sxs-lookup"><span data-stu-id="0916a-121">**GetFrameLength**</span></span>](getframelength.md)  
[<span data-ttu-id="0916a-122">**жетфраместоредленгс**</span><span class="sxs-lookup"><span data-stu-id="0916a-122">**GetFrameStoredLength**</span></span>](getframestoredlength.md)  
[<span data-ttu-id="0916a-123">**жетфрамемактипе**</span><span class="sxs-lookup"><span data-stu-id="0916a-123">**GetFrameMacType**</span></span>](getframemactype.md)  
[<span data-ttu-id="0916a-124">**жетфраменумбер**</span><span class="sxs-lookup"><span data-stu-id="0916a-124">**GetFrameNumber**</span></span>](getframenumber.md)  
[<span data-ttu-id="0916a-125">**жетфраметиместамп**</span><span class="sxs-lookup"><span data-stu-id="0916a-125">**GetFrameTimeStamp**</span></span>](getframetimestamp.md)  
</dl>

<span data-ttu-id="0916a-126">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетфрамефромфрамехандле** .</span><span class="sxs-lookup"><span data-stu-id="0916a-126">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameFromFrameHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0916a-127">Требования</span><span class="sxs-lookup"><span data-stu-id="0916a-127">Requirements</span></span>



| <span data-ttu-id="0916a-128">Требование</span><span class="sxs-lookup"><span data-stu-id="0916a-128">Requirement</span></span> | <span data-ttu-id="0916a-129">Значение</span><span class="sxs-lookup"><span data-stu-id="0916a-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0916a-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0916a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0916a-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0916a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0916a-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0916a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0916a-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0916a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0916a-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0916a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0916a-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0916a-135"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="0916a-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0916a-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="0916a-137"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0916a-137"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0916a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0916a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0916a-139"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0916a-139"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




