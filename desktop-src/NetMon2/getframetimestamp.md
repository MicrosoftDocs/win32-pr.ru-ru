---
description: Функция Жетфраметиместамп возвращает метку времени данного кадра.
ms.assetid: 4ac50400-6674-40fa-9a69-9c0ccb55b92c
title: Функция Жетфраметиместамп (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 37a75f946a5fc0ddb2b32d99334368a272fdf2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663455"
---
# <a name="getframetimestamp-function"></a><span data-ttu-id="0f8c9-103">Функция Жетфраметиместамп</span><span class="sxs-lookup"><span data-stu-id="0f8c9-103">GetFrameTimeStamp function</span></span>

<span data-ttu-id="0f8c9-104">Функция **жетфраметиместамп** возвращает метку времени данного кадра.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-104">The **GetFrameTimeStamp** function returns the time stamp of a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f8c9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f8c9-105">Syntax</span></span>


```C++
__int64 WINAPI GetFrameTimeStamp(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="0f8c9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f8c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f8c9-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f8c9-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f8c9-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f8c9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f8c9-109">Return value</span></span>

<span data-ttu-id="0f8c9-110">Если функция выполнена успешно, возвращаемое значение — это метка времени кадра в микросекундах.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-110">If the function is successful, the return value is the time stamp of the frame   in microseconds.</span></span>

<span data-ttu-id="0f8c9-111">Если функция завершилась неудачно, возвращаемое значение равно минус единице (-1).</span><span class="sxs-lookup"><span data-stu-id="0f8c9-111">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f8c9-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f8c9-112">Remarks</span></span>

<span data-ttu-id="0f8c9-113">Функция **жетфраметиместамп** возвращает метку времени, которая показывает время, прошедшее с начала процесса записи, и запись кадра.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-113">The **GetFrameTimeStamp** function returns a time stamp that shows the elapsed time between the start of the capture process, and the recording of the frame.</span></span>

<span data-ttu-id="0f8c9-114">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетфраметиместамп** .</span><span class="sxs-lookup"><span data-stu-id="0f8c9-114">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameTimeStamp** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f8c9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="0f8c9-115">Requirements</span></span>



| <span data-ttu-id="0f8c9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="0f8c9-116">Requirement</span></span> | <span data-ttu-id="0f8c9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0f8c9-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0f8c9-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f8c9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0f8c9-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f8c9-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0f8c9-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f8c9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0f8c9-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f8c9-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0f8c9-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0f8c9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f8c9-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f8c9-123"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="0f8c9-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0f8c9-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="0f8c9-125"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f8c9-125"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0f8c9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="0f8c9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f8c9-127"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f8c9-127"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




