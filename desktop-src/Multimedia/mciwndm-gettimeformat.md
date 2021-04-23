---
title: Сообщение MCIWNDM_GETTIMEFORMAT (VFW. h)
description: Сообщение МЦИВНДМ \_ жеттимеформат извлекает текущий формат времени устройства MCI в двух формах как числовое значение и в виде строки. Это сообщение можно отправить явно или с помощью макроса МЦивнджеттимеформат.
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- MCIWNDM_GETTIMEFORMAT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a09f969c009ff23bc0951ed2efbc0dbf7aa95dda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801330"
---
# <a name="mciwndm_gettimeformat-message"></a><span data-ttu-id="a3ecb-105">\_Сообщение мЦивндм жеттимеформат</span><span class="sxs-lookup"><span data-stu-id="a3ecb-105">MCIWNDM\_GETTIMEFORMAT message</span></span>

<span data-ttu-id="a3ecb-106">Сообщение **мЦивндм \_ жеттимеформат** извлекает текущий формат времени устройства MCI в двух формах: как числовое значение и как строка.</span><span class="sxs-lookup"><span data-stu-id="a3ecb-106">The **MCIWNDM\_GETTIMEFORMAT** message retrieves the current time format of an MCI device in two forms: as a numerical value and as a string.</span></span> <span data-ttu-id="a3ecb-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджеттимеформат**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="a3ecb-107">You can send this message explicitly or by using the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span>


```C++
MCIWNDM_GETTIMEFORMAT 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="a3ecb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3ecb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3ecb-109"><span id="len"></span><span id="LEN"></span>*len*</span><span class="sxs-lookup"><span data-stu-id="a3ecb-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="a3ecb-110">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="a3ecb-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a3ecb-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="a3ecb-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="a3ecb-112">Указатель на буфер, содержащий строку формата времени, завершающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="a3ecb-112">Pointer to a buffer to contain the null-terminated string form of the time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3ecb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3ecb-113">Return Value</span></span>

<span data-ttu-id="a3ecb-114">Возвращает целое число, соответствующее константе MCI, определяющей формат времени.</span><span class="sxs-lookup"><span data-stu-id="a3ecb-114">Returns an integer corresponding to the MCI constant defining the time format.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3ecb-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3ecb-115">Remarks</span></span>

<span data-ttu-id="a3ecb-116">Если длина строки формата времени превышает размер буфера возврата, МЦивнд усекает строку.</span><span class="sxs-lookup"><span data-stu-id="a3ecb-116">If the time format string is longer than the return buffer, MCIWnd truncates the string.</span></span>

<span data-ttu-id="a3ecb-117">Устройство MCI может поддерживать один или несколько следующих форматов времени.</span><span class="sxs-lookup"><span data-stu-id="a3ecb-117">An MCI device can support one or more of the following time formats.</span></span>



| <span data-ttu-id="a3ecb-118">Формат времени</span><span class="sxs-lookup"><span data-stu-id="a3ecb-118">Time format</span></span>                      | <span data-ttu-id="a3ecb-119">Константа MCI</span><span class="sxs-lookup"><span data-stu-id="a3ecb-119">MCI constant</span></span>               |
|----------------------------------|----------------------------|
| <span data-ttu-id="a3ecb-120">Байты</span><span class="sxs-lookup"><span data-stu-id="a3ecb-120">Bytes</span></span>                            | <span data-ttu-id="a3ecb-121">\_ \_ байты формата MCI</span><span class="sxs-lookup"><span data-stu-id="a3ecb-121">MCI\_FORMAT\_BYTES</span></span>         |
| <span data-ttu-id="a3ecb-122">Получен</span><span class="sxs-lookup"><span data-stu-id="a3ecb-122">Frames</span></span>                           | <span data-ttu-id="a3ecb-123">\_кадры формата \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a3ecb-123">MCI\_FORMAT\_FRAMES</span></span>        |
| <span data-ttu-id="a3ecb-124">Часы, минуты, секунды</span><span class="sxs-lookup"><span data-stu-id="a3ecb-124">Hours, minutes, seconds</span></span>          | <span data-ttu-id="a3ecb-125">\_Формат MCI \_ ХМс</span><span class="sxs-lookup"><span data-stu-id="a3ecb-125">MCI\_FORMAT\_HMS</span></span>           |
| <span data-ttu-id="a3ecb-126">Миллисекунды</span><span class="sxs-lookup"><span data-stu-id="a3ecb-126">Milliseconds</span></span>                     | <span data-ttu-id="a3ecb-127">\_ \_ миллисекунды формата MCI</span><span class="sxs-lookup"><span data-stu-id="a3ecb-127">MCI\_FORMAT\_MILLISECONDS</span></span>  |
| <span data-ttu-id="a3ecb-128">Минуты, секунды, кадры</span><span class="sxs-lookup"><span data-stu-id="a3ecb-128">Minutes, seconds, frames</span></span>         | <span data-ttu-id="a3ecb-129">формат MCI, \_ \_ MSF</span><span class="sxs-lookup"><span data-stu-id="a3ecb-129">MCI\_FORMAT\_MSF</span></span>           |
| <span data-ttu-id="a3ecb-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="a3ecb-130">Samples</span></span>                          | <span data-ttu-id="a3ecb-131">\_примеры формата \_ MCI</span><span class="sxs-lookup"><span data-stu-id="a3ecb-131">MCI\_FORMAT\_SAMPLES</span></span>       |
| <span data-ttu-id="a3ecb-132">SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="a3ecb-132">SMPTE 24</span></span>                         | <span data-ttu-id="a3ecb-133">\_Формат MCI \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="a3ecb-133">MCI\_FORMAT\_SMPTE\_24</span></span>     |
| <span data-ttu-id="a3ecb-134">SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="a3ecb-134">SMPTE 25</span></span>                         | <span data-ttu-id="a3ecb-135">\_Формат MCI \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="a3ecb-135">MCI\_FORMAT\_SMPTE\_25</span></span>     |
| <span data-ttu-id="a3ecb-136">SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="a3ecb-136">SMPTE 30 drop</span></span>                    | <span data-ttu-id="a3ecb-137">\_Формат MCI \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="a3ecb-137">MCI\_FORMAT\_SMPTE\_30DROP</span></span> |
| <span data-ttu-id="a3ecb-138">SMPTE 30 (без перетаскивания)</span><span class="sxs-lookup"><span data-stu-id="a3ecb-138">SMPTE 30 (non-drop)</span></span>              | <span data-ttu-id="a3ecb-139">\_Формат MCI \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="a3ecb-139">MCI\_FORMAT\_SMPTE\_30</span></span>     |
| <span data-ttu-id="a3ecb-140">Дорожек, минут, секунд, кадров</span><span class="sxs-lookup"><span data-stu-id="a3ecb-140">Tracks, minutes, seconds, frames</span></span> | <span data-ttu-id="a3ecb-141">\_Формат MCI \_ тмсф</span><span class="sxs-lookup"><span data-stu-id="a3ecb-141">MCI\_FORMAT\_TMSF</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="a3ecb-142">Требования</span><span class="sxs-lookup"><span data-stu-id="a3ecb-142">Requirements</span></span>



| <span data-ttu-id="a3ecb-143">Требование</span><span class="sxs-lookup"><span data-stu-id="a3ecb-143">Requirement</span></span> | <span data-ttu-id="a3ecb-144">Значение</span><span class="sxs-lookup"><span data-stu-id="a3ecb-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a3ecb-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3ecb-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a3ecb-146">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a3ecb-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a3ecb-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3ecb-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a3ecb-148">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a3ecb-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a3ecb-149">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a3ecb-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3ecb-150"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3ecb-150"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3ecb-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3ecb-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3ecb-152">**мЦивнджеттимеформат**</span><span class="sxs-lookup"><span data-stu-id="a3ecb-152">**MCIWndGetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 





