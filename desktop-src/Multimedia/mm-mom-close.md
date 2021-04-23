---
title: Сообщение MM_MOM_CLOSE (Ммсистем. h)
description: '\_ \_ При закрытии выходного устройства MIDI в окно отправляется сообщение Close MOM.'
ms.assetid: 4829bbe5-5103-4354-88a7-37def22e926e
keywords:
- MM_MOM_CLOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae55cbca7c5effc146dee0c5ef9be67469a9201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489393"
---
# <a name="mm_mom_close-message"></a><span data-ttu-id="f515e-104">\_Сообщение закрытия MOM (mm) \_</span><span class="sxs-lookup"><span data-stu-id="f515e-104">MM\_MOM\_CLOSE message</span></span>

<span data-ttu-id="f515e-105">При закрытии выходного устройства MIDI в окно отправляется сообщение **\_ \_ Close MOM** .</span><span class="sxs-lookup"><span data-stu-id="f515e-105">The **MM\_MOM\_CLOSE** message is sent to a window when a MIDI output device is closed.</span></span>


```C++
MM_MOM_CLOSE 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="f515e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f515e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f515e-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*хаутпут*</span><span class="sxs-lookup"><span data-stu-id="f515e-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="f515e-108">Обработчик для устройства вывода MIDI.</span><span class="sxs-lookup"><span data-stu-id="f515e-108">Handle to the MIDI output device.</span></span>

</dd> <dt>

<span data-ttu-id="f515e-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="f515e-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f515e-110">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="f515e-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f515e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f515e-111">Return Value</span></span>

<span data-ttu-id="f515e-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f515e-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f515e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f515e-113">Remarks</span></span>

<span data-ttu-id="f515e-114">После отправки этого сообщения маркер устройства больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="f515e-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="f515e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f515e-115">Requirements</span></span>



| <span data-ttu-id="f515e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f515e-116">Requirement</span></span> | <span data-ttu-id="f515e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f515e-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f515e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f515e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f515e-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f515e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f515e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f515e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f515e-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f515e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f515e-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f515e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f515e-123"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f515e-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f515e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f515e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f515e-125">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="f515e-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





