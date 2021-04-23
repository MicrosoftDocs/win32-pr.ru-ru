---
title: Сообщение MCIWNDM_RETURNSTRING (VFW. h)
description: Сообщение МЦИВНДМ \_ ретурнстринг извлекает ответ на последнюю командную строку MCI, отправленную на устройство MCI.
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- MCIWNDM_RETURNSTRING сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_RETURNSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b99307bd7d61a70db594d0a696cceccd6d246a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071596"
---
# <a name="mciwndm_returnstring-message"></a><span data-ttu-id="1a6e9-104">\_Сообщение мЦивндм ретурнстринг</span><span class="sxs-lookup"><span data-stu-id="1a6e9-104">MCIWNDM\_RETURNSTRING message</span></span>

<span data-ttu-id="1a6e9-105">Сообщение **мЦивндм \_ ретурнстринг** извлекает ответ на последнюю командную строку MCI, отправленную на устройство MCI.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-105">The **MCIWNDM\_RETURNSTRING** message retrieves the reply to the most recent MCI string command sent to an MCI device.</span></span> <span data-ttu-id="1a6e9-106">Сведения в ответе передаются в виде строки, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-106">Information in the reply is supplied as a null-terminated string.</span></span> <span data-ttu-id="1a6e9-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндретурнстринг**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .</span><span class="sxs-lookup"><span data-stu-id="1a6e9-107">You can send this message explicitly or by using the [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) macro.</span></span>


```C++
MCIWNDM_RETURNSTRING 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="1a6e9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a6e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a6e9-109"><span id="len"></span><span id="LEN"></span>*len*</span><span class="sxs-lookup"><span data-stu-id="1a6e9-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="1a6e9-110">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1a6e9-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="1a6e9-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="1a6e9-112">Указатель на определенный приложением буфер, содержащий строку, завершающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-112">Pointer to an application-defined buffer to contain the null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a6e9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a6e9-113">Return Value</span></span>

<span data-ttu-id="1a6e9-114">Возвращает целое число, соответствующее строке MCI.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-114">Returns an integer corresponding to the MCI string.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a6e9-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a6e9-115">Remarks</span></span>

<span data-ttu-id="1a6e9-116">Если строка, завершающаяся нулем, длиннее, чем буфер, строка усекается.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-116">If the null-terminated string is longer than the buffer, the string is truncated.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a6e9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1a6e9-117">Requirements</span></span>



| <span data-ttu-id="1a6e9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1a6e9-118">Requirement</span></span> | <span data-ttu-id="1a6e9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1a6e9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1a6e9-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a6e9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1a6e9-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1a6e9-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1a6e9-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a6e9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1a6e9-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1a6e9-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1a6e9-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1a6e9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a6e9-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a6e9-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a6e9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a6e9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a6e9-127">**мЦивндретурнстринг**</span><span class="sxs-lookup"><span data-stu-id="1a6e9-127">**MCIWndReturnString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 





