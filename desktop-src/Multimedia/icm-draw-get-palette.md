---
title: Сообщение ICM_DRAW_GET_PALETTE (VFW. h)
description: Сообщение ICM \_ \_ Get, получающая \_ палитру, запрашивает драйвер подготовки к просмотру для возврата палитры.
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- ICM_DRAW_GET_PALETTE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03f3658d2a2653f940e18e9b82b7cc3d7690ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071239"
---
# <a name="icm_draw_get_palette-message"></a><span data-ttu-id="64d58-104">\_Сообщение о \_ получении \_ палитры ICM Draw</span><span class="sxs-lookup"><span data-stu-id="64d58-104">ICM\_DRAW\_GET\_PALETTE message</span></span>

<span data-ttu-id="64d58-105">Сообщение **ICM \_ \_ Get, получающая \_ палитру** , запрашивает драйвер подготовки к просмотру для возврата палитры.</span><span class="sxs-lookup"><span data-stu-id="64d58-105">The **ICM\_DRAW\_GET\_PALETTE** message requests a rendering driver to return a palette.</span></span>


```C++
ICM_DRAW_GET_PALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="64d58-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64d58-106">Return Value</span></span>

<span data-ttu-id="64d58-107">Драйвер должен возвращать один из следующих элементов: маркер используемой палитры, **значение NULL** , если он не имеет возвращаемого маркера, или ИЦЕРР не \_ поддерживается, если он не поддерживает палитры.</span><span class="sxs-lookup"><span data-stu-id="64d58-107">The driver should return one of the following: a handle of the palette being used, **NULL** if it doesn't have a handle to return, or ICERR\_UNSUPPORTED if it doesn't support palettes.</span></span>

## <a name="requirements"></a><span data-ttu-id="64d58-108">Требования</span><span class="sxs-lookup"><span data-stu-id="64d58-108">Requirements</span></span>



| <span data-ttu-id="64d58-109">Требование</span><span class="sxs-lookup"><span data-stu-id="64d58-109">Requirement</span></span> | <span data-ttu-id="64d58-110">Значение</span><span class="sxs-lookup"><span data-stu-id="64d58-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="64d58-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64d58-111">Minimum supported client</span></span><br/> | <span data-ttu-id="64d58-112">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="64d58-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="64d58-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64d58-113">Minimum supported server</span></span><br/> | <span data-ttu-id="64d58-114">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="64d58-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="64d58-115">Заголовок</span><span class="sxs-lookup"><span data-stu-id="64d58-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="64d58-116"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="64d58-116"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64d58-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64d58-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64d58-118">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="64d58-118">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="64d58-119">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="64d58-119">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





