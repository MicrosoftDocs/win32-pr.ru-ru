---
title: Сообщение WM_CAP_SET_MCI_DEVICE (VFW. h)
description: В \_ \_ сообщении об установке устройства mci с закреплениями WM \_ \_ указывается имя видеоустройства MCI, которое будет использоваться для записи данных. Это сообщение можно отправить явно или с помощью макроса КапсетмЦидевиценаме.
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- WM_CAP_SET_MCI_DEVICE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86187f3357bf72866e05b497332454c10bcd2fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801192"
---
# <a name="wm_cap_set_mci_device-message"></a><span data-ttu-id="2193d-105">\_ \_ \_ \_ Сообщение об установке устройства mci с закреплениями WM</span><span class="sxs-lookup"><span data-stu-id="2193d-105">WM\_CAP\_SET\_MCI\_DEVICE message</span></span>

<span data-ttu-id="2193d-106">В сообщении об **\_ \_ установке \_ \_ Устройства MCI с закреплениями WM** указывается имя видеоустройства MCI, которое будет использоваться для записи данных.</span><span class="sxs-lookup"><span data-stu-id="2193d-106">The **WM\_CAP\_SET\_MCI\_DEVICE** message specifies the name of the MCI video device to be used to capture data.</span></span> <span data-ttu-id="2193d-107">Это сообщение можно отправить явно или с помощью макроса [**капсетмЦидевиценаме**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) .</span><span class="sxs-lookup"><span data-stu-id="2193d-107">You can send this message explicitly or by using the [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) macro.</span></span>


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="2193d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2193d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2193d-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="2193d-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="2193d-110">Указатель на строку с завершающим нулем, содержащую имя устройства.</span><span class="sxs-lookup"><span data-stu-id="2193d-110">Pointer to a null-terminated string containing the name of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2193d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2193d-111">Return Value</span></span>

<span data-ttu-id="2193d-112">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2193d-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2193d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2193d-113">Remarks</span></span>

<span data-ttu-id="2193d-114">Это сообщение сохраняет имя устройства MCI во внутренней структуре.</span><span class="sxs-lookup"><span data-stu-id="2193d-114">This message stores the MCI device name in an internal structure.</span></span> <span data-ttu-id="2193d-115">Он не открывает устройство и не обращается к нему.</span><span class="sxs-lookup"><span data-stu-id="2193d-115">It does not open or access the device.</span></span> <span data-ttu-id="2193d-116">Имя устройства по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="2193d-116">The default device name is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2193d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2193d-117">Requirements</span></span>



| <span data-ttu-id="2193d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2193d-118">Requirement</span></span> | <span data-ttu-id="2193d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2193d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2193d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2193d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2193d-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2193d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2193d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2193d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2193d-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2193d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2193d-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2193d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2193d-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2193d-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2193d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2193d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2193d-127">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="2193d-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="2193d-128">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="2193d-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





