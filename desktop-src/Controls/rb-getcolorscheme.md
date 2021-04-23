---
title: Сообщение RB_GETCOLORSCHEME (Коммктрл. h)
description: Извлекает сведения о цветовой схеме из элемента управления главной панели.
ms.assetid: 01f81c4b-bbc9-43ae-a1f5-1e289c6fa278
keywords:
- Элементы управления Windows для RB_GETCOLORSCHEME сообщений
topic_type:
- apiref
api_name:
- RB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d154fd14b93127aa22148f2882f70018225cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534664"
---
# <a name="rb_getcolorscheme-message"></a><span data-ttu-id="48c15-104">\_Сообщение ЖЕТКОЛОРСЧЕМЕ RB</span><span class="sxs-lookup"><span data-stu-id="48c15-104">RB\_GETCOLORSCHEME message</span></span>

<span data-ttu-id="48c15-105">Извлекает сведения о цветовой схеме из элемента управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="48c15-105">Retrieves the color scheme information from the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="48c15-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="48c15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48c15-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48c15-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="48c15-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="48c15-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="48c15-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48c15-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48c15-110">Указатель на структуру [**колорсчеме**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) , которая получит сведения о цветовой схеме.</span><span class="sxs-lookup"><span data-stu-id="48c15-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that will receive the color scheme information.</span></span> <span data-ttu-id="48c15-111">Перед отправкой этого сообщения необходимо задать для элемента **двсизе** этой структуры значение **sizeof**(колорсчеме).</span><span class="sxs-lookup"><span data-stu-id="48c15-111">You must set the **dwSize** member of this structure to **sizeof**(COLORSCHEME) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48c15-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48c15-112">Return value</span></span>

<span data-ttu-id="48c15-113">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="48c15-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="48c15-114">Требования</span><span class="sxs-lookup"><span data-stu-id="48c15-114">Requirements</span></span>



| <span data-ttu-id="48c15-115">Требование</span><span class="sxs-lookup"><span data-stu-id="48c15-115">Requirement</span></span> | <span data-ttu-id="48c15-116">Значение</span><span class="sxs-lookup"><span data-stu-id="48c15-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48c15-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48c15-117">Minimum supported client</span></span><br/> | <span data-ttu-id="48c15-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48c15-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48c15-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48c15-119">Minimum supported server</span></span><br/> | <span data-ttu-id="48c15-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="48c15-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48c15-121">Header</span><span class="sxs-lookup"><span data-stu-id="48c15-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="48c15-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="48c15-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48c15-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48c15-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48c15-124">**\_СЕТКОЛОРСЧЕМЕ RB**</span><span class="sxs-lookup"><span data-stu-id="48c15-124">**RB\_SETCOLORSCHEME**</span></span>](rb-setcolorscheme.md)
</dt> </dl>

 

 





