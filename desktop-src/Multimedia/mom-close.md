---
title: Сообщение MOM_CLOSE (Ммсистем. h)
description: '\_Сообщение закрытия MOM отправляется в функцию обратного вызова MIDI OUTPUT при закрытии выходного устройства MIDI.'
ms.assetid: 229b3701-16f1-4ec8-920e-cd8231561541
keywords:
- MOM_CLOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68f173daa2fb104305979a72c9a14106175d7d20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989273"
---
# <a name="mom_close-message"></a><span data-ttu-id="12338-104">\_Сообщение закрытия MOM</span><span class="sxs-lookup"><span data-stu-id="12338-104">MOM\_CLOSE message</span></span>

<span data-ttu-id="12338-105">Сообщение **\_ закрытия MOM** отправляется в функцию обратного вызова MIDI OUTPUT при закрытии выходного устройства MIDI.</span><span class="sxs-lookup"><span data-stu-id="12338-105">The **MOM\_CLOSE** message is sent to a MIDI output callback function when a MIDI output device is closed.</span></span>


```C++
MOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="12338-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="12338-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12338-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="12338-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="12338-108">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="12338-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="12338-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="12338-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="12338-110">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="12338-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12338-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12338-111">Return Value</span></span>

<span data-ttu-id="12338-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="12338-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12338-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12338-113">Remarks</span></span>

<span data-ttu-id="12338-114">После отправки этого сообщения маркер устройства больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="12338-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="12338-115">Требования</span><span class="sxs-lookup"><span data-stu-id="12338-115">Requirements</span></span>



| <span data-ttu-id="12338-116">Требование</span><span class="sxs-lookup"><span data-stu-id="12338-116">Requirement</span></span> | <span data-ttu-id="12338-117">Значение</span><span class="sxs-lookup"><span data-stu-id="12338-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12338-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12338-118">Minimum supported client</span></span><br/> | <span data-ttu-id="12338-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="12338-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="12338-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12338-120">Minimum supported server</span></span><br/> | <span data-ttu-id="12338-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="12338-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="12338-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="12338-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="12338-123"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12338-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12338-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12338-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12338-125">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="12338-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





