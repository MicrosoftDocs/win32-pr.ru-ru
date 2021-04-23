---
title: Сообщение PGM_GETPOS (Коммктрл. h)
description: Извлекает текущее расположение прокрутки элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Жетпос пейджера.
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- Элементы управления Windows для PGM_GETPOS сообщений
topic_type:
- apiref
api_name:
- PGM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611a27e9cb952c5be190fa041af3d238f0184b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654572"
---
# <a name="pgm_getpos-message"></a><span data-ttu-id="9697c-105">\_Сообщение ЖЕТПОС PGM</span><span class="sxs-lookup"><span data-stu-id="9697c-105">PGM\_GETPOS message</span></span>

<span data-ttu-id="9697c-106">Извлекает текущее расположение прокрутки элемента управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="9697c-106">Retrieves the current scroll position of the pager control.</span></span> <span data-ttu-id="9697c-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жетпос пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) .</span><span class="sxs-lookup"><span data-stu-id="9697c-107">You can send this message explicitly or use the [**Pager\_GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9697c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9697c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9697c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9697c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9697c-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9697c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9697c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9697c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9697c-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9697c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9697c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9697c-113">Return value</span></span>

<span data-ttu-id="9697c-114">Возвращает значение типа INT, содержащее текущую точку прокрутки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="9697c-114">Returns an INT value that contains the current scroll position, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="9697c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9697c-115">Requirements</span></span>



| <span data-ttu-id="9697c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9697c-116">Requirement</span></span> | <span data-ttu-id="9697c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9697c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9697c-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9697c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9697c-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9697c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9697c-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9697c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9697c-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9697c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9697c-122">Header</span><span class="sxs-lookup"><span data-stu-id="9697c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9697c-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9697c-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





