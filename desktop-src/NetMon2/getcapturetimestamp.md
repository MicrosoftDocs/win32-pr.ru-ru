---
description: Функция Жеткаптуретиместамп возвращает дату и время начала записи кадров записью.
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: Функция Жеткаптуретиместамп (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 855aa8b5432fd06bb25571fcb48c091dcfe502f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540210"
---
# <a name="getcapturetimestamp-function"></a><span data-ttu-id="413ad-103">Функция Жеткаптуретиместамп</span><span class="sxs-lookup"><span data-stu-id="413ad-103">GetCaptureTimeStamp function</span></span>

<span data-ttu-id="413ad-104">Функция **жеткаптуретиместамп** возвращает дату и время начала записи кадров записью.</span><span class="sxs-lookup"><span data-stu-id="413ad-104">The **GetCaptureTimeStamp** function returns the time and date when the capture started recording frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="413ad-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="413ad-105">Syntax</span></span>


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="413ad-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="413ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="413ad-107">*хкаптуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="413ad-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="413ad-108">Обработчик для записи.</span><span class="sxs-lookup"><span data-stu-id="413ad-108">Handle to the capture.</span></span> <span data-ttu-id="413ad-109">Дополнительные сведения о получении маркера записи см. в подразделе "Примечания" этой статьи **жеткаптуретиместамп** .</span><span class="sxs-lookup"><span data-stu-id="413ad-109">For information about obtaining the capture handle, see the Remarks section of this **GetCaptureTimeStamp** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="413ad-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="413ad-110">Return value</span></span>

<span data-ttu-id="413ad-111">Если функция выполнена успешно, возвращаемое значение является указателем на структуру [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="413ad-111">If the function is successful, the return value is a pointer to a [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

<span data-ttu-id="413ad-112">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="413ad-112">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="413ad-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="413ad-113">Remarks</span></span>

<span data-ttu-id="413ad-114">Функция **жеткаптуретиместамп** Возвращает время, когда поставщик сетевых пакетов (НПП) начинает сбор данных, а не когда эксперт загружает запись для анализа.</span><span class="sxs-lookup"><span data-stu-id="413ad-114">The **GetCaptureTimeStamp** function returns the time when the Network Packet Provider (NPP) starts collecting data, not when the expert loads the capture for analysis.</span></span>

<span data-ttu-id="413ad-115">Не перезаписывайте данные в структуре **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="413ad-115">Do not overwrite the data in the **SYSTEMTIME** structure.</span></span> <span data-ttu-id="413ad-116">Данные являются частью записи.</span><span class="sxs-lookup"><span data-stu-id="413ad-116">The data is part of the capture.</span></span> <span data-ttu-id="413ad-117">Попытка изменить данные приведет к нарушению прав доступа.</span><span class="sxs-lookup"><span data-stu-id="413ad-117">Trying to modify the data causes an access violation.</span></span>

<span data-ttu-id="413ad-118">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жеткаптуретиместамп** .</span><span class="sxs-lookup"><span data-stu-id="413ad-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureTimeStamp** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="413ad-119">Требования</span><span class="sxs-lookup"><span data-stu-id="413ad-119">Requirements</span></span>



| <span data-ttu-id="413ad-120">Требование</span><span class="sxs-lookup"><span data-stu-id="413ad-120">Requirement</span></span> | <span data-ttu-id="413ad-121">Значение</span><span class="sxs-lookup"><span data-stu-id="413ad-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="413ad-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="413ad-122">Minimum supported client</span></span><br/> | <span data-ttu-id="413ad-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="413ad-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="413ad-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="413ad-124">Minimum supported server</span></span><br/> | <span data-ttu-id="413ad-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="413ad-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="413ad-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="413ad-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="413ad-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="413ad-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="413ad-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="413ad-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="413ad-129"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="413ad-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="413ad-130">DLL</span><span class="sxs-lookup"><span data-stu-id="413ad-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="413ad-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="413ad-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="413ad-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="413ad-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="413ad-133">SYSTEMTIME</span><span class="sxs-lookup"><span data-stu-id="413ad-133">SYSTEMTIME</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 

