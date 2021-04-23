---
title: Сообщение WM_CAP_DRIVER_CONNECT (VFW. h)
description: '\_ \_ Сообщение Connect с драйвером WM Cap \_ подключает окно записи к драйверу записи. Это сообщение можно отправить явно или с помощью макроса Капдриверконнект.'
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- WM_CAP_DRIVER_CONNECT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_CONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fdeb89968926429f7225912e3d1b3b348e287
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415345"
---
# <a name="wm_cap_driver_connect-message"></a><span data-ttu-id="a196c-105">\_Сообщение о \_ подключении драйвера WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="a196c-105">WM\_CAP\_DRIVER\_CONNECT message</span></span>

<span data-ttu-id="a196c-106">Сообщение **\_ \_ \_ Connect с драйвером WM Cap** подключает окно записи к драйверу записи.</span><span class="sxs-lookup"><span data-stu-id="a196c-106">The **WM\_CAP\_DRIVER\_CONNECT** message connects a capture window to a capture driver.</span></span> <span data-ttu-id="a196c-107">Это сообщение можно отправить явно или с помощью макроса [**капдриверконнект**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) .</span><span class="sxs-lookup"><span data-stu-id="a196c-107">You can send this message explicitly or by using the [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) macro.</span></span>


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="a196c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a196c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a196c-109"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*ииндекс*</span><span class="sxs-lookup"><span data-stu-id="a196c-109"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="a196c-110">Индекс драйвера записи.</span><span class="sxs-lookup"><span data-stu-id="a196c-110">Index of the capture driver.</span></span> <span data-ttu-id="a196c-111">Индекс может находиться в диапазоне от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="a196c-111">The index can range from 0 through 9.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a196c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a196c-112">Return Value</span></span>

<span data-ttu-id="a196c-113">Возвращает **значение true** в случае успеха или **false** , если указанный драйвер записи не может быть подключен к окну Capture.</span><span class="sxs-lookup"><span data-stu-id="a196c-113">Returns **TRUE** if successful or **FALSE** if the specified capture driver cannot be connected to the capture window.</span></span>

## <a name="remarks"></a><span data-ttu-id="a196c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a196c-114">Remarks</span></span>

<span data-ttu-id="a196c-115">Подключение драйвера записи к окну записи автоматически отключает все ранее подключенные драйверы записи.</span><span class="sxs-lookup"><span data-stu-id="a196c-115">Connecting a capture driver to a capture window automatically disconnects any previously connected capture driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="a196c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a196c-116">Requirements</span></span>



| <span data-ttu-id="a196c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a196c-117">Requirement</span></span> | <span data-ttu-id="a196c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a196c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a196c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a196c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a196c-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a196c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a196c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a196c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a196c-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a196c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a196c-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a196c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a196c-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a196c-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a196c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a196c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a196c-126">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="a196c-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="a196c-127">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="a196c-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





