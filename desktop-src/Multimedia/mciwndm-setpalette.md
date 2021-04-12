---
title: Сообщение MCIWNDM_SETPALETTE (VFW. h)
description: Сообщение МЦИВНДМ \_ сетпалетте отправляет маркер палитры на устройство MCI, связанное с окном мЦивнд. Это сообщение можно отправить явно или с помощью макроса МЦивндсетпалетте.
ms.assetid: d2399cb7-d83c-465c-b02f-e6a016c28ae3
keywords:
- MCIWNDM_SETPALETTE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7e354082de4fc15f4179555a8b635b9426af90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491721"
---
# <a name="mciwndm_setpalette-message"></a><span data-ttu-id="870c8-105">\_Сообщение мЦивндм сетпалетте</span><span class="sxs-lookup"><span data-stu-id="870c8-105">MCIWNDM\_SETPALETTE message</span></span>

<span data-ttu-id="870c8-106">Сообщение **мЦивндм \_ сетпалетте** отправляет маркер палитры на устройство MCI, связанное с окном мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="870c8-106">The **MCIWNDM\_SETPALETTE** message sends a palette handle to the MCI device associated with the MCIWnd window.</span></span> <span data-ttu-id="870c8-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндсетпалетте**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) .</span><span class="sxs-lookup"><span data-stu-id="870c8-107">You can send this message explicitly or by using the [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) macro.</span></span>


```C++
MCIWNDM_SETPALETTE 
wParam = (WPARAM) (HPALETTE) hpal; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="870c8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="870c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="870c8-109"><span id="hpal"></span><span id="HPAL"></span>*хпал*</span><span class="sxs-lookup"><span data-stu-id="870c8-109"><span id="hpal"></span><span id="HPAL"></span>*hpal*</span></span>
</dt> <dd>

<span data-ttu-id="870c8-110">Маркер палитры.</span><span class="sxs-lookup"><span data-stu-id="870c8-110">Palette handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="870c8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="870c8-111">Return Value</span></span>

<span data-ttu-id="870c8-112">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="870c8-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="870c8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="870c8-113">Requirements</span></span>



| <span data-ttu-id="870c8-114">Требование</span><span class="sxs-lookup"><span data-stu-id="870c8-114">Requirement</span></span> | <span data-ttu-id="870c8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="870c8-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="870c8-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="870c8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="870c8-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="870c8-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="870c8-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="870c8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="870c8-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="870c8-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="870c8-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="870c8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="870c8-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="870c8-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="870c8-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="870c8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="870c8-123">**мЦивндсетпалетте**</span><span class="sxs-lookup"><span data-stu-id="870c8-123">**MCIWndSetPalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 





