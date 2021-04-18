---
title: Сообщение RB_SETCOLORSCHEME (Коммктрл. h)
description: Задает сведения о цветовой схеме для элемента управления главной панели.
ms.assetid: ddf8f3e4-66b7-4b53-a04e-b4dd372f71c4
keywords:
- Элементы управления Windows для RB_SETCOLORSCHEME сообщений
topic_type:
- apiref
api_name:
- RB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9c7725d3c0bc3f3a7a7a72db16e19626a3c4d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534349"
---
# <a name="rb_setcolorscheme-message"></a><span data-ttu-id="b79eb-104">\_Сообщение СЕТКОЛОРСЧЕМЕ RB</span><span class="sxs-lookup"><span data-stu-id="b79eb-104">RB\_SETCOLORSCHEME message</span></span>

<span data-ttu-id="b79eb-105">Задает сведения о цветовой схеме для элемента управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="b79eb-105">Sets the color scheme information for the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b79eb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b79eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b79eb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b79eb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b79eb-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b79eb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b79eb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b79eb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b79eb-110">Указатель на структуру [**колорсчеме**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) , содержащую сведения о цветовой схеме.</span><span class="sxs-lookup"><span data-stu-id="b79eb-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that contains the color scheme information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b79eb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b79eb-111">Return value</span></span>

<span data-ttu-id="b79eb-112">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="b79eb-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="b79eb-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b79eb-113">Remarks</span></span>

<span data-ttu-id="b79eb-114">Элемент управления "Главная панель" использует сведения о цветовой схеме при рисовании трехмерных элементов в элементах управления и делений.</span><span class="sxs-lookup"><span data-stu-id="b79eb-114">The rebar control uses the color scheme information when drawing the 3-D elements in the control and bands.</span></span>

## <a name="requirements"></a><span data-ttu-id="b79eb-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b79eb-115">Requirements</span></span>



| <span data-ttu-id="b79eb-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b79eb-116">Requirement</span></span> | <span data-ttu-id="b79eb-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b79eb-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b79eb-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b79eb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b79eb-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b79eb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b79eb-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b79eb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b79eb-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b79eb-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b79eb-122">Header</span><span class="sxs-lookup"><span data-stu-id="b79eb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b79eb-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b79eb-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b79eb-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b79eb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b79eb-125">**\_ЖЕТКОЛОРСЧЕМЕ RB**</span><span class="sxs-lookup"><span data-stu-id="b79eb-125">**RB\_GETCOLORSCHEME**</span></span>](rb-getcolorscheme.md)
</dt> </dl>

 

 





