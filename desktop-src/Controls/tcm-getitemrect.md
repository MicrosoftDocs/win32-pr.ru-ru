---
title: Сообщение TCM_GETITEMRECT (Коммктрл. h)
description: Извлекает ограничивающий прямоугольник для вкладки в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл жетитемрект.
ms.assetid: 6abd8cdf-5f19-4b7e-800e-970097bc891b
keywords:
- Элементы управления Windows для TCM_GETITEMRECT сообщений
topic_type:
- apiref
api_name:
- TCM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa6c214efbeeaf58d1ff3def9f50f10011b41dfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892533"
---
# <a name="tcm_getitemrect-message"></a><span data-ttu-id="d0813-105">\_Сообщение ЖЕТИТЕМРЕКТ TCM</span><span class="sxs-lookup"><span data-stu-id="d0813-105">TCM\_GETITEMRECT message</span></span>

<span data-ttu-id="d0813-106">Извлекает ограничивающий прямоугольник для вкладки в элементе управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="d0813-106">Retrieves the bounding rectangle for a tab in a tab control.</span></span> <span data-ttu-id="d0813-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ жетитемрект**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="d0813-107">You can send this message explicitly or by using the [**TabCtrl\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0813-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0813-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0813-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0813-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0813-110">Индекс вкладки.</span><span class="sxs-lookup"><span data-stu-id="d0813-110">Index of the tab.</span></span>

</dd> <dt>

<span data-ttu-id="d0813-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0813-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0813-112">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая получает ограничивающий прямоугольник вкладки в координатах окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="d0813-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle of the tab, in viewport coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0813-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0813-113">Return value</span></span>

<span data-ttu-id="d0813-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d0813-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0813-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d0813-115">Requirements</span></span>



| <span data-ttu-id="d0813-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d0813-116">Requirement</span></span> | <span data-ttu-id="d0813-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d0813-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0813-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0813-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d0813-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0813-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0813-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0813-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d0813-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d0813-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0813-122">Header</span><span class="sxs-lookup"><span data-stu-id="d0813-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0813-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0813-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

