---
title: Сообщение PGM_GETDROPTARGET (Коммктрл. h)
description: Извлекает указатель интерфейса интерфейс IDropTarget элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Жетдроптаржет пейджера.
ms.assetid: 6b548c30-2d32-4372-90e4-346a27dda218
keywords:
- Элементы управления Windows для PGM_GETDROPTARGET сообщений
topic_type:
- apiref
api_name:
- PGM_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b90f7f9667dd30a79b9345eec211a6ebfcd7a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491790"
---
# <a name="pgm_getdroptarget-message"></a><span data-ttu-id="a47ea-105">\_Сообщение ЖЕТДРОПТАРЖЕТ PGM</span><span class="sxs-lookup"><span data-stu-id="a47ea-105">PGM\_GETDROPTARGET message</span></span>

<span data-ttu-id="a47ea-106">Извлекает указатель интерфейса [**интерфейс IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) элемента управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="a47ea-106">Retrieves a pager control's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface pointer.</span></span> <span data-ttu-id="a47ea-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жетдроптаржет пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="a47ea-107">You can send this message explicitly or use the [**Pager\_GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a47ea-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a47ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a47ea-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a47ea-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a47ea-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a47ea-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a47ea-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a47ea-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a47ea-112">Указатель на указатель [**интерфейс IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) , получающий указатель интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a47ea-112">Pointer to an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pointer that receives the interface pointer.</span></span> <span data-ttu-id="a47ea-113">Вызов метода [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) с этим указателем, когда он больше не нужен, является обязанностью вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="a47ea-113">It is the caller's responsibility to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on this pointer when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a47ea-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a47ea-114">Return value</span></span>

<span data-ttu-id="a47ea-115">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="a47ea-115">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="a47ea-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a47ea-116">Requirements</span></span>



| <span data-ttu-id="a47ea-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a47ea-117">Requirement</span></span> | <span data-ttu-id="a47ea-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a47ea-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a47ea-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a47ea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a47ea-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a47ea-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a47ea-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a47ea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a47ea-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a47ea-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a47ea-123">Header</span><span class="sxs-lookup"><span data-stu-id="a47ea-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a47ea-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a47ea-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

