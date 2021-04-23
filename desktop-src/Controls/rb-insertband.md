---
title: Сообщение RB_INSERTBAND (Коммктрл. h)
description: Вставляет новый полосу в элемент управления главной панели.
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- Элементы управления Windows для RB_INSERTBAND сообщений
topic_type:
- apiref
api_name:
- RB_INSERTBAND
- RB_INSERTBANDA
- RB_INSERTBANDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39b45eb662fb4c2058b87837352339c84762188
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892809"
---
# <a name="rb_insertband-message"></a><span data-ttu-id="30c1a-104">\_Сообщение ИНСЕРТБАНД RB</span><span class="sxs-lookup"><span data-stu-id="30c1a-104">RB\_INSERTBAND message</span></span>

<span data-ttu-id="30c1a-105">Вставляет новый полосу в элемент управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="30c1a-105">Inserts a new band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="30c1a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="30c1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30c1a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30c1a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30c1a-108">Отсчитываемый от нуля индекс расположения, в которое будет вставлен полоса.</span><span class="sxs-lookup"><span data-stu-id="30c1a-108">Zero-based index of the location where the band will be inserted.</span></span> <span data-ttu-id="30c1a-109">Если задать для этого параметра значение-1, элемент управления добавит новую полосу в последнее расположение.</span><span class="sxs-lookup"><span data-stu-id="30c1a-109">If you set this parameter to -1, the control will add the new band at the last location.</span></span>

</dd> <dt>

<span data-ttu-id="30c1a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30c1a-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30c1a-111">Указатель на структуру [**ребарбандинфо**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) , определяющую полосу для вставки.</span><span class="sxs-lookup"><span data-stu-id="30c1a-111">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that defines the band to be inserted.</span></span> <span data-ttu-id="30c1a-112">Перед отправкой этого сообщения необходимо задать для элемента **кбсизе** этой структуры значение **sizeof**(ребарбандинфо).</span><span class="sxs-lookup"><span data-stu-id="30c1a-112">You must set the **cbSize** member of this structure to **sizeof**(REBARBANDINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30c1a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30c1a-113">Return value</span></span>

<span data-ttu-id="30c1a-114">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="30c1a-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="30c1a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="30c1a-115">Requirements</span></span>



| <span data-ttu-id="30c1a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="30c1a-116">Requirement</span></span> | <span data-ttu-id="30c1a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="30c1a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30c1a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30c1a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="30c1a-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30c1a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="30c1a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30c1a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="30c1a-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="30c1a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30c1a-122">Header</span><span class="sxs-lookup"><span data-stu-id="30c1a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="30c1a-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="30c1a-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="30c1a-124">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="30c1a-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="30c1a-125">**RB \_ ИНСЕРТБАНДВ** (Юникод) и **RB \_ инсертбанда** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="30c1a-125">**RB\_INSERTBANDW** (Unicode) and **RB\_INSERTBANDA** (ANSI)</span></span><br/>               |



 

 





