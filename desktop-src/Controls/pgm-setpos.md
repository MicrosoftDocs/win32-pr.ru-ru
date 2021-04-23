---
title: Сообщение PGM_SETPOS (Коммктрл. h)
description: Задает текущую точку прокрутки для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Сетпос пейджера.
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- Элементы управления Windows для PGM_SETPOS сообщений
topic_type:
- apiref
api_name:
- PGM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5af4497e97a8263fa9ec8e454d367bb57e830c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802068"
---
# <a name="pgm_setpos-message"></a><span data-ttu-id="a6e85-105">\_Сообщение СЕТПОС PGM</span><span class="sxs-lookup"><span data-stu-id="a6e85-105">PGM\_SETPOS message</span></span>

<span data-ttu-id="a6e85-106">Задает текущую точку прокрутки для элемента управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="a6e85-106">Sets the current scroll position for the pager control.</span></span> <span data-ttu-id="a6e85-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ сетпос пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) .</span><span class="sxs-lookup"><span data-stu-id="a6e85-107">You can send this message explicitly or use the [**Pager\_SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a6e85-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6e85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6e85-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6e85-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a6e85-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a6e85-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a6e85-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6e85-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6e85-112">Значение типа **int** , содержащее новую точку прокрутки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="a6e85-112">Value of type **int** that contains the new scroll position, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6e85-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6e85-113">Return value</span></span>

<span data-ttu-id="a6e85-114">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="a6e85-114">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6e85-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a6e85-115">Requirements</span></span>



| <span data-ttu-id="a6e85-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a6e85-116">Requirement</span></span> | <span data-ttu-id="a6e85-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a6e85-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6e85-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6e85-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a6e85-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6e85-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6e85-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6e85-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a6e85-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a6e85-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6e85-122">Header</span><span class="sxs-lookup"><span data-stu-id="a6e85-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6e85-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6e85-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





