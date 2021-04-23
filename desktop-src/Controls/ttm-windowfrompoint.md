---
title: Сообщение TTM_WINDOWFROMPOINT (Коммктрл. h)
description: Позволяет процедуре-подкласс отображать текст для окна, отличного от того, под которым находится курсор мыши.
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- Элементы управления Windows для TTM_WINDOWFROMPOINT сообщений
topic_type:
- apiref
api_name:
- TTM_WINDOWFROMPOINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68679f6b6c2477a8279c22f11d0d300e44c8370d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802843"
---
# <a name="ttm_windowfrompoint-message"></a><span data-ttu-id="2d232-104">\_Сообщение ТТМ виндовфромпоинт</span><span class="sxs-lookup"><span data-stu-id="2d232-104">TTM\_WINDOWFROMPOINT message</span></span>

<span data-ttu-id="2d232-105">Позволяет процедуре-подкласс отображать текст для окна, отличного от того, под которым находится курсор мыши.</span><span class="sxs-lookup"><span data-stu-id="2d232-105">Allows a subclass procedure to cause a tooltip to display text for a window other than the one beneath the mouse cursor.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d232-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d232-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d232-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d232-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2d232-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2d232-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2d232-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d232-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d232-110">Указатель на структуру [**точек**](/previous-versions//dd162805(v=vs.85)) , определяющую проверяемую точку.</span><span class="sxs-lookup"><span data-stu-id="2d232-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that defines the point to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d232-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d232-111">Return value</span></span>

<span data-ttu-id="2d232-112">Возвращаемое значение — это маркер окна, содержащего точку, или **значение NULL** , если в указанной точке не существует окна.</span><span class="sxs-lookup"><span data-stu-id="2d232-112">The return value is the handle to the window that contains the point, or **NULL** if no window exists at the specified point.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d232-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d232-113">Remarks</span></span>

<span data-ttu-id="2d232-114">Это сообщение должно быть обработано приложением, которое подклассировать подсказку.</span><span class="sxs-lookup"><span data-stu-id="2d232-114">This message is intended to be processed by an application that subclasses a tooltip.</span></span> <span data-ttu-id="2d232-115">Оно не предназначено для отправки приложением.</span><span class="sxs-lookup"><span data-stu-id="2d232-115">It is not intended to be sent by an application.</span></span> <span data-ttu-id="2d232-116">Перед отображением текста для окна подсказка отправляет это сообщение самому себе.</span><span class="sxs-lookup"><span data-stu-id="2d232-116">A tooltip sends this message to itself before displaying the text for a window.</span></span> <span data-ttu-id="2d232-117">Изменяя координаты точки, заданной параметром *lParam*, процедура подкласса может привести к отображению в подсказке текста для окна, отличного от того, под которым находится курсор мыши.</span><span class="sxs-lookup"><span data-stu-id="2d232-117">By changing the coordinates of the point specified by *lParam*, the subclass procedure can cause the tooltip to display text for a window other than the one beneath the mouse cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d232-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2d232-118">Requirements</span></span>



| <span data-ttu-id="2d232-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2d232-119">Requirement</span></span> | <span data-ttu-id="2d232-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2d232-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d232-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d232-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2d232-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d232-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2d232-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d232-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2d232-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2d232-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d232-125">Header</span><span class="sxs-lookup"><span data-stu-id="2d232-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d232-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d232-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

