---
title: Сообщение PBM_SETBKCOLOR (Коммктрл. h)
description: Задает цвет фона на индикаторе выполнения.
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- Элементы управления Windows для PBM_SETBKCOLOR сообщений
topic_type:
- apiref
api_name:
- PBM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfaf84695221cf998275d76a9d2d67773150da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803053"
---
# <a name="pbm_setbkcolor-message"></a><span data-ttu-id="19e05-104">\_Сообщение СЕТБККОЛОР PBM</span><span class="sxs-lookup"><span data-stu-id="19e05-104">PBM\_SETBKCOLOR message</span></span>

<span data-ttu-id="19e05-105">Задает цвет фона на индикаторе выполнения.</span><span class="sxs-lookup"><span data-stu-id="19e05-105">Sets the background color in the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="19e05-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="19e05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19e05-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19e05-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19e05-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="19e05-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="19e05-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19e05-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19e05-110">Значение **COLORREF** , указывающее новый цвет фона.</span><span class="sxs-lookup"><span data-stu-id="19e05-110">**COLORREF** value that specifies the new background color.</span></span> <span data-ttu-id="19e05-111">Укажите \_ значение по умолчанию CLR, чтобы индикатор выполнения использовал цвет фона по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19e05-111">Specify the CLR\_DEFAULT value to cause the progress bar to use its default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19e05-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19e05-112">Return value</span></span>

<span data-ttu-id="19e05-113">Возвращает предыдущий цвет фона или \_ значение по умолчанию CLR, если цвет фона является цветом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19e05-113">Returns the previous background color, or CLR\_DEFAULT if the background color is the default color.</span></span>

## <a name="remarks"></a><span data-ttu-id="19e05-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19e05-114">Remarks</span></span>

<span data-ttu-id="19e05-115">Если стили оформления включены, это сообщение не действует.</span><span class="sxs-lookup"><span data-stu-id="19e05-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="19e05-116">Требования</span><span class="sxs-lookup"><span data-stu-id="19e05-116">Requirements</span></span>



| <span data-ttu-id="19e05-117">Требование</span><span class="sxs-lookup"><span data-stu-id="19e05-117">Requirement</span></span> | <span data-ttu-id="19e05-118">Значение</span><span class="sxs-lookup"><span data-stu-id="19e05-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19e05-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19e05-119">Minimum supported client</span></span><br/> | <span data-ttu-id="19e05-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19e05-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19e05-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19e05-121">Minimum supported server</span></span><br/> | <span data-ttu-id="19e05-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="19e05-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19e05-123">Header</span><span class="sxs-lookup"><span data-stu-id="19e05-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="19e05-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="19e05-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





