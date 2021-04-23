---
title: Сообщение WM_CAP_GET_SEQUENCE_SETUP (VFW. h)
description: Сообщение о \_ настройке "получение последовательности" WM Cap \_ \_ \_ получает текущие параметры параметров сбора потоковой передачи. Это сообщение можно отправить явно или с помощью макроса Капкаптурежетсетуп.
ms.assetid: 2220c92a-1994-4f15-9730-1cf01972dda6
keywords:
- WM_CAP_GET_SEQUENCE_SETUP сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_GET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5cd1585b165581f9c9646741b92c5dc841472ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988172"
---
# <a name="wm_cap_get_sequence_setup-message"></a><span data-ttu-id="4bbcb-105">\_Сообщение о \_ \_ настройке получения последовательностей WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="4bbcb-105">WM\_CAP\_GET\_SEQUENCE\_SETUP message</span></span>

<span data-ttu-id="4bbcb-106">Сообщение **о \_ \_ \_ \_ настройке "получение последовательности" WM Cap** получает текущие параметры параметров сбора потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-106">The **WM\_CAP\_GET\_SEQUENCE\_SETUP** message retrieves the current settings of the streaming capture parameters.</span></span> <span data-ttu-id="4bbcb-107">Это сообщение можно отправить явно или с помощью макроса [**капкаптурежетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) .</span><span class="sxs-lookup"><span data-stu-id="4bbcb-107">You can send this message explicitly or by using the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro.</span></span>


```C++
WM_CAP_GET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (s); 
```



## <a name="parameters"></a><span data-ttu-id="4bbcb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4bbcb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bbcb-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*</span><span class="sxs-lookup"><span data-stu-id="4bbcb-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="4bbcb-110">Размер (в байтах) структуры, на которую ссылается **s**.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="4bbcb-111"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="4bbcb-111"><span id="s"></span><span id="S"></span>*s*</span></span>
</dt> <dd>

<span data-ttu-id="4bbcb-112">Указатель на структуру [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="4bbcb-112">Pointer to a [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bbcb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4bbcb-113">Return Value</span></span>

<span data-ttu-id="4bbcb-114">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4bbcb-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bbcb-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4bbcb-115">Remarks</span></span>

<span data-ttu-id="4bbcb-116">Сведения о параметрах, используемых для управления потоковой передачей, см. в разделе Структура [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="4bbcb-116">For information about the parameters used to control streaming capture, see the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bbcb-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4bbcb-117">Requirements</span></span>



| <span data-ttu-id="4bbcb-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4bbcb-118">Requirement</span></span> | <span data-ttu-id="4bbcb-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4bbcb-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4bbcb-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4bbcb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4bbcb-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4bbcb-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4bbcb-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4bbcb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4bbcb-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4bbcb-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4bbcb-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4bbcb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bbcb-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bbcb-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bbcb-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4bbcb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bbcb-127">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="4bbcb-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="4bbcb-128">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="4bbcb-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





