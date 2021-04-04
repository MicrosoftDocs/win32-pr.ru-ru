---
title: Сообщение RB_SIZETORECT (Коммктрл. h)
description: Пытается найти оптимальный макет полос для данного прямоугольника.
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- Элементы управления Windows для RB_SIZETORECT сообщений
topic_type:
- apiref
api_name:
- RB_SIZETORECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3db5727ee8c94d2473b503c9a81b7669bb829a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137614"
---
# <a name="rb_sizetorect-message"></a><span data-ttu-id="0d09a-104">\_Сообщение СИЗЕТОРЕКТ RB</span><span class="sxs-lookup"><span data-stu-id="0d09a-104">RB\_SIZETORECT message</span></span>

<span data-ttu-id="0d09a-105">Пытается найти оптимальный макет полос для данного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="0d09a-105">Attempts to find the best layout of the bands for the given rectangle.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d09a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d09a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d09a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d09a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0d09a-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="0d09a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0d09a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d09a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d09a-110">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , указывающую прямоугольник, в котором должен быть изменен размер элемента управления "Главная панель".</span><span class="sxs-lookup"><span data-stu-id="0d09a-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the rectangle to which the rebar control should be sized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d09a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d09a-111">Return value</span></span>

<span data-ttu-id="0d09a-112">Возвращает ненулевое значение, если произошло изменение макета, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0d09a-112">Returns nonzero if a layout change occurred, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d09a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d09a-113">Remarks</span></span>

<span data-ttu-id="0d09a-114">Полосы главной панели будут упорядочены и упакованы по мере необходимости для размещения прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="0d09a-114">The rebar bands will be arranged and wrapped as necessary to fit the rectangle.</span></span> <span data-ttu-id="0d09a-115">Размеры полос, имеющих стиль РББС вариаблехеигхт, будут изменяться \_ по мере необходимости, чтобы вместить прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="0d09a-115">Bands that have the RBBS\_VARIABLEHEIGHT style will be resized as evenly as possible to fit the rectangle.</span></span> <span data-ttu-id="0d09a-116">Высота горизонтальной главной панели или ширина вертикальной главной панели может измениться в зависимости от нового макета.</span><span class="sxs-lookup"><span data-stu-id="0d09a-116">The height of a horizontal rebar or the width of a vertical rebar may change, depending on the new layout.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d09a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0d09a-117">Requirements</span></span>



| <span data-ttu-id="0d09a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0d09a-118">Requirement</span></span> | <span data-ttu-id="0d09a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0d09a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d09a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d09a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0d09a-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d09a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d09a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d09a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0d09a-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0d09a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d09a-124">Header</span><span class="sxs-lookup"><span data-stu-id="0d09a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d09a-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d09a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

