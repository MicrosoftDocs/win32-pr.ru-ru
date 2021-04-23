---
title: Сообщение WM_CAP_GET_MCI_DEVICE (VFW. h)
description: В сообщении о получении крепления WM получается \_ \_ \_ \_ имя устройства MCI, установленное ранее с помощью \_ \_ \_ сообщения устройства mci Set с закреплениями WM \_ . Это сообщение можно отправить явно или с помощью макроса КапжетмЦидевиценаме.
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- WM_CAP_GET_MCI_DEVICE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_GET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0960ff9aa1366802611f444383212c4bcc45bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488964"
---
# <a name="wm_cap_get_mci_device-message"></a><span data-ttu-id="7c770-105">\_Закрепление \_ WM \_ Получение \_ сообщения устройства mci</span><span class="sxs-lookup"><span data-stu-id="7c770-105">WM\_CAP\_GET\_MCI\_DEVICE message</span></span>

<span data-ttu-id="7c770-106">В сообщении о **\_ \_ получении \_ крепления \_ WM** получается имя устройства MCI, установленное ранее с помощью сообщения [**\_ \_ \_ \_ Устройства MCI Set с закреплениями WM**](wm-cap-set-mci-device.md) .</span><span class="sxs-lookup"><span data-stu-id="7c770-106">The **WM\_CAP\_GET\_MCI\_DEVICE** message retrieves the name of an MCI device previously set with the [**WM\_CAP\_SET\_MCI\_DEVICE**](wm-cap-set-mci-device.md) message.</span></span> <span data-ttu-id="7c770-107">Это сообщение можно отправить явно или с помощью макроса [**капжетмЦидевиценаме**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) .</span><span class="sxs-lookup"><span data-stu-id="7c770-107">You can send this message explicitly or by using the [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) macro.</span></span>


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="7c770-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c770-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c770-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*</span><span class="sxs-lookup"><span data-stu-id="7c770-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="7c770-110">Длина в байтах буфера, на который ссылается параметр **szName**.</span><span class="sxs-lookup"><span data-stu-id="7c770-110">Length, in bytes, of the buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="7c770-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="7c770-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="7c770-112">Указатель на строку, завершающуюся нулем, которая содержит имя устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="7c770-112">Pointer to a null-terminated string that contains the MCI device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c770-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c770-113">Return Value</span></span>

<span data-ttu-id="7c770-114">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7c770-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c770-115">Требования</span><span class="sxs-lookup"><span data-stu-id="7c770-115">Requirements</span></span>



| <span data-ttu-id="7c770-116">Требование</span><span class="sxs-lookup"><span data-stu-id="7c770-116">Requirement</span></span> | <span data-ttu-id="7c770-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7c770-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7c770-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c770-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7c770-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7c770-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7c770-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c770-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7c770-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7c770-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7c770-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7c770-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c770-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c770-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c770-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c770-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c770-125">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="7c770-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="7c770-126">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="7c770-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





