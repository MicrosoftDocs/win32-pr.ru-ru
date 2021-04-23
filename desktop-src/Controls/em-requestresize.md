---
title: Сообщение EM_REQUESTRESIZE (RichEdit. h)
description: Заставляет расширенный элемент управления "поле ввода" Отправить \_ код уведомления EN рекуестресизе в его родительское окно.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- Элементы управления Windows для EM_REQUESTRESIZE сообщений
topic_type:
- apiref
api_name:
- EM_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41e7be8e0f30d5c1ec011247f3964292c2218e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262222"
---
# <a name="em_requestresize-message"></a><span data-ttu-id="57a00-104">\_Сообщение РЕКУЕСТРЕСИЗЕ EM</span><span class="sxs-lookup"><span data-stu-id="57a00-104">EM\_REQUESTRESIZE message</span></span>

<span data-ttu-id="57a00-105">Заставляет расширенный элемент управления "поле ввода" отправить код уведомления [**en \_ рекуестресизе**](en-requestresize.md) в его родительское окно.</span><span class="sxs-lookup"><span data-stu-id="57a00-105">Forces a rich edit control to send an [**EN\_REQUESTRESIZE**](en-requestresize.md) notification code to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="57a00-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="57a00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57a00-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57a00-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57a00-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="57a00-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="57a00-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57a00-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57a00-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="57a00-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57a00-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57a00-111">Return value</span></span>

<span data-ttu-id="57a00-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="57a00-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57a00-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="57a00-113">Remarks</span></span>

<span data-ttu-id="57a00-114">Это сообщение полезно при обработке [**\_ размера WM**](/windows/desktop/winmsg/wm-size) для родителя элемента управления неформатированного редактирования самого нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="57a00-114">This message is useful during [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) processing for the parent of a bottomless rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="57a00-115">Требования</span><span class="sxs-lookup"><span data-stu-id="57a00-115">Requirements</span></span>



| <span data-ttu-id="57a00-116">Требование</span><span class="sxs-lookup"><span data-stu-id="57a00-116">Requirement</span></span> | <span data-ttu-id="57a00-117">Значение</span><span class="sxs-lookup"><span data-stu-id="57a00-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57a00-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57a00-118">Minimum supported client</span></span><br/> | <span data-ttu-id="57a00-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="57a00-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57a00-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57a00-120">Minimum supported server</span></span><br/> | <span data-ttu-id="57a00-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="57a00-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57a00-122">Header</span><span class="sxs-lookup"><span data-stu-id="57a00-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="57a00-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="57a00-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57a00-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57a00-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="57a00-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="57a00-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="57a00-126">**EN \_ рекуестресизе**</span><span class="sxs-lookup"><span data-stu-id="57a00-126">**EN\_REQUESTRESIZE**</span></span>](en-requestresize.md)
</dt> <dt>

<span data-ttu-id="57a00-127">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="57a00-127">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="57a00-128">**\_Размер WM**</span><span class="sxs-lookup"><span data-stu-id="57a00-128">**WM\_SIZE**</span></span>](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

