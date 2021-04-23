---
title: Сообщение MOM_DONE (МЦиапи. h)
description: Сообщение «MOM \_ done» отправляется в функцию обратного вызова MIDI Output, когда заданный системный или потоковый буфер воспроизводится и возвращается приложению.
ms.assetid: 0b9bd0e1-c87d-4f21-912e-5ac9f5c04192
keywords:
- MOM_DONE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MOM_DONE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af3f58f7d8f4625971dde5d7ec807c9f963d40f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415269"
---
# <a name="mom_done-message"></a><span data-ttu-id="4829a-104">\_Сообщение о завершении MOM</span><span class="sxs-lookup"><span data-stu-id="4829a-104">MOM\_DONE message</span></span>

<span data-ttu-id="4829a-105">Сообщение « **MOM \_ done** » отправляется в функцию обратного вызова MIDI Output, когда заданный системный или потоковый буфер воспроизводится и возвращается приложению.</span><span class="sxs-lookup"><span data-stu-id="4829a-105">The **MOM\_DONE** message is sent to a MIDI output callback function when the specified system-exclusive or stream buffer has been played and is being returned to the application.</span></span>


```C++
MOM_DONE 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="4829a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4829a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4829a-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*лпмидихдр*</span><span class="sxs-lookup"><span data-stu-id="4829a-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="4829a-108">Указатель на структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , определяющую буфер.</span><span class="sxs-lookup"><span data-stu-id="4829a-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="4829a-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="4829a-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="4829a-110">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="4829a-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4829a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4829a-111">Return Value</span></span>

<span data-ttu-id="4829a-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4829a-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4829a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4829a-113">Requirements</span></span>



| <span data-ttu-id="4829a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4829a-114">Requirement</span></span> | <span data-ttu-id="4829a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4829a-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4829a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4829a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4829a-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4829a-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4829a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4829a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4829a-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4829a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4829a-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4829a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4829a-121"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="4829a-121"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4829a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4829a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4829a-123">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="4829a-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

