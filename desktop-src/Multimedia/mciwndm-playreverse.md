---
title: Сообщение MCIWNDM_PLAYREVERSE (VFW. h)
description: Сообщение МЦИВНДМ \_ плайреверсе воспроизводит текущее содержимое в обратном направлении, начиная с текущей позиции и заканчивая в начале содержимого, или пока другая команда не останавливает воспроизведение.
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- MCIWNDM_PLAYREVERSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYREVERSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b0a2e230e3c57e8314e455be5dfbc5cea2c013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135074"
---
# <a name="mciwndm_playreverse-message"></a><span data-ttu-id="52f6d-104">\_Сообщение мЦивндм плайреверсе</span><span class="sxs-lookup"><span data-stu-id="52f6d-104">MCIWNDM\_PLAYREVERSE message</span></span>

<span data-ttu-id="52f6d-105">Сообщение **мЦивндм \_ плайреверсе** воспроизводит текущее содержимое в обратном направлении, начиная с текущей позиции и заканчивая в начале содержимого, или пока другая команда не останавливает воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="52f6d-105">The **MCIWNDM\_PLAYREVERSE** message plays the current content in the reverse direction, beginning at the current position and ending at the beginning of the content or until another command stops playback.</span></span> <span data-ttu-id="52f6d-106">Это сообщение можно отправить явно или с помощью макроса [**мЦивндплайреверсе**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) .</span><span class="sxs-lookup"><span data-stu-id="52f6d-106">You can send this message explicitly or by using the [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) macro.</span></span>


```C++
MCIWNDM_PLAYREVERSE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="52f6d-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52f6d-107">Return Value</span></span>

<span data-ttu-id="52f6d-108">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="52f6d-108">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="52f6d-109">Требования</span><span class="sxs-lookup"><span data-stu-id="52f6d-109">Requirements</span></span>



| <span data-ttu-id="52f6d-110">Требование</span><span class="sxs-lookup"><span data-stu-id="52f6d-110">Requirement</span></span> | <span data-ttu-id="52f6d-111">Значение</span><span class="sxs-lookup"><span data-stu-id="52f6d-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="52f6d-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52f6d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="52f6d-113">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="52f6d-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="52f6d-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52f6d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="52f6d-115">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="52f6d-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="52f6d-116">Заголовок</span><span class="sxs-lookup"><span data-stu-id="52f6d-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="52f6d-117"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="52f6d-117"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52f6d-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52f6d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f6d-119">**мЦивндплайреверсе**</span><span class="sxs-lookup"><span data-stu-id="52f6d-119">**MCIWndPlayReverse**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
</dt> </dl>

 

 





