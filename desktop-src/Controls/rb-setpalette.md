---
title: Сообщение RB_SETPALETTE (Коммктрл. h)
description: Задает текущую палитру элемента управления главной панели.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- Элементы управления Windows для RB_SETPALETTE сообщений
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ee47985c05bcd8a857620e7fe501bddf53bdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988984"
---
# <a name="rb_setpalette-message"></a><span data-ttu-id="fc1b2-104">\_Сообщение СЕТПАЛЕТТЕ RB</span><span class="sxs-lookup"><span data-stu-id="fc1b2-104">RB\_SETPALETTE message</span></span>

<span data-ttu-id="fc1b2-105">Задает текущую палитру элемента управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="fc1b2-105">Sets the rebar control's current palette.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc1b2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc1b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc1b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc1b2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fc1b2-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="fc1b2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fc1b2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc1b2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc1b2-110">Объект **хпалетте** , указывающий новую палитру, которую будет использовать элемент управления "Главная панель".</span><span class="sxs-lookup"><span data-stu-id="fc1b2-110">An **HPALETTE** that specifies the new palette that the rebar control will use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc1b2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc1b2-111">Return value</span></span>

<span data-ttu-id="fc1b2-112">Возвращает объект **хпалетте** , указывающий предыдущую палитру элемента управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="fc1b2-112">Returns an **HPALETTE** that specifies the rebar control's previous palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc1b2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc1b2-113">Remarks</span></span>

<span data-ttu-id="fc1b2-114">Приложение, отправляющее это сообщение, отвечает за удаление **хпалетте** , переданных в этом сообщении (см. [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)).</span><span class="sxs-lookup"><span data-stu-id="fc1b2-114">It is the responsibility of the application sending this message to delete the **HPALETTE** passed in this message (see [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)).</span></span> <span data-ttu-id="fc1b2-115">Элемент управления "Главная панель" не удалит набор **хпалетте** с этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="fc1b2-115">The rebar control will not delete an **HPALETTE** set with this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc1b2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fc1b2-116">Requirements</span></span>



| <span data-ttu-id="fc1b2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fc1b2-117">Requirement</span></span> | <span data-ttu-id="fc1b2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fc1b2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc1b2-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc1b2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fc1b2-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc1b2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fc1b2-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc1b2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fc1b2-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fc1b2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc1b2-123">Header</span><span class="sxs-lookup"><span data-stu-id="fc1b2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc1b2-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc1b2-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc1b2-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc1b2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc1b2-126">**панель \_ RB**</span><span class="sxs-lookup"><span data-stu-id="fc1b2-126">**RB\_GETPALETTE**</span></span>](rb-getpalette.md)
</dt> </dl>

 

