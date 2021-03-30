---
title: Сообщение MOM_OPEN (Ммсистем. h)
description: Сообщение о \_ открытом вызове MOM отправляется в функцию обратного вызова MIDI OUTPUT при открытии выходного устройства MIDI.
ms.assetid: f3360482-7d16-419c-b5d1-0dd3a6e3c690
keywords:
- MOM_OPEN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24072aad6bff9ce192460c2c8525da4506f32746
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803671"
---
# <a name="mom_open-message"></a><span data-ttu-id="60f44-104">\_Открытое сообщение MOM</span><span class="sxs-lookup"><span data-stu-id="60f44-104">MOM\_OPEN message</span></span>

<span data-ttu-id="60f44-105">Сообщение **о \_ открытом** вызове MOM отправляется в функцию обратного вызова MIDI OUTPUT при открытии выходного устройства MIDI.</span><span class="sxs-lookup"><span data-stu-id="60f44-105">The **MOM\_OPEN** message is sent to a MIDI output callback function when a MIDI output device is opened.</span></span>


```C++
MOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="60f44-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="60f44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60f44-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="60f44-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="60f44-108">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="60f44-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="60f44-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="60f44-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="60f44-110">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="60f44-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60f44-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60f44-111">Return Value</span></span>

<span data-ttu-id="60f44-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="60f44-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="60f44-113">Требования</span><span class="sxs-lookup"><span data-stu-id="60f44-113">Requirements</span></span>



| <span data-ttu-id="60f44-114">Требование</span><span class="sxs-lookup"><span data-stu-id="60f44-114">Requirement</span></span> | <span data-ttu-id="60f44-115">Значение</span><span class="sxs-lookup"><span data-stu-id="60f44-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60f44-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60f44-116">Minimum supported client</span></span><br/> | <span data-ttu-id="60f44-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="60f44-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="60f44-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60f44-118">Minimum supported server</span></span><br/> | <span data-ttu-id="60f44-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="60f44-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="60f44-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="60f44-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="60f44-121"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60f44-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60f44-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60f44-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60f44-123">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="60f44-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





