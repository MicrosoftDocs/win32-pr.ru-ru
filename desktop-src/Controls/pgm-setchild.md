---
title: Сообщение PGM_SETCHILD (Коммктрл. h)
description: Задает вложенное окно для элемента управления страничного навигатора.
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- Элементы управления Windows для PGM_SETCHILD сообщений
topic_type:
- apiref
api_name:
- PGM_SETCHILD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c934c3c5688ac79b5c5ce67aef68e28ad3627ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135710"
---
# <a name="pgm_setchild-message"></a><span data-ttu-id="3174b-104">\_Сообщение СЕТЧИЛД PGM</span><span class="sxs-lookup"><span data-stu-id="3174b-104">PGM\_SETCHILD message</span></span>

<span data-ttu-id="3174b-105">Задает вложенное окно для элемента управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="3174b-105">Sets the contained window for the pager control.</span></span> <span data-ttu-id="3174b-106">Это сообщение не изменит родителя автономного окна. Он назначает только обработчику окна страничного навигатора для прокрутки.</span><span class="sxs-lookup"><span data-stu-id="3174b-106">This message will not change the parent of the contained window; it only assigns a window handle to the pager control for scrolling.</span></span> <span data-ttu-id="3174b-107">В большинстве случаев вложенное окно будет дочерним.</span><span class="sxs-lookup"><span data-stu-id="3174b-107">In most cases, the contained window will be a child window.</span></span> <span data-ttu-id="3174b-108">В этом случае вложенное окно должно быть дочерним элементом элемента управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="3174b-108">If this is the case, the contained window should be a child of the pager control.</span></span> <span data-ttu-id="3174b-109">Это сообщение можно отправить явным образом или использовать макрос [**\_ сетчилд пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) .</span><span class="sxs-lookup"><span data-stu-id="3174b-109">You can send this message explicitly or use the [**Pager\_SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3174b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3174b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3174b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3174b-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3174b-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3174b-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3174b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3174b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3174b-114">Обработчик для содержащегося в нем окна.</span><span class="sxs-lookup"><span data-stu-id="3174b-114">Handle to the window to be contained.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3174b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3174b-115">Return value</span></span>

<span data-ttu-id="3174b-116">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="3174b-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3174b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3174b-117">Requirements</span></span>



| <span data-ttu-id="3174b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3174b-118">Requirement</span></span> | <span data-ttu-id="3174b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3174b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3174b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3174b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3174b-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3174b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3174b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3174b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3174b-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3174b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3174b-124">Header</span><span class="sxs-lookup"><span data-stu-id="3174b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3174b-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3174b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





