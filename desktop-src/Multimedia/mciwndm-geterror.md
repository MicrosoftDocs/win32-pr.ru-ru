---
title: Сообщение MCIWNDM_GETERROR (VFW. h)
description: МЦИВНДМ \_ сообщение об ошибке извлекает последнюю обнаруженную ошибку MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетеррор.
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- MCIWNDM_GETERROR сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2977bb079351824b48da21f4ba3cc2dc5afe7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891546"
---
# <a name="mciwndm_geterror-message"></a><span data-ttu-id="88d29-105">\_Сообщение об ошибке мЦивндм</span><span class="sxs-lookup"><span data-stu-id="88d29-105">MCIWNDM\_GETERROR message</span></span>

<span data-ttu-id="88d29-106">МЦивндм сообщение об **\_ ошибке** извлекает последнюю обнаруженную ошибку MCI.</span><span class="sxs-lookup"><span data-stu-id="88d29-106">The **MCIWNDM\_GETERROR** message retrieves the last MCI error encountered.</span></span> <span data-ttu-id="88d29-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетеррор**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) .</span><span class="sxs-lookup"><span data-stu-id="88d29-107">You can send this message explicitly or by using the [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) macro.</span></span>


```C++
MCIWNDM_GETERROR 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="88d29-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="88d29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88d29-109"><span id="len"></span><span id="LEN"></span>*len*</span><span class="sxs-lookup"><span data-stu-id="88d29-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="88d29-110">Размер буфера ошибок в байтах.</span><span class="sxs-lookup"><span data-stu-id="88d29-110">Size, in bytes, of the error buffer.</span></span>

</dd> <dt>

<span data-ttu-id="88d29-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="88d29-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="88d29-112">Указатель на определенный приложением буфер, используемый для возврата строки ошибки.</span><span class="sxs-lookup"><span data-stu-id="88d29-112">Pointer to an application-defined buffer used to return the error string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88d29-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88d29-113">Return Value</span></span>

<span data-ttu-id="88d29-114">Возвращает целочисленное значение ошибки в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="88d29-114">Returns the integer error value if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="88d29-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88d29-115">Remarks</span></span>

<span data-ttu-id="88d29-116">Если *LP* является допустимым указателем, в его буфере возвращается строка, завершающаяся нулем, соответствующая ошибке.</span><span class="sxs-lookup"><span data-stu-id="88d29-116">If *lp* is a valid pointer, a null-terminated string corresponding to the error is returned in its buffer.</span></span> <span data-ttu-id="88d29-117">Если строка ошибки длиннее, чем буфер, МЦивнд усекает ее.</span><span class="sxs-lookup"><span data-stu-id="88d29-117">If the error string is longer than the buffer, MCIWnd truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="88d29-118">Требования</span><span class="sxs-lookup"><span data-stu-id="88d29-118">Requirements</span></span>



| <span data-ttu-id="88d29-119">Требование</span><span class="sxs-lookup"><span data-stu-id="88d29-119">Requirement</span></span> | <span data-ttu-id="88d29-120">Значение</span><span class="sxs-lookup"><span data-stu-id="88d29-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="88d29-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88d29-121">Minimum supported client</span></span><br/> | <span data-ttu-id="88d29-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="88d29-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="88d29-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88d29-123">Minimum supported server</span></span><br/> | <span data-ttu-id="88d29-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="88d29-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="88d29-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="88d29-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="88d29-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="88d29-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88d29-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88d29-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88d29-128">**мЦивнджетеррор**</span><span class="sxs-lookup"><span data-stu-id="88d29-128">**MCIWndGetError**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





