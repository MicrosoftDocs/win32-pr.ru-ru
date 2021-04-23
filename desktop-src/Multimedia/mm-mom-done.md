---
title: Сообщение MM_MOM_DONE (Ммсистем. h)
description: Сообщение о \_ завершении программы mm MOM \_ отправляется в окно при воспроизведении указанного системы или буфера потока MIDI и возвращается приложению.
ms.assetid: 4651d5b4-3c98-4fa7-b761-dafb30e0d31e
keywords:
- MM_MOM_DONE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ad5d4a7e91cc05aa51017cba79418b34445362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071228"
---
# <a name="mm_mom_done-message"></a><span data-ttu-id="1a189-104">\_Сообщение о \_ завершении диспетчера мм</span><span class="sxs-lookup"><span data-stu-id="1a189-104">MM\_MOM\_DONE message</span></span>

<span data-ttu-id="1a189-105">Сообщение **о \_ \_ завершении программы mm MOM** отправляется в окно при воспроизведении указанного системы или буфера потока MIDI и возвращается приложению.</span><span class="sxs-lookup"><span data-stu-id="1a189-105">The **MM\_MOM\_DONE** message is sent to a window when the specified MIDI system-exclusive or stream buffer has been played and is being returned to the application.</span></span>


```C++
MM_MOM_DONE 
wParam = (WPARAM) hOutput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="1a189-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a189-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a189-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*хаутпут*</span><span class="sxs-lookup"><span data-stu-id="1a189-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="1a189-108">Обработчик на устройстве вывода MIDI, который воспроизводил буфер.</span><span class="sxs-lookup"><span data-stu-id="1a189-108">Handle to the MIDI output device that played the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1a189-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*лпмидихдр*</span><span class="sxs-lookup"><span data-stu-id="1a189-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="1a189-110">Указатель на структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , определяющую буфер.</span><span class="sxs-lookup"><span data-stu-id="1a189-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a189-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a189-111">Return Value</span></span>

<span data-ttu-id="1a189-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1a189-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a189-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1a189-113">Requirements</span></span>



| <span data-ttu-id="1a189-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1a189-114">Requirement</span></span> | <span data-ttu-id="1a189-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1a189-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a189-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a189-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1a189-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1a189-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1a189-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a189-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1a189-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1a189-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1a189-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1a189-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a189-121"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a189-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a189-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a189-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a189-123">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="1a189-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

