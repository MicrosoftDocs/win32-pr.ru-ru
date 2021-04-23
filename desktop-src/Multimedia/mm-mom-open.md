---
title: Сообщение MM_MOM_OPEN (Ммсистем. h)
description: Сообщение о \_ открытом формате mm MOM \_ отправляется в окно при открытии выходного устройства MIDI.
ms.assetid: 1374a07c-02fa-4b43-82df-cbd96302aec5
keywords:
- MM_MOM_OPEN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f676dccf532290ab2153b888c20fad7b19d98d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488970"
---
# <a name="mm_mom_open-message"></a><span data-ttu-id="7ac40-104">\_Открытое сообщение для MOM (mm) \_</span><span class="sxs-lookup"><span data-stu-id="7ac40-104">MM\_MOM\_OPEN message</span></span>

<span data-ttu-id="7ac40-105">Сообщение **о \_ \_ открытом формате mm MOM** отправляется в окно при открытии выходного устройства MIDI.</span><span class="sxs-lookup"><span data-stu-id="7ac40-105">The **MM\_MOM\_OPEN** message is sent to a window when a MIDI output device is opened.</span></span>


```C++
MM_MOM_OPEN 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="7ac40-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ac40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ac40-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*хаутпут*</span><span class="sxs-lookup"><span data-stu-id="7ac40-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="7ac40-108">Обработчик для устройства вывода MIDI.</span><span class="sxs-lookup"><span data-stu-id="7ac40-108">Handle to the MIDI output device.</span></span>

</dd> <dt>

<span data-ttu-id="7ac40-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ac40-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="7ac40-110">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="7ac40-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ac40-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ac40-111">Return Value</span></span>

<span data-ttu-id="7ac40-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7ac40-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ac40-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7ac40-113">Requirements</span></span>



| <span data-ttu-id="7ac40-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7ac40-114">Requirement</span></span> | <span data-ttu-id="7ac40-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7ac40-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac40-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ac40-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7ac40-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7ac40-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7ac40-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ac40-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7ac40-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7ac40-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7ac40-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7ac40-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ac40-121"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ac40-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ac40-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ac40-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ac40-123">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="7ac40-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





