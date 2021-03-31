---
title: Сообщение WM_CAP_GET_STATUS (VFW. h)
description: '\_ \_ \_ Сообщение о состоянии крепления WM получает состояние окна сбора данных. Это сообщение можно отправить явно или с помощью макроса Капжетстатус.'
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- WM_CAP_GET_STATUS сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_GET_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ef6590770e8a9ece3eb8abaffb4dbca0b1a4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071086"
---
# <a name="wm_cap_get_status-message"></a><span data-ttu-id="d99bb-105">\_ \_ Получение \_ сообщения о состоянии крепления WM</span><span class="sxs-lookup"><span data-stu-id="d99bb-105">WM\_CAP\_GET\_STATUS message</span></span>

<span data-ttu-id="d99bb-106">Сообщение **\_ \_ \_ о состоянии крепления WM** получает состояние окна сбора данных.</span><span class="sxs-lookup"><span data-stu-id="d99bb-106">The **WM\_CAP\_GET\_STATUS** message retrieves the status of the capture window.</span></span> <span data-ttu-id="d99bb-107">Это сообщение можно отправить явно или с помощью макроса [**капжетстатус**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) .</span><span class="sxs-lookup"><span data-stu-id="d99bb-107">You can send this message explicitly or by using the [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) macro.</span></span>


```C++
WM_CAP_GET_STATUS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPSTATUS) (s); 
```



## <a name="parameters"></a><span data-ttu-id="d99bb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d99bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d99bb-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*</span><span class="sxs-lookup"><span data-stu-id="d99bb-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="d99bb-110">Размер (в байтах) структуры, на которую ссылается **s**.</span><span class="sxs-lookup"><span data-stu-id="d99bb-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="d99bb-111"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="d99bb-111"><span id="s"></span><span id="S"></span>*s*</span></span>
</dt> <dd>

<span data-ttu-id="d99bb-112">Указатель на структуру [**капстатус**](/windows/win32/api/vfw/ns-vfw-capstatus) .</span><span class="sxs-lookup"><span data-stu-id="d99bb-112">Pointer to a [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d99bb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d99bb-113">Return Value</span></span>

<span data-ttu-id="d99bb-114">Возвращает **значение true** в случае успеха или **false** , если окно записи не подключено к драйверу записи.</span><span class="sxs-lookup"><span data-stu-id="d99bb-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="d99bb-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d99bb-115">Remarks</span></span>

<span data-ttu-id="d99bb-116">Структура [**капстатус**](/windows/win32/api/vfw/ns-vfw-capstatus) содержит текущее состояние окна сбора данных.</span><span class="sxs-lookup"><span data-stu-id="d99bb-116">The [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure contains the current state of the capture window.</span></span> <span data-ttu-id="d99bb-117">Поскольку это состояние является динамическим и изменяется в ответ на различные сообщения, приложение должно инициализировать эту структуру после отправки сообщения [**\_ видеоформат WM \_ DLG \_**](wm-cap-dlg-videoformat.md) (или с помощью макроса [**капдлгвидеоформат**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ) и всякий раз, когда необходимо включить пункты меню или определить фактическое состояние окна.</span><span class="sxs-lookup"><span data-stu-id="d99bb-117">Since this state is dynamic and changes in response to various messages, the application should initialize this structure after sending the [**WM\_CAP\_DLG\_VIDEOFORMAT**](wm-cap-dlg-videoformat.md) message (or using the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro) and whenever it needs to enable menu items or determine the actual state of the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="d99bb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d99bb-118">Requirements</span></span>



| <span data-ttu-id="d99bb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d99bb-119">Requirement</span></span> | <span data-ttu-id="d99bb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d99bb-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d99bb-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d99bb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d99bb-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d99bb-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d99bb-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d99bb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d99bb-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d99bb-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d99bb-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d99bb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d99bb-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d99bb-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d99bb-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d99bb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d99bb-128">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="d99bb-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d99bb-129">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="d99bb-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





