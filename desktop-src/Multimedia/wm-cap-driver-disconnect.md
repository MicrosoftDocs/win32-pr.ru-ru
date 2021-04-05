---
title: Сообщение WM_CAP_DRIVER_DISCONNECT (VFW. h)
description: '\_ \_ \_ Сообщение об отключении драйвера WM Cap отключает драйвер записи из окна записи. Это сообщение можно отправить явно или с помощью макроса Капдривердисконнект.'
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- WM_CAP_DRIVER_DISCONNECT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_DISCONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acad628cc61bbb50c56f68fda91ac87be4feb728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988529"
---
# <a name="wm_cap_driver_disconnect-message"></a><span data-ttu-id="ed8ac-105">\_ \_ \_ Сообщение об отключении драйвера WM Cap</span><span class="sxs-lookup"><span data-stu-id="ed8ac-105">WM\_CAP\_DRIVER\_DISCONNECT message</span></span>

<span data-ttu-id="ed8ac-106">Сообщение **об \_ \_ \_ отключении драйвера WM Cap** отключает драйвер записи из окна записи.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-106">The **WM\_CAP\_DRIVER\_DISCONNECT** message disconnects a capture driver from a capture window.</span></span> <span data-ttu-id="ed8ac-107">Это сообщение можно отправить явно или с помощью макроса [**капдривердисконнект**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) .</span><span class="sxs-lookup"><span data-stu-id="ed8ac-107">You can send this message explicitly or by using the [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) macro.</span></span>


```C++
WM_CAP_DRIVER_DISCONNECT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="ed8ac-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed8ac-108">Return Value</span></span>

<span data-ttu-id="ed8ac-109">Возвращает **значение true** в случае успеха или **false** , если окно записи не подключено к драйверу записи.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-109">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed8ac-110">Требования</span><span class="sxs-lookup"><span data-stu-id="ed8ac-110">Requirements</span></span>



| <span data-ttu-id="ed8ac-111">Требование</span><span class="sxs-lookup"><span data-stu-id="ed8ac-111">Requirement</span></span> | <span data-ttu-id="ed8ac-112">Значение</span><span class="sxs-lookup"><span data-stu-id="ed8ac-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ed8ac-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed8ac-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ed8ac-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ed8ac-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ed8ac-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed8ac-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ed8ac-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ed8ac-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ed8ac-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ed8ac-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed8ac-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed8ac-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed8ac-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed8ac-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed8ac-120">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="ed8ac-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="ed8ac-121">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="ed8ac-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





