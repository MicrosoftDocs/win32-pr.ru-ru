---
description: Возвращает указатель на комментарий записи.
ms.assetid: 3ef5c5b3-5586-469f-8975-049713715403
title: Функция Жеткаптурекоммент (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureComment
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ca2d3dd3fdc91c54c49b12119a56180396df5ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662191"
---
# <a name="getcapturecomment-function"></a><span data-ttu-id="9645d-103">Функция Жеткаптурекоммент</span><span class="sxs-lookup"><span data-stu-id="9645d-103">GetCaptureComment function</span></span>

<span data-ttu-id="9645d-104">Функция **жеткаптурекоммент** возвращает указатель на комментарий записи.</span><span class="sxs-lookup"><span data-stu-id="9645d-104">The **GetCaptureComment** function returns a pointer to the comment of a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="9645d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9645d-105">Syntax</span></span>


```C++
LPSTR WINAPI GetCaptureComment(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="9645d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9645d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9645d-107">*хкаптуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9645d-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9645d-108">Маркер записи.</span><span class="sxs-lookup"><span data-stu-id="9645d-108">A handle to the capture.</span></span> <span data-ttu-id="9645d-109">Дополнительные сведения о получении маркера записи см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="9645d-109">For more information about obtaining the capture handle, see the Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9645d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9645d-110">Return value</span></span>

<span data-ttu-id="9645d-111">Если функция выполнена успешно (то есть, если запись содержит комментарий), возвращаемое значение является указателем на строку комментария.</span><span class="sxs-lookup"><span data-stu-id="9645d-111">If the function is successful (that is, if the capture contains a comment), the return value is a pointer to the comment string.</span></span>

<span data-ttu-id="9645d-112">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="9645d-112">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9645d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9645d-113">Remarks</span></span>

<span data-ttu-id="9645d-114">Не изменяйте возвращенную строку комментария, которая является действительной строкой комментариев, которая находится в загруженной записи.</span><span class="sxs-lookup"><span data-stu-id="9645d-114">Do not alter the returned comment string which is the actual comment string that is in the loaded capture.</span></span> <span data-ttu-id="9645d-115">Любые изменения могут повредить запись.</span><span class="sxs-lookup"><span data-stu-id="9645d-115">Any changes can corrupt the capture.</span></span> <span data-ttu-id="9645d-116">Попытка изменить строку приводит к нарушению прав доступа.</span><span class="sxs-lookup"><span data-stu-id="9645d-116">Attempts to modify the string result in an access violation.</span></span>

<span data-ttu-id="9645d-117">Маркер записи можно получить несколькими способами, в зависимости от того, сделан ли вызов экспертом или средством синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="9645d-117">The handle of the capture can be obtained in several ways, depending if the call is made by an expert or parser.</span></span> <span data-ttu-id="9645d-118">Для экспертов этот маркер указывается в элементе **хкаптуре** структуры [експертстартупинфо](expertstartupinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="9645d-118">For experts, the handle is specified in the **hCapture** member of the [EXPERTSTARTUPINFO](expertstartupinfo.md) structure.</span></span> <span data-ttu-id="9645d-119">Для средств синтаксического анализа можно получить маркер записи, вызвав функцию [жетфрамекаптурехандле](getframecapturehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="9645d-119">For parsers, the capture handle can be obtained by calling the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

<span data-ttu-id="9645d-120">Чтобы получить комментарий записи из файла записи, вызовите функцию [жеткаптурекомментфромфиленаме](getcapturecommentfromfilename.md) .</span><span class="sxs-lookup"><span data-stu-id="9645d-120">To retrieve the comment of a capture from its capture file, call the [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) function.</span></span>

<span data-ttu-id="9645d-121">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жеткаптурекоммент** .</span><span class="sxs-lookup"><span data-stu-id="9645d-121">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureComment** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9645d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9645d-122">Requirements</span></span>



| <span data-ttu-id="9645d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="9645d-123">Requirement</span></span> | <span data-ttu-id="9645d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9645d-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9645d-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9645d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9645d-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9645d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9645d-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9645d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9645d-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9645d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9645d-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9645d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9645d-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9645d-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="9645d-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9645d-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="9645d-132"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9645d-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9645d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9645d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9645d-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9645d-134"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9645d-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9645d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9645d-136">експертстартупинфо</span><span class="sxs-lookup"><span data-stu-id="9645d-136">EXPERTSTARTUPINFO</span></span>](expertstartupinfo.md)
</dt> <dt>

[<span data-ttu-id="9645d-137">жеткаптурекомментфромфиленаме</span><span class="sxs-lookup"><span data-stu-id="9645d-137">GetCaptureCommentFromFilename</span></span>](getcapturecommentfromfilename.md)
</dt> <dt>

[<span data-ttu-id="9645d-138">жетфрамекаптурехандле</span><span class="sxs-lookup"><span data-stu-id="9645d-138">GetFrameCaptureHandle</span></span>](getframecapturehandle.md)
</dt> </dl>

 

 




